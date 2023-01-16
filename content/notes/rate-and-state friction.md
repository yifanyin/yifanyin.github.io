---
title: "Rate-and-state friction"
created: 2020-05-22
tags: 
- friction
- mechanics
- reference
aliases:
- rsf
- rate-and-state
---

Rate-and-state friction is a friction law born from tribology experiments. 
Established by friction experiments and theory works from [[notes/James H Dieterich|James H. Dieterich]], Andy Ruina

---
# Formulation
Conventional rate-and-state:
$$\mu(V, \theta) = \mu^* + a\ln(\frac{V}{V^*}) + b\ln(\frac{\theta V^*}{D_c})$$

Or add the force
![[@Rubin2005-sf#^Rubin2005-1]]

![[Herrendörfer.JGR.2018#^RRJAM1983]] 
![[Lapusta.JGR.2000#^JmrTrzaHy]]  
And when V << $V_0$ the friction can be negative. ^fejqkAyFK

## The regularized rate and state formulation
From [[Lapusta.JGR.2000]]:
![[Lapusta.JGR.2000#^RRSF]]

![[Herrendörfer.JGR.2018#^3dRox20UC]] 

Evolution laws commonly includes:
1. ![[@Ruina1983-vc#^RuinaAgeLaw]]
   Let $\Omega = \frac{V\theta}{D_c}$. When V=0, state increases. When $\Omega$ = 1, state does not change. [[@Ruina1983-vc]]

2. Slip law: $$\frac{d\theta}{dt} = -\frac{\theta V}{D_c}\ln(\frac{\theta V}{D_c})$$
   Or by using $\Omega$: $\dot\theta = -\Omega\ln\Omega$. No state change when V=0

# Parameters
## A
- direct effect coefficient
- It relate the slip speed with friction.
- $A$ generally has values between 0.005-0.012 [[@Dieterich1994-rd#^jN7GXVW6b]]
## B
- Evolution effect coefficient
- It relate the state of the fault with friction.
## $D_C$, or $L$
- Critical slip distance Dc or L in (Hillers et al., 2006) & [[Hillers.GJI.2007]].
- The characteristic sliding distance for the evolution of $\theta$ to start.
- Typical values obtained in experiments are between 1e-6 - 5e-4 m
![[Hillers.GJI.2007#^rWfTmm1k2]]
  - Dc scales with the dominant wavelength that characterizes the roughness of the sliding surfaces
   - Events are prone to nucleate on points with smaller Dc. However the magnitude is controlled by the local stres
  - For the first try constant Dc is enough
- $\mu^*$, reference steady-state friction coefficient
- $V^*$, Reference steady-state slip velocity
- $\tau$: frictional strength (or shear stress)
- $\sigma$: normal stress
- The ratio of the weakening to healing rate: $$\Omega = \frac{V\theta}{D_c}$$