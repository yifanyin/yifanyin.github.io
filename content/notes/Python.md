---
title: "Python"
alias:
- Python
tags:
- how-to
- coding
---

# Basic
- Checking the object type: `type(some_object)`
- Mutable and immutable objects
    - [Reference](https://medium.com/@meghamohan/mutable-and-immutable-side-of-python-c2145cf72747)
    - When an object is initiated, it is assigned a unique object id. Its type is defined at runtime and once set can never change, however, its state can be changed if it is mutable. Simply put, a **mutable** object can be changed after it is created, and an **immutable** object can’t. Objects of built-in types like (int, float, bool, str, tuple, Unicode) are immutable. Objects of built-in types like (list, set, dict) are mutable. __Custom classes are generally mutable__. To simulate immutability in a class, one should override attribute setting and deletion to raise exceptions.
        - The objects are immutable, but the objects that serve as "containers" are mutable as the objects they contain can be altered.
- Add path for your own functions
```python
import sys
sys.path.append('path/to/folder')
```
- Check function arguments
```python
import inspect
inspect.getargspec()
```
- [ ] Decorator "@" 
- Pickle

# Conda
## Manage environments
- create: `conda create --name myenv python=3.6`
- Add new environment to ipython kernel
  `python -m ipykernel install --user --name myenv --display-name "myenv"`
- Remove: `conda remove --name myenv --all`
- Remove unwanted tarball, cache, etc. : `conda clean -a`
-   A good sequence to create a new environment
    -   python, numpy, scipy, matplotlib, pandas
    -   geopandas
    -   cartopy

# Parallel computing in Python
- GIL
## Multithreading
- Good for IO-bound operations

## Multiprocessing
- When your problem is CPU-bound

See also [[notes/parallel computing]]

# iPython
## Built-in magic commands
- show the variables and imports in the shell: `%whos`
- Command history. Called using the  line number in prompt: `In [123]: %history -n 4-6`
- Run debugger: `%run -d foobar.py`
- Time the execution of a Python statement or expression: `%time` before the statement

# Spyder
- There is a problem with Qt in MacOS Big Sur. So far the solution is adding this before execute `export QT_MAC_WANTS_LAYER=1`

# Jupyterlab
- Start: `jupyter lab` 
- Interactive [[notes/matplotlib|matplotlib]] plot: `%matplotlib widget` 

# Parallel in Python
## ipython parallel
## Dask
- Bit more friendly for scientific computing


# MOC
- [[notes/numpy|NumPy]]
- [[notes/Pandas|Pandas]]
- [[notes/matplotlib|matplotlib]]
- [[notes/maps with python|Making maps]]
