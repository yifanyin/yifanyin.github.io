---
title: "Graeme Weatherill"
aliases:
- Graeme Weatherill
tags:
- scholar
---
# Fault2SHA Learning Series (11) Source models for [[notes/PSHA|PSHA]]
  - [[2022-06-15 Wed]] 

<iframe title="Fault2SHA Learning Series (11) Source models for PSHA" src="https://www.youtube.com/embed/oliQ22qc41Q?feature=oembed" height="113" width="200" allowfullscreen="" allow="fullscreen" style="aspect-ratio: 1.76991 / 1; width: 100%; height: 100%;"></iframe>

## Harmonized catalog
- Each EQ has a uniq and preferred location
- Modified Mercalli intensity (MMI) scale
- Common magnitude unit
    - Magnitudes are a bag of worms
    - Weatherill et al., 2016: Find common events reported as different magnitude scales.
    - Hierachies of agencies for selecting the catalog
    - Multi-objective harmonization
        - Magnitude difference provide info on attenuation, ground motion, etc.
- Estimation of spatiotemporal completeness
    - Expected rate method
## MFD fitting
- Double-truncated GR law $$f_{M_i}(m)=\begin{cases}\beta e^{-\beta(m-m_\text{min})}, m_\text{min}\le m\le m_\text{max} \\1-e^{-\beta(m_\text{max}-m_\text{min})}, \text{otherwise}\end{cases}$$
- where $\beta=b\ln(10)$ 
## Smoothed seismicity model
- Gridded seismic activity ^^rate^^ 
- Fixed-width kernel
- Adaptive kernel like magnitude-dependent and Nth nearest neighbor
- This is what the majority of SHMs need. Faults are extra 🤔
- You can test the kernel using pseudo-perspective test
- Kernels influence the productivity, or the variation in rate, or the [a value](research/statistical seismology/magnitude-frequency distribution/Gutenberg-Richter's Law/a value.md)
- Other parameters of MFD are determined from "superzones"
## Area source models
- Cut by experts. Very subjective.
- Used in [ESHM](research/European Seismic Hazard Model.md)
- Cut using ML algorithms? The objective functions can still be very subjective.
- Can test in CSEP but the short forecasting period bias towards ASM that follows current seismicity distribution
## Active faults
- Check the OpenQuake documentation for fault geometry
- Recurrence models are "moment-balanced"
- Composite source approach (mostly in Europe)
- [UCERF3](research/Uniform California Earthquake Rupture Forecast version 3.md): earthquake rupture forecasts
    - Grand inversion of fault ruptures
## Modeling uncertainties
- [aleatory](research/statistical seismology/Statistical terms/aleatory.md) variability
    - Comes with the uncertainty in measurement
- [epistemic](research/statistical seismology/Statistical terms/epistemic.md) uncertainty
    - Comes from the lack of knowledge about the model
    - Solved using logic tree through various alternative model selections.

- Geodesy help with fault slip rates and tectonic units
- UCERF4 putting more emphasis on [earthquake simulator ](research/earthquake simulator.md) 
