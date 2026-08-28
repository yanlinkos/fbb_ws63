

# fbb_ws63开发指南

## 代码仓介绍

  ws63系列是2.4GHz Wi-Fi 6 星闪多模解决方案，其中ws63E支持2.4GHz的雷达人体活动检测功能，适用于大小家电、电工照明及对人体出没检测有需求的常电类物联网智能场景。该fbb_ws63代码包从统一开发平台FBB（Family Big Box，统一开发框架，统一API）构建而来，在该平台上开发的应用很容易被移植到其他星闪解决方案上，有效降低开发者门槛，缩短开发周期，支持开发者快速开发星闪产品。软件文档在线化链接：https://docs.hisilicon.com/repos/fbb_ws63/zh-CN/master/  

## 目录介绍

| 目录   | 介绍                                                         |
| ------ | ------------------------------------------------------------ |
| docs   | 存放软件资料手册、IO复用关系表、用户指南手册，帮助用户快速了解WS63系列 |
| src    | 开发接入SDK源码包，用户基于源码进行二次开发                  |
| tools  | 开发工具及环境搭建指南文档，帮助用户搭建开发环境             |
| vendor | 存放合作产商的开发板硬件和软件资料，包含案例代码、硬件原理图、案例开发指南文档 |


## 开发板示例

HiHope_NearLink_DK3863E_V03提供了以下Demo供开发参考：

<table  width="990" border="0" cellpadding="0" cellspacing="0" style='border-collapse:collapse;table-layout:fixed;'>
 <tr height="18" style='height:13.50pt;'>
  <td width="140" x:str><strong>一级分类</strong></td>
  <td width="170" x:str><strong>子分类</strong></td>
  <td width="680" colspan="6" align="center" x:str><strong>应用示例</strong></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="5" style='height:27.00pt' x:str>
<strong>基础驱动</strong></td>
  <td x:str><strong>I2C</strong></td>
  <td width="170" x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/i2c">I2C组件master端案例</a></td>
  <td width="170" x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/i2c">I2C组件slave端案例</a></td>
  <td width="170" x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/oled">SSD1306 OLED屏幕显示“Hello World”</a></td>
  <td width="170" x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/environment">AHT20模块读取当前温湿度并显示在屏幕案例</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>SPI</strong></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/spi">SPI组件master端案例</a></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/spi">SPI组件slave端案例</a></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/gyro">LSM6DSM模块读取横滚角、俯仰角、偏航角</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>UART</strong></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/uart">UART轮询案例</a></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/uart">UART中断读取案例</a></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/uartdemo">开发板UART自发自收</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>PWM</strong></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/src/application/samples/peripheral/pwm">PWM案例</a></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/beep">蜂鸣器案例</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>GPIO</strong></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/buttondemo">按键案例</a></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/led">点亮LED灯案例</a></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/servo">实现SG92R舵机转动-90°、-45°、0°、45°、90°</a></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/tricolored">实现SK6812三色灯亮绿、红、蓝三种颜色</a></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/ultrasonic">超声波测距</a></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/trafficlight">交通灯案例</a></td>
 </tr>
  <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="5" style='height:27.00pt' x:str>
<strong>操作系统</strong></td>
  <td x:str><strong>Thread</strong></td>
  <td width="170" x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/thread">线程使用案例</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>semaphore</strong></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/semaphore">信号量使用案例</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
  <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>event</strong></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/event">事件使用案例</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
  <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>message</strong></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/message">消息队列使用案例</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
  <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>mutex</strong></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/mutex">互斥锁使用案例</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
  <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="1" style='height:27.00pt' x:str>
<strong>星闪</strong></td>
  <td x:str><strong>SLE</strong></td>
  <td width="170" x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/sle_distribute_network">SLE配网</a></td>
  <td width="170" x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/sle_led">通过SLE控制LED灯</a></td>
  <td width="170" x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/sle_wifi_coexist">WiFi/SLE共存</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
 </tr>
  <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="1" style='height:27.00pt' x:str>
<strong>BLE</strong></td>
  <td x:str><strong>BLE</strong></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
 </tr>
  <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="1" style='height:27.00pt' x:str>
<strong>Wi-Fi</strong></td>
  <td x:str><strong>Wi-Fi</strong></td>
  <td width="170" x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/wifista">Wi-Fi STA</a></td>
  <td width="170" x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/wifiap">Wi-Fi AP</a></td>
  <td width="170" x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/wifidemo">Wi-Fi TCP/UDP测速</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="1" style='height:27.00pt' x:str>
<strong>TIMER</strong></td>
  <td x:str><strong>定时器</strong></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/timer">定时器</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="1" style='height:27.00pt' x:str>
<strong>雷达</strong></td>
  <td x:str><strong>运动感知</strong></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/radar_led">运动感知1.0</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="1" style='height:27.00pt' x:str>
<strong>低功耗</strong></td>
  <td x:str><strong>低功耗</strong></td>
  <td width="170" x:str><a href=""></a></td>
  <td x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
  <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="1" style='height:27.00pt' x:str>
