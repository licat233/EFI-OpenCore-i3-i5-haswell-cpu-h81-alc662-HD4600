# OpenCore-i3-i5-haswell-h81-alc662-HD4600-EFI
Personal office computer is the most simple OpenCore EFI boot, except iMessage cannot be used, everything else is normal.

----

**[中文](https://github.com/licat233/EFI-OpenCore-i3-i5-haswell-cpu-h81-alc662-HD4600/blob/main/README-zh.md) | [English](https://github.com/licat233/EFI-OpenCore-i3-i5-haswell-cpu-h81-alc662-HD4600/blob/main/README.md)**

----

## Configuration:
* CPU: 3.3 GHz quad-core Intel Core i5 4590
* Graphics Card: HD4600 + NVIDIA Quadro K600
* Motherboard: intel H81 chipset (Colorful H81M)
* Memory: 16 GB 1600 MHz DDR3
* Network card + Bluetooth: bcm94360cd (free drive network card fenvi T919)
* Sound card: alc662
* Video cable: HDMI (because the K600 graphics card only has a DP port, a DP to HDMI adapter is used)
* Display: 23 inches (1920 x 1080)


## OpenCore description:

> A lot of unnecessary patches and settings have been simplified, and others are basically in the best settings, and the entire EFI size is only 3M;
> For example: remove the hfs patch, because the OC after 0.6.0 comes with hfs;
> The default config.plist has turned off the running code mode, please use config-debug.plist for installation, and then use the config.plist file after installation;
> Please use the corresponding EFI according to your system;


## illustrate:

1. If it is intel's wifi and bluetooth, please patch it yourself, it is very simple. Strong financial resources, you can buy bcm94360 network card;
2. If it is not supported by USB3.0, please patch it yourself, there are a lot of online tutorials;
3. If there is no problem, then congratulations, enjoy the black fruit;

## Having trouble installing?

> <a href="https://heipg.cn/tutorial/opencore-install-errors-handbook.html">1. OpenCore installation stuck rescue manual Q&A</a>
> <a href="https://shuiyunxc.github.io/2020/04/06/Faults/index/">2. OpenCore configuration errors, faults and solutions</a>
> <a href="https://blog.daliansky.net/">3. The blog of the black fruit soldier</a>
> 4. Supplement: Please pay attention to whether the Misc -> Security -> secureBootModel option is Default. It is known that in the 10.13.6 system, it needs to be set to Disabled to enter the system, or the BIOS closes secureBoot;
> 5. There is no install option in the boot interface? ①Change the USB socket, do not use the USB3.0 socket; ②Button the motherboard battery; ③Change the U disk, it is best to prepare two U disks;

It is reasonable to support all Haswell architecture processors, supported core graphics: HD4400 ~ HD4600

My main work machine has been used for more than two years, and everything is normal now;

## Adapt to macOS Instructions:

* Applicable systems: MacOS 10.13, MacOS 10.14, MacOS 10.15, MacOS 11;
* The EFI of macos13 Monterey system is added. Since the latest version of Monterey has removed the built-in NVIDIA Kepler driver, you need to print the driver by yourself: [install NVIDIA driver tutorial]（ https://github.com/chris1111/Geforce-Kepler-patcher )；
* Monterey is much smoother than bigsur. Monterey is recommended for both;

## Tips:
1. OpenCore does not mean that the more patches and drivers, the better, but the less the better. The newbie here is easy to step on the thunder. He mistakenly thinks that the more patches the better, it is actually wrong! This EFI has been reduced to 3M size, the boot speed is very fast, and there is basically no lag!
2. The OpenCore version is not the newer the better. Heigo pursues stability. If there is nothing wrong with using it, there is no need to pursue the latest version of OC. The new version of OC will bring new problems. It is usable, stable, and has no bugs. Toss the party please.

If I can help you, I hope I can give a star  
If you encounter problems, welcome issues! Or email: licat233@gmail.com