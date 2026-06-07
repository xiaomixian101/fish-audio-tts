---
name: matt-pocock
description: Matt Pocock 的 120k⭐ AI 编码 Skills — grill-me（深度提问对齐需求）、tdd（红绿重构循环）、diagnose（系统调试）、zoom-out（全局视角）、手把手教你写好代码。适用场景：写代码前先对齐、调试bug、改善架构、拆分需求。
---

# Matt Pocock 编程技能包 (120k⭐)

TypeScript 大神 Matt Pocock 每天都在用的 AI 编码技能。核心理念：**软件工程基本原则比以往任何时候都重要**。

## 核心技能

### 🔥 grill-me / grill-with-docs — 需求对齐（最受欢迎）
- 在写代码**之前**，让 Agent 对你进行一场深度拷问
- 逼你思考清楚你到底要什么
- grill-with-docs 额外会帮你建立**共享语言**（CONTEXT.md）和**架构决策记录**（ADR）
- **永远先对齐再写代码**

### 🧪 tdd — 测试驱动开发
- 严格执行 RED → GREEN → REFACTOR 循环
- 先写失败测试 → 看到它红 → 写最少代码让它绿 → 重构
- 自动删除还没写测试就写的代码
- 包含测试反模式参考

### 🔍 diagnose — 系统调试
- 四步根因分析：复现 → 最小化 → 假设 → 打桩 → 修复 → 回归测试
- 绝不猜，用证据说话

### 🏗️ improve-codebase-architecture — 改善代码架构
- 找到代码库中的「深模块」机会
- 基于共享语言和 ADR 做架构优化
- **建议每几天跑一次**，防止代码腐化

### 🔭 zoom-out — 全局视角
- 让 Agent 拉远视角，从系统层面解释代码
- 理解代码在整个系统中的位置

### 📋 to-prd / to-issues — 需求拆分
- 把对话上下文直接变成 PRD，提交为 Issue
- 把任何计划拆成可独立执行的 GitHub Issues

### 🏷️ triage — Issue 分类
- 用状态机模式对 Issue 进行分类
- 基于你定义好的标签体系

### 🗜️ caveman — 极简沟通模式
- 压缩 token 用量 ~75%
- 保持技术准确性，砍掉废话

### 🤝 handoff — 会话交接
- 把当前对话压缩成交接文档
- 另一个 Agent 可以无缝接手继续工作

## 核心理念

1. **别让 Agent 猜你要什么** — 先 grill，对齐再写
2. **建立共享语言** — CONTEXT.md 让沟通更精准，省 token
3. **缩短反馈环** — TDD 让 Agent 边写边验证
4. **每天关心架构** — 跑 improve-codebase-architecture 防止变成一坨屎山

## 安装方式
```bash
npx skills@latest add mattpocock/skills
```

## 使用方式
在 Claude Code / Codex / Cursor 中直接用斜杠命令：
- `/grill-me` — 对齐需求
- `/grill-with-docs` — 对齐 + 建立文档
- `/tdd` — 测试驱动开发
- `/diagnose` — 调试
- `/improve-codebase-architecture` — 改善架构
- `/zoom-out` — 全局视角
- `/to-prd` — 生成 PRD
- `/to-issues` — 拆 Issues
- `/triage` — 分类 Issues
- `/caveman` — 极简模式
- `/handoff` — 会话交接
