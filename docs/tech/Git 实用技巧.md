---
title: Git 实用技巧
description: 整理日常开发中常用的 Git 操作和技巧
category: tech
pubDate: 2026-04-15
tags: [git, 工具, 开发效率]
---

![Git](/images/git-tools.jpg)

## 交互式变基

```bash
git rebase -i HEAD~3
```

## 暂存工作区

```bash
git stash           # 暂存
git stash pop       # 恢复并删除暂存
```

## 查找引入 Bug 的提交

```bash
git bisect start
git bisect bad
git bisect good <commit-hash>
git bisect reset
```

## 格式化日志

```bash
git log --oneline --graph --all
```
