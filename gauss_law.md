# Introduction

## Integral Form

Gauss's law states that the integral of electric flux, $\Phi_E$ over a closed surface, $\mathcal{A}$, is related to the amount of charge inside the surface according to

$$\Phi_E\equiv\oint_{\mathcal{A}} \mathbf{E}\cdot d\mathbf{A} = \frac{Q_{\text{Inside }\mathcal{A}}}{\epsilon_0}$$

To simplify notation, $Q_{Inside\text{ }\mathcal{A}}$ is usually written as $Q_{encl}$ and often the $\mathcal{A}$ is dropped:

$$\boxed{\oint \mathbf{E}\cdot d\mathbf{A} = \frac{Q_{encl}}{\epsilon_0}}$$

This equation is also known as Gauss's law in integral form.


## Problem

1. A point charge $q$ is placed outside of a spherical shell.  What is the electric flux through its surface due to the point charge?
2. A point charge is placed at the center of a spherical shell. What is the electric flux through the shell's surface due to the point charge?
3. A point charge is placed just inside a spherical shell.
   1. What is the electric flux through the shell's surface?
   2. Is the electric field magnitude constant on the surface of the shell?

Justify your answers.

%**Answer**
%1. Zero.  
%2. $q/\epsilon_0$%

%   The answer for 1. and 2. follow from Gauss' Law in integral form: $\Phi_E = \oint \mathbf{E}\cdot d\mathbf{A} = Q_{encl}/\epsilon_0$. In both cases, $q$ is the total charge inside of the surface on which we want to know the electric flux, $\Phi_E$. The integral would be difficult to compute for 2.
%3. &nbsp;
%   1. $q/\epsilon_0$. We can think of flux as proportional to the number of field lines that pass through a surface.  Lines going in provide negative flux, lines out positive.  If you draw field lines due to a point charge through a closed surface that does not enclose the point charge, all of the point charge's field lines going into the surface must exit.
%   2. Note that in cases 1. and 3., Gauss' Law would not be useful for computing the electric field. Gauss' Law is useful for computing the electric field when it is constant or zero on a Gaussian surface, and its angle with respect to the surface normal is constant, in which case it can be factored out of the integral.

## Problem

If a Gaussian sphere is drawn such that there is no charge enclosed, does it follow that $\mathbf{E}=0$ on the surface of the sphere? Justify your answer.

**Answer**

No. All we can say is that $\oint \mathbf{E}\cdot d\mathbf{A}=0$. There are two ways for this to be true:
1. $\mathbf{E}=0$ everwhere on the surface and
2. $\mathbf{E}\cdot \hat{\mathbf{n}}$ varies over the surface in such a way that when summed over all differential areas, it is zero. 

> A common error in Gauss's law problems is the claim that $Q_{encl}=0$ implies $\mathbf{E}=0$. This is not always true.

## Problem

A point charge is located at $z=b$. Consider a Gaussian sphere centered on the origin with a radius of $b/2$. The point charge is outside of the sphere, so $Q_{encl}=0$. Does it follow that $\mathbf{E}=0$ on the surface of the Gaussian sphere? If not, what can you say about $\mathbf{E}$ on the surface of the Gaussian sphere?

## Problem

The electric field was measured by placing a lump of charge in a cubical cardboard box of side length 1 meter and measuring the electric field at the center of each face of the box. The measurements of the electric field for each face (in mV/m) are shown below.

```
Face #     Ex       Ey      Ez
  1
  2
  3
  4
  5
  6
```

Estimate the charge inside of the box.

## Differential Form

Gauss's law in differential form relates the divergence of the vector field $\mathbf{E}$ at anly location in space to the charge density, $\rho$, at that location:

$$\boxed{\boldsymbol{\nabla}\bfcdot \mathbf{E} = \frac{\rho}{\epsilon_o}}$$

It is important to remember that both $\mathbf{E}$ and $\rho$ in general depend on position, which can be emphasized by writing $\mathbf{E}$ and $\rho$ with argument of $x,y,z$ or, more generally, $\mathbf{r}$, so that there is no reference to a coordinate system:

$${\boldsymbol{\nabla}\bfcdot \mathbf{E}(\mathbf{r}) = \frac{\rho(\mathbf{r})}{\epsilon_o}}$$

Gauss's law in integral form states that one can find the charge density at any point in space by computing the divergence of $\mathbf{E}$ at that point.

### Derivation

Starting with Gauss's law

$$\oint \mathbf{E}\cdot d\mathbf{A} = \frac{Q_{encl}}{\epsilon_0}$$

rewrite $Q_{enc}$ in terms of an integral over the volume enclosed by the closed surface associated with the flux. This gives

$$\oint \mathbf{E}\cdot d\mathbf{A} = \frac{1}{\epsilon_0}\int \rho d\tau$$

From the [divergence theorem](divergence.html), the left--hand side can be written as

$$\int(\boldsymbol{\nabla}\bfcdot \mathbf{E}) d\tau = \frac{1}{\epsilon_0}\int \rho d\tau$$

This can be written as

$$\int \left(\boldsymbol{\nabla}\bfcdot\mathbf{E} - \frac{\rho}{\epsilon_0} \right)d\tau = 0$$

This equation applies to an arbitrary volume. Suppose there is a volume for which the integrand is positive in a subvolume. The integral can be zero if the contribution to the integral for the rest of the volume is opposite in value. However, because the volume is arbitrary, the integral must also apply to the subvolume. As a result, we conclude that the integrand must always be zero. Another way of looking at this is to consider an arbitrary infinitesimal volume $\Delta \tau$. As $\Delta \tau \rightarrow 0$, the equation approaches $\left(\boldsymbol{\nabla}\bfcdot\mathbf{E} - {\rho}/{\epsilon_0} \right)\Delta \tau=0$. To be true, for all $\Delta \tau$, $\boldsymbol{\nabla}\bfcdot\mathbf{E} = {\rho}/{\epsilon_0}$ is required.

# Partial Proof of Gauss's Law in Integral Form

In this section, we only consider the start and end of the proof of Gauss's law in integral form. It is not important for you to be able to derive the part of the proof that was omitted. However, you should have a general understanding of the approach needed for the omitted part of the derivation based on the discussion given in the [notes on Flux](flux.html).

Consider a charge $q_{origin}$ at the origin and a Gaussian surface of a spherical shell of radius $R$ centered on the origin. Gauss's law is then

$$\Phi_E = \oint_{SS}\mathbf{E}\cdot d\mathbf{A}=\frac{q_{origin}}{\epsilon_o}$$

For this surface, $d\mathbf{A}=R^2\sin\theta d\theta d\phi \mathbf{\hat{r}}$ and the field on the surface is $\mathbf{E}=kq_{origin}\mathbf{\hat{r}}/R^2$. Subtitution gives

\begin{aligned}
\displaystyle\oint_{SS}\mathbf{E}\cdot d\mathbf{A} = & kq_{origin}\int_{\phi=0}^{2\pi}\int_{\theta=0}^\pi \frac{\mathbf{\hat{r}}}{R^2}\bfcdot (R^2\sin\theta d\theta d\phi \mathbf{\hat{r}})\\\\
=& kq_{origin}\int_{\phi=0}^{2\pi}\int_{\theta=0}^\pi \sin\theta d\theta d\phi\\\\
=& kq_{origin}4\pi\\\\
=& \frac{q_{origin}}{\epsilon_o}
\end{aligned}

Where $k=1/4\pi\epsilon_o$ was used in the last step.
## Problem

In another universe, the electric field created by a charge $q$ at the origin is found to be $\mathbf{E} = k'q\hat{\mathbf{r}}/r^3$, where $k'$ is a constant with appropriate units.

Is Gauss's law valid in this universe?

----

At this point, we have not proven the general equation, only a special case. To complete the proof, we would proceed by

1. Considering a charge inside of a spherical surface but not at the origin.
2. Considering a charge outside of a spherical surface.
3. Considering the previous two cases for an arbitrary surface.

