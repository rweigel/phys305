# Electric Current

<div style="background-color:yellow">
**This section on surface currents can be skipped. We will revisit it in Chapter 5.**
</div>

This topic is covered briefly in Chapter 5.1.3 of Griffiths. At this point, these notes only contain an overview, and examples and problems will be added when Chapter 5 is covered.

## Definitions

The current that flows through a wire has units of charge/s. The equation developed for $\dot{N}$ at a point on a line can be used to compute current if we redefine $\lambda$ to be the number of charges per unit length instead of the number of particles per unit length. In this case, instead of using $\dot{N}$, we use $I$:

$$I=\lambda v$$

Similarly, re--defining $\sigma$ as the number of charges per unit area, the flow of current past a line $\mathcal{L}$ is

$$I=\int_{\mathcal{L}}\sigma \mathbf{v}\bfcdot \hat{\mathbf{n}}dl$$

Finally, redefining $\rho$ as the number of charges per unit volume, the flow of current past an area $\mathcal{A}$ is 

$$I=\int_{\mathcal{A}}\rho \mathbf{v}\bfcdot \hat{\mathbf{n}}dA$$

### Example -- Computing Total Charge Passing a Point

### Problem -- Computing Total Charge Passing a Line

## Surface Currents

When working with current flowing on a surface, we will need to use the current densities $\mathbf{K}$ and $\mathbf{J}$, respectively.

Surface currents are described and used in Chapter 5.1 of Griffiths.

### Surface Current $\mathbf{K}$


$\mathbf{K}$ has units of (charge/s)/length = (current/length) and is defined by

$\displaystyle \mathbf{K} \equiv \sigma \mathbf{v}$ so that $\displaystyle I=\int_{\mathcal{L}}\sigma\mathbf{v}\bfcdot \hat{\mathbf{n}}=\int_{\mathcal{L}}\mathbf{K}\bfcdot \hat{\mathbf{n}}dl$

From which it follows that

$\displaystyle dI = \mathbf{K}\bfcdot \hat{\mathbf{n}}dl=Kdl_\perp$

where $dl_\perp$ is a differential element of length that is perpendicular to $\mathbf{K}$.

Griffiths uses the equivalent definition

$\displaystyle \mathbf{K} \equiv \frac{d\mathbf{I}}{dl_\perp}$

which follows from $dI=Kdl_\perp$ by multiplying both sides by a unit vector in the direction of $\mathbf{K}$.

### Volume Current $\mathbf{J}$

$\mathbf{J}$ has units of (charge/s)/area and is defined by

$\displaystyle\mathbf{J} \equiv \rho \mathbf{v}$ so that $\displaystyle I=\int_{\mathcal{A}} \rho\mathbf{v}\bfcdot \hat{\mathbf{n}}=\int_{\mathcal{A}} \mathbf{J}\bfcdot \hat{\mathbf{n}}dA$

From which it follows that

$\displaystyle dI = \mathbf{J}\bfcdot \hat{\mathbf{n}}dA=Jda_\perp$

Griffiths uses the equivalent definition

$\displaystyle \mathbf{J} \equiv \frac{d\mathbf{I}}{da_\perp}$

which follows from $dI = Jda_\perp$ by multiplying both sides by a unit vector in the direction of $\mathbf{J}$.

# Current Distributions

## Current

A current $I$ flows through a wire of radius $a$.

1. If the current is uniformly distributed over the surface, what is the surface current density $K$?
2. If the current is distributed in such a way that the volume current density is inversely proportional to the distance from the axis, what is $J$?

**Answer**
1\. 

In general, $\mathbf{K}=d\mathbf{I}/dl_{\perp}$.

Because $I$ is constant along and perpendicular to $l_{\perp}$, and $l_{\perp}=2\pi a$, one can immediately write $K = \frac{I}{2\pi a}$.

For a more formal solution, assume the wire is along the $z$-axis so that $\mathbf{I}=I\hat{\mathbf{z}}$. The perpendicular direction is along the $\hat{\phi}$ direction so that $dl_{\perp}=ds=ad\phi$, where $ds$ is a differential length along circumference.

