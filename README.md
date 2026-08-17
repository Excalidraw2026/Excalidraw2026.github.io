# AI探索者 · 个人网站

深色终端风格的个人门户站，纯静态（HTML + CSS + JS），双击 `index.html` 即可在浏览器打开，无需任何环境。

## 网站结构

```
个人网站/
├── index.html     ← 主页：终端开场 + 卡片墙 + 能力三栏 + 作品集 + 收尾
├── style.css      ← 子页面公共样式
├── about.html     ← 关于我
├── blog.html      ← 实践手记（文章列表）
├── timeline.html  ← 成长路径（时间线）
├── works.html     ← 作品集
├── contact.html   ← 联系我（邮箱/微信/公众号）
└── coming.html    ← "建设中"占位页（新栏目先指向这里）
```

主页的每张卡片都是一个入口，点击进入对应子页面。新栏目想上线时，复制 `coming.html` 改内容，再把主页卡片的 `href` 指过去即可。

## 内容替换清单

所有占位内容用 `【】` 标出，全局搜索 `【` 即可找到每一处。

| 位置 | 说明 |
|------|------|
| 主页终端动画 | 搜 `BOOT_LINES`，改每一行命令和输出；`TYPE_SPEED` 控制打字速度 |
| 主页收尾金句 | 搜 `FORTUNES` 数组 |
| 子页面 | 各页面内 `【】` 处，如联系方式的邮箱/微信/公众号 |
| 卡片链接 | 主页 `index.html` 里 12 张卡片的 `href` |

## 部署（免费）

任选其一：

### GitHub Pages（推荐）
1. 注册 [GitHub](https://github.com)，新建仓库，例如 `username.github.io`
2. 把整个文件夹（8 个 html + style.css）传上去
3. 仓库 Settings → Pages → Source 选 main 分支，保存
4. 等 1 分钟，访问 `https://username.github.io` 即可

### Vercel / Netlify
1. 注册后点 "New Project" → 导入这个文件夹
2. 框架选 "Other"，直接 Deploy，免费域名即刻可用

## 自定义域名（可选）
买好域名（`.me` 等约 ¥50~80/年，阿里云/Namesilo），DNS 加 CNAME 记录指向部署地址即可。

## 技术说明
- 零外部依赖，离线可用，中文直接 UTF-8
- 响应式：900px / 600px 断点，移动端卡片墙变单列
- 无障碍：尊重 `prefers-reduced-motion`
- 设计规范参考 [esther-design-system](https://github.com/esthersjw/esther-design-system)（CC BY-NC-SA 4.0），已署名

## License
页面内容：你拥有，随便改。
设计规范：esther-design-system © ESTHER不二，CC BY-NC-SA 4.0，使用已署名。
