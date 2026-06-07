---
name: 07-git-commit
description: ✍️ 自动分析 git 变更，生成符合 conventional commits 规范的提交信息。适用：「帮我写commit」「提交一下」「怎么写commit」。
---

---
name: ✍️ Git提交
description: 自动分析 git 变更，生成符合 conventional commits 规范的提交信息（feat/fix/refactor等）。适用：「帮我写commit」「提交一下」「怎么写commit」。
---

# ✍️ Git 提交信息生成器

分析变更，生成符合 Conventional Commits 规范的提交信息。

## 何时使用
- 「帮我生成 commit」「提交一下」「这个 commit 怎么写」

## 流程

### 1. 查看变更
```bash
git diff --staged   # 暂存区
git diff            # 未暂存
```

### 2. 确定类型
| 前缀 | 场景 |
|------|------|
| `feat:` | 新功能 |
| `fix:` | Bug修复 |
| `refactor:` | 重构 |
| `docs:` | 文档 |
| `test:` | 测试 |
| `chore:` | 构建/依赖 |
| `perf:` | 性能优化 |

### 3. 写信息
```
<type>: <简短描述（≤72字符）>

<正文 — 做了什么、为什么>

<脚注 — Breaking changes、Issue引用>
```

### 4. 提交
**始终先询问再提交** — 绝不自动提交。

## 示例
```
feat: 添加 JWT 用户认证功能

实现登录/登出流程，支持 refresh token 轮换。
密码使用 bcrypt 哈希。

Closes #42
```

## 注意事项
- 首行用祈使语气：「添加」而非「添加了」
- 不相关的改动建议拆分提交
- 引用 Issue：`Closes #N` 或 `Refs #N`
