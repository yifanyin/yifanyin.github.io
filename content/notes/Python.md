---
title: "Python"
alias:
- Python
tags:
- how-to
- coding
---

# Basic
- Add path
```python
import sys
sys.path.append('path/to/folder')
```

# Conda
- Remove tarballs, cache, etc: `conda clean -a`

## Managing environment
- create: `conda create --name myenv python=3.6`
- Add new environment to ipython kernel
  `python -m ipykernel install --user --name myenv --display-name "myenv"`
- remove: `conda remove --name myenv --all`

# MOC
- [[notes/numpy|NumPy]]
- [[notes/Pandas|Pandas]]
- [[notes/Making maps in Python|Making maps]]