# ELET114A dual-mode (Dual Mode) Bluetooth module
* made by www.elinketone.com
* supports Bluetooth 3.0 / 2.1 + EDR and 4.0 (BLE) specification
* has passed CE (HS0000174), FCC (2ACWW13002), BQB (QDID: 59836) Certification

Changes:

2015.01.12 V2.1.1

* increase the measured power data module
* increase CE, FCC, BQB information

2015.01.27 V2.2

* increase LED and GPIO control in reference to the schematic diagram indicating the status of the Bluetooth connection

2015.01.29 V2.2.1

* updated reference schematics Notes

1. Outline

ELET114A Shenzhen Yi Autopass Technology Co., Ltd. is designed for intelligent wireless data transmission and to create a dual-mode Bluetooth module, follow BT2.1 + EDR / 3.0 / 4.0 Bluetooth specification, branched Bluetooth serial port protocol support SPP, HID, BLE, etc; also do Bluetooth master mode (Host), Connection SPP, HID, BLE device (Device).
Module integrated ARM® Cortex™-M0 US Broadcom (Broadcom) Bluetooth chip, CPU frequency up to 48MHz, rich interface resources, can meet customer demand, tailor Proprietary software system. Supports UART, SPI, I2C, I2S interfaces, including 4 PWM Ports and six 12bit ADC channels, high integration, low power consumption, Bluetooth radio property Can advantageous characteristics.

2. Features

  * support BT3.0 + EDR and BT4.0 (BLE) Dual-Mode, both modes can work simultaneously
  * support low power, sleep (Sleep) current of 50uA
  * Bluetooth (Device) Profile, SPP, HID, BLE, transparent data transmission solutions
  * Bluetooth (Host), can be connected to Bluetooth SPP, HID, BLE and other equipment (Device)
  * support to meet customer demand, tailored proprietary software; CPU frequency up to 48MHz, rich interface resources
  * support high-speed serial interface (UART), maximum support 921600 baud rate
  * support upgrade the air (OTA) firmware to solve the customer's worries
  * module as SMD chip technology, semi-hole pin, ROHS process
  * Built-in 2.4G PCB antenna, users do not need an antenna debugging; also supports external antenna, long-distance transmission
  * adaptive frequency hopping technology, high-performance wireless transceiver system, in open areas, more than 50 meters away from the transceiver
  * Easy to use for close-serial transparent transmission of wireless alternatives, without understanding the Bluetooth protocol specific development

3. Applications

This module is mainly used in the field of wireless transmission of data over short distances, it can be easily and PC, smart phones and other non Bluetooth devices on the wireless terminal is connected, it can also exchange data between two modules, to avoid the cumbersome cable connections And space limitations, can be a direct replacement for the serial cable.
  * Bluetooth and RS232 (RS483) serial data conversion
  * Bluetooth wireless data transmission
  * medical and industrial equipment distributed remote control
  * Bluetooth printer, bar code scanning equipment
  * POS system, wireless keyboard, mouse
  * Remote control and monitoring
  * indoor positioning, alarm
  * wireless meter reading, wireless data collection
  * building automation, security, wireless monitoring and control room equipment, access control systems
  * intelligent home, industrial control
  * automotive testing equipment
  * wireless LED display system, touch screen equipment
  * Bluetooth joystick, Bluetooth game pad, Bluetooth remote control, remote control toys

4. Physical characteristics

| | |
|---|---
| Operating Frequency Band | 2.4GHz-2.48GHz unlicensed ISM band
| Bluetooth Specification | V2.1 + EDR, BT3.0, BT4.0 (BLE)
| Output Power Class | Programmable Class 1, Class 2 or Class 3
| RX Sensitivity | -88dBm
| Operating Voltage | 3.3V
| Main Digital Interface | UART
| Other Interface | 1 Ge SPI, 2 Ge I2C, 1 an I2S
| PIO Control | 4 Ge PWM, 6 Ge ADC, 27 GPIO lines
| Dimension | 27mm (L) x 13mm (W) x 2mm (H)

