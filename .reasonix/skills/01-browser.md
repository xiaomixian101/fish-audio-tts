---
name: 01-browser
description: 🌐 用真实 Chrome 浏览器做网页测试、截图、爬虫、填表。适用：「截图这个网页」「帮我填表单」「抓取页面数据」。
---

---
name: 🌐 浏览器控制
description: 用真实 Chrome 浏览器做网页测试、截图、爬虫、填表。适用：「截图这个网页」「帮我填表单」「抓取页面数据」。
---

# 🌐 浏览器控制 (dev-browser)

用 `dev-browser` CLI 操控真实浏览器实现网页测试、截图、爬虫、自动化。对标 SawyerHood/dev-browser (6.2k⭐)。

## 何时使用
- 用户要测试网页、截图、或跟网站交互
- 需要从 JS 渲染的页面抓数据
- 需要验证 UI 行为、填表、点击流程
- 用户想看看网页长什么样

## 前提条件
`dev-browser` 已全局安装。Chrome 需以 `--remote-debugging-port=9222` 启动才能用 `--connect` 模式。

## 使用方式

### Headless 模式
```powershell
@"
const page = await browser.getPage("main");
await page.goto("https://example.com", { waitUntil: "domcontentloaded" });
console.log(await page.title());
"@ | dev-browser --headless
```

### 连接已打开的 Chrome
```powershell
@"
const page = await browser.getPage("main");
console.log(await page.title());
"@ | dev-browser --connect
```

### 截图
```powershell
@"
const page = await browser.getPage("main");
await page.goto("https://example.com");
const buf = await page.screenshot({ fullPage: true });
const path = await saveScreenshot(buf, "example.png");
console.log(path);
"@ | dev-browser --headless
```

### 填表 & 点击
```powershell
@"
const page = await browser.getPage("main");
await page.goto("https://example.com/login");
await page.fill('input[name="email"]', 'test@test.com');
await page.click('button[type="submit"]');
console.log(await page.url());
"@ | dev-browser --headless
```

## 核心 API
- `browser.getPage(name)` - 获取或创建命名页面
- `browser.newPage()` - 创建匿名页面
- `browser.listPages()` - 列出所有标签页
- `page.goto(url, opts)` - 导航
- `page.click(sel)`, `page.fill(sel, val)` - 交互
- `page.screenshot(opts)` - 截图
- `page.evaluate(fn)` - 在页面中执行 JS
- `saveScreenshot(buf, name)` - 保存截图到磁盘