<strong>端云协同</strong></td>
  <td x:str><strong>MQTT</strong></td>
  <td x:str><a href="https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/HiHope_NearLink_DK_WS63E_V03/demo/mqtt">华为云与开发板通过MQTT实现订阅、发布</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="4" style='height:27.00pt' x:str>
<strong>行业解决方案</strong></td>
  <td x:str><strong>鼠标</strong></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>键盘</strong></td>
  <td x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>车钥匙</strong></td>
  <td x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>遥控器</strong></td>
  <td x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
  <td ></td>
 </tr>
 </tr>
 <tr>
<![if supportMisalignedColumns]>
   <tr height="18" style="display:none;">
   </tr>
  <![endif]>
</table>
BearPi-Pico H3863提供了以下Demo供开发参考：

<table  width="990" border="0" cellpadding="0" cellspacing="0" style='border-collapse:collapse;table-layout:fixed;'>
 <tr height="18" style='height:13.50pt;'>
  <td width="140" x:str><strong>一级分类</strong></td>
  <td width="170" x:str><strong>子分类</strong></td>
  <td width="680" colspan="6" align="center" x:str><strong>应用示例</strong></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="6" style='height:27.00pt' x:str>
<strong>基础驱动</strong></td>
  <td x:str><strong>I2C</strong></td>
  <td width="170" x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/6.I2C%20%E9%A9%B1%E5%8A%A8OLED%E5%B1%8F%E5%B9%95%E6%B5%8B%E8%AF%95.html">I2C驱动OLED屏幕案例</a></td> <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>SPI</strong></td>
  <td x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/7.SPI%20%E9%A9%B1%E5%8A%A8OLED%E5%B1%8F%E5%B9%95%E6%B5%8B%E8%AF%95.html">SPI驱动OLED屏幕案例</a></td><td ></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
 </tr>
 <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>UART</strong></td>
  <td x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/5.UART%E6%95%B0%E6%8D%AE%E4%BC%A0%E8%BE%93%E6%B5%8B%E8%AF%95.html">开发板UART自发自收</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
  <td ></td>
 </tr> <tr height="18" style='height:13.50pt;'>
  <td x:str><strong>ADC</strong></td>
  <td x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/4.ADC%E9%87%87%E6%A0%B7%E6%B5%8B%E8%AF%95.html">ADC案例</a></td>  <td ></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
 </tr><tr height="18" style='height:13.50pt;'>
  <td x:str><strong>PWM</strong></td>
  <td x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/3.PWM%E8%BE%93%E5%87%BA%E6%B5%8B%E8%AF%95.html">PWM案例</a></td><td ></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td ></td>
 </tr><tr height="18" style='height:13.50pt;'>
  <td x:str><strong>GPIO</strong></td>
  <td x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/1.GPIO%E7%82%B9%E4%BA%AELED%E7%81%AF%E6%B5%8B%E8%AF%95.html">点亮LED灯案例</a></td>
  <td x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/study/2.GPIO%E6%8C%89%E9%94%AE%E4%B8%AD%E6%96%AD%E6%B5%8B%E8%AF%95.html">按键案例</a></td><td ></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
 </tr> <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="1" style='height:27.00pt' x:str>
<strong>星闪</strong></td>
  <td x:str><strong>SLE</strong></td>
  <td width="170" x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/SLE%E4%B8%B2%E5%8F%A3%E9%80%8F%E4%BC%A0%E6%B5%8B%E8%AF%95.html">SLE串口透传</a></td>
  <td width="170" x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/SLE%E7%BD%91%E5%85%B3%E9%80%8F%E4%BC%A0%E6%B5%8B%E8%AF%95.html">SLE网关透传</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td> </tr>
  <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="1" style='height:27.00pt' x:str>
<strong>BLE</strong></td>
  <td x:str><strong>BLE</strong></td>
    <td width="170" x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/BLE%E4%B8%B2%E5%8F%A3%E9%80%8F%E4%BC%A0%E6%B5%8B%E8%AF%95.html">BLE串口透传</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td></tr>
  <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="1" style='height:27.00pt' x:str>
<strong>Wi-Fi</strong></td>
  <td x:str><strong>Wi-Fi</strong></td>
  <td width="170" x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/Wi-Fi%20STA%20%E8%BF%9E%E6%8E%A5%E6%97%A0%E7%BA%BF%E7%83%AD%E7%82%B9%E6%B5%8B%E8%AF%95.html">Wi-Fi STA</a></td>
  <td width="170" x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/Wi-Fi%20SoftAP%20%E5%BC%80%E5%90%AF%E6%97%A0%E7%BA%BF%E7%83%AD%E7%82%B9%E6%B5%8B%E8%AF%95.html">Wi-Fi AP</a></td>
  <td width="170" x:str><a href="https://www.bearpi.cn/core_board/bearpi/pico/h3863/software/Wi-Fi%20UDP%E5%AE%A2%E6%88%B7%E7%AB%AF%E6%B5%8B%E8%AF%95.html">Wi-Fi UDP客户端</a></td> <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td></tr>
  <tr height="18" style='height:13.50pt;'>
  <td width="140" align="center" rowspan="1" style='height:27.00pt' x:str>
