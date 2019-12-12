# Magicbook-Pro-16.1-Hackintosh 黑苹果尝鲜版
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
| 屏幕 | 1920*1080|
| SMBIOS | Macbook Pro 15,4|
| Clover | Updated to 5097|

大家直接在Release下载吧，不在code里面上传更新了
[GatesYang/Magicbook-Pro-16.1-Hackintosh/releases](https://github.com/GatesYang/Magicbook-Pro-16.1-Hackintosh/releases)

### 写在前面
  其实这个EFI我也是无偿提供，纯个人兴趣而且想让每一位热爱黑苹果，使用爱机Magicbook Pro 16.1的大家一起开心，一起折腾，一起研究的，众所周知这是个开源项目，是无偿的，我看见有人在其它地方使用我的EFI，不说明出处就算了，还指责我的EFI“有毛病”。换位思考一下，如果是你自己辛辛苦苦花了大量时间来调试来摸索的一个EFI，别人不仅不对你表示感谢，还对你进行指责，我觉得这种事情确实令人不解。当然了，也有很多支持我的朋友，很多朋友也为我反馈BUG，提出可行方案，我很感动，我是一个黑果小白，不是敲代码如流水的大神，如果不喜欢我的EFI大可以去TB花钱找人定制一个完美的EFI，我在EFI里面既没有留下作者信息也没有留下印记，就是想让大家能一起学习交流一起进步，希望Magicbook Pro这台机子能陪伴我们走得更远，为我们提供更大的生产力和潜力。感谢大家使用我的EFI，有问题欢迎一起交流！
  
### 更新
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
* 扬声器/耳机/麦克风 (AppleALC)
* USB3.0/2.0
* 显示器亮度调节（系统偏好设置-显示器）
* FN+f1,f2亮度调节（外接USB更改快捷键），非FN+F4,F5,F6调节音量（静音，音量减，音量加）
* 电池电量显示（快速充电正常）
* 关盖睡眠以及唤醒（未测试休眠耗电）
* CPU 变频(900MHz~3900MHz)，11个档位，睿频正常

### 目前不可用
* iMessage、Facetime、Siri（和网卡有关，需要等网卡解决了才能解决）
* 触摸板（暂时编译不成功）
* 随航（sidecar）可能和网卡有关
* 蓝牙（从Windows热启动有时可用，玄学）
* 摄像头（不明原因，等大神指教）

### 无法驱动的设备
* WIFI（CNVI协议网卡全球无解，要华为官方愿意开放BIOS才能更换可用的网卡，这需要大家共同努力向官方反馈）
* MX250
* 指纹识别

### 说明
作者本人也是黑苹果新手一枚，有Z390 M Gaming的成功安装经历，现在入手了Magicbook Pro但发现全网都没有人做EFI(可能是因为自带的三星PM981?)，所以献丑自己摸索了整整三天做了一个暂时不完善的EFI，用了TB的USB网卡，目前看看网页写写文档都没问题，还有很多地方没有完善，其实我也有很多不会的地方，希望能和大家交流学习，一起完善这个EFI，我也会长期更新这个EFI~

### 感谢：
* 1.黑苹果长期维护清单[github: frezs/MateBook14-Hackintosh](https://github.com/frezs/MateBook14-Hackintosh)
* 2.黑苹果长期维护清单[github: hjmmc/Honor-Magicbook](https://github.com/hjmmc/Honor-Magicbook)
* 3.黑苹果长期维护清单[github: 4323770/Hackintosh-For-Matebook-X](https://github.com/4323770/Hackintosh-For-Matebook-X)
* 4.[黑果小兵]macOS Catalina 10.15 19A583 正式版 with Clover 5096原版镜像[双EFI双平台版]
* 5.[黑果小兵]Hackintool(原Intel FB-Patcher)使用教程及插入姿势
* 6.[远景论坛-微软极客社区](http://www.pcbeta.com)
