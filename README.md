# Magicbook-Pro-16.1-Hackintosh 黑苹果稳定版
>Install macOS Catalina 10.15.2 19C57 from Huawei Honor Magicbook Pro 16.1 HBL-W19L

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
| OpenCore | Updated to 0.5.4|

大家直接在Release下载吧，不在code里面上传更新了
[GatesYang/Magicbook-Pro-16.1-Hackintosh/releases](https://github.com/GatesYang/Magicbook-Pro-16.1-Hackintosh/releases)

### 关于2019版Magicbook
  经热心群友测试，2019版Magicbook（i3,i5,i7）同样可以使用本efi，触摸板可用，声卡id需改成57
 
### 长期维护更新QQ群
  收到几个帮忙测试的朋友的邮件，都建议我改为收费提供。如果你认为值得，请为技术服务付费（二维码往下拉），享受后期免费维护更新，目前新版本都需要解压密码，密码在群中，入群9.9元以上看着给吧。QQ群号 963407871

### 更新至此，本Clover EFI除了无线网卡基本完美！

### 更新预告 
* 1.现在正在全力折腾OC，目前OC触摸板和声卡不能用，还在探索阶段，尝鲜包发在群里（这句话刚写出来几个小时后，OC就折腾接近完美了，嘿嘿😄）
* 2.摄像头黑屏修复（Magicbook 2019可用）
* 3.更新所有驱动程序
* 4.有朋友私信我锐龙版的能不能安装，我暂时没有实机进行测试（本EFI基于IntelCPU，不能直接用于AMD！），理论上AMD暂时只能支持到10.14.5
* 5.WIFI（目前看来硬件上貌似存在PCI通道，但是好像BIOS限制了只能识别CNVI协议的网卡，因此更换DW1560，DW1820A等网卡不能被识别，要华为官方愿意开放BIOS才能更换可用的网卡，经过多次反馈，华为官方说只有反馈的人多了才愿意开放这个BIOS切换选项，这需要大家共同努力向官方反馈，拨打0755-950800，向客服说自己需要使用WiFi6的非cnvi网卡Intel AX200，要求研发部对BIOS进行更新并电话答复，客服态度很好的，但是反馈的人实在是太少了）

### 更新内容（使用OC引导必须解锁CFG-Lock）
-2020.1.21 v1.0a Beta
* 1.加入PM981尝试补丁

-2020.1.21 v1.0 Beta
* 1.更换全新的Opencore引导（v0.5.4）
* 2.去除冲突的驱动、热补丁、更名补丁
* 3.第一版完全满足日常使用要求，Clover能用的在OC里面都能用
* 4.OC也去除了三码，建议大家用Opencore Configurator自行生成以免冲突造成ID被锁！
* 5.OC默认直接进Mac，如果想使用Win10请在开机时按下F12使用Windows Boot Manager进入

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
* 9.此次更新部分代码参考了@hjmmc的成熟代码，在此表示感谢！
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

### 目前可用的设备
* USB-C/HDMI输出（没尝试过同时输出，等有条件的机油测试反馈8）
* 核芯显卡 (正确识别成UHD620 Mobile Whiskey Lake)
* 触摸板（支持多任务手势）
* 随航（sidecar）有线连接
* 蓝牙（可以冷启动，可以开关，连接正常，目前未发现BUG）
* 扬声器/耳机/麦克风 (AppleALC)
* USB3.0/2.0
* 显示器亮度调节（系统偏好设置-显示器）
* F1,F2亮度调节；F3键盘灯；F4,F5,F6调节音量（静音，音量减，音量加）
* 电池电量显示（快速充电正常）
* 关盖睡眠以及唤醒（休眠耗电正常）
* CPU 变频(900MHz~3900MHz)，11个档位，睿频正常

### 目前不可用
* 摄像头（Pro版可识别型号但黑屏，Magicbook 2019可用）

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
作者本人也是黑苹果新手一枚，有Z390 M Gaming的成功安装经历，现在入手了Magicbook Pro但发现全网都没有人做EFI(可能是因为自带的三星PM981?)，所以自己摸索了好多好多好多好多好多天做了一个不完善的EFI，用了TB买的USB网卡，目前看看网页写写文档都没问题，还有一些地方没有完善，希望能和大家交流学习，一起完善这个EFI，我也会长期更新这个EFI！

### 感谢：
* 1.黑苹果长期维护清单[github: hjmmc/Honor-Magicbook](https://github.com/hjmmc/Honor-Magicbook)
* 2.黑苹果长期维护清单[github: frezs/MateBook14-Hackintosh](https://github.com/frezs/MateBook14-Hackintosh)
* 3.黑苹果长期维护清单[github: 4323770/Hackintosh-For-Matebook-X](https://github.com/4323770/Hackintosh-For-Matebook-X)
* 4.[黑果小兵]macOS Catalina 10.15.2 19C57 正式版 with Clover 5100原版镜像[双EFI双平台版]
* 5.[黑果小兵]Hackintool(原Intel FB-Patcher)使用教程及插入姿势
* 6.[远景论坛-微软极客社区](http://www.pcbeta.com)
