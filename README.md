## Introduction

Leap Motion projects with BB8 version of Sphero, using Bluetooth Low Energy (BLE).

## YouTube

YouTube: https://www.youtube.com/watch?v=EIlxlL9_1YY&list=PLgAD2y-6wgwr6kyU8Qx4wdFeWmvL66oAT&index=1

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

The main file is `leap_sphero.js`. The `test.js` and `color.js` files are just test files in me trying to get BB8 to work through BLE. Feel free to use them as starting points to understand how BB8 works.

## Control

Below is a diagram of how BB8 should move, in relation to your hand being over the Leap Motion.

If your hand is at a vlaue of at least 300 on the Y axis as interpretted by the Leap Motion, BB8 will stop moving, and turn white. BB8 will also stop moving if the Leap Motion can't see your hand at all.

If your hand is below 300 on the Y-axis, then depending on where your hand is in the X and Z axes, you can move BB8 in 8 different directions. You can use your hand like a giant joystick, and see how BB8 follows where your hand is in relation to the Leap Motion. I also make BB8 change a different color for each of the 8 directions, so it's easier to see which direction he is heading. Also it helps for troubleshooting if his heading gets messed up (example: red means straight forward, so if BB8 turns red but starts going right, that means his heading needs to be reset, otherwise he wont exactly follow your hand correctly, everything has been shifted).

![BB8 Control Diagram](/BB8 Control.jpg?raw=true "BB8 Control Diagram")

## Gesture Support

BB8 supports 1 gesture, the circle gesture. If you have your hand above 300 on the Y axis, BB8 will stop moving and turn white. But if you do a circle motion with your finger while above 300, this will activate "Party Mode" on BB8, and make him spin in place and change colors randomly, as long as you continue doing the circle motion. It's quite fun!