To do this, one could apply arguments for Approach II used in the [notes on Flux](flux.html#through-a-closed-line). (One would need to generalize these arguments to apply to a closed surface instead of a closed line.)

Once the proof is complete for a single point charge inside an arbitrary closed surface and outside of an arbitrary closed surface, there is one final step of generalization to an arbitrary number of charges. This step only requires the use of superposition.

Assuming that we have shown that the electric field $\mathbf{E}\_{1i}$ due a single point charge $q_{1i}$ inside of an arbitrary closed surface satisfies the relationship

$$\oint \mathbf{E}\_{q_{1i}}\cdot d\mathbf{A} = \frac{q_{1i}}{\epsilon_0}$$

we can apply this to another point charge inside of the surface by simply changing the subscript:

$$\oint \mathbf{E}\_{q_{2i}}\cdot d\mathbf{A} = \frac{q\_{2i}}{\epsilon_0}$$

These two equations can be combined to be

$$\oint \mathbf{E}\_{q_{1i}}\cdot d\mathbf{A} + \oint \mathbf{E}\_{q_{2i}}\cdot d\mathbf{A} = \frac{q_{1i}}{\epsilon_0} + \frac{q\_{2i}}{\epsilon_0}$$

By superposition, the total electric field is $\mathbf{E}\_I=\mathbf{E}\_{q\_{1i}}+\mathbf{E}\_{q\_{2i}}$. As a result, it follows that

$$\oint \mathbf{E}\_I\cdot d\mathbf{A} = \frac{q_{1i}+q_{2i}}{\epsilon_0}$$

This argument can be repeated for an arbitrary of number of charges inside of a volume, giving

$$\oint \mathbf{E}\_I\cdot d\mathbf{A} = \frac{q_{1i}+q_{2i}+...}{\epsilon_0}$$

To finish the proof, assume that we have shown that for a single point charge $q_{1o}$ outside of a closed surface that

$$\oint \mathbf{E}\_{q\_{1o}}\cdot d\mathbf{A} = 0$$

This applies to another charge outside of the same closed surface

$$\oint \mathbf{E}\_{q\_{2o}}\cdot d\mathbf{A} = 0$$

So by superposition, the electric field $\mathbf{E}\_O=\mathbf{E}\_{1o}+\mathbf{E}\_{2o}$ due to all charges outside of the surface is

$$\oint \mathbf{E}_O\cdot d\mathbf{A} = 0$$

Finally, combine the two equations

$$\oint \mathbf{E}\_I\cdot d\mathbf{A} = \frac{q_{1i}+q_{2i}+...}{\epsilon_0}$$

$$\oint \mathbf{E}\_O\cdot d\mathbf{A} = \frac{q_{1i}+q_{2i}+...}{\epsilon_0}$$

to give

$$\oint \mathbf{E}\_I\cdot d\mathbf{A} + \oint \mathbf{E}\_O\cdot d\mathbf{A} = \frac{Q_i}{\epsilon_o}$$

Finally, we can use superposition to state that the total electric field, $\mathbf{E}$, is the sum of the electric field due to charges inside with the electric field due to charges outside the sphere. That is, $\mathbf{E}=\mathbf{E}_I+\mathbf{E}_O$. As a result

$$\oint \mathbf{E}\cdot d\mathbf{A} = \frac{q_{1i}+q_{2i}+...}{\epsilon_0}=\frac{Q_{encl}}{\epsilon_o}$$

# Using -- Charges on an Insulator

By insulator, we mean that the charges are fixed. Insulator and non--conductor mean the same thing.

In Gauss' Law, the electric field is inside of an integral:

$$\oint \mathbf{E}\cdot d\mathbf{A} = \frac{Q_{encl}}{\epsilon_0}$$

As a result, using it to find the electric field for a collection of charges would seem more difficult than using Coulomb's law, for which the electric field is written explicitly as

$$\displaystyle \mathbf{E}=\int  \frac{\hat{\textbf{\char"0509}}}{\char"0509^2}\lambda dl
\qquad
\displaystyle \mathbf{E}=\int  \frac{\hat{\textbf{\char"0509}}}{\char"0509^2}\sigma dA
\qquad
\displaystyle \mathbf{E}=\int  \frac{\hat{\textbf{\char"0509}}}{\char"0509^2}\rho d\tau
$$

for charges on a line, on a surface, or in a volume, respectively.


In general, Coulomb's law can always be used to compute $\mathbf{E}$ if the charge density is known. However, there is a certain class of problems for which using Gauss's law is much easier than using Coulomb's law.

> When a symmetry argument can be made for why
>
> 1. $|\mathbf{E}|$ is constant or zero on a closed surface and
> 2. why the angle between $\mathbf{E}$ and $d\mathbf{A}$ is constant on the part of the closed surface for which $|\mathbf{E}|$ is not zero,
>
> then Gauss's law can be used to easily find **the magnitude** of an electric field on a surface. **The direction** of the field is determined by a symmetry argument.

The location and charge distributions for which symmetry + Gauss's law can be used to find $\mathbf{E}$ includes

* near the center of a long and uniformly charged line;
* near the center of a long and uniformly charged cylindrical shell;
* near the center of a long and uniformly charged solid cylinder for which the density only varies with radius;
* near the center of a large and uniformly charged flat sheet (of any shape);
* at any location for a uniformly charged spherical shell;
* at any location for charged sphere for which the density only varies with radius;
* just outside of _any_ conductor, even if the charge density is not uniform on the surface (we will use Gauss's law to show that all of the charge on a conductor must be on its surface); and
* at any point inside a conductor with _any_ shape and any surface charge density.

Gauss' law is also useful when one can find a surface on which the electric field is always zero -- in this case, one can conclude the amount of charge inside the surface is zero. Finally, Gauss' Law is useful if you are given the electric field on a surface and want to calculate the amount of charge enclosed.

There are three equally important steps to using Gauss's law

1. The symmetry argument
2. Computing $\Phi_E$
3. Computing $Q_{encl}$

Because there are only a few problems for which Gauss's law can be used, the symmetry argument is often forgotten. In the following, I emphasize the symmetry argument and provide an explicit justification for each of the calculations made in the three steps above. On homeworks and exams, I am interested in knowing that you understood the justifications for the steps. It is quite easy to get the correct answer for Gauss's law problems without really understanding the justifications and just writing one or two unjustified equations that are consistent with the answer.

## Common Error

A common usage error is to draw a Gaussian surface that has no net charge inside of it and conclude that the electric field is zero on the surface. Without any other information, if the net charge inside a surface is zero, you can only conclude the electric flux, $\Phi_E$ is zero.

## Problem -- Field Due to Point Charge

To compute the electric flux for a point charge at the origin using the integral equation for Gauss' Law, the following steps are made

$$\oint \mathbf{E}\cdot d\mathbf{A} = \oint |\mathbf{E}|dA = |\mathbf{E}|\oint dA = |\mathbf{E}|4\pi r^2$$

Justify each step and explain all terms.  Provide a diagram.

**Answer**

1. Assuming that the Gaussian surface is the surface of a sphere of radius $r$ centered on the origin, $\oint \mathbf{E}\cdot d\mathbf{A} =  \oint |\mathbf{E}|dA$ because $\mathbf{E}$ and $d\mathbf{A}$ are parallel on the Gaussian surface. This will only be true of the Gaussian sphere is centered on the charge.
2. $\oint |\mathbf{E}|dA = |\mathbf{E}|\oint dA$ because $|\mathbf{E}|$ is constant on the Gaussian surface.
3. $|\mathbf{E}|\oint dA = |\mathbf{E}|4\pi r^2$ - The surface area of a sphere of radius $r$ $4\pi r^2$.

## Problem -- General Equation

Is the following a valid equation for Gauss's law?

$$\int \mathbf{E}\cdot d\mathbf{A} = \frac{Q_{encl}}{\epsilon_0}$$

Justify your answer.

## Example -- Long Line of Charge

In a previous homework, the electric field due to a long line of charge was considered. An argument was made for why the field only has a vertical component on a line centered on and perpendicular to the charged line.

Consider a Gaussian cylinder as shown on the left of the following figure.

<img src="figures/Gauss_Law_Line_of_Charge.svg"/>

The electric field vectors at a few points on the Gaussian surface are also shown on the right, which is a side view of the image on the left. It would seem that this Gaussian surface does not satisfy the constraint of "$|\mathbf{E}|$ is constant or zero on all surfaces, and the angle between $\mathbf{E}$ and $d\mathbf{A}$ is constant on a surface".

However, consider what happens when we make the line very long (or equivalently, shrink the Gaussian surface). The field lines in the region of the Gaussian surface become more and more vertical. Based on this, we can state that the electric field must have the form

$\mathbf{E}=E_s(s)\hat{\mathbf{s}}$

in the region of the Gaussian cylinder. Thus, symmetry has told us that although the general equation for the electric field has the form

$\mathbf{E}(s,\phi,z)=E_s(s,\phi,z)\hat{\mathbf{s}}+E_\phi(s,\phi,z)\boldsymbol{\hat{\phi}}+E_z(s,\phi,z)\zhat$

At this point, we only know that $\mathbf{E}$ will only have an $\hat{\mathbf{s}}$ component and can only possibly depend only on $s$.

$\mathbf{E}(s)=E_s(s)\hat{\mathbf{s}}$

The next step is to do the surface integral, which can be split into three parts: 

$\displaystyle \oint \mathbf{E}\cdot d\mathbf{A} = \int_{\text{Right cap}} \mkern-36mu\mathbf{E}\bfcdot d\mathbf{A} + \int_{\text{Left cap}}\mkern-30mu\mathbf{E}\bfcdot d\mathbf{A} + \int_{\text{Curved surface}}\mkern-60mu\mathbf{E}\bfcdot d\mathbf{A}$

On each surface, $d\mathbf{A}$ is different.

1. Right cap, for which $d\mathbf{A}=s'ds'd\phi\hat{\mathbf{z}}$
2. Left cap, for which $d\mathbf{A}=-s'ds'd\phi\hat{\mathbf{z}}$
3. Curved surface, for which $d\mathbf{A}=sd\phi dz\hat{\mathbf{s}}$

The dot products $\mathbf{E}\cdot d\mathbf{A}$ for each integrals are
1. Right cap: $E_s(s)\hat{\mathbf{s}}\bfcdot (s'ds'd\phi\hat{\mathbf{z}})=0$ because $\hat{\mathbf{s}}$ is perpendicular to $\zhat$.
2. Left cap: $E_s(s)\hat{\mathbf{s}}\bfcdot (-s'ds'd\phi\hat{\mathbf{z}})=0$ because $\hat{\mathbf{s}}$ is perpendicular to $\zhat$.
3. Curved surface: $E_s(s)\hat{\mathbf{s}}\bfcdot sd\phi dz\hat{\mathbf{s}}=E_s(s) s d\phi dz$

As argued above, the integrand for the first two integrals are zero, so we are left with

$\displaystyle \oint\mathbf{E}\cdot d\mathbf{A} = \int_{\text{Curv surface}}\mkern-60mu\mathbf{E}\bfcdot d\mathbf{A}$

The electric field is constant on the curved surface, so integration is not needed. The area of the curved surface is $2\pi s h$ and so

$\displaystyle\int_{\text{Curved surface}}\mkern-60mu\mathbf{E}\bfcdot d\mathbf{A}=E_s(s)2\pi s h$

The charge enclosed in the cylinder is

$Q_{encl}=\lambda_o h$

Using Gauss's law, we can equate the flux the curved surface and $Q_{encl}/\epsilon_o$:

$\displaystyle E_s(s)2\pi s h = \frac{\lambda_o h}{\epsilon_o}$

And so

$\displaystyle E_s(s) = \frac{\lambda_o}{2\pi\epsilon_o}\frac{1}{s}$

We are not done. The problem asked for $\mathbf{E}$. Using symmetry arguments, we concluded that $\mathbf{E}$ must have the form

$\displaystyle \mathbf{E}(s)=E_s(s)\hat{\mathbf{s}}$

So combining the symmetry argument equation with the result of Gauss's law gives

$\displaystyle\mathbf{E}(s) = \frac{\lambda_o}{2\pi\epsilon_o}\frac{\hat{\mathbf{s}}}{s}$

To be technically correct, we should also state that this result is valid only in the limit that the length of the line approaches infinity, or equivalently, at locations near the center of a finite line of charge at a radial distance from the center that approaches zero.

## Example -- Long Line of Charge Alt. Version

In general, in cylindrical coordinates, the electric field has the form

$$\mathbf{E}(s,\phi,z)=E_s(s,\phi,z)\hat{\mathbf{s}}+E_{\phi}(s,\phi,z)\hat{\boldsymbol{\phi}}+E_z(s,\phi,z)\hat{\mathbf{z}}$$

where $s$ is the radial coordinate in cylindrical coordinates.

Consider an infinite line of charge with a uniform charge per unit length of $\lambda_o$ on the $z$-axis. The typical approach to finding that the equation for the electric field is

$$\mathbf{E}(s)=\frac{\lambda_o}{2\pi\epsilon_o}\frac{\hat{\mathbf{s}}}{s}$$

is to use a cylindrical Gaussian surface and Gauss' law. When using Gauss' law, one must make arguments for why

1. $E_s$ does not depend on $\phi$ and $z$

2. $E_z=0$

With these two justifications and Gauss' law, one arrives at only an equation for the radial component of the electric field, $E_s$. To complete the solution, one also needs to provide an argument for why 

3. $E_{\phi}=0$.

Derive the equation given above for the electric field using Gauss' law and explicitly state arguments for 1.-3.

**Solution**

I gave this problem because I have come to realize that students can use Gauss' law to find the electric field, but can't often answer conceptual questions about justifications for the steps needed to get the solution. The problem is that most textbooks don't emphasize the arguments or provide follow-up questions to test their understanding of the arguments and so students don't think too deeply about them.

Understanding the reasoning for this problem is critical for understanding the boundary condition equations

$$(\mathbf{E}\_2-\mathbf{E}\_1)\cdot \hat{\mathbf{n}} = \mathbf{E}\_{2\perp}-\mathbf{E}\_{1\perp} = \left[-\frac{\partial \Psi_2}{\partial n}+\frac{\partial \Psi_1}{\partial n}\right]_{n=0}=\frac{\sigma}{\epsilon_o}$$

$$\mathbf{E}\_{2\parallel}-\mathbf{E}\_{2\parallel}=(\mathbf{E}\_2-\mathbf{E}\_1)\cdot \hat{\mathbf{t}}=0$$

where $n$ is the coordinate that is perpendicular to the boundary surface and outward to the volume enclosed by the boundary surface; $t$ is any coordinate parallel to the surface.

Several students used the solution for $\mathbf{E}$ given for arguments 1.-3., but this is circular reasoning. The point of the problem is to justify all of the steps needed to get to the solution.

I did not expect a solution with the level of detail in what follows. I generally looked for arguments or words that seemed close to something said below. I did not write extended comments on your solutions for statements that were wrong - you should be able to determine what was wrong by reading the following solution.

1. $E_s$ does not depend on $z$ because the charge distribution does not change if we shift the origin of $z$. Said another way, two people who solve this problem using a different location for $z=0$ should get the same result. $E_s$ does not depend on $\phi$ because if we rotate the charge distribution around the $z$-axis by $\phi$, the charge distribution does not change. Said another way, two people who solve the problem using a different $\phi=0$ line perpendicular to the line of charge should get the same answer. The same argument can be used to argue that $E_z$ and $E_{\phi}$ do not depend on $\phi$ and $z$, but this is not needed because in 2. and 3. they are found to be zero.

2. $E_z=0$ - Assume the line extends from $z=\pm L$. Adding the electric field due to a differential charge at $z$ to that from a differential charge at $-z$ gives an electric field that points in the $\hat{\mathbf{s}}$ direction in the $x-y$ plane. An infinite line of charge can be created by letting $L\rightarrow\infty$. Or, for very small $s$, in the $x-y$ plane the line of charge appears infinite.

3. $E_{\phi}=0$ by the same argument as 2.

_Detailed solution using 1.-3. and Gauss' law_

$$\mathbf{E}(s,\phi,z)=E_s(s,\phi,z)\hat{\mathbf{s}}+E_{\phi}(s,\phi,z)\hat{\boldsymbol{\phi}}+E_z(s,\phi,z)\hat{\mathbf{z}}$$

A Gaussian cylinder of radius $s$ and a height $h$ and centerline along the $z$-axis has three surfaces, with normals of $\hat{\mathbf{z}}$ on the top cap, $-\hat{\mathbf{z}}$ on the bottom cap, and $\hat{\mathbf{s}}$ on the curved side.

$$\oint \mathbf{E}\cdot \hat{\mathbf{n}}da = \int_\text{top cap} \mathbf{E}\cdot \hat{\mathbf{z}} da +  \int_\text{bottom cap} \mathbf{E}\cdot (-\hat{\mathbf{z}}) da + \int_\text{side}\mathbf{E}\cdot \hat{\mathbf{s}} da$$

$\mathbf{E}\cdot \hat{\mathbf{z}} = E_z(s,\phi,z)$ and we have argued that $E_z=0$, so the first two integrals are zero.

$\mathbf{E}\cdot \hat{\mathbf{s}} = E_s(s,\phi,z)$, so the last integral is, using $da=sdzd\phi$,

$$\int_\text{side}\mathbf{E}\cdot \hat{\mathbf{s}} da = \int_{z=-h/2}^{h/2}\int_{\phi=0}^{2\pi} E_s(s,\phi,z) sdz\thinspace d\phi$$

Because $E_s$ is independent of $z$, we can write

$$\int_{z=-h/2}^{h/2}\int_{\phi=0}^{2\pi} E_s(s,\phi,z) sdz\thinspace d\phi=\int_{z=-h/2}^{h/2}\int_{\phi=0}^{2\pi} E_s(s,\phi) sdz\thinspace d\phi=h\int_{\phi=0}^{2\pi} E_s(s,\phi) sd\phi$$

Because $E_s$ is independent of $\phi$, we can write

$$h\int_{\phi=0}^{2\pi} E_s(s,\phi) sd\phi=h\int_{\phi=0}^{2\pi} E_s(s) sd\phi$$

Because $s$ and $\phi$ are orthogonal,

$$h\int_{\phi=0}^{2\pi} E_s(s) sd\phi=hE_s(s) s\int_{\phi=0}^{2\pi} d\phi=hE_s(s) s2\pi$$

Note that Gauss' law only gave us $E_s$ - we had to argue why $E_{\phi}$ and $E_z$ were zero. In addition, in order to do the integration in Gauss' law, we needed to provide additional justification for why $E_s$ could only depend on $s$. So this Gauss' law problem had two separate components: 1. arguments that reduce and simplify the general solution

$$\mathbf{E}(s,\phi,z)=E_s(s,\phi,z)\hat{\mathbf{s}}+E_{\phi}(s,\phi,z)\hat{\boldsymbol{\phi}}+E_z(s,\phi,z)\hat{\mathbf{z}}$$

and then 2. evaluation of the integral in Gauss' law. I find that students that don't understand 1. are not able to articulate why a given Gaussian surface can't be used to find the electric field. For example, their answer to why a Gaussian sphere could not be used to find the electric field in this problem typically only involves an ambiguous statement about symmetry; "symmetry" is ambiguous because both a Gaussian sphere and a Gaussian cylinder have symmetry).


## Problem -- Long Cylinder


1\. Use Gauss's law to find the electric field near the center (from $s=0$ to $s=3R$) of a long solid nonconducting cylinder  of length $L$, radius $R$, and uniform charge density $\rho_o$. Assume $L\gg R$.

<img src="figures/Gauss_Law_Long_Solid_Cylinder.svg" width="100%"/>

Provide explicit justifications for the symmetry argument (described in [the notes](gauss_law.html#using-charges-on-an-insulator)) required to apply Gauss's law and include supporting diagrams. Also, provide justifications for all steps in evaluating the integral in Gauss's law.

2\. Plot the electric field magnitude as a function of $s$ from $s=0$ to $s=3R$.

**Answer**:

This problem is given as an example in many textbooks. The motivation for asking for justifications is that I want you to show me that you understand the steps. It is easy to write a few equations and get the correct result without understanding much. I looked for evidence that you understood the steps based on correct justifications when grading.

1\. A common error was a lack of justification for $\mathbf{E}=E_s(s)\hat{\mathbf{s}}$. More justification is needed than "because it is long" or "due to symmetry" because the reason is not obvious. Also, a diagram showing straight field lines is not a justification -- it _follows_ from a symmetry argument. As covered in the notes on symmetry, there are two types: Cancellation and geometrical. To use symmetry as an argument, you must provide an explanation and/or diagram.

There are three ways to justify $\mathbf{E}=E_s(s)\hat{\mathbf{s}}$.

1. Consider pairs of infinite lines of charge. It was shown in [HW #2](hw2.html#symmetry) that the field is perpendicular to a long line of charge and that there is no component along the direction of the line.

    If the cylinder is long, then it can be thought of as being composed of many long lines of charge. A view looking down the axis of the cylinder is shown in the following figure. Lines of charge at a radial distance $s$ and angles $\varphi$ and $-\varphi$ each create an electric field with components parallel and perpendicular to the $\varphi=0$ line. However, the perpendicular components cancel leaving only a parallel component. 
(This will also be true for a point inside of the cylinder.) As a result, the net electric field is perpendicular to the cylinder.

    <img src="figures/Gauss_Law_Long_Solid_Cylinder_Symmetry_Argument.svg" width="100%">

2. Consider 4 charges at $\pm z$ and $\phi$ and $\pm z$ and $-\phi$. On the $x$ axis, the field from the two charges at $+z$ will have canceling horizontal components but $z$ components that do not cancel and is in the $+x$ direction. The two charges at $-z$ will have canceling horizontal components but $z$ components that do not cancel and is in the $-x$ direction. The net field in the $x$ direction due to the four charges is zero.

    **Insert Figure**

3. Using geometrical symmetry (translational and rotational).

   In general, $\mathbf{E}=E_s(s,\phi,z)\hat{\mathbf{s}}+E_\phi(s,\phi,z)\hat{\boldsymbol{\phi}}+E_z(s,\phi,z)\hat{\mathbf{z}}$.
   
   If the cylinder is infinitely long, then the solution can have no $z$ dependence -- the system is the same if the origin of $z$ changes. The cylinder is symmetric with respect to rotation about $z$, so there can be no $\phi$ dependence. Based on these two statements, the field can only have the form
   
   $\mathbf{E}=E_s(s)\hat{\mathbf{s}}+E_\phi(s)\hat{\boldsymbol{\phi}}+E_z(s)\hat{\mathbf{z}}$
   
    The system is symmetric with respect to rotation of $\pi$ around the $s$ axis and any angle $\phi$ around the $z$ axis. If $E_z$ was not zero, then rotation by $\pi$ around the $z$ axis would give $E_z$ in the same direction. However, rotation by $\pi$ around the $s$ axis would give $E_z$ in the opposite direction. 
    
    **Insert Figure**

    This contradiction implies that $E_z=0$. A similar argument leads to $E_\phi=0$. Based on these two statements, the field can only have the form
    
    $\mathbf{E}=E_s(s)\hat{\mathbf{s}}$

2\. The flux equation is the same for all $s$: $\Phi_E=E_s2\pi s h$. (I expected a diagram of a Gaussian cylinder and a statement that the flux through only one surface is non--zero due to the constraint that $\mathbf{E}=E_s(s)\hat{\mathbf{s}}$ from part 1. of this problem; in addition, the same level of detail shown in the notes and during class should be provided.)

A common error was plugging in a value of $R$ or $3R$ in the $\Phi_E$ equation. To determine the functional dependence of $E_s$, we need to consider all values of $s$.

Plugging in a value for $s$ will restrict us to finding $E_s$ at that radius.

For $s\le R$, $Q_{encl}=\rho_o\pi s^2 h$

For $s\ge R$, $Q_{encl}=\rho_o\pi R^2 h$

Equating the flux $\Phi_E=E_s2\pi s h$ to $Q_{encl}/\epsilon_o$ and solving for $E_s$ gives 

$E_s=\rho_o s/(2\epsilon_o)$ for $s\le R$

$E_s=\rho_o R^2/(2\epsilon_o s)$ for $s\ge R$

Using this with the symmetry argument that gave $\mathbf{E}=E_s(s)\hat{\mathbf{s}}$ gives

$\displaystyle\mathbf{E}(s)=\frac{\rho_o}{ 2\epsilon_o}s\hat{\mathbf{s}}$ for $s\le R$

$\displaystyle\mathbf{E}(s)=\frac{\rho_o R^2}{2\epsilon_o}\frac{\hat{\mathbf{s}}}{s}$ for $s\ge R$

<img src="figures/Gauss_Law_Long_Solid_Cylinder_Plot.svg"/>

## Problem -- Comparison of Gauss's law Result with Exact

From Gauss's law, for a "long" line of charge,

$\displaystyle \mathbf{E}_G(s) = \frac{\lambda_o}{2\pi\epsilon_o}\frac{\hat{\mathbf{s}}}{s}$

In the notes on [Continuous Charge Distributions](continuous_charge_distributions.md!#example-integral-can-be-solved-exactly), it was shown that the exact answer is

$\displaystyle \mathbf{E}_C(s)=k\frac{2L\lambda_o}{s\sqrt{L^2 + s^2}}\hat{\mathbf{s}}$

1\. Compute $E_G/E_C$ for $s/L=1/10$.

2\. Show that for $s\ll L$, $\mathbf{E}_C$ can be written in the form
   
$\displaystyle \mathbf{E}_C(s) \simeq \left(\frac{B_1}{s} + \frac{B_2}{s^2} + \frac{B_3}{s^3}\right)\hat{\mathbf{s}}$

   and find the non--zero constants in terms of $\epsilon_o$, $\lambda_o$, and $L$.
   
## Problem -- Sheet of Charge

A large non--conducting sheet has a uniform charge density $\sigma_o$. Find $\mathbf{E}$ using Gauss's law.

## Problem -- Sheet of Charge

In the following image, four Gaussian surfaces are shown. The non-conducting plane has a uniform charge density of $\sigma$ and is infinite in extent.

<img src="figures/Gaussian_Surfaces_Plane2.png" width="500px"/>

1. Write down Gauss' Law in integral form.
2. Which of the surfaces cannot be used with Gauss' Law to find an equation for the electric field above/below the plane? Justify your answers.
3. Which of the surfaces can be used with Gauss' Law to find an equation for the electric field above/below the plane? Use Gauss' Law to find the electric field for these surfaces. Justify all steps.

**Answer**:

%In grading 2.-3., I looked for all of the justifications that appeared to be related to those that are given in my solution, in particular

%2. Why the electric field is perpendicular to the plane
%3. Why III and IV cannot be used to find \(E\) (because we don't know that \(\mathbf{E}\cdot d\mathbf{a}\) on the surface is such that \(E\) can be factored out of the integral).
%4. Acknowledgement that computing the flux for I and II requires computing a closed surface integral and so integration on all sides (6 surfaces for cube, 3 surfaces for cylinder).

%For 3., one needs to arrive at \(E=\sigma/2\epsilon_o\) and there needs to be a statement that the direction is perpendicular to and away from the plane. 

%Here I'll give a mathematical treatment as an alternative to the more visual way method I used in class and that is used in introductory textbooks. (Either approach is acceptable.)

1\.

$$\oint_{S} \mathbf{E}\cdot d\mathbf{a} = \frac{Q_{enc}}{\epsilon_o}$$

where $Q_{enc}$ is the total charge enclosed by closed surface $S$. The subscript $S$ is optional.

For parts 2. and 3., assume the plane of charge is in the $x-y$ plane and the Gaussian surface is centered at the origin and is small. For any charge at point $(x_o,y_o)$, there is a charge at $(-x_o,-y_o)$ that creates an electric field at the origin that cancels the electric field due to the charge at $(x_o,y_o)$. So we can conclude the electric field must be perpendicular to the plane. Based on a diagram of the electric field vectors due to charges at $(x_o,y_o)$ and $(-x_o,-y_o)$ at a location above and below the origin, we conclude that the electric field will be in the $+z$ direction above the plane and in the $-z$ direction below the plane.

2\. 

III and IV cannot be used. We know the direction of $\mathbf{E}$ and that it can only (possibly) depend on $z$ based on the above arguments. So we can write $\mathbf{E}=E(z)\hat{\mathbf{z}}$ and

$$\oint_SE(z)\hat{\mathbf{z}}\cdot d\mathbf{a} = \frac{Q_{enc}}{\epsilon_o}$$

Because $E(z)$ is not known to be constant on the curved surfaces of III and IV, we cannot factor it out of the integral over these surfaces. (In the case of III, on the caps of the cylinder, we can do the integral because the dot product of $\mathbf{E}$ and $d\mathbf{a}$ is zero on those surfaces so the integral is zero.) 

Using surfaces I and II, we'll find that $E$ does not depend on $z$ (but its direction depends on $z$ from the argument given earlier).

3\. 

I and II

For I and II, the closed surface is made up of a top, bottom, and side surface(s) (for I, there is only one side surface).

$$\oint_{S} \mathbf{E}\cdot d\mathbf{a} = \int_{top} \mathbf{E}\cdot d\mathbf{a} + \int_{bottom} \mathbf{E}\cdot d\mathbf{a} + \int_{side(s)} \mathbf{E}\cdot d\mathbf{a}$$

Because we have argued that the electric field is perpendicular to the plane, the dot product in the integral for the side surface(s) will be zero because the side surface normals are parallel to the plane.

Because the normals of a Gaussian surface point outward from the volume it encloses, the top/bottom surfaces have a normal direction of $\pm \hat{\mathbf{z}}$. We have argued that above/below the plane, $\mathbf{E}$ is in the $\pm \hat{\mathbf{z}}$ direction.

For the top surfaces of I and II, $d\mathbf{a}=da\hat{\mathbf{n}}=da\hat{\mathbf{z}}$ and $\mathbf{E}=E(z) \hat{\mathbf{z}}$.

For the bottom surfaces of I and II, $d\mathbf{a}=da\hat{\mathbf{n}}=-da\hat{\mathbf{z}}$ and $\mathbf{E}=-E(z) \hat{\mathbf{z}}$.

For both I and II

$$\int_{top} \mathbf{E}\cdot d\mathbf{a} = \int_{top} E(z)\hat{\mathbf{z}}\cdot\hat{\mathbf{z}}da$$

$$\int_{bottom} \mathbf{E}\cdot d\mathbf{a} = \int_{bottom} E(z)(-\hat{\mathbf{z}})\cdot(-\hat{\mathbf{z}})da$$

In both cases, the integral is over a surface that does not vary with $z$, so $E(z)$ can be factored out the integral, giving

$$\int_{top} \mathbf{E}\cdot d\mathbf{a} + \int_{bottom} \mathbf{E}\cdot d\mathbf{a} = 2E(z)A$$

where $A$ is the area of the top (or bottom) surface. The charge enclosed for both cases is $Q_{enc}=\sigma A$.

Therefore, in both cases, we arrive at an electric field magnitude

$$E(z)=\frac{\sigma}{2\epsilon_o}$$

The RHS does not depend on $z$, so we can write

$$E=\frac{\sigma}{2\epsilon_o}$$

The direction of the electric field is recovered from the earlier statement that it is perpendicular to the plane and points away. Thus, in vector notation

$$\mathbf{E}=\frac{\sigma}{2\epsilon_o}\hat{\mathbf{z}}\quad z>0$$

$$\mathbf{E}=-\frac{\sigma}{2\epsilon_o}\hat{\mathbf{z}}\quad z<0$$

As an aside, these two expressions can be combined into one using $z/|z|$ to get the correct sign.

$$\mathbf{E}=\frac{\sigma}{2\epsilon_o}\frac{z}{|z|}\hat{\mathbf{z}}$$

## Problem -- Line of Charge

Which of the following object's surfaces can be used to compute the electric field for an infinitely long line of charge? Assume the line passes through the center of the objects. Object IV is a sphere.

<img src="figures/Gauss_Law_Options_Line_of_Charge.svg"/>

## Problem -- Sphere with $\sigma(\theta)$

Consider sphere centered on the origin with a surface charge density of $\sigma_o\cos\theta$. Sketch the sphere and surface charges and indicate where the density is largest. Sketch field lines.

Can a spherical Gaussian surface be used to find the electric field 
1. inside the sphere?
2. outside the sphere?

## Problem -- Long Duct

Consider long duct with a square cross-section with a uniform surface charge density on its surfaces. Sketch the tube and surface charges.

Can a Gaussian surface be used to find the electric field 
1. inside the tube?
2. outside the tube?

## Dented Sphere

A non-conducting spherical shell is covered with charge uniformly on its surface. It is then dented.

1. The electric field near the center of the shell is zero because a Gaussian sphere centered at the origin and fully inside of the shell will have zero enclosed charge.
   * True
   * False

    Justify your answer.

%**Answer**

%False. It is only the electric flux, \(\Phi_E\) through the Gaussian sphere that is zero, because 

%$$\Phi_E\equiv\oint \mathbf{E}\cdot d\mathbf{a} = Q_{Inside\,S}/\epsilon_0 = 0$$.

%But $\mathbf{E}$ can't be pulled out of the integral so we can't say  $\mathbf{E}=0$. All we can say is that if we were to compute the electric field by other means, integral would be zero. 

2. To calculate the electric field near the center of the shell, Gauss' Law could be easily used
    * True
    * False

    Justify your answer.

%**Answer**

%Nope. Gauss' Law is generally only useful for computing \(\mathbf{E}\) when it can be pulled out of the integral. Here we don't have a symmetry argument that would allow this. To compute the electric field, you would need to do an integral like the ones done for continuous charge distributions. And it would be complicated.

3. If the dent is inward (so sphere was punched from the outside), will the electric field at the origin be larger or smaller than that for the un-dented sphere? Justify your answer.

# Using -- Charges on a Conductor

In problems where we are given a charge denstity that is placed on a non--conductor, we can use the Coulomb's law integral to directly find the electric field. For example, if we are told charges are distributed on a square with $\sigma(x,y)$, we can directly evaluate the integral

$$\displaystyle \mathbf{E}=\int  \frac{\hat{\textbf{\char"0509}}}{\char"0509^2}\sigma dA$$

In the case of conductors, all we typically know is that a certain amount of charge has been placed on it. If the conductor is not a perfect sphere, we don't know how the charge distributes on the conductor's surface and so we don't know $\sigma$. If we don't know $\sigma$, we can't evaluate the integral.

However, Gauss's law can be used to give us some information about $\mathbf{E}$.

Prior to using Gauss's law to determine this additional information, we need to know the properties of conductors (see 2.5.1 of Griffiths and make sure that you understand the justifications for each of the following):

1. $\mathbf{E}=0$ inside a conductor.
2. All charges must reside on the surface of a conductor.
3. The electric field is perpendicular to the surface of a conductor.

Suppose a net charge $Q$ is placed on a conductor of arbitrary shape. We can make three statements about the electric field.

1. For points far away, the electric field will approach $kQ\hat{\mathbf{r}}/r^2$, where $r$ is the distance from the center of the conductor.
2. Inside the field is zero due because it is a conductor.
4. The electric field is perpendicular to the surface because it is a conductor.

There is one more statement about the electric field that we can make using Gauss's law. Consider a small Gaussian cylinder as shown in the following diagram. The cylinder is oriented so that the centerline is perpendicular to the surface and half of the cylinder is inside the conductor.

<img src="figures/Conductor-Arbitrary-Shape.svg"/>

The surface charge density $\sigma$ on the conductor is not known. If the cylinder radius is small, the charge inside of the cylinder is $\sigma \pi s^2$ and integration of $\sigma$ is not needed. Gauss's law then reads

$$\oint \mathbf{E}\cdot d\mathbf{A} = \int_{\text{Right cap}} \mkern-36mu\mathbf{E}\bfcdot d\mathbf{A} + \int_{\text{Left cap}}\mkern-30mu\mathbf{E}\bfcdot d\mathbf{A} + \int_{\text{Curved surface}}\mkern-60mu\mathbf{E}\bfcdot d\mathbf{A}=\frac{Q_{encl}}{\epsilon_o}=\frac{\sigma \pi s^2}{\epsilon_o}$$

The field on the left cap is zero because it is inside of the conductor and so the second integral is zero. The field just outside of the curved surface and outside of the conductor is perpendicular to the surface because it is the surface of the conductor, so the integrand of the third integral is zero. (Said another way, the normal vector for the curved surface is perpendicular to the electric field just outside of the conductor).

The field on the right cap will be perpendicular to its surface, so $E_z\hat{\mathbf{z}}$, where $E_z$ is unknown. If the cylinder is small, the integral for the flux through the right cap is the product of the field and the area, $E_z\pi s^2$ because the field is nearly constant on cap. Thus,

$$E_z\pi s^2 = \frac{\sigma \pi s^2}{\epsilon_o}$$

and so

$$E_z = \frac{\sigma}{\epsilon_o}$$

Based on this, and in more general terms, the additional statement is that we can make about the electric field due to charges on a conductor is

4. $\displaystyle E_\perp = \frac{\sigma}{\epsilon_o}$, where in general $\sigma$ is not constant on the surface of the conductor.

> * This is the magnitude of the field. The direction depends on the sign of $\sigma$. If $\sigma$ is positive, $\mathbf{E}$ points outwards from the volume of the conductor.
> * In general, we will not know $\sigma$. Finding it will require the techniques covered in Chapter 3 of Griffiths. 
> * This field is twice the magnitude of the field due to charges uniformly distributed on a non--conducting sheet. The reason for this is considered in the following example.

## Example -- Large and Charged Conducting Slab

A large conducting slab of thickness $t$ and surface area $A$ has a net charge of $Q$ placed on it. A side view is shown below.

<img src="figures/Conductors-Large-Slab-1a.svg"/>

Find and plot the electric field for all $x$.

**Answer**:

When a net charge is placed on a conductor, the charges rearrange themselves such that the electric field inside it is zero. If half of the charges move to the right surface and the other half moves to the left, the charge distribution will appear as two sheets of charge, each with the same surface charge density of $\sigma$.

If the slab is large and we are near it, the surface charge density will appear uniform.

The electric field to the right is the field due to the charges on the two faces: $(\sigma/2\epsilon_o+\sigma/2\epsilon_o)\xhat=\sigma/\epsilon_o\xhat$. The field to the left is $-(\sigma/2\epsilon_o+\sigma/2\epsilon_o)\xhat=\sigma/\epsilon_o\xhat$.

The total charge on the conductor is the sum of the charges on both faces: $Q=Q_L+Q_R=\sigma A + \sigma A$, from which it follows that $\sigma = (Q/2)/A$ and $Q_L=Q_R=Q/2$. This means that half of the net charge is on the right face and the other half on the left face.

This result is consistent with the claim that the field just outside of the conductor is $\sigma/\epsilon_o$. This field is twice that of a sheet of charge because the field just outside of the conductor is due to all charges -- the left and right face of the conductor both create an electric field.

<img src="figures/Conductors-Large-Slab-1b.svg"/>

A general feature of plots of this form is that when one passes through a surface (conducting or non--conducting) with a charge density $\sigma$, there is a jump in the electric field of $\sigma/\epsilon_o$.

**Alternative Answer**

The following procedure will work for more complicated problems than the one given.

Assume unknown charge distributions $\sigma_L$ and $\sigma_R$ appear on the left and right faces of the conductor, respectively. Then, write the electric field in each of the three regions. This process is similar to that used in free-body diagrams. One assumes a direction of the force and if the magnitude computed from summing the forces in that direction is negative, the assumed direction was wrong. 

The charges on each face constitute a sheet of charge and so the magnitude of their fields are $\sigma_L/2\epsilon_o$ and $\sigma_R/2\epsilon_o$. The direction of the field due to a sheet of charge changes direction as you pass through the sheet.

The electric field due to each sheet in three regions, assuming the unknown charge densities are positive, is shown in the following figure.

<img src="figures/Conductors-Large-Slab-1d.svg"/>

The total charge on the conducting slab is $Q_L+Q_R=\sigma_LA+\sigma_RA=Q$.

* For $-t/2 \lt x \lt t/2$,
 
   Assuming $\sigma_L$ is postive, the left sheet produces a field in the $+\xhat$ direction. Assuming $\sigma_R$ is positive, the right sheet produces a field in the $-\xhat$ direction.

   $\displaystyle E_x = +\frac{\sigma_L}{2\epsilon_o}-\frac{\sigma_R}{2\epsilon_o}$

   Note that if $\sigma_L$ turns out to be negative, its contribution to the field in the $\xhat$ direction will be negative in this region. If $\sigma_R$ turns out to be negative, its contribution to the field in the $\xhat$ direction will be positive in this region. 

   Because this region is conducting, the electric field must be zero. This gives

   $\displaystyle 0 = +\frac{\sigma_L}{2\epsilon_o}-\frac{\sigma_R}{2\epsilon_o}\quad\Rightarrow\quad \sigma_L=\sigma_R$
   
   (If there were additional sheets of charge in the system or an external electric field, their contributions would be included in the above equation.)
   
   Plugging $\sigma_L=\sigma_R$ into $\sigma_LA+\sigma_RA=Q$ gives
   
   $2\sigma_RA=Q\quad\Rightarrow\quad \sigma_R=(Q/2)/A$ and $\sigma_L=(Q/2)/A$

* For $x \lt t/2$,

   Assuming both sheets have a positive surface charge density, both sheets create a field that points in the $-\xhat$ direction.

   $\displaystyle E_x = -\frac{\sigma_L}{2\epsilon_o}-\frac{\sigma_R}{2\epsilon_o}$

   (If there were additional sheets of charge in the system or an external electric field, their contributions would be included in the above equation.)
 
   Using the charge densities found earlier,

   $\displaystyle E_x = -\frac{Q/2A}{2\epsilon_o}-\frac{Q/2A}{2\epsilon_o}=-\frac{Q/A}{2\epsilon_o}$

* For $x \gt t/2$,

  Both sheets create a field that points in the $+\xhat$ direction.
  
   $\displaystyle E_x = +\frac{\sigma_L}{2\epsilon_o}+\frac{\sigma_R}{2\epsilon_o}$

   (If there were additional sheets of charge in the system or an external electric field, their contributions would be included in the above equation.)
 
   Using the charge densities found earlier,

   $\displaystyle E_x = +\frac{Q/2A}{2\epsilon_o}+\frac{Q/2A}{2\epsilon_o}=+\frac{Q/A}{2\epsilon_o}$


**Check:** In solving this problem, we used the fact that the magnitude of electric field due to charges uniformly distributed on a sheet is $\sigma/2\epsilon_o$. We also know from Gauss's law that just outside of a conductor, the electric field in the normal direction is $\sigma/\epsilon_o$ (this electric field does not have a factor of 2 because it is the field due to _all_ charges in the system, not just the charges on one face of the conductor). Based on this, just to the right of the right face, we expect $E_n=\sigma_R/\epsilon_o$. Because the normal for this face is in the $+\xhat$ direction, $E_n=E_x$.

Plugging $E_n=E_x=\frac{Q/A}{2\epsilon_o}$ and $\sigma_R=(Q/2)/A$ into

$\displaystyle E_x=\sigma_R/\epsilon_o$

gives

$\displaystyle\frac{Q/A}{2\epsilon_o}=[(Q/2)/A]\epsilon_o$

and so the electric field just outside of the right face of the conductor is consistent with the claim that it should be $\sigma_R/\epsilon_o$.

## Problem -- Large and Charged Conducting Slab with External $\mathbf{E}$

Repeat the previous example when there is an external electric field of $\mathbf{E}=E_o\xhat$.

## Problem -- Conducting Slab Between Charged Sheets
% Copied to notes

A conducting slab is centered on the origin, has thickness $t$, surface area $A=w^2$, and has a net charge of $Q$. At $x=\pm 5t$ there are large nonconducting sheets with uniform charge density $\pm \sigma_o$. The thickness $t$ of the slab is much smaller than $w$.

<img src="figures/Conductors-Slab-Between-Sheets.svg"/>

1. Find the surface charge density on both faces of the conducting slab, assuming that any charge on the faces is uniformly distributed.
2. Find and plot $E_x$ versus $x$.
3. Find and plot the electric potential $V$ versus $x$. Assume $V(0)=0$.

**Answer**

Technically you should have provided answers for $E_x$ and $V$ for $x\gt 5t$ and $x\lt -5t$. I gave extra credit if answers were given for these regions.

A common error involved issues with signs. In the notes, I mentioned that one way of getting the signs right is to assume all unknown surface charges are positive and write the equations for the electric field accordingly.

Another common error was in plotting $V$. $V$ should be continuous. If $E_x(x)$ is constant, $V(x)$ should be linear. If $E_x$ is positive, the slope of $V$ should be negative. To check your $V$ plot, draw vectors for $\mathbf{E}$ with directions given by your $E_x$ plot. If you are moving in the direction of $\mathbf{E}$, $V$ should decrease.

1\. There are two unknown surface charge densities,  $\sigma_L$ and $\sigma_R$, corresponding to the surface charge density on the left and right faces of the slab, respectively. Because the slab is a conductor, all charges must be on its surface. The total charge on the slab is

$Q=\sigma_L A+\sigma_R A$

so that

$\displaystyle \sigma_L+\sigma_R=\frac{Q}{A}$

Assume that $\sigma_L$ and $\sigma_R$ are positive. Inside the slab, the net electric field is zero and the field has four contributions

$\displaystyle  0=-\frac{\sigma_o}{2\epsilon_0}+\frac{\sigma_L}{2\epsilon_o}-\frac{\sigma_R}{2\epsilon_o}-\frac{\sigma_o}{2\epsilon_0}$

Note the sign associated with each. At points to the right of a sheet with a positive surface charge density, the field is to the right. At points to the left of a sheet with a positive surface charge density, the field is to the left. (The directions reverse for a sheet with a negative surface charge density.)

Solving the last two equations for $\sigma_L$ and $\sigma_R$ gives

$\displaystyle \sigma_L=\left(\frac{Q}{2A}+\sigma_o\right)$

$\displaystyle \sigma_R=\left(\frac{Q}{2A}-\sigma_o\right)$

This answer can be checked by comparing with [the example given in the notes](gauss_law.html#using-charges-on-a-conducto). In that problem, there were no sheets of charge on the left and right, so setting $\sigma_o=0$ should give the same surface charge densities as that problem.

To find the potentials, start at a point where the potential is known and then integrate from that point to $x$. In the following, the potentials in Region 2 and 4 labeled in the following figure are computed first to obtain potentials at $V(5t)$ and $V(-5t)$. In general, I looked only at the sketch of the potential -- when $E_x$ is negative, the potential should be increasing with $x$; when $E_x$ is positive, the potential should be decreasing with $x$.

<img src="figures/Conductors-Slab-Between-Sheets-Regions.svg"/>

**Region 2**

$\displaystyle  E_{x2}=-\frac{\sigma_o}{2\epsilon_0}-\frac{\sigma_L}{2\epsilon_o}-\frac{\sigma_R}{2\epsilon_o}-\frac{\sigma_o}{2\epsilon_0}=-\frac{\sigma_o}{\epsilon_o}-\frac{Q/A}{2\epsilon_o}$

$\displaystyle V_2(x) = V(-t/2)-\int^x_{-t/2}E_{x2}dx'=0-E_{x2}\left(x+\frac{t}{2}\right)$

**Region 3**

$E_{x3}=0$ because this region is inside a conductor.

The potential is constant in this region because the field is zero. The potential was given at $x=0$ to be zero, so

$V_3(x)=0$

**Region 4**

$\displaystyle  E_{x4}=-\frac{\sigma_o}{2\epsilon_0}+\frac{\sigma_L}{2\epsilon_o}+\frac{\sigma_R}{2\epsilon_o}-\frac{\sigma_o}{2\epsilon_0}=-\frac{\sigma_o}{\epsilon_o}+\frac{Q/A}{2\epsilon_o}$

$\displaystyle V_4(x) = V(t/2)-\int^x_{t/2}E_{x4}dx'=0-E_{x4}\left(x-\frac{t}{2}\right)$

----

I gave extra credit for answers in Region 1 and 5.

**Region 1**

The fields due to the two sheets with charge density $\pm \sigma_o$ cancel.

$\displaystyle  E_{x1}=+\frac{\sigma_o}{2\epsilon_0}-\frac{\sigma_L}{2\epsilon_o}-\frac{\sigma_R}{2\epsilon_o}-\frac{\sigma_o}{2\epsilon_0}=-\frac{Q/A}{2\epsilon_o}$

$\displaystyle V_1(x) = V(-5t)-\int^x_{-5t}E_{x1}dx'=V(-5t)-E_{x1}\left(x+5t\right)$

Where $V(-5t)$ is obtained by plugging in $x=-5t$ in the equation for $V_2(x)$.

**Region 5**

The fields due to the two sheets with charge density $\pm \sigma_o$ cancel.

$\displaystyle  E_{x5}=-\frac{\sigma_o}{2\epsilon_0}+\frac{\sigma_L}{2\epsilon_o}+\frac{\sigma_R}{2\epsilon_o}+\frac{\sigma_o}{2\epsilon_0}=\frac{Q/A}{2\epsilon_o}$

$\displaystyle V_5(x) = V(5t)-\int^x_{5t}E_{x5}dx'=V(5t)-E_{x5}\left(x-5t\right)$

Where $V(5t)$ is obtained by plugging in $x=5t$ in the equation for $V_4(x)$

----

The final plot is shown in the following figure. It was assumed that $Q/A=4\sigma_o$. As noted in class, if $Q/A < 2\sigma_o$, $E_{x4}$ will be negative and a plot with either sign of $E_{x4}$ was accepted. 

<img src="figures/Conductors-Slab-Between-Sheets-Solution.svg"/>

## Example -- Charge Inside Sphere with a Cavity

A charge $q$ is placed at the center of an uncharged spherical conductor of radius $2R$ with a spherical cavity of radius $R$.

<img src="figures/Conductors_Sphere_with_Cavity.svg"/>

Use Gauss' law to find equations for the electric field in the following three regions

1. $r \lt R$
2. $R \lt r \lt 2R$
3. $r \gt 2R$

and the surface charge density at $r=R$ and $r=2R$.

Plot the electric field versus the distance from the charge.

**Answer**:

A conductor will only have charges on its surface. There are two surfaces, one at $r=R$ and the other at $r=2R$. 

Symmetry argument: (Important!) Any surface charge density must be uniform because the geometry appears the same with a rotation about any axis.

A Gaussian sphere with radius $r\lt R$ will have an enclosed charge of $q$. If all of the charge on the conducting surface is uniform, the will create no electric field for $r \lt R$. Thus, for $r\lt R$, the field is only that due to the point charge and is $E_r=kq/r^2$.

A Gaussian sphere with radius $R\lt r \lt 2R$ has zero electric field on its surface because the surface is inside of a conductor. Thus $\Phi_E=0=Q_{encl}/\epsilon_o$. $Q_{encl}=q + Q_{r=R}$, so $Q_{r=R}=-q$.

If the conductor is uncharged, then by charge conservation, $+q$ must be on its outer surface, so $Q_{r=2R}=+q$.

A Gaussian sphere with $r\gt 2R$ will have an electric field on it that is radial and uniform based on the symmetry argument. The flux is $4\pi r^2 E_r$. The enclosed charge is $q + Q_{r=R} + Q_{r=2R}=q$. Gauss's law thus gives $E_r = kq/r^2$ for $r\gt 2R$.

In summary:

1. $\mathbf{E}=kq\mathbf{\hat{r}}/r^2$ for $r\lt R$.
2. $\mathbf{E}=0$ for $R \lt r \lt 2R$
3. $\mathbf{E}=kq\mathbf{\hat{r}}/r^2$ for $r\gt 2R$.

The plot shown has $E_r=kq/R^2$ when $r=R$ and $E_r=kq/(4R^2)$ when $r=2R$. If the conductor were not there, the curve would be $E_r=kq/r^2$; the presence of the conductor makes this curve zero in the range $R\lt r\lt 2R$.

<img src="figures/Conductors_Sphere_with_Cavity_Plot.svg"/>

## Problem -- Charge Inside Conductor with a Cavity

An uncharged conducting sphere of radius $2b$ is centered on the origin and has a spherical cavity of radius $b$ that is also centered on the origin.

1. If a charge of $+q$ is at the origin, explain why the surfaces at $r=2b$ and $r=b$ each have a net charge of $+q$ and $-q$, respectively, and not, say, $+q/2$ and $-q/2$.
1. Repeat this question for the case where the inner surface of the cavity is not spherical (but the charge at the origin is still in a cavity)

**Solution**

Several students used the justification of "E is zero inside a conductor". This is not a full justification. If someone said "$+q/2$ and $-q/2$ give E of zero inside the conductor", your proof that this statement is wrong would require using Gauss' law.

1.

Gauss' law using a sphere of radius $b\lt r\lt 2b$:

$$\oint \mathbf{E}\cdot d\mathbf{a} = \frac{Q_{encl}}{\epsilon_o} = \frac{q + q_{r=b}}{\epsilon_o}$$

LHS is zero because field is zero inside conductor. So $q_{r=b}=-q$.

2. 

Same approach but the surface is not a sphere but rather a surface that is always inside conductor; $q_{r=b}=-q$.
## Problem -- Charge Inside Conductor with a Cavity

Repeat the previous problem when the conductor has a net charge of $3Q$.

## Problem -- Conducting Sphere with a Cavity
% Copied to notes

The following figure shows the cross--section of a spherical conductor of radius $2R$ with a spherical cavity of radius $R$, both of which are centered on the origin. There is a nonconducting spherical shell that is also centered on the origin, has a $3q$ uniformly distributed on its surface, and a radius $3R$. At the origin, there is a charge $q$.

<img src="figures/Conductors_Sphere_with_Cavity_with_Shell.svg"/>

Using Gauss's law, 

1. Find and plot $E$ versus $r$.
2. Find and plot $V$ versus $r$. Assume $V(r=\infty)=0$.

Justify your steps when using Gauss's law.

**Answer**

Not graded.

For $r\lt 3R$, the answer to this will be idential to the [example given in the notes](gauss_law.html#example-charge-inside-conductor-with-a-cavity). There are two justifications: (1) inside of a uniformly charged spherical shell the electric field is zero and (2) the equations for Gauss's law for the inner regions will not depend on the charge on the shell at $3R$ because this charge is outside of the Gaussian surfaces used to find the field for $r\lt 3R$.

For $r\gt 3R$, the field is $4kq/r^2$; a Gaussian sphere with a radius of $r\gt 3R$ will have $Q_{encl}=4q$.

To find $V$, start with a point where the potential is known. In this case, it is $r=\infty$.

----

$r\ge 3R$

$\displaystyle V(r)=V(\infty)-\int_{\infty}^rE(r')dr'=0+\frac{4kq}{r}$

----

$2R \le r\le 3R$

$\displaystyle V(r)=V(3R)-\int_{3R}^rE(r')dr'=\frac{4kq}{3R}+kq\left(\frac{1}{r}-\frac{1}{3R}\right)$

Simlifying gives

$\displaystyle V(r)=kq\left(\frac{1}{R}+\frac{1}{r}\right)$

----

$R \le r\le 2R$

$\displaystyle V(r)=V(2R)-\int_{2R}^r 0dr'=V(2R)$

where $V(2R)$ is obtained from plugging in $r=2R$ into the equation for $V(r)$ in the region $2R \le r\le 3R$.

$\displaystyle V(2R)=kq\left(\frac{1}{R}+\frac{1}{2R}\right)=\frac{3}{2}\frac{kq}{R}$

so

$\displaystyle V(r)=\frac{3}{2}\frac{kq}{R}=const$

----

$0 \lt r\le R$

$\displaystyle V(r)=V(R)-\int_{R}^r \frac{kq}{r^2}dr'=\frac{3}{2}\frac{kq}{R}+kq\left(\frac{1}{r}-\frac{1}{R}\right)$

where $V(R)=3kq/2R$ is the potential in the region $R \le r\le 2R$. Simplifying gives

$\displaystyle V(r)=kq\left(\frac{1}{2R}+\frac{1}{r}\right)$

----

<img src="figures/Conductors_Sphere_with_Cavity_with_Shell_Solution.svg"/>