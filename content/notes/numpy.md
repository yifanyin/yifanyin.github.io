---
title: "NumPy"
date: 2020-11-17
aliases:
- NumPy
tags:
- python
- coding
DocumentClass: manual
---

Numpy is the foundation of scientific [[python]]

# Basic
numpy array shape is n-rows * n-columns. For example
```python
a = np.array([[1, 2, 3], [4, 5, 6]])
a.shape
... (2, 3)```

## Views and copies
A subset of NumPy array `Z[:3]` is a view. Using fancy indexing `Z[[1, 2, 3]]` produce a copy.

## Broadcasting
[NumPy fundamentals](https://numpy.org/doc/stable/user/basics.broadcasting.html)
[Python data science handbook](https://jakevdp.github.io/PythonDataScienceHandbook/02.05-computation-on-arrays-broadcasting.html)
The term broadcasting describes how NumPy treats arrays with different shapes during arithmetic operations. Subject to certain constraints, the smaller array is “broadcast” across the larger array so that they have compatible shapes. Broadcasting provides a means of vectorizing array operations so that *looping occurs in C instead of Python*.

When operating on two arrays, NumPy compares their shapes element-wise. It starts with the trailing (i.e. *rightmost*) dimensions and works its way left. Two dimensions are compatible when
1.  they are equal, or
2.  one of them is 1

## Save and load
```python
np.save('numpy_matrix', a)
a = np.load('numpy_matrix.npy')
```

# Resources
- [From Python to NumPy](https://www.labri.fr/perso/nrougier/from-python-to-numpy/) by [[notes/Nicolas P Rougier|Nicolas P. Rougier]]

