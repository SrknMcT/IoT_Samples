# IoT_Samples
Esp32 based IoT applications

## Development Environment
- Install preferably Ardunio IDE or VsCode with Ardunio extension or other IDEs to start. [Arduino IDE link](https://www.arduino.cc/en/software)
- At IDE Toolbar; navigate to **File-Preferences Additional boards manager URLs** and paste "https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json" without quotes  .This is the latest esp32 url. (needed for default *analogWrite()* etc.)
- Navigate to **Tools-Board-Boards Manager** then search for *esp32* and install the latest package version.
- Navigate  to **Tools-Board-esp32-Esp32 Dev Module** to select your board and connect it to your pc.After that , navigate to **Tools-Port** and select a port to use.
- Generate a sample code file and try to upload it to your board.If you got errors, try with different ports and if you still got errors, try to download or update your usb port driver.[USB Port Driver Link](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers?tab=downloads). After downloading driver,right click *silabser.inf* and install the driver. 
- Lastly, if you get *"the last usb device you connected to this computer malfunctioned and windows does not recognise it"* error , change usb cable to an original one. If the error continues, follow the instrunctions on the link [USBErrorFix](https://www.youtube.com/watch?v=kRn2IWjVR7g) .

## Esp32 and Peripherals

**NodeMCU Esp-32S, 38 pin**
  - 34-35-36-39 are input-only pins.
  - 1-3 internal pins ( for UART communication with the PC )
  - 6-7-8-9-10-11 are internal pins ( Connected to the internal flash )
  
![Esp32 38 pin](/assets//Esp32.png)

**L298n as H-Bridge**

- Remove all three jumpers on l298n
- ENA, ENB pins can be freed up if pwm signals aren't needed to use. 

![H Bridge](/assets//HBridge.PNG)

**Keypad 4x4**

Keypad(4x4) has 4 row-pins(R1,R2,R3,R4) and 4 column-pins(C1,C2,C3,C4)  
"*Keypad 3.1.1 library by M. Stanley, A. Brevig*" can be used.(before a library installation, make sure of saving your code file.) 

![4x4 Keypad](/assets/keypad.PNG)

**IPS Panel 240x240**

To use ips panel properly, install "*TFT_eSPI by Bodmer*" library and use the default pins below for esp32:  

BLK --> -    
DC  --> 2  
RST --> 4  
SDA --> 23  
SCL --> 18  
GND --> GND  
VCC --> VCC  
(These are for 38 pin esp32s which we actively use, the picture below is different)  

![240x240 IPS](/assets/ips240x240.jpg)
