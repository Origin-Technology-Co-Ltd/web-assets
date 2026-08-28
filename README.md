# web-assets

无锡起源科技有限公司（Wuxi Origin Technology Co., Ltd.）的静态 Web 资源仓库，供各应用商店、合规文档及对外链接使用。

通过 **GitHub Pages** 发布，访问根路径：

**https://origin-technology-co-ltd.github.io/web-assets/**

## 目录结构

按项目分子目录，每个项目可包含隐私政策、使用条款等页面：

```
web-assets/
├── index.html              # 站点首页（项目列表）
├── _assets/style.css       # 共享样式
├── calc-plus/              # Calc Plus 计算器
│   ├── index.html
│   ├── privacy/
│   │   ├── index.html      # 按浏览器语言跳转 en / zh
│   │   ├── en.html
│   │   └── zh.html
│   └── terms/
│       ├── index.html
│       ├── en.html
│       └── zh.html
└── fingertip-notes/        # Fingertip Notes 笔记应用
    ├── index.html
    ├── privacy/
    │   ├── index.html
    │   ├── en.html
    │   └── zh.html
    └── terms/
        ├── index.html
        ├── en.html
        └── zh.html
```

新增项目时，在根目录 `index.html` 的项目列表中增加链接即可。

## Calc Plus 链接

| 文档 | URL |
|------|-----|
| 项目首页 | https://origin-technology-co-ltd.github.io/web-assets/calc-plus/ |
| 隐私政策（自动跳转） | https://origin-technology-co-ltd.github.io/web-assets/calc-plus/privacy/ |
| 隐私政策 · English | https://origin-technology-co-ltd.github.io/web-assets/calc-plus/privacy/en.html |
| 隐私政策 · 中文 | https://origin-technology-co-ltd.github.io/web-assets/calc-plus/privacy/zh.html |
| 使用条款（自动跳转） | https://origin-technology-co-ltd.github.io/web-assets/calc-plus/terms/ |
| 使用条款 · English | https://origin-technology-co-ltd.github.io/web-assets/calc-plus/terms/en.html |
| 使用条款 · 中文 | https://origin-technology-co-ltd.github.io/web-assets/calc-plus/terms/zh.html |

Play Console **隐私政策 URL** 建议填写英文版：`.../calc-plus/privacy/en.html`，或根路径 `.../privacy/`（会按浏览器语言跳转）。

## Fingertip Notes 链接

| 文档 | URL |
|------|-----|
| 项目首页 | https://origin-technology-co-ltd.github.io/web-assets/fingertip-notes/ |
| 隐私政策（自动跳转） | https://origin-technology-co-ltd.github.io/web-assets/fingertip-notes/privacy/ |
| 隐私政策 · English | https://origin-technology-co-ltd.github.io/web-assets/fingertip-notes/privacy/en.html |
| 隐私政策 · 中文 | https://origin-technology-co-ltd.github.io/web-assets/fingertip-notes/privacy/zh.html |
| 使用条款（自动跳转） | https://origin-technology-co-ltd.github.io/web-assets/fingertip-notes/terms/ |
| 使用条款 · English | https://origin-technology-co-ltd.github.io/web-assets/fingertip-notes/terms/en.html |
| 使用条款 · 中文 | https://origin-technology-co-ltd.github.io/web-assets/fingertip-notes/terms/zh.html |

Play Console **隐私政策 URL** 建议填写英文版：`.../fingertip-notes/privacy/en.html`，或根路径 `.../privacy/`（会按浏览器语言跳转）。

## AdMob app-ads.txt

| 文件 | URL |
|------|-----|
| app-ads.txt | https://origin-technology-co-ltd.github.io/web-assets/app-ads.txt |

Play Console / App Store Connect 里的**开发者网站**必须填：

`https://origin-technology-co-ltd.github.io/web-assets`

（与上表域名完全一致，不要漏掉 `/web-assets` 路径。）

文件内容（IAB 规范）：

```txt
google.com, pub-2082434913159874, DIRECT, f08c47fec0942fa0
```

推送 `master` 到 GitHub 后，在 AdMob 控制台点「抓取验证」；通常几分钟到几小时生效。

## 启用 GitHub Pages

仓库首次推送后，在 GitHub 仓库设置中：

1. **Settings → Pages**
2. **Source**: Deploy from a branch
3. **Branch**: `master` / **Folder**: `/ (root)`
4. 保存后等待 1–3 分钟生效

或使用 GitHub CLI：

```bash
gh api repos/Origin-Technology-Co-Ltd/web-assets/pages -X POST \
  -f source[branch]=master -f source[path]=/
```

## 本地预览

```bash
cd web-assets
python3 -m http.server 8080
# 打开 http://localhost:8080/calc-plus/privacy/
```
