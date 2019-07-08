---
title: Machine Learning
keywords: programming, java
sidebar: main_sidebar
permalink: main_ml.html
folder: main
tags: [control-systems]
---

Edmond Lee, one of our volunteer mentors, did a [lecture](https://docs.google.com/presentation/d/1FlCyOCPtCTY9GKsJKqa1DWfxdVA4FjvDrSX9ASkOZWM/edit#slide=id.p) during the 2017 offseason on machine learning theory, SSD Caffe, and applying it to identifying FRC game objects.

When Edmond joined the team, he took on the task of researching possibilites to improve the team's autonomous programming. He had a bit of experience with machine learning which lead him to look into SSD (Single Shot Detection) algorithms for object detection, primarily a Caffe fork. Before the 2018 build season started, he worked on two repos:
* [The team's SSD Caffe fork, with customized instructions and scripts](https://github.com/Team4159/caffe)
* [Image dataset for Steamworks and Power Up](https://github.com/Team4159/caffe-data)

# Performance and Working with the Jetson TX1
Object detection based on Neural Networks is among the most applicable techniques for FRC, but also among the most resource intense. SSD is a relatively fast algorithm but embedded environments still pose performance barriers. Edmond used a NVIDIA GeForce GTX 1060 to train models and test image detection. Initially he found the inference (identifying objects) time to be about 57 milliseconds when using SSD, and closer to 30 when using smaller images and models. With a Jetson TX1 however the same tests were much slower by a factor of 6 to 8, in other words we can only expect while performing object detection a rate of 3 to 5 FPS, which is similar to other reports of SSD users.

While we were not able to utilize object detection during competition, we made some notable findings on increasing performance:
* Use GPU, not CPU acceleration. OpenCV can performance CPU inference only, but Caffe may do it with the GPU which is 8-10 times as fast.
* Shrinking the neural network can have a linear effect of performance gain, and a bigger effect on training time and memory consumption while preserving accuracy.
* The Jetson's software comes with TensorRT, a runtime that can greatly boost performance on top of other optimzations. However integrating it with SSD is not trivial at all, and we should plan on using out of the box solutions like [DetectNet](https://github.com/dusty-nv/jetson-inference/#locating-object-coordinates-using-detectnet) instead.

# Recommended Links:
* [The Incomplete Guide to Using the TX1 for FRC by the Zebracorns (Team 900)](https://docs.google.com/document/d/13AoeIFF3kKoX3-IzGBw2naoREyNXJA3SDAEPcFOD_VM/edit)
* [Detecting Power Cubes with TensorRT (with DetectNet)](https://www.youtube.com/watch?v=EOpnBV8SsVU)
