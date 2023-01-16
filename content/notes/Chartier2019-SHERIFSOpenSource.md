---
title: "Chartier-SRL-2019-SHERIFS"
aliases:
- Chartier2019
- SHERIFS
tags:
- reference
- hazard
- SRL
---

# SHERIFS: Open-Source Code for Computing Earthquake Rates in Fault Systems and Constructing Hazard Models
- Authors:: [[Thomas Chartier]], [[Oona Scotti]], and Hélène Lyon-Caen
- Source:: [[Seismol. Res. Lett.]]
- [Source code](https://github.com/tomchartier/SHERIFS)

## Abstract
- Modeling the seismic potential of active faults and their associated epistemic uncertainties is a fundamental step of [probabilistic seismic hazard assessment](../research/probabilistic seismic hazard assessment.md) (PSHA). Seismic hazard and earthquake rate in fault systems (SHERIFS) is an open‐source python code that builds hazard models including earthquake ruptures involving several fault sections or fault‐to‐fault (FtF) ruptures. It contains user‐friendly tools to calculate the annual rate of FtF ruptures in a fault system based on the slip‐rate estimates and accounting for associated background seismicity.
- SHERIFS applies a forward incremental approach following three rules: 
    - (1) the FtF ruptures allowed in the fault system are defined as input by the user and explored randomly, 
    - (2) the magnitude–frequency distribution of the modeled seismicity in the fault system must follow an imposed shape, and 
    - (3) the slip‐rate budget attributed to each fault section must be preserved in the calculation if the first two rules allow it. 
- Indeed, in some cases, a fraction of the slip‐rate budget must be considered as being spent in non‐mainshock events such as creep or postseismic slip. Background seismicity rates are defined by the hazard modeler as the ratio of seismicity occurring on the modelled faults for different ranges of magnitude.
- Given a coherent set of input hypotheses, SHERIFS allows end users to build the seismic‐hazard fault model thanks to an interactive user‐friendly interface. It aims to help interactions between field data collectors and hazard modelers to explore and weight epistemic uncertainties affecting the input hypotheses. To do so, SHERIFS includes tools to compare modeled earthquake rates with the available local data (earthquake catalog and paleoseismological data). This comparison can be used to weigh different hypotheses explored in a logic tree and discard the hypotheses that are not in agreement with the data. SHERIFS’s outputs are in a format that can be used directly as inputs for PSHA in the OpenQuake engine ([[Pagani.SRL.2014.OpenQuake]]).

 
## Highlights
### Page 01
- Each modeler has a different approach for translating slip rates into earthquake rates on faults which sometimes does not allow a straightforward understanding of the resulting hazard model
- Thus, in most hazard models (e.g., Woessner et al. , 2015 ; Taiwan Earthquake Model [TEM], Wang et al. , 2016 ), small faults are usually grouped into large structures to allow for larger magnitude earthquakes
- background earthquakes are handled using a truncated approach in which earthquakes with a magnitude lower or equal to M w 6.4 occur only in the back- ground zone with a rate defined by the rate in the earthquake catalog, whereas magnitudes higher than M w 6.4 are located on the faults with a rate defined using the average slip rate of the fault
### Page 02
- modeling procedures to allow a large set of possible FtF ruptures to occur in an aleatory fashion in the hazard model while reflecting the individual slip rate of each section
- The Uniform California Earthquake Rupture Forecast version 3 (UCERF3, Field et al. , 2014 ) tackles this issue and allows FtF ruptures to occur in the model by relaxing the segmentation assumption and treating the problem at the faults system level
- In this article, we propose an alternative approach to calculate the earthquake rates in a fault system, which preserves the main philosophy of UCERF3.
- This methodology requires as input data fault section geometries and slip-rate estimates for all the faults of the fault system to calculate the earthquake rupture rates
- The SHERIFS iterative methodology requires first ==establishing possible FtF earthquake rupture scenarios in the fault system and fixing the shape of the target MFD for the entire fault system==.
- At the beginning of the iterative process, the absolute value of the target MFD is not known, only the **shape** is imposed
### Page 03
- Faults with a longer length should be cut in smaller sections (that can rupture together). The sections should be defined as small as necessary to account for local information. For example, a change in slip rate, rake, or dip should be considered for defining the sections.
### Page 04
- In SHERIFS, the MFD for the whole system has been defined to follow a target shape
- SHERIFS workflow includes three tools that should be used sequentially (Fig. 2 ). The first tool sets up and runs the SHERIFS calculation, and the logic tree exploring the episte- mic uncertainties with the help of a graphical interface. The second tool allows visualizing the hazard model and comparing the modeled earthquake rates with available data. After a critical analysis of this comparison, the third tool allows the end- user setting the weights of the logic-tree branches. The final outputs can then be directly used to perform PSHA.
### Page 11
- MATLAB tools to turn fault data into seismic-hazard models

## Notes
- Seismic Hazard and Earthquake Rates In Fault Systems
- Adapt the main philosophy of [[notes/UCERF3|UCERF3]]

### Inputs
- Fault geometry and basic descriptions
- Target [[statistical seismology#Magnitude-frequency distribution|magnitude-frequency distribution]] shape of fault seismicity
    - This is expressed as the **ratio** of magnitudes occurring in the background hypothesis input.

## See also
[[notes/Pace-SRL-2016-FiSH]]
[[Chartier.NHESS.2017]]
[[@Visini2020-dr]]
[[GeoJSON]]

# Alternative models
[[@Visini2020-dr#SUNFiSH|SUNFiSH]] that grew out of [[@Pace2016-wb|FiSH]]. Feels just like UCERF3?


