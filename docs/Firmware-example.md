# Firmware-example

LimeTK_SomeSlime 完全使用 SlimeVR 的追踪器固件，因此该文档仅提供需要修改的部分代码片段

注意：所有**配置仅作参考**，均需要随着 SlimeVR 追踪器固件的变更而随机应变

最后更新时 SomeSlime 硬件版本为: `v0.1`

## File: platformio.ini

```ini
[env:esp32-c3]
platform = espressif32 @ 6.1.0
build_flags =
 ${env.build_flags}
 -DESP32C3
board = esp32-c3-devkitm-1
```

## File: defines.h

```c
#define IMU IMU_BMI160
#define SECOND_IMU IMU
#define BOARD BOARD_CUSTOM
#define IMU_ROTATION DEG_270
#define SECOND_IMU_ROTATION DEG_270
```

> SomeSlime 并没有第二个追踪器，所以可以随便填写角度

```c
#elif BOARD == BOARD_CUSTOM
  // Define pins by the examples above
  #define PIN_IMU_SDA 0
  #define PIN_IMU_SCL 1
  #define PIN_IMU_INT NULL
  #define PIN_IMU_INT_2 NULL
  #define PIN_BATTERY_LEVEL NULL
  #define LED_PIN 7
  #define LED_INVERTED false
```

此处的引脚编号就是芯片中 GPIO 的编号。\
或许是因为 ESP32 的所有引脚都可以是 GPIO 吧，连类似 D0 这种格式都不用了

> 我也不知道 NULL 会对固件内部产生什么影响，但我总不能空着吧\
> It just works.