If $\mathbf{K}=d\mathbf{I}/dl_{\perp}$, then

$\int_0^{2\pi}Kad\phi = I$.

$K$ is independent of $\phi$, so it can be factored out of the integral, leaving

$2\pi aK = I$ or

$K = \frac{I}{2\pi a}$

and the vector is

$\mathbf{K} = \frac{I}{2\pi a}\hat{\phi}$

2\.

In general, $\mathbf{J}=d\mathbf{I}/da_{\perp}$.

Assume the wire is along the $z$-axis so that $\mathbf{I}=I\hat{\mathbf{z}}$. The perpendicular area is a circle (cross-section of wire) so that a differential element is $da_{\perp}=rdrd\phi$.

If $I$ were constant along and perpendicular to $a_{\perp}$, and using $a_{\perp}=\pi a^2$, one can immediately write $J = \frac{I}{\pi a^2}$.

In this case, however, $J$ is not constant; we are given $J=c/r$.

If $\mathbf{J}=d\mathbf{I}/da_{\perp}$, we can write $\mathbf{J}da_{\perp}=d\mathbf{I}$; noting that both vectors are in the $z$-direction and integrating gives

$\int_0^{2\pi}\int_0^{a}Jrdrd\phi = I$.

Subsititution of $J=c/r$ gives

$\int_0^{2\pi}\int_0^{a}(c/r)rdrd\phi= I$.

Integration gives

$c2\pi a = I$ or

$c =I/2\pi a$

So that 

$\mathbf{J} = \frac{I}{2\pi ar}\hat{\mathbf{z}}$

As a final check, note that the units on $J$ are current/area, as expected from  $\mathbf{J}=d\mathbf{I}/da_{\perp}$.

## Current

A disk with a uniform charge density $\sigma_o$ rotates at an angular velocity $\omega$ around its symmetry axis. What is the surface current density $K(r)$, where $r$ is the distance from the center of the disk? (<span style="background-color:yellow">+2</span>)

What is the total current? (<span style="background-color:yellow">++2 (extra credit)</span>)

**Answer**

In general, $\mathbf{K}=\sigma \mathbf{v}$. The velocity depends on distance according to $\mathbf{v}=\omega r\hat{\phi}$, giving

$\mathbf{K}=\sigma_o \omega r\hat{\phi}$

The total current can be found by considering $K$ along a radial line. $K$ represents the current per unit length that flows perpendicular this line: $\mathbf{K}=d\mathbf{I}/dl_{\perp}$, where $dl_{\perp}=dr$.

$\mathbf{K}=\sigma_o \omega r\hat{\phi}=d\mathbf{I}/dr$. Integrating both sides gives

$\int_0^{a}\sigma_o \omega r dr = I$

so that 

$$\mathbf{I}=\frac{\sigma_o \omega a^2}{2}\hat{\phi}$$

## Current

A current $\mathbf{I}=I_o\hat{\mathbf{z}}$ flows through a wire of radius $a$ centered on the $z$-axis.

1. If the current is uniformly distributed over the surface, what is the surface current density $\mathbf{K}$?
2. If the current is distributed in such a way that the volume current density is inversely proportional to the distance from the axis, what is $\mathbf{J}$?

**Answer**

1\. In general, $\mathbf{K}=d\mathbf{I}/dl_{\perp}$.

Because $I$ is constant along and perpendicular to $l_{\perp}$, and $l_{\perp}=2\pi a$, one can immediately write $K = \frac{I}{2\pi a}$.

For a more formal solution, assume the wire is along the $z$-axis so that $\mathbf{I}=I\hat{\mathbf{z}}$. The perpendicular direction is along the $\hat{\phi}$ direction so that $dl_{\perp}=ds=ad\phi$, where $ds$ is a differential length along circumference.

If $\mathbf{K}=d\mathbf{I}/dl_{\perp}$, then

$\int_0^{2\pi}Kad\phi = I$.

$K$ is independent of $\phi$, so it can be factored out of the integral, leaving

$2\pi aK = I$ or

$K = \frac{I}{2\pi a}$

and the vector is

$\mathbf{K} = \frac{I}{2\pi a}\hat{\phi}$

