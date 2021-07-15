# Vector Notation

The general form of a 2-dimensional vector is

$$
\mathbf{A} = A_x\xhat + A_y\yhat
$$

Variations on notation include the equivalent equations 

$$
\mathbf{A} = A_x\ihat + A_y\jhat\quad\text{and}\quad \mathbf{A} = \langle A_x, A_y \rangle
$$

The vector $\mathbf{A}$ can be viewed as the sum of the two vectors $A_x\xhat$ and $A_y\yhat$. 

Figure: Left diagram of $\mathbf{A}$ (assuming the scalar quantities $A_x$ and $A_y$ are both positive); Right - equivalent representation of $\mathbf{A}$.

Figure: Left: Diagram showing $A_x\xhat$ and $A_y\yhat$; Right: Diagram used to aid in recalling the following definitions.

By definition, the magnitude of $\mathbf{A}$ is the given by the Pythagorean formula

$$
A = |\mathbf{A}| = \sqrt{A_x^2 + A_y^2}
$$

$A$ and $|\mathbf{A}|$ are equivalent -- often one is used instead of the other for clarity of presentation. Yet another representation for the magnitude of $\mathbf{A}$ uses the dot product -- $A =sqrt{\mathbf{A}\cdot\mathbf{A}}$.

Also by definition

$$
A_x = A\cos\theta\quad\text{and}\quad A_y=A\sin\theta
$$

where $\theta$ is the angle from the $x$-axis with positive angles counter--clockwise. Writing the previous equation as

$$
A_x = |\mathbf{A}|\cos\theta\quad\text{and}\quad A_y=|\mathbf{A}|\sin\theta
$$

makes it clear that the the sign of $A_x$ is due to the $\cos\theta$ term and not the term that multiplies it. Although we know that $A$ is a positive number because it is a magnitude, writing $A$ as $|\mathbf{A}|$ may make this point clearer.

Elimination of $A$ in the two defining equations 

$$
A_x = A\cos\theta\quad\text{and}\quad A_y=A\sin\theta
$$

gives

$$
\frac{\sin\theta}{\cos\theta} = \frac{A_y}{A_x}\quad\text{or} \quad \tan\theta = \frac{A_y}{A_x}
$$

which is expected based on the diagram given above.

Common error: referring to $|\mathbf{A}|$ as "The absolute value of $\mathbf{A}$". The absolute value operator operates on a scalar, e.g., $-12.1$. In this context, the vertical bars mean "The magnitude of $\mathbf{A}$". Both the absolute value and magnitude operations yield a positive scalar, but their calculation is different.

If done any programming, you've encountered the concept of ["operation overloading"](https://en.wikipedia.org/wiki/Operator_overloading) - a mathemmatical operation has multiple meanings depending on the arguments. For example the `+` sign in the statement `1 + 2` means "add the numbers before and after it" and in the statement `'B' + 'ob'`, the `+` sign means "concatenate strings to give `'Bob'`. In a similar way, the operator $|\cdot|$ means "absolute value" if $\cdot$ is a scalar and "vector magnitude" if $\cdot$ is a vector.

## References

Every introductory physics and calculaus textbook has a comprehensive introduction to vectors. The reader is encouraged to use them for review.

Several unique perspectives on vectors include 

* [The Feynman Lectures on Physics](https://www.feynmanlectures.caltech.edu/I_11.html), which introduces and motivates the use of vectors by the fact that many laws of physics have invariance (symmetry) under translation and rotation. In the Vector Addition/Subtraction section of these notes, I motivate the use of vectors by noting that they simplify geometric calculations for which one would usually use Pythagorean's theorem and the Law of Cosines (which is derived from the Pythagorean theorem) multiple times.
* [The Math Centre's Introduction to Vectors](https://www.mathcentre.ac.uk/resources/uploaded/mc-ty-introvector-2009-1.pdf) gives several examples of proving geometrical relationships using vectors (mid-point theorem and an unnamed theorem).

## Problems

###

Why do you think that we write $A$ or $|\mathbf{A}|$ for the magnitude of a vector instead of $|A|$? Is $|A|$ a valid expression for the magnitude of a vector?

###

Draw ... and compute $A$ and $\theta$, where $\theta$ is as defined in the text.

###

The conventional notation is

$$
\mathbf{A} = A_x\xhat + A_y\yhat
$$

$$
A_x = A\cos\theta\quad\text{and}\quad A_y=A\sin\theta
$$

where $\theta$ is defined by ....
'a'

1. Suppose that in the equations for $A_x$ and $A_y$, we want to use $\theta'$ instead of $\theta$. Write the equations for $A_x$ and $A_y$ in terms of $\theta'$.

2. If $A=1$ and $\theta'=45^\circ$, find $A_x$ and $A_y$.

# Unit Vectors


A unit vector is a vector with "unit length" (meaning a length of unity, that is, 1).

The "unit" in "unit vector" means "unit length"; perhaps confusingly, unit vectors do not have a unit (e.g., meters) -- they are dimensionless.

A unit vector associated with an arbitrary vector is obtained by dividing it by its magnitude. We indicate that it is a unit vector by using a hat. So a vector such as

$$\mathbf{r}=r_x\ihat + r_y\jhat\,,$$

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

### Example - Finding a unit vector tangent to a curve

Find a unit vector that is tangent to the curve $y=x^2$.


## References

* https://www.youtube.com/watch?v=bJyPy4Del2E

## Problems

###

If $\mathbf{A} = -3\xhat + 4\yhat$, find $\hat{\mathbf{A}}$, the unit vector in the direction of $\mathbf{A}$

###

The velocity of a particle is given by $\mathbf{v}= v_{x}\xhat - gt\yhat$, where $v_x = 10\text{ m/s}$ and $g=9.8\text{ m/s}^2$.

Find a unit vector in the direction of $\mathbf{v}$ at $t=0$ and $t=1\text{ s}$.

### 

Find the unit vector tangent to the curve $y=\sqrt{1-x^2}$

# Vector Addition/Subtraction

# Curvilinear Unit Vectors

Often it is useful to write vectors in terms of unit vectors of either cylindrical or spherical coordinates.

https://math.stackexchange.com/questions/1365622/adding-two-polar-vectors

https://math.stackexchange.com/questions/802077/cross-product-in-cylindrical-coordinates?rq=1

Discuss fact that cross and dot products require two vectors to have same position.

