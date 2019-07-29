# 免责声明和版权公告

本手册中的信息仅适用于摩图科技公司所生产的小MU视觉传感器第3代产品（下称产品），本手册所描述内容仅适用于当前固件版本，
新版本功能需要更新传感器固件，否则可能导致部分产品功能失效，版本更新不另行通告，请关注摩图科技官网。
应仔细阅读和理解本手册中的各项条款，否则可能导致产品无法正常工作，检测效果变差，甚至产品损坏。

在未经摩图科技确认及授权的情况下，不可私自维修或改装产品上的电子元件，造成损坏的将不予以保修。

严禁任何组织或个人进行芯片内部代码拷贝、破解等侵权行为，芯片内部所有代码信息均归属于摩图科技所有，
对于任何侵权行为，摩图科技将采取法律措施予以维权。

本手册中所提及的技术方案、视觉算法、通讯协议均为摩图科技自主研发，任何组织或个人不得拷贝、抄袭、剽窃摩图科技的技术成果，
对于任何侵权行为，摩图科技将采取法律措施予以维权。

MORPX是杭州摩图科技有限公司的注册商标，MU是小MU视觉传感器的注册商标。
文本或图片中提到的所有商标名称、商标和注册商标均属其各自所有者的财产，特此声明。

本手册仅供指定公司客户或个人用户内部资料使用，在产品正式上市或发布之前，使用方应对本产品及手册采取保密措施，
在未经摩图科技授权的情况下，不得将产品及本手册传阅至第三方公司或个人。

版权归 © 2019 摩图科技所有。保留所有权利。

# 1.Arduino库导入
在Arduino官网下载最新的Arduino IDE 1.8.9

https://www.arduino.cc/en/Main/Software?setlang=cn

在github下载最新的MUVisionSensorIII的Arduino库

https://github.com/mu-opensource/MuVisionSensorIII

按照默认路径安装Arduino IDE，则Arduino的第三方库在“文档\Arduino\libraries”文件夹下。
将下载的MUVisionSensorIII-1.1.6解压后放入该文件夹则完成导入。

打开Arduino IDE，选择顶部的“工具 - 开发板”，常用开发板为Arduino Uno。如果使用MoonBot主控，则选开发板为Arduino Mega 2560，
并选择处理器为ATmega 1280。连接开发板后选择相应端口则完成Arduino开发板的连接。

如果成功导入了开发板兼容的库，选择顶部的“文件 - 示例 - 第三方示例 - MU Vision Sensor III”可以打开官方示例程序。

# 2.Arduino硬件连接

![](./images/MUVS3_pinout.png)

## 2.1 I2C模式

1）将模块左侧输出模式拨码开关1拨至下方，2拨至上方，切换至I2C模式；

2）（不推荐修改此设置）将模块右侧的地址选择拨码开关拨至对应位（默认地址0x60，1、2都在下方）；

3）将模块输出接口SDA口接至Arduino对应的SDA口，SCL口接至Arduino对应的SCL口。

## 2.2 串口模式

1）将模块左侧输出模式拨码开关1、2都拨至下方，切换至串口模式；

2）（不推荐修改此设置）将模块的地址选择拨码开关拨至对应位（默认地址1、2都在下方）；

3）将模块输出接口RX口接至Arduino对应的TX口，TX口接至Arduino对应的RX口。

