# Magicbook-(Pro)-16.1-Hackintosh-2019&2020 黑苹果稳定版
>Install macOS Catalina 11.0 20A5354i from Huawei Honor Magicbook (Pro) 2019&2020

### 详细配置参数
| 项目 | 详细参数|
| :--: | :-------------------- |
| 型号 | Magicbook (Pro) 2019&2020 |
| CPU1 | Intel Whiskey Lake i3-8145U & i5 8265U & i7-8565U |
| CPU2 | Intel Comet Lake i5-10210u & i7-10710U |
| 内存 | DDR4 2666 8G|
| 显卡 | Intel UHD620 2048 MB & NVIDIA MX250|
| 硬盘 | HS(海康威视) C2000 Pro 1TB （自己购买替换的）|
| 声卡 | Realtek ALC 256|
| 触控板 | ELAN 2204|
| 屏幕 | 1920*1080|
| SMBIOS | Macbook Pro 15,4|
| Clover | Updated to 5100|
| OpenCore | Updated to 0.6.1|
| macOS | Up to 11.0 Big Sur Public Beta 2|

### 关于2020版Magicbook（Pro）
  2020已经完成适配，各功能正常！
### 关于2019版Magicbook
  本群已适配2019&2020版非Pro（i3,i5,i7）的Magicbook，同步所有更新的特性
 
### 长期维护更新QQ群
  收到几位帮忙测试的朋友的邮件，都建议我改为收费提供。如果你认为值得，请为技术服务付费（二维码往下拉），享受后期免费维护更新，理论上永久更新至荣耀官方放弃这台机子（价位可以参考淘宝安装黑苹果价格，tb安装的还不会给你更新哦。只是请群主喝杯咖啡而已，群主为这个EFI真的是付出了几百甚至几千小时的努力和心血的）目前新版本都需要解压密码，密码在群中，群中有详细的Clover/OpenCore/PM981还原大法安装教程，还有群主和群友们的热♂心指导，小白也能快速入门！入群9.9元以上看着给吧 QQ群号 963407871

### 群中已经有内置Intelwifi的测试驱动，日常使用没毛病

### 目前可用的设备
* intel 9560 cnvi Wifi（日常使用完美）2020版本的MagicBook Pro也支持
* USB-C/HDMI输出（同时输出正常，加上随航一共4个显示器没毛病，亲测！）
* 随航（sidecar）有线连接
* 核芯显卡
* 触摸板（支持多任务手势）
* 蓝牙（可以冷启动，可以开关，连接正常）
* 扬声器/耳机/麦克风 (AppleALC)
* USB3.0/2.0
* 显示器亮度调节（系统偏好设置-显示器）
* F1,F2亮度调节；F3键盘灯；F4,F5,F6调节音量（静音，音量减，音量加）
* 电池电量显示（快速充电正常）
* 关盖睡眠以及唤醒（休眠耗电正常，盒盖一晚上9个小时耗电0-1%）
* CPU 变频、睿频、超线程正常

### 更新内容 OpenCore
-2020.9.24 v5.0.1 Release
* 1.对Big Sur Developer Beta 8 进行细节适配，经测试可以直接全新安装

-2020.9.8 v5.0 Release
* 1.同步OpenCore0.6.1更新
* 2.更新所有驱动程序
* 3.内置Z大 itlwm 1.0.0 Release
* 4.经测试可以直接全新安装Big Sur Public Beta 2

-2020.8.8 v4.9 Release
* 1.修复已知问题，更新支持至Big Sur Beta4

-2020.7.16 v4.8 Beta
* 1.更新至OpenCore 0.6.0beta，以支持Big Sur

-2020.6.10 v4.7.2 Release
* 1.加入z大编写的itlwm至开机启动项（可切换不同的wifi）

-2020.6.2 v4.7.0 Release
* 1.同步OpenCore0.5.9更新
* 2.更新所有驱动程序
* 3.下一版更新将加入z大编写的itlwm（可切换不同的wifi）

-2020.5.17 v4.6.6 Release
* 1.修复OC0.5.8下的触摸板BUG
* 2.如果遇到开机后半段进度条特别慢的情况，请在进入桌面后第一时间重启（关机也会变慢），出现这种情况是因为蓝牙驱动出问题了，目前只能等蓝牙大佬更新

-2020.5.9 v4.6 Release
* 1.内测群友更新至OC 0.5.8

