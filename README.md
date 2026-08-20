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
└── calc-plus/              # Calc Plus 计算器
    ├── index.html
    ├── privacy/index.html
    └── terms/index.html
```

新增项目时，在根目录 `index.html` 的项目列表中增加链接即可。

## Calc Plus 链接

| 文档 | URL |
|------|-----|
| 项目首页 | https://origin-technology-co-ltd.github.io/web-assets/calc-plus/ |
| 隐私政策 | https://origin-technology-co-ltd.github.io/web-assets/calc-plus/privacy/ |
| 使用条款 | https://origin-technology-co-ltd.github.io/web-assets/calc-plus/terms/ |

Play Console **隐私政策 URL** 请填写隐私政策地址。

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