<strong>Matter</strong></td>
  <td x:str><strong>Matter</strong></td>
  <td width="170" x:str><a href="https://gitcode.com/HiSpark/fbb_ws63/blob/master/docs/zh-CN/software/Matter%E7%94%A8%E6%88%B7%E6%8C%87%E5%8D%97/Matter%E7%94%A8%E6%88%B7%E6%8C%87%E5%8D%97.md">Matter Device设备开发</a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td>
  <td width="170" x:str><a href=""></a></td></tr>
 </tr>
 <tr>
<![if supportMisalignedColumns]>
   <tr height="18" style="display:none;">
   </tr>
  <![endif]>
</table>
华清远见WS63鸿蒙星闪开发板提供了以下Demo供开发参考：

| 一级分类     | 子分类             | 应用示例                                                     |                                                              |                                                              |                                                              |
| :----------- | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **基础驱动** | **GPIO**           | [点亮LED灯案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_01_ledblink) |                                                              |                                                              |                                                              |
|              | **UART**           | [串口轮询、中断收发案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_02_uart) |                                                              |                                                              |                                                              |
|              | **I2C**            | [0.96寸OLED屏幕驱动案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_03_ssd1306) | [RGB灯珠驱动案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_04_rgb) | [SHT20传感器温湿度读取](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_05_sht20) | [AP3216读取光照、红外、人体接近数据](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_06_ap3216) |
|              | **SPI**            | [2.8寸LCD屏驱动案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/base_07_spi_lcd) |                                                              |                                                              |                                                              |
| **操作系统** | **Thread**         | [任务调度使用案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_01_task) |                                                              |                                                              |                                                              |
|              | **Timer**          | [软件定时器使用案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_02_timer) |                                                              |                                                              |                                                              |
|              | **Event**          | [事件使用案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_03_event) |                                                              |                                                              |                                                              |
|              | **Mutex**          | [互斥锁使用案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_04_mutex) |                                                              |                                                              |                                                              |
|              | **MutexSemaphore** | [互斥信号量使用案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_05_mutex_Semaphore) |                                                              |                                                              |                                                              |
|              | **SyncSemaphore**  | [同步信号量使用案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_06_sync_Semaphore) |                                                              |                                                              |                                                              |
|              | **CountSemaphore** | [计数型信号量使用案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_07_count_Semaphore) |                                                              |                                                              |                                                              |
|              | **MessgeQueue**    | [消息队列使用案例](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/kernel_08_message_queque) |                                                              |                                                              |                                                              |
| **WI-FI**    | **WI-FI**          | [WI-FI STA](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_01_sta) | [WI-FI AP](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_02_ap) | [WI-FI UDP通信](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_03_udp) | [Wi-Fi TCP通信](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_04_tcp) |
| **端云协同** | **MQTT**           | [MQTT本地回环测试](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_05_mqtt) | [连接华为云实现控制板载资源](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/wifi_06_huawei_iot) |                                                              |                                                              |
| **星闪**     | **SLE**            | [SLE串口透传](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/sle_01_trans_server) |                                                              |                                                              |                                                              |
| **BLE**      | **BLE**            | [BLE串口透传](https://github.com/yanlinkos/fbb_ws63/tree/master/vendor/Hqyj_Ws63/Farsight/ble_02_trans_server) |                                                              |                                                              |                                                              |

DyCloud_WF6301_DK开发板提供了以下Demo供开发参考：

| <a href="vendor/DyCloud_WF6301_DK V1.0/demo/at24c02">at24c02案例</a> | <a href="vendor/DyCloud_WF6301_DK V1.0/demo/breathing_light">breathing_light案例</a> | <a href="vendor/DyCloud_WF6301_DK V1.0/demo/cht20">cht20案例</a> |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| <a href="vendor/DyCloud_WF6301_DK V1.0/demo/lcd">lcd案例</a> | <a href="vendor/DyCloud_WF6301_DK V1.0/demo/cht20">sc7a20案例</a> | <a href="vendor/DyCloud_WF6301_DK V1.0/demo/ws2812b">ws2812b案例</a> |

MYF-F63VA01开发板提供了以下Demo供开发参考：

| [闪烁灯案例](vendor/MYF_F63/peripheral/blinky) | [按键案例](vendor/MYF_F63/peripheral/button)     | [DMA案例](vendor/MYF_F63/peripheral/dma)      |
| ---------------------------------------------- | ------------------------------------------------ | --------------------------------------------- |
| [PWM呼吸灯案例](vendor/MYF_F63/peripheral/pwm) | [SYSTICK案例](vendor/MYF_F63/peripheral/systick) | [定时器案例](vendor/MYF_F63/peripheral/timer) |
| [串口案例](vendor/MYF_F63/peripheral/uart)     | [看门狗案例](vendor/MYF_F63/peripheral/watchdog) | [AT指令案例](vendor/MYF_F63/products/at_test) |
