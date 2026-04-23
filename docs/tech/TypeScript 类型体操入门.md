---
title: TypeScript 类型体操入门
description: 掌握 TypeScript 高级类型，写出更安全的代码
category: tech
date: 2026-04-18
tags: [typescript, 前端, 编程]
---

![TypeScript](/images/typescript.jpg)

## 基础泛型

```typescript
function identity<T>(arg: T): T {
  return arg
}
```

## 条件类型

```typescript
type IsString<T> = T extends string ? true : false
type A = IsString<'hello'>  // true
```

## 映射类型

```typescript
type Readonly<T> = {
  readonly [K in keyof T]: T[K]
}
```

## 实战：DeepPartial

```typescript
type DeepPartial<T> = {
  [K in keyof T]?: T[K] extends object ? DeepPartial<T[K]> : T[K]
}
```
