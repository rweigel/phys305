# Vector Notation

The general form of a 2-dimensional vector is

$$
\mathbf{A} = A_x\xhat + A_y\yhat
$$

Variations on notation include the equivalent equations 

$$
\mathbf{A} = A_x\ihat + A_y\jhat\quad\text{and}\quad \mathbf{A} = \langle A_x, A_y \rangle
$$

The vector $\mathbf{A}$ can be viewed as the sum of the two vectors $A_x\xhat$ and $A_y\yhat$. On the left-hand side of the diagram below, the two components of $\mathbf{A}$ are shown (assuming the scalar quantities $A_x$ and $A_y$ are both positive). On the right-hand side, the sum of these components is shown.

By definition, the magnitude of $\mathbf{A}$ is the given by the Pythagorean formula

$$
A = |\mathbf{A}| = \sqrt{A_x^2 + A_y^2}
$$

$A$ and $|\mathbf{A}|$ are equivalent -- often one is used instead of the other for clarity of presentation. Another representation for the magnitude of $\mathbf{A}$ uses the dot product -- $A =\sqrt{\mathbf{A}\cdot\mathbf{A}}$.


----

**Common error**: referring to $|\mathbf{A}|$ as "The absolute value of $\mathbf{A}$". The absolute value operator operates on a scalar, e.g., $-12.1$. When used with a vector, the vertical bars mean "The magnitude of $\mathbf{A}$". Both the absolute value and magnitude operations yield a positive scalar, but their calculation is different. The absolute value operation is to simply drop a negative sign. The magnitude operation requires the use of the Pythagorean formula.

If done any programming, you've encountered the concept of ["operation overloading"](https://en.wikipedia.org/wiki/Operator_overloading) - a mathemmatical operation has multiple meanings depending on the arguments. For example the `+` sign in the statement `1 + 2` means "add the numbers before and after it" and in the statement `'B' + 'ob'`, the `+` sign means "concatenate strings to give `'Bob'`. In a similar way, the operator $|\cdot|$ means "absolute value" if $\cdot$ is a scalar and "vector magnitude" if $\cdot$ is a vector.

----


Also by definition

$$
A_x = A\cos\theta\quad\text{and}\quad A_y=A\sin\theta
$$

where $\theta$ is the angle from the $x$-axis with positive angles counter--clockwise. Writing the previous equation as

$$
A_x = |\mathbf{A}|\cos\theta\quad\text{and}\quad A_y=|\mathbf{A}|\sin\theta
$$

makes it clear that the the sign of $A_x$ is due to the $\cos\theta$ term and not the term that multiplies it. Although we know that $A$ is a positive number because it is a magnitude, writing $A$ as $|\mathbf{A}|$ may make this point clearer.

Elimination of $A$ in the two defining equations of

$$
A_x = A\cos\theta\quad\text{and}\quad A_y=A\sin\theta
$$

gives

$$
\frac{\sin\theta}{\cos\theta} = \frac{A_y}{A_x}\quad\text{or} \quad \tan\theta = \frac{A_y}{A_x}
$$

which is expected based on the diagram given above.

## References

Every introductory physics and calculus textbook has a comprehensive introduction to vectors. The reader is encouraged to use them for review.

Several unique perspectives on vectors include 

