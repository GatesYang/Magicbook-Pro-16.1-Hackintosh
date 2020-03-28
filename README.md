# Magicbook-Pro-16.1-Hackintosh 黑苹果稳定版
>Install macOS Catalina 10.15.4 19E266 from Huawei Honor Magicbook Pro 16.1 HBL-W19L

### 详细配置参数
| 项目 | 详细参数|
| :--: | :-------------------- |
| 型号 | Magicbook Pro 16.1 HBL-W19L |
| CPU  | Intel Whiskey Lake i5 8265U & i7-8565U |
| 内存 | DDR4 2666 8G|
| 显卡 | Intel UHD620 2048 MB & NVIDIA MX250|
| 硬盘 | HS(海康威视) C2000 Pro 1TB （自己购买替换的）|
| 声卡 | Realtek ALC 256|
| 触控板 | ELAN 2204|
| 屏幕 | 1920*1080|
| SMBIOS | Macbook Pro 15,4|
| Clover | Updated to 5100|
| OpenCore | Updated to 0.5.6|
| macOS | Up to 10.15.4|

### 关于2019版Magicbook
  经热心群友测试，2019版Magicbook（i3,i5,i7）同样可以使用本efi，触摸板可用，声卡id需改成57
 
### 长期维护更新QQ群
  收到几位帮忙测试的朋友的邮件，都建议我改为收费提供。如果你认为值得，请为技术服务付费（二维码往下拉），享受后期免费维护更新，（价位可以参考淘宝安装黑苹果加格...只是请群主喝杯咖啡而已，群主是真的为这个EFI付出了几百甚至几千小时的努力和心血的）目前新版本都需要解压密码，密码在群中，群中有详细的Clover/OpenCore/PM981还原大法安装教程，还有群主和群友们的热♂心指导，小白也能快速入门！入群9.9元以上看着给吧 QQ群号 963407871

### 更新至此，本Clover/OC EFI除了无线网卡基本完美！

### 更新预告 
* 1.摄像头黑屏修复（Magicbook 2019已经可用）
* 2.更新所有驱动程序
* 3.有朋友私信我锐龙版的能不能安装，AMD的核芯显卡暂时无法驱动，所以不能安装
* 4.WIFI（目前看来硬件上貌似存在PCI通道，但是好像BIOS限制了只能识别CNVI协议的网卡，因此更换DW1560，DW1820A等网卡不能被识别，要华为官方愿意开放BIOS才能更换可用的网卡，经过多次反馈，华为官方说只有反馈的人多了才愿意开放这个BIOS切换选项，这需要大家共同努力向官方反馈，拨打0755-950800，向客服说自己需要使用WiFi6的非cnvi网卡Intel AX200，要求研发部对BIOS进行更新并电话答复，客服态度很好的，但是反馈的人实在是太少了）
* 5.目前远景有大佬在做Intel的wifi驱动，魔法书自带的Intel AC9560 实现了联网使用几个小时，然后报错重启的情况，虽然不能日常使用，但是以后有很大希望能用，离成功也不远了！

### 目前可用的设备
* USB-C/HDMI输出（同时输出正常，加上随航一共4个显示器嘿嘿）
* 核芯显卡
* 触摸板（支持多任务手势）
* 随航（sidecar）有线连接
* 蓝牙（可以冷启动，可以开关，连接正常）
* 扬声器/耳机/麦克风 (AppleALC)
* USB3.0/2.0
* 显示器亮度调节（系统偏好设置-显示器）
* F1,F2亮度调节；F3键盘灯；F4,F5,F6调节音量（静音，音量减，音量加）
* 电池电量显示（快速充电正常）
* 关盖睡眠以及唤醒（休眠耗电正常，盒盖一晚上9个小时耗电0-1%）
* CPU 变频、睿频、超线程正常

### 目前不可用
* 摄像头（Pro版可识别型号但黑屏，Magicbook 2019可用）
* 指纹
* MX250（NVIDIA的老黄和苹果决裂了，估计有生之年是难驱动了）
* intel 9560 WIFI

