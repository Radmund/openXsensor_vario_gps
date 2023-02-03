# openXsensor_vario_gps
Config files openXsensor for project Arduino NANO (CH340), MS5611 sensor and Breitan BN-220 GPS

After struggling with Breitan BN-220 gps settings, finally I got the gps data shown on my Taranis X9D with the standard lua scripts
I will post the 3 config files, so others can benefit from it.
In these config files you can see that the BN-220 gps serial port is working at 9600bps.
The problem is that when you buy a whatever GPS and try to use the openXsensor, you have greater change it doesnt work because the settings the sketch and the settings in the gps do not match.
So if you use my config files, make sure you set the speed of your BN-220 to 9600bps with the app U-Center. Get familiar with this tool otherwise you keep struggling with your GPS.
There are great youtube video's that explain how it works but nobody explains the whole picture in one video because its really too much.
