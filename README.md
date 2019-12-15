# Magicbook-Pro-16.1-Hackintosh 黑苹果稳定版
>Install macOS Catalina 10.15.2 19C57 from Huawei Honor Magicbook Pro 16.1 HBL-W19L

### 详细配置参数
| 项目 | 详细参数|
| :--: | :-------------------- |
| 型号 | Magicbook Pro 16.1 HBL-W19L |
| CPU  | Intel Whiskey Lake i5 8265U |
| 内存 | DDR4 2666 8G|
| 显卡 | Intel UHD620 2048 MB & NVIDIA MX250|
| 硬盘 | HS(海康威视) C2000 Pro 1TB （自己购买替换的）|
| 声卡 | Realtek ALC 256|
| 触控板 | ELAN 2204|
| 屏幕 | 1920*1080|
| SMBIOS | Macbook Pro 15,4|
| Clover | Updated to 5100|

大家直接在Release下载吧，不在code里面上传更新了
[GatesYang/Magicbook-Pro-16.1-Hackintosh/releases](https://github.com/GatesYang/Magicbook-Pro-16.1-Hackintosh/releases)
 
### 长期维护更新QQ群
  收到几个帮忙测试的朋友的邮件，都建议我改为收费提供。如果你认为值得，请为技术服务付费，享受后期免费维护更新，目前新版本都需要解压密码，密码在群中，入群9.9元以上看着给吧。QQ群号 963407871

### 更新预告 
* 1.iMessage、Facetime、Siri
* 2.更新所有驱动程序
* 3.有朋友私信我锐龙版的能不能安装，我暂时没有实机进行测试（本EFI基于IntelCPU，不能直接用于AMD！），理论上AMD暂时只能支持到10.14.5

### 更新内容
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
* 扬声器/耳机/麦克风 (AppleALC)
* USB3.0/2.0
* 显示器亮度调节（系统偏好设置-显示器）
* F1,F2亮度调节；F4,F5,F6调节音量（静音，音量减，音量加）
* 电池电量显示（快速充电正常）
* 关盖睡眠以及唤醒（休眠耗电正常）
* CPU 变频(900MHz~3900MHz)，11个档位，睿频正常

### 目前不可用
* iMessage、Facetime、Siri（可能和网卡有关，因为涉及到MAC地址，或者有懂的朋友欢迎讨论）
* 蓝牙（从Windows热启动可用，玄学）
* 摄像头（不明原因）

### 无法驱动的设备
* WIFI（CNVI协议网卡全球无解，要华为官方愿意开放BIOS才能更换可用的网卡，这需要大家共同努力向官方反馈）
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
