# An ESP32 8 channels motor controller (shield) | Floor heating controller for proportional actuator
(Can replace Homematic IP Floor Heating Actuator [HmIP-FALMOT-C12] ~210$ + [CCU3] ~150$)

![alt text](https://github.com/nliaudat/esp32_8ch_motor_shield/blob/main/imgs/board.jpg "board")

![alt text](https://github.com/nliaudat/esp32_8ch_motor_shield/blob/main/imgs/floor_heating.jpg "floor_heating")

The ready to go board costs less than 30$

## 2 Goals : 

* Make a floor heating controller
* ESP motor shield
    
## Functionalities : 
* Can control 8 DC motors or 4 steppers motor
* Can drive 8 Homematic valve actuators [HmIP-VDMOT] (~15$ each)
* The card use a ESP32-WROOM-32D as logics and wifi connection. (You can get a 32U if you want an external antenna)
* The software runs under esphome to be easy to customize and linked with https://www.home-assistant.io 
* Can be extended up to 16 channels (I recommend to get 2 boards for better performances, but the shifts registers can be extended up to 4)
* Use BEMF (back electromotive force) from motors to get endstops
* Can be directly linked to external temperature sensors (wifi,BLE, or via available [free pins](https://github.com/nliaudat/esp32_8ch_motor_shield/blob/main/extension.md))
* Wide range of input [power](https://github.com/nliaudat/esp32_8ch_motor_shield/blob/main/power.md) 2.5 to 6V
* Easily [hackable](https://github.com/nliaudat/esp32_8ch_motor_shield/blob/main/hack.md)


## Fabrication : 

* PCB can be ordered with chips assembled at JLPCB for 5.8$/unit.
* The 3.3v power can be HKL-5M03 or HKL-PM03 (under 2.75$)
* ESP32-WROOM-32D costs approx 3.8$
* Box is 3D printed

## New version 1.3 : 
![alt text](https://github.com/nliaudat/esp32_8ch_motor_shield/blob/main/imgs/v1-3.png "1.3")
* Compatible with HKL-5M03 or HKL-PM03
* Compatible with 1000 or 900 mil ESP32 board width

## New version 1.4 : 
![alt text](https://github.com/nliaudat/esp32_8ch_motor_shield/blob/main/imgs/v1-4.png "1.4")
* Input power can be 5V to 12V
* 5V Jumper + 3.3V exposed copper cutout

## New version v53 rev 1.19 : 
![alt text](https://github.com/nliaudat/esp32_8ch_motor_shield/blob/main/imgs/v53.PNG "53")
* Complete rebuild
* All part can be assembled at JLPCB
* Costs rise to 25$ / board (ESP not included, shipping included)
* Fix issue [#5] (https://github.com/nliaudat/esp32_8ch_motor_shield/issues/5)
* Fix HLK-PM03 footprint
* Change L9110s chips (the old one was not available anymore)
* change version number to real job


## New version v54 rev 1.34 : 
* Change 230V input socket with screw
* Fix regression in HLK-PM03 footprint
* Change resistors to 1.07 ohm

## New version with DC input power (4.9-18 V 5A - usb and DC 2.5/6.3 plug): 
![alt text](https://user-images.githubusercontent.com/6782613/189536557-082be6a7-045b-4e5f-b878-b08ebfe7910c.PNG)

## Firmware : 
* Floor heating : https://github.com/nliaudat/floor-heating-controller
* Motor control : https://github.com/nliaudat/esphome-8-ch-motor-controller

## Diy proportionnal valves | smart proportional actuator (TRV) with Esp-C3 mcu
https://github.com/nliaudat/floor-heating-proportional-valve/tree/beta

## Licence: 
* Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC-BY-NC-SA)
* No commercial use
* Actually I did not share the PCB source 
