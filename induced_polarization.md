# Introduction 0

Dielectrics (Polarizable Material)

When there is only one dipole in a constant electric field, it is easy to compute the modified electric field.

When there are many dipoles, each induced dipole modifies the total electric field, and the total electric field is what determines how large $\mathbf{P}$ is.

In response to an external electric field, $\mathbf{E}_o$, the molecules in a dielectric material reconfigure so as to produce a generally opposing electric field inside the material. In general, the electric field outside of the dielectric is also modified from $\mathbf{E}_o$.

This is similar to what happens in a conductor in an external electric field, with the difference being that in the conductor, free electrons can move to the surface of the conductor in such a way as to completely cancel the electric field inside the material. In a dielectric, electrons are bound and can only shift their position slightly. This shift creates an induced dipole. The large-scale electric field inside a dielectric material is the external electric field plus the electric field created by all of the induced dipoles.

There are two general types of dielectric materials:

1. materials that have molecules that have no net electric field - these are referred to as non-polar molecules; and
2. materials that have molecules that each have a net intrinsic electric field but are randomly oriented so on average the electric field is zero. These are referred to as polar molecules.

In simple dielectrics, the amount of polarization in a small volume is given by

$$\mathbf{P}(x,y,z)=\epsilon_0\chi_e\mathbf{E}(x,y,z)$$

where $\chi_e$ is a dimensionless proportionality constant and $\mathbf{E}$ is the net electric field at the location of the small volume.

In the following two examples, we give a physical justification for this equation for non-polar and polar dielectrics.

The interpretation of this equation is that in a given volume in the dielectric, the induced polarization is proportional to the electric field, $\mathbf{E}$, at that location. The electric field at a given location in the material depends on the external electric field, $\mathbf{E}_o$, ''and'' the electric field created by all of the other induced dipoles in the material. This fact makes the calculation of the electric field inside of a dielectric complicated. This complication is highlighted in an example below.

## Mental Model for Non-Polar Dielectrics

At the atomic level, the creation of a dipole when an atom is exposed to an external electric field can be understood from a simple model of the atom.

## Mental Model for Polar Dielectrics

A simple model for understanding polar molecules involves considering only the torque exerted on the polar molecule and ignoring the shift of the electron orbits considered for the non-polar molecule.

## Calculation of Electric Field

It was noted that calculation of the net electric field inside and outside of a dielectric is complicated by the fact that at a given location the electric field is that due to external sources plus that due to all of the induced dipoles at other locations in the material. Here we give an example of how this could be handled mathematically. This is ''not'' a good way of computing the electric field, but serves to justify the "complicated" claim. This example is based on Example XX in Griffiths, 1989.

Asking a given location in a material to report on its polarization is akin to calling for a vote among a group of humans where everyone prefers to vote only after hearing how everyone else is going to vote.

$$\mathbf{P}(x,y,z)=\epsilon_0\chi_e\mathbf{E}(x,y,z)$$

# Fundamental Dielectric Example

In reality, the "pure" dipoles are not created by gluing dipoles into and onto an object - they are induced. The charges in an atom or molecule separate due to a local electric field and a dipole is induced. The dipole is "bound" in the sense that the charges that make up the dipole are bound to the atom or molecule.

An external electric field, $\mathbf{E}\_{ext}=E_{ext}\hat{\mathbf{x}}$ is created by two non-conducting sheets of charge.

A dielectric slab is placed between the sheet.

Find $\mathbf{E}_b$ and $\mathbf{E}$ inside the dielectric slab assuming that the dipole density induced in the slab depends on the electric field in the slab according to $\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$, where $\mathbf{E}$ is the total electric field, which is due to the induced bound charge densities and the external electric field.

The result is $\mathbf{E}=\frac{1}{1+\chi_e}E_{ext}\hat{\mathbf{x}}$. The key steps are

$$\mathbf{E} = \mathbf{E}_{ext} + \mathbf{E}_b$$

$$\mathbf{P} = \epsilon_o\chi_e\mathbf{E}$$

The key to this problem is realizing that $\mathbf{P}$ depends directly on $\mathbf{E}$ in this way and not on $\mathbf{E}_{ext}$.  That is, $\mathbf{P}$ depends on the electric field due to both bound charges that are induced and external charges (the charges on the sheets).

$$\sigma_b\equiv\mathbf{P}\cdot\hat{\mathbf{n}}=\epsilon_o\chi_e\mathbf{E}\cdot\hat{\mathbf{n}}$$

On the right/left face of the dielectric $\hat{\mathbf{n}}=\pm\hat{\mathbf{x}}$, so the right/left face has a bound surface charge density of

$$\sigma_b = \pm\epsilon_o\chi_eE$$

