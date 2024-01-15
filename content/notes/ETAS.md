---
title: ETAS
aliases:
  - ETAS
  - epidemic-type aftershock sequence
tags:
  - seismology
  - hazard
  - simulation
  - statistics
---
# Metadata
- Authors: Ogata Yosihiko 尾形良彦
- Links:: [[Statistical seismology]]
- Idea: every earthquake can trigger other earthquake with a rate that decays in time and increase with magnitude.

# Basics
![[@Zhuang2011-pz#Notes]]

[[Question|Question]]: How to control the total energy output by ETAS model? 

# Resources
- SED PhD student [[Leila Mizrahi]] has a python version of the ETAS model on [github](https://github.com/lmizrahi/etas)
- [[Shyam Nandan]]'s papers

# References
- Zhuang, J., D. Harte, M.J. Werner, S. Hainzl, and S. Zhou (2012), Basic models of  seismicity: temporal models, Community Online Resource for Statistical Seismicity  Analysis, doi:10.5078/corssa-79905851. Available at [www.corssa.org](http://www.corssa.org/export/sites/corssa/.galleries/articles-pdf/Zhuang-et-al-2012-CORSSA-Temporal-models.pdf_2063069299.pdf).
- Zhuang, J., M.J. Werner, S. Hainzl, D. Harte, and S. Zhou (2011), Basic models of seismicity: spatiotemporal models, Community Online Resource for Statistical Seismicity Analysis, doi:10.5078/corssa-07487583. Available at [www.corssa.org](http://www.corssa.org/export/sites/corssa/.galleries/articles-pdf/Zhuang-et-al-2011-CORSSA-Spatiotemporal-models.pdf_2063069299.pdf).




--------------------- Portal ---------------------
    - reference
--------------------- Portal ---------------------
    - reference
- $$\lambda(t, x, y, m)=[\nu u(x, y)+ \displaystyle\sum_{i:t_i<t} g(t-t_i)\kappa(m_i)f(r_i)]\beta e^{-\beta(m-m_{min})}$$
- Time law:  [Omori-Utsu law](../research/statistical seismology/Scaling Laws/Omori-Utsu law.md) 
- Magnitude law: $N \sim10^{\alpha m}$ 
--------------------- Portal ---------------------
