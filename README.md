# ys1145141 的安全笔记

信息安全学习笔记博客，基于 [Hugo](https://gohugo.io/) + [Stack 主题](https://github.com/CaiJimmy/hugo-theme-stack) 构建，托管于 GitHub Pages。

## 博客地址

https://ys1145141.github.io/

## 写新文章

在 `content/post/` 下新建 Markdown 文件：

````markdown
---
title: "文章标题"
description: "一句话描述"
date: 2026-09-28
tags: ["标签1", "标签2"]
categories: ["分类"]
---

正文内容……
````

然后提交推送：

```bash
git add .
git commit -m "新文章：标题"
git push
```

推送后 GitHub Actions 会自动构建发布，约 1 分钟后访问博客即可看到新文章。

## 本地预览（可选）

安装 [Hugo extended](https://gohugo.io/installation/) 后：

```bash
hugo server -D
```

浏览器打开 http://localhost:1313 预览。

## 目录结构

```
myblog/
├── hugo.toml          # 站点配置
├── content/
│   ├── post/          # 文章
│   └── page/          # 独立页面（关于/归档/搜索）
├── static/img/        # 静态资源（头像等）
├── themes/stack/      # Stack 主题
└── .github/workflows/ # GitHub Actions 自动部署
```
