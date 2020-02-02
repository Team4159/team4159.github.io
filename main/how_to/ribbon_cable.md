---
title: Ribbon Cable
keywords: actuators
tags: [electronics, how-to]
---

<b>Purchasing Links</b>:

[CTRE Pre-Made Cable](http://www.ctr-electronics.com/talon-srx-data-cable-4-pack.html)

[CTRE Custom Length Cable](http://www.ctr-electronics.com/talon-srx-data-cable-kit-new-product.html)

[Digi-Key Cable](https://www.digikey.com/product-detail/en/3756%2F10%20100/ME10G-100-ND/3867658) / [Digi-Key Connectors](https://www.digikey.com/product-detail/en/3230-10-0101-00/1175-1645-ND/3883465)

[Breakout Module](http://www.ctr-electronics.com/net-gadgeteer/modules/breakoutmodule.html)

[Breakout Board](http://www.ctr-electronics.com/net-gadgeteer/modules/talon-srx-encoder-breakout-board.html)

<b>Summary</b>:

In FRC, the most commonly used ribbon cable has 10 30-gauge wires and is used in the Talon SRX / Gadgeteer ecosystem.

However, you can [breakout of that ecosystem](#breaking-out) and use Mag Encoders and other Gadgeteer sensors for non-Talon SRX applications as a regular Quadrature Encoder.

## Crimping Ribbon Cables

1. Cut ribbon cable to your desired length.

2. Insert one end of the cable into the grooved slot of the top part of the connector and press the two parts together with a vice. 

3. Repeat with the other end.

{% include image.html file="main/how_to/ribbon_cable_connector.webp" max-width="200" %}

** Insert image of finished ribbon cable **

## Breaking Out

If you want to use a sensor that outputs into ribbon cable without a Talon SRX, you can use a breakout module or board.

See section 1.3 and 5.4.2 of the [Magnetic Encoder User Guide](http://www.ctr-electronics.com/downloads/pdf/Magnetic%20Encoder%20User's%20Guide.pdf) for more information on pinout and breaking out, respectively.

For instance, for the Mag Encoders, you can solder wires onto the corresponding pads on the breakout modules / boards and then plug those into two DIO ports on the RoboRIO. You should end up with 4 wires, one for power, one for ground, and two signal wires for the A and B channels.

You can plug the power, ground, and one of the signal wires into one of the DIO ports and plug in the other signal wire into the signal pin of a second DIO port.

You can use the [Encoder](https://first.wpi.edu/FRC/roborio/release/docs/java/edu/wpi/first/wpilibj/Encoder.html) class to decode those signal data.

** Insert image of soldered breakout module **

** Insert image of plugged in breakout module **
