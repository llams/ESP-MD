# ESP-MD (ESP Measuring Device)
This firmware allows you to use the ESP32 as SMTPv2 server to receive and publish data from digital or analog sensors, as well as from the digital inputs of the controller.
<br>
<br>
The project uses the library <a href="https://github.com/0neblock/Arduino_SNMP">SNMP_Agent</a>  
<br>
<b>Key features:</b><br>
- all settings and control of the controller is carried out through the web interface,
- available ports can be configured by the user for available functionality depending on the selected interface,
- I2C support,
- 1 Wire sensors and bus support,
- support of the SNMPv2 protocol,
- web configuration, with basic authentication, no SSL support,
- OTA firmware update,
- static or dynamic IP,
- automatic OID address generation depending on the type of port and sensor.
- three firmware options are presented depending on the periphery:<br>
<b>a) <a href="https://github.com/Xinyuan-LilyGO/LilyGO-T-ETH-POE">LILYGO®TTGO T-Internet-POE</a></b> - ESP32 + LAN8720A:<br>
- LAN & PoE 802.3at,<br>
- available ports IO2, IO4, I12, IO16, IO32, IO34, IO35, IO36, IO39.<br>
<b>b) <a href="http://www.wireless-tag.com/portfolio/wt32-eth01/">WT32-ETH01</a></b> - ESP32 + LAN8720A:<br>
- LAN & PoE,<br>
- available ports IO2, IO4, IO5, I12, IO14, IO15, IO17, IO33, IO35, IO36, IO39.<br>
<b>c) ESP32-WROOM</b>:<br>
- Wi-Fi,
- available ports IO4, IO12, IO14, IO16, IO18, IO19, IO23, IO25, IO26, IO27, IO32, IO33, IO34, IO35, IO36, IO39,
- IO13 set to factory reset, you need to connect to GND and apply power, then open the circuit.
<br>
<b>Supported input functions:</b>
<br>
1. digital <b>input</b>, the port status and the number of operations since power-up are monitored, the choice of the edge of the event latching, pressing, releasing, or both at once is supported,
<br>
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/IO_input.png">
2. digital <b>output</b> (functionality is under development, the purpose for the monitoring device has not yet been determined),
<br>
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/IO_output.png">
3. sensor <b>DS18B20</b>, connection of one digital sensor, it is possible to set the polling period of the sensor, 10-254 * 0.1 second, taking into account the multiplier (1-25 seconds),
<br>
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/IO_DS18B20.png">
4. sensors <b>DHT11</b>, <b>DHT22</b>, <b>AM2302</b>, <b>AM2303</b>, <b>RHT03</b>, connection of one digital sensor, it is possible to set the sensor polling period, 10-254 * 0.1 second, taking into account the multiplier (1-25 seconds),
<br>
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/IO_AM2303.png">
5. bus sensors <b>DS18B20</b> up to 10 pieces on one port. In total, up to 120 sensors can be connected to the controller with a Wi-Fi connection (in firmware without support for LAN connection).
<br>
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/IO_DS_BUS.png">
The procedure for scanning connected sensors has been implemented. The address is assigned to the logical number of the sensor on the bus and is stored in the non-volatile memory of the controller.
<br>
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/IO_DS_BUS_Scan.png">
6. sensors connected to the I2C bus. The following sensors <b>BME280</b>, <b>HTU21D (Si7021)</b> and <b>BH1750</b> are supported. To connect sensors of this type, two ports are used, depending on the firmware, the port numbers differ, so for LILYGO®TTGO T-Internet-POE it is SDA IO33 and SCL IO32 (P5 and P4), for WT32-ETH01 it is SDA IO15 and SCL IO14 (P4 and P3), for ESP32-WROOM these are SDA IO33 and SCL IO32 (P11 and P10).
<br>
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/IO_I2C.png">
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/HTU.png">
7. analog input <b>ADC</b>, displays the actual value from the analog-to-digital converter of the port (where available).
<br>
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/IO_ADC.png">
<br>
Web http://ip/
<br>
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/ui_main.gif">
<br>
<br>
Example snmpwalk output OIDs
<br>
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/OIDs.png">
<br>
Template for Zabbix server allows dynamically detect port settings.
