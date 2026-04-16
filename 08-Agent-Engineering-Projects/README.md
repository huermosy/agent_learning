# Agent 工程实战

## 模块简介
本模块将前面所有能力串联起来，从 demo 走向工程化项目，形成完整的 Agent 开发工程师能力闭环。

## 你将学到
- 从需求到架构设计
- 从原型到可维护工程
- 与 RAG、工具系统、评估体系集成
- 面向真实业务的 Agent 项目拆解方式

## 推荐学习顺序
1. **agency-agents**：最适合先学。它更像一个面向业务协作与角色分工的 Agent 工程样板，方便先建立“一个 Agent 项目如何组织”的整体认知。
2. **hermes-agent**：第二个学。它更贴近真实代码实现，适合继续拆解 runtime、CLI、plugin、state 与测试结构。
3. **gemini-cli**：最后学。它工程规模更大、模块更多，适合在你已经熟悉前两个项目后再读，重点看成熟 CLI Agent 工程如何组织。

## 三个仓库的学习入口

### 1. agency-agents
- 仓库位置：[`./agency-agents`](./agency-agents)
- 适合阶段：工程视角入门
- 推荐先看：
  - [`agency-agents/README.md`](./agency-agents/README.md)
  - [`agency-agents/product`](./agency-agents/product)
  - [`agency-agents/engineering`](./agency-agents/engineering)
  - [`agency-agents/project-management`](./agency-agents/project-management)
  - [`agency-agents/examples`](./agency-agents/examples)
- 学习重点：
  - 理解一个 Agent 项目如何围绕业务目标组织角色与模块
  - 看产品、工程、项目管理材料如何共同支撑交付
  - 先建立“工程化 Agent 项目”的全局地图

### 2. hermes-agent
- 仓库位置：[`./hermes-agent`](./hermes-agent)
- 适合阶段：实现层拆解
- 推荐先看：
  - [`hermes-agent/README.md`](./hermes-agent/README.md)
  - [`hermes-agent/agent`](./hermes-agent/agent)
  - [`hermes-agent/hermes_cli`](./hermes-agent/hermes_cli)
  - [`hermes-agent/plugins`](./hermes-agent/plugins)
  - [`hermes-agent/tests`](./hermes-agent/tests)
- 学习重点：
  - 关注 agent runtime、CLI 入口与插件扩展方式
  - 看状态管理、命令执行与测试结构如何协同
  - 理解从原型走向可维护工程需要哪些模块边界

### 3. gemini-cli
- 仓库位置：[`./gemini-cli`](./gemini-cli)
- 适合阶段：大型 CLI Agent 工程观察
- 推荐先看：
  - [`gemini-cli/README.md`](./gemini-cli/README.md)
  - [`gemini-cli/packages`](./gemini-cli/packages)
  - [`gemini-cli/integration-tests`](./gemini-cli/integration-tests)
  - [`gemini-cli/memory-tests`](./gemini-cli/memory-tests)
  - [`gemini-cli/perf-tests`](./gemini-cli/perf-tests)
- 学习重点：
  - 观察大型 CLI Agent 工程如何拆分 packages、测试与性能模块
  - 理解成熟项目在集成测试、记忆测试、性能测试上的投入
  - 当前仓库在 Windows 下存在长路径 checkout 不完整问题，阅读时优先看已落地目录与可访问文件

## 建议学习方法
- 第 1 轮：只看 README 和顶层目录，先判断每个项目解决什么工程问题
- 第 2 轮：先读 `agency-agents` 建立全局图，再读 `hermes-agent` 看实现主线
- 第 3 轮：最后再拆 `gemini-cli`，重点关注 packages、tests 和 CLI 组织方式
- 每读完一个仓库，补一份自己的“模块图 + 数据流 + 扩展点”笔记

## 学习导航
- 学习路线：[`md/learning-roadmap.md`](./md/learning-roadmap.md)
- 术语表：[`md/glossary.md`](./md/glossary.md)
- 实践项目：[`md/practice-projects.md`](./md/practice-projects.md)
- 面试题：[`md/interview-questions.md`](./md/interview-questions.md)
- 学习清单：[`md/checklist.md`](./md/checklist.md)
- 返回总目录：[`../README.md`](../README.md)