%$\rho_b=\left(\frac{\epsilon_o}{\epsilon}-1\right)\rho_f=-\left(\frac{\chi_e}{1+\chi_e}\right)\rho_f$ for reasons explained in the next section.

The electric field due to the bound surface charge densities can be found by finding the electric field due to $\sigma_b$ on an infinite sheet of charge. 

Inside the dielectric, the electric field $\mathbf{E}_b$, which is due to $\sigma_b$, is $\mathbf{E}_b=-(\sigma_b/\epsilon_o)\hat{\mathbf{x}}$. Using $\sigma_b=\pm\epsilon_o\chi_eE$ found above gives

$$\mathbf{E}_b = -\chi_eE\hat{\mathbf{x}}$$

Inside the dielectric, the total field is

$$\mathbf{E} = E\hat{\mathbf{x}} = \mathbf{E}\_{ext} + \mathbf{E}\_b=E_{ext}\hat{\mathbf{x}} - \chi_eE\hat{\mathbf{x}}$$

Solving for $E$ gives

$$E=\frac{1}{1+\chi_e}E_{ext}$$

Note that if you solved this problem by (wrongly) assuming $\mathbf{P} = \epsilon_o\chi_e\mathbf{E}$, you would have found

$$E=(1-\chi_e)E_{ext}\qquad\mbox{(wrong answer)}$$

To see why this is wrong, consider the physical implications of this equation when $\chi_e>1$ (for example, for water).

# Relationship Between $\rho_f$ and $\rho_b$ for Linear Dielectric

We first need to derive the Poisson equation

$$\boldsymbol{\nabla}^2\Phi=-\frac{\rho_f}{\epsilon}$$

Starting with the definition $\mathbf{D}\equiv \epsilon_o\mathbf{E}+\mathbf{P}$, with the assumption of linear material - $\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$ 

$$\mathbf{D}=\epsilon_o\mathbf{E}+\mathbf{P}=\epsilon_o\mathbf{E} + \epsilon_o\chi_e\mathbf{E}=\epsilon_o(1+\chi_e)\mathbf{E}=\epsilon\mathbf{E}$$

$$\Rightarrow\qquad\mathbf{D}=\epsilon\mathbf{E}\qquad\mbox{ where }\quad\epsilon \equiv \epsilon_o(1+\chi_e)$$

Next, consider using the above in $\boldsymbol{\nabla}\cdot\mathbf{D}=\rho_f$

$$\boldsymbol{\nabla}\cdot\mathbf{D}=\boldsymbol{\nabla}\cdot(\epsilon\mathbf{E})=\rho_f$$

Using assumption that $\boldsymbol{\nabla}\epsilon=0$,

$$\epsilon\boldsymbol{\nabla}\cdot\mathbf{E}=\rho_f$$

And using $\mathbf{E}=-\boldsymbol{\nabla}\Phi$ (which does not require assumption of linear material)

$$\boldsymbol{\nabla}^2\Phi=-\frac{\rho_f}{\epsilon}$$

Note that Poisson's equation still applies when we don't treat the bound and free charges separately:

$$\boldsymbol{\nabla}^2\Phi=-\frac{\rho}{\epsilon_o}=-\frac{\rho_f+\rho_b}{\epsilon_o}$$

So the bound volume charge density is related to the free charge density:

$$\rho_b=\left(\frac{\epsilon_o}{\epsilon}-1\right)\rho_f=-\left(\frac{\chi_e}{1+\chi_e}\right)\rho_f$$

Therefore, $\rho_b=0$ when $\rho_f=0$. That is, if there are no free charges embedded in the dielectric, the bound charge volume density will be zero. Note that this also requires the condition $\boldsymbol{\nabla}\epsilon=0$.

# Introduction

In [Continuous Electric Dipole Distributions](continuous_electric_dipole_distributions.html), the problem of finding the electric field due to an object that had a polarization $\mathbf{P}$ "frozen in" was considered.

The approach was to find the bound charge densities that result from this polarization. Then the electric field due to the bound charge densities was computed.

Consider an object that is unpolarized ($\mathbf{P}=0$), but is placed in an external electric field, $\mathbf{E}_{ext}$. In response to this electric field, atomic--sized dipoles will tend to form. Thes induced dipoles create an electric field, which called an induced electric field.

The total field is then

$\mathbf{E}\_{total}=\mathbf{E}\_{external} + \mathbf{E}_{induced}$

By convention, we drop the "total" subscript and abbreviate "external" as "ext". Given that the induced field is can be computed from bound charge densities, we can use $\mathbf{E}\_b$ in place of $\mathbf{E}\_{induced}$ to emphasize this point. In this notation, we have

$\mathbf{E}=\mathbf{E}\_{ext} + \mathbf{E}_{b}$

It is important to note that $\mathbf{E}_b$ depends on $\mathbf{E}$.

