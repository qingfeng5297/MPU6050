实验器材:
	NANO STM32F103开发板V1版本
	
实验目的:
	学习ATK-MPU6050 六轴传感器(三轴加速度+三轴陀螺仪)的使用.
	
硬件资源:
	1,DS0(连接在PC0)
	2,串口1(波特率:115200)
	3,按键KEY_UP(连接在PA0)
	4,ATK-MPU6050六轴传感器模块，同NANO板的连接关系如下:
	  STM32开发板-->ATK-MPU6050六轴传感器模块
			  PA2-->SCL
			  PA3-->SDA
			  GND-->GND
		      5V-->VCC 
	  注意：INT、AD0未用到
			
	
实验现象:

    本实验开机后，先初始化MPU6050，然后利用DMP库，初始化MPU6050及使能DMP，最后，在死循环里面不停
	读取：温度传感器、加速度传感器、陀螺仪、DMP姿态解算后的欧拉角等数据，通过串口输出到串口助手上。
	另外,本例程也可以通过USMART调用MPU_Read_Byte/MPU_Write_Byte等函数,来实现对MPU6050寄存器的读写操作
	(建议在GETDATA OFF状态下,GETDA状态通过KEY_UP按键选择).
	  
	  

					正点原子@ALIENTEK
					2018-7-18
					广州市星翼电子科技有限公司
					电话：020-38271790
					传真：020-36773971
					购买：http://shop62103354.taobao.com
					http://shop62057469.taobao.com
					公司网站：www.alientek.com
					技术论坛：www.openedv.com