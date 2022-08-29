---
title: "Python"
tags:
- how-to
---

# Conda
- Remove tarballs, cache, etc: `conda clean -a`

## Managing environment
- create: `conda create --name myenv python=3.6`
- Add new environment to ipython kernel
  `python -m ipykernel install --user --name myenv --display-name "myenv"`
- remove: `conda remove --name myenv --all`

# Related pages
- [[Pandas]]
- [[Making maps in Python|Making maps]]