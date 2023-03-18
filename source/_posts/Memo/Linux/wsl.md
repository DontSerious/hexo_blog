---
title: wsl 备忘基操
date: 2023-02-24 10:24:20

categories:
- Memo

tags:
- Wsl
- Linux
---
# 安装 WSL
```
# 此方法安装默认使用wsl2 之后无需额外设置
wsl --install -d Debian

# 检查版本
cat /etc/issue

# 重装
wsl --unregister Debian
wsl --install -d Debian
```
## 修改 root 密码
### powershell中输入 设置进入root用户
> Debian config --default-user root
### 进入wsl系统 输入此命令按提示修改密码
> passwd
### powershell 根据个人需求选择是否设置回普通用户
> Debian config --default-user tomato

## 记得换源

## 迁移wsl位置到其他盘
```
#导出系统
wsl --export Debian E:\Debian2.tar

#取消挂载（删除debian系统）
wsl --unregister Debian

#重新挂载到E盘wsl2目录下
wsl --import Debian E:\wsl2\Debian E:\Debian2.tar
```

# WSL操作
## 配置WSL性能
在文件 `%USERPROFILE%\.wslconfig` 中配置
```Bash
# Settings apply across all Linux distros running on WSL 2
[wsl2]

# Limits VM memory to use no more than 4 GB, this can be set as whole numbers using GB or MB
memory=4GB 

# Sets the VM to use two virtual processors
processors=2

# Specify a custom Linux kernel to use with your installed distros. The default kernel used can be found at https://github.com/microsoft/WSL2-Linux-Kernel
kernel=C:\\temp\\myCustomKernel

# Sets additional kernel parameters, in this case enabling older Linux base images such as Centos 6
kernelCommandLine = vsyscall=emulate

# Sets amount of swap storage space to 8GB, default is 25% of available RAM
swap=8GB

# Sets swapfile path location, default is %USERPROFILE%\AppData\Local\Temp\swap.vhdx
swapfile=C:\\temp\\wsl-swap.vhdx

# Disable page reporting so WSL retains all allocated memory claimed from Windows and releases none back when free
pageReporting=false

# Turn off default connection to bind WSL 2 localhost to Windows localhost
localhostforwarding=true

# Disables nested virtualization
nestedVirtualization=false

# Turns on output console showing contents of dmesg when opening a WSL 2 distro for debugging
debugConsole=true
```