### 目前三星PM981硬盘只能使用Clover引导*（因为补丁不支持OpenCore）*，同时也只能使用还原大法安装黑苹果，为了解决群友的三星PM981还原大法安装问题，特地更新了Clover 2020.3.25 v3.2，详细更新内容在OpenCore更新内容的下方。但是PM981会遇到偶尔无缘无故死机、重启、无法直接升级系统等等奇怪的问题（详情请百度：黑苹果 PM981），所以想稳定使用黑苹果的话，还是建议换掉PM981硬盘以获得更好的体验，如果使用2019 Pro的话可以加装一个SATA固态硬盘；
### 更新内容 OpenCore
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

-2020.3.18 v3.8 Release
* 1.一些小修小补
* 2.将屏蔽pm981补丁更名为SSDT-Nopm981.aml，以免混淆

-2020.3.17 v3.7 Release
* 1.修复偶尔可能出现的热启动系统失败问题
* 2.使用Nvmefix驱动1.0.2
* 3.修复魔法书Pro的USB-A口苹果设备快充问题（步骤：用OCG在config.plist中，选择Kernel-内核设置-> 添加-> 在USBPorts.kext的最右边勾选“启用”）非Pro的设备可能会导致USB2.0口不可用，无实机进行测试
* 4.如果出现USBwifi不可用的问题，建议大家卸载以前安装的USBwifi驱动（按住Start/Windows键，鼠标单击wifi图标，卸载/Uninstall），然后安装群文件中的Wireless USB Adapter-V11 New.pkg；（防止大家无法联网，特地把pkg安装包打包进OC文件夹）
* 5.关于扬声器声音小的问题，请使用群文件的Boom3D（感谢群友fxxk和407729~）；同时建议大家善用群文件夹“OC安装完以后做的一些优化”

-2020.3.8 v3.6 Release
* 1.一些小修小补，提升稳定性
* 2.优化耗电

-2020.3.7 v3.5 Release
* 1.恢复使用OpenCore 0.5.6官方Release版本，此版开始，不会再适配OC引导Windows，除非OC官方进行完美适配
* 2.在启动界面默认倒计时3秒进入系统是为了方便大家进行Reset NVRAM操作，想在Grub引导选择OpenCore以后直接进入macOS，请参考群文件“跳过引导界面的倒计时.png”
* 3.如果想使用图形化的启动磁盘选择界面，可以用OCG在config.plist中，选择UEFI设置-> UEFI驱动-> 浏览-> 选择Drivers文件夹里面的NdkBootPicker.efi并确定；同时在Misc-其他设置-> Boot-> PickerMode选择“External”
* 4.如果想体验白果的开机声音，可以用OCG到UEFI设置-Audio-勾选AduioSupport和PlayChime，同时在UEFI设置-> UEFI驱动-> 浏览-> 选择Drivers文件夹里面的AudioDxe.efi并确定。（加载此驱动会使得开机慢几秒）
* 5.启动界面为默认图标和背景，可以个性化，自行定制请操作Icons文件夹
* 6.Grub引导：从此版开始，如果想引导Windows，请将群文件中BootMenu文件夹粘贴至EFI文件夹下，使用easyUEFI将BootMenu.efi设置为第一启动项“和设置OpenCore.efi的步骤一模一样”。此为Grub引导，自定义背景图和内容请操作themes文件夹

-2020.3.5 v3.4 Release
* 1.使用OpenCore分支MOD版，更新至OC 0.5.7-2020.3.3
* 2.根据新的OC适配优化选项和设置
* 3.如果想体验白果的开机声音，可以用OCG到UEFI设置-Audio-勾选AduioSupport和PlayChime
* 4.启动界面为默认图标和背景，可以个性化，自行定制请操作Icons文件夹

-2020.3.3 v3.3 Release
* 1.使用OpenCore 0.5.6官方Release，加入NdkBootPicker的OC启动界面UI，自行定制请操作Icons文件夹（感谢@Takagi-sang提供的背景图片）
* 2.更新声卡、显卡等全家桶驱动程序
* 3.为了减少出错，推荐做一次Reset NVRAM，并认真仔细看上面的注意事项！

-2020.3.1 v3.1 Release
* 1.支持C口+HDMI同时输出(测试通过)
* 2.从此版开始，默认的config.plist为已经解锁Cfg-Lock和修改DVMT64M适用的配置（二者缺一不可），config-no-Cfg&DVMT为从未对BIOS进行过高级修改所使用的config（关闭安全启动不算高级更改）

