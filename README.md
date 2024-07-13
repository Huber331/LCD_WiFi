# LCD_WiFi
Для проекта потребуется:
-  nodemcu (esp8266)
-  LCD1602 с модулем PCF8574 (I2C)
-  сервер с Ubuntu 24.04

## Frontend
Frontend - презентационная часть web приложений, информационной или программной системы, её пользовательский интерфейс и связанные с ним компоненты.
В этой роли у нас будет выступать nodemcu и LCD1602.

Схема подключения:

![image](https://github.com/user-attachments/assets/ff3bdc99-6f7e-4f25-9eb6-c5da6880513b)

## Backend
Backend - это внутренняя часть продукта, которая находится на сервере и скрыта от пользователей.
В этой роли у нас будет выступать сервер с параметрами:
- Static hostname: dc
- Icon name: computer-desktop
- Chassis: desktop 
- Machine ID: 295aa0e810a0469f88c913729b7f112b
- Boot ID: e2496429535a427ba10914a059ebb246
- Operating System: Ubuntu 24.04 LTS
- Kernel: Linux 6.8.0-35-generic
- Architecture: x86-64
- Hardware Vendor: ASUSTeK Computer INC.
- Hardware Model: AT5NM10-I
- Firmware Version: 0502
- Firmware Date: Wed 2010-07-21
- Firmware Age: 13y 11month 3w 2d
- ОЗУ: 3 Gb
- SSD: 200 Gb

### Узнаем температуру процессора
```
$ sudo apt install lm-sensors hddtemp psensor
```
### Настраиваем мониторинг температур
```
$ sudo sensors-detect
$ sudo systemctl enable lm-sensors
```
### посмотреть температуру процессора и не только командой
```
$ sudo sensors
```
> ### Примечание!
> Осторожно, напряжение!
