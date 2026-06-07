---
name: 04-react-best-practices
description: ⚛️ Vercel 团队的 React & Next.js 性能优化指南(27.7k⭐)。70条规则：消除瀑布流、打包体积、SSR性能、重渲染优化。适用：「优化React性能」「审查组件」。
---

---
name: ⚛️ React最佳实践
description: Vercel 工程团队的 React & Next.js 性能优化指南(27.7k⭐)。70条规则：消除瀑布流、打包体积、SSR性能、重渲染优化。适用：「优化React性能」「审查这个组件」。
---

# ⚛️ React & Next.js 最佳实践 (Vercel)

来自 Vercel 工程团队 (27.7k⭐)，70 条规则，8 大类别。

## 何时使用
- 编写或审查 React 组件 / Next.js 页面
- 优化打包体积或加载时间
- 重构 React/Next.js 代码追求性能

## 核心规则

### 消除请求瀑布流（严重）
- 多个独立异步用 `Promise.all()` — 绝不要顺序 await
- 把 `await` 移到真正使用数据的分支里
- 用 `Suspense` 边界流式传输

### 打包体积（严重）
- 直接从源文件导入，**不要**从 barrel 文件导入
- 大组件用 `next/dynamic` + `ssr: false`
- 第三方脚本延迟到 hydration 之后

### 服务端性能（高）
- Server Action 要鉴权
- 用 `React.cache()` 做请求级去重
- 静态 I/O 提升到模块顶层

### 重渲染优化（中）
- 昂贵计算提取到 `React.memo`
- 非紧急 UI 用 `startTransition`
- 绝不要在组件内部定义组件

### 渲染性能（中）
- 长列表用 `content-visibility: auto`
- 条件渲染用三元而非 `&&`
- 非关键脚本用 `defer`/`async`

### JS 性能（低中）
- CSS 变更用 class 批量操作
- O(1) 查找用 Set/Map 而非数组 includes
- 尽早 return

## 审查清单
1. 独立异步调用是否并行了？
2. 有没有 barrel import？
3. 大组件是否动态导入了？
4. Server Action 是否做鉴权了？
5. 事件监听器是否正确清理？
6. 有没有内联组件定义？
