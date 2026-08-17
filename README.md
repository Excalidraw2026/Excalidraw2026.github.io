# AI探索者 · 长野的个人网站

纯静态个人门户站（HTML + CSS + JS），双击 `index.html` 即可在浏览器打开，无需任何环境。
视觉基于 esther-design-system（CC BY-NC-SA 4.0）升级：暖米底 + 蓝黄红三色 + 衬线标题，保留深色终端开场作为个人招牌。

## 网站结构

```
个人网站/
├── index.html               ← 主页：终端开场 + 卡片墙 + 能力三栏 + 作品集 + 终端收尾
├── brand-dna.md             ← 品牌基因：三色/字体/气质/禁忌（改版前先读）
├── README.md                ← 本文件
├── assets/
│   ├── style.css            ← 子页面公共样式（esther 亮色版）
│   └── images/
│       └── avatar.svg       ← 头像占位（换成你自己的 avatar.jpg 后引用）
├── references/
│   └── 组件与布局速查.md      ← 本站组件清单 + 可扩展方向
├── about.html               ← 关于我
├── blog.html                ← 博客/随笔（文章列表）
├── article-1.html           ← 《看见框架，然后真实地活》
├── article-2.html           ← 《我是怎么用 AI 搭起个人系统的》
├── timeline.html            ← 成长路径（时间线）
├── works.html               ← 作品集
├── crm.html                 ← 作品详情：家装 CRM 管理系统
├── projects.html            ← 正在折腾的项目
├── notes.html               ← 灵感碎片
├── shelf.html               ← 书架
├── about-site.html          ← 这个站是怎么做的
├── contact.html             ← 联系我（邮箱/微信/公众号）
└── coming.html              ← "建设中"占位页（新栏目先指向这里）
```

主页每张卡片是一个入口，点击进入对应子页面。新栏目想上线：复制 `coming.html` 改内容，再把主页卡片的 `href` 指过去即可。

## 内容替换清单

所有占位内容用 `【】` 标出，全局搜索 `【` 即可找到每一处。

| 位置 | 说明 |
|------|------|
| 主页终端动画 | 搜 `BOOT_LINES`，改每一行命令和输出；`TYPE_SPEED` 控制打字速度 |
| 主页收尾金句 | 搜 `FORTUNES` 数组 |
| 子页面 | 各页面内 `【】` 处，如联系方式、作品占位 |
| 卡片链接 | 主页 `index.html` 里 11 张卡片的 `href` |
| 品牌色 | `brand-dna.md` 顶部三色值 → 同步改 `assets/style.css` 与 `index.html` 的 `:root` |

## 部署（免费）

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
- 设计规范参考 [esther-design-system](https://github.com/esthersjw/esther-design-system)（CC BY-NC-SA 4.0），已署名

## License
页面内容：长野原创，保留所有权利。
设计规范：esther-design-system © ESTHER不二，CC BY-NC-SA 4.0，使用已署名。
