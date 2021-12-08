---
title: "Self-Steering Boat"
date: 2021-12-04T21:28:04+11:00
draft: false
---

{{< figure src="boat.jpg" alt="" position="center" style="border-radius: 8px;" caption="The dissasembled boat, with 2 prototype control boards which had different compass IC's mounted." captionPosition="right" captionStyle="color: black;" >}}

Group project completed for ENSC3020 Digital Embedded Systems at the University of Western Australia. The challenge was to design a boat which would be placed at one end of a pool and, once powered, drive foward in as straight a line as possible (regardless of disturbances) until it detected the opposite edge of the pool. At this point it must execute a 180 degree turn and then repeat the process, stopping completely once it reached the starting point. It was required that we use an Arduino Nano for control of the boat, with the rest of the design up to us.

I designed and manufactured the carrier board for the Arduino, and wrote all the firmware. The firmware implemented a simple PI controller which stabilised the heading of the boat by independently controlling the speed of the boat's two rear motors. Current heading data was obtained from a compass sensor IC, which communicated with the Arduino over I2C. Obstacle detection was performed by a sonar sensor at the front of the boat.

{{< figure src="realpcb.jpg" alt="" position="center" style="border-radius: 8px;" caption="Closeup of one of the control boards." captionPosition="right" captionStyle="color: black;" >}}
