# Pi_stats_OLED
Show your Raspberry Pi stats on an i2c OLED display.  e.g. IP address, CPU load, memory usage, SD usage and temperature

This Sktipt is based around the Adafruit_Python_SSD1306 (https://github.com/adafruit/Adafruit_Python_SSD1306) library and inspired by RPI_SSD1306 (https://github.com/xxlukas42/RPI_SSD1306).

# HOW TO:

Connect to your Pi via SSH
---
Install some depentencies for the library
sudo apt-get install build-essential python-dev python-pip
---
Install the RPI.GPIO library
sudo pip install RPi.GPIO
---
Install the Python Imaging Library and smbus library
sudo apt-get install python-imaging python-smbus
---
Install git
sudo apt-get git
---
Clone the Adafruit SSD1306 python library
git clone https://github.com/adafruit/Adafruit_Python_SSD1306.git
---
Clone this repository
git clone https://github.com/David-Ka/Pi_stats_OLED
---
Enable i2c and restart the Pi
---
Scan for devices
sudo i2cdetect -y 1
---
Go to /Pi_stats_OLED and run stats.py
sudo python stats.py
----------
Run it on boot 

go in the Pi_stats_OLED dir
give permissions to execute
chmod 755 launcher.sh
---
go to the root user

edit crontab
crontab -e
---
put this in crontab
@reboot sh /home/pi/Pi_stats_OLED/launcher.sh &
---
reboot
you are done
