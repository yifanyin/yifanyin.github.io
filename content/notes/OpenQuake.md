---
title: "OpenQuake"
aliases:
- OQ
- OpenQuake
tags:
- PSHA
- python
---

OpenQuake is a Python package created by the Global Earthquake Model foundation (GEM) for producing [[notes/probabilistic seismic hazard assessment|PSHA]] models. It does not support [[python#Conda|conda]] install however.
- [github repository](https://github.com/gem/oq-engine)
- [Website](https://www.globalquakemodel.org/openquake)

# Before OQ
Gotta prepare the input files that are...
1. The catalog
2. The fault model

# Structures
## Setup on MacOS
- Download source using `git clone` 
- python3 install.py devel
- Activate venv with `source /Users/yifan/openquake/bin/activate` 

## hazardlib
- calc
- geo
- gsim
- mfd
- scalerel
- shakemap
- source
- tests
## risklib
- hmtk
    - Many handy functions in here
    - parsers
    - seismicity
    - strain

