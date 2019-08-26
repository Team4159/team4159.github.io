---
title: Wiring for FRC
keywords: wiring, electronics
summary: "Wire with good practices to prevent sudden brownouts and comm drops"
tags: [electronics]
---

Read WPILib's wiring guide [here](https://wpilib.screenstepslive.com/s/currentCS/m/cs_hardware/l/144971-wiring-the-frc-control-system), their recommended [best practices](https://wpilib.screenstepslive.com/s/currentCS/m/cs_hardware/l/826661-wiring-best-practices), then take a look at our notes below on our wiring standards.

The most important power lines to pay attention to are Battery to Breaker to PDP, and PDP to VRM to Radio. Ensuring that these connections are intact will prevent your robot from voltage drops and losing communications in a cruicial competition match.

## 0. Wires

Wire size is determined by its diameter and we use American wire gauge (AWG) as the unit. It uses an inverted logarithmic scale so as AWG decreases, wire diameter increases.

(insert awg chart) (insert stranded/solid img)

Wires come in [stranded or solid core](https://learn.sparkfun.com/tutorials/working-with-wire/stranded-vs-solid). When using the Weidmuller connectors, solid core is recommended. However for wires going up an elevator for example stranded wire would be advantageous.

Read [this article](https://blog.muellerelectric.com/types-of-wire-insulation) to learn about 3 different types of wire insulation: PVC, rubber, and silicone.

For lower AWG wires such as the battery, try to use softer (rubber or silicone) wires. We have had problems in the past bending the wires but using softer ones would be much easier to work with.

When buying wire, 

## 1. Battery and Breaker

Mount the battery lying flat, not upright, if at all possible. This will stablize your battery and lower the chances of it losing connection to the main breaker or PDP. You can tighten the power wires to be coming directly out of the battery, or at a 90 degree angle, depending on space restrictions.

Tighten the nut on the main breaker as tight as possible. Then apply electrical tape over it to prevent any metal shavings from shorting it out.

## 2. PDP

