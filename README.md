# 开源四旋翼飞行器GLDrone

## 简介

GLDrone是独立自制机架和电调飞控的开源项目，轴距在140左右的小机型，为GLMocap项目的室内飞行与室内编队实验而研发。  
GLDrone项目使用MIT协议，代码及机架、电调飞控PCB皆开放源文件。
## 设计文件

[机架设计文件(使用Fusion360)](https://github.com/guanglun/GLDrone)  
[电调原理图PCB(立创EDA)](https://oshwhub.com/guanglun/gldrone_blheli_esc)  
[飞控原理图PCB(立创EDA)](https://oshwhub.com/guanglun/gldrone_px4)  
[修改后的PX4源码](https://github.com/guanglun/PX4-Autopilot)  
机架设计文件Fusion360分享地址(在线查阅)：[https://a360.co/30LNv4s](https://a360.co/30LNv4s)  

## 电调说明
* 主控:EFM8BB21F16G，驱动:FD6288Q，MOS:TPN2R703NL
* 电调使用BLHeli_S方案，固件使用C_H_30，详见[BLHeli](https://github.com/bitdump/BLHeli)  
* 电调设计参考[https://github.com/ckflight/ESC_BLDC_HARDWARE](https://github.com/ckflight/ESC_BLDC_HARDWARE)  

## 飞控说明
* 飞控使用PX4方案：FMUv4,参考[pixracer](https://docs.px4.io/v1.12/en/flight_controller/pixracer.html)
* 主控: STM32F427VIT6
* IMU： ICM-20602 ICM-20689
* 磁力计：IST8310
* 气压计：MS5611
* 光流：PMW3901MB(未板载)
* 激光：VL53L1X(未板载)

## 存在的问题
* 警告！电调PCB由于四合一电调采用了模块复制，所以丝印只有MOTO4的正确，其他MOTO请参考MOTO4放置元器件！其中未连接的网络是由于复制过程中没有改网络编号所致，无需连接。
* 电调供给飞控的5V电源由于经过了在飞控PCB中经过了一个二极管导致压降至4.5V左右，应提高电调输出的电压。
* 由于电调飞控V1.1版本修改了V1.0版本发现的问题后未经打样测试，所以请谨慎使用！

## 图片及演示视频 
* [【硬核开源】自制运动捕捉我的自制飞行器！自研开源项目GLMocap与GLDrone最新进展](https://www.bilibili.com/video/BV1cQ4y1U7HJ/)  
* [自制机架GLMocap室内定位效果](https://www.bilibili.com/video/BV1EP4y1L723/)  
* [>>硬核开源! GLDrone开源四旋翼无人机项目](https://www.bilibili.com/video/BV1vf4y1M7S2/)  
  
![gldrone](http://guanglundz.com/gldrone/img/gldrone7.jpg)  
![gldrone](http://guanglundz.com/gldrone/img/gldrone12.jpg)  
![gldrone](http://guanglundz.com/gldrone/img/gldrone13.jpg)  
![gldrone](http://guanglundz.com/gldrone/img/gldrone1.jpg)   
![gldrone](http://guanglundz.com/gldrone/img/gldrone2.jpg)   
![gldrone](http://guanglundz.com/gldrone/img/gldrone3.jpg)   
![gldrone](http://guanglundz.com/gldrone/img/gldrone6.jpg)   
![gldrone](http://guanglundz.com/gldrone/img/gldrone10.jpg)  
![gldrone](http://guanglundz.com/gldrone/img/gldrone8.jpg)  
![gldrone](http://guanglundz.com/gldrone/img/gldrone9.jpg)  
![gldrone](http://guanglundz.com/gldrone/img/gldrone4.jpg)   
![gldrone](http://guanglundz.com/gldrone/img/gldrone5.jpg)   
![gldrone](http://guanglundz.com/gldrone/img/gldrone11.jpg)  

