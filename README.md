# W5200 Ethernet Shield
W5200 Ethernet Shield is compatible with Official [Arduino Ethernet Shield](http://arduino.cc/en/Main/ArduinoEthernetShield) and support fast SPI and 8 sockets. 

![W5200 Ethernet Shield](http://blog.wiznet.co.kr/FIles/W5200_Ethernet_Shield.jpeg "W5200 Ethernet Shield")

## Hardware
These are PCB files for the W5200 Ethernet Shield for Arduino. The files were created in the free & low cost EagleCad software available from [CadSoft](http://www.cadsoftusa.com/download-eagle/?language=en).


## Software
You need to change the existing W5100 files to W5200 library files.

1. Install W5200 library
   Overwrite w5100.cpp, w5100.h to the "/libraries/Ethernet/utility" folder in your Arduino IDE. 

2. Using the W5200 library and evaluate existing Ethernet example.
   In the Arduino IDE, go to Files->Examples->Ethernet and open any example, compile and upload the file to Arduino board.

3. Note: libraries/Ethernet/Ethernet.h needs the following at line 10 instead of #define MAX_SOCK_NUM 4, since it doesn't #include "w5100.h" anymore:

 `#ifdef W5200`

 `#define MAX_SOCK_NUM 8`

 `#else`
 
 `#define MAX_SOCK_NUM 4`

 `#endif`



## Revision History
Initial Release : 10 June 2013


