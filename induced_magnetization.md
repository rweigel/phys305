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

%## Problem -- Long Cylinder

%An infinitely long cylinder with an inner radius $a$ and outer radius $b$ has a permeability of $\mu=2\mu_o$. A wire carrying current $I$ runs along its axis. Note that in this problem, $\rho$ is the standard label for the cylindrical radial distance and not a charge density.

%1. Compute and plot $B(\rho)$.  <span style="background-color:yellow">5 points</span>
%2. Compute all bound surface currents, $\mathbf{K}_b$.  <span style="background-color:yellow">5 points</span>
%3. Compute the bound volume current density, $\mathbf{J}_b$.  <span style="background-color:yellow">3 points</span>

%Write all of your answers and label your plot at appropriate points in terms of $\mu_o, I, a,$ and $b$.

%[[Image:cylinder.png|300px]]

%**Answer**

%Assuming $I$ is in the $\hat{\mathbf{z}}$ direction,

%* $\mathbf{H}=\frac{I}{2\pi\rho}\hat{\mathbf{\phi}}$
%* $\mathbf{B} = \frac{\mu_oI}{2\pi\rho}\hat{\mathbf{\phi}}$ for $r<a$
%* $\mathbf{B} = \frac{2\mu_oI}{2\pi\rho}\hat{\mathbf{\phi}}$ for $a<r< b$
%* $\mathbf{B} = \frac{\mu_oI}{2\pi\rho}\hat{\mathbf{\phi}}$ for $r> b$

%$\mathbf{M}=\chi_m\mathbf{H}=(\mu/\mu_o-1)\mathbf{H}=(\mu/\mu_o-1)\frac{I}{2\pi\rho}\hat{\mathbf{\phi}}$

%$\mathbf{K}_b=\mathbf{M}\times \hat{\mathbf{n}}$

%On the inside of the cylinder, $\hat{\mathbf{n}}=-\hat{\mathbf{\rho}}$ and $\mathbf{M}=(\mu/\mu_o-1)\frac{I}{2\pi a}\hat{\mathbf{\phi}}$ so $\mathbf{K}_b = (2\mu_0/\mu_o-1)\frac{I}{2\pi a}\hat{\mathbf{z}}$.

%On the outside of the cylinder, $\hat{\mathbf{n}}=\hat{\mathbf{\rho}}$ and $\mathbf{M}=(\mu/\mu_o-1)\frac{I}{2\pi 2a}\hat{\mathbf{\phi}}$ so $\mathbf{K}_b = -(2\mu_0/\mu_o-1)\frac{I}{2\pi b}\hat{\mathbf{z}}$.

%Note that $\hat{\mathbf{\phi}}\times\hat{\mathbf{\rho}}=-\hat{\mathbf{z}}$.

%Also note that the net-bound current in the vertical direction is zero.

%$\mathbf{J}_b=\nabla\times \mathbf{M}=0$

%because

%$\mathbf{M}=(const)\hat{\mathbf{\phi}}/\rho$

%and the two terms in involving $M_\phi = (const)/\rho$ in

%$$\nabla \times \mathbf{M} = \left({\frac {1}{\rho }}{\frac {\partial M_{z}}{\partial \phi }}-{\frac {\partial M_{\phi }}{\partial z}}\right){\hat {\boldsymbol {\rho }}}+\left({\frac {\partial M_{\rho }}{\partial z}}-{\frac {\partial M_{z}}{\partial \rho }}\right){\hat {\boldsymbol {\phi }}}+{\frac {1}{\rho }}\left({\frac {\partial \left(\rho M_{\phi }\right)}{\partial \rho }}-{\frac {\partial M_{\rho }}{\partial \phi }}\right){\hat {\mathbf {z} }}$$

%evaluate to zero.

%To check your answer, use Ampere's Law $\oint \mathbf{B}\cdot d\mathbf{l}=\mu_o I_{enclosed}$ accounting for these bound currents and verify that you get the same magnetic field computed earlier.