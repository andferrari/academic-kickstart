---
# Course title, summary, and position.
linktitle: CVX MAUCA
summary: Learn how to use Academic's docs layout for publishing online courses, software documentation, and tutorials.
weight: 3

# Page metadata.
title: Convex optimization  
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
    name: CVX MAUCA
    weight: 1
---

This course is taught to [MAUCA](http://mauca.unice.fr) students.

## Abstract

The course is devoted to  the task of estimating parameters from data contaminated by noises. The objective is to help the students to develop the skills needed to derive a possibly optimal algorithm to solve a given practical estimation problem. 

It will particularly focus on the implementation. For that a large part of the course will be devoted to mathematical optimization which consists of deriving an algorithm to numerically minimize a cost function over a defined domain.

## Theory

In experimental and observational sciences one is always faced with the
problem of drawing conclusions from data contaminated by noises. The
theory of deterministic signal processing is insufficient for tackling
these problems and  we are forced to model and study such data in
probabilistic and statistical fashion.

The most common task in this context is the estimation which consists
of  determining a signal waveform or  some signal aspects from noisy
measurements. The objectives of estimation theory  are: 1. to show how
to derive the best possible algorithm for extracting the information
we seek, 2. to provide the performances of the algorithm.

In astrophysics these problems arise  in all the systems designed to
extract information from measurements, e.g. gravitational waves,
exo-planets, cosmic microwave background, helioseismology... The same
problems arise in a broad range of areas including geophysics,
communication, finance, radar, biomedecine...

This problem can be addressed in a range from theoretical exposition
by statisticians  to the more practical treatment contributed by
experimentalists in different areas.  The course strikes a balance
between these two extremes focusing on the application of state of the
art results to practical problems. 


In this context, mathematical optimization is a central tool for many
practical estimation problems. A large part of the course will be
devoted to help the students to develop the skills needed to
numerically solve  a convex optimization problem. Particular attention
will be paid to optimization with constraints and optimization of
non-differentiable functions  which are both widely used today.

Mathematical optimization arises in many  scientific areas and is an
important enough topic that everyone in physics should know at least 
a little about it.

## Applications

A large part of the course is devoted to practical projects, where the students 
will code various algorithms and compare theoretical results with simulation results.
Students will have to complete three projects during the course and are welcomed to 
work in pairs and to submit a single document. The computations will be 
preferentially carried out in julia or python.  

