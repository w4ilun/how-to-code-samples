# Equipment Activity Monitor

## Introduction

This shop-floor equipment activity monitor application is part of a series of how-to Internet of Things (IoT) code sample exercises using Intel® IoT Platforms. This project lets you create a shop-floor equipment activity monitor that:

- tracks equipment usage by monitoring sound and vibration sensors.
- provides a visual notification whenever the equipment is in use.
- logs equipment usage data using cloud-based storage.

## How It Works

This equipment activity monitor checks for sound and vibration.

If both parameters cross a predefined threshold, the display is lit to indicate the equipment is in use.

Once the equipment is no longer being used, the monitor clears the display.

Optionally, data can be stored using one of the many supported cloud service providers.

## Hardware Requirements

- Intel IoT Platform
- One of the supported sensor kits:
    - [Grove\* Starter Kit for Arduino](https://www.seeedstudio.com/Grove-Starter-Kit-for-Arduino-p-1855.html)
        1. [Grove Sound Sensor](http://iotdk.intel.com/docs/master/upm/node/classes/microphone.html)
        2. [Grove Piezo Vibration Sensor](http://iotdk.intel.com/docs/master/upm/node/classes/ldt0028.html)
        3. [Grove RGB LCD](http://iotdk.intel.com/docs/master/upm/node/classes/jhd1313m1.html) 
    - [DFRobot\* Start Kit](https://www.dfrobot.com/product-1200.html)
        1. [Analog Sound Sensor](http://www.dfrobot.com/index.php?route=product/product&product_id=83).
        2. [Digital Vibration Sensor](http://www.dfrobot.com/index.php?route=product/product&product_id=79)
        3. [LCD Keypad Shield](http://iotdk.intel.com/docs/master/upm/node/classes/sainsmartks.html)

### Intel® IoT Gateway setup

You can run this example using an Intel® IoT Gateway connected to an Arduino 101\* (branded Genuino 101\* outside the U.S.).

Make sure your Intel® IoT Gateway is setup properly by following the directions on the web site here:

https://software.intel.com/en-us/getting-started-with-intel-iot-gateways-and-iotdk

The Arduino 101\* (branded Genuino 101\* outside the U.S.) needs to have the Firmata\* firmware installed. If you have IMRAA installed on your gateway, this will be done automatically. Otherwise, install the StandardFirmata or ConfigurableFirmata sketch manually onto your Arduino 101\* (branded Genuino 101\* outside the U.S.).

### Connecting the Grove\* sensors

You need to have the Grove\* Base Shield V2 connected to an Arduino\* compatible breakout board to plug all the Grove devices into the Grove Base Shield V2. Make sure you have the tiny VCC switch on the Grove Base Shield V2 set to **5V**.

1. Plug one end of a Grove cable into the Grove Sound Sensor, and connect the other end to the AO port on the Grove Base Shield V2.<br>
![](./../images/js/equipment-activity.jpg)
2. Plug one end of a Grove cable into the Grove Piezo Vibration Sensor, and connect the other end to the A2 port on the Grove Base Shield V2.
3. Plug one end of a Grove cable into the Grove\* RGB LCD, and connect the other end to any of the I2C ports on the Grove Base Shield V2.

### Connecting the DFRobot\* sensors

![](./../images/js/equipment-activity-dfrobot.jpg)

You need to have a LCD Keypad Shield connected to an Arduino\* compatible breakout board to plug all the DFRobot\* devices into the LCD Keypad Shield.

1. Plug one end of a DFRobot\* cable into Analog Sound Sensor, then connect the other end to the A3 port on the LCD Keypad Shield.

2. Plug one end of a DFRobot\* cable into the Digital Vibration Sensor, then connect the other end to the A2 port on the LCD Keypad Shield.

## Software Prerequisites

1. Intel IoT Platform configured with a supported OS
2. I/O & sensor middleware (MRAA & UPM) installed on target system
3. **Optional** cloud connector middleware instaleld on target system

### IoT cloud setup

You can optionally store the data generated by this sample program using cloud-based IoT platforms from Microsoft Azure\*, IBM Bluemix\*, AT&T M2X\*, AWS\*, Predix\*, or SAP\*.

For information on how to connect to your own cloud server, go to:

[https://github.com/intel-iot-devkit/iot-samples-cloud-setup](https://github.com/intel-iot-devkit/iot-samples-cloud-setup)

### Data store server setup

Optionally, you can store the data generated by this sample program in a back-end database deployed using Microsoft Azure\*, IBM Bluemix\*, or AWS\*, along with Node.js\*, and a Redis\* data store.

For information on how to set up your own cloud data server, go to:

[https://github.com/intel-iot-devkit/intel-iot-examples-datastore](https://github.com/intel-iot-devkit/intel-iot-examples-datastore)

## Tools & IDE Configuration

- [Intel® System Studio (Eclipse IDE for C/C++ and Java\* development)](https://software.intel.com/en-us/node/672439)
    - To run the example in C++, follow these wiki instructions [here](https://github.com/w4ilun/how-to-code-samples/wiki/Intel%C2%AE-System-Studio---IoT-Edition)


- [Follow this guide for NodeJS development](https://www.google.com)


<br><br><br>
IMPORTANT NOTICE: This software is sample software. It is not designed or intended for use in any medical, life-saving or life-sustaining systems, transportation systems, nuclear systems, or for any other mission-critical application in which the failure of the system could lead to critical injury or death. The software may not be fully tested and may contain bugs or errors; it may not be intended or suitable for commercial release. No regulatory approvals for the software have been obtained, and therefore software may not be certified for use in certain countries or environments.