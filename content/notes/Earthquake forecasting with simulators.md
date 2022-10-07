---
title: "Earthquake forecasting with simulators"
date: "2020"
tags:
- research
- writing
---

# Earthquake forecast and its boundary
- We can not predict an earthquake (i.e. report its time, location and magnitude.) We can only make very coarse forecast not because we do not know the physics, but because the direct measurements of the key physical properties are impossible. Comparing to weather systems, one can measure the temperature, pressure and water content in the atmosphere. One can see the cloud cover and even methane and ozone.  The atmosphere is continuous and can be modeled using continuous PDEs. However, we can not see the stress and strain field underground. The elastic property and fluid content can only be measured using indirect methods.  We don’t even know where all the faults are. We can only know the partial history of seismic events if they leave geological marks or historical accounts.
- The 2014 Working Group on California Earthquake Probabilities (WGCEP 2014) put out perhaps the most comprehensive earthquake model to date. The Uniform California Earthquake Rupture Forecast version 3 ([[notes/UCERF3|UCERF3]]) contains four sub-components but can be split into two: the time-independent models ([[Field2014]]) and the time-dependent models (; [Field et al., 2015](https://pubs.geoscienceworld.org/bssa/article/105/2A/511-543/331850)).
- The time-independent models sum up the geological and geodetic data that describe the fault geometries and slip velocities, and earthquake rate models inverted from the former constraints.
- The (long-term) time-dependent part then gives the probabilities of all possible ruptures based on the PDF of renewal models by taking in the historical and paleo-seismology results.  The results can then be aggregated for specific faults or time period. Although dubbed “time-dependent”, the model has a horizon of decades and is built for risk assessment such as building codes and insurances.
- For the short-term forecasts, WGCEP published the UCERF3-ETAS model ([Field et al., 2017](http://www.bssaonline.org/lookup/doi/10.1785/0120160173)) aiming to have a forecast period from days to decades, aka. Operational earthquake forecasting.  [[notes/ETAS|ETAS]] model treats every event as a seed to trigger more events, thus the name “epidemic”. The distribution of the events generated follows a generalization of Omori-Utsu low of aftershock generation. It is in a way close to the data assimilation concept as the current catalog can serve as the input and swath of forecasts can provide the forecasting probabilities. By combining the UCERF3 with ETAS, it is able to generate synthetic catalogs that obey various constraints posed by the UCERF3-TD model.
- However, the workaround UCERF3-ETAS did in order to make the probabilities resemble elastic rebound triggering will be straight-forward using the physics-based simulator along with some form of stochastic modeling. There are two components that the present physics-based simulators can not cover. First, physics-based models can not achieve is producing background seismicity, or “off-fault seismicity” as defined in UCERF3. ([Robinson et al., 2011](https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1365-246X.2011.05161.x)) attempted to address this by putting small random faults in the half-space to produce off-fault seismicity that subjected to Coulomb stress change. Second, a physics-based simulator provides mainly long-term hazard analysis, mainly because the minimum magnitudes it reaches for regional scale is much larger than the network resolution. Only the return periods of large (M>=7, for example) on-fault earthquakes are used in hazard analysis.

# Can physics-based [[earthquake simulator]] help more?
- Yes, and it should. Until a full 3-D continuum model ([Dal Zilio et al., 2018](https://linkinghub.elsevier.com/retrieve/pii/S0012821X17306210)) become feasible for a crustal fault system, the boundary-element models are the best simulation tool we have for seismicity evolution.  Models are made to predict. But so far, the input for the earthquake simulator only contains boundary conditions.  The time series they produce are only of statistical value. In other words, researchers compress the temporal evolution of the seismicity into distributions of return periods, MFD, etc. and only extract the PDF out of them. But in [[notes/earthquake simulator#Virtual Quake|Virtual Quake]], at least, the seismicity is exact when one fixes the input stress field. If so, can we invert for the initial given the time series?

# Initial value problem of earthquake simulators?
- We need to create an inversion strategy for simulators. But how?
* Given a set of, say all M>5 historical plus paleoseismic plus instrumental, events, there should be a way to invert for the possible stress distribution that fits the data to a certain extent.

# [[data assimilation]], but using what data?
## B-value distribution
* The b values are an integrated phenomenon over space and/or time. It can serve as the initial condition of the simulation and the temporal change that serve as the “observation”
* [[RSQSim|RSQSim]] does show b-value fluctuation following the earthquake sequence. And the time increment should anyway be meaningful.
* Earthquake sequence
    * The happening and not-happening of an event.
    * discrete-event simulation