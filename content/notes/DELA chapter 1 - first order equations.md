---
tags: math
---

# The basic first-order linear differential equation
<iframe width="560" height="315" src="https://www.youtube.com/embed/0r2L3wTqkBc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

With a source/sink term q(t): $\frac{dy}{dt}=ay+q(t)$, Start from y(0) at t=0

The solution:
$$y(t)=e^{at}y(0)+e^{at}\int_0^t e^{-as}q(s)ds \tag{4}$$

## q(t) is most likely
### Constant source: $q(t)=\mathbf{q}$
### Step function at T
$q(t)=H(t-T)$

<iframe width="560" height="315" src="https://www.youtube.com/embed/ECslmuGlu-U" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Delta function at T
$q(t)=\delta(t-T)$
- $\delta(t)$ is the derivative of $H(t)$
- The integral of $\delta(t)$ is 1
> [!note]
> $e^{at}$ is the growth or decay factor $G(t)$ for all inputs (from $ay$)

### Exponential: $q(t)=e^{ct}$
<iframe width="560" height="315" src="https://www.youtube.com/embed/CB9I4mwpQ5E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Real and Complex Sinusoids
- Real: $\frac{dy}{dt}-ay=A\cos\omega t+B\sin\omega t$
- Complex: $\frac{dy}{dt}-ay=Re^{i\omega t}$

### Real sinusoids
Using only the real number to solve it:
<iframe width="560" height="315" src="https://www.youtube.com/embed/xw3ccgYhFis" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Complex Sinusoid $e^{i\omega t}$
Bringing the exponential back in!

> [!note]
> Euler's formula says $e^{i\theta}=\cos\theta+i\sin\theta$ ^eulersformula

<iframe width="560" height="315" src="https://www.youtube.com/embed/kIT2uMxYh6M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Sinusoids $R\cos(\omega t-\phi)$
Any combination of $\cos\omega t$ and $\sin\omega t$ is a *shifted cosine*. So, the term $A\cos\omega t+B\sin\omega t$ is equal to the real part of $R\cos(\omega t-\phi)$

# Models of growth and decay

> Often the hardest part is to get the right equation. (Definitely harder than the right solution formula.) This section presents both steps of applied mathematics:
> 1. From the **model** to the **equation**
> 2. From the **equation** to the **solution**.
> Our plan is to take the second step (the easier step) first: *solve the equation*. Find the output $y(t)$ from inputs $a(t)$ and $q(t)$ and $y(0)$. Then comes models.

$$\frac{dy}{dt}=a(t)y+q(t)$$, start from $y(0)$ at $t=0$. Now, a(t) is allowed to vary.

Solution $$y(t)=G(0,t)y(0)+\int_0^t G(s,t)q(s)ds$$, with growth factor $G(s,t)$ from time s to time t.

## Particular solution from $q(t)$ with constant rate a

<iframe width="560" height="315" src="https://www.youtube.com/embed/MJUjSKew4nQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Changing growth rate $a(t)$
<iframe width="560" height="315" src="https://www.youtube.com/embed/qJOQOkJ7rI8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

> The whole point of a differential equation is to give a mathematical model of a practical problem

## Newton's law of cooling
$$\frac{dT}{dt}=k(T_\infty-T)$$
# Logistic equation

$$\frac{dy}{dt}=ay-by^2$$
The solution is the logistic equation $$y=\frac{a}{de^{-at}+b}$$
- First non-linear equation!
> Most non-linear equations have no solution formula

- It's symmetric!
- It's autonomous, meaning the change of $y(t)$ only depends on $y$ and not $t$.

<iframe width="560" height="315" src="https://www.youtube.com/embed/TCkLSYxx21c" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Steady states
<iframe width="560" height="315" src="https://www.youtube.com/embed/NmntYoB1uJg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# Next
[[DELA chapter 2 - second order equations]]