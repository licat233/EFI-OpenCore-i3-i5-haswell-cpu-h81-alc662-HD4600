# EFI-OpenCore-i3-i5-haswell-cpu-h81-alc662-HD4600
个人自用最简洁OpenCore引导

OpenCore版本：0.6.9

移除了 hfs 补丁，因为0.6.0之后的OC都自带了hfs

安装的时候如果安装不上，请留意secureBootModel选项是否为Default，已知在10.13.6系统，需设置为Disabled才能进入系统；

其它基本已经处于最佳设置

按理支持 所有Haswell处理器

HD4400 ~ HD4600均可

本人目前自用的H81芯片组板无任何问题，一切正常；

说明：OpenCore并非补丁和驱动越多越好，而是越少越好，这里刚入门的小白容易踩雷，误以为补丁越多越好，其实是错的！此 EFI 已经被精简到 3M 大小了，开机速度非常快，基本无卡顿！
如有遇到问题，欢迎issues！

或者联系本人，邮箱：licat233@gmail.com

