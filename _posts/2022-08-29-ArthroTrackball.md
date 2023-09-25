---
title: ArthroTrackball -  A python package to control a spherical treadmill for walking arthropods
layout: post
post-image: "https://massimodeagro.github.io/assets/images/hero.webp"
description: The package will be capable of controlling cameras (for experiment recording), displays (for stimuli presentation), devices (for recording trackball, reward dispenser). These are timed and syncronized.
---

<img style="float: left; max-width:500px;   margin-right: 10px; " src="https://massimodeagro.github.io/assets/images/hero.webp">

For years I have been interested in [jumping spiders vision](https://massimodeagro.github.io/blog/SpiderVision). However, testing these animals had many limitations, with the most prominent being the presentation of artificial stimuli at a known angle, but without impeding the spiders' motion.

The use of spherical treadmill unlocked for me the possibility to [test many hypothesis](https://massimodeagro.github.io/publications)! In such a system, the animal is affixed ad placed onto a frictionless ball. The ball movement are registered and used to derive the intended motion of the animal. Shoutout to the excellent [FicTrac](https://github.com/rjdmoore/fictrac) software, which is what I mostly use to record the sphere rotations.

**However, it is crucial to syncronize the video recording of the sphere together with the stimuli presentation. The control is further complicated by adding other devices, like a second camera or multiple monitors.**

I have developed a python package leveraging multithreading and the internal clock of the computer to simultaneously record and present data, saving everything in a compressed format ready to be analyzed together.

- - -

## Features:
- Recording from usb cameras, with timestamps from every frame as a list

- Displaying of visual stimuli (based on [psychopy](https://www.psychopy.org/))

  - Including pre-programmed stimuli types (looming, translating, appearing)
  - support any number of monitors in any orientation (specified in a cartesian plane)

- Controlling serial devices:

  - Sphere tracker based on optic mice
  - Reward dispenser
  - LED based ring around the sphere

- holistic data logging and compressing into a single files, independently from the number of modules loaded

## Dependencies:
![logo](https://img.shields.io/badge/numpy-required-brightgreen "numpy")
![logo](https://img.shields.io/badge/scipy-required-brightgreen "scipy")
![logo](https://img.shields.io/badge/opencv-cameras-yellow "opencv")
![logo](https://img.shields.io/badge/pyserial-devices-yellow "pyserial")
![logo](https://img.shields.io/badge/psychopy-stimuli-yellow "psychopy")

- - -

## State of development
I plan to publish the first version of package on github by mid 2024. At the current version, the software is functional but lacks documentation. 