Without additional information, it is not possible to compute $\mathbf{E}$ -- we need to know how much $\mathbf{P}$ is generated given $\mathbf{E}$. Once we have $\mathbf{P}$, we can compute the bound charge densities and then $\mathbf{E}_b$.

For many materials, the relationship between $\mathbf{P}$ and $\mathbf{E}$ is linear:

$\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$

where the constant $\chi_e$ is the **electric susceptibility**.

A constant that often appears in induced polarization problems is $\epsilon_o(1+\chi_e)$, which is called **permittivity** or the **dielectric constant**:

$\epsilon\equiv \epsilon_o(1+\chi_e)$

## Example -- Infinite Slab

An object with an electric susceptibility of $\chi_e$ is in the region $|z| \le t$. The object is infinite in extent in the $x$ and $y$ directions.

There is an external electric field of $E_o\zhat$.

Find $\mathbf{E}$

**Answer**

$\mathbf{E}=\mathbf{E}\_{ext} + \mathbf{E}_{b}$

$E_z = E_{ext\text{ z}} + E_{b\text{ z}}$

$E_z = E_o + E_{b\text{ z}}$

At this point, $E_z$ and $E_{b\text{ z}}$ are unknown. We know that $E_{b\text{ z}}$ is related to $P_z$, which is in turn related to $E_z$.

The bound surface densities are $\sigma_b=\pm P_z$ on the top/bottom surfaces of the slab. The polarization is related to $E_z$ by $P_z = \epsilon_o\chi_e E_z$, so $\sigma_b=\pm \epsilon_o\chi_e E_z$.

$\rho_b=0$. This can be seen by taking the divergence of both sides of $\mathbf{E} = \mathbf{E}\_{ext} + \mathbf{E}_{b}$, which gives $\boldsymbol{\nabla}\bfcdot\mathbf{E} = 0 + \rho_b$. Using $\rho_b=-\epsilon_o\boldsymbol{\nabla}\bfcdot\mathbf{P}$ and $\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$ results in $\rho_b=0$ and $dE_z/dz=0$, so the field inside of the dielectric is constant.

% This need to be justified. See notes where rho_b is related to rho_f.

As a result of $\sigma_b$, the $E_{b\text{ z}}=-P_z/\epsilon_o=-\chi_e E_z$ in the slab and $E_{b\text{ z}}=0$ outside of the slab.

Thus, inside the slab

$E_z = E_o + E_{b\text{ z}}=E_o-\chi_e E_z$

Solving for $E_z$ gives

$\displaystyle E_z=\frac{E_o}{1+\chi_e}$

Outside the slab, $E_z=E_o$.

Inside the slab, the induced polarization opposes the external electric field and causes the field to be smaller. Outside the slab, the induced electric field has no effect.

## Problem -- Infinite Slab

A slab of polarizable material is placed between two infinite sheets of charge as shown in the following figure.

<img src="figures/Polarizable_Objects_Slab.svg"/>

The slab is between $y=t$ and $y=2t$ and is infinite in extent in the $x$ and $z$ directions. The bottom sheet of charge is in the $y=0$ plane and has a charge density of $\sigma_o$. The top sheet of charge is in the $y=3t$ plane and has a charge density of $-\sigma_o$.

You may assume without proof that $\rho_b=0$.

1. Find and plot $E_y(y)$ if the slab has an electric susceptibility of $\chi_e=0$.
2. Find and plot $E_y(y)$ if the slab has $\chi_e=0.5$.
3. Using $E_y(y)$ from part 2. of this problem, compute the potential difference between $y=3t$ and $y=0$ (that is, find $V(3t)-V(0)$).

%**Answer**

%In the following, all of the fields are in the $y$ direction and so the subscript $y$ is omitted.

%$E_{ext}=(\sigma_o/\epsilon_o)$

%$E = E_{ext} + E_b$

%$\rho_b=0$ and $\rho_b=-\boldsymbol{\nabla}\bfcdot \mathbf{E}=-dE/dy$ imply that the field does not change in the slab, so the field at $y=2t$ will be the same as that at $y=t$.

%$\sigma_b = \pm \mathbf{P}\bfcdot \zhat = \pm \epsilon_o\chi_e E$

%These bound charges create a bound field that is $-\chi_eE$ inside the slab and zero outside. Thus

%Outside 

%$\displaystyle E=E_{ext}=\frac{\sigma_o}{\epsilon_o}$

%Inside,

%$E=E_{ext}-\chi_eE$

%Solving for $E$ gives

%$\displaystyle E=\frac{\sigma_o}{(1+\chi_e)\epsilon_o}=\frac{\sigma_o}{\epsilon}$

## Example -- Dielectric Around a Charged Sphere

