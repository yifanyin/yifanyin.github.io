---
title: "Fault2FMD"
aliases:
- Fault2FMD
tags:
- hazard
- writing
---

Not an intentional copy of [[Fault2SHA]] but hey.

# Motivation
How do we take the available fault and GPS measurement and use some kind of machine to generate a frequency-magnitude distribution that inform the [[notes/probabilistic seismic hazard assessment|PSHA]] model?

To have FMD means to produce earthquake sequences via some kind of physical model. So far the means are 1. [[earthquake simulator|earthquake simulator]] and 2. [[SEAS]] models

Another approach from [[notes/UCERF3|UCERF3]] is figuring out the possible rupture combination. That became [[notes/Chartier2019-SHERIFSOpenSource|SHERIFS]] and [[@Pace2016-wb|FiSH]]

## Alternative opinion
For forecast's sake, we should not focus on reproduce FMD, but instead focus on observing the stress evolution and forecast it.  

# Tech stack
- [[Virtual Quake]]
- [[PyLith]]?

## Method
Insert linear velocity weakening into VQ with the RSQSim approach

# Bibliography
- [[@Sachs2012-mb]]
- [[@Yoder2015-du]]