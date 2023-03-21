# IoT_Samples
Esp32 based IoT applications

## Development Environment
- Install preferably Ardunio IDE or VsCode with Ardunio extension or other IDEs to start. [Arduino IDE link](https://www.arduino.cc/en/software)
- At IDE Toolbar; navigate to **File-Preferences Additional boards manager URLs** and paste "https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json" without quotes  .This is the latest esp32 url. (needed for default *analogWrite()* etc.)
- Navigate to **Tools-Board-Boards Manager** then search for *esp32* and install the latest package version.
- Navigate  to **Tools-Board-esp32-Esp32 Dev Module** to select your board.After that , navigate to **Tools-Port** and select a port to use.
- Generate a sample code file and try to upload it to your board.If you got errors, try with different ports and if you still got errors, try to download or update your usb port driver.[USB Port Driver Link](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers?tab=downloads). After downloading driver,right click *silabser.inf* and install the driver.
