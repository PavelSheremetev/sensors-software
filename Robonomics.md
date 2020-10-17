# Connecting sensors to robonomics network
### Requiremets
* ESP8266 Node MCU v3
* particle sensor SDS011
* micro USB cable
* connecting wires

### Installation
Install platformio:
```bash
pip install -U platformio
```
Clone ropository with firmware
```bash
git clone https://github.com/LoSk-p/sensors-software
cd sensors-software/airrohr-firmware
```
Connect your ESP to computer via micro USB and upload firmware:
```bash
platformio run -e nodemcuv2_en -t upload
```
You can choose language changing "nodemcuv2_en".

In the end you will see

![upload](https://github.com/LoSk-p/media/blob/master/esp/upload.jpg)

### Configuration
Connect to airRohr--xxxxxxx wi-fi network and in your browser write address 192.168.4.1:

![menu](https://github.com/LoSk-p/media/blob/master/esp/menu1.jpg)

Go to Configuration and in Wi-Fi Settings add information about your wi-fi network:

![config](https://github.com/LoSk-p/media/blob/master/esp/config.png)

Reboot NodeMcu and it will connect to your wi-fi.

Find NodeMcu in local network, for ubuntu firstly find your address:
```bash
ip a
```

![ipa](https://github.com/LoSk-p/media/blob/master/esp/ipa.jpg)

Then you can find NodeMcu with nmap (use your address with "0" in the end):
```bash
nmap -sn 192.168.100.0/24
```
Write in your browser it's local address, go to Configuration and tick 'API Robonomics'. 

![robonomics](https://github.com/LoSk-p/media/blob/master/esp/APIrobonomics.jpg)

Then enable GPS and all sensors that you use and write your coordinates:

![gps](https://github.com/LoSk-p/media/blob/master/esp/gps.jpg)

### Results
Go to [sensors.robonomics.network](https://sensors.robonomics.network/#/), and you will see your sensor on the map.
![map](https://github.com/LoSk-p/media/blob/master/esp/map.jpg)