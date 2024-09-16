# SOIL_INTEGRATED_Sensor_NPK-PH-MOISTURE-EC_InterfaceESP32
NPK soil sensor provides NPK, PH, MOISTURE, TEMPERATURE &amp; EC of soil interface ESP32.

### Nếu bạn cần hỗ trợ đề tài này, đừng ngần ngại liên hệ mình để được hỗ trợ.

![images]()
## Components
- ESP32-DevKitC
- NPK pH EC RS485 5-Pin Sensor 7 in 1 for Agriculture

## Introduction
This all in one soil sensor can reflect seven elements of soil moisture content, electrical conductivity, temperature, nitrogen, phosphorus, potassium, and pH. Suitable for all kinds of soil. It can be widely used in water-saving irrigation, greenhouses, flowers and vegetables, grassland pastures, soil rapid testing, plant cultivation, sewage treatment, precision agriculture and other occasions.

## Technical parameter
Power Supply | DC 4.5-30V | 
--- | --- | 
Maximum power consumption| 0.5W (24V DC power supply) | 
Working temperature| -30 to 70 oC| 
Protection grade | IP68 | 
Output signal | RS485 (Modbus) |

https://www.htebd.com/npk-ph-ec-rs485-5-pin-sensor-7-in-1-for-agriculture/
## Datasheet
https://dl.artronshop.co.th/RS485%20Sensor/Soil%20TH-NPK%20&%20TH-PH-NPK%20&%20TH-EC-NPK%20&%20TH-EC-PH-NPK%20manual_V1.1.pdf

## ⚛️Software - Programming language & Framework
- Programming for microcontroller: Arduino IDE (`2.3.2`)
- Server: Javascript
- Website: HTML5, CSS, Bootstrap 5
- Leafletjs
  
## Version Recommend
*Version Arduino IDE:*
`2.3.2`

*Version Board:* ESP32 by Espressif Systems - `3.0.3`

*Version Library:* 

- ThingSpeak by MathWorks - `2.0.1`

- TinyGPSPlus by Mikal Hart - `1.0.3`

## The working Principle of the GPS

The system of GPS consists of three main parts, including the GPS satellites, the control system, and the control system.

The satellites have covered virtually every corner of the earth.No matter where you are,at least four GPS satellites can be visible at any time.

Everyone regularly transmits information about their location and real-time. These signals that are traveling at the speed of light are intercepted by the GPS receiver, and the GPS receiver calculates the distance of each satellite from us based on the length of time the information arrives.

What a GPS receiver does is locate the four or more satellites and calculate the distance between each one of them. Using this information the GPS tracking system in our car or other devices finds out its current location. The information is presented as maps, latitude And longitude specification, etc.

Once you have information about the distance between you and the three satellites, the GPS receiver can use a method called trilateration to determine your position. It is easy to understand this for the people who have learned math.

![images](https://www.eelinktracker.com/Images/attached/image/20190717/20190717150542_14537.png)

## The working Principle
![images](https://github.com/VinhCao09/ESP32_GPS_Tracking_Device_with_Webserver_Maps/blob/main/images/2.jpg)

## How to use
*Connect*

Pin Neo 6M | Pin ESP32 | 
--- | --- |
VCC | Vin (5V) |
GND | GND |
TX | GPIO16 (RX) |
RX | GPIO17 (TX) |

Change the wifi configuration

```bash
char ssid[] = "YOUR_SSID"; 
char pass[] = "YOUR_PASSWORD";  
```

Change the ThingSpeak configuration

```bash
unsigned long myChannelNumber = YourChannelNumber;
const char * myWriteAPIKey = "YourAPIKey";
```
![images](https://github.com/VinhCao09/ESP32_GPS_Tracking_Device_with_Webserver_Maps/blob/main/images/5.jpg)

ex:
```bash
unsigned long myChannelNumber = 2543450;
const char * myWriteAPIKey = "WW2QG9CRI57KMB2U";
```
Change the UART Pin:
```bash
HardwareSerial GPSSerial(1);
GPSSerial.begin(9600, SERIAL_8N1, 16, 17);
```

These are the default assignments for the ESP32:
UART Port | TX | RX |
--- | --- | --- |
UART0 | 1 | 3 |
UART1 | 10 | 9 |
UART2 | 17 | 16 |

✔️Please read the code to connect the button pins.

Change channel and api_key in javascript file. 

```bash
        function fetchData() {
            fetch('https://api.thingspeak.com/channels/yourchannel/feeds/last.json?api_key=yourapikey')
                .then(response => response.json())
                .then(data => {
                    updateMap(data);
                })
                .catch(error => console.error('Error fetching data:', error));
        }
```

![images](https://github.com/VinhCao09/ESP32_GPS_Tracking_Device_with_Webserver_Maps/blob/main/images/3.jpg)

## ⬆️Deloy
https://vinhcaodatabase.com/gpstracking.html

## 🚀 About Me
Hello 👋I am Vinh. I'm studying HCMC University of Technology and Education

**Major:** Electronics and Telecommunication

**Skill:** 

*- Microcontroller:* ESP32/8266 - ARDUINO - PIC - Raspberry Pi

*- Programming languages:* C/C++/HTML/CSS/PHP/SQL and
related Frameworks (Bootstrap)

*- Communication Protocols:* SPI, I2C, UART, CAN

*- Data Trasmissions:* HTTP, TCP/IP, MQTT
## Authors

- [@my_fb](https://www.facebook.com/vcao.vn)
- [@my_email](contact@vinhcaodatabase.com)

## Demo

👉Click on the icon below to watch the demo video:

[![Watch the video](https://media3.giphy.com/media/A7LF3J4uMJQ4r8ApLg/giphy.gif?cid=6c09b95275l1l3krhehcppcrgllmv64r7jd6py964efin2av&ep=v1_internal_gif_by_id&rid=giphy.gif&ct=s)](https://www.tiktok.com/@vinhcaoplay/video/7396630681628970256?lang=vi-VN)

https://www.tiktok.com/@vinhcaoplay/video/7396630681628970256?lang=vi-VN


![Logo](https://codingninja.asia/images/codeninjalogo.png)

