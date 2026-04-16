# 安全与护栏

## 模块简介
本模块帮助你理解 Agent 系统的安全风险与治理方式，尤其是提示注入、权限边界、敏感操作控制与审计问题。

## 你将学到
- Prompt Injection 风险
- Tool 权限边界设计
- 敏感操作确认机制
- 审计与可追责能力

## 推荐学习顺序
1. **poco-claw**：最适合先学。它提供了相对直观的全栈安全沙箱实践，你可以先从产品界面和整体部署方式理解“安全 Agent 运行环境”是什么。
2. **goclaw**：第二个学。它更偏后端与平台实现，适合继续拆解多租户隔离、会话控制、执行环境与服务治理。
3. **agentic_coding_flywheel_setup**：最后学。它更像把安全、开发流程、评审和工程规范整合进一套工作流，适合在前两个项目基础上再看工程级落地。

## 三个仓库的学习入口

### 1. poco-claw
- 仓库位置：[`./poco-claw`](./poco-claw)
- 适合阶段：入门到进阶
- 推荐先看：
  - [`poco-claw/README.md`](./poco-claw/README.md)
  - [`poco-claw/README_zh.md`](./poco-claw/README_zh.md)
  - [`poco-claw/backend`](./poco-claw/backend)
  - [`poco-claw/frontend`](./poco-claw/frontend)
  - [`poco-claw/docker-compose.yml`](./poco-claw/docker-compose.yml)
- 学习重点：
  - 从产品形态理解受控 Agent 执行环境
  - 看前后端如何配合暴露安全控制能力
  - 理解容器化部署与隔离边界如何影响实际安全性

### 2. goclaw
- 仓库位置：[`./goclaw`](./goclaw)
- 适合阶段：后端安全机制拆解
- 推荐先看：
  - [`goclaw/README.md`](./goclaw/README.md)
  - [`goclaw/CLAUDE.md`](./goclaw/CLAUDE.md)
  - [`goclaw/internal`](./goclaw/internal)
  - [`goclaw/pkg`](./goclaw/pkg)
  - [`goclaw/docker-compose.yml`](./goclaw/docker-compose.yml)
- 学习重点：
  - 理解多租户、安全隔离与任务执行的后端实现
  - 关注内部模块边界、核心服务与安全约束
  - 对照部署配置看系统如何从代码走向可运行平台

### 3. agentic_coding_flywheel_setup
- 仓库位置：[`./agentic_coding_flywheel_setup`](./agentic_coding_flywheel_setup)
- 适合阶段：工程工作流安全与治理
- 推荐先看：
  - [`agentic_coding_flywheel_setup/README.md`](./agentic_coding_flywheel_setup/README.md)
  - [`agentic_coding_flywheel_setup/AGENTS.md`](./agentic_coding_flywheel_setup/AGENTS.md)
  - [`agentic_coding_flywheel_setup/packages`](./agentic_coding_flywheel_setup/packages)
  - [`agentic_coding_flywheel_setup/apps`](./agentic_coding_flywheel_setup/apps)
  - [`agentic_coding_flywheel_setup/tests`](./agentic_coding_flywheel_setup/tests)
- 学习重点：
  - 理解如何把安全约束嵌入 Agent 开发与交付工作流
  - 关注代码组织、测试、评审与自动化流程的协同关系
  - 看工程规范如何减少高风险操作和错误扩散

## 建议学习方法
- 第 1 轮：先看三个项目 README 和目录结构，只建立“安全问题地图”
- 第 2 轮：优先拆 `poco-claw` 的整体运行方式，再读 `goclaw` 的后端实现
- 第 3 轮：最后看 `agentic_coding_flywheel_setup`，重点理解安全如何进入工程流程
- 每读完一个仓库，补一份自己的“风险点 / 控制点 / 审计点”笔记

## 学习导航
- 学习路线：[`md/learning-roadmap.md`](./md/learning-roadmap.md)
- 术语表：[`md/glossary.md`](./md/glossary.md)
- 实践项目：[`md/practice-projects.md`](./md/practice-projects.md)
- 面试题：[`md/interview-questions.md`](./md/interview-questions.md)
- 学习清单：[`md/checklist.md`](./md/checklist.md)
- 返回总目录：[`../README.md`](../README.md)
