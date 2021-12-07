---
title: "Self-Driving Boat"
date: 2021-12-04T21:28:04+11:00
draft: false
---

{{< figure src="boat.jpg" alt="" position="center" style="border-radius: 8px;" caption="The dissasembled boat, with 2 prototype control boards which had different compass IC's mounted." captionPosition="right" captionStyle="color: black;" >}}

Group project completed for ENSC3020 Digital Embedded Systems at the University of Western Australia. The task was to design a boat which would be placed at one side of a pool and, at power on, drive foward in as straight a line as possible until it detected an obstacle (opposite edge of the pool), at which point it would execute a 180 degree turn and then drive again in a straight line until it reached its starting position. The control of the boat was to be performed by an Arduino Nano, however the rest of the design was up to us. I designed and manufactured the carrier board for the Arduino, and wrote its firmware. The firmware implemented a simple PI controller which stabilised the heading of the boat by independently controlling the speed of the boat's two motors. Current heading data was obtained from a compass sensor IC, which communicated with the Arduino over I2C, using a premade library which processed the incoming data and returned an absolute bearing.

{{< figure src="realpcb.jpg" alt="" position="center" style="border-radius: 8px;" caption="Closeup of one of the control boards." captionPosition="right" captionStyle="color: black;" >}}
