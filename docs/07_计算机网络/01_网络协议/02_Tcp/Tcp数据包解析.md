---
title: Tcp数据包解析
date: 2022-12-06 17:25:56
permalink: /pages/8ccc41/
categories:
  - 07_计算机网络
  - 02_Tcp
tags:
  - 
author: 
  name: xugaoyi
  link: https://github.com/xugaoyi
---
![image-20221206172621541](https://gikkiares-image-bed.oss-cn-guangzhou.aliyuncs.com/img/image-20221206172621541.png)

TCP报文由首部和数据两部分组成。首部一般由20-60字节（Byte）构成，长度可变。其中前20B格式固定，后40B为可选。

 　因为，TCP报文还得传给下层网络层，封装成IP包，而一个IP包最大长度为65535，同时IP包首部也包含最少20B，所以一个IP包或TCP包可以包含的数据部分最大长度为65535-20-20=65495B。

 　TCP报文中数据部分是可选的，即TCP报文可以不包含数据（同理IP包也可以不包含数据）。不含数据的TCP报文通常是一些确认和控制信息类的报文，如TCP建立连接时的三次握手和TCP终止时的四次挥手等。



Tcp中填充的数据,为应用层实际传输的数据.

# 数据偏移

数据偏移是那个字节中的高四位,这个图片上的0-8的顺序还是有问题.



# 标志

```
public static final int FIN = 0x01;
public static final int SYN = 0x02;
public static final int RST = 0x04;
public static final int PSH = 0x08;
public static final int ACK = 0x10;
public static final int URG = 0x20;
```

可见,每个字节,左边表示高位,右边表示地位.



Tcp:Transmission Control Protocol

Udp:User Datagram Protocol 用户数据报协议



Ddp:Dlks Datagram Protocol 多路快收 数据报协议.