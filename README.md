# Lenovo ThinkCentre M910x 黑苹果 EFI

## 我的配置

|         硬件       |                   型号                  | 
|-------------------:|:----------------------------------------|
|               主板 | Lenovo ThinkCentre M910x                       |
|                CPU | Intel Core i3-9100                      |
|               显卡 | 宝龙达 RX460 4G   |
|              硬盘1 | 三星 PM961 256G M2 NVMe                 |
|              硬盘2 | 铠侠 RC10 500G M2 NVMe            |
|               内存1 | 玖合 DDR4 2666Mhz 16G  |
|               内存2 | 枭鲸 DDR4 2666Mhz 16G  |
|        无线 + 蓝牙 | BCM943224PCIEBT2 双频 BT4.0 无线网卡    |
|               键盘 | 海盗船 K70 LUX                               |
|               鼠标 | 罗技 G304无线                               |
|            显示器 | 27寸 4K 宏基显示器 H277HK          |


## 折腾日志

2020年6月10日：启用10.14的原生`IO80211Family.kext`加载WIFI

## 注意事项

更新 EFI 之后，第一次进系统最好是带 `-v` 参数启动、`重建缓存并修复权限`否则可能会出现禁止符号，无法启动。

## EFI 简介

折腾M910x黑苹果过程中，各种搜索都找不到EFI，索性我就把EFI分享出来，避免后者走投无路。

鸣谢：`hyhy8766`  `ATC`


这个 EFI 的特点是使用的是 `iMac19,1` 机型，双硬解正常，因已做了 USB 定制，所有 USB 接口都可用。

缺点：

1、关于睡眠：其表现为可手动/自动睡眠，但是会秒醒。USB定制无误，BIOS中也关闭了串口，问题依旧。



OpenCore 版本为：0.5.8。

OpenCore 驱动包含：

* AudioDxe-64.efi
* HFSPlus.efi
* HiiDatabase.efi
* NdkBootPicker.efi
* NvmExpressDxe.efi
* OpenCanopy.efi
* OpenRuntime.efi
* OpenUsbKbDxe.efi
* Ps2KeyboardDxe.efi
* Ps2MouseDxe.efi
* UsbMouseDxe.efi
* XhciDxe.efi

系统驱动包含：

* AirportBrcmFixup.kext
* AppleALC.kext
* GenericUSBXHCI.kext
* IntelMausi.kext
* Lilu.kext
* SMCProcessor.kext
* USBPorts.kext
* USBPower.kext
* WhateverGreen.kext
* VirtualSMC.kext

## EFI 使用

如果你的配置跟我上面配置相同或兼容，那么你可以直接使用该 EFI 进行安装。安装前请注意，要先加入`三码`。生成时，请选择 `iMac19,1` 机型。

如果你的网卡和我一样请按照教程添加`IO80211Family.kext`。


## 系统截图
![avatar](https://github.com/ylen0l/Hackintosh-Lenovo-Thinkcentre-M910x-OpenCore-Efi/blob/master/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E6%88%AA%E5%9B%BE/%E5%85%B3%E4%BA%8E%E6%9C%AC%E6%9C%BA%402x.png)关于本机

加图片打开太慢了，就留了关于本机，其他截图去`系统状态截图`里面打开看吧




都看到这里了，说明你很需要，如您解决了唤醒秒醒，请联系我，感谢。
