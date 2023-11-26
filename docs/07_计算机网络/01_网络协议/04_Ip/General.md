---
title: General
date: 2022-12-06 17:20:21
permalink: /pages/899276/
categories:
  - 07_计算机网络
  - 03_Ip
tags:
  - 
author: 
  name: xugaoyi
  link: https://github.com/xugaoyi
---
　IP数据包是一种可变长分组，它由首部和数据负载两部分组成。首部长度一般为20-60字节（Byte），其中后40字节是可选的，长度不固定，前20字节格式为固定。数据负载部分的长度一般可变，整个IP数据包的最大长度为65535B。

![image-20221206172210107](https://gikkiares-image-bed.oss-cn-guangzhou.aliyuncs.com/img/image-20221206172210107.png)



# **1、版本号（Version）**

　　　　长度为4位（bit），IP v4的值为0100，IP v6的值为0110。

# **2、首部长度**

　　指的是IP包头长度，用4位（bit）表示，十进制值就是[0,15]，一个IP包前20个字节是必有的，后40个字节根据情况可能有可能没有。如果IP包头是20个字节，则该位应是20/4=5。

选项数据为0-40个字节,所以整个ip包头部为20-60个字节.

首部长度中存储的为 首部字节数/4.

# 3 Tos

比较复杂

```
IP Type of Service(tos)
```





```
https://www.cnblogs.com/HpeMephisto/p/11317686.html
数据包报文格式（IP包、TCP报头、UDP报头）
```

```
2021-1-11 DoS攻击
https://zhuanlan.zhihu.com/p/343381959
```

