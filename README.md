# SOIL_INTEGRATED_Sensor_NPK-PH-MOISTURE-EC_InterfaceESP32
NPK soil sensor provides NPK, PH, MOISTURE, TEMPERATURE &amp; EC of soil interface ESP32.


## Components
- ESP32-DevKitC
- NPK pH EC RS485 5-Pin Sensor 7 in 1 for Agriculture

## Introduction
This all in one soil sensor can reflect seven elements of soil moisture content, electrical conductivity, temperature, nitrogen, phosphorus, potassium, and pH. Suitable for all kinds of soil. It can be widely used in water-saving irrigation, greenhouses, flowers and vegetables, grassland pastures, soil rapid testing, plant cultivation, sewage treatment, precision agriculture and other occasions.

## Technical parameter
Technical specifications | Parameter |
--- | --- | 
Power Supply | DC 4.5-30V | 
Maximum power consumption| 0.5W (24V DC power supply) | 
Working temperature| -30 to 70 oC| 
Protection grade | IP68 | 
Output signal | RS485 (Modbus) |
Respond time | <1s |

https://www.htebd.com/npk-ph-ec-rs485-5-pin-sensor-7-in-1-for-agriculture/
## Datasheet
https://dl.artronshop.co.th/RS485%20Sensor/Soil%20TH-NPK%20&%20TH-PH-NPK%20&%20TH-EC-NPK%20&%20TH-EC-PH-NPK%20manual_V1.1.pdf

## The working Principle
*Master sends:*

![images](https://github.com/VinhCao09/SOIL_INTEGRATED_Sensor_NPK-PH-MOISTURE-EC_InterfaceESP32/blob/main/images/read.jpg)

*Sensor responds:*

![images](https://github.com/VinhCao09/SOIL_INTEGRATED_Sensor_NPK-PH-MOISTURE-EC_InterfaceESP32/blob/main/images/respond.jpg)

*Calculations:*
```bash
Temperature: 14C H= 332=> temperature= 33.2℃
Humidity: 1D0 H= 464 => humidity= 46.4%
Conductivity: 2C H= 44 => Conductivity = 44 us/cm
PH: 5A H= 56 => PH= 9
Nitrogen (N): 20 H= 56 => N= 32 mg/kg
Phosphorus (P): 58 H= 56 => P= 88 mg/kg
Potassium (K): 68 H= 104 => K= 104 mg/kg
```
*Code:*
```bash
    unsigned int soilHumidity = (receivedData[3] << 8) | receivedData[4];
    unsigned int soilTemperature = (receivedData[5] << 8) | receivedData[6];
    unsigned int soilConductivity = (receivedData[7] << 8) | receivedData[8];
    unsigned int soilPH = (receivedData[9] << 8) | receivedData[10];
    unsigned int nitrogen = (receivedData[11] << 8) | receivedData[12];
    unsigned int phosphorus = (receivedData[13] << 8) | receivedData[14];
    unsigned int potassium = (receivedData[15] << 8) | receivedData[16];
```

## ⚛️Software - Programming language & Framework
- Programming for microcontroller: Arduino IDE (`2.3.2`)
  
## Version Recommend
*Version Arduino IDE:*
`2.3.2`

*Version Board:* ESP32 by Espressif Systems - `2.0.9`

*Version Library:* 

- EspSoftwareSerial by Dirk Karr, Peter Lerup - `8.1.0`

## How to use
*Schematic*

![images](https://github.com/VinhCao09/SOIL_INTEGRATED_Sensor_NPK-PH-MOISTURE-EC_InterfaceESP32/blob/main/images/schematic.jpg)

Change the pinout configuration

```bash
SoftwareSerial mySerial(17, 16);  // RX, TX

int DE =5;
int RE= 4;
```



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

![Logo](https://codingninja.asia/images/codeninjalogo.png)

