---
title: "matplotlib"
created: 2022-09-20 Tue
aliases: matplotlib
tags:
- python
- coding
DocumentClass: manual
---

# Resources
- [Scientific visualization in matplotlib](https://github.com/rougier/scientific-visualization-book)
- [Effectively using matplotlib](https://pbpython.com/effective-matplotlib.html)
    -   If you take nothing else away from this post, I recommend the following steps for learning how to use matplotlib:
        -   Learn the basic matplotlib terminology, specifically what is a Figure and an Axes.
        -   Always use the object-oriented interface. Get in the habit of using it from the start of your analysis.
        -   Start your visualizations with basic pandas plotting.
        -   Use seaborn for the more complex statistical visualizations.
        -   Use matplotlib to customize the pandas or seaborn visualization.
        -   ![](https://matplotlib.org/_images/anatomy1.png)

# Basic
```python
fig = plt.figure()
ax = fig.add_subplot(nrows, ncols, index)
ax.set_title('An Awesome Plot')
```

## Gridspec
- Basic usage
```python
gs = mpl.gridspec.GridSpec(nrows=2, ncols=2, height_ratios=(2.5, 1), wspace=0.,
    hspace=0.2)
ax = fig.add_subplot(gs[0, 0])
```

## Linestyles
![](https://matplotlib.org/stable/_images/sphx_glr_linestyles_001.png) 

## Annotations
- Using [[Latex]]: `matplotlib.rcParams['text.usetex'] = True`
- And wrap the text with `r"text"`

## Mapping contour
- `contour` and `contourf` use regular grids. `tricontour` and `tricontourf` use irregular grids
- `tripcolor` plot the color filled triangular grid

# Colors

## Color names

![color name](https://matplotlib.org/_images/sphx_glr_named_colors_003.png)

## [Choosing Colormaps in Matplotlib](https://matplotlib.org/stable/tutorials/colors/colormaps.html)

![](https://matplotlib.org/stable/_images/sphx_glr_colormaps_001_2_0x.png)
![](https://matplotlib.org/stable/_images/sphx_glr_colormaps_002_2_0x.png)
![](https://matplotlib.org/stable/_images/sphx_glr_colormaps_004_2_0x.png)

## Create an color transformer
```python
norm = matplotlib.colors.Normalize(vmin=V.min().min(), vmax=V.max().max())
ax.plot_surface(X, Y, Z, facecolors=plt.cm.jet(norm(V)))
```

## matplotlib Discrete Colormap
- The `.mpl_colormap` attribute is a continuous, interpolated map. If you want to make discrete color map you can use matplotlib's ListedColormap:
    - `cmap = ListedColormap(palettable.colorbrewer.qualitative.Dark2_7.mpl_colors)`
- [Controlling the position and size of colorbars with Inset Axes](https://matplotlib.org/stable/gallery/axes_grid1/demo_colorbar_with_inset_locator.html)
## Palettable colormaps
- matplotlib Color Cycle
    - matplotlib follows a default color cycle when drawing a plot. This can be modified as described in this example. To substitute a Palettable palette use the `.mpl_colors` attribute:
    - `ax.set_prop_cycle('color', palettable.colorbrewer.qualitative.Dark2_8.mpl_colors)`
- matplotlib Colormap
     - Many matplotlib functions and methods take a cmap argument. You can use the `.mpl_colormap` attribute with this:
```python
from palettable.colorbrewer.sequential import Blues_8
ax.imshow(data, cmap=Blues_8.mpl_colormap)
```
- Note that the colorbrewer2 color palettes are all available in Matplotlib Palettes already. See the full list of available color maps in matplotlib [here](http://matplotlib.org/examples/color/colormaps_reference.html).
