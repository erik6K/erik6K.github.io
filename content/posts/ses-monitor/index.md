---
title: "SES Remote Monitor"
date: 2021-12-04T21:46:17+11:00
draft: false
---

Project completed for the State Emergency Service Communications Unit, during CITS3200 Professional Computing at the University of Western Australia. During this unit, groups of students studying the Computer Science major were placed into university-sourced industry projects involving real clients.

The SES must often respond to large scale bushfire emergencies in very remote locations, which are often radio blackspots. In these sitations, maintaining constant communication is vital, and so the SES Communications Unit (SES CSU) sets up remote radio repeaters to cover such blackspots. The repeaters are powered primarily by a diesel generator, but also have a 12V battery as backup, which is sometimes connected to a solar panel. They are often left unattended for extended periods of time, and have no way of reporting the current status of the generator or the battery's charge level. SES CSU would only become aware of a repeater power faliure when that repeater ceased to function, which was obviously far too late. The project given to us was to design a hardware device which monitored the primary and secondary power sources of the repeater and reported the operational data (generator status and battery voltage) over the internet to be displayed on a webpage.

{{< figure src="both.jpg" alt="" position="center" style="border-radius: 8px;" caption="The remote monitoring hardware (grey) and a prototype antenna with amplifier for sensing the 240Vac (black)." captionPosition="right" captionStyle="color: black;" >}}

<!--The project was multifaceted in the sense that not only was there a need to design the actual embedded system, but the logistics of getting the data to the webpage had to be thought out, and the webpage itself needed to be built and hosted somewhere that presented a good cost-to-benefit ratio for the client. Not to mention the need to create extensive documentation, progress reports, and technical documents.-->

The device which we delivered was based on the Arduino MKR1010 development board, which incorperated a WiFi modem. The analog frontend picks up a very noisy 50Hz 240Vac signal from the generator using an inductive probe, and samples the battery voltage at regular intervals. The AC signal is then processed using FFT analysis in order to detect the 50 Hz component. This data is then packaged into an MQTT message and reported to Microsoft Azure's IoT Hub over the internet, which is accessed via either a cellular or satellite network.

I designed the carrier board for the Arduino MKR1010 and wrote a majority of the firmware. The github repository for the project can be found [here](https://github.com/erik6K/remote-monitor).

{{< figure src="monitor_close.jpg" alt="" position="center" style="border-radius: 8px;" caption="The carrier board and MKR1010 in their enclosure." captionPosition="right" captionStyle="color: black;" >}}