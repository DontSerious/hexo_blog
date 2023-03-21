---
title: git
date: 2023-03-18 15:41:53
categories:
- Memo

tags:
- git
---

# 配置
## github用户名邮箱设置
```bash
# --global 全局
git config --global user.name  "username"  
git config --global user.email  "email"
git config --replace-all user.name "name"
git config --replace-all user.email "email"
```

# clone 下来的项目脱离git管理
> 删除.git文件夹  
> `git rm --cached`  
>> 解决“子项目错误”问题，会导致外层git也脱离