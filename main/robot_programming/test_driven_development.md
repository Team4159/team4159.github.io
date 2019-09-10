---
title: Test Driven Development
keywords: programming, wpilib
summary: "A way to program"
tags: [programming]
---

Test Driven Development is a software development where you write failing tests that define what you want your code to eventually achieve, and then write the code to fulfill that test.

Though not mutually exclusive from [command-based programming](/main/robot_programming/command_based_programming), TDD lends itself to more abstraction than is traditionally used in command-based programming.

To understand how we can apply these principles to our robot, you should watch the [Control Systems Modelling](https://youtu.be/RLrZzSpHP4E) and [Test Driven Development](https://youtu.be/uGtT8ojgSzg) workshops from 971, in that order.

The general process undergone in these workshops is: first, building a model of the system you want to control using physics, and then second, using that model to simulate that system in code in order to test it.

If you want another look at what this might look like code-wise, you can look at the [`tdd` branch of our 2019 robot code](https://github.com/Team4159/FRC-2019/tree/tdd), where we tried to apply these concepts to our 2019 robot during the off-season.
