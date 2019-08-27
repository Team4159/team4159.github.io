---
title: Basic Electrical Theory
keywords: electrical, electronics, basics
tags: [electronics]
---
<!-- Still have General tips, Multimeter and PWM to do -->

## Overview
Electricity, according to [dictionary.com](http://www.dictionary.com/browse/electricity), is the study of electric charges. It powers all electronics. It is a vast field, but for FRC purposes, you really just need to grasps these 3 concepts: *Voltage, Current, Power*



## Current
It is common sense that we know electricity flows. The word "current" is used to describe this flow of electricity. Just like how water flows through a river is water current, the flow of electricity through a wire is electric current.

Formally electric current is defined as the amount of charge traveling through a given cross section in a given amount of time. To make it less wordy, it means the flow of charge. **Remember current is the flow of charge, not electrons**.

{% include image.html
file="/electroBasicTheoryImg/current.gif" alt="electric current" caption = "Here is a conceptual representation of electric current"%}

### What is charge?
Charge is the fundamental quantity of electricity. There are positive charges and negative charges. In an atom, the electrons have negative charge, and the protons have positive charge. By convention, people usually look at the movement of positive charge going through a wire as current. *However, that does not mean current is the movement of protons through the wire*.


Well then, if current is not the movement of protons through a wire, then how does a positive charge move?

We all know that positive attracts negative and vice versa. Therefore, when the robot is connected, the positive terminal of the battery attracts the electrons on the nearby atom, which causes the nearby atom to have a "gap" in its electron cloud, making the entire atom positive temporarily. Then this "positive" atom attracts the electrons in its nearby atom, repeating the process all the way until the end of the wire at the negative terminal of the battery. This creates an impression that some sort of positive charge carrier travels through the wire, but in reality, it is just that positive charged "gap" that is propagating through the wire. Since the gap goes from the positive terminal of the battery to the negative terminal, by convention, electric current flows from the positive end to the negative end.

### Important Notes
- Since current flows only one way, **never mix up the negative and the positive terminal of any electrical component!!!** (Seems silly, but believe me many people will make this dumb mistake)
- Current is expresses in units of *Amperes* or *Amps* or just *A* for short, and the symbol of current is *I*.
- Amperes is Coulombs per second, fitting the definition of current.



## Voltage
It is common sense that water flows from places that are high to places that are low. Places that are high have a high gravitational potential, places that are low have a low gravitational potential. In other words, water flows from where there is high potential to low potential. Same with electricity. However, instead of high gravitational potential, it is high electric potential; instead of low gravitational potential, it is low electric potential. Therefore, electricity flows from where there is high electric potential to low electric potential. Now, since we know current also flows from where it is positive to where it is negative, we can conclude that where it is positive, there will be higher electric potential; where it is negative, there will be lower electric potential.

Now, what is voltage? **Voltage is the electric potential difference of two points** in space, but for our purposes, it is two points on our circuit. *Therefore, voltage is relative* By convention, when people refer to the voltage of a single point, it means the electric potential difference between that point and a point infinitely far away, which again by convention, have the electric potential of 0. In our case, when people refers to a single point on a circuit, they are comparing the electric potential at that point with "ground" or the negative terminal of your battery, which by convention have the electric potential, or voltage of 0.

{% include image.html
file="electroBasicTheoryImg/voltage.png" alt="electric voltage" caption = "Here is a conceptual representation of the relationship between current and voltage"%}

### Important Notes
- Voltage is the potential difference between 2 points.
- Voltage have the units of *Volts* or *V* for short.
- On our robot we use a 12V battery, which means the electric potential difference between the positive and negative terminal of the battery is 12V.



## Power
Power refers to the amount of work outputted in a certain amount of time. In general, we all know that when you work on something, say your homework, you expended some amount of energy for that to happen. Work in electricity mean kind of the same thing. It means the amount of energy the charges used to make something happen, say lighting up a bulb or turning a motor. Power means how fast the energy is being used up.

### Another Look at Voltage
Well then, you might ask where did the charges get the energy in the first place? The answer is voltage. Remember charges flow from the high potential to low potential, at the starting point, where there is a high potential, charges carries a lot of energy, as they go down, they use up their energy to perhaps power up motors or other electrical components. One way to think about this is that the word "potential" in English means the capability to do something, well if you have high "potential", it means you are capable of doing more things, which means you have more energy to do those things than a person that have less "potential" than you. Therefore, the higher the voltage, the more energy a charge there will have.

Following this idea, we can see that voltage can also means the amount of energy a charge has.

With this new idea of voltage in mind, we can see that the more charges are together, the more energy, and so the more of those charges flowing means the higher the power, because the charges are doing more things.

This leads to a very important formula: **P=IV**
where **P** is *Power*, **I** is *Current*, **V** is *Voltage*

### Barbequing Electronic Components
An electronic component gets burnt when there are too much excess energy applied to it. In other words, to much charges are going through it, giving the component their energy to the point where the component can't use all the energy being provided. Then the excess energy becomes heat, barbequing the electronic component. So basically, the charges are overworking the component, and are too powerful for the component to handle.

To preventing that from happening, we can look at P=IV. Limiting both I or V could work, but in our case on our robot, the current usually is easier to limit. We can put a fuse to protect the component or figure out the reason why so much current is going through to the component.

### Important Notes
- Power is given in units called *Watts* or *W* for short, *P* is the symbol for power


## Recap of Basic Concepts
Here is a recap video on the fundamental things about basic electrical concepts: [Recap Video](https://www.youtube.com/watch?v=mvuHsu8S6v8)

Don't worry so much about resistance, it is not that crucial in our case because we don't really get to alter the resistance of anything, but it is a good thing to know.

In short, resistance means how much a electrical component resists the flow of current. Its relationship with voltage and current can be described as the following equation:

**V=IR** *(Ohm's Law)*
where *R* is resistance.

Resistance as described above is represented by *R* and have the units of "Ohm" or the capitalized Greek letter "Omega" for short.

## Other Topics
### Pulse Width Modulation (PWM)
Here is a cool video that explains PWM pretty well: [PWM Video](https://www.youtube.com/watch?v=ISzRh5eN_Pg) *(Sorry about the ads in this video)*

PWM is used by digital devices to "fake" analog signals, because digital devices only have an On or Off state. In order to output a signal that is not as strong as a full on, and not as weak as an off, PWM is used to modulate the signal.

The key for PWM to work is the idea of a duty cycle. In order to achieve the same effect as an analog device, the signal is pulsating at different intervals. Duty cycle in this case means for each cycle of the pulse, how long is the device on? It is usually presented as a percentage of the total time of the entire cycle, or a period. The higher the duty cycle means the stronger the signal because the device is on for longer; the lower the duty cycle is means the weaker the signal because the device is off longer.

Here is a video that explains more in depth of how to calculate the duty cycle: [Duty Cycle Video](https://www.youtube.com/watch?v=4PtepH8CcEE&t=402s)

In our case, PWM is used more for a communication purposes between components in simpler and older robots we built.

### Controller Area Network(CAN Bus)
This is another method of communication between components. Rather than just altering signal send between different components, CAN is a protocol of communication between multiple components, allowing more complex information being transmitted. This method is becoming more and more popular, because more info can be acquired about components using this protocol.

On our recent robots we use CAN, for more details on how to wire it check out [Wiring](/wiring)


## Image sources
- Current, voltage: https://www.physics.uci.edu/~outreach/demos/electricity/foamp.php
