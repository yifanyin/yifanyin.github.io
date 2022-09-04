---
title: "Fortran How-to"
aliases:
- Fortran
tags:
- coding
- how-to
---

[Improve your Fortran 77 programs using some Fortran 90 features](http://iprc.soest.hawaii.edu/users/furue/improve-fortran.html) by Ryo Furue

# Arrays
- Referring sections: `array([lower]:[upper][:stride])`
- If no lower or upper is given, the default is the dimension of the array.

# f2py
Interface the fortran module with [[notes/python|Python]]. Numpy use this regularly.