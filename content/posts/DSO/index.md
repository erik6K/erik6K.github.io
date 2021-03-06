---
title: "Digital Storage Oscilloscope"
date: 2021-12-04T22:07:36+11:00
draft: false
#cover: "bench.jpg"
#useRelativeCover: true
---

Individual design project completed for ELEN90053 Electronic System Design at the University of Melbourne. The project brief was for a 40 MS/s single channel scope with a +/- 5V input range, fixed 64 KB acquisition buffer, DAC controllet trigger level, and a galvanically isolated serial over USB interface for PC data transfer.

The DSO I designed improves upon these specifications by providing a single channel capable of sampling at up to 60 MS/s, a variable-length memory buffer between 2 to 128 KB, software switchable +/- 2.5V, 5V, 12.5V, and 25V input stages with 240Vac protection, and an automatic calibration system.

{{< figure src="bench.jpg" alt="" position="center" style="border-radius: 8px;" caption="DSO on the test bench, sampling a 20 kHz sine wave." captionPosition="right" captionStyle="color: black;" >}}

{{< figure src="dso.jpg" alt="Closeup of DSO" position="center" style="border-radius: 8px;" caption="Closeup of the DSO." captionPosition="right" captionStyle="color: black;" >}}

{{< figure src="pcb.png" alt="" position="center" style="border-radius: 8px;" caption="PCB in Altium Designer." captionPosition="right" captionStyle="color: black;" >}}