# Agent 开发学习总目录

> 目标：围绕 Agent 开发工程师核心能力构建系统化学习路径。当前以 Markdown 学习工程为主，后续可平滑扩展为交互式网页通关指南。

## 学习目标
- 理解 Agent 系统的核心组成：模型、提示词、工具、记忆、规划、执行、评估、安全。
- 能独立设计单 Agent 与多 Agent 工作流。
- 能构建可评测、可观察、可迭代优化的 Agent 应用。
- 能把 RAG 与 Agent 能力组合为完整系统。

## 推荐学习顺序
1. [01-Agent-Foundation](./01-Agent-Foundation/README.md)
2. [02-LLM-and-Prompting](./02-LLM-and-Prompting/README.md)
3. [03-Tool-Use-and-Workflow](./03-Tool-Use-and-Workflow/README.md)
4. [04-Memory-and-Planning](./04-Memory-and-Planning/README.md)
5. [RAG](./RAG/README.md)
6. [05-Multi-Agent-Systems](./05-Multi-Agent-Systems/README.md)
7. [06-Evaluation-and-Observability](./06-Evaluation-and-Observability/README.md)
8. [07-Agent-Safety-and-Guardrails](./07-Agent-Safety-and-Guardrails/README.md)
9. [08-Agent-Engineering-Projects](./08-Agent-Engineering-Projects/README.md)

## 能力地图
- 基础认知：Agent 定义、运行时结构、常见模式
- 模型能力：Prompt、上下文、结构化输出、推理控制
- 工具调用：Function Calling、环境交互、工作流编排
- 记忆规划：短期记忆、长期记忆、任务分解、计划执行
- 检索增强：RAG、知识库、召回与重排、Agent + RAG
- 多体协作：角色分工、路由、监督、并发执行
- 评估运维：离线评测、在线观测、日志与追踪
- 安全治理：权限、注入防护、边界控制、审计
- 项目实战：从 demo 到可扩展工程

## 目录规范
每个模块包含：
- `README.md`：模块简介、适用人群、导航入口
- `md/learning-roadmap.md`：该模块的详细学习路线
- `md/glossary.md`：核心术语与易混淆概念
- `md/practice-projects.md`：分层实践项目与验收标准
- `md/interview-questions.md`：基础题、场景题、开放题
- `md/checklist.md`：学习完成标准与自测清单

## 后续扩展建议
- 当前已具备：模块简介、学习路线、术语表、实践项目、面试题、学习清单
- 下一步可补充：示例代码、练习题详解、标准答案、案例拆解
- 统一元数据格式，后续可直接渲染为网页
- 增加 `assets/`、`examples/`、`checkpoints/` 子目录以支持闯关式学习
