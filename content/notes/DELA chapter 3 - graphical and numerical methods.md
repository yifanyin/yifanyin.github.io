---
title: "DELA chapter 3 - graphical and numerical methods"
aliases:
- DELA chapter 3 - graphical and numerical methods
tags:
- 
---

# Nonlinear equations
$$\frac{dy}{dt}=f(t, y)$$
No more easy formula to solve the equation. We only know the slope of y at (t, y).

<iframe width="560" height="315" src="https://www.youtube.com/embed/cDfWtSqGiBY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# Phase planes

# Linearization near the critical points

# Numerical methods
## Euler's method
$$y_n=y_{n-1}+\Delta t f(y_{n-1})$$
And the *local* error of one step
$$y(t+\Delta t)=y(t)+\Delta ty'(t)+\frac{1}{2}(\Delta t)^2y''(t)+...$$
is just the Taylor expansion starting from the third term. So, the error is of the order $(\Delta t)^2$. When we take $n$ steps with local error $C(\Delta t)^2$, the *global* error is $C(n\Delta t)\Delta t=CT\Delta t$.

> [!note]
> Euler's method is first-order accurate, meaning it's porpotional to $\Delta t$

## Stiff equations and implicit methods
When the decay of two terms are vastly different, we are forced to do more work; otherwise the solution will not be stable.
Solution: Backward differencing instead of the forward differencing we see before. 
$$\frac{y^B_{n+1}-y_n}{\Delta t}=f_{n+1}=f(t_{n+1}, y^B_{n+1})$$