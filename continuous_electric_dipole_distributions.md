# Introduction

Define "Polarized object" as an analog to "Charged Object"

## Review of Continuous Charge Distributions

## Review of "Perfect" Dipoles

## Dipole Density and the Polarization Vector, $\mathbf{P}$

## Computation of $V$ using $\mathbf{P}$


## Bound Charge Densities $\sigma_b$ and $\rho_b$

## Computation of $V$ using $\sigma_b$ and $\rho_b$



# Problems

## Slab

An infinite slab parallel to the $y$-$z$ plane has a thickness $t$ and a frozen-in polarization $\mathbf{P}=P_o\hat{\mathbf{x}}$. 

Find $\Phi_b$ and $\mathbf{E}_b$.

## Cylinder

A solid cylinder of radius $a$ and height $h$ is aligned with the $z$-axis and has a polarization $\mathbf{P}=P_o\hat{\mathbf{z}}$.

Find $\sigma_b$ and $\rho_b$.

Compute the total bound charge.

Sketch the field lines inside and outside of the cylinder when $h<<a$.

Sketch the field lines inside and outside of the cylinder when $h>>a$.

**Answer**
* Top has $\sigma_b=P_o$, bottom has $\sigma_b=-P_o$, side has $\sigma_b=0$. Interior has $\rho_b=0$. 
* Total bound charge is zero (as it must be).
The equivalent system is two circular disks with an equal and opposite number of charges.
* When $h<<a$, disks are very close and system field between is like that of to infinite surfaces (straight field lines). Overall, looks like [https://i.stack.imgur.com/YJXXP.gif] up-side down.
* When $h>>a$, disks are very far and appear as point charges of magnitude $q=\pm\pi a^\sigma_b$. Field likes look like that of a dipole with a very large separation (field line curvature is much less than that of a perfect dipole or [https://www.physicsforums.com/attachments/600px-vfpt_dipole_electric-svg-png.191109/ the typical dipole diagram] that you see).

## Sphere

A sphere centered on the origin has a polarization of $\mathbf{P}=P_o\hat{\mathbf{z}}$.

Find $\sigma_b$ and $\rho_b$.

Compute the total bound charge.

Sketch the field lines inside and outside of the sphere.

Repeat this problem assuming the sphere has an empty center out to a radius $a_o<a$.

**Answer**

$\hat{\mathbf{n}}=\hat{\mathbf{r}}$

$\sigma_b=\mathbf{P}\cdot\hat{\mathbf{n}}=P_o\hat{\mathbf{z}}\cdot\hat{\mathbf{r}}$

Dot product is angle between the two unit vectors, which is $\cos\theta$ from a diagram.

Or one can derive explicit formula for $\hat{\mathbf{z}}$ in spherical using a diagram: $\hat{\mathbf{z}}=\cos\theta\hat{\mathbf{r}}-\sin\theta\hat{\boldsymbol{\theta}}$.

So

$\sigma_b=P_o\cos\theta$

$\rho_b=-\nabla\cdot\mathbf{P}=0$

Bound charges on sphere are largest at the poles with the top pole being positively charged. Field lines are dipolar outside. Inside then are generally pointing downward (exact result is that they point straight down inside).

Integrating $\sigma_b$ over surface gives net bound charge of zero (as expected).

With hole in center, need to account for a new surface at $r=a_o$, which has $\hat{\mathbf{n}}=-\hat{\mathbf{r}}$.

## Sphere

A sphere centered on the origin has a polarization of $\mathbf{P}=P_o\hat{\mathbf{z}}$.

Find $\sigma_b$ and $\rho_b$.

Compute the total bound charge.

Sketch the field lines inside and outside of the sphere.

Repeat this problem assuming the sphere has an empty center out to a radius $a_o<a$.

## Sphere

A sphere centered on the origin has a polarization of $\mathbf{P}=P_o\mathbf{r}$.

Find $\sigma_b$ and $\rho_b$.

Compute the total bound charge.

Sketch the field lines inside and outside of the sphere.

Repeat this problem assuming the sphere has an empty center out to a radius $a_o<a$.

## Cube

A cube with side length $2a$ and centered on the origin has a polarization $\mathbf{P}=P_o\mathbf{r}$.

## Cube

A cube with side length $2a$ and centered on the origin has a polarization $\mathbf{P}=P_o\hat{\mathbf{z}}$.

# Appendix

## Partial Proof of $V$ Integral

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
