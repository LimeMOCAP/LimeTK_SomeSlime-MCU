# LimeTK_SomeSlime-MCU

这是 LimeTK 项目中产生的一个副产品，它的上游是 `LimeTK_Soda-MCU v1.2` 但由于 ESP-IDF 对新手过于的不友好导致它的固件编写停滞了很久很久。\
SomeSlime-MCU 顾名思义（指 Slime）是一个 SlimeVR 的硬件设计方案，所以并不使用自定义的固件或者特别的 SlimeVR 固件分支，照常修改配置文件即可

这个项目有着不少 Soda 上残存的怨念，所以它的版本号永远都会以 `v0.` 开头

## 硬件制造

下载发布版本中的 `.zip` 或者带有 `gerber` 字样的压缩文件并提交到制造商即可，或者也可以检出对应的 git 标签用 kicad 打开项目从头导出一份 gerber 文件。\
至于导出标准嘛...

## 固件配置

文档位于: [docs/Firmware-example.md](docs/Firmware-example.md)

## 共享许可

硬件设计: CERN-OHL-W v2\
CERN Open Hardware Licence - weakly reciprocal - version 2

文档许可: CC BY 4.0\
Creative Commons - Attribution 4.0 International
