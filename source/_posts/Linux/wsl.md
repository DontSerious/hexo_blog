---
title: wsl 备忘基操
date: 2023-02-24 10:24:20

categories:
- Linux

tags:
- Memo
- Wsl
---

# 安装 Debian 代码
```
# 此方法安装默认使用wsl2 之后无需额外设置
wsl --install -d Debian

# 检查版本
cat /etc/issue

# 重装
wsl --unregister Debian
wsl --install -d Debian
```
<!--more-->
# 修改 root 密码
## powershell中输入 设置进入root用户
> Debian config --default-user root
## 进入wsl系统 输入此命令按提示修改密码
> passwd
## powershell 根据个人需求选择是否设置回普通用户
> Debian config --default-user tomato

# 记得换源

# **迁移wsl位置到其他盘**
```
#导出系统
wsl --export Debian E:\Debian2.tar

#取消挂载（删除debian系统）
wsl --unregister Debian

#重新挂载到E盘wsl2目录下
wsl --import Debian E:\wsl2\Debian E:\Debian2.tar
```