In Example 4.5 of Griffiths, he finds the total electric field when a dielectric (polarizable material) is wrapped around a spherical shell with a net charge. 

The total electric field is the sum of the field due to the induced polarization and the charges on the spherical shell.

Verify the equations for the total electric field stated in the solution to Example 4.5 by computing it using

$\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$

where $\mathbf{E}_b$ is the field due to the bound surface charge densities on the inner and outer surface of the dielectric, and $\mathbf{E}_Q$ is the field due to the charges on the surface of the sphere. Use the surface charge densities found in Example 4.5 for you calculations of the electric field.

**Answer**

Use Gauss's law to find the electric field as a function of $r$ due to three surface charges: $\sigma_Q = Q/4\pi a^2$ on a sphere of radius $a$, $\sigma_{bi}=-\epsilon_o\chi_eQ/4\pi\epsilon a^2$ at $r=a$, and $\sigma_{bo}=\epsilon_o\chi_eQ/4\pi\epsilon b^2$ at $r=b$

$\sigma_Q$ creates $\mathbf{E}_Q$, which is zero for $r\lt a$ and $Q/4\pi\epsilon_o r^2$ for $r\gt a$.

$\sigma_{bi}$ creates $\mathbf{E}\_{bi}$, which is zero for $r\lt a$ and $4\pi a^2\sigma_{bi}/4\pi\epsilon_o r^2$ for $r\gt a$.

$\sigma_{bo}$ creates $\mathbf{E}\_{bo}$, which is zero for $r\lt b$ and $4\pi b^2\sigma_{bo}/4\pi\epsilon_o r^2$ for $r\gt b$.

The sum of the fields due to the three surface charge densities $\mathbf{E}\_{bi} + \mathbf{E}\_{bo} + \mathbf{E}\_Q$ gives $\mathbf{E}$ given in Example 4.5.

# Problems

## Dielectric Around a Charged Sphere

Solve Example 4.5 of Griffiths without using Gauss's law for dielectrics (which is $\oint\mathbf{D}\bfcdot d\mathbf{A}=Q_{f\text{ }encl})$.

Start with $\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$ and then find $\mathbf{E}_b$ by finding the surface charge densities on the inner and outer surface. These surface charge densities are $\sigma_b(a)=\mathbf{P}(a)\bfcdot\hat{\mathbf{n}}$ and $\sigma_b(b)=\mathbf{P}(b)\bfcdot\hat{\mathbf{n}}$. To find $\mathbf{E}_b$, use the relationship $\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$. Assume that $\rho_b$ is zero.

Once $\mathbf{E}_b$ is found, $\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$ can be used to solve for $\mathbf{E}$.

Hint: Inside the dielectric, the equation for $\mathbf{E}$ should depend on $E_r(a)$, $r$, and constants. To finish the problem, one needs to solve for the unknown $E(a)$. This can be done by setting $r=a$ in the equation for $\mathbf{E}$.

**Answer**

Inside the dielectric, the field is due to $\sigma_b(a)=-P(a)$ and the uniform charge on the conducting surface. The net field inside is then

$\displaystyle E_r(r) = k\frac{Q}{r^2}+k\frac{\sigma_b(a)4\pi a^2}{r^2} = k\frac{Q}{r^2}-\frac{1}{4\pi\epsilon_o}\frac{P(a)4\pi a^2}{r^2}=k\frac{Q}{r^2}-\frac{1}{\epsilon_o}\frac{P(a) a^2}{r^2}$

We don't know $P(a)$ yet. However, for a linear dielectric, the polarization $P_r$ is related $E_r$ by $P_r=\epsilon_o\chi_eE_r$. Substitution gives

$\displaystyle E_r(r)=k\frac{Q}{r^2}-\frac{a^2}{r^2}\chi_e E_r(a)$

To finish the problem, set $r=a$, solve for $E_r(a)$, and then substitute the found value of $E_r(a)$ into the above equation.

Setting $r=a$ gives

$\displaystyle E_r(a)=k\frac{Q}{a^2}-\chi_e E_r(a)\quad\Rightarrow\quad E_r(a)=\frac{kQ}{(1+\chi_e)a^2}$

Substitution into the equation above for $E_r(r)$ gives

$\displaystyle E_r(r)=k\frac{Q}{r^2}-\frac{a^2}{r^2}\chi_e \frac{kQ}{(1+\chi_e)a^2}$

This simplifies to

$\displaystyle E_r(r)=\frac{k}{1+\chi_e}\frac{Q}{r^2}$

With $k=4\pi\epsilon_o$ and the definition $\epsilon=\epsilon_o(1+\chi_e)$, this is

$\displaystyle E_r(r)=\frac{1}{4\pi\epsilon}\frac{Q}{r^2}$

Note that the electric field is reduced in the dielectric ($\chi_e\gt 0$), as expected.
