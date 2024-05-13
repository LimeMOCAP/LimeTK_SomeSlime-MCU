# LimeTK_SomeSlime-MCU

LimeTK_SomeSlime 是 SlimeVR 的一套硬件设计，但只有 PCB 部分没有外壳。

它是 LimeTK 项目中产生的一个副产品，它的上游是 `LimeTK_Soda-MCU v1.2` 但由于 ESP-IDF 对新手过于的不友好导致它的固件编写停滞了很久很久。\
SomeSlime-MCU 顾名思义（指 Slime）是一个 SlimeVR 的硬件设计方案，所以并不使用自定义的固件或者特别的 SlimeVR 固件分支，照常修改配置文件即可

也是因此这个项目有着不少 Soda 上残存的怨念，所以它的版本号永远都会以 `v0.` 开头

## 硬件设计理念

它们的理念都是尽可能的实现：最小的空间占用，以及可管控的电池安全

对此 LimeTK_SomeSlime 使用了 ESP32-C3 模组而非完整的开发板作为通讯模块。\
对于电池... 自己插根 JST-PH 的线上去，我不管啦（坏笑）。而且如果你想的话，板子上有三个接口可供菊花链哦

## PCB 制造

下载发布版本中的 `.zip` 或者带有 `gerber` 字样的压缩文件并提交到制造商即可，或者也可以检出对应的 git 标签用 kicad 打开项目从头导出一份 gerber 文件。\
至于导出标准嘛...

## 固件配置

文档位于: [docs/Firmware-example.md](docs/Firmware-example.md)

## 共享许可

硬件设计: CERN-OHL-W v2\
CERN Open Hardware Licence - weakly reciprocal - version 2

文档许可: CC BY 4.0\
知识共享许可协议 - 署名 4.0 国际