* [The Feynman Lectures on Physics](https://www.feynmanlectures.caltech.edu/I_11.html), which introduces and motivates the use of vectors by the fact that many laws of physics have invariance (symmetry) under translation and rotation. In the Vector Addition/Subtraction section of these notes, I motivate the use of vectors by noting that they simplify geometric calculations for which one would usually use Pythagorean's theorem and the Law of Cosines (which is derived from the Pythagorean theorem) multiple times.
* [The Math Centre's Introduction to Vectors](https://www.mathcentre.ac.uk/resources/uploaded/mc-ty-introvector-2009-1.pdf) gives several examples of proving geometrical relationships using vectors (mid-point theorem and an unnamed theorem).

## Problems

### Notation

Is $|A|$ a valid expression for the magnitude of a vector? If not, explain why.

**Answer**: $A$ is a magnitude of a vector that corresponds to a length so $A\ge 0$ and taking its absolute value is not needed. A reader seeing the statement $|A|$ may conclude that $A$ can be a positive or negative number (because otherwise why would it be written as $|A|$?).

### Computing magnitude and angle

Draw $\mathbf{A}=-1\xhat + \yhat$ and compute $A$ and $\theta$, where $\theta$ is as defined as the angle with respect to the $x$--axis with positive $\theta$ corresponding to counter-clockwise rotation.

### Notation

The conventional notation is

$$
\mathbf{A} = A_x\xhat + A_y\yhat
$$

$$
A_x = A\cos\theta\quad\text{and}\quad A_y=A\sin\theta
$$

where $\theta$ is as defined as the angle with respect to the $x$--axis with positive $\theta$ corresponding to counter-clockwise rotation.


Let $\theta'$ be defined as the angle with respect to the $y$--axis with positive $\theta'$ corresponding to counter-clockwise rotation.

1. Write the equations for $A_x$ and $A_y$ in terms of $\theta'$.

2. If $A=1$ and $\theta'=45^\circ$, find $A_x$ and $A_y$.


### Notation

If 

$$\mathbf{A} = (x-y)\hat{\mathbf{x}}-y\hat{\mathbf{y}}$$

1. Compute $|\mathbf{A}|$
2. Compute $A$
3. What are the values of $x$ and $y$ that will give $A < 0$?
4. What are the values of $x$ and $y$ that will give $90^\circ \le \theta \le 270^\circ$?

# Vector Addition/Subtraction

Adding or subtracting vectors in a non-Cartesian notation, in general, does not make sense because the direction of their unit vectors depends on position. To see this, consider drawing the following vectors given in cylindrical notation

\(\mathbf{A} = 1\hat{\boldsymbol{\rho}} + 1\hat{\boldsymbol{\phi}}\) at the position \((\rho,\phi,z)\)= \((1,0,0)\)

\(\mathbf{B} = 1\hat{\boldsymbol{\rho}} + 1\hat{\boldsymbol{\phi}}\) at the position \((\rho,\phi,z)\)= \((1,\pi/2,0)\)

\(\mathbf{A}-\mathbf{B}=0\)

In cartesian coordinates, the vectors are

\(\mathbf{A} = 1\hat{\mathbf{x}}\)

\(\mathbf{B} = 1\hat{\mathbf{y}}\)

\(\mathbf{A}-\mathbf{B}=1\hat{\mathbf{x}}-1\hat{\mathbf{y}}\)

### Problems

###

\(\mathbf{A}\) is 1 unit in the \(x-\)direction and \(\mathbf{B}\) is 1 unit in the \(y-\)direction.  

Graphically (make no calculations) estimate the vectors \(\mathbf{A}\) + \(\mathbf{B}\) where 

###

* \(\mathbf{A}\) points east and \(A=4\) units
* \(\mathbf{B}\) is at an angle of \(120^o\) from east and \(B=4\) units.
* \(\mathbf{C}\) is at an angle of \(30^o\) south of east and \(|\mathbf{C}|=4\) units.

Graphically (make no calculations) estimate the vectors

1. \(\mathbf{A}+\mathbf{B}\)
2. \(3\mathbf{A}-4\mathbf{C}\)
3. \(\mathbf{A}+\mathbf{B}-\mathbf{C}\)

###

Vector \(\mathbf{A}\) connects the origin to the point \(a\) at \((x,y)=(2,1)\). Vector \(\mathbf{B}\) connects the origin to the point \(b\) at \((x,y)=(1,2)\).  Draw and label the following vectors to scale:
*\(\mathbf{A}\) and \(\mathbf{B}\);
*\(\hat{\mathbf{A}}\) and \(\hat{\mathbf{B}}\);
*the unit vectors \(\hat{\mathbf{x}}\) and \(\hat{\mathbf{y}}\).
*Draw and label
**\(\mathbf{C}=\mathbf{A}+\mathbf{B}\)
**\(\mathbf{D}=\mathbf{A}-\mathbf{B}\)
**\(\mathbf{E}=-\mathbf{A}+\mathbf{B}\), and
**\(\mathbf{F}=-\mathbf{A}-\mathbf{B}\).
*Compute, in terms of \(\hat{\mathbf{x}}\) and \(\hat{\mathbf{y}}\) and numbers
**\(\mathbf{C}\), \(C\), and \(\hat{\mathbf{C}}\)
**\(\mathbf{D}\), \(D\), and \(\hat{\mathbf{D}}\)
**\(\mathbf{E}\), \(E\), and \(\hat{\mathbf{E}}\)
**\(\mathbf{F}\), \(F\), and \(\hat{\mathbf{F}}\)

###

Find the vector made by connecting a line from \((x,y,z)=(1,2,3)\) to \((x,y,z)=(4,5,6)\).

###

Write an equation for the vector made by connecting a line from \((x_o,y_o,z_o)\) to \((x,y,z)\).

# Unit Vectors


A unit vector is a vector with "unit length" (meaning a length of unity, that is, 1).

The "unit" in "unit vector" means "unit length"; perhaps confusingly, unit vectors do not have a unit (e.g., meters) -- they are dimensionless.

A unit vector associated with an arbitrary vector is obtained by dividing it by its magnitude. We indicate that it is a unit vector by using a hat. So a vector such as

$$\mathbf{r}=r_x\ihat + r_y\jhat$$

which has magnitude

$$r = |\mathbf{r}|=\sqrt{r_x^2 + r_y^2}$$

has an associated unit vector 

$$\hat{\mathbf{r}} = \frac{\mathbf{r}}{r}=\frac{r_x\ihat + r_y\jhat}{r}=\frac{r_x}{\sqrt{r_x^2 + r_y^2}}\ihat + \frac{r_y}{\sqrt{r_x^2 + r_y^2}}\jhat $$

## Example

One reason that unit vectors are useful is that they allow us to make statements of the form: "An object is 10 meters along the direction of $\mathbf{r}$". Suppose $\mathbf{r}=(10\text{ m})\ihat+(20\text{ m})\jhat$. To find a position that is 11 meters along the direction of $\mathbf{r}$, first find a vector of length 1 that is in the direction of $\mathbf{r}$, namely, its unit vector. Then multiply this unit vector by 11 meters.

$$r = \sqrt{(10\text{ m})^2 + (20\text{ m})^2} = \sqrt{500}\text{ m}$$

$$\hat{\mathbf{r}}=\frac{\mathbf{r}}{r}=\frac{10\text{ m}}{\sqrt{500}\text{ m}}\ihat + \frac{20\text{ m}}{\sqrt{500}\text{ m}}\jhat=\frac{1}{\sqrt{5}}\ihat + \frac{2}{\sqrt{5}}\jhat$$

Notice how the units of meters ($\text{m}$) canceled - a unit vector is dimensionless (we also use the term "unit--less" for "dimensionless").

It was claimed that a unit vector has a length of 1. Let's check:

$$|\hat{\mathbf{r}}| = \sqrt{\left(\frac{1}{\sqrt{5}}\right)^2 + \left(\frac{2}{\sqrt{5}}\right)^2}=1\quad\checkmark$$


We can now form a vector for the position of the object that is 11 meters along the direction of $\mathbf{r}$:

$$(11\text{ m})\\,\hat{\mathbf{r}}=(11\text{ m})\left(\frac{1}{\sqrt{5}}\ihat + \frac{2}{\sqrt{5}}\jhat\right)$$

Note that unit vector can be associated with any type of vector, not just position vectors.

## References

* https://www.youtube.com/watch?v=bJyPy4Del2E

## Problems

###

If $\mathbf{A} = -3\xhat + 4\yhat$, find $\hat{\mathbf{A}}$, the unit vector in the direction of $\mathbf{A}$

###

The velocity of a particle is given by $\mathbf{v}= v_{x}\xhat - gt\yhat$, where $v_x = 10\text{ m/s}$ and $g=9.8\text{ m/s}^2$.

Find a unit vector in the direction of $\mathbf{v}$ at 

1. $t=0$ and 
1. $t=1\text{ s}$.

# Curvilinear Unit Vectors

Thus far, only the cartesian unit vectors $\xhat$, $\yhat$, and $\zhat$ have been considered.

Two vectors that are not written with cartesian unit vectors

1. cannot be drawn unless one knows the position because the direction of the unit vectors depends on position and
2. cannot be added, subtracted, dotted, or crossed unless the positions of the vectors are the same.

Two coordinate systems that have curilinear unit vector are cylindrical and spherical.

In cylindrical coordinates, the unit vectors are $\hat{\mathbf{s}}$, $\hat{\boldsymbol{\phi}}$, and $\zhat$ as shown in the following diagram. Although the magnitudes of the unit vectors are the same at both locations, their direction is not.

By definition

* $\hat{\mathbf{s}}$ is always parallel to the $x$--$y$ plane and points radially outward, 
* $\zhat$ always points parallel to the $z$--axis, and
* $\hat{\boldsymbol{\phi}}$ is perpendicular to $\hat{\mathbf{s}}$ and $\zhat$ and points in the direction of increasing $\phi$.

To see that vectors written with cylindrical unit vectors cannot be added, consider the vectors

$\mathbf{A} = 1\hat{\mathbf{s}}$ at $(s,\phi,z)=(1,0,0)$

$\mathbf{B} = 1\hat{\mathbf{s}}$ at $(s,\phi,z)=(1,\pi,0)$

Visually, these vectors point in opposite directions and so their sum should be zero. However, straightforward addition gives $\mathbf{A}+\mathbf{B}=2\hat{\mathbf{s}}$, which is incorrect.

As a result, to add, subtract, dot, or cross two vectors written with curvilinear unit vectors, one must first re-write the two vectors with cartesian unit vectors. 

At $(s,\phi,z)=(1,0,0)$, $\mathbf{A} = 1\hat{\mathbf{s}} = \xhat$

At $(s,\phi,z)=(1,\pi,0)$, $\mathbf{B} = 1\hat{\mathbf{s}} = -\xhat$

so $\mathbf{A}+\mathbf{B} = \xhat - \xhat = 0$, which is correct.

The relationship between cartesian and cylindrical unit vectors is

$\hat{\mathbf{s}} = \cos\phi\xhat + \sin\phi\yhat$

$\hat{\boldsymbol{\phi}} = -\sin\phi\xhat + \cos\phi\yhat$

$\zhat=\zhat$

The relationship between cartesian and spherical unit vectors is

$\hat{\mathbf{r}} = \sin\theta\cos\phi\xhat + \sin\theta\sin\phi\yhat + \cos\theta\zhat$

$\hat{\boldsymbol{\theta}} = \cos\theta\cos\phi\xhat + \cos\theta\sin\phi\yhat-\sin\theta\zhat$

$\hat{\boldsymbol{\phi}} = -\sin\phi\xhat + \cos\phi\yhat$

## Example - Deriving unit vector relationships with a sketch


## References

* https://math.stackexchange.com/questions/1365622/adding-two-polar-vectors
* https://math.stackexchange.com/questions/802077/cross-product-in-cylindrical-coordinates?rq=1

## Problems

### Cartesian

Draw a sketch with a dot indicating the location of $(x,y,z)=(1,2,3)$

### Cylindrical

Draw a sketch with a dot indicating the location of $(s,\phi,z)=(1,\pi/4,3)$

### Spherical

Draw a sketch with a dot indicating the location of $(r,\theta,\phi)=(1,\pi/4,\pi/4)$

### Cylindrical

Draw a sketch with a dot indicating the location of 

1. $\mathbf{A} = 1\hat{\boldsymbol{\rho}} + 2\hat{\boldsymbol{\phi}}$ at the position $(\rho,\phi,z) = (1,0,0)$ and

2. $\mathbf{A} = 1\hat{\boldsymbol{\rho}} + 2\hat{\boldsymbol{\phi}}$ at the position $(\rho,\phi,z) = (1,\pi/2,0)$.

### Spherical

Draw a sketch with a dot indicating the location of 

$\mathbf{A} = 1\hat{\mathbf{r}} + 2\hat{\boldsymbol{\theta}}$ at the position $(\rho,\theta,\varphi) = (1,0,0)$

$\mathbf{A} = 1\hat{\mathbf{r}} + 2\hat{\boldsymbol{\theta}}$ at the position $(\rho,\theta,\varphi) = (1,\pi/2,0)$

# Tangent Vectors

# Normal Vectors
