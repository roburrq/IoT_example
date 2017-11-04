# Project Title

controlling ESP32 GPIO ports from a webserver

### Prerequisites

An ESP32 and three cable and a RGB LED.

connect them together.

### Connecting LED to the ESP32

### Installing and running ESP32

first need to install baseboards

```
wget http://micropython.org/resources/firmware/esp32-20171021-v1.9.2-280-g2305d848.bin
esptool.py -p /dev/ttyUSB0 -b 460800 erase_flash
esptool.py -p /dev/ttyUSB0 -b 460800 write_flash --flash_mode dio 0x1000 esp32-*.bin
```
and then going to Python prompt

```
picocom -b115200 /dev/ttyUSB0
```
You can check the Python version as well 

```
import sys
sys.version # This should return 3.4.0 at the moment
```
### Running on webserver

Start with boot.py. 
firstly Update the IP address for webserver.
and then need to open main.py and run it in python. Then go to your browser and type the webserver IP address and then you would be able to blink the LED from the browser.





## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
