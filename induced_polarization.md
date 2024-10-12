# Introduction

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

A dielectric slab is placed between the sheets.

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

# Maxwell Equations for Dielectrics 


The basic boundary value equations are

$$\mathbf{D}=\epsilon\mathbf{E}\qquad\boldsymbol{\nabla}^2\Phi=-\frac{\rho_f}{\epsilon} \qquad\mathbf{E}=-\boldsymbol{\nabla}\Phi\qquad \epsilon \equiv \epsilon_o(1+\chi_e)$$

Recall that when $\rho_f=0$,

$$\boldsymbol{\nabla}^2\Phi=0$$

requires assumption that $\boldsymbol{\nabla}\epsilon=0$. If $\epsilon$ changes, we will split the volume into separate regions where it is constant. (Similar to what was done in the homework problem where we solved $\boldsymbol{\nabla}^2\Phi=0$ in two regions separated by a sheet of charge so that we could solve Laplace's equation in two regions instead of Poisson's equation with a delta function charge density.).

$$\Phi_2(\mathbf{x}_2)-\Phi_1(\mathbf{x}_1)= \int_{\mathbf{x}_1}^{\mathbf{x}_2} \mathbf{E}\cdot d\mathbf{l}\quad\Rightarrow $$

$$\Phi_1=\Phi_2$$

$$\oint \mathbf{E}\cdot d\mathbf{l}=0\quad \Rightarrow $$

$$E_{2\parallel}=E_{1\parallel}\qquad \mbox{or}\qquad \frac{\partial\Phi_2}{\partial t}=\frac{\partial\Phi_1}{\partial t}$$

where $t$ is any coordinate parallel to the interface.

$$\oint_S\mathbf{D}\cdot d\mathbf{a}=Q_{f\thinspace enc} \Rightarrow$$

$$D_{2\perp}-D_{1\perp}=\sigma_f\quad\mbox{or}\quad\epsilon_2E_{2\perp}-\epsilon_1E_{1\perp}=\sigma_f\quad\mbox{or}\quad-\epsilon_2\frac{\partial\Phi_2}{\partial n}+\epsilon_1\frac{\partial\Phi_1}{\partial n}=\sigma_f$$

where $n$ is outward normal of volume $1$.

In summary, across any surface (but most useful when $\epsilon_2\ne \epsilon_1$)

$$\Phi_1=\Phi_2$$

$$\frac{\partial\Phi_2}{\partial t}=\frac{\partial\Phi_1}{\partial t}$$

$$-\epsilon_2\frac{\partial\Phi_2}{\partial n}+\epsilon_1\frac{\partial\Phi_1}{\partial n}=\sigma_f\qquad n \mbox{ is outward normal of volume 1}$$

And when $\rho_f=0$ and $\boldsymbol{\nabla}\epsilon=0$,

$$\boldsymbol{\nabla}^2\Phi=0$$

Note that if $\epsilon_2=\epsilon_1=\epsilon_o$, the boundary conditions are the same as were used previously.

## 1-D Example I.

Dielectric fills space between large parallel capacitor plates held at $\psi(x=0)=0$ and $\psi(x=d)=V_o$ and $\rho_f=0$.

Laplace's equation applies:

$$\boldsymbol{\nabla}^2\Phi=0$$

and the solution is the same as if the dielectric is not there!

$$\psi = \frac{V_o}{d}x$$

$$\mathbf{E} = -\frac{V_o}{d}\hat{\mathbf{x}}$$

What happens physically?

The battery must keep potential the same, so the electric field must not change. Polarization reduces the electric field, so extra charge must appear on plates.

On left side, consider a Gaussian cylinder with cap in conductor and cap just inside of dielectric:

$$\sigma_{f}=\mathbf{D}\cdot\hat{\mathbf{n}}=\epsilon\mathbf{E}\cdot\hat{\mathbf{n}}=\epsilon\left(-\frac{V_o}{d}\hat{\mathbf{x}}\right)\cdot(+\hat{\mathbf{x}})=-\epsilon\frac{V_o}{d}$$

$$\sigma_{f}=-\epsilon\frac{V_o}{d}=-\epsilon_o(1+\chi_e)\frac{V_o}{d}$$

$$\sigma_b=\mathbf{P}\cdot\hat{\mathbf{n}}=\epsilon_o\chi_e\mathbf{E}\cdot\hat{\mathbf{n}}$$

On the left side, normal to dielectric is in $-\hat{\mathbf{x}}$ direction.

$$\sigma_b=\epsilon_o\chi_e\mathbf{E}\cdot\hat{\mathbf{n}}=\epsilon_o\chi_e\left(-\frac{V_o}{d}\hat{\mathbf{x}}\right)\cdot(-\hat{\mathbf{x}})=+\epsilon_o\chi_e\frac{V_o}{d}$$

Checks:

