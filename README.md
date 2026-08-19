# AI探索者 · 长野的个人网站

纯静态个人门户站（HTML + CSS + JS），双击 `index.html` 即可在浏览器打开，无需任何环境。
视觉为**长野自有的哑光新中式设计系统**（奶黄 `#F2D791` + 泥青 `#108B96` + 朱砂红 `#C0392B`，米白底，哑光纸感噪点+暖柔影），并叠加 logo 头像与深色终端开场作为个人招牌。

> 设计规范以 `D:\我的知识库\长野设计系统`（GitHub: `Excalidraw2026/changye-design-system`）为源，本站是它的落地应用之一。

## 网站结构

```
个人网站/
├── index.html               ← 主页：终端开场 + 卡片墙 + 能力三栏 + 作品集 + 终端收尾（独立内联样式，桌面 OS 拟物架构）
├── brand-dna.md             ← 品牌基因：三色/字体/气质/禁忌（改版前先读）
├── README.md                ← 本文件
├── assets/
│   ├── style.css            ← 子页面公共样式（哑光新中式 + 纸感材质）
│   └── images/
│       ├── logo.png         ← 正式定稿 logo（方形头像款）
│       ├── logo-256.png     ← 压缩版 UI 头像（logo 头像位用）
│       ├── logo-96.png      ← 超小版
│       ├── favicon.png      ← 站点图标
│       └── (文章配图 article-*.png)
├── references/
│   └── 组件与布局速查.md      ← 本站组件清单 + 可扩展方向
├── about.html               ← 关于我
├── blog.html                ← 博客/随笔（文章列表）
├── article-1..4.html        ← 文章（含配图）
├── timeline.html            ← 成长路径（时间线）
├── works.html               ← 作品集
├── crm.html                 ← 作品详情：家装 CRM 管理系统
├── projects.html            ← 正在折腾的项目
├── notes.html               ← 灵感碎片
├── shelf.html               ← 书架
├── recommends.html          ← 推荐
├── about-site.html          ← 这个站是怎么做的
├── contact.html             ← 联系我（邮箱/微信/公众号）
└── (quotes.html, works 等)  ← 更多栏目
```

主页每张卡片是一个入口，点击进入对应子页面。新栏目想上线：复制一个子页面改内容，再在主页把卡片 `href` 指过去即可。

## 品牌与视觉（对齐长野设计系统）

- **品牌三色**：奶黄 `#F2D791`（地）+ 泥青 `#108B96`（骨）对分背景，朱砂红 `#C0392B` 点睛（10% 以内）
- **字体**：中文标题 `Noto Serif SC`、正文 `Noto Sans SC`、手写 `Caveat`、英文 `Fraunces`
- **材质**：全局 `--paper-noise` 哑光噪点肌理 + `--paper-shadow` 暖调柔影，卡片/文章/面板叠纸感
- **署名**：`长野 · 阿浩`；页脚/卡片标注归属
- 深色终端开场（index）为个人招牌，保留原创架构，不改配色

## 内容替换清单

所有占位内容用 `【】` 标出，全局搜索 `【` 即可找到每一处。

| 位置 | 说明 |
|------|------|
| 主页终端动画 | 搜 `BOOT_LINES`，改每一行命令和输出；`TYPE_SPEED` 控制打字速度 |
| 主页收尾金句 | 搜 `FORTUNES` 数组 |
| 子页面 | 各页面内 `【】` 处，如联系方式、作品占位 |
| 卡片链接 | 主页 `index.html` 里卡片的 `href` |
| 品牌色 | `brand-dna.md` 顶部三色值 → 同步改 `assets/style.css` 与 `index.html` 的 `:root` |

## 部署

### GitHub Pages（已上线）
仓库 `Excalidraw2026/Excalidraw2026.github.io`，改完文件后：
1. `git add -A && git commit -m "update"`
2. `git push origin master`
3. 等约 1 分钟，访问 `https://excalidraw2026.github.io`

### 本地预览
直接双击 `index.html`，或 `python -m http.server` 起本地服务。

## 技术说明
- 零外部依赖（仅 Google Fonts 网络字体，离线时回退系统字体）
- 响应式：900px / 600px 断点，移动端卡片墙变单列
- 无障碍：尊重 `prefers-reduced-motion`
- 视觉规范源自**长野自有设计系统**（`Excalidraw2026/changye-design-system`），品牌归长野（阿浩）所有

## License
页面内容：长野原创，可自由商用，署名 `长野 · 阿浩`。
视觉规范：长野设计系统（归长野所有），可自由商用。
