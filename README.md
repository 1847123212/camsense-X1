# camsense-X1
unofficial reverse engineering of a Chinese LiDAR. 

Discussed this on my discord: https://discord.gg/zRGJcqa

![alt text](doc/camsense2.jpg)
![alt text](doc/camsense.jpg)


## Electrical Connections
There are 3 pins needed to connect to the lidar: 5V, GND and TX. For this you can use the mounted connector(part number unknown) or solder some pinheader to the pcb.

A FTDI adapter is used to connect the lidar to a computer. The TX pin of the lidar needs to be connected to the RX pin of th FTDI adapter. The lidar can be powered using the 5V of the FTDI adapter.

![alt text](doc/lidar_wiring.png "Connection diagram")

## Communication Protocol

still not fully known...

<0x55><0xAA><0x03><0x08><br>
\<speedL>\<speedH><br>
\<unknown>\<unknown><br>
\<distance0L>\<distance0H>\<quality0><br>
\<distance1L>\<distance1H>\<quality1><br>
\<distance2L>\<distance2H>\<quality2><br>
\<distance3L>\<distance3H>\<quality3><br>
\<distance4L>\<distance4H>\<quality4><br>
\<distance5L>\<distance5H>\<quality5><br>
\<distance6L>\<distance6H>\<quality6><br>
\<distance7L>\<distance7H>\<quality7><br>
\<unknown>\<unknown><br>
\<unknown>\<unknown><br>
