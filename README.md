# esp-snmp
SNMPv2 monitoring device based on <b>ESP32</b> and <b>LAN8720A</b> (LILYGO®TTGO T-Internet-POE)
<br>The device has the following functionality:
- ESP32 + LAN8720A
- support of the SNMPv2 protocol,
- PoE,
- web configuration ,with basic authentication, no SSL support,
- OTA wirmware update,
- static or dynamic IP,
- the ability to work with sensors DS18b20, DHT11, DHT22, AM2302, RHT03,
- dry contact with operation counter,
- ADC input.
- automatic MIB address generation depending on the type of port and sensor.
<br>
Web config http://ip/cfg/<br><br>

<img src="https://github.com/llams/esp-snmp/blob/main/img/MAIN.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/SNMP.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/IO.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/IO-DS.PNG">

<br>The data is collected by the Zabbix server.
<img src="https://github.com/llams/esp-snmp/blob/main/img/zabbix-data.PNG">
<img src="https://github.com/llams/esp-snmp/blob/main/img/zabbix-graph.PNG">
