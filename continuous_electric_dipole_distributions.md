# Introduction

The electric potential due to a "pure" electric dipole centered on the origin is

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\frac{\mathbf{p}\bfcdot\mathbf{\hat{r}}}{r^2}$$

and the electric field is

$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\frac{1}{r^3}\left(3(\mathbf{p}\cdot\hat{\mathbf{r}})\hat{\mathbf{r}}-\mathbf{p}\right)$$

(Griffiths defines a "pure" dipole on page 159; when $r/d\rightarrow \infty$, where $d$ is the separation distance between the charges, the field of the dipole approaches being purely due to the $1/r^2$ term in the expansion of the potential due to the two charges.)

If the dipole is not at the origin, then we need to replace $r$ with $\char"0509$ and $\hat{\mathbf{r}}$ with $\hat{\textbf{\char"0509}}$. Then the electric potential and field at $\mathbf{r}$ due to an electric dipole with its center at $\mathbf{r}'$ is

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\frac{\mathbf{p}\bfcdot\hat{\textbf{\char"0509}}}{\char"0509^2}$$

and the electric field is

$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\frac{1}{\char"0509^3}\left(3(\mathbf{p}\cdot\hat{\textbf{\char"0509}})\hat{\textbf{\char"0509}}-\mathbf{p}\right)$$

If the dipoles can be considered as being continuously distributed, then the differential potential, $dV$, due to a differential dipole, $d\mathbf{p}$ is

$$dV(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\frac{d\mathbf{p}\bfcdot\hat{\textbf{\char"0509}}}{\char"0509^2}$$

If we define an electric dipole density $\mathbf{P}$ according to

$$d\mathbf{p}(\mathbf{r}')=\mathbf{P}(\mathbf{r}')d\tau'$$

then

$$dV(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\frac{\mathbf{P}\bfcdot\hat{\textbf{\char"0509}}}{\char"0509^2}d\tau'$$

and the total potential at a point $\mathbf{r}$ is

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\int\frac{\mathbf{P}\bfcdot\hat{\textbf{\char"0509}}}{\char"0509^2}d\tau'$$

A corresponding equation for $\mathbf{E}$ could also be derived. However, it is usually easier to compute $\mathbf{E}$ by first computing $V$.

## Example -- Computation of $V$ using $\mathbf{P}$

A solid cylinder of radius $R$ and height $h$ is aligned with the $z$-axis, centered on the origin, and has a polarization $\mathbf{P}=P_o\hat{\mathbf{z}}$.

1. Compute the potential on the $z$--axis using $\displaystyle V=\frac{1}{4\pi\epsilon_o}\int\frac{\mathbf{P}\bfcdot\hat{\textbf{\char"0509}}}{\char"0509^2}d\tau'$

2. Show that the result for $V(z)$ is idential to the equation for potential for two disks centerd on $z=\pm h/2$ with $\sigma=\pm P_o$.

**Answer**

1.

$d\tau'=s'ds'd\phi'dz'$

$\mathbf{r}=z\zhat$

$\mathbf{r}'=s'\hat{\mathbf{s}}'+z'\zhat=x'\cos\phi'\xhat + y'\sin\phi'\yhat+ z'\zhat$

Substitution and integration over $\phi'$ gives

$\displaystyle V(z)=\frac{1}{4\pi\epsilon_o}2\pi P_o\int_0^Rs'ds'\int_{-h/2}^{h/2}\frac{z-z'}{\left(s'^2 + (z-z')^2\right)^{3/2}}dz'$

Using

$\displaystyle\frac{d}{dz'}\left(s'^2 + (z-z')^2\right)^{-1/2}=\frac{z-z'}{\left(s'^2 + (z-z')^2\right)^{3/2}}$

Gives

$\displaystyle V(z)=\frac{1}{4\pi\epsilon_o}2\pi P_o\int_0^Rs'ds'\int_{-h/2}^{h/2}\frac{d}{dz}\left(s'^2 + (z-z')^2\right)^{-1/2}dz'$

$\displaystyle \phantom{V(z)} = \frac{1}{4\pi\epsilon_o}2\pi P_o\int_0^Rs'ds'\left[\frac{1}{\left(s'^2 + (z-z')^2\right)^{-1/2}}\right]_{-h/2}^{h/2}$

and

$\displaystyle V(z)=\frac{1}{4\pi\epsilon_o}2\pi P_o\int_0^Rs'ds'\left[\frac{1}{\left(s'^2 + (z-h/2)^2\right)^{-1/2}}-\frac{1}{\left(s'^2 + (z+h/2)^2\right)^{-1/2}}\right]$

2. These two integrals are the same as the integrals one would obtain for computing $V(z)$ for the two disks. In this case, the starting equation would be $V(z)=\int \sigma da'/\char"0509$. For both disks, $da'=s'ds'd\phi'$ and $\mathbf{r}=z\zhat$. For the top/bottom disk, $\mathbf{r}'=s'\hat{\mathbf{s}}'\pm(h/2)\zhat=x'\cos\phi'\xhat + y'\sin\phi'\yhat\pm(h/2)\zhat$ so $\char"0509=\sqrt{s'^2+(z\mp (h/2))^2}$.

# Alternative form of $V$

The equation

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\int\frac{\mathbf{P}\bfcdot\hat{\textbf{\char"0509}}}{\char"0509^2}d\tau'$$

can be written as

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int_{\mathcal V} \frac{\rho_b}{\char"0509}d\tau'+\oint \frac{\sigma_b}{\char"0509}da'\right)$$

where the closed integral is taken over the closed surface of volume $\mathcal V$ and

$\sigma_b\equiv \mathbf{P}\bfcdot \hat{\mathbf{n}}$ (with $\mathbf{P}$ evaluated on the surface.)

and

$\rho_b\equiv -\boldsymbol{\nabla}\bfcdot\mathbf{P}$. 

A partial proof is [given in the Appendix](#Appendix).

Recall that for regular (non--bound) charges on a surface or in a volume, the equation for $V$ is

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int_{\mathcal V} \frac{\rho}{\char"0509}d\tau'+\oint \frac{\sigma}{\char"0509}da'\right)$$

This has the same form as the new equation

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int_{\mathcal V} \frac{\rho_b}{\char"0509}d\tau'+\oint \frac{\sigma_b}{\char"0509}da'\right)$$

The implication is that we can use the same techniques used to find $V$ or $\mathbf{E}$ created by charge densities $\sigma$ and $\rho$ for problems with $\sigma_b$ and $\rho_b$. If we encounter a problem where $\rho_b$ and $\sigma_b$ (1) are on the same surfaces and (2) have the same spatial dependence as $\rho$ and $\sigma$ in a problem solved previously, we can use the previous solution with the replacement of $\rho$ with $\rho_b$ and $\sigma$ with $\sigma_b$.

## Example

A solid cylinder of radius $R$ and height $h$ is aligned with the $z$-axis, centered on the origin, and has a polarization $\mathbf{P}=P_o\hat{\mathbf{z}}$.

1. Compute $\sigma_b$ and $\rho_b$.
2. Compute $\mathbf{E}(z)$

**Answer**

This problem was solved earlier using the formula 

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\int\frac{\mathbf{P}\bfcdot\hat{\textbf{\char"0509}}}{\char"0509^2}d\tau'$$

Here it is solved using the alternative form for $V$ that involves bound charge densities.

$\rho_b=-\boldsymbol{\nabla}\bfcdot\mathbf{P}=0$ can be shown by direct calculation using the divergence formula in either cartesian or cylindrical coordinates. Using $\sigma_b\equiv \mathbf{P}\bfcdot \hat{\mathbf{n}}$, on the top/bottom caps $\hat{\mathbf{n}}=\pm \zhat$ so $\sigma_b=\pm P_o$. On the side surface, $\hat{\mathbf{s}}$, so $\sigma_b=0$. 

To find the electric field, we could compute the potential using 

$$V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\oint \frac{\sigma_b}{\char"0509}da'$$

and then compute $\mathbf{E}=-\boldsymbol{\nabla}V$. Or, we can simply use [the equation for the electric field on the $z$--axis due to a uniformly charged disk](continuous_charge_distributions.html#charge-on-disk)  found previously:

$\displaystyle \mathbf{E} = \frac{\sigma z}{2\epsilon_0} \left(\frac{1}{|z|}-\frac{1}{\sqrt{R^2+z^2}}\right)\hat{\mathbf{z}}$

This equation is for a uniformly charged disk in the $x$--$y$ plane and centered on the origin. The field due to $\sigma_b$ on the top surface is this equation with the replacement of $\sigma$ with $P_o$ and $z$ with $z-h/2$. The field due to $\sigma_b$ on the bottom surface is this equation with the replacement of $\sigma$ with $-P_o$ and $z$ with $z+h/2$. The total field is the sum of these two fields.

# Interpretation of Bound Surface Charges

In 4.2 of Griffiths, he models a polarized sphere by using two uniformly charged spheres with centers that are separated by a small distance $d$. One sphere has a postive charge and the other a negative charge. He then computes the electric field in the overlap region and in the region outside of both spheres where there is no overlap.

In this problem, a polarized slab will be modeled using two slabs of charge with uniform and opposite charge density that are offset by a small distance $d$.

1. Find $\mathbf{E}(y)$ for the slab with uniform charge density $\rho_o$ shown in the following figure. Assume that the slab is infinite in extent in the $\pm z$ and $\pm x$ directions so that Gauss's law can be used. (This slab can be thought of as being composed of thin sheets of charge stacked together and so an alternative to using Gauss's law is to sum the electric field due to sheets of charge.)

   <img src="figures/Gausss_Law_Uniform_Slab.svg"/>

2. Plot $\mathbf{E}(y)$ vs $y$.

3. Next, compute and plot $\mathbf{E}(y)$ for the same slab if it had charge density of $-\rho_o$ and was shifted by $-d$ in the $y$--direction. Assume that $d\ll t$.

4. Compute $\mathbf{E}$ in the region of overlap of the $+\rho_o$ and $-\rho_o$ slabs.

**Answer**

Details on how to solve this problem were given in class and so only a summary is given here.

1\. Gauss's law can be used to find the field for $|y|\ge t/2$ (a cylinder centered on the origin or with its bottom cap at $y=0$ can both be used). This gives $E\_y=\pm \rho_o t/2\epsilon_o$ above/below the slab. Inside the slab, we know $E_y=0$ at $y=0$ because the field due to the upper part of the slab cancels that due to the lower part. We also expect that inside the slab, $E\_y(y)$ field will increase linearly (why?). From this, we can write $E\_y(y)=\rho_o y/\epsilon_o$. This equation gives zero at the origin and matches the outer field at $y=\pm t/2$. Alternatively, we can also use Gauss's law. For a cylinder centered on the origin and height $2y$, the charge enclosed is $\rho_o 2y$.

2\.

3\. Invert the plot from 2. and then translate it by $d$ in the $y$ direction. Inside the negatively charged slab, the field will be $E\_y(y)=-\rho_o (y+d)/\epsilon_o$. (This gives $E_y=0$ when $y=-d$, corresponding to the center of the negatively charged slab.)

4\. In the region of overlap we need to sum

$E\_y(y) = E^+\_y(y) + E^-\_y(y)$

Using $E^+\_y(y)=\rho_o y/\epsilon_o$ and $E^-\_y(y)=-\rho_o (y+d)/\epsilon_o$ gives

$E\_y(y) = -\rho_od/\epsilon_o$

This is the same field one would get if we had a positive sheet of charge at $y=t/2$ and a negative sheet at $y=-t/2$ if the sheets had a charge density of $\rho_o d$. If one draws the charge density when the two slabs are superimposed, the system appears to be two such sheets of charge.

# Problems

## Thick infinite slab

$\mathbf{P}=P_o\zhat$ in the region $|z|\lt t$ on a slab that is infinite in the $x$ and $y$ directions.

1. Find $\sigma_b$ and $\rho_b$
2. Find $\mathbf{E}_b$

**Answer**

On the top surface, $\sigma_b=+P_o$ (because $\hat{\mathbf{n}}=\zhat$) and on the bottom surface, $\sigma_b=-P_o$ (because $\hat{\mathbf{n}}=-\zhat$). The bound volume charge density is $\rho_b= -\boldsymbol{\nabla}\bfcdot\mathbf{P}=0$. 

To find $\mathbf{E}$ due to this polarized slab, we need to find $\mathbf{E}$ created by two infinite sheets of charge that are parallel with to the $x$--$y$ plane. The sheets have $\sigma=\pm \sigma_b$ and are at $z=\pm t/2$. This problem has been considered before and the result is $\mathbf{E}=-\sigma/\epsilon_o\zhat$ between the sheets and zero outside. Therefore, $\mathbf{E}=-P_o/\epsilon_o\zhat$ betwen the sheets and $\mathbf{E}=0$ outside. See also [HW #8](hw8.html#slab-of-charge) where a polarized slab was created by superimposing two slabs of charge density $\pm \rho_o$ and then shifting one down by a small distance.

**Follow--up Questions**

* Is this direction of $\mathbf{E}$ expected for $\mathbf{P}=P_o\zhat$? Base your answer on the fact that $\mathbf{P}$ represents dipoles oriented in the $\zhat$ direction within a small volume.
* The net polarization charge is zero. Is this expected?
* What is the field if two of these slabs are stacked together to form a slab of thickness $2t$?

## Long Polarized Solid Cylinder with $\hat{\mathbf{s}}$ Polarization

A long solid cylinder of radius $R$ has a polarization $\mathbf{P}=P_o\hat{\mathbf{s}}$. The cylinder is centered on the origin an aligned with the $z$--axis.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(s)$ for small $z$, which is the electric field due to the bound charge densities found in part 1. of this problem.

%**Answer**

%1. $\sigma_b=P_o$ (at $s=R$). $\rho_b=-P_o/s$.
%2. Gauss's law with these charge densities gives $\mathbf{E}=-(P_o/\epsilon_o)\hat{\mathbf{s}}$ inside and $0$ outside. A common error was to not use integration to find $Q_{encl}$, which is required if $\rho$ is not constant. Using Gauss's law for dielectrics gives the same result and requires less calculation.

## Finite Cylinder with $\zhat$ Polarization

A solid cylinder of radius $a$ and height $h$ is aligned with the $z$-axis and has a polarization $\mathbf{P}=P_o\hat{\mathbf{z}}$.

1. Find $\sigma_b$ and $\rho_b$.
2. Compute the total bound charge.
3. Sketch the field lines inside and outside of the cylinder when $h<<a$.
4. Sketch the field lines inside and outside of the cylinder when $h>>a$.

%**Answer**
%* Top has $\sigma_b=P_o$, bottom has $\sigma_b=-P_o$, side has $\sigma_b=0$. Interior has $\rho_b=0$. 
%* Total bound charge is zero (as it must be). The equivalent system is two circular disks with an equal and opposite number of charges.
%* When $h<<a$, disks are very close and system field between is like that of to infinite surfaces (straight field lines). Overall, looks like [https://i.stack.imgur.com/YJXXP.gif] up-side down.
%* When $h>>a$, disks are very far and appear as point charges of magnitude $q=\pm\pi a^\sigma_b$. Field likes look like that of a dipole with a very large separation (field line curvature is much less than that of a perfect dipole or [https://www.physicsforums.com/attachments/600px-vfpt_dipole_electric-svg-png.191109/ the typical dipole diagram] that you see).

## Solid Sphere with $\hat{\mathbf{r}}$ Polarization

A solid sphere of radius $R$ has a polarization $\mathbf{P}=P_o\hat{\mathbf{r}}$. The sphere is centered on the origin.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(s)$, which is the electric field due to the bound charge densities found in part 1. of this problem.
3. Sketch the field lines inside and outside of the sphere.

## Solid Sphere with $r^2\hat{\mathbf{r}}$ Polarization

% Copied to notes

A sphere of radius $R_o$ has a spherical cavity of radius $R_i$. The sphere and cavity are centered on the origin. The region $R_i\le r\le R_o$ has a polarization $\mathbf{P}=(P_or^2/R_i^2)\hat{\mathbf{r}}$.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(r)$, which is the electric field due to the bound charge densities found in part 1. of this problem.

**Answer**

1. $\sigma_b=-P_o$ at $r=R_i$ and $\sigma_b=P_oR_o^2/R_i^2$ at $r=R_o$. $\rho_b=-4P_o r/R_i^2$.

    A common error is to write $\sigma_b$ in terms of $r$. Remember that the equation for $\sigma_b$ is evaluated on the surface. In this problem, the surface is at either $r=R_i$ or $r=R_o$.

2. One can use Gauss's law with the above charge densities to find: $\mathbf{E}=0$ for $r\lt R_i$ and $r\gt R_o$ and $\mathbf{E}=-P_r(r)\hat{\mathbf{r}}/\epsilon_o$, where $P_r(r) = P_o r^2/R_i^2$.

   It is easier to use Gauss's law for dielectrics. Inside the sphere, there is no free charge, so $\oint\mathbf{D}\bfcdot d\mathbf{A}=0$. From symmetry arguments (what are they?), we can write $\mathbf{D}=D_r(r)\hat{\mathbf{r}}$ and so the integral reduces to $D_r 4\pi r^2=0 \Rightarrow D_r=0$ for all $r\gt 0$.  Using the definition of $\mathbf{D}=\epsilon_o\mathbf{E}+\mathbf{P}$ with $\mathbf{P}=0$ for $0\lt r\lt R_i$ and $r\gt R_o$ gives $\mathbf{E}=0$ in these regions. $E_r=0$ at $r=0$ from a symmetry argument (what is it?). Inside the sphere, $\mathbf{P}$ is non--zero and $D_r=0 \Rightarrow E_r + P_r/\epsilon_0\Rightarrow E_r=-P_r/\epsilon_o$ as before.

## Solid Sphere with $\hat{\mathbf{z}}$ Polarization

A sphere centered on the origin has a polarization of $\mathbf{P}=P_o\hat{\mathbf{z}}$.

1. Find $\sigma_b$ and $\rho_b$.
2. Compute the total bound charge.
3. Sketch the field lines inside and outside of the sphere.
4. Repeat this problem assuming the sphere has an empty center out to a radius $a_o<a$.

**Answer**

$\hat{\mathbf{n}}=\hat{\mathbf{r}}$, so $\sigma_b=\mathbf{P}\cdot\hat{\mathbf{n}}=P_o\hat{\mathbf{z}}\cdot\hat{\mathbf{r}}$

$\hat{\mathbf{z}}\cdot\hat{\mathbf{r}}=\cos\theta$, which can be obtained from a diagram or by writing $\hat{\mathbf{r}}=\mathbf{r}/r=(x\xhat+y\yhat+z\zhat)/r$ and using $z=r\cos\theta$. Or, one can derive explicit formula for $\hat{\mathbf{z}}$ in spherical using a diagram: $\hat{\mathbf{z}}=\cos\theta\hat{\mathbf{r}}-\sin\theta\hat{\boldsymbol{\theta}}$.

$\sigma_b=P_o\cos\theta$

$\rho_b=-\nabla\cdot\mathbf{P}=0$

Bound charges on sphere are largest at the poles with the top pole being positively charged. Field lines are dipolar outside. Inside then are generally pointing downward (exact result is that they point straight down inside).

Integrating $\sigma_b$ over surface gives net bound charge of zero (as expected).

With hole in center, need to account for a new surface at $r=a_o$, which has $\hat{\mathbf{n}}=-\hat{\mathbf{r}}$.

## Long Polarized Cylinder with a Cavity with $\hat{\mathbf{s}}$

A long cylinder of inner radius $R_i$ and outer radius $R_o$ has a polarization $\mathbf{P}=P_o\hat{\mathbf{s}}$. The cylinder is centered on the origin an aligned with the $z$--axis.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(s)$ for small $z$, which is the electric field due to the bound charge densities found in part 1. of this problem. 

## Sphere with a Cavity and $\hat{\mathbf{r}}$ Polarization

A sphere of radius $R_o$ has a spherical cavity of radius $R_i$. The sphere and cavity are centered on the origin. The region $R_i\le r\le R_o$ has a polarization $\mathbf{P}=(P_or^2/R_i^2)\hat{\mathbf{r}}$.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(r)$, which is the electric field due to the bound charge densities found in part 1. of this problem.

%**Answer**

%1. $\sigma_b=-P_o$ at $r=R_i$ and $\sigma_b=P_oR_o^2/R_i^2$ at $r=R_o$. $\rho_b=-4P_o r/R_i^2$.

%2. One can use Gauss's law with the above charge densities to find: $\mathbf{E}=0$ for $r\lt R_i$ and $r\gt R_o$ and $\mathbf{E}=-P_r(r)\hat{\mathbf{r}}/\epsilon_o$, where $P_r(r) = P_o r^2/R_i^2$. It is easier to use Gauss's law for dielectrics. Inside the sphere, there is no free charge, so $\oint\mathbf{D}\bfcdot d\mathbf{A}=0$. From symmetry arguments (what are they?), we can write $\mathbf{D}=D_r(r)\hat{\mathbf{r}}$ and so the integral reduces to $D_r 4\pi r^2=0 \Rightarrow D_r=0$ for all $r\gt 0$.  Using the definition of $\mathbf{D}=\epsilon_o\mathbf{E}+\mathbf{P}$ with $\mathbf{P}=0$ for $0\lt r\lt R_i$ and $r\gt R_o$ gives $\mathbf{E}=0$ in these regions. $E_r=0$ at $r=0$ from a symmetry argument (what is it?). Inside the sphere, $\mathbf{P}$ is non--zero and $D_r=0 \Rightarrow E_r + P_r/\epsilon_0\Rightarrow E_r=-P_r/\epsilon_o$ as before.

## Gauss's Law and Potential Differences

The following figure shows a cross section of three spherical objects.

* For the charged solid sphere within $r\le R$, $\rho=(Q/\pi R^4)r$
* The net charge on the conducting shell is $-Q$. This shell has an inner radius of $2R$ and an outer radius of $3R$.
* The ("frozen in") polarization of the polarized outer shell is $\displaystyle\mathbf{P}=\frac{P_o}{4\pi}\frac{R^2}{r^2}\hat{\mathbf{r}}$. This shell has an inner radius of $4R$ and an outer radius of $5R$.

1. Find $E_r(r)$
2. Find the potential difference between the charged solid sphere and the inner surface of the conductor (that is, find $V(2R)-V(R)$).

<img src="figures/Gauss_Law_Compound.svg" width="80%"/>

%**Answer**

%1. For $r\le R$, $Q_{encl}=Qr^4/R^4$, so $E_r(r)=kQr^2/R^4$
%
%   For $R\le r\lt 2R$, $Q_{encl}=Q$, so $E_r(r)=kQ/r^2$
%
%   For $2R\le r\lt 3R$, $E_r(r)=0$
%   
%   For $3R\le r\lt 4R$, $Q_{encl}=0$, so $E_r(r)=0$
%
%   For $r \gt 4R$, the field due to the charges on the conductor and solid sphere is zero.
%
%   At $r=4R$, $\sigma_{bi}=-P_o/(4\pi (4R)^2)$, so $Q_{bi}=\sigma_{bi} 4\pi (4R)^2 = -P_o R^2$
%
%   $\rho_b=0$ inside polarized object.
%   
%   Inside the polarized object, $E_{b\text{ }r}(r)=kQ_{b\text{ }encl}/r^2 = kQ_{bi}/r^2 = -kP_oR^2/r^2$
%   
%   At $r=5R$, $\sigma_b=P_o/(4\pi (5R)^2)$ so $Q_{bo} = P_oR^2$.
%
%   Outside the polarized object, $Q_{b\text{ }encl}=Q_{bi}+Q_{bo}=0$, so $E_{b\text{ }r}(r)=0$.
%   
%   The total field for $r\gt 4R$ is the field due to the bound charges and the field due to the other charges. The field due to the other charges is zero, so the field is only due to the bound charges.
%   
%   For $4R\lt r\lt 5R$, $E_r(r)=-kP_oR^2/r^2$
%   
%   For $r\gt 5R$, $E_r(r)=0$   
%   
%2. $V(2R)-V(R)=-\int_{R}^{2R}E_r(r)dr=-kQ/2R$. Could also use point charge formula $V=kQ/r$ because field is equivalent to that of a point charge $Q$ at the origin, so $V(2R)-V(R)=kQ\left(1/2R-1/R\right)=-kQ/2R$.

## Cube with $\zhat$ Polarization

A cube with side length $2a$ and centered on the origin has a polarization $\mathbf{P}=P_o\hat{\mathbf{z}}$.

Find the bound charge densities.

## Cube with $\hat{\mathbf{r}}$ Polarization

A cube with side length $2a$ and centered on the origin has a polarization $\mathbf{P}=P_o\mathbf{r}$.

Find the bound charge densities.

## Polarized Sheet

A square of side $w$ lies in the $x$--$y$ plane, is centered on the origin, and has sides parallel to the coordinate axes.

The square has a polarization of $P_o\xhat$.

Find the electric field.

% See hand-written notes for how to handle this. Here $\sigma_b$ and $\rho_b$ are zero.

## Polarized Disk

A disk of radius $R$ lies in the $x$--$y$ plane, is centered on the origin, and has a polarization $\mathbf{P}=P_o\hat{\mathbf{s}}$

Find the electric field.

# Appendix -- Partial Proof of Alternative form of $V$

Consider a point far enough away that dipole term dominates.

Assume a dipole volume density of

$$\mathbf{P}(\mathbf{x}') = \frac{\langle\mathbf{p}(\mathbf{x}')\rangle}{\Delta v'}$$

where $\langle\mathbf{p}(\mathbf{x}')\rangle$ is the average dipole moment in the small volume $\Delta v'$

For a single "perfect" (or "pure" or "ideal") dipole at the origin

$$\Phi_{p_O}(\mathbf{x}) = \frac{1}{4\pi\epsilon_o}\frac{\mathbf{p}\cdot\mathbf{x}}{r^3}$$

For a "perfect" dipole at $\mathbf{x}'$, make the replacements $r\equiv|\mathbf{x}| \rightarrow |\mathbf{x}-\mathbf{x}'|$ and $\mathbf{x} \rightarrow \mathbf{x}-\mathbf{x}'$

$$\Phi_{p'}(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\frac{\mathbf{p}(\mathbf{x}')\cdot(\mathbf{x}-\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|^3}$$

Using $\mathbf{P}(\mathbf{x}') = \langle\mathbf{p}(\mathbf{x}')\rangle/\Delta v'$, the potential at $\mathbf{x}$ due to the differential volume $\mathcal{\Delta v'}$

$$\Phi_{\Delta v'}(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\frac{\mathbf{P}(\mathbf{x}')\cdot(\mathbf{x}-\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|^3}\Delta v'$$

where $\mathbf{x}'$ now means the location of the differential volume $\Delta v'$. For $\Delta v'\rightarrow 0$, $\Delta v'\rightarrow d^3x'$; summing over all $\Delta v'$ in $\mathcal{V}$ gives

$$\Phi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}\frac{\mathbf{P}(\mathbf{x}')\cdot(\mathbf{x}-\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|^3}d^3x'$$

Using

$$\boldsymbol{\nabla}'\left(\frac{1}{|\mathbf{x}-\mathbf{x}'|}\right)=\frac{\mathbf{x}-\mathbf{x}'}{|\mathbf{x}-\mathbf{x}'|^3}$$

this can be written as

$$\Phi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}\mathbf{P}(\mathbf{x}')\cdot\boldsymbol{\nabla}'\left(\frac{1}{|\mathbf{x}-\mathbf{x}'|}\right)d^3x'$$

It is important to remember that we assumed $\mathbf{x}$ was outside of the volume of integration $\mathcal{V}$ and that the dipoles are perfect. It can be shown that this same equation applies to points inside the volume and when the dipoles are not perfect (See Zangwell or Griffiths; Jackson also addresses in Chapter 4.1, but does not mention in derivation similar to the above that appears in Chapter 4.3).

Integration by parts (or the identity $\boldsymbol{\nabla}\cdot (f\mathbf{F})=\mathbf{F}\cdot\boldsymbol{\nabla} f+f\boldsymbol{\nabla}\cdot\mathbf{F}$)

$$\Phi(\mathbf{x})=\int_{\mathcal{V}} \boldsymbol{\nabla}'\cdot \left(\frac{\mathbf{P}(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}\right)d^3x'+\int_{\mathcal{V}} \frac{-\boldsymbol{\nabla}'\cdot \mathbf{P}(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}d^3x'$$

The first term can be rewritten using the divergence theorem

$$\Phi(\mathbf{x})=\oint_{\mathcal{S}} \frac{\mathbf{P}(\mathbf{x}')\cdot \mathbf{\hat{n}}\,}{|\mathbf{x}-\mathbf{x}'|}da'+\int_{\mathcal{V}} \frac{-\boldsymbol{\nabla}'\cdot \mathbf{P}(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}d^3x'$$

Compare this equation with the equation for the potential due to a charge density $\rho$ and surface charge density $\sigma$

$$\Phi(\mathbf{x})=\oint_{\mathcal{S}} \frac{\sigma(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}da'+\int_{\mathcal{V}} \frac{\rho(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}d^3x'$$

from which it followed that

$$\boldsymbol{\nabla}\cdot\mathbf{E}=\frac{\rho}{\epsilon_o}$$

If we define "bound" densities $\sigma_b\equiv \mathbf{P}\cdot\hat{\mathbf{n}}$ and $\rho_b\equiv -\boldsymbol{\nabla}\cdot\mathbf{P}$

$$\Phi_b(\mathbf{x})=\oint_{\mathcal{S}} \frac{\sigma_b(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}da+\int_{\mathcal{V}} \frac{\rho_b(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}d^3x'$$

In addition, one can compute the electric field, $\mathbf{E}_b$, due to the bound charge density using $\mathbf{E}_b=\boldsymbol{\nabla}\Phi$.

At this point, we have essentially considered a system of two types of charges: single charges, represented by $\rho_f$ and pure dipoles, represented by $\rho_b$. There is a class of problems one can solve where you are given a fixed (or "frozen-in") $\mathbf{P}$ and are asked to find $\Phi$. In this case, one simply computes $\sigma_b$ and $\rho_b$ and integrates to find $\Phi$. Quite often, one does not even need to do an integration - if we know the potential for an ordinary charge distribution $\sigma$ (or $\rho$) and we find $\sigma_b$ (or $\rho$) has the same distribution, we only need to replace $\sigma$ (or $\rho$) with the value of $\sigma_b$ (or $\rho_b$) in terms of $\mathbf{P}$. 

See the description for [[#Magnetized_Objects]] for a way of thinking about how an object gets polarized. The main difference is that an electric field causes the random dipoles to become aligned anti-parallel to an external electric field. If the object is somehow "frozen" so the non-random dipoles can't randomize after the external field is turned off, you get a polarized object. Most materials are such that the induced polarization electric field tends to oppose the external electric field (dielectrics). In contrast to magnetizable objects which can enhance (paramagnets) or oppose (diamagnets) the external magnetic field.

The mnemonic I mention in class for the prefix is that "di" or "dia" means the object wants to "die" (kill) the external field. (From a language perspective, dielectrics should be called diaelectrics since dia in Greek is "oppose", but Faraday decided it did not look right and so used "di". If you happened to know the prefix "di" means double in Greek, you would be a bit upset about this decision; perhaps he should have used "un-di-electrics" ...).
