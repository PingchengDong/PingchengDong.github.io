# Pingcheng Dong 主页维护指南

核对日期：2026-11-17。本文依据本地工作树，未核验线上部署状态。

## 项目与内容

仓库：`/Users/dongpingcheng/web/PingchengDong.github.io`。
Git remote：`https://github.com/PingchengDong/PingchengDong.github.io.git`。
配置站点：`https://pingchengdong.github.io`。
基于 AcadHomepage 的 Jekyll 单页英文学术主页，GitHub Pages 发布，无 Node 构建步骤。

页面依次为介绍、Honors and Awards、News、Selected Publication、Collaborative Publications、Teaching Assistant。侧栏由配置生成，顶部导航独立定义，顺序不完全等同正文。
当前介绍聚焦软硬件协同、3D IC、DTCO、硬件感知模型压缩。个人身份、论文与荣誉以主页源文件和用户后续提供的事实为准，不在此重复维护履历。

## 常见修改入口

| 修改内容 | 源文件与注意事项 |
| --- | --- |
| 简介、新闻、教育、奖项、论文、助教经历、CV 链接 | `_pages/about.md`，HTML + Markdown + Liquid；根路径 `/`，保留 front matter 和显式锚点 |
| 姓名、邮箱、侧栏简介、头像、Scholar、SEO 描述 | `_config.yml`；修改后重启本地服务器 |
| 顶部导航 | `_data/navigation.yml`；锚点须与正文同步 |
| 论文图片、头像、CV | `images/`；核对大小写及实际引用，旧版本不凭文件名删除 |
| 论文卡片和锚点偏移 | `assets/css/main.scss` 尾部，卡片在小屏文字先于图片，大屏图片在左 |
| 颜色、字号、断点 | `_sass/_variables.scss` |
| 正文、侧栏、导航样式 | `_sass/_page.scss`、`_sass/_sidebar.scss`、`_sass/_masthead.scss`、`_sass/_navigation.scss` |
| 页面组件 | `_layouts/default.html` 组合 `_includes/`；侧栏资料在 `author-profile.html` |
| favicon、MathJax | `_includes/head/custom.html` |
| 脚本加载、引用数 | `_includes/scripts.html`、`_includes/fetch_google_scholar_stats.html` |
| 发布工作流 | `.github/workflows/jekyll-gh-pages.yml` |

添加主论文时复用 `paper-box` / `paper-box-image` / `paper-box-text`，保留 `markdown="1"` 与块之间空行。作者顺序、标题、会议年份和链接依据用户材料，姓名沿用加粗方式。合作论文当前采用列表。
导航使用 `about-me`、`news`、`publications`、`honors` 显式 ID，不依赖含 emoji 标题生成的自动 ID。

## 运行、检查与发布

```bash
cd /Users/dongpingcheng/web/PingchengDong.github.io
bundle install
bash run_server.sh
# Preview: http://127.0.0.1:4000
# Build only:
bundle exec jekyll build
```

`run_server.sh` 实际运行 `bundle exec jekyll liveserve`（hawkins）。2026-11-17 默认 shell 中 Ruby 为 2.6.10，Bundler 为 1.17.2，`bundle check` 因缺少锁文件要求的 Bundler 2.2.19 失败，因此尚未验证本机可构建。后续需要预览时先解决 Ruby/Bundler 环境，不为绕过环境问题盲目更新锁文件。

工作流在 push 到 `main` 或手动触发时构建 `_site` 并部署 Pages。配置事实不等于线上已经发布；发布后需检查 Actions 与线上页面。此次仅学习与记录，无提交或推送。

内容修改检查资源路径和导航锚点；布局修改额外检查桌面与手机宽度、侧栏、卡片和导航。生成的 `_site/` 不作为源码编辑。`docs/` 已在 Jekyll 排除列表中，维护文档放这里。

## Scholar 的实际状态

爬虫 `google_scholar_crawler/main.py` 读取 `GOOGLE_SCHOLAR_ID`，输出 `results/gs_data.json` 与 `results/gs_data_shieldsio.json`。当前作者 ID 为 `axUZg6MAAAAJ`。
前端配置使用 jsDelivr 从仓库 `google-scholar-stats` 分支获取数据，关闭 CDN 后使用 raw.githubusercontent.com。论文徽章通过 `show_paper_citations` 类和 `data` 中的论文 ID 匹配。
**当前工作树只有 Pages 部署 workflow，没有 Scholar 爬虫 workflow，不能认为每日自动更新已启用。** 当前正文引用数示例位于 HTML 注释中；没有引用占位元素时，前端直接跳过请求。远端数据分支和 Secret 未核验。

