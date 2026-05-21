# superpowers — Agentic Skills Framework

> **Summary:** Explored superpowers — a complete software development workflow built on composable agent skills. It transforms Claude Code from a coding assistant into a full engineering team with subagent-driven development, automatic spec extraction, TDD enforcement, and autonomous multi-hour work sessions. Studied as a reference for agent orchestration patterns.

## Problem

单一 AI 编程助手（如 Claude Code）在面对复杂项目时容易：跳过需求分析直接写代码、缺乏系统化测试、偏离原始设计、无法长时间自主工作。需要一套完整的开发流程框架，让 agent 像真正的工程团队一样运作。

## Features

- **自动需求提取**：从对话中自动提炼规格说明，分段确认
- **子智能体驱动开发**：多个 agent 协作，分别负责任务规划、编码、审查
- **TDD 强制**：强调红绿重构循环、YAGNI 和 DRY 原则
- **可组合技能集**：16 个模块化技能覆盖完整开发流程
- **长时间自主工作**：agent 可在批准后连续工作数小时不偏离计划
- **自动触发**：安装后无需特殊操作，agent 自动应用技能

## Architecture

- **技能层**：每个技能是独立模块（prompt + 工作流定义）
- **编排层**：根据任务类型自动激活对应技能组合
- **子智能体层**：并行 agent 处理独立子任务
- **工作流阶段**：spec → design → plan → implement → review → qa → ship

技能目录包括：`brainstorming`、`subagent-driven-development`、`test-driven-development`、`using-git-worktrees`、`verification-before-completion` 等。

## Highlights

- 深入研究了子智能体驱动开发模式（SADD）
- 学习了如何将单一 LLM 调用转化为结构化工程流程
- 理解了技能组合（composable skills）在 agent 系统中的价值
- 探索了 TDD 在 AI 生成代码中的实践方式
- 分析了 agent 长时间自主工作的保持策略（上下文锚点、阶段性检查）

## Results

- 完成了 superpowers 框架的全量技能分析
- 将关键模式整合到本地 gstack 技能系统中
- 为 InkMuse 平台的 AI 辅助写作流程提供了架构参考
- 建立了 agent 工作流设计的评估框架

## Reflection

Superpowers 的核心洞见是：**流程比能力更重要**。单个 LLM 的能力已经很强，但缺乏工程纪律。通过结构化的技能组合，可以将 AI 编程从"辅助工具"升级为"工程团队"。关键学习：subagent 编排需要明确的责任边界和检查点；TDD 在 AI 场景中比传统开发更有价值，因为 AI 容易过度工程化。

## Project Status

**Active Integration.** 框架已深入使用，多个技能已集成到本地开发环境。持续跟踪上游更新并选择性合并。
