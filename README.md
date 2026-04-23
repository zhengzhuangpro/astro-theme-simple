# astro-theme-simple

一个简洁的 Astro 博客主题模板，支持深色/浅色模式、全文搜索、代码高亮等功能。

## 功能特性

- 深色/浅色/跟随系统三种主题模式
- 全文搜索（支持 `⌘ K` 快捷键）
- 文章分类和标签
- 代码语法高亮（Shiki - GitHub Dark 主题）
- 代码块一键复制
- 图片点击灯箱预览
- 文章目录导航（大屏侧边栏）
- 响应式设计，移动端友好
- 智能返回导航
- RSS 订阅
- Sitemap 自动生成

## 快速开始

### 1. 克隆仓库

```bash
git clone https://github.com/your-username/astro-theme-simple.git
cd astro-theme-simple
```

### 2. 安装依赖

```bash
pnpm install
```

### 3. 修改配置

编辑 `src/config.ts`，设置你的站点信息：

```ts
export const siteConfig = {
  title: 'My Blog',
  description: 'A minimal Astro blog',
  site: 'https://your-domain.com',
  ogImage: '/favicon.ico',
  author: 'Your Name',
  nav: [
    { label: '首页', href: '/' },
    { label: '分类', href: '/categories' },
    { label: 'GitHub', href: 'https://github.com/your-username', external: true },
  ],
  footer: '© {year} {title}. All rights reserved.',
}
```

编辑 `astro.config.mjs`，将 `site` 改为你的域名：

```ts
export default defineConfig({
  site: 'https://your-domain.com',
  // ...
})
```

### 4. 添加文章

在 `docs/` 目录下创建 Markdown 文件：

```md
---
title: 我的第一篇文章
description: 文章描述
category: 技术
tags: [Astro, 博客]
date: 2025-01-01
---

文章内容...
```

### 5. 启动开发服务器

```bash
pnpm dev
```

### 6. 构建

```bash
pnpm build
```

构建产物在 `dist/` 目录，可以部署到任何静态托管服务。

## 配置项说明

| 字段 | 说明 |
|------|------|
| `title` | 站点名称，显示在导航栏和页面标题 |
| `description` | 站点描述，用于首页和 SEO |
| `site` | 站点完整 URL，用于 sitemap 和 RSS |
| `ogImage` | Open Graph 图片路径 |
| `author` | 作者名称 |
| `nav` | 导航链接数组，`external: true` 会在新标签页打开 |
| `footer` | 页脚文本，支持 `{year}` 和 `{title}` 占位符 |

## 目录结构

```
├── src/
│   ├── config.ts             # 主题配置
│   ├── content.config.ts     # 内容集合配置
│   ├── layouts/              # 页面布局
│   └── pages/                # 页面路由
├── docs/                     # Markdown 文章
├── public/                   # 静态资源
└── astro.config.mjs          # Astro 配置
```

## 技术栈

- [Astro](https://astro.build) - 静态站点生成器
- [Shiki](https://shiki.style) - 代码语法高亮
- TypeScript
