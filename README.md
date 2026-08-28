# fbb_ws63 Development Guide

## Repository Introduction

The YL63 series is a 2.4GHz Wi-Fi 6 NearLink multi-mode solution. Among them, the YL63E supports 2.4GHz radar human motion detection for home appliances, electrical lighting, and always-on IoT smart scenarios requiring detection of human presence. The fbb_ws63 code package is built on the unified development platform FBB (Family Big Box, a unified development framework and unified API). Applications developed on this platform can be easily ported to other NearLink solutions, effectively lowering the barrier for developers, shortening the development cycle, and supporting developers in rapidly building NearLink products. 

## Directory Introduction

| Directory | Description |
| --------- | ----------- |
| docs   | Contains software manuals, IO multiplexing tables, and user guide manuals to help users quickly get familiar with the YL63 series |
| src    | SDK source package for development integration; users perform secondary development based on the source code |
| tools  | Development tools and environment setup guide documents to help users set up the development environment |
| vendor | Contains hardware and software materials for development boards from partner manufacturers, including case code, hardware schematics, and case development guide documents |

## Development Board Examples

### YL63E-DevKitC-1-N4

The YL63E-DevKitC-1-N4 provides the following demos for development reference:

| Primary Category | Subcategory | Application Examples |
| ------------ | ---------- | ----------- |
| **Basic Drivers** | **I2C** | [I2C component master-end example](https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/i2c) / [I2C component slave-end example](https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/i2c) / [SSD1306 OLED screen displaying "Hello World"](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/oled) / [AHT20 module reading current temperature and humidity and displaying them on screen](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/environment) |
| | **SPI** | [SPI component master-end example](https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/spi) / [SPI component slave-end example](https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/spi) / [LSM6DSM module reading roll, pitch, and yaw angles](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/gyro) |
| | **UART** | [UART polling example](https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/uart) / [UART interrupt read example](https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/uart) / [Development board UART self-send/self-receive](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/uartdemo) |
| | **PWM** | [PWM example](https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/pwm) / [Buzzer example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/beep) |
| | **GPIO** | [Button example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/buttondemo) / [Turning on LED example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/led) / [SG92R servo rotation of -90°, -45°, 0°, 45°, 90°](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/servo) / [SK6812 tricolor LED lighting in green, red, and blue](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/tricolored) / [Ultrasonic distance measurement](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/ultrasonic) / [Traffic light example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/trafficlight) |
| **Operating System** | **Thread** | [Thread usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/thread) |
| | **Semaphore** | [Semaphore usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/semaphore) |
| | **Event** | [Event usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/event) |
| | **Message** | [Message queue usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/message) |
| | **Mutex** | [Mutex usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/mutex) |
| **NearLink** | **SLE** | [SLE network configuration](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/sle_distribute_network) / [Controlling LED via SLE](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/sle_led) / [WiFi/SLE coexistence](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/sle_wifi_coexist) |
| **BLE** | **BLE** | |
| **Wi-Fi** | **Wi-Fi** | [Wi-Fi STA](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/wifista) / [Wi-Fi AP](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/wifiap) / [Wi-Fi TCP/UDP speed test](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/wifidemo) |
| **TIMER** | **Timer** | [Timer](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/timer) |
| **Radar** | **Motion sensing** | [Motion sensing 1.0](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/radar_led) |
| **Low Power** | **Low Power** | |
| **Device-Cloud Collaboration** | **MQTT** | [Huawei Cloud and development board implementing subscription and publishing via MQTT](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/mqtt) |
| **Industry Solutions** | **Mouse** | |
| | **Keyboard** | |
| | **Car key** | |
| | **Remote control** | |

### BearPi-Pico H3863

The BearPi-Pico H3863 provides the following demos for development reference:

