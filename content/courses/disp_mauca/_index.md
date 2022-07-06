---
# Course title, summary, and position.
linktitle: DISP MAUCA M1
summary: Learn how to analyze signals and images using numerical tools.
weight: 4

# Page metadata.
title: Digital Image and Signal Processing
date: "2018-09-09T00:00:00Z"
lastmod: "2018-09-09T00:00:00Z"
draft: false  # Is this a draft? true/false
toc: true  # Show table of contents? true/false
type: docs  # Do not modify.

# Add menu entry to sidebar.
# - name: Declare this menu item as a parent with ID `name`.
# - weight: Position of link in menu.
menu:
  example:
    name: DISP MAUCA1
    weight: 4
---

This course is taught to [MAUCA1](http://mauca.unice.fr) students.

## Description

The objective of this course is to present the fundamental mathematics and concepts of discrete-time signal and image processing. 
These topics are presented in the context of signal processing and extended to image processing. 
A large part of the course will be devoted to computer implementation of signal and image processing systems.

![Example image](figure_1.png)


## Content 

1. Discrete-time signals and systems
	- Properties of systems
	- Linear and time invariant (LTI) systems. convolution
	- Linear constant-coefficients difference equations
	- Frequency response of a stable LTI
2. The z-transform and filter design
	- z-transform properties. properties of the roc
	- z-transforms and LTI systems
	- Design of discrete-time iir filters and design of fir filters
3. The discrete fourier transform
	- Representation of periodic sequences: the discrete fourier series 
	- Fourier representation of finite-duration sequences
	- Properties of the dft, linear convolution using the dft
	- Computation of the discrete fourier transform and fft algorithms 
4. Image processing
	- Convolutions in space domain and fourier domain
	- Matrix representation of convolution and properties 
	- Elementary image transforms, edge detection
	- Image filtering
5. Introduction to wavelets
	- Time frequency analysis
	- Continuous and discrete wavelets transform
	- Multi-resolution analysis

![Example image](figure_2.png)

## Practical work

A large part of the course is devoted to 4 practical projects, where the students will code various algorithms and compare theoretical results with simulation results.  
1. Signal filtering
2. Fourier analysis and circular convolution
3. Image processing
4. Wavelets analysis

Students will have to complete these projects during the course and are welcomed to work in pairs and to submit a single document. The computations will be preferentially carried out in julia or python.

## Course textbooks

![Example image](figure_3.png)
![Example image](figure_4.png)
![Example image](figure_5.png)

The course will cover parts of:

> [1] Discrete-Time Signal Processing (3rd Edition) 
> Alan V. Oppenheim, Ronald W. Schafer, and John R. Buck. 
> Prentice-Hall Signal Processing Series

> [2] Digital Image Processing, 4th Edition
> Rafael C. Gonzalez, Richard E. Woods, 
> Pearson 

and

> [3] A Wavelet Tour of Signal Processing: The Sparse Way
> Stéphane Mallat, Academic Press Inc.

- Chapters 1., 2. and 3. of the course:  Chapters 1-6 and 8-9 of [1]
- Chapter 4. of the course: Chapters 3-4 of [2]
- Chapter 5. of the course:  parts of [3]