2\. In general, $\mathbf{J}=d\mathbf{I}/da_{\perp}$.

Assume the wire is along the $z$-axis so that $\mathbf{I}=I\hat{\mathbf{z}}$. The perpendicular area is a circle (cross-section of wire) so that a differential element is $da_{\perp}=rdrd\phi$.

If $I$ were constant along and perpendicular to $a_{\perp}$, and using $a_{\perp}=\pi a^2$, one can immediately write $J = \frac{I}{\pi a^2}$.

In this case, however, $J$ is not constant; we are given $J=c/r$.

If $\mathbf{J}=d\mathbf{I}/da_{\perp}$, we can write $\mathbf{J}da_{\perp}=d\mathbf{I}$; noting that both vectors are in the $z$-direction and integrating gives

$\int_0^{2\pi}\int_0^{a}Jrdrd\phi = I$.

Subsititution of $J=c/r$ gives

$\int_0^{2\pi}\int_0^{a}(c/r)rdrd\phi= I$.

Integration gives

$c2\pi a = I$ or

$c =I/2\pi a$

So that 

$\mathbf{J} = \frac{I}{2\pi ar}\hat{\mathbf{z}}$

As a final check, note that the units on $J$ are current/area, as expected from  $\mathbf{J}=d\mathbf{I}/da_{\perp}$.

## Current

A disk with a uniform charge density $\sigma_o$ rotates at an angular velocity $\omega$ around its symmetry axis. What is the surface current density $\mathbf{K}(r)$, where $r$ is the distance from the center of the disk?

**Answer**

In general, $\mathbf{K}=\sigma \mathbf{v}$. The velocity depends on distance according to $\mathbf{v}=\omega r\hat{\phi}$, giving

$\mathbf{K}=\sigma_o \omega r\hat{\phi}$

The total current can be found by considering $K$ along a radial line. $K$ represents the current per unit length that flows perpendicular this line: $\mathbf{K}=d\mathbf{I}/dl_{\perp}$, where $dl_{\perp}=dr$.

$\mathbf{K}=\sigma_o \omega r\hat{\phi}=d\mathbf{I}/dr$. Integrating both sides gives

$\int_0^{a}\sigma_o \omega r dr = I$

so that 

$$\mathbf{I}=\frac{\sigma_o \omega a^2}{2}\hat{\phi}$$

## Current

A uniformly charged sphere of radius $a$ and total charge $Q$ is centered at the origin and spinning with an angular velocity $\omega$ about the $z$-axis. Find the current density $\mathbf{J}$ as a function of the spherical coordinates $r,\theta,\phi$ in the sphere.

## Rotating Disk

A disk with a uniform charge density $\sigma_o$ rotates at an angular velocity $\omega$ around its symmetry axis. What is the surface current density $\mathbf{K}(r)$, where $r$ is the distance from the center of the disk?

**Answer**

In general, $\mathbf{K}=\sigma \mathbf{v}$. The velocity depends on distance according to $\mathbf{v}=\omega r\hat{\phi}$, giving

$\mathbf{K}=\sigma_o \omega r\hat{\phi}$

The total current can be found by considering $K$ along a radial line. $K$ represents the current per unit length that flows perpendicular this line: $\mathbf{K}=d\mathbf{I}/dl_{\perp}$, where $dl_{\perp}=dr$.

$\mathbf{K}=\sigma_o \omega r\hat{\phi}=d\mathbf{I}/dr$. Integrating both sides gives

$\int_0^{a}\sigma_o \omega r dr = I$

so that 

$$\mathbf{I}=\frac{\sigma_o \omega a^2}{2}\hat{\phi}$$

## Rotating Sphere

A uniformly charged sphere of radius $a$ and total charge $Q$ is centered at the origin and spinning with an angular velocity $\omega$ about the $z$-axis. Find the current density $\mathbf{J}$ as a function of the spherical coordinates $r,\theta,\phi$ in the sphere.

## Wire

A current $\mathbf{I}=I_o\hat{\mathbf{z}}$ flows through a wire of radius $a$ centered on the $z$-axis.

If the current is uniformly distributed over the surface, what is the surface current density $\mathbf{K}$?

