# Introduction

In [Continuous Magnetic Dipole Distributions](continuous_magnetic_dipole_distributions.html), the problem of finding the magnetic field due to an object that had a magnetization $\mathbf{M}$ "frozen in" was considered.

The approach was to find the bound currents that result from this magnetization. Then the magnetic field due to the bound currents was computed.

Consider an object that is unmagnetized ($\mathbf{M}=0$), but is placed in an external magnetic field, $\mathbf{B}_{ext}$. In response to this magnetic field, atomic--sized current loops will tend to align with the external magnetic field. This alignment creates a magnetic field, which called an induced magnetic field.

The total field is then

$\mathbf{B}\_{total}=\mathbf{B}\_{external} + \mathbf{B}_{induced}$

By convention, we drop the "total" subscript and abbreviate "external" as "ext". Given that the induced field is can be computed from bound current densities, we can use $\mathbf{B}\_b$ in place of $\mathbf{B}\_{induced}$ to emphasize this point. In this notation, we have

$\mathbf{B}=\mathbf{B}\_{ext} + \mathbf{B}_{b}$

It is important to note that $\mathbf{B}_b$ depends on $\mathbf{B}$.

Without additional information, it is not possible to compute $\mathbf{B}$ -- we need to know how much $\mathbf{M}$ is generated given $\mathbf{B}$. Once we have $\mathbf{M}$, we can compute the bound currents and then $\mathbf{B}_b$.

## Example -- Infinite Slab

_For more details and a diagram, see the class video from November 23rd._

# Problems

## Long Cylinder

A long solid cylinder of inner radius $R_i$ and outer radius $R_o$ has a magnetic susceptibility of $\chi_m$ and is initially unmagnetized. The cylinder is centered on the origin and aligned with the $z$--axis.

There is an external magnetic field of $\displaystyle\mathbf{B}_{ext}=\frac{\mu_oI_{ext}}{2\pi s}\hat{\boldsymbol{\phi}}$ that is created by a wire that runs along the $z$ axis.

The total field is given by $\mathbf{B}=\mathbf{B}\_{ext} + \mathbf{B}_{b}$, where $\mathbf{B}_b$ is the field due to $\mathbf{K}_b$ and $\mathbf{J}_b$ that are induced by the external magnetic field. 

It can be shown that $\mathbf{B}=(1+\chi_m)\mathbf{B}\_{ext}$ for $R_i\lt s\lt R_o$ and $\mathbf{B}=\mathbf{B}_{ext}$ for $s\lt R_i$ and $s\gt R_o$. That is, inside the cylinder, the material modifies the external field by a factor of $1+\chi_m$ and outside, the field is the same as it would be if the cylinder was not present.

This result was found using the assumption that the induced magnetization was related to the total field $\mathbf{B}$ according to

$$\mathbf{M}=\frac{\chi_m}{\mu_o(1+\chi_m)}\mathbf{B}$$

1. Find $\mathbf{K}\_b$ on the inner and outer curved surfaces of the cylinder in terms of $\mu\_o$, $\chi_m$, <strike>I<sub>ext</sub></strike>, $B_{\phi}$, and $R_o$ or $R_i$
2. Find $\mathbf{J}_b$
3. Show that these bound currents give $\mathbf{B}\_b$ such that $\mathbf{B}\_{ext} + \mathbf{B}_{b}$ matches the equation given form $\mathbf{B}$ for all $s$.

**Answer**

I did not grade this problem.

In the following, it is assumed that $B_s$ and $B_z$ are zero. This means that the induced magnetization has $M_s=0$ and $M_z=0$ due to the relationship between $\mathbf{M}$ and $\mathbf{B}$ given in the problem statement.

The symmetry argument that justifies the assumtion is somewhat subtle. 

Suppose that from your perspective $\mathbf{I}$ is upwards and $B_r$ is outwards. If you hung upsidedown, you see that a downward current also corresponds to an outwards $B_r$. However, accoring to the Biot--Savart law, changing the direction of $\mathbf{I}$ inverts the direction of the field and so upside--down you should see an inwards $B_r$. The only way for consistency is if $B_r$ is zero.

Far from the $z$--axis, the field due to the external and bound currents must approach zero. Ampere's law and the fact that $B_z$ is independent of $z$ can be used to show that $B_z$ is independent of distance from the $z$--axis using a square loop in the $s$--$z$. Together, this implies $B_z=0$. (A similar argument was used to justify $B=0$ outside of a long solenoid in Example 5.9 of Griffiths.)

