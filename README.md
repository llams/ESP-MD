# esp-snmp
SNMPv2 monitoring device based on <b>ESP32</b> and <b>LAN8720A</b> (LILYGO®TTGO T-Internet-POE)
<br>The device has the following functionality:
- ESP32 + LAN8720A
- support of the SNMPv2 protocol,
- PoE,
- web configuration ,with basic authentication, no SSL support,
- OTA firmware update,
- static or dynamic IP,
- dry contact with operation counter, on all available ports for <a href="https://github.com/Xinyuan-LilyGO/LilyGO-T-ETH-POE">LILYGO®TTGO T-Internet-POE</a>, IO4, IO16, IO32, IO34, IO35, IO36, IO39,
- the ability to work with sensors DS18b20, DHT11, DHT22, AM2302, RHT03 on ports IO4, IO16, IO32,
- ADC input on ports IO34, IO35, IO36, IO39,
- automatic MIB address generation depending on the type of port and sensor.
<br>
Web config http://ip/cfg/<br><br>

<img src="https://github.com/llams/esp-snmp/blob/main/img/MAIN.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/SNMP.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/IOList.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/IOCfg.PNG">

<br>The data is collected by the Zabbix server.
<br>Template allows dynamically detect port settings.
<br>
<img src="https://github.com/llams/esp-snmp/blob/main/img/ZABBIX.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/ZABBIXCfg.PNG">
