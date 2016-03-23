## Introduction

Leap Motion projects with BB8 version of Sphero, using Bluetooth Low Energy (BLE).

## YouTube

YouTube:

## Code Setup

Make sure you have nodejs and npm installed.

Make sure you have the Leap Motion SDK installed: https://developer.leapmotion.com/get-started

This is all using the V2 Desktop (and was developed on OSX Yosemite).

Install cylonjs, a robotics javascript framework. More info here: https://cylonjs.com

For more info on Leap Motion, check out: http://cylonjs.com/documentation/drivers/leapmotion/

For more info on Sphero-BLE, check out: http://cylonjs.com/documentation/platforms/sphero-ble/

Clone the directory: `git clone https://github.com/cwalk/LeapMotion-BB8-Sphero`

Navigate to the directory and do an `npm install` and you should have cylon, cylon-ble, cylon-sphero-ble, and cylon-leapmotion.

## BB8 Setup

This code will only work with the BB-8 version of Sphero. It uses Bluetooth Low Energy (BLE) to communicate, as opposed to the Sphero that uses Bluetooth classic. I have not yet tested this on the Sphero Ollie, but for that, you should check out: http://cylonjs.com/documentation/drivers/ollie/ and see what the differences are, if any.

BB8 comes with it's own mobile app, that allows you to instantly connect and drive BB8 with your phone, as long as you have Bluetooth on. This is important to know because you need to set the **heading** of BB8 correctly, as the code in this repo is all based off a specific heading. 

You can set the heading in the mobile app, as the blinking blue light. I set it directly behind BB8. So if BB8's head is facing away from me, and the back of his head is facing me, the blue light should also be facing me. This allows me to move BB8 with the Leap Motion, in relation to where my hand is. If it ever looks like BB8 is going the wrong way, you might need to stop the script, and reopen the mobile app to reset his heading.

## Usage

Run the files by using the command `node filename.js`




## Control
