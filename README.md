# esp-snmp
SNMPv2 monitoring device based on <b>ESP32</b> and <b>LAN8720A</b> (LILYGO®TTGO T-Internet-POE or WT32-ETH01)
<br><b>The device has the following functionality:</b>
- ESP32 + LAN8720A
- support of the SNMPv2 protocol,
- web configuration ,with basic authentication, no SSL support,
- OTA firmware update,
- static or dynamic IP,
- automatic OID address generation depending on the type of port and sensor.
<br><b>LILYGO®TTGO T-Internet-POE</b>
- PoE 802.3at,
- dry contact with operation counter, on all available ports for <a href="https://github.com/Xinyuan-LilyGO/LilyGO-T-ETH-POE">LILYGO®TTGO T-Internet-POE</a>, IO2, IO4, I12, IO16, IO32, IO34, IO35, IO36, IO39,
- the ability to work with sensors DS18b20, DHT11, DHT22, AM2302, RHT03 on ports IO2, IO4, I12, IO16, IO32,
- 1 Wire bus support with DS18B20 on ports IO2, IO4, I12, IO16, IO32,
- ADC input on ports IO34, IO35, IO36, IO39,
- I2C support BME280 and BH1750 (I2C bus on SDA IO33 and SCL IO32),
<br><b>WT32-ETH01</b>
- dry contact with operation counter, on all available ports for <a href="http://www.wireless-tag.com/portfolio/wt32-eth01/">WT32-ETH01</a>, IO2, IO4, I12, IO14, IO15, IO33, IO35, IO36, IO39,
- the ability to work with sensors DS18b20, DHT11, DHT22, AM2302, RHT03 on ports IO2, IO4, I12, IO14, IO15, IO33,
- 1 Wire bus support with DS18B20 on ports IO2, IO4, I12, IO14, IO15, IO33,
- ADC input on ports IO33, IO35, IO36, IO39,
- I2C support BME280 and BH1750 (I2C bus on SDA IO15 and SCL IO14),
<br>
Web config http://ip/<br><br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/INFO.PNG">
<br>
Web config http://ip/cfg/<br><br>

<img src="https://github.com/llams/esp-snmp/blob/main/img/MAIN.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/SNMP.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/IOList.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/IOCfg.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/BUS.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/BUSScan.PNG">

<br>The data is collected by the Zabbix server.
<br>Template allows dynamically detect port settings.
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/ZABBIX.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/ZABBIXCfg.PNG">
