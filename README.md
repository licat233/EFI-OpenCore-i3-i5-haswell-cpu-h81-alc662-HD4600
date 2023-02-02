<!--
 * @Author: licat
 * @Date: 2023-01-03 14:20:12
 * @LastEditors: licat
 * @LastEditTime: 2023-02-02 10:55:13
 * @Description: licat233@gmail.com
-->
# OpenCore-i3-i5-haswell-cpu-h81-alc662-HD4600-EFI  

This EFI has been reduced to 3m size. The boot speed is very fast, and there is basically no jam.

The most concise OpenCore EFI boot for personal office computers. Everything is normal except IMessage.  
it supports all i3-i5 processors used in the 4th generation Haswell architecture, and supports core display: hd4400 ~ hd4600

![Monterey 系统截图](https://img.alicdn.com/imgextra/i2/917298378/O1CN01AEuBbc2BlB0YYRlK2_!!917298378.png)

----

**[中文](https://github.com/licat233/EFI-OpenCore-i3-i5-haswell-cpu-h81-alc662-HD4600/blob/main/README-zh.md) | [English](https://github.com/licat233/EFI-OpenCore-i3-i5-haswell-cpu-h81-alc662-HD4600/blob/main/README.md)**

----

## Configuration  

* Cpu:  3.3 GHz quad core Intel Core i5 4590
* Graphics card:  hd4600 + NVIDIA Quadro K600
* Motherboard:  Intel H81 chipset (colorful [C.H81M 全固态版 V22](https://www.colorful.cn/product_show.aspx?mid=84&id=145))
* Memory:  16 GB 1600 MHz DDR3
* Network card + Bluetooth:  bcm94360cd (drive free network card fenvi t919)
* Sound card:  alc662
* Video cable:  HDMI (since K600 graphics card only has DP port, a DP to HDMI adapter is used)
* Display:  23 inches (1920 x 1080)

## OpenCORE Description

> Many unnecessary patches and settings have been simplified, and other settings are basically in the best setting. The entire EFI size is only 3M;
> For example, the HFS patch is removed because OCS after 0.6.0 have their own HFS;
> Please use config debug Plist, and then use config product Plist file;
> Please use the corresponding EFI according to your own system;
> If you install macOS High Sierra, you need to modify the machine time before installation: date 0712122318

## Note: platformInfo must be modified

1. if it is Intel WiFi and Bluetooth, please patch it yourself. It is very simple. With abundant financial resources, you can buy bcm94360 network card;
2. if USB3.0 does not support it, please patch it by yourself and do a lot of online tutorials;
3. if there is no problem, congratulations and enjoy the black fruit;
4. If the wired network card driver fails, please use RealtekRTL8100.kext driver instead;

## Problem with installation?

> 1. [OpenCore installation stuck Rescue Manual QA](https://heipg.cn/tutorial/opencore-install-errors-handbook.html)
> 2. [OpenCore configuration errors, faults and solutions](https://shuiyunxc.github.io/2020/04/06/Faults/index)
> 3. [blog of black fruit soldier](https://blog.daliansky.net/)
> 4. There is no install option in the boot interface?
>
> * ① misc - > Security - > set scan policy to 0;
> * ② UEFI - > UEFI driver - > add these two drivers: OpenHfsPlus.efi、OpenRuntime.efi;

This EFI has been used on my computer for more than two years, and everything is normal at present;

## MacOS adapted

* MacOS High Sierra (I3 CPU recommended, silky experience)
* MacOS Mojave (according to personal preference: the system starts to abandon the AR network card driver and needs to drive it into SLE by itself)
* MacOS Catalina (recommended for i5 CPU, good compatibility, not recommended for I3 CPU, not very smooth)
* MacOS Big Sur (not smooth enough, Not recommended for i3 CPU and i5 CPU)
* MacOS Monterey (try it out. Since the latest version of Monterey has removed the built-in NVIDIA Kepler driver, you need to print the driver by yourself: [install NVIDIA driver tutorial](https://github.com/chris1111/Geforce-Kepler-patcher), Monterey is much smoother than bigsur, and Monterey is recommended for both)
* MacOS Ventura (EFI for this version of the system is under development, please look forward to it)

## Related drives

* Atheros network card driver: the system above MacOS Mojave cancels the support for Atheros network card. If you have an Atheros network card, please call the Atheros network card driver into SLE by yourself. Remember to close SIP and rebuild the cache;
* If your CPU is not successful, please refer to [Black Apple CPU Remax Tutorial]（ https://www.bilibili.com/read/cv16546696/ ）, the key driver CPUFriend.kext has been placed in the dirvers folder;
After successful Remax, the test results are as follows, and the CPU frequency can reach the highest Remax:  
![CPU Remax screenshot](https://img.alicdn.com/imgextra/i2/917298378/O1CN01qwYCFn2BlB0Ul0Nmu_!!917298378.png)  
If the diagram is convenient, you can add these drivers according to your own needs: my own computer Ruipin is normal, so there is no check in config.list  
![Optional drivers can be added according to your needs](https://img.alicdn.com/imgextra/i3/917298378/O1CN01UPeyyN2BlB0VqtmT6_!!917298378.png)  
* Cable network card drive failed?
The reason is that the RealtekRTL8111.kext driver does not support the local wired network card. You need to change it to RealtekRTL8100.kext driver. There are two methods:
① Put the RealtekRTL8100.kext drive into the EFI and restart it;
![Failed to resolve the cable network card driver](https://img.alicdn.com/imgextra/i3/917298378/O1CN01UanqFz2BlB2nKgWz9_!!917298378.png)  
② Put the RealtekRTL8100.kext driver into the SLE. Remember to turn off SIP and rebuild the cache;

## Tips  

1. OpenCORE does not mean that the more patches and drivers, the better, but the less. Novices are prone to misunderstandings.  

2. the OpenCORE version is not as new as possible. Heiguo pursues stability. If there is nothing wrong with using it, there is no need to pursue the latest version of OC. The new version of OC will bring new problems. It can be used, stable, and free of bugs. Please help the party.

## Concluding remarks  

If I can help you, I hope I can give a star
If you have any problems, please issue! Or email: licat233@gmail.com
