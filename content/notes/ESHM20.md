---
title: "European Seismic Hazard Model 2020"
aliases:
- ESHM20
- ESHM
tags:
- PSHA
- Europe
---

# Metadata
- Authors:: [[notes/Laurentiu Danciu]], [[Shyam Nandan]], Celso Reyes, Roberto Basili, [[Graeme Weatherill]], Celine Beauval, Andrea Rovida, Susana Vilanova, [[Karin Şeşetyan]], Pierre-Yves Bard, Fabrice Cotton, [[Stefan Wiemer]] and [[Dominico Giradini]]
- Links:: [report pdf](<file:///Users/yifan/Research/EMME/References/EFEHR_TR001_ESHM20.pdf>)

# Model components
## Inputs
- Historical catalog (1000-1899)
- Instrumental catalog (1900-2014)
    - [[notes/Question|Question:]] why is the catalog declustered before the $a$ and $b$ calculation?
- Active crustal faults and subduction zones
- Tectonic regionalizations

## Seismogenic source models
- Area source model
    - Fitting the $a$ and $b$ of an area source is a big deal. There are many distributions that one can individually fit. The fitted MFD impact the recurrence rate of large events.
- Active faults and background smoothed seismicity model
    - [Database of individual seismogenic sources](https://diss.ingv.it/diss330/dissmap.html)
    - Background area source and fault source were separated but is combined in 2020.
- Subduction zones
- Non-subducting deep Seismicity Sources

## Ground Motion Models
- A whole different world that I do not trespass.

# Technical stuff
- QGIS
- OpenQuake

