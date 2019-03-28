---
layout: post
title:  "什么是雷电3及其用处"
date:   2018-09-12 18:41:17 +0800
categories: work
tags: work dev
sitemap:
    priority: 1
    changefreq: 'weekly'
---


### 雷电 是 高速传输的硬件接口, 解决的是 
 -  ####   连接线材(数据/视频/供电) 过多的问题.  
 -  ####   连接 扩展组件  

雷电设备可以 拓普 连接  
<br><br>

[雷电3](https://thunderbolttechnology.net/blog/thunderbolt-3-usb-c-does-it-all) 线 是 DisplayPort(视频) 和 PCIEx4(数据) 的汇集.   走的是USB Type-C的物理接口. 雷电3线两头 需要接有 雷电3芯片(负责切换, 实现线路复用). 雷电3芯片有几种版本.  



PCIe 是 外围组件高速互联接口, 可扩展 显卡, 网卡, 磁盘[阵列, 驱动器], 网卡  

<br><br>

雷电3 和 USB3.1 type-c完全不能当一回事, usb-c连接线 两头 有雷电芯片才可能跑的是雷电3, 两个类型的 扩展坞 价格/功能 完全不是一回事.  
这个 挂羊头卖狗肉的典型 [**Hyperdrive**](https://item.jd.com/22849739404.html).  


- 雷电3速率能达到 40Gbps  (40G 比特位(不是字节)/ 每秒)
  -  一个4k 是 4096×2160 × **60Hz** x 32位色 / (1024×1024×1024) = 15.8 Gbps  
  -  也就是说 一个雷电3 带出来两个4K@**60Hz**, 带宽还绰绰有余 ( 40-15.8*2 = 8.4 Gbps )  
  -  这些带宽 8.4Gbps可以分成 USB3.0 (**5Gbps**, 其可扩展成多个口, 共享5Gbps / 500MB/s带宽), 网口什么的  
- usb-c速率 10Gbps
  - 其扩展潜力是 4k@**30Hz**,, 就是 7.91Gbps + 其他    
  

雷电3 同时可以 桥接计算机 传数据. 数据10Gbps对等传输.  
雷电3 同时能提供电力传输.  
雷电3 同时可以组菊花链设备.  

<br><br>
**雷电3应用示例**

- ​    扩展坞  扩展接口 把显示 和 数据 扩展出来. 
  - 带多个显示器, 和 键鼠输入, usb设备.
  - 同时能够给笔记本充电. 方便 笔记本便携.
  - diy 5k显示器, 挂上这个扩展坞

- ​    组件扩展(显卡扩展坞, 外部raid阵列存储).
- ​    数据传输(对等网络传输, 雷电3服务集群). 比如 笔记本和工作站主机  融合 各种共享(文件/网络/外设)
<br><br>

**雷电3 其他用处**

- 双机合璧
  - 桥接对等网, 开远程连接, 文件共享, 磁盘互访, 数据传输 都是超快的.
    - [雷电3对等网络copy文件](https://blog.csdn.net/baidu_23587703/article/details/72873562?utm_source=blogxgwz0).
  - 设备相连  工作站&笔记本    台式机上得有雷电3接口, 带雷电3的主板 [雷电3的主板](http://item.jd.com/5407487.html) 也不是很贵. 新cpu核心也多.
  - 要么[技嘉雷电3](https://www.chiphell.com/thread-1674226-1-1.html)扩展卡(需要主板上有雷电3针脚 -- 看[技嘉卡](http://www.gigabyte.cn/Motherboard/GC-ALPINE-RIDGE-rev-10#ov) 支持的技嘉主板) . 一张卡接入pciex4和DP视频输入 和 TB_HEADER针脚.  还有[华硕的扩展卡](https://www.asus.com/tw/Motherboard-Accessory/ThunderboltEX-3/)(不太推荐).
  - 台式机可以访问用笔记本里面的代码库, 笔记本可以用台式机里面的备份盘. 笔记本可以访问台式机里面的raid资料库.
  - 另外macbook pro 以 目标磁盘模式 或者 以其他磁盘 启动.

- 双机切换   切换笔记本和台式机, 连接计算机组件.
  - 抽出来显卡 显卡扩展坞
  - 扩展坞

- 5k显示器, 就是有双dp口驱动板的那种显示器. diy5k显示器[资料](https://www.youtube.com/watch?v=UfO9aUGQJ6E), 成本不高于 2600.. 咨询经验人.

<br><br>

### HP Elite/ZBook dock 是雷电3 扩展坞

<iframe frameborder="0" style="height:500px; width:800px;" src="https://v.qq.com/txp/iframe/player.html?vid=u0837v7z68f" allowFullScreen="true"></iframe>

​    

**HP Elite/Zbook dock 官方文档与设备解析**

扩展出的 接口  
（1 个）节能型 智能 AC 适配器(65/90/150/200 w), 雷电3/AC混合口 (圆口 4.5*3.0mm).  
（1 个）USB 3.0 端口（充电）   
（3 个）USB 3.0 端口   
（1 个）雷电3/USB-C™ 端口       (可以提供15w的供电, 20Gbps).  
（2 个）DisplayPort 1.2 端口  
（1 个）VGA 端口            (最大1080)  
（1 条）Thunderbolt™/AC电源线   
（1 个）集成线缆锁插槽   
（1 个）千兆以太网端口   
（1 个）麦克风/耳机音频组合插孔    

​    

惠普的笔记本雷电3 dock, 电源适配器分四种功率  65w / 90w / 150w / 200w, 电源输入电压 19.5v . 电流分别 为  3.33A /  4.62A / 7.7A / 10.3A.  

HP dock 其 雷电3口 只能提供60w的供电, HP雷电3线 有个额外的供电圆口, 提高供电功率. 而这个供电口除了在惠普笔记本上其他电脑上用不了的. **如要额外供电    可用辅助供电口 90w~200w 需要电源适配器功率支持**; **一个电源适配器器供电 两个扩展坞 -- 并联两个 -- 辅助供电口 直连 另一个扩展坞电源口.**    

另外在 非**hp**笔记本上, 笔记本电源指示灯和开关键 不好使**.**



官方中文[使用说明](http://h10032.www1.hp.com/ctg/Manual/c05270338)   [该dock的en文档](http://www8.hp.com/h20195/v2/getpdf.aspx/4AA6-5088ENW.pdf)   HP该dock  [常见问题](https://support.hp.com/tw-zh/document/c05144405),  [常见问题En](http://www8.hp.com/h20195/v2/getpdf.aspx/4AA6-5088ENW.pdf). 

其他  [HP dock 65w产品概要参数](http://www8.hp.com/emea_middle_east/en/products/oas/product-detail.html?oid=9822180)   [文档列表](http://h20195.www2.hp.com/v2/default.aspx?cc=emea_middle_east&lc=en&oid=9822180)     [HP扩展坞方案s](http://h20195.www2.hp.com/v2/GetDocument.aspx?docname=c04168358&doctype=quickspecs&doclang=EN_US&searchquery=&cc=uk&lc=en)    

   

​     
**win10/7, macOS  驱动, 固件.**

bios固件, 系统驱动, 扩展坞固件.  

- bios固件和设置(POx支持), mac地址通过, WOL,   


- Win 更新固件, 安装驱动.
  - [EliteBook Dock win_x64驱动固件](https://support.hp.com/us-en/drivers/selfservice/hp-elite-90w-thunderbolt-3-dock/15832458)   [ZBook Dock官方驱动固件](https://support.hp.com/us-en/drivers/selfservice/hp-zbook-dock-with-thunderbolt-3/11122586)
  -  [其他系统驱动](https://pan.baidu.com/s/1o8yKzUdnMgnk0NoNN1Yh4Q) (Windows 7/8/10/Server)


- macOS 切换驱动(打开第三方雷电3设备信任). 
  - 苹果自带雷电3芯片的驱动, 但是不兼容第三方, 官方推荐的[雷3配件](https://www.apple.com/cn/search/thunderbolt3?page=1&sel=accessories&src=globalnav) 及 [雷电3扩展坞2804](https://www.apple.com/cn/shop/product/HKQ12PA/A?fnode=0373457b9b93f7d30fdeeaaf58ddbed0513d4ae0ed2258169d0153fcadde33cc473c1df190a9cb7dfbc0156897440144083511d58235c5338c0f053a421dfc4564599ec09010b8da9bc50797b8cb6873d70ccb73a3af536f19edf4851ab3627c).
  - [MacOS使用HP Dock](https://appleinsider.com/articles/17/10/20/how-to-use-unsupported-thunderbolt-3-docks-and-enclosures-on-sierra-and-high-sierra)   macOS开启第三方雷电3 驱动切换[方法1](https://github.com/KhaosT/tb3-enabler)  [方法2](https://github.com/rgov/Thunderbolt3Unblocker)
  - 注意  苹果macOS升级有时候会驱动变化 或者 校验驱动, 这时候升级有问题. 切换驱动后升级, 再切换回来.

  macOS对硬件的兼容范围和利用能力 是和 windows 有差别的.



​    
**显示接口参数, 转接头, 显示方案**

  - HDMI 接口最普及  
      -  hdmi 1.4 最大  3820x2160 * 30hz   4,096x2,160 * 24 hz  
      -  hdmi 2.0    18Gbps   4k * 60 hz  
  - DP接口 普及少, 由其在电视上;
      -  DP 1.2    3820x2160 * 60hz  
      -  DP 1.3.....  ;   
      -  DP 1.4   8K*60hz  
  - DVI  
      -  单通道  
      -  双通道   2560*1600
  - vga 模拟信号

  

另外 i7-7700k的集显Intel HD Graphics 630  是有5k输出潜力的.   

两个系统 多个显示器@60Hz,  可带两个4K.   需要用到  USB-C口 可以扩展出来 一个显示器.   

win 可以带4台显示器. (macOS一般情况下 对硬件的兼容范围和驱动 一般 没有windows好, macos雷电3扩展坞做多分出来两个显示器, 苹果的设定).  
- 4k+2.5K\*2+FHD  即 4096\*2160 + 2560*1600 * 2 + 1920*1200, 乘以 60Hz和32位色深 = 37,139,251,200 = 37Gbps  
- FHD*4  1920\*1200 * 4, 约17,694,720,000  
- 5k+FHD  

如果 买额外转接头. 注意版本和分辨率.  推荐闲鱼上两个. usb-c转hdmi2.0, 38元/个;  DP1.2转hdmi2.0,  16元/个;  

TODO: diy方案

优点   是市场上最便宜的雷电3扩展坞方案了!  因为买新版 macbook的, 都是雷电3 接口, 坑呀.

​     

**自己笔记本支不支持雷电3 ?**  
​    	搜索笔记本参数  接口参数. 百度搜 "zol 笔记本型号" 看有没有 雷电3/雷劈3 接口.  

​	笔记本 [MBP2016](http://nb.zol.com.cn/604/6045116_param.html)   [zol参数](http://detail.zol.com.cn/1137/1136141/param.shtml)  



macOS nvidia 外置eGPU[打开](https://egpu.io/forums/mac-setup/wip-nvidia-egpu-support-for-high-sierra/)