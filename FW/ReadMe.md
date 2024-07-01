# 说明

此处提供成品固件。

固件源代码可见candleLight官方固件，查看本人fork的分支(作为备份)：

- https://github.com/HEYAHONG/candleLight_fw.git
- https://gitee.com/HEYAHONG/candleLight_fw.git

固件列表:

- [candleLight_fw_3e79d973533e3e663921ec3eff3725f46ee3839d.bin](candleLight_fw_3e79d973533e3e663921ec3eff3725f46ee3839d.bin)

# 固件烧录

对于已经烧录固件的硬件，candleLight可采用DFU方式升级。

对于未烧录固件的硬件的用户，可采用以下方式烧录固件:

- 芯片内嵌Bootloader自带的DFU烧录。
- 采用SWD调试接口烧录,可使用各种调试器/烧录器,。

其中推荐采用使用芯片Bootloader自带的DFU烧录,只需要在上电时拉高Boot0引脚即可。

## 芯片内嵌Bootloader的DFU烧录

### 准备工作

在极海官网的[APM32F072](https://geehy.com/product/fifth/APM32F072#document)介绍页中安装好以下工具:

- [GeehyProg SetUp](https://geehy.com/uploads/tool/GeehyProg_V1.0.2_Chinese.msi)
- [DFU驱动安装](https://geehy.com/uploads/tool/dfu驱动安装.zip)

### 进入内嵌Bootloader

拉高Boot0(只需要短接板上的Boot即可)。将硬件通过USB连接至计算机。

![APM32 Bootloader的DFU设备](APM32 Bootloader的DFU设备.png)



### 烧录

![Geehy Prog USB DFU](Geehy Prog USB DFU.png)

### 烧录完成

烧录完成后并重新上电后，可在设备管理器中找到candleLight设备。

![candleLight](candleLight.png)

