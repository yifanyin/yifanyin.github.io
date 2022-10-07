---
title: "data assimilation"
tags:
- simulation
- research
- reference
- seed
---

Links:: [[notes/prj-eqsim]]

Calibrate numerical model using the observed values.

# Inspiration
[[Ylona van Dinther|Ylona van Dinther]], Hans R Künsch, Andreas Fichtner, Ensemble data assimilation for earthquake sequences: probabilistic estimation and forecasting of fault stresses, _Geophysical Journal International_, Volume 217, Issue 3, June 2019, Pages 1453–1478, [doi: 10.1093/gji/ggz063](https://doi.org/10.1093/gji/ggz063)

The answer to the future of [[notes/earthquake simulator]]?
Making the time-independent model time-dependent.
The aim: Derive probabilistic estimates for the temporal evolution of unobserved physical variables (state and parameters) and their uncertainties.
How: by combining the information from both observations and a model, along with their errors.
State-space models of the time series
State space : the set of all possible configurations of a system
Point-process model (M. Werner)—> __Boundary element model__ —> continuum model (Ylona)
Ylona’s model is the easiest to implement as it is essentially very similar to weather models
What are the methods available?
Recognize the __observation operator__ H
Phase field model for fault growth?
Simon’s (from GFD) paper on 2-D a/seismic fault growth

# Challenges
- For earthquakes or InSAR, we can only get [[stress drop]] or deformation. There’s little knowledge of the absolute stress underground. How do we get closer to the true value with each update?
- Time steps of an earthquake simulator. Start from a fault, or an imaginary fault system? 