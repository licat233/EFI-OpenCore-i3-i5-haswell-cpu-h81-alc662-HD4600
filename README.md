# OpenCore-i3-i5-haswell-cpu-h81-alc662-HD4600-EFI
个人自用最简洁OpenCore引导，除了iMessage不能使用，其它一切正常！

## 配置：
* CPU: 3.3 GHz 四核Intel Core i5 4590  
* 显卡: HD4600 + NVIDIA Quadro K600 
* 主板: intel H81 芯片组 (七彩虹/colorful H81M)   
* 内存: 16 GB 1600 MHz DDR3  
* 网卡+蓝牙：bcm94360cd (免驱网卡 fenvi T919)  
* 声卡：alc662  
* 视频线：HDMI  
* 显示器：23英寸(1920 x 1080)  


## OpenCore版本：0.6.9

> 精简掉了很多不必要的补丁和设置，其它基本已经处于最佳设置，整个 OC 大小仅 3M；  
> 如: 移除了 hfs 补丁，因为0.6.0之后的OC都自带了hfs；  
> 默认config.plist已关闭跑码模式，安装请使用config-debug.plist，安装完成再使用config.plist文件；

## 说明：

1. 如果是intel的wifi和蓝牙，请自行打上补丁，很简单。财力雄厚，可以购买bcm94360网卡；
2. 如果是USB3.0不支持，请自行打上补丁，网上教程一大把；
3. 如果啥问题都没有，那恭喜你，好好享用黑果吧；

## 安装遇到问题？

> <a href="https://heipg.cn/tutorial/opencore-install-errors-handbook.html">1. OpenCore 安装卡住的拯救手册Q&A</a>  
> <a href="https://shuiyunxc.github.io/2020/04/06/Faults/index/">2. OpenCore配置错误、故障与解决办法</a>  
> <a href="https://blog.daliansky.net/">3. 黑果小兵的部落格</a>  
> 4.补充：请留意 Misc -> Security -> secureBootModel 选项是否为Default，已知在10.13.6系统，需设置为Disabled才能进入系统，或者BIOS关闭secureBoot；  
> 5. 引导界面无install选项？①换USB插口，请勿使用USB3.0插口；②扣主板电池；③换U盘，最好准备两个U盘；

按理支持所有Haswell架构处理器，支持的核显：HD4400 ~ HD4600

本人主力工作机已使用两年有余，目前一切正常；

## 适配 macOS 说明：  

* 最新的macOS 12 monterey及以上的系统无法使用；
* 适用系统：macOS 10.13、macOS 10.14、macOS 10.15、macOS 11；
* 推荐 macOS 10.15，再往上就不太适合了；

## Tips：  
1.  OpenCore并非补丁和驱动越多越好，而是越少越好，这里刚入门的小白容易踩雷，误以为补丁越多越好，其实是错的！此 EFI 已经被精简到 3M 大小了，开机速度非常快，基本无卡顿！  
2.  OpenCore版本并不是越新越好，黑果追求的是稳定性，如果用着没什么毛病，没必要追求最新版OC，新版OC会带来新的问题，能用，稳定，无Bug就行，折腾党请便。  

如有遇到问题，欢迎issues！或邮箱：licat233@gmail.com