**Answer**

In general, $\mathbf{K}=d\mathbf{I}/dl_{\perp}$.

Because $I$ is constant along and perpendicular to $l_{\perp}$, and $l_{\perp}=2\pi a$, one can immediately write $K = \frac{I}{2\pi a}$.

For a more formal solution, assume the wire is along the $z$-axis so that $\mathbf{I}=I\hat{\mathbf{z}}$. The perpendicular direction is along the $\hat{\phi}$ direction so that $dl_{\perp}=ds=ad\phi$, where $ds$ is a differential length along circumference.

If $\mathbf{K}=d\mathbf{I}/dl_{\perp}$, then

$\int_0^{2\pi}Kad\phi = I$.

$K$ is independent of $\phi$, so it can be factored out of the integral, leaving

$2\pi aK = I$ or

$K = \frac{I}{2\pi a}$

and the vector is

$\mathbf{K} = \frac{I}{2\pi a}\hat{\phi}$

If the current is distributed in such a way that the volume current density is inversely proportional to the distance from the axis, what is $\mathbf{J}$?

**Answer**

In general, $\mathbf{J}=d\mathbf{I}/da_{\perp}$.

Assume the wire is along the $z$-axis so that $\mathbf{I}=I\hat{\mathbf{z}}$. The perpendicular area is a circle (cross-section of wire) so that a differential element is $da_{\perp}=rdrd\phi$.

If $I$ were constant along and perpendicular to $a_{\perp}$, and using $a_{\perp}=\pi a^2$, one can immediately write $J = \frac{I}{\pi a^2}$.

In this case, however, $J$ is not constant; we are given $J=c/r$.

If $\mathbf{J}=d\mathbf{I}/da_{\perp}$, we can write $\mathbf{J}da_{\perp}=d\mathbf{I}$; noting that both vectors are in the $z$-direction and integrating gives

$\int_0^{2\pi}\int_0^{a}Jrdrd\phi = I$.

Subsititution of $J=c/r$ gives

$\int_0^{2\pi}\int_0^{a}(c/r)rdrd\phi= I$.

Integration gives

$c2\pi a = I$ or

$c =I/2\pi a$

So that 

$\mathbf{J} = \frac{I}{2\pi ar}\hat{\mathbf{z}}$

As a final check, note that the units on $J$ are current/area, as expected from  $\mathbf{J}=d\mathbf{I}/da_{\perp}$.

## Hollow Cylinder

An hollow cylinder of radius $a$ carries a total current $\mathbf{I}=I_o\hat{\mathbf{z}}$ on its surface. Compute $\mathbf{K}$.

**Answer**

The current flows perpendicular to the rim of the cylinder. The length of the perpendicular line the current flows through is $2\pi a$. So

$$\mathbf{K}=\frac{I_o}{2\pi a}\hat{\mathbf{z}}$$

## Hollow Cylinder

An hollow cylinder of radius $a$ carries a current density $K_o\sin^2\phi\hat{\mathbf{z}}$ on its surface. Compute $\mathbf{I}$.

**Answer**

The current flows perpendicular to the rim of the cylinder. The differential length of a line perpendicular to the current is $dl_\perp=ad\phi$. So

$$\mathbf{I}=\int_0^{2\pi}K_o\sin^2\phi a d\phi\hat{\mathbf{z}}$$

because

$$\mathbf{K}\equiv \frac{d\mathbf{I}}{dl_\perp}$$

## Solenoid

A hollow cylinder of radius $a$ and length $l$ carries a surface current density of $\mathbf{K}=K_o\hat{\mathbf{\phi}}$.

How much current passes a line parallel to its axis on the surface?

How many wire loops of radius $a$ carrying a current $I_o$ would you need to stack together to create this surface current density?

**Answer**

The current flows perpendicular to a line of length $l$. So $I=K_ol$ is the number of coulombs/sec that pass the line.

We need the total current to be

$I=K_ol$

using $N$ loops each carrying current $I_o$.

$K_ol=NI_o$

or 

$N=K_ol/I_o$

The number of loops per unit length is

$N/l=n=K_o/I_o$
