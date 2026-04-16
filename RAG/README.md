# RAG 学习模块

## 模块简介
本模块聚焦检索增强生成（RAG）的核心理论与工程实践，帮助你建立从知识库构建、检索召回、重排到生成增强的完整认知，并理解 RAG 如何与 Agent 系统协同工作。

## 你将学到
- RAG 的基本组成与工作流程
- 文档切分、向量化、召回与重排
- 检索质量、生成质量与系统评估
- Agent + RAG 组合系统的设计思路

## 推荐学习顺序
1. **hello-agents**：最适合先学。它是系统化中文教程，覆盖 Agent 基础、框架实践、记忆与检索、上下文工程与评估，适合先建立完整认知框架。
2. **claude-mem**：第二个学。它更偏真实工程实现，重点看持久记忆、检索、向量搜索、hook 流程和 worker 架构，适合把前面的概念落到可运行系统上。
3. **ruflo**：最后学。它规模最大、概念最密，偏多智能体编排与平台化能力，适合在你已经熟悉 Agent + Memory/RAG 基础后再拆解。

## 三个仓库的学习入口

### 1. hello-agents
- 仓库位置：[`./hello-agents`](./hello-agents)
- 适合阶段：入门到进阶
- 推荐先看：
  - [`hello-agents/README.md`](./hello-agents/README.md)
  - [`hello-agents/docs/chapter1/第一章 初识智能体.md`](./hello-agents/docs/chapter1/%E7%AC%AC%E4%B8%80%E7%AB%A0%20%E5%88%9D%E8%AF%86%E6%99%BA%E8%83%BD%E4%BD%93.md)
  - [`hello-agents/docs/chapter8/第八章 记忆与检索.md`](./hello-agents/docs/chapter8/%E7%AC%AC%E5%85%AB%E7%AB%A0%20%E8%AE%B0%E5%BF%86%E4%B8%8E%E6%A3%80%E7%B4%A2.md)
  - [`hello-agents/code`](./hello-agents/code)
- 学习重点：
  - 先建立 Agent 与 RAG 的全局地图
  - 理解“记忆、检索、上下文工程、评估”在系统中的角色
  - 配合 `code/` 目录做章节式实践

### 2. claude-mem
- 仓库位置：[`./claude-mem`](./claude-mem)
- 适合阶段：工程实现拆解
- 推荐先看：
  - [`claude-mem/README.md`](./claude-mem/README.md)
  - [`claude-mem/CLAUDE.md`](./claude-mem/CLAUDE.md)
  - [`claude-mem/src/hooks`](./claude-mem/src/hooks)
  - [`claude-mem/src/services`](./claude-mem/src/services)
  - [`claude-mem/plugin/skills/mem-search`](./claude-mem/plugin/skills/mem-search)
- 学习重点：
  - hook 如何采集上下文并写入记忆系统
  - worker service、SQLite、Chroma 如何协同形成检索链路
  - memory search 如何服务后续会话与 Agent 工作流

### 3. ruflo
- 仓库位置：[`./ruflo`](./ruflo)
- 适合阶段：高级编排与平台化
- 推荐先看：
  - [`ruflo/README.md`](./ruflo/README.md)
  - [`ruflo/CLAUDE.md`](./ruflo/CLAUDE.md)
  - [`ruflo/v3`](./ruflo/v3)
  - [`ruflo/plugin`](./ruflo/plugin)
  - [`ruflo/tests`](./ruflo/tests)
- 学习重点：
  - 多智能体编排、记忆、路由、工具系统如何组合成平台
  - 理解大规模 Agent orchestration 与 RAG/Memory 的关系
  - 重点看 v3 架构，而不是一开始就试图全部读完

## 建议学习方法
- 第 1 轮：只读 README 和目录结构，建立全局地图
- 第 2 轮：优先精读 `hello-agents` 的相关章节，再对照 `claude-mem` 的实现
- 第 3 轮：最后再进入 `ruflo`，只抓主线：路由、记忆、agent coordination、plugin/MCP
- 每读完一个仓库，补一份自己的“系统图 + 数据流 + 核心模块”笔记

## 学习导航
- 学习路线：[`md/learning-roadmap.md`](./md/learning-roadmap.md)
- 术语表：[`md/glossary.md`](./md/glossary.md)
- 实践项目：[`md/practice-projects.md`](./md/practice-projects.md)
- 面试题：[`md/interview-questions.md`](./md/interview-questions.md)
- 学习清单：[`md/checklist.md`](./md/checklist.md)
- 返回总目录：[`../README.md`](../README.md)
