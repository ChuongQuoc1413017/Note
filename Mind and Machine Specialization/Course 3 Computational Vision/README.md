## Computational Vision

### Table of contents
* [1. Vision as a Computational Problem](#1-Vision-as-a-Computational-Problem) 
* [2. Edge Detection & Depth Perception & Object Recognition](#2-Edge-Detection-&-Depth-Perception-&-Object Recognition)
* [3. The Turn Towards Neuroscience](#3-The-Turn-Towards-Neuroscience)
* [4. Heuristics and Biases](#4-Heuristics-and-Biases)


### 1. Vision as a Computational Problem
+ The eye is like a pinhole camera
+ "Solving" the vision problem is mathematically impossible
+ Illusions can tell us something about the computational side of human vision
+ Let's try to make a first (approximate) statement of the "vision problem"

### 2. Edge Detection & Depth Perception & Object Recognition
+ ***Edge detection***
	+ As a first step, we'd like to find the edges in an image (the boundaries of the three-dimensional objects that we hope to identify)
	+ It's hard to identify an object if you can't determine its edges
	+ ***Convolution*** is a signal-processing technique that can be used to identify edges in an image
	+ In machine vision, we convolve the image with a "sombrero function"
	+ Every single pixel in the image is convolved with a sombrero function; "zero crossings" of the resulting image correspond to edges
	+ Convolution can be "tuned" to coarser or finer scales
	+ ***Human vision includes an approximate convolution step as well***
+ ***Depth Perception***
	+ Using two eyes to determine distance
	+ Let's begin with a question: how do you know using just your eyes, how far (from you) an object is?
		+ Size of objects
		+ Movement of objects
	+ Using geometry to determine distance
+ ***Object Recognition***
	+ Identifying objects as collections of "Geons"
	+ What object-recognizing phenomena do geons not explain?

### 3. The Turn Towards Neuroscience

***

<br><br>
<br><br>
_This note was created by [**ChuongQuoc1413017**](https://github.com/ChuongQuoc1413017/Note/tree/main/Mind%20and%20Machine%20Specialization)@2022_
