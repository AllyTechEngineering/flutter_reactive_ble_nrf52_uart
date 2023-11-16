# flutter_reactive_ble_example_two
## This project connects the nrf52 DK running the sample hex file for the BLE UART Service
- You will need to be able to setup the nrf52 DK and load the nordic required software.
- Be familiar with programming the nrf52 DK using the nrfConnect programming software.
- Understand how to deal with the many issues that may come up while setting up the nordic system.
- Understand how to use the nrfConnect serial port app.
- 90% of the difficulty in getting this to work is dealing with the Nordic stuff!

## Getting Started
### Equipment and Software needed 
You will need a nordic Semiconductor nrf52DK dev kit.
https://www.nordicsemi.com/Products/Development-hardware/nRF52-DK
## DO NOT Update the Interface MCU Firmware with the downloads on this page. 
If you allow the system to update the Interface MCU Firmware you may brick the nRF52 DK.
- If that happens you need to install the nRF Command Line Tools
- https://www.nordicsemi.com/Products/Development-tools/nrf-command-line-tools/download
- After a successful install you need to check if you can connect to the nRF52 DK
- In a terminal program you can use nrfjprog --deviceversion and you should get an id from the device.
- If not then you will need to trouble shoot your setup and that is out of scope of this readme.
- If you can connect to the nRF52 DK use nrfjprog --recover and this should un-brick your nRF52DK.
- After a recover you will need to use nRFConnect to reload the UART hex file.

### You will need the nRF Connect to Desktop
You will use the serial port and the programmer apps.
https://www.nordicsemi.com/Products/Development-tools/nrf-connect-for-desktop

The Nordic Semiconductor documentation is difficult to navigate and links may change.
At the time of writing this here are the key links:
### Explains how to test - go to the Testing section.
 You will not need to use PuTTY! You can use the nrfConnect serial port app instead.
https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/samples/bluetooth/peripheral_uart/README.html

### This link gives more details such as the services and characteristics UUID.
https://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.sdk5.v15.0.0%2Fusbd_ble_uart_example.html

### This link explains the nrf52 DK button and LED assignment for the UART over BLE
https://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.sdk5.v15.0.0%2Fusbd_ble_uart_example.html

### This is the link to get the nRF52 DK Peripheral UART demo zip file. I prefer to use this one.
https://www.nordicsemi.com/Products/Development-hardware/nRF52-DK/Download#infotabs

### OR you can follow this link to the nRF5 SDK download - you need this to get the example hex file.
The problem with this code is it stops advertising about X seconds and you need to restart by
pushing button one. It can cause you headaches when you don't realize it is asleep. 

Download the sdk and then go to this folder to get the UART hex file to program the nrf52 DK.
At the time of writing this the most recent SDK is 17.1.0 .
/nRF5_SDK_17.1.0_ddde560/examples/ble_peripheral/ble_app_uart/hex/ble_app_uart_pca10040_s112.hex

https://www.nordicsemi.com/Products/Development-software/nrf5-sdk/download
