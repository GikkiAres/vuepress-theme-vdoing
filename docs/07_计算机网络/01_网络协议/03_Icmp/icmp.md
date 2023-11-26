---
title: icmp
date: 2022-12-06 18:35:02
permalink: /pages/de4742/
categories:
  - 07_计算机网络
  - 01_网络协议
  - 03_Icmp
tags:
  - 
author: 
  name: xugaoyi
  link: https://github.com/xugaoyi
---


![image-20221206183508438](https://gikkiares-image-bed.oss-cn-guangzhou.aliyuncs.com/img/image-20221207171223381.png)

icmp数据报的报头部分是8个字节.



# 控制每个包数据payload的大小

即icmp的数据部分的长度.

```
ping -s 32 192.168.109.1
```

Linux平台上默认每个包的 payload 是56，最大是 65507

Windows默认是 32，最大是 65500，Windows平台所用参数是 -l

linux参数是-s.

可以设置为0.



# 1 Linux下ping命令

icmp报头是8字节.

Linux下的ping命令产生的ICMP报文大小是（56+8）64个字节，其中56是ICMP报文数据部分长度，8是ICMP报头部分长度。



```
-l size       指定发送的数据包的大小，默认发送的数据包大小为32byte。
```

```
配合 -s 大包来压测服务器
```





```
https://www.cnblogs.com/mmzql/p/14584552.html
ICMP报文结构
```

```
https://zhuanlan.zhihu.com/p/519694134
ICMP小结
```

