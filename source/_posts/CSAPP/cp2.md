---
title: Bits, Bytes, and Integer
categories:
  - CSAPP
tags:
  - notes
date: 2023-03-22 11:25:43
---
# 信息存储

## 虚拟内存

大多数计算机使用 8 位的块，或者字节(Byte)，作为最小的可寻址的内存单元，而不是访问内存中单独的位。机器级程序将内存视为一个非常大的字节数组，称为虚拟内存(virtual address space)。

内存的每个字节都有一个唯一的地址，所有可能地址的集合就称为虚拟地址空间。

# 有符号和无符号之间的相互转换

![Alt text](../../static/CSAPP/C2UorU2C.png)

## unsigned 和 signed 建议不要混用