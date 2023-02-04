# openXsensor_vario_gps
Config files and tips for openXsensor for project FRSKY Taranis X9D+ ACCST LBT, Arduino NANO (CH340), MS5611 barometer sensor and Breitan BN-220 GPS

After struggling with Breitan BN-220 gps settings, finally I got the gps data shown on my Taranis X9D with the standard lua scripts.
I will post the 3 config files, so others can benefit from it.

In these config files you can see that the BN-220 gps serial port is working at 9600 bps.

The problem is that when you buy a whatever GPS and try to use the openXsensor, you have greater change it doesnt work because the settings in the the sketch and the settings in the gps do not match.

So if you use my config files, make sure you set the speed of your BN-220 to 9600bps with the app U-Center. Get familiar with this tool otherwise you keep struggling with your GPS. There are great youtube video's that explain how U-Center works.

Nobody explains the whole project in one video because its really too much. 
It consists of:

-Know how to use Arduino IDE

-Buying the right hardware

-Know how to configure your Taranis with LUA scripts/upgrades/menu's etc. 

-Solder techniques

-Know a little bit about electronics otherwise you fry your hardware

-Know your way a bit in the OpenXsensor sketchup

-Know how to connect your gps with an serial port adapter like CH340 or FTDI

-Know how to use U-Center app

-Try to understand what you are doing

-Like to learn things

-Be patient, sleep over it when you are stuck in the project or learning. Your brains will make new connections when you are sleeping. Its no joke.

So this project is not for beginners, but with perseverence you can make it to the end.

My hardware consists of:

-FRSKY Taranis EU (aka LBT) X9D ACCST Firmware:OpenTX-x9d+ version 2.3.9-otx (60e1edc1) Date 2020-06-14  EEPR :219

-Receiver FRSKY EU (aka LBT) S6r SPORT

-Arduino NANO clone with mini USB connector and CH340 serial port to USB adapter. This works always fine for me. No FTDI adapter because in the past my FTDI clone got bricked by Microsoft and the manufacturer of the original FTDI adapter causing tremendous problems in some hardware all over the world and also on my hardware. So I stay far away from it.

-MS5611 sensor connected to SPI as adviced. I did not change pin numbers in the original sketch

-Breitan BN-220 gps connected as adviced. I did not changed pin numbers in the original sketch

Software apps:

- U-center version 22.07 

- Arduino IDE latest version

Very important tips:

-For the used LUA telemetry scripts goto github account moschotto/OpenTX_GPS_Telemetry

-Make sure that your FRSKY Taranis radio is a least on OpenTX 2.3.x

-The big trick is to change serial port speed of your GPS to 9600 bps in U-center and only use UBX protocol as output. Default settings of the BN-220 are set to be 57600 bps, so you must always check the speed with U-Center.

-Consider buying GPS and vario Sensor that all work on same volt, so you dont have to struggle with different voltages like 3.3 for your GPS and 5 for your vario sensor.

-Use a breadboard to prototype your setup. When everything works put it together for your plane.

-Keep in mind when you make the final assembly of your hardware that you must be able to disconnect the GPS, otherwise uploading does not work. Being able to disconnect the 5volt wire does the job.

-Very important: I read that the GPS only works if the vario works. If not then the program stops. So first you must be sure the vario works fine. Then go on connecting and configuring the GPS.

-Buy a gps that has been proven to work with this sketch. Some gps you cannot change settings to your like, e.g. baudrate.

-Be sure that when you save settings in U-center, the settings are stored on your gps. Lots of time the settings are not stored. So retry and be sure. Save your settings to a file on your computer so you can use again for other projects or restore a backup.

-The sketch only supports UBX (binary) protocol. So NMEA settings are not needed in the config of your gps. Remove them.

So if everything works, you get your vario and GPS coordinates on your Taranis. It works great.
I will put the links of the hardware I bought for this project in the description of the YT video.
