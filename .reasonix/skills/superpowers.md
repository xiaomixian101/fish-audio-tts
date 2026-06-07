---
name: superpowers
description: 220k⭐ 最强 AI 编程方法论 — 自动触发脑暴→设计→计划→TDD→子Agent开发→代码审查→分支收尾的完整工作流。解决 AI 写代码的 4 大痛点：需求不对齐、代码太啰嗦、写完不能跑、越写越乱。一装上 Agent 自动变强。
---

# Superpowers 超级编程工作流 (220k⭐)

GitHub 上 Star 最高 (220k) 的 AI 编程方法论。**不只改代码，改了 Agent 的工作方式** — 从一开始就介入，强制执行完整软件工程流程。

## 核心理念

当你跟 Agent 说「帮我做个东西」，它不会直接冲去写代码。它会：

1. **先退一步问** — 你到底想做什么？
2. **出设计稿** — 分成小块让你审阅
3. **你签字后出计划** — 详细到每 2-5 分钟的任务
4. **子 Agent 开发** — 每个任务独立子 Agent 执行 + 两阶段审查
5. **写完收尾** — 测试验证、分支清理

## 自动化工作流（全自动触发）

### 🧠 brainstorming — 需求脑暴
- 在写代码**之前**自动激活
- Socratic 式提问，帮你把粗糙想法打磨成型
- 输出设计文档，分块展示

### 🌿 using-git-worktrees — 隔离工作区
- 设计通过后自动创建独立 git worktree
- 在新分支上跑项目初始化，验证测试基线

### 📝 writing-plans — 实施计划
- 把设计拆成 **2-5 分钟一个** 的小任务
- 每个任务有精确的文件路径、完整代码、验证步骤

### 🤖 subagent-driven-development — 子 Agent 开发
- 每个任务派一个**干净的子 Agent** 去执行
- 两阶段审查：先查是否符合规格，再查代码质量
- Claude 可以连续自主工作 **几个小时** 不偏离计划

### 🧪 test-driven-development — TDD
- **强制**红 → 绿 → 重构
- 看到测试先失败 → 写最少代码让它过 → commit
- 会删掉先写代码再写测试的投机行为

### 🔍 requesting-code-review — 代码审查
- 任务之间自动触发
- 按严重度分级报告问题
- 严重问题会**阻塞**进展

### 🏁 finishing-a-development-branch — 分支收尾
- 所有任务完成后触发
- 验证测试 → 给出选项（merge / PR / 保留 / 丢弃）
- 自动清理 worktree

## 解决的核心痛点

| 痛点 | Superpowers 怎么解决 |
|------|---------------------|
| Agent 做的东西不对 | brainstorming 先对齐，你签字再动手 |
| 代码太啰嗦难维护 | TDD + 两阶段审查确保代码质量 |
| 写好的代码跑不起来 | TDD 红绿循环 + 每个任务有验证步骤 |
| 越写越乱成屎山 | 子 Agent 隔离 + 架构审查 + 强制规划 |

## 安装方式
```bash
# Claude Code
/plugin install superpowers@claude-plugins-official

# Codex CLI
/plugins → 搜索 superpowers → Install

# Cursor
/add-plugin superpowers
```

## 不需要手动触发
Skills 会**自动激活** — 你跟 Agent 正常说话，Superpowers 在后台保证流程正确。