5. Electrical Characteristics

Absolute Maximum Ratings

| Rating | Min | Max
|---|---|---
| Storage Temperature | -40 ℃ | + 85 ℃
| Operating Temperature | -30 ℃ | + 85 ℃
| Supply Voltage: VDD | 2.2V | 3.6V
| Other Terminal Voltages | VSS-0.3V | VDD + 0.3V

6. Interface Specification

| | |
|---|---|---
| Normal Power Supply: | + 3.3V
| Operating Current: | <20mA (average)
| Host Interface | UART serial ports (CMOS, TTL level)
| Interface signals | RX, TX, CTS, RTS

7. Typical circuit and PIN pin definitions

![alt text](https://github.com/RussNelson/ELET114A/blob/master/otherdocs/elet114a-schematic2.jpg "ELET114A schematic")

| Pin.No | Name | Type | Description
|---|---|---|---
| 1 | UART_TX | O | UART transmitted data output pin
| 2 | UART_RX | I | UART received data input pin
| 3 | UART_CTS | I/O | UART clear to send input pin
||||    General purpose digital input and output pin
| 4 | UART_RTS | I/O | UART request input pin
||||    General purpose digital input and output pin
| 5 | AIO1 | I/O | BT_WAKEUP, digital input pin, MCU (customer controls) Bluetooth module wakeup
||||    0: low level (LOW) Bluetooth module into the power-saving sleep mode
||||    1: high level (HIGH) wake Bluetooth module
||||    Note: When the MCU to send data to a Bluetooth module, the first BT_WAKEUP
||||    From a low level (LOW) pulled high (HIGH), then send the data to the UART
| 6 | AIO2 | I/O | CMD / DATA_SWITCH, digital input pin, switching data mode and command mode
||||    (Bluetooth module connected state)
||||    0: low level (LOW), digital mode (Data transfer mode)
||||    1: high level (HIGH), the command mode (Command mode)
||||    Note: When the Bluetooth module in the connected state, this pin is useful; when in Bluetooth module
||||    Non-connected state, are in command mode
| 7 | AIO3 | I/O | HOST_WAKEUP, digital output pin, a Bluetooth module wakeup MCU (customer control Device)
||||    0: output low (LOW), indicates that the serial data is not sent to the MCU
||||    1: output high (HIGH), indicates the serial port has data to send to the MCU
||||    Note: When the Bluetooth module has sent data to the MCU, this pin will be from a low level (LOW)
||||    Goes high (HIGH), wake the MCU receives data
| 8 | AIO4 | I/O | General purpose digital input and output pin,
||||    PWM2: PWM output
| 9 | ICE_DATA | I/O | Serial data pin debugger
| 10 | ICE_CLK I debugger serial clock pin
| 11 | RESET # I External reset input, active low with internal pullup
| 12 | VCC Power 3.3V external power input
| 13 | GND0 Ground Ground
| 14 | AIO5 | I/O | General purpose digital input and output pin,
||||    ADC4: ADC analog input
| 15 | AIO6 | I/O | General purpose digital input and output pin,
||||    ADC3: ADC analog input
| 16 | AIO7 | I/O | SPI slave select pin
||||    General purpose digital input and output pin
||||    I2S channel around the clock
| 17 | AIO8 O SPI MOSI (master output, slave input)
||||    General purpose digital input and output pin
||||    I2S data output
| 18 | AIO9 I SPI MISO (master input, slave output)
||||    General purpose digital input and output pin
||||    I2S data input
| 19 | AIO10 | I/O | SPI Serial Clock pin
||||    General purpose digital input and output pin
||||    I2S bit clock pin
| 20 | AIO11 | I/O | General purpose digital input and output pin,
||||    PWM3: PWM output pin
||||    I2SMCLK: I2S master clock output pin
| 21 | GND1 Ground Ground
| 22 | GND2 Ground Ground
| 23 | BIO0 | I/O | General purpose digital input and output pin,
||||    ADC5: ADC analog input
| 24 | BIO1 | I/O | General purpose digital input and output pin,
|||   25 | BIO2 | I/O | General purpose digital input and output pin,
||||    I2C1 the clock pin
| 26 | BIO3 | I/O | General purpose digital input and output pin,
||||    I2C1 data input and output pins
| 27 | BIO4 | I/O | General purpose digital input and output pin,
||||    I2C0 the clock pin
||||    A typical LED control circuit is added, customers can request custom status, such as:
||||    When the Bluetooth is not connected: LED flashes
||||    When the Bluetooth connection: LED lit
| 28 | BIO5 | I/O | General purpose digital input and output pin,
||||    I2C0 data input and output pins
||||    Typical circuit added BT_STATUS level output, according to requirements definition, such as:
||||    When the Bluetooth is not connected: BT_STATUS output low
||||    When the Bluetooth connection: BT_STATUS output high
| 29 | BIO6 | I/O | General purpose digital input and output pin,
||||    External interrupt input pin 1
| 30 | BIO7 | I/O | General purpose digital input and output pin,
||||    ADC2: ADC analog input
| 31 | BIO8 | I/O | General purpose digital input and output pin,
||||    ADC1: ADC analog input
| 32 | BIO9 | I/O | General purpose digital input and output pin,
||||    ADC0: ADC analog input
| 33 | BIO10 | I/O | General purpose digital input and output pin,
||||    PWM0: PWM output
| 34 | BIO11 | I/O | General purpose digital input and output pin,
||||    PWM1: PWM output
When not in use leave GPIO disconnected.

8. Module Reference PCB package size

![alt text](https://github.com/RussNelson/ELET114A/blob/master/otherdocs/elet114a-footprint.png "ELET114A footprint")
Above the yellow border is the area of the 2.4G Bluetooth antenna. The PCB area directly below is subject to the clearance process. Keep the antenna area as much as possible away from metal objects. Usually the Bluetooth module antenna is placed near the edge of the PCB.

9. Measured power data

| Operation | Peak Current | Average Current | Note
|---|---|---|---
||  ELET114A | ELET114A |
| Disconnected ||  0.05mA
| Class BR / EDR connected + Sniff | | 2.19mA | No data was transmitted, Sniff (40 20 4 0)
| Class BR / EDR connected + Receiving | 22.5mA | | 
| BLE connected + Sniff | | 1.12mA | No data was transmitted.  connection interval = 20ms (LE_Connection_Interval_Max = 0x0010)
| BLE connected + Receiving | | 16.34mA | connection interval = 20ms (LE_Connection_Interval_Max = 0x0010)

10. Typical Application

After the Bluetooth 4.0 (BLE) protocol appears Apple IPHONE 4S or later the phone began to support BT4.0,
Developers can be used directly BT4.0 terminal product development, rather than requiring complex licensing and support Apple MFI
Pay the appropriate licensing fees, so that a developer iOS Bluetooth peripherals BT4.0 best choice.
But for the Android operating system, in particular in the following versions Android4.3 not supported BT4.0 agreement,
Only supports traditional Bluetooth SPP protocol. Therefore, the traditional Bluetooth developers often only two programs using the final production of Bluetooth
The end product: Bluetooth SPP module on Android, using BT4.0 modules on iOS. This leads to students
Rising production costs and inconvenience to users.
Our research and development production ELET114A dual-mode (Dual-Mode) Bluetooth module can support Bluetooth 4.0, and with
When classic mode SPP protocol support, to achieve a variety of operations including iOS (Apple system), Android (Andrews), etc.
System compliant result, Bluetooth devices allows developers to easily achieve the upgrading of products to enhance the inherent product
value!


11. Information
Consulting and marketing services
Email: 13990980 @ qq.com
Mobile: 13903026250
QQ: 13990980 449617984 395872313 2048375151
Website: http://www.elinketone.com