1. $\sigma_b \lt \sigma_f$ at $x=0$.
2. As $\chi_e\rightarrow 0$ should get same solution as when dielectric is not there.
3. As $\chi_e\rightarrow\infty$ dielectric becomes like a conductor (can't use in this problem ...).


## 1-D Problem

1. Set up the equations that must be solved to find the potential.
2. Write down all boundary condition relationships.
3. If $\epsilon_2 \gt \epsilon_1$, sketch expected potential (Hint: Imagine 2 is a conductor).
4. Write down other checks on the solution that can be made.

## 2-D Problem I.

A long dielectric cylinder of radius $a$ is placed into a vacuum region of space with an initially uniform electric field of magnitude $E_o\hat{\mathbf{x}}$. The axis of the cylinder is parallel to the $z-$axis.

The cylinder has a dielectric constant of $\epsilon$. Find the potential everywhere.

## 2-D Problem II.

A perfect dipole $\mathbf{p}=p_o\hat{\mathbf{z}}$ at the origin is at the center of a dielectric sphere of radius $a$. The dielectric constant of the sphere is $\epsilon$.

1. For $\epsilon_r=1$, what is is the potential?
2. For $\epsilon_r\ne 1$, what is $\psi(r,\theta)$ for $r\le a$ and $r\ge a$?

(Note - this one cannot be solved using the method of images because the method of images cannot be used to find the potential for a point charge inside or outside of a dielectric. One needs to use the standard boundary value method that starts with $\sum_{l=0}^{\infty} (A_lr^l+B_l/r^{l+1})P_l(\cos\theta)$ ).

# Problems 

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

# $\mathbf{D}$ and Gauss' Law for Dielectrics

# Definition of $\mathbf{D}$ and Derivation of Gauss' Law for Dielectrics

We have shown that induced dipoles will form when an electric field exists in a dielectric. The electric field at a given location in the dielectric depends on the electric field due to all of the other dipoles and the external electric field. So, as it stands, to compute the electric field in a dielectric ... you need to know the electric field in the dielectric.

One way of resolving this is to assume that the electric field in a dielectric is reduced by a factor of what it would have been if the dielectric was not there. This is only sometimes correct and is thus about as useful as the grammar rule "i before e except after c" [https://www.washingtonpost.com/news/wonk/wp/2017/06/28/the-i-before-e-except-after-c-rule-is-a-giant-lie/?utm_term=.ea1af8b230c3].

Gauss' Law can be used to find the correct answer for certain problems (the same types of problems where it is useful for calculating the electric field - problems with symmetry that allows simplification of the integral). More generally, special techniques are needed (Boundary Value Method and the Method of Images), both of which rely of Gauss' Law for dielectrics.

We being by first defining a new quantity related to $\mathbf{E}$, the oddly named electric displacement or electric flux density<sup>*</sup>, $\mathbf{D}$, which is also called the electric flux density,

$$\mathbf{D}\equiv\epsilon_0\mathbf{E}+\mathbf{P}$$

$\mathbf{E}$ is the electric field, which is due to external electric fields and the electric field of the induced dipoles. $\mathbf{P}$ is the polarization, which depends on $\mathbf{E}$. We are combining two things that are difficult to calculate to define $\mathbf{D}$, which perhaps unexpectedly, will be easier to calculate.

We also distinguish charges among those that are due to polarization, $Q_{bound}$, and the rest, $Q_{free}$ (again, naming choice could be clearer, but is standard):

$$Q = Q_{free} + Q_{bound}$$

Next, write Gauss' Law in terms of $\mathbf{D}$, $\mathbf{P}$, $Q_{free}$, and $Q_{bound}$:

Gauss' Law is

$$\Phi_E\equiv\oint_{S} \mathbf{E}\cdot d\mathbf{a} = Q_{Inside\thinspace S}/\epsilon_0$$

substitution gives 

$$\oint_{S} (\mathbf{D}/\epsilon_0 - \mathbf{P}/\epsilon_0) \cdot d\mathbf{a} = Q_{Free\thinspace inside\thinspace S}/\epsilon_0 + Q_{Bound\thinspace inside\thinspace S}/\epsilon_0$$

simplifying

$$\oint_{S} \mathbf{D}\cdot d\mathbf{a} - \oint_{S}\mathbf{P}\cdot d\mathbf{a} = Q_{Free\thinspace inside\thinspace S}+ Q_{Bound\thinspace inside\thinspace S}$$

The second term on both sides of the equation are equal<sup>*</sup>, leaving

$$\oint_{S}\mathbf{D}\cdot d\mathbf{a} = Q_{Inside\thinspace S\thinspace free}$$

This is another form of Gauss' Law and is referred to here as Gauss' Law for dielectrics in integral form. It is also valid for non-dielectrics. In older textbooks, one often finds a discussion of electric displacement flux, $\Phi_D$

$$\Phi_D\equiv\oint_{S}\mathbf{D}\cdot d\mathbf{a} = Q_{Inside\thinspace S\thinspace free}$$

before the electric flux

$$\Phi_E\equiv\oint_{S}\mathbf{D}\cdot d\mathbf{a} = Q_{Inside\thinspace S}$$

The equation for $\Phi_D$ looks similar to that for $\Phi_E$, except that its right-hand side only refers to non-bound charges ("free charges") inside a surface and the factor of $\epsilon_0$ is missing. The equations for $\Phi_E$ and $\Phi_D$ are equally valid, but $\Phi_D$ should be used for dielectrics as it simplifies the solution. 

----
<sup>*</sup>Using $\sigma_b = \mathbf{P}\cdot\hat{\mathbf{n}}$ and $d\mathbf{a}\equiv \hat{\mathbf{n}}da$ gives

$-\oint_{S}\mathbf{P}\cdot d\mathbf{a} = -\oint_{S}\mathbf{P}\cdot \hat{\mathbf{n}}da = -\oint_{S}\sigma_bda$

$\sigma_b$ refers to charges ''on'', but not inside of, a Gaussian surface. Because we are talking about dipoles, there must be an equal an opposite number of charges just below, and so inside, the Gaussian surface. So $Q_{Bound\thinspace enclosed} = -\oint_{S}\sigma_bda$.

## Historical Origin and Units on $\mathbf{D}$

The units on electric displacement are 

$[\mathbf{D}]=\ds\frac{\mbox{Coulomb}}{\mbox{m}^2}$

whereas for electric field

$[\mathbf{E}]=\ds\frac{\mbox{Newtons}}{\mbox{Coulomb}}$

In a sense, $\mathbf{D}$ is more natural quantity with regard to its units - because the units in its denominator are $m^2$, it ''seems'' like a quantity that you would want to integrate over an area. But then this leads to the awkward question of "Flux is usually a quantity fo 'stuff' flowing through a surface". According to Gauss' Law for dielectrics, the 'stuff' has units of coulombs. But no actual charge flows through the surface?!" When the laws of electricity were being formulated, Faraday, Maxwell and others were very much influenced by the physics of fluid flow. The word "flux" means flow. In Faraday's 1837 experiment, he noted that it was if charge was induced on the outer sphere and was displaced by lines of force originating on the inner sphere. [https://docs.lib.noaa.gov/rescue/Rarebook_treasures/QC503F211839_PDF/QC503F211839v2.pdf] [https://en.wikisource.org/wiki/Page%3AA_Treatise_on_Electricity_and_Magnetism_-_Volume_1.djvu/100 First reference of Maxwell to "displacement"]

See also http://www.jpier.org/PIER/pier149/17.14092503.pdf

This is one of the many reasons why E&M is conceptually difficult. Consider Lord Kelvin's opinion: "That is why I take plain dynamics. I can get a model in plain dynamics; I cannot in electromagnetics." [http://zapatopi.net/kelvin/quotes/]. Also "I have not had a moment's peace or happiness in respect to electromagnetic theory since Nov. 28 1846." [https://books.google.com/books?id=mN0TDAAAQBAJ&lpg=PA229&ots=mlKk9PJkji&dq=Nov.%2028%201846%20Faraday%20publication&pg=PA229#v=onepage&q=Nov.%2028%201846%20Faraday%20publication&f=false]. See [https://books.google.com/books?id=kdm9nmAkKvIC&lpg=PA1015&dq=November%2028%201846%20kelvin&pg=PA1015#v=onepage&q=November%2028%201846%20kelvin&f=false] for the relevance of the date."

## Using Gauss' Law for Dielectrics

Here is how Gauss' Law has can be used to resolve the issue for certain types of problems. First, compute $\mathbf{D}$ using Gauss' Law for dielectrics. The charges in this version of the law refer to charges that we usually know about - their location and magnitude (this is the motivation for calling them "free" - we can freely, or at least more easily, modify their location and magnitude). Then, use $\mathbf{P}=\chi_e\epsilon_0\mathbf{E}$ and the definition of $\mathbf{D}$

$$\mathbf{D}\equiv\epsilon_0\mathbf{E}+\mathbf{P}=\epsilon_0\mathbf{E}+\chi_e\epsilon_0\mathbf{E}$$

and solve for $\mathbf{E}$

$$\mathbf{E}=\frac{\mathbf{D}}{\epsilon_0(1+\chi_e)}$$

Another common way of writing this is 

$$\mathbf{E}=\mathbf{D}/\epsilon$$

using the definition

$$\epsilon=\equiv\epsilon_0(1+\chi_e)$$

$$\frac{\epsilon}{\epsilon_0}=\epsilon_r\equiv(1+\chi_e)$$

They are a measure of the magnitude of the dielectric permittivity relative to the permittivity of free space.

To complicate matters, some references use dielectric constant $\kappa$ or relative permittivity $\kappa_r$ instead of $\epsilon$ and $\epsilon_r$.

## Alternative Derivations

## Problems

### Dielectric Between Sheets of Charge

An infinite non-conducting sheet in the $x=d$ plane has a charge density of $-\sigma_0$; An infinite non-conducting sheet in the $x=-d$ plane has a charge density of $+\sigma_0$, where $\sigma_0>0$. (That is, the sheet in the $x=d$ plane is negatively charged and the sheet in the $x=-d$ plane is positively charged.)

Label key points on your plots in terms of $\sigma_0, d$, and $\epsilon_0$. A diagram is given on the board.

1. Plot the electric field as a function of $x$ from $x=-2d$ to $x=+2d$. 
2. Plot the electric potential as a function of $x$ from $x=-2d$ to $x=+2d$. Set the electric potential to zero at $x=0$.

**Answer**

Each sheet produces an electric field with magnitude $\sigma_0/(2\epsilon_0)$. Electric field lines point towards negative sheet and away from the positive sheet. Because we are treating sheets are infinite, the electric field does not depend on distance from the sheet and electric field is perpendicular to the sheet. Because the sheets have equal and opposite charge, the electric field sums to zero in the regions $x<-d$ and $x>d$. Between the sheets, the electric fields add and are both in the $+\hat{\mathbf{x}}$-direction.

* $x < -d$, $\mathbf{E}=0\hat{\mathbf{x}}$
* $-d < x < -d$, $\mathbf{E}=+\sigma_0/\epsilon_0\hat{\mathbf{x}}$
* $x > d$, $\mathbf{E}=0\hat{\mathbf{x}}$

We expect the electric potential to be the highest near the positive sheet as this is the location where a positive test charge will have the highest potential energy. We are given the potential at $x=0$ - a reference potential must always be given or specified because differences in potential are what determine physical quantities of interest. We can approach this problem in two ways:

1. Ask what $V$ would give the correct $\mathbf{E}$ when we use $\mathbf{E}=-\nabla V = -\hat{\mathbf{x}}\partial V/\partial x$
2. Use $\Delta V=-\int_a^b \mathbf{E}\cdot d\mathbf{l}$

From 1., we conclude that $V$ must be linear with a negative slope of $\sigma_0/\epsilon_0$ between the sheets and it must be constant (and not necessarily zero) outside of the sheets. The given $V(0)=0$ give the intercept as $0$. The electric potential must be continuous and it does not change for $x<-d$ and $x>d$ because the electric field is zero. So for $x<-d$, the potential must be the same as it is at $x=-d$ and similar for $x>d$. These considerations give

* $x < -d$, $V=\sigma_0d/\epsilon_0$
* $-d < x < -d$, $V=-\sigma_0x/\epsilon_0$
* $x > d$, $V=-\sigma_0d/\epsilon_0$

The second approach is to use $\delta V= V(b)-V(a) = -\int_a^b \mathbf{E}\cdot d\mathbf{l}$ in the different regions. In all regions, $d\mathbf{l}=\hat{\mathbf{x}}dx$. Choosing $a=0$ and $b=x$, we have 

$\Delta V = V(b)-V(a) = V(x)-V(0)=-\int_0^x +\sigma_0/\epsilon_0\hat{\mathbf{x}}'\cdot \hat{\mathbf{x}}'dx'=-\sigma_0x/\epsilon_0$

where $\hat{\mathbf{x}}\cdot\hat{\mathbf{x}}=1$ has been used and the dummy integration variable was set to $x'$. Since $V(0)=0$, we have, $V(x)=-\sigma_0x/\epsilon_0$, which applies only to the region for which $\mathbf{E}=+\sigma_0/\epsilon_0\hat{\mathbf{x}}$. This equation can be used to find $V(d)=-\sigma_0d/\epsilon_0$ and $V(-d)=\sigma_0d/\epsilon_0$. To find the potential for $x>d$, we can use

$\Delta V=V(x)-V(d)=-\int_d^x 0\hat{\mathbf{x}}'\cdot \hat{\mathbf{x}}'dx'=0$

so that $V(x)=V(d)$ for $x>d$. Similarily, for $x<-d$

$\Delta V=V(x)-V(-d)=-\int_{-d}^x 0\hat{\mathbf{x}}'\cdot \hat{\mathbf{x}}'dx'=0$

giving $V(x)=V(-d)=\sigma_0d/\epsilon_0$.

### Dielectric Next to a Sheet of Charge

A dielectric of thickness $t$ is placed next to a sheet of charge with charge density $\sigma_o$.

As a function of distance from the sheet,

1. Plot the electric displacement, $D$
2. Plot the electric field, $E$
3. Plot the electric potential, $V$

**Answer**

We proceed as if the dielectric is not there.

Draw a Gaussian cylinder as shown in the figure. We seek to find

Left cap: $\mathbf{D}=-D\hat{\mathbf{x}}$

Right cap: $\mathbf{D}=D\hat{\mathbf{x}}$

From the diagram,

Left cap: $d\mathbf{a}=-da\hat{\mathbf{x}}$

Right cap: $d\mathbf{a}=da\hat{\mathbf{x}}$

and

$Q_{Inside\thinspace S\thinspace free}=\sigma_oA$

Gauss' Law for dielectric is

$$\oint_{S}\mathbf{D}\cdot d\mathbf{a} = Q_{Inside\thinspace S\thinspace free}$$

Expanding the surface integral into three parts gives

$$\oint_{Left\thinspace cap}\mathbf{D}\cdot d\mathbf{a}+\oint_{Right\thinspace cap}\mathbf{D}\cdot d\mathbf{a}+\oint_{Side}\mathbf{D}\cdot d\mathbf{a} = Q_{Inside\thinspace S\thinspace free}$$

Plugging in $\mathbf{D}$ and $d\mathbf{A}$ and $Q_{Inside\thinspace S\thinspace free}=\sigma_oA$ and noting that on the side, $\mathbf{D}$ is perpendicular to $d\mathbf{a}$, so their dot product is $0da$ gives

$$\oint_{Left\thinspace cap}D\hat{\mathbf{x}}\cdot da\hat{\mathbf{x}}+\oint_{Right\thinspace cap}-D\hat{\mathbf{x}}\cdot (-da\hat{\mathbf{x}})+\oint_{Side}0da = \sigma_oA$$

$D$ is constant on the caps, so it can be factored out of the integral

$$D\oint_{Left\thinspace cap}\hat{\mathbf{x}}\cdot da\hat{\mathbf{x}}+D\oint_{Right\thinspace cap}\hat{\mathbf{x}}\cdot da\hat{\mathbf{x}}+0 = \sigma_oA$$

Further simplifcation can be done by noting that $\hat{\mathbf{x}}\cdot \hat{\mathbf{x}}=1$

Leaving

$$D\oint_{Left\thinspace cap}da+D\oint_{Right\thinspace cap}da+0 = \sigma_oA$$

Integration gives

$$+DA-DA=\sigma_oA$$

Solving for $D$ gives

$$D=\sigma_o/2$$

Inserting this magnitude for $\mathbf{D}$ into the original equations gives

Left side: $\mathbf{D}=-D\hat{\mathbf{x}}=-\sigma_o/2\hat{\mathbf{x}}$

Right side: $\mathbf{D}=D\hat{\mathbf{x}}=\sigma_o/2\hat{\mathbf{x}}$

In a dielectric in general,

$$\mathbf{E}=\mathbf{D}/\epsilon$$

so that

Left side: $\mathbf{E}=\mathbf{D}/\epsilon=-\sigma_o/(2\epsilon_0)\hat{\mathbf{x}}$

Right side: $\mathbf{E}=\mathbf{D}/\epsilon=\sigma_o/(2\epsilon)\hat{\mathbf{x}}$
|}

### Dielectric Between Sheets of Charge

Label key points on your plots in terms of $\sigma_0, d,\epsilon_0$, and $t$.

An infinite linear dielectric with thickness $t$ and dielectric constant $\epsilon/\epsilon_0=\epsilon_r$ (some books use $\kappa_r$) is placed in the $x=0$ plane between the two non-conducting sheets. 

1. Plot the electric field as a function of $x$ from $x=-2d$ to $x=+2d$.
2. Plot the electric potential as a function of $x$ from $x=-2d$ to $x=+2d$. Set the electric potential to zero at $x=0$. ''Draw trends - no axis labels needed.''
3. What is the induced surface charge density on
    1. the left side of the dielectric?;
    2. the right side of the dielectric?

The electric field in the dielectric is reduced because the induced surface charges produce an electric field that opposes the external electric field.

4. What is the induced electric field in the dielectric?

**Answer**

$$D=\sigma_o\hat{\mathbf{x}}$$ for $-d<x<d$, zero otherwise.

In the dielectric,

$$\mathbf{E}=\mathbf{D}/\epsilon=(\sigma_o/(\epsilon_0\epsilon_r)\hat{\mathbf{x}}$$

* $x<-d$, $\mathbf{E}=0\hat{\mathbf{x}}$
* $-d<x<-t/2$, $\mathbf{E}=\sigma_0/\epsilon_0\hat{\mathbf{x}}$
* $-t/2<x<t/2$, $\mathbf{E}=\sigma_0/(\epsilon_r\epsilon_0)\hat{\mathbf{x}}$
* $t/2<x<d$, $\mathbf{E}=\sigma_0/\epsilon_0\hat{\mathbf{x}}$
* $x>d$, $\mathbf{E}=0\hat{\mathbf{x}}$

Potential will be highest at + sheet, constant to the left and linearly decreasing to the right. Will decrease slower in the dielectric. Must pass through zero since $V(0)=0$ given. Will be constant for $x>d$.

Gauss' Law can be used with Gaussian cylinder with one cap at $x<t/2$ and the other at $x>t/2$. Gives $\sigma_{P\thinspace Right}=\sigma_o(1-1/\epsilon_r)$. For $\epsilon_r \rightarrow \infty$, $\sigma_{P\thinspace Right}\rightarrow\sigma_o$ as expected (dielectric is like a conductor - electric field inside is zero when $\epsilon_r >> 1$. By charge conservation, $\sigma_{P\thinspace Left}=-\sigma_{P\thinspace Right}$. Induced electric field can be computed by treating surfaces of dielectric as sheets of charge so that $E_p=(\sigma_{P\thinspace Right}/(2\epsilon_0)+\sigma_{P\thinspace Left}/(2\epsilon_0)=(\sigma_o/\epsilon_0)(1-1/\epsilon_r)$.  Or, one can write

$$\mathbf{E}_o + \mathbf{E}_p = \mathbf{E}_r$$

$$\sigma_0/\epsilon_0\hat{\mathbf{x}} + \mathbf{E}_p =\sigma_0/(\epsilon_r\epsilon_0)\hat{\mathbf{x}}$$

giving

$$\mathbf{E}_p=-(\sigma_o/\epsilon_0)(1-1/\epsilon_r)\hat{\mathbf{x}}$$

Check - when $\epsilon_r\rightarrow \infty$, expect polarization field to be equal and opposite to $\mathbf{E}_o=(\sigma_o/\epsilon_0)\hat{\mathbf{x}}$.

### Dielectric Around Cylindrical Shell of Charge

A cylindrical shell with radius $a$ has a charge density $\sigma_o$ on its surface. It is surrounded by a dielectric with inner radius $a$ and outer radius $b$.

1. Draw a Gaussian cylinder with radius $\rho<a$ and use it to compute $\mathbf{D}$ for $\rho<a$
2. Draw a Gaussian cylinder with radius $a<\rho<b$ and use it to compute $\mathbf{D}$ for $a <\rho < b$
3. Compute and plot $\mathbf{D}$ versus $\rho$. Label key points on the plot.
4. Compute and plot $\mathbf{E}$ versus $\rho$. Label key points on the plot.
5. Compute and plot $V$ versus $\rho$. Label key points on the plot.

**Answer**

The Gaussian cylinders are shown in the figure. On the left end cap, $d\mathbf{a}=\pi \rho^2\hat{\mathbf{z}}$ while on the right it is $d\mathbf{a}=-\pi\rho^2\hat{\mathbf{z}}$.

Because the charged cylinder is infinite in length, for each point on the Gaussian cylinder, a charge on the left will have a charge on the right that cancels the horizontal component of $\mathbf{D}$ on the Gaussian cylinder. So $\mathbf{D}$ will only be in the $\hat{\mathbf{\rho}}$ direction.

Left cap: $\mathbf{D}=D_\rho\hat{\mathbf{\rho}}$

Right cap: $\mathbf{D}=D_\rho\hat{\mathbf{\rho}}$

Side: $\mathbf{D}=D_\rho\hat{\mathbf{\rho}}$

From the diagram,

Left cap: $d\mathbf{a}=da\hat{\mathbf{\rho}}$

Right cap: $d\mathbf{a}=da\hat{\mathbf{\rho}}$

Side: $d\mathbf{a}=2\pi\rho L\hat{\mathbf{\rho}}$

and

$Q_{Inside\thinspace S\thinspace free}=0$ when $\rho < a$

$Q_{Inside\thinspace S\thinspace free}=\sigma_o2\pi a L$ when $\rho > a$

Gauss' Law for a dielectric is

$$\oint_{S}\mathbf{D}\cdot d\mathbf{a} = Q_{Inside\thinspace S\thinspace free}$$

Expanding the surface integral into three parts gives

$$\oint_{Left\thinspace cap}\mathbf{D}\cdot d\mathbf{a}+\oint_{Right\thinspace cap}\mathbf{D}\cdot d\mathbf{a}+\oint_{Side}\mathbf{D}\cdot d\mathbf{a} = Q_{Inside\thinspace S\thinspace free}$$

Plugging in values for $\mathbf{D}$ and $d\mathbf{a}$ gives

$$\oint_{Left\thinspace cap}D_\rho\hat{\mathbf{\rho}}\cdot da\hat{\mathbf{z}}+\oint_{Right\thinspace cap} D_\rho\hat{\mathbf{\rho}}\cdot da\hat{\mathbf{z}}+\oint_{Side}D_\rho\hat{\mathbf{\rho}}\cdot da\hat{\mathbf{\rho}} = Q_{Inside\thinspace S\thinspace free}$$

The first two terms are zero because, $\hat{\mathbf{\rho}}\cdot \hat{\mathbf{z}}=0$, leaving

$$\oint_{Side}D_\rho\hat{\mathbf{\rho}}\cdot da\hat{\mathbf{\rho}} = Q_{Inside\thinspace S\thinspace free}$$

Further simplification can be done by noting that $\hat{\mathbf{\rho}}\cdot \hat{\mathbf{\rho}}=1$ and that $D_{\rho}$ is constant on the side of the Gaussian surface, leaving

$$D_\rho\oint_{Side}da =Q_{Inside\thinspace S\thinspace free}$$

The surface area of the Gaussian cylinder is $2\pi \rho L$, giving

$$D_\rho  2\pi \rho L = Q_{Inside\thinspace S\thinspace free}$$

When $\rho<a$, $Q_{Inside\thinspace S\thinspace free}=0$, so $D_\rho=0$.

When $\rho<a$, $Q_{Inside\thinspace S\thinspace free}=\sigma_o2\pi a L$, giving

$$D_\rho = \sigma_o (a/\rho)$$

Note that the units of $D_{\rho}$ are $C/m^2$, as expected.

* $\mathbf{D} =  0$ for $\rho<a$
* $\mathbf{D} =  \sigma_o (a/\rho)\hat{\mathbf{\rho}}$ for $\rho>a$

Note that we do not have a separate equation for $\mathbf{D}$ for $\rho>b$ because the amount of free charge enclosed by a Gaussian cylinder does not change as its radius is increased above $\rho=a$.

To compute the electric field in the regions, we use $\mathbf{E}=\mathbf{D}/\epsilon$, where $\epsilon$ is the dielectric constant in each region. 

* $\mathbf{E} =  0$ for $\rho<a$
* $\mathbf{E} =  (\sigma_o/\epsilon)(a/\rho)\hat{\mathbf{\rho}}$ for $a < \rho < b $
* $\mathbf{E} =  (\sigma_o/\epsilon_0)(a/\rho)\hat{\mathbf{\rho}}$ for $\rho > b$

Note that the electric field "jumps" at each location that there is a free charge or a polarization charge, e.g., $\rho=a$ and $\rho=b$. This is expected - think about moving from one side of a sheet of charge to the other. The change in $\mathbf{E}$ is $\sigma_o/\epsilon_0$ (from -$\sigma_o/\epsilon_0\hat{\mathbf{x}}$ to $+\sigma_o/\epsilon_0\hat{\mathbf{x}}$).

To compute the electric potential, we first choose $V=0$ at $\rho=0$. The electric field is zero from $\rho=0$ to $\rho=a$, so the potential does not change in this range.

$$\Delta V = V_{final}-V_{initial} = -\int_{initial}^{final} \mathbf{E}\cdot d\mathbf{l}$$

Although the change in potential from an initial location to a final location does not depend on path, we choose the most direct path as it reduces the amount of calculation. The direct path is with $d\mathbf{l}=d\rho\hat{\mathbf{\rho}}$. The equation for potential is found by setting the initial location as a location where we know the potential and the final location as a variable:

For $a < \rho < b$, $\sigma_o/\epsilon)(a/\rho)\hat{\mathbf{\rho}}$ and $V(a)=0$

$$\Delta V = V(\rho)-V(a) = -\int_{a}^{\rho} (\sigma_o/\epsilon)(a/\rho')\hat{\mathbf{\rho}}'\cdot d\rho\hat{\mathbf{\rho}}'$$

which simplifies to

$$V(\rho)= -(\sigma_oa/\epsilon)\int_{a}^{\rho} d\rho'/\rho'=-(\sigma_oa/\epsilon)\ln(\rho/a)=(\sigma_oa/\epsilon)\ln(a/\rho)$$

To compute the $V$ for $\rho>b$, we need the potential at $\rho=b$, which is found by plugging this into the above equation

$$V(b)=(\sigma_oa/\epsilon)\ln(a/b)$$

For $a < \rho < b$, $(\sigma_o/\epsilon_0)(a/\rho)\hat{\mathbf{\rho}}$

$$V(\rho)-V(b) = -\int_{b}^{\rho} (\sigma_o/\epsilon_0)(a/\rho')\hat{\mathbf{\rho}}'\cdot d\rho\hat{\mathbf{\rho}}'$$

$$V(\rho)-(\sigma_oa/\epsilon)\ln(a/b) = (\sigma_oa/\epsilon_0)\ln(b/\rho)$$

$$V(\rho) = (\sigma_oa/\epsilon_0)\ln(b/\rho)+(\sigma_oa/\epsilon)\ln(a/b)$$

In summary,

* $V(\rho) = 0$ for $\rho < a$
* $V(\rho) = (\sigma_oa/\epsilon)\ln(a/\rho)$ for $a < \rho < b$
* $V(\rho) = (\sigma_oa/\epsilon_0)\ln(b/\rho)+(\sigma_oa/\epsilon)\ln(a/b)$ for $\rho>b$

It may not be obvious how to plot these lines, but the task is simplified by noting that $V$ must be continuous and decreasing as one moves away from the charged cylinder. This is enough information to start a sketch. Note that one often sets the potential to zero at infinity. With a cylinder that is infinite in length, the potential is infinite at infinity. A similar issue occurs with infinite sheets of charge.

### Dielectric Around Line of Charge

### Dielectrics Around Shell of Charge

A spherical shell of radius $a$ has a free surface density of $\sigma_0$ and is centered at the origin.

The shell is surrounded by a spherical dielectric with a dielectric constant $\epsilon_1=2\epsilon_0$, inner radius $a$, and outer radius $2a$. Use Gauss' Law for Dielectrics to

1. Find equations for the electric field as a function of $r$.
2. Plot the electric field as a function of $r$. Label important locations.
3. Compute the bound polarization charge on the inner and outer surface of the dielectric.

(Above question is identical to HW problem except for part for computing potential has been removed and I have given a value for $\epsilon_1$)

A spherical shell of radius $2a$ and a free surface density of $-\sigma_0$ is then placed around the dielectric.

4. Plot the electric field as a function of $r$. Label important locations. You do not need to show your work.

**Answer**

$$\oint_{S}\mathbf{D}\cdot d\mathbf{a} = Q_{Inside\thinspace S\thinspace free}$$

* $\mathbf{D}=0$ for $r<a$
* $\mathbf{D}=\sigma_0(a^2/r^2)\hat{\mathbf{r}}$ for $r>a$

$$\mathbf{E}=\mathbf{D}/\epsilon$$

* $\mathbf{E}=0$ for $r<a$
* $\mathbf{E}=(\sigma_0/\epsilon_1)(a^2/r^2)\hat{\mathbf{r}}=(\sigma_0/(2\epsilon_0))(a^2/r^2)\hat{\mathbf{r}}$ for $a<r<2a$
* $\mathbf{E}=(\sigma_0/\epsilon_0)(a^2/r^2)\hat{\mathbf{r}}$ for $r>2a$

Curve for $a<r<2a$ starts at $\sigma_0/(2\epsilon_0)$ and ends at $\sigma_0/(8\epsilon_0)$

Curve for $r>2a$ starts at $\sigma_0/(4\epsilon_0)$ and ends at 0.

Note that $\epsilon_1=2\epsilon_0$ implies $\epsilon_r=2$.

$$\sigma_b=\mathbf{P}\cdot\hat{\mathbf{n}}$$

and 

$$\mathbf{P} = \epsilon_0\chi_e\mathbf{E}=\epsilon_0(\epsilon_r-1)\mathbf{E}$$

where $\epsilon_r=\epsilon/\epsilon_0$ so that

$$\sigma_b=\epsilon_0(\epsilon_r-1)\mathbf{E}\cdot\hat{\mathbf{n}}$$

Normal to surface points outwards from volume, so at $r=a$, $\hat{\mathbf{n}}=-\hat{\mathbf{r}}$ and at $r=b$, $\hat{\mathbf{n}}=\hat{\mathbf{r}}$.

Inner surface at $r=a$, $\mathbf{E}=(\sigma_0/\epsilon_1)(a^2/a^2)\hat{\mathbf{r}}$, so

$\sigma_b=\epsilon_0(\epsilon_r-1)(\sigma_0/\epsilon_1)(a^2/a^2)\hat{\mathbf{r}}\cdot(-\hat{\mathbf{r}})=-\sigma_0/2$

Outer surface at $r=b$, $\mathbf{E}=(\sigma_0/\epsilon_1)(a^2/(2a)^2)\hat{\mathbf{r}}$, so

$\sigma_b=\epsilon_0(\epsilon_r-1)(\sigma_0/\epsilon_1)(a^2/(2a)^2)\hat{\mathbf{r}}\cdot\hat{\mathbf{r}}=\sigma_0/8$

Check answers using Gauss' Law 

$$\oint_{S} \mathbf{E}\cdot d\mathbf{a} = Q_{Inside\thinspace S}/\epsilon_0$$

with the computed bound charges included in $Q_{Inside\thinspace S}$ and the computed values of $\mathbf{E}$ for each region. Draw a Gaussian sphere in dielectric and then outside of dielectric and verify that Gauss' Law is satisfied for both cases.

When outer shell is added, only modification is for $r>2a$

$$\oint_{S}\mathbf{D}\cdot d\mathbf{a} = Q_{Inside\thinspace S\thinspace free}$$

The free charges are on the surfaces at $r=a$ and $r=2a$, 

$$Q_{Inside\thinspace S\thinspace free}=4\pi a^2 \sigma_0 - 4\pi (2a)^2 \sigma_0 = -12\pi\sigma_0$$

so that

$$\mathbf{D}=-3\sigma_0(a^2/r^2)\hat{\mathbf{r}}$$

$$\mathbf{E}=-3(\sigma_0/\epsilon_0)(a^2/r^2)\hat{\mathbf{r}}$$

Note that I accepted $\mathbf{E}=0$ as an answer in case you were assuming that the charge on the outer shell equaled the charge on the inner shell, which is a common type of problem and easy to miss if you are working quickly.

### Dielectrics Around Sphere of Charge

A solid sphere of charge with radius $a$ and uniform charge density $\rho_o$ is surrounded by three materials, each with a different permittivity. A cross-section of the sphere is shown.

1. Compute and plot $E(r)$.
2. Compute $V(2a)-V(a)$.
3. Compute all bound surface charge densities, $\sigma_b$.
4. Compute all bound volume charge densities, $\rho_b$.

Write all of your answers and label your plot at appropriate points in terms of $\rho_o, \epsilon_o,$ and $a$.

**Answer**

$D$ and $E$ are in $\hat{\mathbf{r}}$ direction.
* $\mathbf{D}=\rho_o (4/3)\pi r^3/(4\pi r^2)$ for $r<a$
* $\mathbf{D}=\rho_o (4/3)\pi a^3/(4\pi r^2)$ for $r>a$

* $\mathbf{E} =(\rho_o/\epsilon_o) (4/3)\pi r^3/(4\pi r^2)\hat{\mathbf{r}}=E_o(r/a)\hat{\mathbf{r}}$ for $r<a$ 
* $\mathbf{E} =(\rho_o/2\epsilon_o) (4/3)\pi a^3/(4\pi r^2)\hat{\mathbf{r}}=(E_o/2)(a^2/r^2)\hat{\mathbf{r}}$ for $a<r<2a$ 
* $\mathbf{E} =(\rho_o/\epsilon_o) (4/3)\pi a^3/(4\pi r^2)\hat{\mathbf{r}}=(E_o)(a^2/r^2)\hat{\mathbf{r}}$ for $2a<r<3a$ 
* $\mathbf{E} =(\rho_o/4\epsilon_o) (4/3)\pi a^3/(4\pi r^2)\hat{\mathbf{r}}=(E_o/4)(a^2/r^2)\hat{\mathbf{r}}$ for $3a<r<4a$ 
* $\mathbf{E} =(\rho_o/\epsilon_o) (4/3)\pi a^3/(4\pi r^2)\hat{\mathbf{r}}=E_o(a^2/r^2)\hat{\mathbf{r}}$ for $r>4a$ 

where $E_o \equiv (\rho_oa/3\epsilon_o)$.

* $V(2a)-V(a) = -\int^{2a}_{a} (\rho_o/2\epsilon_o)\rho_o (4/3)\pi a^3/(4\pi r^2) dr=-E_oa/4$

$\mathbf{P}=\epsilon_o \chi_e \mathbf{E} = \epsilon_o (\epsilon/\epsilon_o-1) \mathbf{E}$

$\sigma_b=\mathbf{P}\cdot\hat{\mathbf{n}}$

At $r=a$, $\hat{\mathbf{n}}$ = -$\hat{\mathbf{r}}$ (normal on inside of $2\epsilon_o$ surface is inward) and $\mathbf{E} =E_o/2\hat{\mathbf{r}}$

At $r=2a$, $\hat{\mathbf{n}}$ = $\hat{\mathbf{r}}$ (normal on outside of $2\epsilon_o$ surface is outward) and $\mathbf{E} = E_o/8\hat{\mathbf{r}}$

At $r=3a$, $\hat{\mathbf{n}}$ = -$\hat{\mathbf{r}}$ (normal on inside of $4\epsilon_o$ surface is inward) and $\mathbf{E} =E_o/36\hat{\mathbf{r}}$

At $r=4a$, $\hat{\mathbf{n}}$ = $\hat{\mathbf{r}}$ (normal on outside of $4\epsilon_o$ surface is outward) and $\mathbf{E} =E_o/64\hat{\mathbf{r}}$

$\rho_b=-\nabla\cdot\mathbf{P}$

Inside of $2\epsilon_o$ and $4\epsilon_o$ dielectrics, $\mathbf{E} = (const) \hat{\mathbf{r}}/r^2$. This is the same form of the field for a point charge, which has zero divergence (except for $r=0$. So $\rho_b=0$. Can also show this using the given equation (replacing $A$ with $E$)

$$\nabla\cdot\mathbf{E}={1 \over r^2}{\partial \left( r^2 E_r \right) \over \partial r} + {1 \over r\sin\theta}{\partial \over \partial \theta} \left(  E_\theta\sin\theta \right) + {1 \over r\sin\theta}{\partial E_\phi \over \partial \phi}$$

$E_{\theta}=E_{\phi}=0$ so the second and third terms are zero. $E_r = (const)/r^2$ in the two dielectrics so $r^2 E_r = (const)$ and $ {\partial \left( r^2 E_r \right) / \partial r} = 0$.

To check your answers, you can use Gauss' Law with a surface inside each of the regions (using bound surface charges + free surface charges when computing $Q_{enclosed}$ and check that you get the same electric field.

[[Image:sphere.png|400px]]

### Dielectrics around a Point Charge

A positive point charge is at the origin. Three spherical dielectrics are also centered on the origin. They have

1. Inner radius $a$, outer radius $2a$, and $\epsilon=2\epsilon_o$
2. Inner radius $2a$, outer radius $3a$, and $\epsilon=4\epsilon_o$
3. Inner radius $3a$, outer radius $4a$, and $\epsilon=2\epsilon_o$

Sketch the electric field as a function of distance from the origin. You do not need to add labels for amplitudes on the electric field axis.

[[Image:Dielectric2.png|300px]]

### Dielectric Between Spherical Shells of Charge

### General Rule for Computing $\mathbf{E}$?

You may find after solving a few dielectric problems using Gauss' Law that it seems as if the electric field in the dielectric is always simply $\mathbf{E}_{in\thinspace dielectric}=\mathbf{E}_o/\epsilon_r$, where $\mathbf{E}_o$ is the electric field that would exist if the dielectric was not there.

For elementary problems involving dielectrics, this is often true. For example:

1. One or more large square dielectrics between two large sheets of charge
2. One or more large square dielectrics between two large capacitor plates '''after''' they are disconnected from a battery (so problem is equivalent to 1.) 
3. 1. and 2. for one or more dielectrics between two co-aligned and long cylindrical shells
4. 1. and 2. for one or more dielectrics between two co-aligned and spherical shells

Incidentally, 1.-4. are all problems for which Gauss' Law for dielectrics can be used to find $\mathbf{D}$ and $\mathbf{E}$.
 
In general, however, $\mathbf{E}_{in\thinspace dielectric}\ne\mathbf{E}_o/\epsilon_r$. Two examples:

1. A large square dielectric between large capacitor plates that are held at a constant potential, $V_o$. The presence of the dielectric causes the amount of charge on the capacitor plates to increase. The electric field in the dielectric is $\mathbf{E}_o/?$ and not $\mathbf{E}_o/\epsilon$, where $E_o=V_o/d$ is the electric field that existed before. This problem is covered in the section on capacitors with dielectrics.

2. A spherical dielectric in a constant electric field, $\mathbf{E}_o$. In this situation, the induced polarization adds up in a way so that the net electric field is $\mathbf{E}_o/?$ instead of $\mathbf{E}_o/\epsilon$ inside the dielectric. This problem is covered in the section on boundary value problems with dielectrics.

