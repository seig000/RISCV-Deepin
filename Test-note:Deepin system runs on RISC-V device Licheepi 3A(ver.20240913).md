### Deepin 系统在RISC-V设备 LicheePi 3A 运行测试笔记（ver.）

这是一份对 Deepin 操作系统在 RISC-V 设备 LicheePi 3A 上运行情况的基础测试
主要内容包括：工具准备、开机情况、桌面使用测试及开启 swapfile 后遇到的无法进入图形界面的处理记录

## 一、工具准备

**实体工具**

<ul>
<li>设备： LicheePi 3A [板卡介绍](https://wiki.sipeed.com/hardware/zh/lichee/K1/lpi3a/1_intro.html)</li>
<li>串口调试工具：RV DebuggerPlus </li>
连接方法参考[sipeed文档](https://wiki.sipeed.com/hardware/zh/lichee/K1/lpi3a/4_peripheral.html)
  
<li>电源适配器</li>
</ul> 

**软件工具**

镜像:[版本20240913](https://ci.deepin.com/repo/deepin/deepin-ports/cdimage/latest/riscv64/)

(注：即 deepin-ports/cdimage/latest/riscv64 下, k1 的 latest 版本）
uboot-k1工具：[下载](https://ci.deepin.com/repo/deepin/deepin-ports/cdimage/latest/riscv64/bootloaders/)

镜像烧录可使用[Titan Flasher](https://cloud.spacemit.com/prod-api/release/download/tools?token=titantools_for_windows_X86_X64)工具进行烧录，过程参考前一篇安装笔记，[传送门](https://github.com/seig000/Test-for-Installing-Deepin-on-LicheePi-Module-3A/)


## 二、开机

正常烧录成功开机，通过putty软件串口查看开机日志中存在部分FAILE：

*未进行update的情况下开机在桌面中会出现多个

## 三、桌面操作

**桌面使用**：

鼠标存在轻微闪烁情况

**音频情况**：

本地音频播放情况：轻微卡顿，至于后台时卡顿较为明显
bilibili视频播放：画面卡顿严重，音频卡还好

## 四、其它

借这篇笔记记录一个在使用过程中遇到一个问题：

**问题描述** 

在更新过软件包+添加swap文件后

**问题处理记录**
