---
title: "QDYN"
alias: QDYN
tags:
- fortran
- simulation
- fault-mechanics
- research
---

# Metadata
- Ying-di Luo, Jean-Paul Ampuero, Percy Galvez Barron, Martijn P A van den Ende and B. Idini (2017). QDYN: a Quasi-DYNamic earthquake simulator (v1.1) [Data set]. Zenodo. doi:10.5281/zenodo.322459
- [Website](https://ydluo.github.io/qdyn) and [github](https://github.com/ydluo/qdyn)

QDYN is a [[notes/boundary element method|boundary-element]] quasi-dynamic earthquake cycle simulation code written in [[fortran|Fortran]]. 

# Governing equations
The differential equations are assembled from moment balance and [[notes/rate-and-state friction|rate-and-state friction]] law.

# Tech stacks
## Strain and stress
- [[@Okada1992-bn#DC3D|DC3D]]
    Parameters needed:
    - MU: shear modulus (Pa)
    - LAM: Elastic modulus (Pa)
- [H-matrix](https://github.com/ambrad/hmmvp) Green's function compression
