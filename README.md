## Introduction

Leap Motion projects with BB8 version of Sphero, using Bluetooth Low Energy (BLE).

## YouTube

YouTube: 

## Setup

Make sure you have nodejs and npm installed.

Make sure you have the Leap Motion SDK installed: https://developer.leapmotion.com/get-started

This is all using the V2 Desktop (and was developed on OSX Yosemite).

Install cylonjs, a robotics javascript framework. More info here: https://cylonjs.com

Clone the directory: `git clone https://github.com/cwalk/LeapMotion-General/`

Navigate to the directory and do an `npm install` and you should have cylon and cylon-leapmotion.

## Usage

Run the files by using the command `node filename.js`

Each file does something a little different, so feel free to look through the code. This mostly includes ogging what the Leap Motion is receiving. You can change it to look for data in the frames, or down to just the hands and even palm_position.

Feel free to play with the scripts and see what data is given for each gesture, or the difference between hand and frame listeners!
