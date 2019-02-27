# STM32duino_clock
这是一个基于STM32F103C8T6小系统板的STM32duino的OLED时钟。  
功能：时间、温度、湿度、气压传感，GPS、北斗时间校正，校时成功提醒。  
使用的模块：DS3231、SHT35-D（可更换SHT3X系列内任意型号）、BMP388、ATGM336H（可更换NEO-M8N）、0.96寸 12864 OLED显示屏（理论上可更换u8g2支持同样分辨率的其他显示屏）、无源蜂鸣器。  
库里面包含：SlashDevin/NeoGPS（已修改配置）、adafruit/RTClib、Seeed-Studio/Grove_SHT31_Temp_Humi_Sensor、adafruit/Adafruit_BMP3XX、olikraus/u8g2  
接口：I²C、SPI、Serial  
连接：DS3231、SHT35-D、BMP388使用I²C连接到PB6（SLC）、PB7（SDA），ATGM336H使用Serial（Serial1）连接到PA9（RX）、PA10（TX），OLED使用SPI连接到PB11（D0）,PB10（D1）,PA7（CS）,PB0（DC）,PB1（RES），蜂鸣器使用GPIO（PWM）连接到PA0。  
