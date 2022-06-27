# OpenCore-i3-i5-haswell-cpu-h81-alc662-HD4600-EFI
个人办公电脑自用最简洁OpenCore EFI引导，除了iMessage不能使用，其它一切正常。  
理论上支持所有使用于4代Haswell架构i3-i5处理器，支持核显：HD4400 ~ HD4600  

----

**[中文](https://github.com/licat233/EFI-OpenCore-i3-i5-haswell-cpu-h81-alc662-HD4600/blob/main/README-zh.md) | [英文](https://github.com/licat233/EFI-OpenCore-i3-i5-haswell-cpu-h81-alc662-HD4600/blob/main/README.md)**

----

## 配置：
* CPU: 3.3 GHz 四核Intel Core i5 4590  
* 显卡: HD4600 + NVIDIA Quadro K600 
* 主板: intel H81 芯片组 (七彩虹/colorful H81M)   
* 内存: 16 GB 1600 MHz DDR3  
* 网卡+蓝牙：bcm94360cd (免驱网卡 fenvi T919)  
* 声卡：alc662  
* 视频线：HDMI （由于K600显卡只有DP端口，所以使用了一个DP转HDMI的转接头）  
* 显示器：23英寸(1920 x 1080)  


## OpenCore说明：

> 精简掉了很多不必要的补丁和设置，其它基本已经处于最佳设置，整个 EFI 大小仅 3M；  
> 如: 移除了 hfs 补丁，因为0.6.0之后的OC都自带了hfs；  
> 默认config.plist已关闭debug，安装请使用config-debug.plist，安装完成再使用config-product.plist文件；
> 请根据自己系统使用对应的 EFI；


## 说明：一定要修改 PlatformInfo  

1. 如果是intel的wifi和蓝牙，请自行打上补丁，很简单。财力雄厚，可以购买bcm94360网卡；
2. 如果是USB3.0不支持，请自行打上补丁，网上教程一大把；
3. 如果啥问题都没有，那恭喜你，好好享用黑果吧；

## 安装遇到问题？

> 1. [OpenCore 安装卡住的拯救手册Q&A](https://heipg.cn/tutorial/opencore-install-errors-handbook.html)
> 2. [OpenCore配置错误、故障与解决办法](https://shuiyunxc.github.io/2020/04/06/Faults/index)
> 3. [黑果小兵的部落格](https://blog.daliansky.net/)
> 4. 引导界面无install选项？  
> * ①  Misc -> Security -> 设置 Scan Policy 为 0;
> * ②  UEFI -> UEFI驱动 -> 添加这两个驱动：OpenHfsPlus.efi、OpenRuntime.efi;

此EFI在本人工作的电脑已使用两年有余，目前一切正常；

## 已适配 macOS ：  
  - macOS High Sierra （i3 CPU推荐，丝滑体验）
  - macOS Mojave （看个人喜好：该系统开始摒弃了AR网卡驱动，需要自行打驱动到SLE内）
  - macOS Catalina （i5 CPU推荐，兼容性好，i3 CPU不推荐，不太流畅）
  - macOS Big Sur （i3 CPU和i5 CPU都不推荐，流畅度不够）
  - macOS Monterey （尝鲜，由于Monterey最新版本已经移除了内置的英伟达开普勒驱动，所以需要自行打上驱动：[安装Nvidia驱动教程](https://github.com/chris1111/Geforce-Kepler-patcher)，Monterey相较BigSur要流畅得多，两者建议使用Monterey）

## 相关驱动:  
* Atheros网卡驱动：macOS Mojave以上系统取消了对Atheros网卡的支持，如果你的是Atheros网卡，请自行打渠道到SLE内，记得关闭SIP，重建缓存；

## Tips：  
1.  OpenCore并非补丁和驱动越多越好，而是越少越好，这里刚入门的小白容易踩雷，误以为补丁越多越好，其实是错的！此 EFI 已经被精简到 3M 大小了，开机速度非常快，基本无卡顿！  
2.  OpenCore版本并不是越新越好，黑果追求的是稳定性，如果用着没什么毛病，没必要追求最新版OC，新版OC会带来新的问题，能用，稳定，无Bug就行，折腾党请便。  

如果能帮到你，希望能给个Star  
如有遇到问题，欢迎issues！或邮箱：licat233@gmail.com
