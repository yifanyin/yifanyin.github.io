---
title: "Fortran"
aliases:
- Fortran
tags:
- coding
- how-to
---

# Basic
- Fortran is column-major: meaning the first index change the fastest and the values are placed next to each other in the memory
- add `-g -fcheck=all` to get more debugging info if segmentation faults appear.

## Arrays
- Referring sections
```fortran
array([lower]:[upper][:stride])
```
- If no lower or upper is given, the default is the dimension of the array
- Masked array assignments
  ```fortran
WHERE(array-logical-expression)
  array = array-expression
ELSEWHERE
  array = array-expression
```

# f2py
Interface the fortran module with [[notes/python|Python]]. Numpy use this regularly.

# Resources
- [Improve your Fortran 77 programs using some Fortran 90 features](http://iprc.soest.hawaii.edu/users/furue/improve-fortran.html)
- f2py: Interface the Fortran function with [[Python]]. [[notes/numpy|NumPy]] use this regularly.

# Packages
[[notes/QDYN|QDYN]] 
[[notes/Okada.BSSA.1992#DC3D|DC3D]] 