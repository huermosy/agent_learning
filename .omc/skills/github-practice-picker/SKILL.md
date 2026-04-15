---
name: github-practice-picker
description: 按主题查找过去一年内 GitHub 高星学习项目，适合作为 Agent 学习实战入口。
argument-hint: "<topic>[:count]，例如：RAG:3"
triggers:
  - github-practice-picker
  - github practice
  - github 项目推荐
  - GitHub 高星项目
---

# GitHub Practice Picker

当调用这个 skill 时，不要复述本文件内容，直接执行查询并把结果返回给用户。

## 执行指令

1. 读取 `ARGUMENTS`，参数格式为 `<topic>[:count]`，例如：`RAG:3`
2. 如果 `ARGUMENTS` 为空，默认使用 `RAG:3`
3. 运行下面这段本地 Python 脚本，并直接把输出返回给用户
4. 只有在查询失败时，才输出错误提示，不要额外解释整个 skill 文档

```bash
python - <<'PY'
from datetime import date, timedelta
import io
import json
import subprocess
import sys

sys.stdout = io.TextIOWrapper(sys.stdout.buffer, encoding="utf-8", errors="replace")

raw = "{{ARGUMENTS}}".strip()
if not raw:
    raw = "RAG:3"

parts = raw.split(':', 1)
topic = parts[0].strip()
count = 3
if len(parts) > 1:
    try:
        parsed = int(parts[1].strip())
        if parsed > 0:
            count = min(parsed, 10)
    except Exception:
        count = 3

if not topic:
    print("请提供主题，例如：/github-practice-picker RAG:3")
    sys.exit(0)

since = (date.today() - timedelta(days=365)).isoformat()
query = f"{topic} created:>={since}"
cmd = [
    "gh", "api", "search/repositories",
    "--method", "GET",
    "-F", f"q={query}",
    "-F", "sort=stars",
    "-F", "order=desc",
    "-F", f"per_page={count}",
]

try:
    result = subprocess.run(
        cmd,
        capture_output=True,
        text=True,
        encoding="utf-8",
        errors="replace",
        check=True,
    )
except subprocess.CalledProcessError as e:
    message = (e.stderr or e.stdout or "").strip()
    lower = message.lower()
    if "auth" in lower or "login" in lower or "gh auth login" in lower:
        print("GitHub CLI 尚未登录，请先执行：! gh auth login")
    else:
        print("GitHub 查询失败。")
        if message:
            print(message)
    sys.exit(0)
except FileNotFoundError:
    print("未检测到 gh CLI，请先安装 GitHub CLI。")
    sys.exit(0)

payload = json.loads(result.stdout)
items = payload.get("items", [])

print(f"GitHub Practice Picks: {topic}")
print(f"筛选条件：过去一年 / 按 stars 排序 / 返回 {count} 个")
print()

if not items:
    print("没有找到结果，建议尝试更宽泛的主题关键词。")
    sys.exit(0)

for idx, repo in enumerate(items[:count], start=1):
    name = repo.get("full_name", "unknown")
    url = repo.get("html_url", "")
    stars = repo.get("stargazers_count", 0)
    created = repo.get("created_at", "")[:10]
    updated = repo.get("updated_at", "")[:10]
    desc = (repo.get("description") or "暂无描述").strip()
    reason = f"主题匹配“{topic}”，且近一年创建并获得较高关注，适合拆解 README、docs、examples 与工程结构。"

    print(f"{idx}. {name}")
    print(f"   URL: {url}")
    print(f"   Stars: {stars}")
    print(f"   Created: {created}")
    print(f"   Updated: {updated}")
    print(f"   Description: {desc}")
    print(f"   Why learn: {reason}")
    print()

print("建议先从 README、docs、examples、src 或 app 目录入手，优先理解项目目标、数据流和核心模块边界。")
PY
```

## 参数规则

- `topic` 是主题关键词，如：`RAG`、`multi-agent`、`eval`
- `count` 是返回数量，默认 `3`
- 如果 `count` 非法、为空、或小于 1，则回退为 `3`
- 为避免输出过长，最大返回 `10` 个结果

## 输出要求

输出格式应保持简洁，至少包含：
- repo 名
- GitHub URL
- star 数
- 创建时间
- 更新时间
- 仓库描述
- 一句简短学习理由

## 规则

- 不要复述整个 skill 文档
- 直接执行命令并返回结果
- 只负责发现项目，不自动 clone、fork 或修改学习目录
- 若 `gh` 未登录，提示用户执行 `! gh auth login`
- 若没有结果，提示用户更换更宽泛的关键词
