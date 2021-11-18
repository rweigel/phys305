# Introduction

In cartesian coordinates with cartesian unit vectors, the approximate magnetic field created by a currnet $I$ flowing in the direction of $\hat{\boldsymbol{\phi}}$ in circle of radius $b$ that is centered on the origin and lies in the $x--y$ plane for $b\ll r$ is

$$\mathbf{B}=\frac{\mu_o}{4\pi}\frac{I\pi b^2}{r^5}\left(3xz\hat{\mathbf{x}}+3yz\hat{\mathbf{y}}+(3z^2-r^2)\hat{\mathbf{z}}\right)$$

where $r^2=x^2+y^2+z^2$. In spherical coordinates with spherical unit vectors, the field is

$$\mathbf{B}=\frac{\mu_0}{4\pi}\frac{I\pi b^2}{r^3}\left(2\cos\theta\mathbf{\hat{r}}+\sin\theta\boldsymbol{\hat{\theta}}\right)$$

With cylindrical unit vectors and spherical coordinates, it was shown in [HW #11](hw11.html) that

$$\mathbf{B}=\frac{\mu_0}{4\pi}\frac{I\pi b^2}{r^3}\left(3\cos\theta\sin\theta\mathbf{\hat{s}}+(3\cos^2\theta-1)\zhat\right)$$

In the limit $b/r\rightarrow 0$, the current loop is referred to as a **perfect dipole**. See [Vector Potential](vector\_potential.html) for the derivation. In those derivations, it was assumed that the loop was circular. It can be shown that this equation applies to loops of arbitrary shape if the maximum extent of the loop is much smaller than $r$.

## Problem -- Magnetic Dipole Transformation from Cartesian to Spherical

Starting with the equation for $\mathbf{B}$ for a magnetic dipole in spherical coordinates with spherical unit vectors, show that

$$\mathbf{B}=\frac{\mu_o}{4\pi}\frac{\pi a^2}{r^5}\left(3xz\hat{\mathbf{x}}+3yz\hat{\mathbf{y}}+(3z^2-r^2)\hat{\mathbf{z}}\right)$$

%**Answer**

%From the equation list on the last page of Griffiths,

%$$\hat{\mathbf{x}} = \sin\theta\,\cos\phi\,\hat{\mathbf{r}} + \cos\theta\,\cos\phi\,\hat{\boldsymbol{\theta}} - \sin\,\theta\,\hat{\boldsymbol{\phi}}$$

%$$\hat{\mathbf{y}} = \sin\theta\,\sin\phi\,\hat{\mathbf{r}} + \cos\theta\,\sin\phi\,\hat{\boldsymbol{\theta}} + \cos\,\theta\,\hat{\boldsymbol{\phi}}$$

%$$\hat{\mathbf{z}} = \cos\theta\,\sin\phi\,\hat{\mathbf{r}} - \sin\,\theta\,\hat{\boldsymbol{\theta}}$$

%Recall that one can check these equations by choosing values of \(\theta\) and \(\phi\) and verifying that the cartesian unit vector points in the expected direction based on a diagram.

%From the previous problem,

%$$\mathbf{B}=\frac{\pi a^2\mu_o}{4\pi}\left(\frac{3xz}{r^5}\hat{\mathbf{x}}+\frac{3yz}{r^5}\hat{\mathbf{y}}+\frac{3z^2-r^2}{r^5}\hat{\mathbf{z}}\right)$$

%Using the unit vector equations above and the relationships

%$$x=r\sin\,\theta\,\cos\,\phi$$

%$$y=r\sin\,\theta\,\sin\,\phi$$

%$$z=r\cos\,\theta$$

%and address each component individually and use \(\cos^2\theta+\sin^2\theta=1\). The final result should be

%$$\mathbf{B}=\frac{\pi a^2\mu_o}{4\pi}\frac{1}{r^3}\left(2\,\cos\,\theta\hat{\mathbf{r}}+\sin\,\theta\,\hat{\boldsymbol {\theta}}\right)$$

## Using the Magnetic Dipole Equation

Use the equation for a magnetic dipole to find the magnetic field at the point $y=y_o$ due to a current loop of radius $b$ centered on the $z$-axis and lying in the $z=d$ plane.

What is the direction of the current required for the dipole equation to apply without modification?

## Magnetic Dipole in Spherical Coordinates

1\. Use

$$\mathbf{A}(r,\theta,\phi) = \frac{\mu_0}{4\pi}\frac{m\sin\theta}{r^2}\boldsymbol{\hat{\phi}}$$

to compute $\nabla \times \mathbf{A}$ using the spherical form of the curl operator. Your answer should be

$$\mathbf{B}(r,\theta,\phi)=\frac{\mu_0}{4\pi}\frac{m}{r^3}\left(2\cos\theta\hat{r}+\sin\theta\hat{\theta}\right)$$

2\. Write the equation for $\mathbf{A}$ above in cartesian coordinates and compute $\nabla \times \mathbf{A}$ using the cartesian form of the curl operator.

## Magnetic Dipole $\mathbf{B}$ in Cylindrical Coordinates

Compute the equation for $\mathbf{B}$ in cylindrical coordinates with cylindrical unit vectors due to a magnetic dipole in the $x--y$ plane that is centered on the origin. 

# Magnetic moment, $\mathbf{m}$

For electric dipoles, we found the potential due to charges $\pm q$ at $z=\pm d$ was

$$V=\frac{1}{4\pi\epsilon_o}\frac{qd}{r^2}$$

The generalization of this equation for charges $\pm q$ at $ \mathbf{r_+}$ and $\mathbf{r\_-}$, was

$$V=\frac{1}{4\pi\epsilon_o}\frac{\mathbf{p}\bfcdot \mathbf{\hat{r}}}{r^2}$$

where the "electric dipole moment" 

$$\mathbf{p}\equiv q(\mathbf{r_+}-\mathbf{r_-})$$

was introduced. This equation has the constraint that $|\mathbf{r_+}-\mathbf{r_-}|\ll r$ and $|\mathbf{r}'_{\pm}|\ll r$; that is, both the separation distance between the charges and the distance to either charge from the origin is small relative to the distance from the origin to the point of interest, $r$.

Previously it was found that the vector potential for a circular current loop of radius $b$ in the $x$--$y$ plane and centered on the origin was

$$\mathbf{A} = \frac{\mu_0}{4\pi}\frac{I\pi b^2}{r^2}\sin\theta\boldsymbol{\hat{\phi}}$$

If we define the **magnetic moment** for a circular loop as

$$\mathbf{m}=IA\hat{\mathbf{n}}$$

then

$$\mathbf{A}=\frac{\mu_o}{4\pi}\frac{\mathbf{m}\times \mathbf{\hat{r}}}{r^2}$$

The normal vector $\hat{\mathbf{n}}$ for the circle is the the vector that point in the direction of your thumb when you wrap your fingers around the loop.

## Example -- Computing $\mathbf{B}$ for Circular Loops not in $x$--$y$ plane.


# Coordinate--Free Dipole Field

The two equations above only apply to a loop with currnet $I$, centered on the origin, and lying in the $x--y$ plane. The "coordinate-free" equation for a loop centered at the origin but with arbitrary orientation is

$$\mathbf{B}=\frac{\mu_0}{4\pi}\frac{1}{r^3}\left(3(\mathbf{m}\cdot\hat{\mathbf{r}})\hat{\mathbf{r}}-\mathbf{m}\right)$$

where $m=I\int d\mathbf{a}$ is the magnetic moment and $d\mathbf{a}$ is a differential area vector. (The integral is over _any_ area bounded by the loop; for a circle, the area could be a disk, which would be the most obvious choice, or a dome, for example. The dome area can be visualized by gluing a circular rubber disk to the circle and then blowing on the disk so as to expand it. Or, think of the shape created when [creating soap bubbles](https://arstechnica.com/science/2020/02/physicists-determine-the-optimal-soap-recipe-for-blowing-gigantic-bubbles/).)

## Using the Coordinate Free Magnetic Dipole Equation

Use the coordinate-free dipole equation

$$\mathbf{B}=\frac{\mu_0}{4\pi}\frac{1}{r^3}\left(3(\mathbf{m}\cdot\hat{\mathbf{r}})\hat{\mathbf{r}}-\mathbf{m}\right)$$

to compute the magnetic field created by a magnetic dipole with dipole moment \(m\) oriented in the \(\hat{z}\)-direction in cartesian coordinates. Convert the cartesian expression that you computed to spherical coordinates.