In the following, I do the problem without assuming that   $\mathbf{B}=(1+\chi_m)\mathbf{B}\_{ext}$. In the original problem statement, I had suggested that you do it this (easier) way, which is why I asked to write the bound currents in terms of $I_{ext}$. However, in class I started to do the problem without using this assumption and is the reason that I changed the problem statement for part 1.

1.

$\mathbf{M}=\chi\mathbf{B}\quad \Rightarrow \quad M_\phi(s)=\chi B_\phi(s)$

$\mathbf{K}_{b\text{ inner}}=\mathbf{M}(R_i)\times\hat{\mathbf{n}}=M_\phi(R_i)\hat{\boldsymbol{\phi}}\times(-\hat{\mathbf{s}})=+M_\phi(R_i)\zhat$

$\mathbf{K}_{b\text{ outer}}=\mathbf{M}(R_o)\times\hat{\mathbf{n}}=M_\phi(R_o)\hat{\boldsymbol{\phi}}\times(+\hat{\mathbf{s}})=-M_\phi(R_o)\zhat$

$\displaystyle\mathbf{B}=\mathbf{B}\_{ext} + \mathbf{B}\_{b} \quad \Rightarrow \quad B\_\phi(s)=B_{\phi\text{ }ext} + B_{\phi b}$

Let $\chi=\chi_m/[(1+\chi_m)\mu_o]$. Using $B_\phi = \chi M_\phi$ gives

$\mathbf{K}_{b\text{ inner}}=+\chi B_\phi(R_i)\zhat$

$\mathbf{K}_{b\text{ outer}}=-\chi B_\phi(R_i)\zhat$

2.

$\displaystyle\mathbf{J}_b=\boldsymbol{\nabla}\times\mathbf{M}=\frac{1}{s}\frac{\partial}{\partial s}(sM_\phi(s))\zhat$

Using $B_\phi = \chi M_\phi$ gives

$\displaystyle\mathbf{J}_b=\frac{\chi}{s}\frac{\partial}{\partial s}(sB_\phi(s))\zhat$

3.

% Note that a symmetry argument is need to conclude non--phi components of B are zero.

Ampere's law for the bound currents gives

$2\pi s B_{\phi b} = \mu_oI_{b\text{ }encl}$

----
$s\lt R_i$

$I_{b\text{ }encl}=0$, so Ampere's law gives $B_{\phi b}=0$ and $\mathbf{B}=\mathbf{B}\_{ext} + \mathbf{B}\_{b}$ gives $\mathbf{B}=\mathbf{B}\_{ext}$.

----

$R_i\lt s\lt R_o$

$I_{b\text{ }encl}$ is due to $\mathbf{K}_{b\text{ inner}}$ and $\mathbf{J}_b$ 

$\displaystyle I_{b\text{ }encl}=2\pi R_iK_{b\text{ inner}} + \int_0^{2\pi}\int_{R_i}^s\frac{\chi}{s'}\frac{\partial}{\partial s'}(s'B_\phi(s'))s'ds'$

$\displaystyle I_{b\text{ }encl}=2\pi \chi R_iB_\phi(R_i)+2\pi\chi\big[sB_\phi(s)-R_iB_\phi(R_i)\big]$

The first and last terms cancel, leaving

$\displaystyle I_{b\text{ }encl}=2\pi\chi sB_\phi(s)$

Substitution of this into $2\pi s B_{\phi b} = \mu_oI_{b\text{ }encl}$ from Ampere's law gives

$B_{\phi b}(s)=\chi B_{\phi}(s)$

Substituion of this into $B\_\phi(s)=B_{\phi\text{ }ext} + B_{\phi b}$

gives

$B\_\phi(s)=B_{\phi\text{ }ext} + \chi B_{\phi}$

and finally

$B_\phi(s)=(1+\chi_m)B_{\phi\text{ }ext}$.

----
For $s\gt R_i$

$I_{b\text{ }encl}$ is the bound current on both surfaces plus the bound current flowing through the volume of the material. It is zero, which follows from

$\displaystyle I_{b\text{ }encl}=2\pi R_iK_{b\text{ inner}} +2\pi R_oK_{b\text{ outer}} + \int_0^{2\pi}\int_{R_i}^{R_o}\frac{\chi}{s'}\frac{\partial}{\partial s'}(s'B_\phi(s'))s'ds'=0$

$I_{b\text{ }encl}=0$, so Ampere's law gives $B_{\phi b}=0$ and $\mathbf{B}=\mathbf{B}\_{ext} + \mathbf{B}\_{b}$ gives $\mathbf{B}=\mathbf{B}\_{ext}$.

----

