---
title: Untitled
date: 2023-06-14 17:09:09
permalink: /pages/75c99b/
categories:
  - 07_计算机网络
tags:
  - 
author: 
  name: xugaoyi
  link: https://github.com/xugaoyi
---

1,MTU的概念

MTU，全称为Maximum Transmission Unit，即最大传输单元，它是数据链路层的概念，指以太网数据通信时，链路层上一次性允许通过或转发的数据帧的最大尺寸。MTU通常与通信接口关联，即同一设备的不同接收/转发接口的MTU值可能不同。MTU值一般以字节为单位，常见结构和字节占比如下图所示。

![img](https://gikkiares-image-bed.oss-cn-guangzhou.aliyuncs.com/img/ce7335a5aabe4583af030a6810693752.png)



由于MTU限制了链路层一次性转发的数据帧尺寸，当数据包尺寸大于接收端MTU值时，就需要对数据包进行拆分传输，或者直接丢弃。拆分传输的过程也称为分片，即在网络层将数据包分解为若干个尺寸小于或等于MTU值的小的数据包，每个分片数据包都会带有一个IP报头，这些被拆分后的小的数据包称为数据碎片。在拆分传输完成后，需要对各数据碎片进行重组，通过各分片IP报头中的标识位、偏移量信息，能够唯一标识特定数据包的特定数据碎片，然后即可按序完成数据包重组。但是，分片和重组过程会增加额外的资源消耗，加重网络传输的负担。



# ip数据包分片

![img](https://gikkiares-image-bed.oss-cn-guangzhou.aliyuncs.com/img/39325b5ac0d04e3ab7df1ecb4e0751da.png)



(1) PMTU

PMTU全称为Path Maximum Transmission Unit，即路径MTU。对于一条IP路径，其MTU值是指在不分片情况下路径上所能传输的最大数据包尺寸，等于该路径上的最小MTU值，所以PMTU的值由路径上所有MTU共同决定。通过MTU间接改变PMTU值，就能够有效避免分片重组，提高网络带宽的利用率。









```
MTU是什么
https://www.ruijie.com.cn/jszl/90149/
```