-2020.2.29 v3.0 Release
* 1.使用OpenCore分支MOD版，更新至OC 0.5.6-2020.2.29
* 2.加入选择启动项的时候的背景图片（类似Clover的启动界面）。如果想替换背景图片，请用1920X1080(分辨率必须一模一样，否则不会显示)的PNG图片，替换Icons文件夹里面的background.png
* 3.现在可以直接使用OpenCore引导Windows了（BootCamp Windows）
* 4.修复热补丁和重命名，进行了一些优化（感谢热心群友965987400！）

-2020.2.23 v2.9 Release
* 1.修复USB-C口输出，现在C口和HDMI直接输出都可以热插拔！
* 2.进一步优化睡眠相关设置（经测试盒盖一晚上9小时耗电0%）
* 3.优化安装在SATA固态盘的系统性能
* 4.文件保险箱驱动有问题，暂时移除
* 5.优化耗电情况，提升续航
* 6.替换可用的Android手机USB网络共享驱动HoRNDIS.kext

-2020.2.20 v2.8 Release
* 1.修复直接使用OC安装会默认显示俄语的BUG

-2020.2.20 v2.7 Beta
* 1.更新Android手机USB网络共享驱动HoRNDIS.kext
* 2.修复偶尔出现的屏幕亮度不能保存的问题
* 3.更新OpenCore至0.5.6
* 4.优化CPU调用（CPUFriend）
* 5.调整睡眠唤醒设置

-2020.2.15 v2.6 Beta
* 1.加入Apple设备快充协议支持
* 2.改善不解锁CFG使用时的稳定性

-2020.2.15 v2.5 Beta
* 1.尝试去掉OC启动菜单中的BootCamp Windows
* 2.尝试修复电源小憩

-2020.2.13 v2.3 Release
* 1.修复USB导致的睡眠唤醒问题
* 2.去掉部分无用更名补丁，提升稳定性
* 3.优化外接显示器时的性能
* 4.修复开启Hidpi后可能出现的开机阶段苹果图标变大的问题
* 5.更新蓝牙驱动程序

-2020.2.8 v2.2 Release
* 1.支持HDMI输出4k分辨率，必须在BIOS中更改DVMT为64M，否则无法进入系统，教程位于群文件中
不使用4k输出的话不要使用"config-4k.plist"!!!;
输出4k的话，先删除原有的config.plist,再将config-4k.plist改名成config.plist）
未解锁CFG-Lock的话使用config-cfg.plist或者config-cfg-4k.plist
* 2.修复部分群友反馈的闪屏问题
* 3.一些例行优化和驱动程序更新

-2020.2.6 v2.1(b) Release
* 1.加入续航提升明显的NVMe固态硬盘省电补丁
* 2.如果遇到休眠不能唤醒的情况，请到系统偏好设置的节能中分别关闭电池和电源适配器选项中的“电能小憩”

-2020.2.5 v2.0(b) Release
* 1.更新OpenCore至0.5.5
* 2.加入大量修补
* 3.对睡眠唤醒进行了一定的定制
* 4.更新所有驱动程序
* 5.未解锁CFG的话，把文件夹里面的config.plist删掉，再将config-b.plist改名成confi.plist
* 6.PM981补丁貌似和OC存在冲突，暂时在OC上停止加入PM981补丁

#### a用于PM981&解锁CFG-lock；b用于非981未解锁CFG；c用于981未解锁CFG

-2020.1.30 v1.2 Release
* 1.优化耗电，CPU变频
* 2.修复睡眠，现在睡眠有更好的表现
* 3.修复偶尔开盖唤醒会黑屏的现象
* 4.进行了新的USB定制

-2020.1.22 v1.1a(c) Beta
* 1.重新配置PM981尝试补丁，成功的几率会大一点

-2020.1.22 v1.1(b) Beta
* 1.重新配置config.plist，解决用图形化OCC出现的某些参数问题
* 2.修复开机时候的大苹果图标
* 3.修复开机后黑屏的现象，提升稳定性

-2020.1.21 v1.0a Beta
* 1.加入PM981尝试补丁

