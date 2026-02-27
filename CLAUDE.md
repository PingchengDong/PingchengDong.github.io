# CLAUDE.md

本文件为 Claude Code (claude.ai/code) 在本仓库中工作时提供指引。请始终使用中文与用户交流。

## 项目概述

基于 Jekyll 的学术个人主页，属于 Pingcheng Dong（香港科技大学），从 [AcadHomepage](https://github.com/RayeRen/acad-homepage.github.io) 模板 fork 而来。通过 GitHub Pages 部署于 PingchengDong.github.io。

## 开发命令

```bash
# 安装 Ruby 依赖
bundle install

# 启动本地开发服务器（支持热重载，访问 http://127.0.0.1:4000）
bash run_server.sh
# 实际执行: bundle exec jekyll liveserve

# 更新 Google Scholar 引用数据（需要 GOOGLE_SCHOLAR_ID 环境变量）
cd google_scholar_crawler && pip install -r requirements.txt && python3 main.py
```

注意：修改 `_config.yml` 后需要重启服务器，Jekyll 不会自动热重载该文件。

## 架构

### 内容流转
`_config.yml`（站点设置 + 作者信息）→ `_layouts/default.html` → `_includes/`（组件）→ `_pages/about.md`（主页内容）

### 关键文件
- **`_pages/about.md`**：主页内容——个人介绍、论文列表、教育背景、获奖情况。使用 HTML+Markdown 混合语法及 Jekyll front matter。
- **`_config.yml`**：站点元数据、作者信息（姓名、头像、社交链接、简介）、插件配置、构建设置。
- **`_data/navigation.yml`**：导航菜单项。
- **`_includes/`**：模板组件——`sidebar.html`、`author-profile.html`、`masthead.html`、`head/custom.html`（MathJax、favicon、academicons）。
- **`_layouts/default.html`**：唯一的页面布局模板，组装所有 includes。

### Google Scholar 引用系统
GitHub Action（`.github/workflows/google_scholar_crawler.yaml`）每天 UTC 08:00 及每次页面构建时运行。执行 `google_scholar_crawler/main.py` 抓取引用数据，JSON 输出到 `google-scholar-stats` 分支。前端通过 CDN 使用 `_includes/fetch_google_scholar_stats.html` 获取数据，填充 `<span class="show_paper_citations" data="PAPER_ID">` 元素。

### 样式
`_sass/` 中的 SCSS 通过 `assets/css/main.scss` 编译。使用 Susy 网格框架和 Breakpoint 实现响应式布局。类名采用 BEM 风格（如 `.author__name`、`.author__bio`）。第三方库位于 `_sass/vendor/`。

### 添加论文
在 `_pages/about.md` 中，论文使用 `paper-box` / `paper-box-image` / `paper-box-text` 的 div 结构，以内联 HTML 编写。引用徽章使用：`<span class='show_paper_citations' data='GOOGLE_SCHOLAR_PAPER_ID'></span>`。
