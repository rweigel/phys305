# Introduction

For a polarized object with a dipole density per unit volume of $\mathbf{P}$, the electric potential due to all of the dipoles at point $\mathbf{r}$ is

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal V} \frac{ \mathbf{P}\bfcdot\hat{\textbf{\char"0509}}}{\char"0509^2}d\tau'$$

This equation is usually not convenient to work with to compute $V$. It can be shown that an alternative form of this equation is

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int_{\mathcal V} \frac{\rho_b}{\char"0509}d\tau'+\oint \frac{\sigma_b}{\char"0509}da'\right)$$

where the closed integral is taken over the closed surface of volume $\mathcal V$ and

$\sigma_b\equiv \mathbf{P}\bfcdot \hat{\mathbf{n}}$ (with $\mathbf{P}$ evaluated on the surface.)

and

$\rho_b\equiv -\boldsymbol{\nabla}\bfcdot\mathbf{P}$. 

We actually did not use this equation for $V$. Instead, we noted that for regular (non--bound) charges on a surface or in a volume, the equation for $V$ is

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int_{\mathcal V} \frac{\rho}{\char"0509}d\tau'+\oint \frac{\sigma}{\char"0509}da'\right)$$

As a result, we can use the same techniques used to find $V$ or $\mathbf{E}$ created by a charge distribution $\sigma$ and/or $\rho$ for problems where we know $\sigma_b$ and $\rho_b$.

In the following example and problems, a polarization vector is given such that $\mathbf{E}$ can be found using Gauss's law.

## Example -- Thick infinite slab

If $\mathbf{P}=P_o\zhat$ in the region $|z|\lt t$ (a thick slab that is infinite in the $x$--$y$ plane), then on the top surface, $\sigma_b=+P_o$ (because $\hat{\mathbf{n}}=\zhat$) and on the bottom surface, $\sigma_b=-P_o$ (because $\hat{\mathbf{n}}=-\zhat$). The bound volume charge density is $\rho_b= -\boldsymbol{\nabla}\bfcdot\mathbf{P}=0$. 

To find $\mathbf{E}$ due to this polarized slab, we need to find $\mathbf{E}$ created by two infinite sheets of charge with $\sigma=\pm \sigma_b$ at $z=\pm t/2$. This problem has been considered before and the result is $\mathbf{E}=-\sigma/\epsilon_o\zhat$ between the sheets and zero outside. Therefore, $\mathbf{E}=-P_o/\epsilon_o\zhat$ betwen the sheets and $\mathbf{E}=0$ outside. See also [HW #8](hw8.html#slab-of-charge) where a polarized slab was created by superimposing two slabs of charge density $\pm \rho_o$ and then shifting one down by a small distance.

* Is this direction of $\mathbf{E}$ expected for $\mathbf{P}=P_o\zhat$? Base your answer on the fact that $\mathbf{P}$ represents dipoles oriented in the $\zhat$ direction within a small volume.
* The net polarization charge is zero. Is this expected?
* What is the field if two of these slabs are stacked together to form a slab of thickness $2t$?

## Problem -- Long Polarized Solid Cylinder

A long solid cylinder of radius $R$ has a polarization $\mathbf{P}=P_o\hat{\mathbf{s}}$. The cylinder is centered on the origin an aligned with the $z$--axis.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(s)$, which is the electric field due to the bound charge densities found in part 1. of this problem.

%**Answer**

%1. $\sigma_b=P_o$ (at $s=R$). $\rho_b=-P_o/s$.
%2. Gauss's law with these charge densities gives $\mathbf{E}=-(P_o/\epsilon_o)\hat{\mathbf{s}}$ inside and $0$ outside. A common error was to not use integration to find $Q_{encl}$, which is required if $\rho$ is not constant. Using Gauss's law for dielectrics gives the same result and requires less calculation.

## Problem -- Polarized Solid Sphere

A solid sphere of radius $R$ has a polarization $\mathbf{P}=P_o\hat{\mathbf{r}}$. The sphere is centered on the origin.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(s)$, which is the electric field due to the bound charge densities found in part 1. of this problem.

## Problem -- Long Polarized Cylinder with a Cavity

A long cylinder of inner radius $R_i$ and outer radius $R_o$ has a polarization $\mathbf{P}=P_o\hat{\mathbf{s}}$. The cylinder is centered on the origin an aligned with the $z$--axis.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(s)$, which is the electric field due to the bound charge densities found in part 1. of this problem.

## Problem -- Polarized Sphere with a Cavity

A sphere of radius $R_o$ has a spherical cavity of radius $R_i$. The sphere and cavity are centered on the origin. The region $R_i\le r\le R_o$ has a polarization $\mathbf{P}=(P_or^2/R_i^2)\hat{\mathbf{r}}$.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(r)$, which is the electric field due to the bound charge densities found in part 1. of this problem.

%**Answer**

%1. $\sigma_b=-P_o$ at $r=R_i$ and $\sigma_b=P_oR_o^2/R_i^2$ at $r=R_o$. $\rho_b=-4P_o r/R_i^2$.

%2. One can use Gauss's law with the above charge densities to find: $\mathbf{E}=0$ for $r\lt R_i$ and $r\gt R_o$ and $\mathbf{E}=-P_r(r)\hat{\mathbf{r}}/\epsilon_o$, where $P_r(r) = P_o r^2/R_i^2$. It is easier to use Gauss's law for dielectrics. Inside the sphere, there is no free charge, so $\oint\mathbf{D}\bfcdot d\mathbf{A}=0$. From symmetry arguments (what are they?), we can write $\mathbf{D}=D_r(r)\hat{\mathbf{r}}$ and so the integral reduces to $D_r 4\pi r^2=0 \Rightarrow D_r=0$ for all $r\gt 0$.  Using the definition of $\mathbf{D}=\epsilon_o\mathbf{E}+\mathbf{P}$ with $\mathbf{P}=0$ for $0\lt r\lt R_i$ and $r\gt R_o$ gives $\mathbf{E}=0$ in these regions. $E_r=0$ at $r=0$ from a symmetry argument (what is it?). Inside the sphere, $\mathbf{P}$ is non--zero and $D_r=0 \Rightarrow E_r + P_r/\epsilon_0\Rightarrow E_r=-P_r/\epsilon_o$ as before.

## Problem -- Polarized Disk


----