| Primary Category | Subcategory | Application Examples |
| ------------ | ---------- | ----------- |
| **Basic Drivers** | **I2C** | [I2C driving OLED screen example](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/6.I2C%20%E9%A9%B1%E5%8A%A8OLED%E5%B1%8F%E5%B9%95%E6%B5%8B%E8%AF%95.html) |
| | **SPI** | [SPI driving OLED screen example](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/7.SPI%20%E9%A9%B1%E5%8A%A8OLED%E5%B1%8F%E5%B9%95%E6%B5%8B%E8%AF%95.html) |
| | **UART** | [Development board UART self-send/self-receive](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/5.UART%E6%95%B0%E6%8D%AE%E4%BC%A0%E8%BE%93%E6%B5%8B%E8%AF%95.html) |
| | **ADC** | [ADC example](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/4.ADC%E9%87%87%E6%A0%B7%E6%B5%8B%E8%AF%95.html) |
| | **PWM** | [PWM example](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/3.PWM%E8%BE%93%E5%87%BA%E6%B5%8B%E8%AF%95.html) |
| | **GPIO** | [Turning on LED example](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/1.GPIO%E7%82%B9%E4%BA%AELED%E7%81%AF%E6%B5%8B%E8%AF%95.html) / [Button interrupt example](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/2.GPIO%E6%8C%89%E9%94%AE%E4%B8%AD%E6%96%AD%E6%B5%8B%E8%AF%95.html) |
| **NearLink** | **SLE** | [SLE serial port transparent transmission](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/SLE%E4%B8%B2%E5%8F%A3%E9%80%8F%E4%BC%A0%E6%B5%8B%E8%AF%95.html) / [SLE gateway transparent transmission](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/SLE%E7%BD%91%E5%85%B3%E9%80%8F%E4%BC%A0%E6%B5%8B%E8%AF%95.html) |
| **BLE** | **BLE** | [BLE serial port transparent transmission](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/BLE%E4%B8%B2%E5%8F%A3%E9%80%8F%E4%BC%A0%E6%B5%8B%E8%AF%95.html) |
| **Wi-Fi** | **Wi-Fi** | [Wi-Fi STA](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/Wi-Fi%20STA%20%E8%BF%9E%E6%8E%A5%E6%97%A0%E7%BA%BF%E7%83%AD%E7%82%B9%E6%B5%8B%E8%AF%95.html) / [Wi-Fi AP](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/Wi-Fi%20SoftAP%20%E5%BC%80%E5%90%AF%E6%97%A0%E7%BA%BF%E7%83%AD%E7%82%B9%E6%B5%8B%E8%AF%95.html) / [Wi-Fi UDP client](https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/Wi-Fi%20UDP%E5%AE%A2%E6%88%B7%E7%AB%AF%E6%B5%8B%E8%AF%95.html) |
| **Matter** | **Matter** | [Matter Device development](https://gitcode.com/HiSpark/fbb_ws63/blob/master/docs/zh-CN/software/Matter%E7%94%A8%E6%88%B7%E6%8C%87%E5%8D%97/Matter%E7%94%A8%E6%88%B7%E6%8C%87%E5%8D%97.md) |

### Farsight WS63 HarmonyOS NearLink Development Board

The Farsight WS63 development board provides the following demos for development reference:

| Primary Category | Subcategory | Application Examples |
| :----------- | ---------- | ----------- |
| **Basic Drivers** | **GPIO** | [Turning on LED example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_01_ledblink) |
| | **UART** | [Serial polling and interrupt send/receive example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_02_uart) |
| | **I2C** | [0.96-inch OLED screen driver example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_03_ssd1306) / [RGB LED driver example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_04_rgb) / [SHT20 sensor temperature and humidity reading](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_05_sht20) / [AP3216 reading ambient light, infrared, and proximity data](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_06_ap3216) |
| | **SPI** | [2.8-inch LCD screen driver example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_07_spi_lcd) |
| **Operating System** | **Thread** | [Task scheduling usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_01_task) |
| | **Timer** | [Software timer usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_02_timer) |
| | **Event** | [Event usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_03_event) |
| | **Mutex** | [Mutex usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_04_mutex) |
| | **MutexSemaphore** | [Mutex semaphore usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_05_mutex_Semaphore) |
| | **SyncSemaphore** | [Synchronous semaphore usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_06_sync_Semaphore) |
| | **CountSemaphore** | [Counting semaphore usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_07_count_Semaphore) |
| | **MessageQueue** | [Message queue usage example](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_08_message_queque) |
| **WI-FI** | **WI-FI** | [WI-FI STA](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_01_sta) / [WI-FI AP](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_02_ap) / [WI-FI UDP communication](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_03_udp) / [Wi-Fi TCP communication](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_04_tcp) |
| **Device-Cloud Collaboration** | **MQTT** | [MQTT local loopback test](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_05_mqtt) / [Connecting to Huawei Cloud to control on-board resources](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_06_huawei_iot) |
| **NearLink** | **SLE** | [SLE serial port transparent transmission](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/sle_01_trans_server) |
| **BLE** | **BLE** | [BLE serial port transparent transmission](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/ble_02_trans_server) |

### DyCloud_WF6301_DK Development Board

The DyCloud_WF6301_DK development board provides the following demos for development reference:

| [at24c02 example](vendor/DyCloud_WF6301_DK V1.0/demo/at24c02) | [breathing_light example](vendor/DyCloud_WF6301_DK V1.0/demo/breathing_light) | [cht20 example](vendor/DyCloud_WF6301_DK V1.0/demo/cht20) |
| ----------- | ----------- | ----------- |
| [lcd example](vendor/DyCloud_WF6301_DK V1.0/demo/lcd) | [sc7a20 example](vendor/DyCloud_WF6301_DK V1.0/demo/cht20) | [ws2812b example](vendor/DyCloud_WF6301_DK V1.0/demo/ws2812b) |

### MYF-F63VA01 Development Board

The MYF-F63VA01 development board provides the following demos for development reference:

| [Blinking light example](vendor/MYF_F63/peripheral/blinky) | [Button example](vendor/MYF_F63/peripheral/button) | [DMA example](vendor/MYF_F63/peripheral/dma) |
| ----------- | ----------- | ----------- |
| [PWM breathing light example](vendor/MYF_F63/peripheral/pwm) | [SYSTICK example](vendor/MYF_F63/peripheral/systick) | [Timer example](vendor/MYF_F63/peripheral/timer) |
| [Serial port example](vendor/MYF_F63/peripheral/uart) | [Watchdog example](vendor/MYF_F63/peripheral/watchdog) | [AT command example](vendor/MYF_F63/products/at_test) |