-2020.4.29 v4.5 Release
* 1.Pro的声卡使用[@hjmmc](https://github.com/hjmmc)大佬定制的AppleALC，非Pro无实机，无法提取CodeC，后续继续优化
* 2.使用[@Zero-zer0](https://github.com/Zero-zer0)大佬提供的触摸板驱动，优化流畅度的同时新增支持模拟“单指用力点按”（需要自行在[系统偏好设置-触摸板]中设置）
* 3.降低了开机挂蓝牙的几率
* 4.此版开始，Pro和非Pro分开更新，请注意！
* 5.一些常规优化

-2020.4.8 v4.4.1 Release
* 1.更新OpenCore至v0.5.7 release
* 2.更新所有驱动程序（Lilu、AppleALC、Nvmefix等）

-2020.3.28 v4.3 Release
* 1.增加睡眠时禁用USB设备唤醒的功能(感谢[@hjmmc](https://github.com/hjmmc/Honor-Magicbook)大佬！[@Zero-zer0](https://github.com/Zero-zer0)大佬！）如果不喜欢，请自行取消勾选SSDT-GPRW和去除重命名GPRW to XPRW
* 2.添加USBPorts-noPro.kext，为非Pro群友定制USB实现苹果设备快充等功能(感谢热心群友@xh和@江枫 的测试！)

-2020.3.25 v4.2 Release
* 1.更新支持10.15.4，触摸板可用
* 2.此版开始Pro和非Pro重新合并成一个config，请注意！

-2020.3.25 v4.1 Release
* 1.修改ScanPolicy，解决部分群友奇奇怪怪的无法引导进U盘进行全新安装的现象(如果出现Time Machine或者BOOTCAMP Windows等等其它引导为默认第一启动项的情况，请用上下键选择至Mac OS，然后按下Ctrl+Enter，即可设置Mac OS为“默认启动项”
* 2.一些常规优化

-2020.3.20 v4.0 Release
* 1.在[@Zero-zer0](https://github.com/Zero-zer0) 大佬的帮助下，进一步优化2019非Pro机型的触摸板！！！从本次更新开始，Pro和非Pro将使用不同的config.plist！

-2020.3.20 v3.9 Release
* 1.在[@Zero-zer0](https://github.com/Zero-zer0) 大佬的帮助下，对SSDT和重命名进行完全优化！
* 2.在[@Zero-zer0](https://github.com/Zero-zer0) 大佬的帮助下，对触摸板进行灵敏度，跟手程度，手势优化！同时修复10.15.4beta触摸板不可使用的BUG
* 3.[@Zero-zer0](https://github.com/Zero-zer0) 大佬是华为黑苹果圈里的真大佬，为Matebook D 2018和Matebook 2020做了巨大的贡献，大家可以给大佬的这两个项目点个Star支持一下！[@Zero-zer0](https://github.com/Zero-zer0) 有能力的朋友也可以请大佬喝杯咖啡，毕竟黑苹果的长期优化真的是需要非常多耐心和时间的付出，还要冒着搞坏电脑然后走售后的风险，一次又一次地用自己的电脑来测试（我自己就搞坏过一次主板，还花钱返修了）。支持一下大佬，让大佬可以开开心心地继续维护项目！黑苹果是一个长期的优化过程，一直伴随着每一次驱动程序的更新和系统更新！

### 更新内容 Clover
-2020.4.7 v3.4 Release
* 1.修改USBports相关，去掉USBpower
* 2.更新所有驱动程序（Lilu、AppleALC、Nvmefix等）

## 关于打赏
如果您认可我的工作，请通过打赏支持我后续的更新(免费的东西长久不了，维护黑果很累的，伴随每次系统或者引导更新，都需要大量时间进行适配和优化；目前已改为收费解压，需微信或支付宝打赏入群，相比tb来说已经非常非常良心了。打赏记得发备注你的qq号，然后申请入群时，说一下，我确认后会通过你的验证的，如果GitHub图挂了，可以挂代理后刷新页面，或者直接在搜QQ群在群成员列表找群主哈）

|            支付宝                                          |                       微信                           |
| ---------------------------------------------------------- | ---------------------------------------------------- |
| ![Alipay](Alipay1.jpg)                                     | ![Wechat](Wechat1.jpg)                                |

|            QQ群                 |
| ------------------------------- |
| ![963407871](QQ1.jpg)            |


### 目前不可用
* 摄像头（Pro版可识别型号但黑屏，Magicbook 2019可用）
* 指纹
* MX250（NVIDIA的老黄和苹果决裂了，估计有生之年是难驱动了）

### 目前三星PM981硬盘只能使用Clover引导*（因为补丁不支持OpenCore）*，同时也只能使用还原大法安装黑苹果，为了解决群友的三星PM981还原大法安装问题，特地更新了Clover 2020.3.25 v3.2，详细更新内容在OpenCore更新内容的下方。但是PM981会遇到偶尔无缘无故死机、重启、无法直接升级系统等等奇怪的问题（详情请百度：黑苹果 PM981），所以想稳定使用黑苹果的话，还是建议换掉PM981硬盘以获得更好的体验，如果使用2019 Pro的话可以加装一个SATA固态硬盘；

### 感谢：
* 1.黑苹果长期维护清单[github: Zero-zer0/Matebook_D_2018](https://github.com/Zero-zer0/Matebook_D_2018_Hackintosh_OpenCore)
* 2.黑苹果长期维护清单[github: hjmmc/Honor-Magicbook](https://github.com/hjmmc/Honor-Magicbook)
* 3.黑苹果长期维护清单[github: Zero-zer0/Matebook_13_14_2020](https://github.com/Zero-zer0/Matebook_13_14_2020_Hackintosh_OpenCore)
* 4.黑苹果长期维护清单[github: frezs/MateBook14-Hackintosh](https://github.com/frezs/MateBook14-Hackintosh)
* 5.黑苹果长期维护清单[github: 4323770/Hackintosh-For-Matebook-X](https://github.com/4323770/Hackintosh-For-Matebook-X)
* 6.[黑果小兵][macOS Catalina 10.15.3 19D76 正式版 with Clover 5103原版镜像](https://blog.daliansky.net/macOS-Catalina-10.15.3-19D76-Release-version-with-Clover-5103-original-image-Double-EFI-Version.html)
* 7.[黑果小兵]Hackintool(原Intel FB-Patcher)使用教程及插入姿势
* 8.[远景论坛-微软极客社区](http://www.pcbeta.com)
