# openXsensor_vario_gps
Config files openXsensor for project Arduino NANO (CH340), MS5611 sensor and Breitan BN-220 GPS

After struggling with Breitan BN-220 gps settings, finally I got the gps data shown on my Taranis X9D with the standard lua scripts.
I will post the 3 config files, so others can benefit from it.
In these config files you can see that the BN-220 gps serial port is working at 9600 bps.
The problem is that when you buy a whatever GPS and try to use the openXsensor, you have greater change it doesnt work because the settings in the the sketch and the settings in the gps do not match.
So if you use my config files, make sure you set the speed of your BN-220 to 9600bps with the app U-Center. Get familiar with this tool otherwise you keep struggling with your GPS. There are great youtube video's that explain how it works but nobody explains the whole picture in one video because its really too much.
My hardware consists of:
FRSKY Taranis EU X9D ACCST Firmware:OpenTX-x9d+ version 2.3.9-otx (60e1edc1) Date 2020-06-14  EEPR :219
Receiver FRSKY EU S6r SPORT
Arduino NANO clone with mini USB connector and CH340 interface and ch340 serial port to USB adapter. This works always fine for me. No FTDI adapter because in the past my FTDI clone got bricked by Microsoft and the manufacturer of the original FTDI adapter causing tremendous problems in some hardware all over the world and also on my hardware. So I stay far away from it.
MS5611 sensor connected to SPI as adviced. I did not change pin numbers in the original sketch
Breitan BN-220 gps connected as adviced. I did not changed pin numbers in the original sketch

Software apps: U-center version 22.07
Arduino IDE latest version

Tips to consider
-The big trick is to change serial port speed of your GPS to 9600 bps in U-center and only use U-BLOX protocol as output. Default settings of the BN-220 are set to be 57600 bps, so you must 
I will make a youtube video asap how to do that
-Very important too: I read that the GPS only works if the vario works. If not then the program stops. So first you be sure the vario works fine. Then go on with the GPS.
-Buy a gps that has been proven to work with this sketch. Some gps you cannot change settings.
-Be sure that when you save settings in U-center, the settings are stored on your gps. Lots of time the settings are not stored. So retry and be sure
-Disconnect the GPS (I just disconnect the 5v wire) when you upload a new sketch to your Arduino NANO, otherwise it will not upload.
-the sketch only supports U-BLOX protocol. So NMEA settings are not needed in the config of your gps. Remove them.

So if everything works, you get your vario and GPS coordinates on your Taranis. It works great.
I will put the links of the hardware I bought for this project in the description of the YT video.
