使用：
去ATK_ESP8266文件夹下面的wifista.c第14行修改wifi的ssid号和密码。编译烧录后即可使用。

实验器材:
	战舰V3\精英STM32F103开发板
	
实验目的:
	学习ATK_ESP8266高性能UART_WIFI模块的使用,掌握基本的TCP，UDP通信串口AT指令配置方法.
	
硬件资源:
	1,DS0(连接在PB5)
	2,串口1(波特率:115200,PA9/PA10连接在板载USB转串口芯片CH340上面)
	3,串口3(波特率:115200，PB10/PB11)
	4,ALIENTEK 2.8/3.5/4.3/7寸TFTLCD模块(通过FSMC驱动,FSMC_NE4接LCD片选/A10接RS)
	5,按键KEY0(PE4)/KEY1(PE3)/KEY_UP(PA0,也称之为WK_UP)
	6,SD卡,通过SDIO(SDIO_D0~D4(PC8~PC11),SDIO_SCK(PC12),SDIO_CMD(PD2))连接 
	7,W25Q128(SPI FLASH芯片,连接在SPI2上)
	8,24C02
	9,ATK_ESP8266 WIFI模块1个
	10.3.5寸LCD屏幕
	
	连接方式：
	模块与带有无线网卡的电脑或其他wifi设备连接：采用wifi连接
	模块与开发板连接（TTL串口方式）：
	ATK-ESP8266 WIFI模块与精英板连接方式（通过4根杜邦线连接）：
	ATK-ESP8266 WIFI模块    战舰V3\精英STM32开发板
	   TXD<------------>PB11
	   RXD<------------>PB10
	   GND<------------>GND
	   VCC<------------>3.3V\5V
		
实验现象:
	本例程，用于实现ATK_ESP8266模块的三种工作模式：串口无线AP（COM-AP）、串口无线STA（COM-STA）
	和串口无线AP+STA（COM-AP+STA）这3个模式的测试，每个模式又包含TCP服务器、TCP客户端和UDP这3个子模式，
	本节我们将详细介绍这些模式的使用。模块配置可以通过串口配置，这里我们通过开发板串口配置，并实现通信。
	具体实验现象，请参考我们的文档<<ATK-ESP8266 WIFI模块使用说明(战舰V3&精英版)_AN1509A>>，验证测试部分


































