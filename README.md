# Magicbook-Pro-16.1-Hackintosh 黑苹果尝鲜版
>Install macOS Catalina 10.15 19A583 from Huawei Honor Magicbook Pro 16.1 HBL-W19L

### 详细配置参数
| 项目 | 详细参数|
| :--: | :-------------------- |
| 型号 | Magicbook Pro 16.1 HBL-W19L    |
| CPU  | Intel Whiskey Lake i5 8265U |
| 内存 | DDR4 2666 8G|
| 显卡 | Intel UHD620 2048 MB & NVIDIA MX250|
| 硬盘 | HS C2000 Pro 1TB|
| 声卡 | Realtek ?|
| 屏幕 | 1920*1080|
| SMBIOS | Macbook Pro 15,2|
| Clover | Updated to 5097|

### 目前可用的设备
* 核芯显卡 (被识别成UHD630 Mobile)
* 扬声器/耳机 (使用VoodooHDA-2.9.2，AppleALC暂时不可用)
* USB3.0/2.0
* FN+f1,f2亮度调节
* 电池电量显示

### 目前不可用
* 摄像头
* 触摸板
* HDMI输出
* 睡眠以及唤醒
* UHD620的HEVC解码

### 无法驱动的设备
* WIFI/蓝牙
* MX250
* 指纹识别

### 未测试的设备
* USB-C 输出
* CPU 变频

### 说明
作者本人也是黑苹果新手一枚，有Z390 M Gaming的成功安装经历，现在入手了Magicbook Pro但发现全网都没有人做EFI(可能是因为自带的PM981?)，所以献丑自己摸索了整整三天做了一个暂时不完善的EFI，用了TB的USB网卡目前看看网页写写文档都没问题，还有很多地方没有完善，其实我也有很多不会的地方，希望能和大家交流学习，一起完善这个EFI，我也会长期更新这个EFI~

### 感谢：
* 1.黑苹果长期维护清单[github: frezs/MateBook14-Hackintosh](https://github.com/frezs/MateBook14-Hackintosh)
* 2.黑苹果长期维护清单[github: hjmmc/Honor-Magicbook](https://github.com/hjmmc/Honor-Magicbook)
* 3.黑苹果长期维护清单[github: 4323770/Hackintosh-For-Matebook-X](https://github.com/4323770/Hackintosh-For-Matebook-X)
* 4.[黑果小兵]macOS Catalina 10.15 19A583 正式版 with Clover 5096原版镜像[双EFI双平台版]
* 5.[黑果小兵]Hackintool(原Intel FB-Patcher)使用教程及插入姿势
* 6.[远景论坛-微软极客社区](http://www.pcbeta.com)
