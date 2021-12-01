# Introduction

A polarized object has an analog of a charged object.

For a polarized object with a dipole density per unit volume of $\mathbf{P}$, the electric potential at point $\mathbf{r}$ due to all of the dipoles is

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal V} \frac{ \mathbf{P}\bfcdot\hat{\textbf{\char"0509}}}{\char"0509^2}d\tau'$$

This equation is usually not convenient to work with to compute $V$. [It can be shown](continuous_electric_dipole_distributions.html#appendix) that an alternative form of this equation is

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int_{\mathcal V} \frac{\rho_b}{\char"0509}d\tau'+\oint \frac{\sigma_b}{\char"0509}da'\right)$$

where the closed integral is taken over the closed surface of volume $\mathcal V$ and

$\sigma_b\equiv \mathbf{P}\bfcdot \hat{\mathbf{n}}$ (with $\mathbf{P}$ evaluated on the surface.)

and

$\rho_b\equiv -\boldsymbol{\nabla}\bfcdot\mathbf{P}$. 

We actually did not use this equation for $V$. Instead, we noted that for regular (non--bound) charges on a surface or in a volume, the equation for $V$ is

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int_{\mathcal V} \frac{\rho}{\char"0509}d\tau'+\oint \frac{\sigma}{\char"0509}da'\right)$$

As a result, we can use the same techniques used to find $V$ or $\mathbf{E}$ created by a charge distribution $\sigma$ and/or $\rho$ for problems where we know $\sigma_b$ and $\rho_b$.

In the following example and problems, a polarization vector is given such that $\mathbf{E}$ can be found using Gauss's law.




