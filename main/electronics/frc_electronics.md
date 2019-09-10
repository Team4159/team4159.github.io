---
title: FRC Electronics
keywords: electronics, frc
summary: "There are several core electrical components that have to be present in every FRC robot to be FRC legal."
tags: [electronics]
---

## 1. Content
The [FRC Control System Hardware Overview](https://wpilib.screenstepslive.com/s/currentCS/m/cs_hardware/l/144968-frc-control-system-hardware-overview) is a quick official guide to learn about FRC electronics. Read this, and the notes below to supplement your knowledge on the different electrical components of every FRC robot.

Here are the slides for our 2019 ["Intro to Electronics" Workshop](https://docs.google.com/presentation/d/1ffs1Fc1p5dTy7iFK4lpKj7pC9f1cEUFPQZVbBLUWARU/edit#slide=id.g5fa3d64124_1_26) for our rookie members.

{% include image.html file="main/frc_electronics/battery.png" caption="Battery" max-width="200" %}
{% include image.html file="main/frc_electronics/breaker.png" caption="Breaker" max-width="200" %}
{% include image.html file="main/frc_electronics/pdp.png" caption="PDP" max-width="200" %}

Starting with the power source, every FRC robot will be primarily powered by a 12V 18 Ah Lead Acid Batery. This will connect to the Power Distribution Panel (PDP) through a 120A circuit breaker. The breaker serves as the main power switch for the robot and to protect your electronics from excessive current draw. The PDP distributes power to all of your electrical components in parallel (Excluding potential custom electronics power sources. See current game manual for more information on its legality).

{% include image.html file="main/frc_electronics/roborio.png" caption="RoboRio" max-width="200" %}
{% include image.html file="main/frc_electronics/jetson.jpg" caption="Jetson TX1" max-width="200" %}

The RoboRio is the robot's main processor. However, it is relatively weak compared to more modern robotic processors in use today. Many teams additionally add a co-processor on their robot to perform more intensive programs such as image recognition, machine learning, calculating trajectories, etc. that would be too slow on the RoboRio. In the 2018 season we worked on the Nvidia Jetson TX1 to run machine learning detecting power cubes. Other co-processors include the Raspberry Pi, Arduino, BeagleBone, and even an Android phone. A challenge with this is that you would have to learn how to program the additional co-processor(s) and how they will communicate with the RoboRio.

{% include image.html file="main/frc_electronics/vrm.png" caption="VRM" max-width="200" %}

The Voltage Regulator Module (VRM) is powered by the PDP and supplies 12V2A power to the OpenMesh Radio. Although this is commonly referred to as the "radio", it's not a RC receiver. The OpenMesh is 1.17 Gbps access point that is used to wirelessly connect to the robot and wirelessly connect to the FMS.

{% include image.html file="main/frc_electronics/pcm.png" caption="PCM" max-width="200" %}

The Pneumatic Control Module only has to be used if you're using pneumatics on your robot. It functions to control and power solenoid valves, but isn't limited to doing so. You can set the PCM to output 12V or 24V, and in the 2018 season utilized this to control and power our LED rings.

{% include image.html file="main/frc_electronics/talonsrx.png" caption="Talon SRX" max-width="200" %}
{% include image.html file="main/frc_electronics/victorspx.png" caption="Victor SPX" max-width="200" %}

Motor controllers are powered by the PDP and power your motors. Every motor on the robot must be controlled by a single motor controller. In the past we have used Victor SP's but they are now discontinued. The two modern motor controllers we use now are the Talon SRX and the Victor SPX. The Talon SRX is the most advanced (but most expensive motor controller on the market that's FRC legal. Other motor controllers in the market that can be used include the Spark, SD540B/C, and Jaguar.

Now that you know about these electrical components, learn how to wire them in the wiring section.

## 2. Custom Electronics (Further Reading)

Being worked on...
