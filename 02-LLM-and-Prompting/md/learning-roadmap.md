# LLM 与 Prompt 工程学习路线

## 1. 学习目标
掌握 Agent 的模型层能力，让输出更稳定、结构更清晰、推理更可控。

## 2. 核心知识点
- Prompt 基本结构：角色、任务、约束、输出格式
- Few-shot / Zero-shot / Chain-of-Thought
- 上下文管理与窗口限制
- 结构化输出：JSON / Schema
- 系统提示词与用户提示词分层

## 3. 学习顺序
### 阶段一：Prompt 基础
- 好 Prompt 的组成
- 常见失败模式
- 降低歧义的方法

### 阶段二：输出控制
- 结构化响应
- 工具调用前的参数约束
- 结果格式校验

### 阶段三：推理增强
- Planning Prompt
- Reflection Prompt
- 多轮上下文压缩

## 4. 建议产出
- 编写一组可复用 Prompt 模板
- 设计一个 JSON 输出规范示例
- 对比不同 Prompt 写法的效果差异

## 5. 进阶衔接
完成后进入：`../03-Tool-Use-and-Workflow/README.md`
