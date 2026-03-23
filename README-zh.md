# Huawei MateBook 14 2020 (AMD) Hackintosh OpenCore EFI

本项目为华为 MateBook 14 2020款 锐龙版（AMD Ryzen）提供 macOS 引导支持。基于 OpenCore 制作。

其他年份的matebook锐龙芯片的笔记本，理论上也可以使用这个efi文件

## 💻 硬件配置 

| 硬件 (Component)     | 型号 (Details)                             |
| :------------------- | :----------------------------------------- |
| **电脑型号**         | Huawei MateBook 14 2020 AMD版  触屏  512GB |
| **处理器 (CPU)**     | AMD Ryzen 5 4600H                          |
| **核显 (iGPU)**      | 核显   AMD Radeon Graphics 512MB           |
| **内存 (RAM)**       | 16GB DDR4 2666MHz                          |
| **硬盘 (SSD)**       | WD SN730 512GB                             |
| **无线网卡 (Wi-Fi)** | 原机 RTL8822CE 已更换为 **Intel AX200**    |
| **声卡 (Audio)**     | Realtek ALC256                             |

## 🍎 系统版本
- 测试通过：macOS 13 Ventura （13.6.9）
- 引导工具：OpenCore  0.8.8

## ✅ 工作状态 (What's working)
- [x] AMD 核显硬件加速 (通过 NootedRed)  屏幕支持2k显示

- [x] 扬声器播放 / 3.5mm 耳机接口

- [x] 麦克风

- [x] Wi-Fi & 蓝牙 (通过 AX200 + itlwm/AirportItlwm)

  注意，原装的RTL8822CE无法在macos系统下工作，务必更换为其他的芯片（例如Intel AX200）

- [x] 触控板 (支持多指手势)

- [x] 触摸屏 (支持多指手势)，能够在Mac系统上像ipad一样使用手势！😍😍😍

- [x] 键盘及背光快捷键调节
  
- [x] [x] USB 接口及 Type-C 接口
  
- [x] 电池电量显示

- [x] 开盖唤醒 

- [x] 开机后引导进入macos系统无卡顿

## ❌已知问题 (Known Issues)
- [ ] **蓝牙**：蓝牙功能有时无法开启，若无法开启蓝牙请重启电脑或者等待一会，具体原因未知。
- [ ] 隔空投送 (AirDrop) 无法使用。

## ⛓️‍💥 Macos 镜像下载

[macOS Ventura 13.6.9(22G830) 正式版官方镜像-黑苹果星球](https://heipg.cn/macos/install-macos-ventura-13-6-9-22g830.html)

或者其他的 Ventura 13.6.9(22G830) 正式版官方镜像 

## ⚙️ BIOS 设置 (BIOS Settings)
开机按 `F2` 进入 BIOS：
- 关闭 Secure Boot (安全启动)

进入opencore 引导后，第一次应该按下空格键，选择Reset NVRAM进行重置

## 🚀 使用说明 (Installation)
1. 将 EFI 文件夹放入你的 U 盘 ESP 分区进行安装。

## 成功运行截图
![成功运行截图](pic/p.jpg)

## 🙏 鸣谢 (Credits)
- 感谢[Acidanthera](https://github.com/acidanthera) 团队提供的 OpenCore 和各类 Kexts。
- 感谢 [ChefKissInc](https://github.com/ChefKissInc/NootedRed) 提供的 NootedRed 让 AMD 核显焕发新生。
- 感谢 [OpenIntelWireless](https://github.com/OpenIntelWireless) 团队提供的 Intel 网卡驱动。
- 感谢 [Dany](https://forum.amd-osx.com/threads/huawei-matebook14-2020-r5-4600h-hackintosh-success-and-some-minor-problems.4618/)提供的Matebook14的安装efi配置文件用以参考