## 已有修改与待核实事项

接手时已有 5 个修改文件：`_config.yml`、`_data/navigation.yml`、`_includes/fetch_google_scholar_stats.html`、`_includes/head.html`、`_pages/about.md`。包括 URL/Scholar 链接修正、显式导航锚点、简介调整、引用空值保护、移除全局新标签打开设置。它们是接手前状态，后续先重新检查 diff。

以下仅记录，未擅改：
- SEO description 仍为旧研究方向，与当前正文介绍不完全一致。
- News 最后列到 2024-10-11，主论文已添加 JSSC 2026 与 ISSCC 2026；是否补新内容由用户提供。
- CV 使用固定路径 `images/pingcheng_dong_cv.pdf`，当前版本来自用户指定的 `/Users/dongpingcheng/Documents/pingcheng_dong_cv_hkust_26fall.pdf`（2026-11-17）。后续替换该文件即可，保持链接稳定；旧模板名 PDF 已移除。
- head 中引用的 `mstile-144x144.png`、`browserconfig.xml` 在当前 images 目录未找到。
- `_layouts/default.html` 声明 `layout: compress`，当前 `_layouts/` 仅有 default，构建时需关注相关警告。
- `.history/` 是已有历史目录，不作为当前内容来源；未检查其保留价值，不擅自清理。

## 维护习惯

先读记忆与 git diff，再按需求编辑最小范围。保留现有英文内容及视觉体系，重大改版由用户明确提出。只把稳定机制与维护入口写进记忆，履历和论文仍以源码为唯一内容来源。收尾清点临时文件，保留正式资产，不留验证脚本副本。

## 2026 论文素材来源

两篇 2026 论文位于 Selected Publication 顶部，顺序为 JSSC、ISSCC，标题和作者已对照用户提供的 PDF 与 https://vsdl.hkust.edu.hk/publications/ 。JSSC 使用原文 DOI `10.1109/JSSC.2026.3718555`，ISSCC 使用 IEEE document 11409211。未复制 PDF 或推测 News 的录用公告日期。

两篇共用用户提供的 `/Users/dongpingcheng/Downloads/RHB.png`，站点资产为 `images/rhb_2026.png`。`paper-box-shared` 在桌面上左侧 30% 图片栏、右侧 70% 两篇论文，图片最大 280px；手机上图片在上、论文在下。两篇间用细线区分，保留各自作者及链接。此前两张独立配图及 compact 样式已被此方案替换并删除。

## 自动发布约定

2026-11-17 用户明确授权：后续主页修改完成并检查后，自动 git commit 和 git push，无需再次确认。推送后核对远端提交，区分推送成功与 Pages 部署成功。此前“未推送”描述仅为对应任务当时状态。

## 论文链接与共同贡献标记

2026-11-17：标题仅显示 `Selected Publication`，有共同贡献星号的每篇论文在作者下方独立显示斜体 `*: Equal contribution`。依据 VSDL 论文页，ISSCC 2025 的 Pingcheng Dong / Yonghao Tan、APSQ (DAC 2025) 的 Yonghao Tan / Pingcheng Dong 标注星号；其他论文不推断共同贡献。ISSCC 2025 链接 IEEE document 10904499，GQA 链接 DOI 10.1145/3649329.3657314（HKUST Research Portal 核对）。APSQ 链接 arXiv 2505.03748，配图 `images/apsq_2025.png` 来自 VSDL `/images/papers/2025/APSQ.png`。

2026-11-17：按用户要求移除独立 Education 板块及对应导航，简介中的教育经历保留。

2026-11-17：用户最终选择侧栏仅显示英文姓名，中文姓名配置、模板及专用样式已移除。

2026-11-17 用户补充：GQA (DAC 2024) 的 Pingcheng Dong / Yonghao Tan、TCAS-I 2021 stereo depth coprocessor 的 Pingcheng Dong / Zhuoyu Chen 也标注共同贡献星号及独立说明。用户指定删除 TCAS-II 2022 rectification、A-SSCC 2021、SOCC 2021、ICTA 2020 四个列表条目。
