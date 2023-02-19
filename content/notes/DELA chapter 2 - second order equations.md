---
title: "DELA chapter 2 - second order equations"
aliases:
- DELA chapter 2 - second order equations
tags:
- book
- math
---

The first example of $F=ma=-ky$. The force applied is opposite in direction and proportional to the distance y
# Fundamental equation of mechanics
$$m\frac{d^2y}{dt^2}+ky=0$$
<iframe width="560" height="315" src="https://www.youtube.com/embed/xCCeV-glFdM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

We would get an oscillation with frequency $\omega=\sqrt{\frac{k}{m}}$

Second-order equations have two initial conditions y(0) and y'(0). Therefore the complete solution is
$$y(t)=y(0)\cos\omega t+\frac{y'(0)}{\omega}\sin\omega t, w=\sqrt{\frac{k}{m}}$$

It describes an **unforced oscillation**. We can combine the two term to
$$R\cos(\omega t-\alpha)=R\cos\omega t\cos\alpha+R\sin\omega t\sin\alpha$$

## Response functions
The response: $y(t)$ to the forcing function: $f=\cos\omega t$
$$my''+ky=\cos\omega t$$
The natural (null!?) frequency $\omega_n$ is $\sqrt{\frac{k}{m}}$ from the left-hand side, and the forcing $\omega_p$ comes from the right-hand side.

## Impulse response is fundamental solution
The fundamental solution $g(t)$ to a linear differential equation is the impulse response in engineering terms. 
$$mg''+kg=\delta(t)$$ with zero initial conditions.

It is the same as solving $mg''+kg=0$ with initial condition g(0)=0 and g'(0)=1/m (no displacement and finite velocity!)

<iframe width="560" height="315" src="https://www.youtube.com/embed/zkFZY6esNOU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# Review complex numbers
[[notes/complex numbers|complex numbers]]

# 2nd-order equations with constant coefficients
A unforced motion with right-hand side as zero:
$$A\frac{d^2y}{dt^2}+B\frac{dy}{dt}+Cy=0$$ starting from $y(0)$ and $y'(0)$. It can grow, decay or oscillate. Thinking in term of a spring-block system, then A is mass (with acceleration), B is damping (following velocity) and C is stiffness (of the spring).

<iframe width="560" height="315" src="https://www.youtube.com/embed/zqks_JcU0cM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

We use the exponential $y=e^{st}$ and can get the characteristic equation
$$As^2+Bs+C=0$$

The roots $s_1, s_2$ are $$\frac{-B\pm\sqrt{B^2-4AC}}{2A}$$. And the complete solution is any combination of the two exponential.

## Fundamental solution
Special choice of initial condition g(0)=0 and g'(0)=1/A gives the fundamental solution. This is a null solution with a jump start, and a particular solution of $Ag''+Bg'+C=\delta(t)$.

<iframe width="560" height="315" src="https://www.youtube.com/embed/PoHO4PZtW78" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Forced oscillations and exponential response
If there's no forcing term on the right-hand side, the equation is *homogeneous* and controlled by the initial conditions.

When forcing terms exist, we expect a particular solution. And the complete solution $y=y_n+y_p$. What would the best forcing function? $e^{st}$!
$$Ay''+By'+Cy=e^{st}$$
$$y=Ye^{st}=\frac{1}{As^2+Bs+C}e^{st}$$
The fraction Y is the **transfer function**. This is pretty neat because if the input is exponential, then a simple function transfer the input to the output y.

<iframe width="560" height="315" src="https://www.youtube.com/embed/o93axeQJqJ8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Real 2nd-order equations with damping
No resonance this time because all the coefficients are nonzero!
However, often we need the real part of the solution, or $f(t)=\cos\omega t$.

<iframe width="560" height="315" src="https://www.youtube.com/embed/SMQPt7t0bHk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Solutions to 2nd-order equations
**Undetermined coefficients** and **variation of parameters**

<iframe width="560" height="315" src="https://www.youtube.com/embed/mKYlNJhK_2o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
And an example
<iframe width="560" height="315" src="https://www.youtube.com/embed/u_XsCvhzzbg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Then comes the variation of parameters. This method requires you to know the null solutions already. And then the particular solution is just the combination of null solutions.
<iframe width="560" height="315" src="https://www.youtube.com/embed/0f15AVSQ770" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# The Laplace transform
The Laplace transform of $f(t)$ is
$$F(s)=\int^{\infty}_0 f(t)e^{-st}dt$$
Then comes the cool stuff: the Laplace transform of $\frac{dy}{dt}$ is $sY(s)-y(0)$. See the initial condition there?

# See also
[[notes/DELA chapter 1 - first order equations]]
[[notes/DELA chapter 3 - graphical and numerical methods]]