-2020.1.21 v1.0 Beta
* 1.更换全新的Opencore引导（v0.5.4）
* 2.去除冲突的驱动、热补丁、更名补丁
* 3.第一版完全满足日常使用要求，Clover能用的在OC里面都能用
* 4.OC也去除了三码，建议大家用Opencore Configurator自行生成以免冲突造成ID被锁！
* 5.OC默认直接进Mac，如果想使用Win10请在开机时按下F12使用Windows Boot Manager进入

### 更新内容 Clover
-2020.3.28 v3.3.1 Release
* 1.增加睡眠时禁用USB设备唤醒的功能(感谢@hjmmc大佬！@Zero大佬！）如果不喜欢，请自行删除SSDT-GPRW和去除重命名GPRW to XPRW
* 2.提升稳定性
* 3.非Pro的群友如果遇到无法使用键盘的情况，请将SSDT-PS2N.aml放入ACPI/patched内，作为应急使用！

-2020.3.25 v3.2 Release
* 1.同步群主的OC最近更新所具备的新特性
* 2.支持至10.15.4，触摸板可用

-2020.3.25 v3.1 Beta
* 1.同步群主的OC最近更新所具备的新特性
* 2.测试版可能会有各种问题（甚至可能无法开机）
* 3.加入pm981补丁
* 4.更新所有驱动程序

-2020.2.13 v2.9 Release
* 1.修复USB导致的睡眠唤醒问题
* 2.修复开启Hidpi后可能出现的开机阶段苹果图标变大的问题
* 3.更新蓝牙驱动程序

-2020.2.8 v2.8 Release
* 1.支持输出4k分辨率，必须在BIOS中更改DVMT为64M，否则无法进入系统，教程位于群文件中
* 不使用4k输出的话不要使用"config-4k.plist"!!!;
* 输出4k的话，先删除原有的config.plist,再将config-4k.plist改名成config.plist）
* 2.尝试修复部分群友反馈的闪屏问题
* 3.一些例行优化和驱动程序更新

-2020.2.6 v2.7 Release
* 1.加入续航提升明显的NVMe固态硬盘省电补丁
* 2.如果遇到休眠不能唤醒的情况，请到系统偏好设置的节能中分别关闭电池和电源适配器选项中的“电能小憩”

-2020.2.5 v2.6 Release
* 1.加入大量修补，力求更稳定省电
* 2.对睡眠唤醒进行了一定的定制
* 3.更新所有驱动程序
* 4.应广大群友萌要求核显的显存改为2048MB

-2020.1.21 v2.5 Release
* 1.回退Clover至5100，解决通过Clover引导进入Win10产生的英特尔智音技术冲突
* 2.蓝牙驱动使用和PM981补丁不冲突的1.0版
* 3.去除无用的驱动
* 4.调整EFI内容，如无意外以后Clover更新频率会减少咯，重心转移到OC了，也欢迎大家继续支持我的OC！

-2020.1.2 v2.3 Beta
* 1.加入@zxystd大神开发的Intel蓝牙驱动IntelBluetoothFirmware
* 2.更新Clover至5102
* 3.更新所有驱动程序
* 4.此版开始抹除三码，大家可以使用自己之前生成的可用三码或者用CloverConfigurator生成新的，以免发生冲突！

-2019.12.21 v2.2 Beta
* 1.修复HDMI，USB-C输出热插拔导致的死机问题

-2019.12.19 v2.1 Beta
* 1.iMessage、Siri完成修复，Facetime可以登陆但是摄像头黑屏
* 2.优化调整ACPI，Driver，Kext目录及内容

-2019.12.14 v2.0 Release
* 1.进一步修复睡眠问题（关盖一晚上耗电0%）
* 2.根据@Takagi-sang的反馈声卡注入ID改为21
* 3.※触摸板（支持多任务手势）
* 4.亮度调节快捷键修复，现在和音量调节（静音，加，减）都是在fn键不亮灯的情况下就可以用了
* 5.随航（sidecar）有线连接可用
* 6.升级Clover至5100（ Clover的升级日志说5098对10.15做了优化，我们的v1.5版刚好是5097）
* 7.电池管理替换成更好的SMCBatteryManager
* 8.添加“文件保险箱”功能所需驱动（有待测试）
* 9.此次更新部分代码参考了[@hjmmc](https://github.com/hjmmc/Honor-Magicbook)大佬的成熟代码，在此表示感谢！
* 10.更新所有驱动程序（AppleALC，Virtual SMC等）

-2019.12.12 v1.5 
* 1.修复UHD620显卡驱动，USB-C输出（1080P@144Hz），HDMI输出（1080P@144Hz），手上没有2K以上的显示器无法测试，但理论上应该都支持
* 2.H.264 & HEVC 解码均修复，目前都可用
* 3.更新Whatevergreen和Lilu
* 4.支持至10.15.2

-2019.11.18 v1.3 
* 1.加入完整的CPU变频、睿频
* 2.支持至10.15.1
* 3.SMBIOS修改成Macbook Pro 15,4

-2019.10.26 v1.2 音频驱动替换为AppleALC（上一版是VoodooHDA）

-2019.10.25 v1.1 
* 1.显卡正确注入为UHD620（上一版是630）
* 2.亮度调节完美
* 3.加入关盖休眠以及唤醒
* 4.更改主题为Black Mojave

-2019.10.25 v1.0 clover升级至5097

### 无法驱动的设备
* WIFI（目前看来硬件上貌似存在PCI通道，但是好像BIOS限制了只能识别CNVI协议的网卡，因此更换DW1560，DW1820A等网卡不能被识别，要华为官方愿意开放BIOS才能更换可用的网卡，经过多次反馈，华为官方说只有反馈的人多了才愿意开放这个BIOS切换选项，这需要大家共同努力向官方反馈，拨打0755-950800，向客服说自己需要使用WiFi6的非cnvi网卡Intel AX200，要求研发部对BIOS进行更新并电话答复，客服态度很好的，但是反馈的人实在是太少了）
* NVIDIA MX250
* 指纹识别

## 关于打赏
如果您认可我的工作，请通过打赏支持我后续的更新(免费的东西长久不了，人都是要恰饭的嘛；已改为收费解压，需微信或支付宝打赏入群。打赏记得发备注你的qq号，然后申请入群时，说一下，我确认后会通过你的验证的。）

|            支付宝                                          |                       微信                           |
| ---------------------------------------------------------- | ---------------------------------------------------- |
| ![Alipay](Alipay1.jpg)                                     | ![Wechat](Wechat1.jpg)                                |

|            QQ群                 |
| ------------------------------- |
| ![963407871](QQ1.jpg)            |

### 说明
作者本人也是黑苹果新手一枚，有Z390 M Gaming的成功安装经历，现在入手了Magicbook Pro但发现全网都没有人做EFI(可能是因为自带的三星PM981?)，所以自己摸索了好多好多天做了一个不完善的EFI，用了TB买的USB网卡，目前看看网页写写文档都没问题，还有一些地方没有完善，希望能和大家交流学习，一起完善这个EFI，我也会长期更新这个EFI！

### 感谢：
* 1.黑苹果长期维护清单[github: Zero-zer0/Matebook_D_2018](https://github.com/Zero-zer0/Matebook_D_2018_Hackintosh_OpenCore)
* 2.黑苹果长期维护清单[github: hjmmc/Honor-Magicbook](https://github.com/hjmmc/Honor-Magicbook)
* 3.黑苹果长期维护清单[github: Zero-zer0/Matebook_13_14_2020](https://github.com/Zero-zer0/Matebook_13_14_2020_Hackintosh_OpenCore)
* 4.黑苹果长期维护清单[github: frezs/MateBook14-Hackintosh](https://github.com/frezs/MateBook14-Hackintosh)
* 5.黑苹果长期维护清单[github: 4323770/Hackintosh-For-Matebook-X](https://github.com/4323770/Hackintosh-For-Matebook-X)
* 6.[黑果小兵][macOS Catalina 10.15.3 19D76 正式版 with Clover 5103原版镜像](https://blog.daliansky.net/macOS-Catalina-10.15.3-19D76-Release-version-with-Clover-5103-original-image-Double-EFI-Version.html)
* 7.[黑果小兵]Hackintool(原Intel FB-Patcher)使用教程及插入姿势
* 8.[远景论坛-微软极客社区](http://www.pcbeta.com)
