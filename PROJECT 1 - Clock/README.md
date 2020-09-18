# Clock 

A clock project with STM32F407.

## Features
* Set the clock through web with NodeMCU or manually
* Set an alarm with ADC or with a command into UART
  - alarm is ringing for 10 seconds then a 20 seconds delay until you cancel it with button
* Display it in the terminal with UART
  - you can use UART menu to choose what you want to change or know 
* Display it on a LCD Screen


## Requirements
* STM32
* LCD Screen ( with a i2c module if it is needed)
* FTDI to USB-TTL
* NodeMCU

## Versions

* v0.1 - TIMER configurations and UART to display it in the terminal with USB-TTL and ADC to set an alarm
* v0.2 - I2C to display it on the 2x16 LCD Screen with I2C Integrated Module
* v0.3 - Buzzer and a button added
* v0.4 - NodeMCU is fetching the time data through the web and communicate with STM through SPI and set the clock
