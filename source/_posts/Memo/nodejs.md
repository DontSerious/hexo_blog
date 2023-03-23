---
title: nodejs
date: 2023-03-18 15:48:52
categories:
- Memo

tags:
- nodejs

toc: true
---

# 1. Linux下使用包管理安装
**[github教程](https://github.com/nodesource/distributions)**

# 2. 换源
因为nrm(NPM registry manager)会因为使用国外源导致无法安装，所以没有魔法就先得使用手动方法换源后安装。
## 2.1. 手动方法
### 2.1.1. 查看源
```
npm config get registry
```
### 2.1.2. 更换源
这里先使用taobao源
```
npm config set registry https://registry.npmmirror.com/
```
> 这个配置会持久化保存到 ~/.npmrc 文件中，你也可以通过手动改该文件来修改配置。
## 2.2. nrm
### 2.2.1. 安装
```
npm i -g nrm
```
### 2.2.2. 使用
```
$ nrm ls

  npm ---------- https://registry.npmjs.org/
  yarn --------- https://registry.yarnpkg.com/
  tencent ------ https://mirrors.cloud.tencent.com/npm/
  cnpm --------- https://r.cnpmjs.org/
  taobao ------- https://registry.npmmirror.com/
  npmMirror ---- https://skimdb.npmjs.com/registry/
```
**应用**
```
$ nrm use taobao


   Registry has been set to: https://registry.npmmirror.com/
```