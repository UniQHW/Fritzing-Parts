# Nude Audio Move S
![Move S](https://rawgit.com/UniQHW/Fritzing-Parts/master/NudeAudio/MoveS/MoveS_Breadboard.svg)

### Pin Out

This section lists all exposed pins on the Nude Audio Move S Circuit board :

|Pin|Description|
|---|-----------|
|BT_LED +|Bluetooth LED +|
|BT_LED -|Bluetooth LED -|
|PWR_LED_VIN|Common Power LED anode (or cathode?)|
|PWR_LED_Green|Power LED Green|
|PWR_LED_Red|Power LED Red|
|BAT|Battery VCC|
|BAT_GND|Battery GND|
|SPK +|Speaker +|
|SPK -|Speaker -|
|SPK+ Pad|Speaker+ Pad|
|SPK- Pad|Speaker- Pad|
|VCHG|Charging Voltage|
|BT_ON/OFF|Battery On/Off gate|
|VBAT|Battery Voltage|
|JTAG_GND|Microcontroller JTAG GND|
|JTAG_SDA|Microcontroller JTAG SDA (For Adress Data related I2C Communication)|
|JTAG_SCL|Microcontroller JTAG SCL (For clock and wait controll for I2C Communication)|
|JTAG_WP|Microcontroller JTAG WP (Write Protection)|
|SPI_CLK|Microcontroller SPI Bus Clock|
|SPI_MOSI|Microcontroller SPI Bus Master Output Slave Input|
|SPI_MISO|Microcontroller SPI Bus Master Input Slave Output|
|SPI_CSB|Microcontroller SPI Chip Select Bus|
|USB_VBUS|Micro USB 5V input|
|USB_GND|Micro USB GND|
|Audio Jack|Headphone Audio Jack|

### Device Flow
This flowchart gives a rough overview about the device runtime : 

### Exploitation
The Nude Audio Move S comes with a fairly hackable circuit. 

Upon opening the speaker case, one will likely first stumble upon the exposed JTAG pins that can control the embedded BT chip using I2C and SPI communication protocols. Additionally, battery, speaker and charging pads can be found across the board. 

While providing less options, the device also exposes male connectors, such as the speaker pins and the battery pins. The device comes with two LEDs, one indicating the BT connection state, the other the Power State. Cutting the top off both LEDs will grant the user with more readable data, as the remaining legs can be used as readable male connectors.
