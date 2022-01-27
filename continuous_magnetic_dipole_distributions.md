# Introduction

The vector potential due to a "perfect" magnetic dipole centered on the origin is

$$\mathbf{A}(\mathbf{r})=\frac{\mu_o}{4\pi}\frac{\mathbf{m}\times \mathbf{\hat{r}}}{r^2}$$

and the magnetic field is

$$\mathbf{B}(\mathbf{r})=\frac{\mu_0}{4\pi}\frac{1}{r^3}\left(3(\mathbf{m}\cdot\hat{\mathbf{r}})\hat{\mathbf{r}}-\mathbf{m}\right)$$

If the dipole is not at the origin, then we need to replace $r$ with $\char"0509$ and $\hat{\mathbf{r}}$ with $\hat{\textbf{\char"0509}}$. Then the vector potential and magnetic field at $\mathbf{r}$ due to a magnetic dipole with its center at $\mathbf{r}'$ is

$$\mathbf{A}(\mathbf{r})=\frac{\mu_o}{4\pi}\frac{\mathbf{m}\times \hat{\textbf{\char"0509}}}{\char"0509^2}$$

and

$$\mathbf{B}(\mathbf{r})=\frac{\mu_0}{4\pi}\frac{1}{\char"0509^3}\left(3(\mathbf{m}\cdot\hat{\textbf{\char"0509}})\hat{\textbf{\char"0509}}-\mathbf{m}\right)$$

Recall that when dealing with Coulomb's law

$$
\mathbf{E}=\frac{q}{4\pi\epsilon_o}\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}
$$

we [replaced $q$ with $dq$](continuous_charge_distributions.html) so that we have a differential electric field due to do a differential charge

$$
d\mathbf{E}=\frac{dq(\mathbf{r}')}{4\pi\epsilon_o}  \frac{\hat{\textbf{\char"0509}}}{\char"0509^2}
$$

We next made the assumption that a point charge was continuously distributed over a small volume. In this case $dq(\mathbf{r}')=\rho(\mathbf{r}') d\tau'$. The functional dependence of $dq$ on $\mathbf{r}'$ was been added because the amount of charge in a given small volume may depend on the location of the small volume. Substitution of $dq(\mathbf{r}')=\rho(\mathbf{r}') d\tau'$ and integration gives

$$
\mathbf{E} = \frac{1}{4\pi\epsilon_o}\int \rho(\mathbf{r}')
\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}d\tau'
$$

Here we will follow a similar procedure. If we replace $\mathbf{m}$ with $d\mathbf{m}(\mathbf{r}')$, then

$$d\mathbf{A}(\mathbf{r})=\frac{\mu_o}{4\pi}\frac{d\mathbf{m}(\mathbf{r}')\times \hat{\textbf{\char"0509}}}{\char"0509^2}$$

If we define a magnetic dipole density $\mathbf{M}$ according to

$$d\mathbf{m}(\mathbf{r}')=\mathbf{M}(\mathbf{r}')d\tau'$$

Then

$$\mathbf{A}(\mathbf{r})=\frac{\mu_o}{4\pi}\int\frac{\mathbf{M}(\mathbf{r}')\times \hat{\textbf{\char"0509}}}{\char"0509^2}d\tau'$$

This equation is usually not convenient to work with to compute $\mathbf{A}$. It can be shown (see 6.2 of Griffiths) that an alternative form of this equation is

$$\displaystyle \mathbf{A}(\mathbf{r})=\frac{\mu_o}{4\pi}\left( \int_\mathcal{V} \frac{\mathbf{J}_b(\mathbf{r}')}{\char"0509}d\tau'+\oint \frac{\mathbf{K}_b(\mathbf{r}')}{\char"0509}da'\right)$$

where the second integral is taken over the bounding surface of volume $\mathcal V$ and

$\mathbf{K}_b\equiv \mathbf{M}\times \hat{\mathbf{n}}$ (with $\mathbf{M}$ evaluated on the surface.)

and

$\mathbf{J}_b\equiv \boldsymbol{\nabla}\times\mathbf{M}$.

We actually will not use this equation for $\mathbf{A}$. Instead, we note that for regular (non--bound) currents on a surface and within a volume, [the equation for $\mathbf{A}$](vector_potential.html) is

$$\displaystyle \mathbf{A}(\mathbf{r})=\frac{\mu_o}{4\pi}\left(\int \frac{\mathbf{J}(\mathbf{r}')}{\char"0509}d\tau' + \int \frac{\mathbf{K}(\mathbf{r}')}{\char"0509}da'\right)$$

As a result, we can use the same techniques used to find $\mathbf{A}$ or $\mathbf{B}$ created by a regular (non--bound) surface current distribution $\mathbf{K}$ and/or a volume current distribution $\mathbf{J}$ for problems where we know $\mathbf{K}_b$ and $\mathbf{J}_b$.

> In summary, to find the $\mathbf{A}$ and $\mathbf{B}$ due to $\mathbf{M}$, compute $\mathbf{K}_b$ and $\mathbf{J}_b$. If these bound currents are the same as those in a problem involving $\mathbf{K}$ and/or $\mathbf{J}$, one can use that solution's $\mathbf{A}$ and $\mathbf{B}$ with the replacement of $\mathbf{K}$ with $\mathbf{K}_b$ and $\mathbf{J}$ with $\mathbf{J}_b$.

## Example -- Thick infinite slab

_For more details and a diagram, see the class video from November 23rd._

If $\mathbf{M}=M_o\xhat$ in the region $|z|\lt t$ (a thick slab that is infinite in the $x$--$y$ plane and centered on the origin), then on the top surface,

$\mathbf{K}_b=\mathbf{M}\times \hat{\mathbf{n}}=M_o\xhat\times \zhat=-M_o\yhat$

On the bottom surface,

$\mathbf{K}_b=\mathbf{M}\times \hat{\mathbf{n}}=M_o\xhat\times (-\zhat)=+M_o\yhat$

As discussed in class, there is a $\mathbf{K}_b$ on two other surfaces, but they are far enough away from the origin that they will create a field that is small in comparison to the top and bottom surfaces.

The bound volume current density is $\mathbf{J}_b= \boldsymbol{\nabla}\times\mathbf{M}=0$. Note that if $\mathbf{M}$ has componenents that are constant _in cartesian coordinates_, we can conclude $\boldsymbol{\nabla}\times\mathbf{M}=0$. This is only true in general for $\mathbf{M}$ in cartesian coordinates. In the following example, $\mathbf{M}$ has components in cylindrical components that are constants. However, $\boldsymbol{\nabla}\times\mathbf{M}\ne 0$.

The equivalent system is an infinite sheet of current at $z=t/2$ with a current of density $K_b=M_o$ flowing in the $-\yhat$ direction and an infinite sheet of current at $z=-t/2$ with a current of density $K_b=M_o$ flowing in the $+\yhat$ direction.

In [HW 11.1](hw11.html), the magnetic field due to the same current configuration was found, but instead of a current density of $M_o$, the current density was $K_o$. So we can take the solution for $\mathbf{B}$ from that problem and replace $K_o$ with $M_o$.

Is this direction of $\mathbf{B}$ expected for $\mathbf{M}=M_o\xhat$? Base your answer on the fact that $\mathbf{M}$ represents dipoles oriented in the $\xhat$ direction within a small volume.

## Example -- Long Magnetized Solid Cylinder

A long cylinder of radius $R$ has a magnetization of $\mathbf{M}=M_o\hat{\boldsymbol{\phi}}$. The cylinder is centered on the origin and aligned with the $z$--axis.

1. Find the bound currents
2. Find $\mathbf{B}(s)$ 

**Partial Answer**

----

$\mathbf{K}_b=\mathbf{M}\times\hat{\mathbf{n}}$

Top: $\hat{\mathbf{n}}=+\zhat$, so $\mathbf{K}_b=\mathbf{M}\times\hat{\mathbf{n}}=(M_o\hat{\boldsymbol{\phi}})\times\zhat=-\hat{\mathbf{s}}$. This corresponds to current flowing inwards on the top cap of the cylinder towards its center (draw this).

Side $\hat{\mathbf{n}}=\hat{\mathbf{s}}$, so $\mathbf{K}_b=\mathbf{M}\times\hat{\mathbf{n}}=(M_o\hat{\boldsymbol{\phi}})\times\hat{\mathbf{s}}=-\zhat$. This corresponds to a current flowing downward on the side of the cylinder (draw this).

If the cylinder is long, then in the $x$--$y$ plane, the field due to the bound currents on the caps of the cylinder will be small. As a result, to find the field due to $\mathbf{K}_b$, we need to find the field due to the surface current on the side of the cylinder. From Ampere's law and a diagram, you should be able to show that the field due to $\mathbf{K}_b$ is

$\mathbf{B}\_{K\_{b}} = 0$ for $s\lt R$

$\displaystyle\mathbf{B}\_{K\_{b}} = -\frac{\mu_oM_oR}{s}\hat{\boldsymbol{\phi}}$ for $s\ge R$.

----

$\displaystyle\mathbf{J}_b=\boldsymbol{\nabla}\times\mathbf{M}=\frac{M_o}{s}\zhat$.

This corresponds to current flowing within the cylinder upwards.

From Ampere's law and a diagram, you should be able to show that the field due to $\mathbf{J}_b$ is 

$\mathbf{B}\_{J\_{b}}=\mu_oM_o\hat{\boldsymbol{\phi}}$ for $s\le R$

$\displaystyle\mathbf{B}\_{J\_{b}}=\frac{\mu_oM_oR}{s}\hat{\boldsymbol{\phi}}$ for $s\ge R$.

----

The total magnetic field is that due to $\mathbf{K}_b$ and $\mathbf{J}_b$.

$\mathbf{B}=\mu_oM_o\hat{\boldsymbol{\phi}}$ for $s\le R$

$\mathbf{B}=0$ for $s\ge R$

# Problems

## $\mathbf{B}$ Due to a Long Magnetized Solid Cylinder I.

A long solid cylinder of radius $R$ has a magnetization $\mathbf{M}=M_o\zhat$. The cylinder is centered on the origin and aligned with the $z$--axis.

1. Find the bound currents $\mathbf{K}_b$ and $\mathbf{J}_b$.
2. Find $\mathbf{B}_b(s)$, which is the magnetic field due to the bound current densities found in part 1. of this problem.

**Answer**

1. $\mathbf{K}_b=M_o\hat{\boldsymbol{\phi}}$ on the curved surface, $\mathbf{K_b}=0$ on the top/bottom caps, and $\mathbf{J}_b=0$. 

2. The bound currents are equivalent to the current on a long solenoid, for which the current flows azimuthally around a cylinder. The magnetic field for a long solenoid of length $L$ is $\mathbf{B}=0$ outside and $B=\mu_o NI/L$ inside. The direction of this field is given by the right--hand rule. $N$ is the number of times the wire is wrapped around the cylinder. $N I/L$ corresponds to a surface current $K$, so the field inside can be written as $B=\mu_oK$. Replacing $K$ with $M_o$ and using the right--hand rule to conclude the direction of $\mathbf{B}_b$ is $+\zhat$ (which is the same direction as $\mathbf{M}$, as expected),  

   $\mathbf{B}_b=\mu_oM_o\zhat=\mu_o\mathbf{M}$ for $s\lt R$
   
   $\mathbf{B}_b=0$ for $s\gt R$.


## $\mathbf{B}$ Due to a Long Magnetized Solid Cylinder II.

A long cylinder of radius $R$ has a magnetization of $\mathbf{M}=(M_os/R)\hat{\boldsymbol{\phi}}$. The cylinder is centered on the origin and aligned with the $z$--axis.

1. Find the bound currents $\mathbf{K}_b$ and $\mathbf{J}_b$.
2. Find $\mathbf{B}_b(s)$, which is the magnetic field due to the bound current densities found in part 1. of this problem.

**Answer**

If the cylinder is long, their contribution to $\mathbf{B}_b$ from the top and bottom caps can be neglected.

1. $\mathbf{K}_b=-M_o\zhat$ on side and $\mathbf{K}_b=\pm M_os/R$ on top/bottom cap. $\mathbf{J}_b=(2M_o/R)\zhat$.
2. $B_{b\phi}=\mu_oM_os/R$ from Ampere's law with an Amperian loop centered on the origin and in the $x$--$y$ plane. $B_s=B_z=0$ follows from thinking of the bound currents as being created my many closly spaced infinitely long wires and cancellation symmetry. Thus, $\mathbf{B}_b=(\mu_oM_os/R)\hat{\boldsymbol{\phi}}=\mu_o\mathbf{M}$.
## Problem -- Long Magnetized Solid Cylinder I.

A long solid cylinder of radius $R$ has a magnetization $\mathbf{M}=M_o\zhat$. The cylinder is centered on the origin and aligned with the $z$--axis.

1. Find $\mathbf{K}_b$ and $\mathbf{J}_b$.
2. Find $\mathbf{B}_b(s)$, which is the magnetic field due to the bound current densities found in part 1. of this problem.

## Problem -- Long Magnetized Solid Cylinder II.

A long cylinder of radius $R$ has a magnetization of $\mathbf{M}=(M_os/R)\hat{\boldsymbol{\phi}}$. The cylinder is centered on the origin and aligned with the $z$--axis.

1. Find the bound currents
2. Find $\mathbf{B}(s)$

## Problem -- Long Magnetized Solid Cylinder III.

A long cylinder of radius $R$ has a magnetization of $\mathbf{M}=(M_os^2/R^2)\hat{\boldsymbol{\phi}}$. The cylinder is centered on the origin and aligned with the $z$--axis.

1. Find the bound currents
2. Find $\mathbf{B}_b(s)$

**Notes**

To find the field of an object with a magnetization $\mathbf{M}$, we first compute the bound surface and volume currents

$\mathbf{K}_b=\mathbf{M}\times \hat{\mathbf{n}}$

$\mathbf{J}_b=\boldsymbol{\nabla}\times \mathbf{M}$

then we use standard techniques (either Biot-Savart or Ampere's Law) to find the field due to the bound currents (most of the bound current systems we encountered were such that Ampere's Law could be used).

We are given $\mathbf{M}=M_os^2/R^2\hat{\boldsymbol{\phi}}$, so $M_{s}=0$, $M_{\phi}=M_os^2/R^2$, $M_{z}=0$:

By definition, the normal direction on the surface of an object is perpendicular to the surface and has its head pointing away from the interior of the object. A cylinder has three surfaces. If the cylinder aligned with the $z$-axis

1. the top cap has a normal pointing in the $\hat{\mathbf{z}}$-direction,
2. the bottom cap has a normal pointing in the -$\hat{\mathbf{z}}$-direction, and
3. the side has a normal pointing in the $\hat{\mathbf{\rho}}$-direction

To compute $\mathbf{J}_b$, we need to evaluate

$\nabla\times \mathbf{M} = \left({\frac {1}{s }}{\frac {\partial M_{z}}{\partial \phi }}-{\frac {\partial M_{\phi }}{\partial z}}\right) {\hat {\boldsymbol {s }}}+\left({\frac {\partial M_{s }}{\partial z}}-{\frac {\partial M_{z}}{\partial s }}\right) {\hat {\boldsymbol {\phi }}}+{\frac {1}{s }}\left({\frac {\partial \left(s M_{\phi }\right)}{\partial s }}-{\frac {\partial M_{s }}{\partial \phi }}\right) {\hat {\mathbf {z} }}$

The only term of the six in this equation that is not zero is

${\frac {1}{s }}\left({\frac {\partial \left(s M_{\phi }\right)}{\partial s }}\right) {\hat {\mathbf {z} }} = {\frac {1}{s }}\left({\frac {\partial \left(s (M_os^2/R^2)\right)}{\partial s }}\right) {\hat {\mathbf {z} }}$

So

$\mathbf{J}_b = \nabla\times \mathbf{M} = (3M_os/R^2) {\hat {\mathbf {z} }}$

On the top cap, $\hat{\mathbf{n}} = \hat{\mathbf{z}}$,

$\mathbf{K}_b=\mathbf{M}\times \hat{\mathbf{n}} = (M_os^2/R^2)\hat{\boldsymbol{\phi}}\times \hat{\mathbf{z}}=(M_os^2/R^2)\hat{\mathbf{s}}$

On the bottom cap,

$\mathbf{K}_b=\mathbf{M}\times \hat{\mathbf{n}} = (M_os^2/R^2)\hat{\boldsymbol{\phi}}\times (-\hat{\mathbf{z}})=-(M_os^2/R^2)\hat{\mathbf{s}}$

On the side, $s=R$ so $M_\phi(R)=M_oR^2/R^2=M_o$

$\mathbf{K}_b=\mathbf{M}\times \hat{\mathbf{n}} = M_o\hat{\boldsymbol{\phi}}\times \hat{\mathbf{s}}=-M_o\hat{\mathbf{z}}$

The technique that I use to figure out the cross products of unit vectors is to draw them out as three perpendicular vectors and then use the "right-hand cross-product method". 

A common error is to write the side surface current density as

$\mathbf{K}_b=-(M_os^2/R^2)\hat{\mathbf{z}}$ instead of $\mathbf{K}_b=-(M_oR^2/R^2)\hat{\mathbf{z}}$

This is an error because this current is flowing at a fixed value of $s=R$. This error occurs because implicit in the equation is $\mathbf{K}_b = \mathbf{M}\times \hat{\mathbf{n}}$ is the statement "evaluated on the surface". (I also see this error made in calculations of the bound surface charge density $\sigma_b$).

You may be thinking that I made this error for my answer for the suface current on the caps. My answer is correct but the explanation is a bit subtle, which is presumably why the problem statement says "long tube" - at least in part so we don't need deal with the caps.

So the current on the sides flows downward. We are told this is a long tube, so we'll ignore further consideration of the caps.

To find the magnetic field, use Ampere's Law with an Amperian loop being a circle parallel to the $x-y$-plane and centered on the origin.

For all $s$, we can write $\oint\mathbf{B}\bfcdot d\mathbf{l}=2\pi s B_\phi$ and $B_s=B_z=0$ based on a symmetry argument (what is it?).

For $s\lt R$,

The enclosed current is due to $J_b$ only. The current on the cylinder's sides does not pass through the Amperian loop. The current density depends on radius, so integration is require to find the amount of current from $J_b$ that flows through the Amperian loop.

$\displaystyle I_{b\text{ }encl}(s) = \int \mathbf{J}\_b \bfcdot d\mathbf{a} = ... = \int_{0}^{2\pi}\int_{0}^s J_b s' ds' d\phi=\int_{0}^{2\pi}\int_{0}^R (3M_os/R^2) s' ds' d\phi = 2\pi M_os^3/R^2$

(You should know how to justify and fill in the missing steps indicated by "...".) 

From $2\pi s B_{b\phi} = \mu_o I_{b\text{ }encl}$, we find

$B_{b\phi} = (\mu_o M_os^2)/R^2$

For $s\gt R$,

To find the net amount of current due to $\mathbf{K}_b$ that flows through the $x-y$-plane, we need to integrate $\mathbf{K}_b$, which is a current per unit length over the rim of the tube. The result is

$I_K=(2\pi R) (-M_o)=-2\pi M_oR$

For $s\gt R$, we need to substitute $s=R$ in the equation for the enclosed bound current to get the enclosed current due to $J_b$. This gives

$I_J=2\pi M_o R$

So the total downward current $I_K$ flowing on the tube's side is equal and opposite to the upward volume current $I_J$: The net amount of bound current flowing through the $x$--$y$ plane is zero. This is reminicient of polarization problems where if an object has a polarization $\mathbf{P}$, we always find the net bound charge on the object, after integrating the volume and surface charge densities is zero.

This volume current can be thought of current flowing along the axis of the tube. At the very center, the flow is zero. The flow inside the tube is largest near the inner walls of the tube. To find the net current flowing in the vertical direction due to $\mathbf{J}_b$, we need to integrate $\mathbf{J}_b$, which is a flow per unit area, over the cross-section of the tube.

$I_{b\text{ }encl}=I_K+I_J=-2\pi M_oR + 2\pi M_oR = 0$

From $2\pi s B_{b\phi} = \mu_o I_{b\text{ }encl}$, we find

$B_{b\phi}=0$.

Thus,

$\displaystyle\mathbf{B}_b=\frac{\mu_o M_o}{2\pi}\frac{s^2}{R^2}\hat{\boldsymbol{\phi}}$ for $s < R$

$\displaystyle\mathbf{B}\_b=0$ for $s > R$

## Problem -- Magnetized Sphere I.

A sphere of radius $R$ has a magnetization of $\mathbf{M}=(M_or^2/R^2)\zhat$

1. Find the bound currents
2. Sketch the surface current by drawing many circular loops on the surface. Indicate which loops have more current.
3. How much bound current flows through the $y$-$z$ plane for $y>0$?

## Problem -- Magnbetized Sphere II.

A sphere of radius $R$ has a magnetization of $\mathbf{M}=M_o\hat{\mathbf{z}}$

1. Find the bound currents
2. Sketch the surface current by drawing many circular loops on the surface. Indicate which loops have more current.
3. How much bound current flows through the $y$-$z$ plane for $y>0$?

%**Notes**

%This is related to Example 6.1 of Griffiths. I may have also done this one in class.

%$$\mathbf{J}_b = \nabla\times \mathbf{M} = 0$$

%1\. The normal vector on the surface of a sphere is $\hat{\mathbf{r}}$. So

%$\mathbf{K}_b=\mathbf{M}\times \hat{\mathbf{n}}=M_o\hat{\mathbf{z}}\times \hat{\mathbf{r}}$

%In one of the lectures on chapter 4, there was a problem I or two where I covered how to compute $\hat{\mathbf{z}}\times \hat{\mathbf{r}}$. Briefly, because the direction of the unit vector changes, we need to put both unit vectors in the same coordinate system.  With a drawing, you can show that $\hat{\mathbf{z}}=\cos\theta\hat{\mathbf{r}} - \sin\theta\hat{\boldsymbol{\theta}}$. So 

%$\mathbf{K}_b=M_o(\cos\theta\hat{\mathbf{r}} - \sin\theta\hat{\boldsymbol{\theta}})\times \hat{\mathbf{r}}=-M_o\sin\theta (\hat{\boldsymbol{\theta}}\times \hat{\mathbf{r}})=M_o\sin\theta \hat{\boldsymbol{\phi}}$

%2\. This surface current is wrapping around the sphere. The current is the largest near the equator and the smallest near the poles. Griffiths notes that if you glued charges to the surface of a sphere and rotated a sphere around the $z$-axis, you would get a surface charge density that is proportional to $\sin\theta \hat{\mathbf{\theta}}$. My diagram is something like [http://photonics101.com/images/articles/magnetic-sphere-with-surface-current/magnetic-sphere-surface-current-256.png] with an indication that the red loops carry more current near the equator.

%3\. $I = \int_0^{\pi} K_b (a d\theta) = M_oa  \int_0^{\pi} \sin\theta d\theta=2M_oa$