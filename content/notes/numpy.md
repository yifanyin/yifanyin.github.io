---
title: "NumPy"
aliases:
- NumPy
tags:
- python
- coding
---

# Resources
- [From Python to NumPy](https://lhoupert.fr/test-jbook/book-jupyterbook.html) by [[notes/Nicolas P Rougier|Nicolas P. Rougier]]

# How-to
## Broadcasting
[NumPy fundamentals](https://numpy.org/doc/stable/user/basics.broadcasting.html)
The term broadcasting describes how NumPy treats arrays with different shapes during arithmetic operations. Subject to certain constraints, the smaller array is “broadcast” across the larger array so that they have compatible shapes. Broadcasting provides a means of vectorizing array operations so that *looping occurs in C instead of Python*.

When operating on two arrays, NumPy compares their shapes element-wise. It starts with the trailing (i.e. *rightmost*) dimensions and works its way left. Two dimensions are compatible when
1.  they are equal, or
2.  one of them is 1
