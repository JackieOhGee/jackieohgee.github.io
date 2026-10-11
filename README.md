# 作品集网站（GitHub Pages + Jekyll）

暗色游戏风作品集：首页 / 拆解案列表 / 文章页。零构建工具链——
写 Markdown 推送 GitHub 即自动发布。

## 怎么加一篇拆解案

1. 在 `_posts/` 里新建文件，命名：`年-月-日-英文短名.md`（如 `2026-10-15-tarkov-extract.md`）
2. 文件开头写元信息（照抄改内容）：

```markdown
---
layout: post
title: 文章标题
subtitle: 一句话副标题
category: 系统拆解
date: 2026-10-15
excerpt: 列表页显示的摘要（80字内）
---

正文从这里开始（标准 Markdown，支持表格/引用/代码块）……
```

3. 提交推送：`git add . && git commit -m "新文章" && git push`
4. 等 1~2 分钟 GitHub 自动构建完成，网站即更新

## 目录结构

- `index.html` 首页（Hero/拆解案卡片/游戏作品/关于）
- `articles/index.html` 拆解案列表页
- `_layouts/` 页面模板（default/post/list）
- `_posts/` 文章（一个 md 一篇）
- `assets/css/main.css` 全站样式（改主题色改 `:root` 里的变量）
- `_config.yml` 站点标题等配置

## 本地预览（可选）

`_site_preview/` 是本地生成的静态快照（已被 gitignore），随手看效果用；
真实发布以 GitHub 自动构建为准。
