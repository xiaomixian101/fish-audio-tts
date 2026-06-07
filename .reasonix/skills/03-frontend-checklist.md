---
name: 03-frontend-checklist
description: 📋 最权威的前端质量审计，385条规则覆盖11大类：无障碍、安全、性能、SEO、HTML、CSS、图片、JS。适用：「审查网站」「检查前端」「上线前自查」。
---

---
name: 📋 前端检查清单
description: 最权威的前端质量审计，385条规则覆盖11大类：无障碍、安全、性能、SEO、HTML、CSS、图片、JS。适用：「审查网站」「检查前端质量」「上线前自查」。
---

# 📋 前端检查清单 — Web 质量审计

基于 Front-End Checklist (72.9k⭐)，385 条规则，11 大类别。

## 何时使用
- 「帮我审查这个网站」「检查前端质量」「上线前自查」

## 审计类别

### 🔴 高优先级（必须修复）
| 类别 | 规则 | 重点 |
|------|------|------|
| **无障碍** | 95 | ARIA、语义HTML、键盘导航、颜色对比度、焦点状态 |
| **安全性** | 22 | HTTPS、CSP、HSTS、X-Frame-Options、Cookie标志 |
| **性能** | 43 | Core Web Vitals、懒加载、打包体积、缓存、关键CSS |

### 🟡 中优先级（应该修复）
| 类别 | 规则 | 重点 |
|------|------|------|
| **SEO** | 94 | Meta标签、结构化数据、Canonical URL、社交卡片 |
| **HTML** | 25 | 语义标记、DOCTYPE、lang属性、viewport、表单 |
| **CSS** | 32 | 响应式、打印样式、暗色模式、选择器优先级 |
| **图片** | 25 | WebP/AVIF、srcset、懒加载、alt文本、CDN |

## 快速审计

### 安全头部（最先检查）
- HTTPS 强制？HSTS？CSP？X-Frame-Options？Cookie Secure+HttpOnly+SameSite？

### 性能信号
- LCP < 2.5s、INP < 200ms、CLS < 0.1
- 图片显式宽高、非关键CSS异步、脚本defer/async

### 无障碍扫描
- lang 属性、图片alt文本、颜色对比度≥4.5:1、焦点指示器、语义HTML、键盘可达

### SEO 要点
- title 存在唯一 <60字符、meta description <155字符、Canonical URL、Open Graph标签

## 输出格式
```
## 前端审计：[URL/组件]
### 🔴 严重问题 — 问题 → 修复建议
### 🟡 警告 — 问题 → 修复建议
### 🟢 建议 — 改进思路
### 评分：X/10
```
