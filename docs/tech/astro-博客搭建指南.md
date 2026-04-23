---
title: Astro 博客搭建指南
description: 从零开始用 Astro 搭建一个简洁高效的个人博客
category: tech
date: 2026-04-20
tags: [astro, 博客, 前端]
---

![Astro](/images/astro-blog.jpg)

## 为什么选择 Astro

Astro 是一个现代静态站点生成器，专为内容型网站设计。它的核心优势：

- **零 JavaScript 默认** — 页面默认不发送 JS，加载飞快
- **Islands 架构** — 按需水合，只有交互组件才加载 JS
- **内容集合** — 内置 Markdown/MDX 支持，带类型安全的 frontmatter 验证
- **多框架支持** — 可以混用 React、Vue、Svelte 等组件

## 快速开始

```bash
npm create astro@latest my-blog
cd my-blog
npm run dev
```

## 部署

- **Vercel** — `npm i vercel && vercel`
- **Netlify** — 连接 Git 仓库自动部署
- **GitHub Pages** — 使用 `@astrojs/github-pages` 适配器
