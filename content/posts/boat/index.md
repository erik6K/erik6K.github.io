---
title: "Self-Driving Boat"
date: 2021-12-04T21:28:04+11:00
draft: false
---

Group project completed for xxxxxx at the University of Western Australia. I designed and assembled the hardware, and wrote firmware for the Arduino (C++). The firmware implemented a simple PI controller which stabilised the heading of the boat by independently controlling the speed of the boat's two motors. Current heading data was obtained from a compass sensor IC, which communicated with the Arduino over I2C, using a premade library which processed the incoming data and returned an absolute bearing.