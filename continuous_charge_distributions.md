# Introduction

Previously, you have calculated the electric field due to a collection of point charges. From superposition, the electric field at any point in space is the sum of the electric field due to all point charges.

Suppose that you wanted to know the electric field created by a plastic rod that was positively charged by rubbing it against fabric. The number of charges that you would need to account for is on the order of $\gt 10^{20}$. If you could do one calculation per second, computing the electric field due to each of the charges would take longer than the time since the Big Bang.

To allow for an answer in a finite amount of time, the approximation that charge is uniformly distributed along a line can be made. Consider 9 charges placed on a line as shown on the left-hand-side of the diagram below. To compute the electric field at the open circle, we would need to compute the electric field due to each of the 9 charges there. Graphically, we will make the approximation shown in the diagram. The 9 charges on the left are smeared out onto the line to form a continuous charge density.

\begin{center}
\input{Continuous_Charge_Distributions/figures/Figure_2_1}
\end{center}

Mathematically, the we are converting a sum to an integral. The electric field at the open circle is

$$\begin{align*}
\mathbf{E}=&kq\_1\frac{\hat{\mathbf{r}}\_1}{r\_1^2}+kq\_2\frac{\hat{\mathbf{r}}\_2}{r\_2^2}+...+kq\_N\frac{\hat{\mathbf{r}}\_N}{r\_N^2}
\end{align*}
$$

Using the notation of Griffiths, $\mathbf{r}$ is the (single) position of the point of interest and $\mathbf{r}'$ is the position of a charge, so

$$\textbf{\char"0509}\_i=\mathbf{r}-\mathbf{r}_i'$$

where 
this is

$$\begin{align*}
\mathbf{E}=&
 kq\_1\frac{\hat{\textbf{\char"0509}}\_1}{\char"0509\_1^2}
+kq\_2\frac{\hat{\textbf{\char"0509}}\_2}{\char"0509\_2^2}
+...
+kq\_9\frac{\hat{\textbf{\char"0509}}\_9}{\char"0509\_N^2}
\\
\\=&\sum_{i=1}^Nkq\_i\frac{\hat{\textbf{\char"0509}}\_i}{\char"0509\_i^2}
\\
\\
\simeq & \int kdq\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}
\end{align*}
$$

where the integral approximation accuracy increases with $N$.

The arguments given above do not depend on the fact that the charges are on a line, and so the $\mathcal{L}$ can be dropped. In addition, by convention, the approxmation symbol is replaced with an equality, giving

$$\boxed{\mathbf{E}=\int k\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}dq}$$

The advantage of using the integral approximation is that to get an answer, we only need to solve an integral -- we do not need to compute electric field contribution for each point charge and then do a vector sum.

To emphasize the fact that the result of the integration depends on the unprimed variable $\mathbf{r}$, and that the result of integration should not have any primed variables, we sometimes write

$$\mathbf{E}(\mathbf{r})=\int k\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}dq$$

To simplify notation, we often write the integrand as

$$d\mathbf{E}=k\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}dq$$

which corresponds to the electric field due to a differential charge $dq$.

In the case where $\mathbf{r}$ was written with cartesian coordinates, this would be

$$\mathbf{E}(x,y,z)=\int k\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}dq$$

# Steps

Introductory physics textbooks often give examples on finding the electric field due to a continuous charge distribution for which there is a short-cut solution (especially for a ring or disk of charge). However, most continuous charge distribution problems do not have a short-cut solution. Griffiths gives only one example on computing the electric field using a general method.

In this section, I provide steps that can used to find the electric field for an arbitrary continuous charge distribution. Part of the method of solution shown here will be needed later when computing dipole approximations; the steps for computing the electric potential due to a continuous charge distribution and the magnetic field due to a current system will be similar (in the case of currents, the Biot-Savart equation is used instead of Coulomb's Law).

## Predicting Answer in Limits

Based on the problem statement and diagram, write down features that you expect your solution to have. For example,

* For large $z$, solution should approach that for case where all charge on line/sheet, etc. is at the origin.
* For small $z$, solution should approach that for an infinite line/sheet of charge, etc.
* The computed electric field should be pointing is $+x$ and $+z$ direction or the computed electric field should have only a $z$-component.

Such statements will be used to check your final answer and also intermediate steps.

For example, in the case of a line of charge that extends from $x=-L$ to $x=L$,

1. The electric field on the $z$-axis should only have a $z$--component. 
2. For $z\gg L$ (far away from the line), one expects an answer that approaches the answer for a problem where all of the charges on the line are placed at the origin. In this case, the basic form of Coulomb's Law for electric fields can be used to find the answer.
3. For $z\ll L$, one expects an answer that approaches the answer for an infinite line of charge (an ant placed near the origin will conclude that the charges extend to infinity in both directions). In this case, one can look up the equation for the electric field due to an infinite line of charge (or use Gauss' Law to find it).

## Finding $dl$, $da$, or $d\tau$

The differential charge $dq$ must be written in terms of a coordinate system.

* For charges on a line, $dq=\lambda dl$
* For charges on a surface, $dq=\sigma da$
* For charges in a volume, $dq=\rho d\tau$

In this step, $dl$, $da$, or $d\tau$ is written in terms of a coordinate system (usually cartesian, cylindrical, or spherical). The choice of coordinate system depends on the problem; usually, the coordinate system that is "best" will be somewhat obvious ("best" is used in the sense that it makes the math easiest).

Note that when writen with a coordinate variable (e.g., $dx'$ instead of a generic variable (e.g., $dl$), the differential element is written with a prime. The reason is that the position of the charges that cause the electric field is by convention written with a prime and we want to integrate over the position of the charges. Ideally, we would use $dq'$, $dl'$, $d\sigma'$, and $d\tau'$ to emphasize this, but this is not the convention.

### Example -- Constant Line of Charge

For a line of charge with charge density $\lambda$ over $-L\le x\le L$, find $dq$.

**Answer**

<img src="figures/Continuous_Charge_Distributions_1a.svg"/>

If the differential charges lie on the $x$--axis, then $dl = dx'$. So the electric field due to $dq$ can now be written by replacing $dq$ with $\lambda dx'$. If $\lambda$ depends on $x'$, we should write $dq=\lambda(x')dx'$ to emphasize the fact that the charge on a differential element depends on its position.

### Example -- Variable Line of Charge

Find $dq$ for

1. a differential charge on the line $y=x$ and
2. a differential charge on the curve $y=x^2/b$, where $b$ is a constant.

**Answer**



### Problem

Write an equation for $dq$ for a differential charge

1. on a circle centered on the origin and in the $x$--$y$ plane
2. on a disk centered on the origin and in the $x$--$y$ plane
3. on a spherical centered of radius $R$ centered on the origin
4. in a solid sphere centered of radius $R$ centered on the origin

## Write out $\mathbf{r}$, $\mathbf{r}'$, and ${\hat{\textbf{\char"0509}}}/{\char"0509^2}$

Write the full definition of $\mathbf{r}$ and $\mathbf{r}'$ using cartesian unit vectors.

The point where we want to compute the field is $\mathbf{r}=x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}$

The position of a charge that contributes to the field at $\mathbf{r}$ is $\mathbf{r}'=x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}+z'\hat{\mathbf{z}}$

Most generally,

$$\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}=\frac{\textbf{\char"0509}}{\char"0509^3}=\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|^3}=\frac{(x-x')\xhat + (y-y')\yhat + (z-z')\zhat}{\Big[\sqrt{(x-x')^2 + (y-y')^2 + (z-z')}\Big]^3}$$

Instead of writing this general equation, it is often easier to first write a reduced version $\mathbf{r}$ and $\mathbf{r}'$ based on the problem statement and geometry and then compute ${\hat{\textbf{\char"0509}}}/{\char"0509^2}$. This is demonstrated in the following example.

%Note that one should generally write ${\textbf{\char"0509}}/{\char"0509^3}$ with cartesian unit vectors. This equation will be integrated, and if the unit vectors depend on one or more of the differential lengths used in integration, they must be first written in terms of

### Example -- Line of Charge

For a line of charge with charge density $\lambda$ over $-L\le x\le L$, find ${\hat{\textbf{\char"0509}}}/{\char"0509^2}$ for a point on the $y$--axis.

**Answer**

<img src="figures/Continuous_Charge_Distributions_1b.svg"/>

For example, if the problem statement is to find $\mathbf{E}$ on the $y$--axis for a line of charge on the $x$--axis as shown in the figure above, then the point of interest has $x=z=0$ and so $\mathbf{r}=y\hat{\mathbf{y}}$

If the differential charges are all on the $x$--axis, then $y'=z'=0$ and $\mathbf{r}'=x'\hat{\mathbf{x}}$. We can now write

$${\textbf{\char"0509}} = \mathbf{r}-\mathbf{r}'= y\hat{\mathbf{y}}-x'\hat{\mathbf{x}}$$

$$\char"0509 = \sqrt{x'^2+y^2}$$

$$\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}=\frac{\textbf{\char"0509}}{\char"0509^3}=\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|^3}=\frac{y\yhat-x'\xhat}{\Big[\sqrt{x'^2+y^2}\Big]^3}$$

**Common Errors**

A common error is a miscalculation of the magnitude, which is

$$\char"0509=|y\hat{\mathbf{y}}-x'\hat{\mathbf{x}}|=\sqrt{y^2+(-x')^2}$$

If this does not make sense, make sure to review [Vectors](#vectors.html) and the following. In general, $\{\textbf{\char"0509}}$ will have the form

$$\textbf{\char"0509}=A\hat{\mathbf{x}}+B\hat{\mathbf{y}}+C\hat{\mathbf{z}}$$

so that

$$\char"0509=\big|A\hat{\mathbf{x}}+B\hat{\mathbf{y}}+C\hat{\mathbf{z}}\big|=\sqrt{A^2+B^2+C^2}$$

where $A, B,$ and $C$ depend on the problem. In the example given here, $A=-x'$ and $C=z$.

Another common error is in the calculation of $\mathbf{r}-\mathbf{r}'$ -- the negative sign applies to all of the components of $\mathbf{r}'$.

For example, if

$$\mathbf{r}=\hat{x\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}$$

and

$$\mathbf{r}'=\hat{x'\mathbf{x}}+y'\hat{\mathbf{y}}+z'\hat{\mathbf{z}}$$

then the error is to write

$$\mathbf{r}-\mathbf{r}'= x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}-x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}+z'\hat{\mathbf{z}}=(x-x')\hat{\mathbf{x}}+(y+y')\hat{\mathbf{y}}+(z+z')\hat{\mathbf{z}}$$

instead of

$$\mathbf{r}-\mathbf{r}'= \hat{x\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}-\left(x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}+z'\hat{\mathbf{z}}\right)= x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}-x'\hat{\mathbf{x}}-y'\hat{\mathbf{y}}-z'\hat{\mathbf{z}}$$

This correct version simplifies to

$$\mathbf{r}-\mathbf{r}'=(x-x')\hat{\mathbf{x}}+(y-y')\hat{\mathbf{y}}+(z-z')\hat{\mathbf{z}}$$

----

## Checking $d\mathbf{E}$

Recall that the integral to be solved is

$$\mathbf{E}(\mathbf{r})=\int k\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}dq$$

and the notation for the integrand of

$$d\mathbf{E}=k\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}dq$$

At this point, you have ${\hat{\textbf{\char"0509}}}/{\char"0509^2}$ and $dq$ in terms of coordinate system variables. The integrand $d\mathbf{E}$ is the electric field at any point $\mathbf{r}$ due to a charge $dq$ at $\mathbf{r}'$.

To check $d\mathbf{E}$, plug in a few values of $(x',y',z')$ and verify that it is consistent the expected result.

### Example -- Line of Charge

For a line of charge with charge density $\lambda$ over $-L\le x\le L$ and for a point on the $y$--axis,

$$d\mathbf{E}=\frac{y\yhat-x'\xhat}{\Big[\sqrt{x'^2+y^2}\Big]^3}kdq$$

Provide three checks of this equation.

**Answer**:

Plugging in $x'=-L/2$, $x'=0$, and $x'=L/2$ and drawing vectors from these points is shown in the following diagram. All of the vectors end at the point of interest.

<img src="figures/Continuous_Charge_Distributions_1c.svg"/>

The above could be repeated by plugging in values of $y=-L$, in which case all of the vectors should point downwards.

Another way to do this is by inspection of $d\mathbf{E}$. When $y>0$, we expect $d\mathbf{E}$ to have a negative $y$--component independent of the location of $dq$ on the line. When $x'>0$, we expect $d\mathbf{E}$ to have a negative $x$--component.

## Simplifying $d\mathbf{E}$ using Symmetry Arguments

The most frequent type of symmetry will be cancelation symmetry, where pairs of differential charges create an electric field at a point with a component that cancels.

### Example -- Constant $\lambda$

For a line of charge with constant charge density $\lambda$ over $-L\le x\le L$ and for a point on the $y$--axis,

$$d\mathbf{E}=\frac{y\yhat-x'\xhat}{\Big[\sqrt{x'^2+y^2}\Big]^3}kdq=\frac{y\yhat-x'\xhat}{\Big[\sqrt{x'^2+y^2}\Big]^3}k\lambda dx'$$

Vectors for $d\mathbf{E}$ and $dE_x$ are shown for to points on the line that are equidistant from the origin in the following figure. The quantity of differential charges for both cases is equal to $\lambda dx'$.

<img src="figures/Continuous_Charge_Distributions_1d.svg"/>

From this, we conclude that the horizontal component of the $\mathbf{E}$ will end up to be zero after integration.

A mathematical way of showing this is to note that $dE_x(x')=-dE_x(-x')$ and so summation of $dE_x$ over $\pm L$ will result in exact cancellation of $dE_x$.

### Example -- Variable $\lambda$

In the previous example, if $\lambda(x')$ is not constant, for example it is $\lambda(x')=\lambda_oe^{x'/L}$, then differential charges on the left side of the line have less charge and so there are no cancelling pairs as was the case for the previous example. For example, the left--most $dq$ is $\lambda_oe^{-1}dx'$ and the right--most  $dq$ is $\lambda_oe^{1}dx'$.

### Example -- Disk

For a disk of charge that is in the $x$--$y$ plane, centered on the origin, with radius $R$, and with constant charge density $\lambda$ point on the $y$--axis,

$$d\mathbf{E}=..$$

## Integrating $d\mathbf{E}$

There are two possibilities:
1. The integral can be solved "exactly", which informally means standard methods can be used to do the integration, e.g., using trig substitutions, an integral table, or entering the integral into Mathematica or WolframAlpha. The technical term is a "closed-form" solution. An example of an integral with a closed-form solution is $\int_0^{\pi} \sin (ku) du = (\cos (k\pi) - 1)/k$.
2. The solution of the integral is an infinite series. An example is the elliptic integral of the first kind:

   $\int_0^{\pi/2}du/\sqrt{1+k^2\sin^2u}=(\pi/2)\big(1+k^2(1/2)^2+k^4((1\cdot 2)/(3\cdot 4))^2+...\big)$.
   
   We will actually encounter such integrals later in the semester - they also appear in classical mechanics.

   In these cases, one must convert the integrand to a polynomial using a Taylor Series expansion. This will be covered in detail later in the semester when electric and magnetic dipoles are covered. The basic procedure is to re-write the integrand as an infinite series, e.g.,

   $$\int f(x')dx' = \int \big(c_0 + c_1x' + c_2x'^2 + ...\big)dx'$$

   where the constants $c_0, c_1, c_2, ...$ are determined using the Taylor Series expansion formula. Written in this way, the integral only involves the integration of polynomials. There are subtleties to this method -- one needs to ensure that the series is converging and sometimes several approximations to $f(x')$ are needed, one for locations near the charge distribution and one at far locations.

### Example -- Integral can be solved exactly

Integrate $d\mathbf{E}$ found in Example 2.2.1.

First, we need to write $dq$ in terms of a differential length element. In general, $dq=\lambda dl$. In this problem, the differential length is the width of $dq$, which is along the $x$ direction, so $dl=dx$ and $dq = \lambda dx$. The equation of the electric field created by a single differential charge at an arbitrary location on the $x$-axis found previously was

$$
d\mathbf{E} = k\frac{\lambda dx}{(x^2 + y_o^2)^{3/2}}(-x\ihat + y_o\jhat)
$$

$$
\mathbf{E} = \int_{-a}^{a}k\lambda\frac{ -x\,dx}{(x^2 + y_o^2)^{3/2}}\ihat + \int_{-a}^{a}k\lambda\frac{ y_o\,dx}{(x^2 + y_o^2)^{3/2}}\jhat
$$

Before you attempt to do an integration, you should find ways to avoid doing integration. Based on the diagram, for every charge with $x<0$, there is a charge with $x>0$ that cancels its horizontal electric field. (Look back at the previous tutorial where this fact was also used.)

As a result, we know that the answer cannot have a $x$ component and the first integral must evaluate to zero. Mathematically, another way to show this is to use the fact that the integrand of the first integral, $-x/(x^2+y_o^2)^{3/2}$ is an odd function on the interval $x=[-a,a]$.

To get the final answer, we only need to do one integral:

$$
\mathbf{E} = \int_{-a}^{a}k\lambda\frac{ y_o\,dx}{(x^2 + y_o^2)^{3/2}}\jhat
$$

On exams, you will only be asked to set up the integral and it will be assumed that you can either do the integral or look it up. For the curious, the integration is given here.

The integral part of the right-hand-side is $E_y$

$$
E_y = \int_{-a}^{a}k\lambda\frac{y_o\,dx}{(x^2 + y_o^2)^{3/2}}
$$

This integral was given in Example 21.10 of the textbook (but with different variables). Using it gives

$$
E_y = k\frac{2a\lambda}{y_o\sqrt{a^2 + y_o^2}}
$$

Note that $2a\lambda$ is the total charge on the line. The answer in terms of the parameters given and $\mathbf{E}$ is

$$
\mathbf{E} = k\frac{Q}{y_o\sqrt{a^2 + y_o^2}}\jhat
$$

## Checking Answer

# Problems

## Line of Charge

A line of charge with charge density of $\lambda$ extends from $-L$ to $L$ on the $x$-axis, where $L>0$.

1. Assuming $L=\infty$,
   1. Sketch electric field lines
   2. Use Gauss' Law to find $\mathbf{E}$
2. For finite $L$
   1. Sketch electric field lines
   2. Find and equation for $\mathbf{E}$ on the $z$-axis in terms of constants times a single integral
   3. Find $V$ on the $z$-axis in terms of constants times a single integral
3. When $z<<L$, what is expected for $\mathbf{E}$ on the $z$-axis, and why?
4. When $z>>L$, what is expected for $\mathbf{E}$ on the $z$-axis, and why?

All final equations should be expressed in terms of $k,\lambda,L,x,y,z$ and cartesian unit vectors.

**Answer**
1. Same integral worked out in class for $-L$ to $L$ case except lower limit is 0 instead of $-L$ and $\hat{\mathbf{x}}$ term will not integrate to zero.
2. $$\mathbf{E}= -k\lambda \int_0^L\frac{xdx}{(x^2+z^2)^{3/2}}\hat{\mathbf{x}} + k\lambda z\int_0^L\frac{dx}{(x^2+z^2)^{3/2}}\hat{\mathbf{z}}$$
3. The result of the integration is 
4. $$\mathbf{E} = \frac{k\lambda}{z}\left[\left(-1+\frac{z}{\sqrt{z^2+L^2}}\right)\hat{\mathbf{x}} + \left(\frac{L}{\sqrt{z^2+L^2}}\right)\hat{\mathbf{z}}\right]$$
5. Practice: Use result of integration and $1/(1+\epsilon)^n\simeq 1-n\epsilon$ to check limits given below.
   * Units check so that result has units of [N]/[C] and a check that no terms like $1+z^2$ (1 is dimensionless, z has units of [m])
   * For $z>>L$ expect to get $\mathbf{E} = \hat{z}k\lambda L/z^2$, where $\lambda L$ is total charge on line.
   * $E_z$ should be half that for a line that extends from $-L$ to $L$
   * As $z$ increases, ratio of $E_x/E_z$ should decrease.
   * As $z$ decreases, ratio of $E_x/E_z$ should increase.
* As $z$ approaches zero, $E$ should become infinite (eventually sitting on top of a charge).
  * As $\lambda$ approaches zero, $E_x$ and $E_y$ should approach zero.

* Some students said $z>>L$, should get $E=kq/z^2$; I accepted this, but technically they should have indicated that they know $q = \lambda L$.
* Some students said "check answer for $z>>L$ and  $z<<L$" without further elaboration.  I did not give credit for this as the problem asks "what features must the solution have".  In addition, the expected answer for $z<<L$ is not obvious.
* For $z<<L$ the answer is not expected to be an infinite line of charge because there is no charge to the left of the z axis.


## Line of Charge

A line of charge with charge density of $\lambda$ extends from $-L$ to $-l$ on the $x$-axis; A second line of charge with charge density of $\lambda$ extends from $l$ to $L$ on the $x$-axis; $L>0$ and $l>0$.

1. Sketch electric field lines
2. Find $\mathbf{E}$ on the $z$-axis in terms of constants times a single integral
3. Find $V$ on the $z$-axis in terms of constants times a single integral
4. At the origin, what is expected for $\mathbf{E}$?
5. When $l\simeq L$ and $z>>L$, what is expected for $\mathbf{E}$ on the $z$-axis, and why?
6. When $L>> l$ and $z>>l$, what is expected for $\mathbf{E}$ on the $z$-axis, and why?

All final equations should be expressed in terms of $k,\lambda,l,L,x,y,z$ and cartesian unit vectors.

**Answers to 2.,4.-6.**

$$
\begin{align}
\mathbf{E} = &-k\lambda \int_l^L\frac{xdx}{(z^2+x^2)^{3/2}}\hat{\mathbf{x}} + k\lambda z\int_l^L\frac{dx}{(z^2+x^2)^{3/2}}\hat{\mathbf{z}}\\
& +k\lambda \int_{-l}^{-L}\frac{xdx}{(z^2+x^2)^{3/2}}\hat{\mathbf{x}} + k\lambda z\int_{-l}^{-L}\frac{dx}{(z^2+x^2)^{3/2}}\hat{\mathbf{z}}
\end{align}
$$

Note that the $\hat{\mathbf{x}}$ terms are expected to cancel based on the symmetry argument given below. (This was not asked for, but if you want to show this mathematically, change the variable in the second $\hat{\mathbf{x}}$ integral using the substitution $u=-x$).

4. The electric field should be zero. Each charge at a position $x$ has a charge at a position $-x$ that creates an equal an opposite electric field at the origin.

5. $l\simeq L$ means the two lines of charge "look" like point charges at $\pm L$. Because $z>>L$, it also looks like the two point charges overlap at the origin. I expect the electric field to be proportional to $\hat{\mathbf{z}}/z^2$. 
  (If you wanted to go further, you could write that the charge at the origin would be $2(L-l)\lambda$, so the electric field would be $2k(L-l)\lambda\hat{\mathbf{z}}/z^2$.)

6. In this case, the gap of $2l$ between the lines of charge is not visible. So the solution should be the same as that for an infinite line of charge (which you should be able to compute using Gauss' Law). 

## Line of Charge Along x-axis

A line of charge with a charge density of $\lambda$ and length $2L$ lies on the $x$-axis and is centered on the origin.

1. What is the expected direction of $\mathbf{E}(z)$?
2. For $z >> L$, what should $\mathbf{E}(z)$ approach?
3. For $z << L$, what should $\mathbf{E}(z)$ approach?
4. Find $\mathbf{E}(z)$ and verify that it satisfies your answers to 2. and 3.

**Answer**

1. For $z>0$, expect $\mathbf{E}(z)$ to be in the $+z$ direction. For $z<0$, expect $\mathbf{E}(z)$ to be in the $-z$ direction.
2. For $z \gg L$, it appears that all of the charge $q'=2L\lambda$ is at the origin and so the electric field is $\mathbf{E}(z)=\hat{\mathbf{z}}kq'/z^2$ for $z>0$ and $\mathbf{E}(z)=-\hat{\mathbf{z}}kq'/z^2$ for $z < 0$.
3. For $z \ll L$, expect solution to be same as that for an infinite line of charge, for which the magnitude of the field is $E=2k\lambda/z$ in a direction perpendicular to the line.
4. The field is (See Griffiths Example 2.2 for derivation)

$$\mathbf{E}=\frac{2k\lambda L}{z\sqrt{z^2+L^2}}\hat{\mathbf{z}}$$

For $z \gg L$, $z^2 \gg L^2$ is also true, so that $z^2+L^2\simeq z^2$. Using $\sqrt{z^2}=|z|$ gives

$$\mathbf{E}=\frac{2k\lambda L}{z|z|}\hat{\mathbf{z}}$$

which is, for $z>0$ (so that $|z|z = z^2$),

$$\mathbf{E}=\frac{2k\lambda L}{z^2}\hat{\mathbf{z}}$$

and is, for $z<0$ (so that $|z|z = -z^2$)

$$\mathbf{E}=-\frac{2k\lambda L}{z^2}\hat{\mathbf{z}}$$

These two equations match the equations predicted from part 2. of this problem. 

----

For now, it is acceptable to do limits in this way, but in the future, we'll want to re-write the equation so that it contains a small ratio of two length scales.

For $z \gg L$, and starting with,

$$\mathbf{E}=\frac{2k\lambda L}{z\sqrt{z^2+L^2}}\hat{\mathbf{z}}$$

factor out the $z$ under the square root to give

$$\mathbf{E}=\frac{2k\lambda L}{z|z|}\frac{1}{\sqrt{1+L^2/z^2}}\hat{\mathbf{z}}$$

The advantage of this formulation is that the it is easier to write a Taylor Series expansion of $1/\sqrt{1+L^2/z^2}$.

----

For $z \ll L$, $z^2 \ll L^2$ is also true, so that $z^2+L^2\simeq L^2$ and

$$\mathbf{E}=\frac{2k\lambda L}{z\sqrt{z^2+L^2}}\hat{\mathbf{z}}$$

reduces to

$$\mathbf{E}=\frac{2k\lambda L}{z}\hat{\mathbf{z}}$$

which matches the equation found in 3.

----

The corresponding re-write of 

$$\mathbf{E}=\frac{2k\lambda L}{z\sqrt{z^2+L^2}}\hat{\mathbf{z}}$$

in terms of a small ratio of two length scales (in this case $z/L$) is

$$\mathbf{E}=\frac{2k\lambda L}{z|L|}\frac{1}{\sqrt{1+z^2/L^2}}\hat{\mathbf{z}}$$

Note that $|L|=L$ because $L$ is positive.

----

## Line of Charge at Angle

A line of charge with a charge density of $\lambda$ lies along the line $z=m x$, where $m$ is a constant, and extends from $x=-a$ to $x=a$. 

1. What is the expected (general) direction of $\mathbf{E}(z)$? How is this direction expected to change as $z$ increases?
2. For $z >> a$, what should $\mathbf{E}(z)$ approach? (Give exact equation in terms of the parameters and coordinate system given in the problem.)
3. For $z << a$, what should $\mathbf{E}(z)$ approach? (Give exact equation in terms of the parameters and coordinate system given in the problem.)
3. Find an integral that must be solved to find $\mathbf{E}(z)$. See the [[F19/Notes#Continuous_Charge_Distributions|note in Step 4]] about integrals with primed variables that don't have a corresponding primed differential variable.

**Answer**

This problem is similar to a problem in [[F19/Notes#Continuous_Charge_Distributions|sample problems for continuous charge distributions in the notes]]. The difference is that in the sample problem

1. the line was at an angle $\alpha$ in the $x-y$ plane
2. the points of interest were along the $y$-axis

and in this problem 

3. the line follows the equation $z=mx$ so that the length of the line is $2\sqrt{a^2+(am)^2}=2a\sqrt{1+m^2}$
4. the points of interest are along the $z$-axis

Instead of the relationship $y'=x'\tan\alpha$, the relationship is $z'=mx'$. So anywhere $\tan\alpha$ appears in the sample problem, it can be replaced with $m$ and any $y$, $y'$, and $\hat{\mathbf{y}}$ can be replaced with $z$, $z'$, and $\hat{\mathbf{z}}$, respectively. The final answer is

$$\mathbf{E}(z)_{\mbox{all }dq'} = \int_{-a}^{a}\frac{dx'\sqrt{1+m^2}}{4\pi\epsilon_0}\frac{-x'\hat{\mathbf{x}}+(z-mx')\hat{\mathbf{z}}}{\big(x'^2 + (z-mx')^2\big)^{3/2}}$$

For question #2., at $z\gg a$, the answer of "0" is technically correct, but the problem statement asks for an equation in terms of the parameters given in the problem. Examples of this were given in class, in example 2.2 of Griffiths, and in the notes. The answer I was looking for is $\mathbf{E}(z)=\hat{\mathbf{y}}kq'/y^2$, where $q'=\lambda L = \lambda 2\sqrt{a^2+(am)^2}=\lambda 2a\sqrt{1+m^2}$. So that in terms of the parameters given in the problem statement, 

$$\mathbf{E}(z)=\frac{k\lambda 2a\sqrt{1+m^2}}{y^2}\hat{\mathbf{y}}$$

For question #3., at $z\ll a$, the point is just above the center of the line and the system "looks" like an infinite line of charge, so the infinite line of charge equation applies. The electric field at this point will be perpendicular to the line. If $s$ is the perpendicular distance from the center of the line, then $\mathbf{E}(s)=(1/2\pi\epsilon_o)\hat{\mathbf{s}}/s$. Some students used this equation with $z$ instead of $s$. 

To get an exact equation in terms of the parameters and coordinate system of the problem, one needs to write $\hat{\mathbf{s}}$ and $s$ in terms of parameters and the coordinate system given in the problem of $x$, $z$, and $m$: $\mathbf{s}=-z(-\hat{\mathbf{x}}+\hat{\mathbf{z}}/m)$. I gave full credit if it was recognized that at $z\ll a$, the field should be perpendicular to the line. Some students said the field would be zero because these points are on the line - this is not correct - $z\ll a$ means just above the infinitely thin line; only $z = 0$ would be exactly on the line.

## Line of Charge at Angle

A line of charge in the $x$-$y$ plane has a charge density of $\lambda$ and is at an angle of $\alpha$ with the x-axis (positive angle towards $+y$ axis) and extends from $x=0$ to $x=a$.

1. What is the expected direction of $\mathbf{E}(y)$ for $y > 0$?
2. For $y \gg a$, what should $\mathbf{E}(y)$ approach?
3. Find and integral that must be solved to find $\mathbf{E}(y)$. See note in Step 4 about integrals with primed variables that don't have a corresponding primed differential variable.

**Answer**

==== Step 0 ====

1. For $y > 0$, the expected direction of $\mathbf{E}(y)$ is in the $-x$ and $+y$ direction. As $y$ increases, $\mathbf{E}(y)$ should have a $y$-component that becomes larger than the $-x$ component because as $y$ increases, the line of charge appears more and more similar to a point charge at the origin.
2. For $y \gg a$, the line of charge appears as a point charge of magnitude $q'=2L\lambda$ at the origin, for which $\mathbf{E}(y)=\hat{\mathbf{y}}kq'/y^2$. The length of the line needs to written in terms of the paramters given ($a$ and $\alpha$). Using $\cos\alpha=a/L$ gives $L=a/\cos\alpha$ and $\mathbf{E}(y)=\hat{\mathbf{y}}k(2a\lambda/\cos\alpha)/y^2$. Use a diagram to show this.
3. See the following steps.

==== Step 1 ====

This is a line of charge, so the general relationship is $dq'=\lambda dl'$.

In general, a differential element parallel to a line in the $x-y$ plane can be written as

$$d\mathbf{l}' = dx'\hat{\mathbf{x}} + dy'\hat{\mathbf{y}}$$

the magnitude of $d\mathbf{l}'$ is

$$dl' = \sqrt{(dx')^2+(dy')^2}$$

factoring out $dx'$ gives a formula that may be familiar from a calculus course in which the the length of a curve is computed:

$$dl' = dx'\sqrt{1+\left(\frac{dy'}{dx'}\right)^2}$$

In this problem, we are not explicitly given $dy'/dx'$, but it can be derived by noting from a diagram that $\tan\alpha = y'/x'$ so that

$$y' = x'\tan\alpha$$

and so $dy'/dx' = \tan\alpha$. Substitution gives

$$dl' = dx'\sqrt{1+\left(\frac{dy'}{dx'}\right)^2}=dx'\sqrt{1+\tan^2\alpha}$$

and finally an equation for $dq'$

$$dq'=\lambda dl'= dx'\sqrt{1+\tan^2\alpha}$$

==== Step 2 ====

In general,

$$\mathbf{r}=x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}$$

$$\mathbf{r}'=x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}+z'\hat{\mathbf{z}}$$

for this problem, we only want to know $\mathbf{r}$ for points on the $y$-axis, so $x=0$ and $z=0$ leaving

$$\mathbf{r}=y\hat{\mathbf{y}}$$

the line of charge is in the $x$-$y$ plane, so $z'$ is always zero, leaving

$$\mathbf{r}'=x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}$$

==== Step 3 ====

Write 

$$\mathbf{E}_{dq'}(x,y,z) = \frac{dq'}{4\pi\epsilon_0}\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|^3}$$

replacing $dq'$ with the differential found in Step 1, $dq' = dx'\sqrt{1+\tan^2\alpha}$, and using the reduced versions of $\mathbf{r}$ and $\mathbf{r}'$ in Step 2. Noting that

$$\mathbf{r}-\mathbf{r}'=y\hat{\mathbf{y}}-\big(x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}\big)$$

which can be rewritten as

$$\mathbf{r}-\mathbf{r}'=-x'\hat{\mathbf{x}}+(y-y')\hat{\mathbf{y}}$$

The magnitude is

$$|\mathbf{r}-\mathbf{r}'|=\sqrt{(-x')^2 + (y-y')^2}=\sqrt{x'^2 + (y-y')^2}$$

and substitution gives

$$\mathbf{E}_{dq'}(x,y,z) = \frac{dx'\sqrt{1+\tan^2\alpha}}{4\pi\epsilon_0}\frac{-x'\hat{\mathbf{x}}+(y-y')\hat{\mathbf{y}}}{\big(x'^2 + (y-y')^2\big)^{3/2}}$$

==== Step 4 ====

The final step is to integrate this equation from $x'=0$ to $x'=a$:

$$\mathbf{E}(y)_{\mbox{all }dq'} = \int_0^{a}\frac{dx'\sqrt{1+\tan^2\alpha}}{4\pi\epsilon_0}\frac{-x'\hat{\mathbf{x}}+(y-y')\hat{\mathbf{y}}}{\big(x'^2 + (y-y')^2\big)^{3/2}}$$

In Step 1, $dl'$ was found in terms of $dx'$, so all of the primed variables need to be written in terms of $x'$. Using $y'=x'\tan\alpha$ gives an equation that is ready for integration

$$\mathbf{E}(y)_{\mbox{all }dq'} = \int_0^{a}\frac{dx'\sqrt{1+\tan^2\alpha}}{4\pi\epsilon_0}\frac{-x'\hat{\mathbf{x}}+(y-x'\tan\alpha)\hat{\mathbf{y}}}{\big(x'^2 + (y-x'\tan\alpha)^2\big)^{3/2}}$$

To solve this, if desired, start by factoring out the constant terms and write the equation in terms of three integrals with $y$ treated as a constant with respect to the integration.

==== Step 5 ====

Two checks were already made.

If the integral was performed, we could use the answer from Griffiths Example 2.2 to compare the answer from this problem for a special value of $y$: the $y$-value where a line drawn from the center of, and perpendicular to, the line of charge crosses the $y$-axis.

## Line of Charge with Parabolic Shape

A line of charge with a charge density of $\lambda$ has a parabolic shape of $z=x^2$ and extends from $x=-a$ to $x=a$. 

1. What is the expected direction of $\mathbf{E}(z)$?
2. For $z >> a$, what should $\mathbf{E}(z)$ approach? (Give exact equation in terms of the parameters and coordinate system given in the problem.)
3. Find an integral that must be solved to find $\mathbf{E}(z)$. See the [[F19/Notes#Continuous_Charge_Distributions|note in Step 4]] about integrals with primed variables that don't have a corresponding primed differential variable.

**Answer**

1. For $z>0$, expect $\mathbf{E}$ to be in $+\hat{\mathbf{z}}$ direction (I gave full credit for this answer, but some correctly noted that there may be a point for small enough z where it is actually in $-\hat{\mathbf{z}}$ direction). For $z>0$, expect $\mathbf{E}$ to be in $-\hat{\mathbf{z}}$ direction. The on the z-axis, the electric field has no component in the $\hat{\mathbf{x}}$ direction because a charge at position $x=x_o$ produces an electric field with a component in the $-\hat{\mathbf{x}}$ direction that is canceled by that from a charge at $x=-x_o$. The electric field component in the $z$-direction for both of these charges are in the $+z$ direction. (Draw this.)

2. When $z>>a$, the distance from all $dq's$ to the point of interest at $z$ is approximately $z$ and so Coulomb's Law for a charge $Q$ at the origin applies: $E=kQ'/z^2$, where $Q'$ is the total charge on the line. $Q'$ needs to be written in terms of the parameters of the problem - it is $Q' = \lambda L$ where $L$ is the length of the line that will depend on $a$. Computing the length of the line requires integration and I gave full credit is this was recognized but $L$ was not calculated. The general formula for the length of a line that follows a path $\mathcal{P}$ is

$$L = \int_{\mathcal{P}} dl$$

The integration requires writing $dl$ and the limits of integration in terms of a coordinate system.

The general formula for a differential element in cartesian coordinates is

$$d\mathbf{l} = dx\hat{\mathbf{x}} + dz\hat{\mathbf{z}}$$

which has a magnitude

$$dl = \sqrt{(dx)^2+(dz)^2}$$

factoring out $dx$ gives a formula that may be familiar from path integration in a calculus course 

$$dl = dx\sqrt{1+\left(\frac{dz}{dx}\right)^2}$$

so the length of the differential element depends on the slope of the line $dz/dx$. For this particular problem, the line follows the path $\mathcal{P}$ according to the equation $z=x^2$, so $dz/dx = 2x$. Substitution gives

$$dl = dx\sqrt{1+4x^2}$$

This $dl$ can now be used to perform the integration of the general equation

$$L = \int_{\mathcal{P}} dl = \int_{-a}^{a}dx\sqrt{1+4x^2}$$

The integral can be perfomed using a $x=(\tan u)/2$ substitution and appears in many references - the key that I am looking in solutions is the recognition that computing the total charge in terms of the parameters given requires integration and the set-up of the integral.

3. 

Step 1

$dl$ was already computed previously and so

$$dq'=\lambda dl'= dx'\sqrt{1+4x'^2}$$

where primes are used following the convention that position variables associated with charges are primed.

Step 2

In general,

$$\mathbf{r}=x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}$$

$$\mathbf{r}'=x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}+z'\hat{\mathbf{z}}$$

for this problem, we only want to know $\mathbf{r}$ for points on the $z$-axis, so $x=0$ and $y=0$ leaving

$$\mathbf{r}=z\hat{\mathbf{z}}$$

the line of charge is in the $x$-$z$ plane, so $y'$ is always zero, leaving

$$\mathbf{r}'=x'\hat{\mathbf{x}}+z'\hat{\mathbf{z}}$$

Step 3.

Write 

$$\mathbf{E}_{dq'}(x,y,z) = \frac{dq'}{4\pi\epsilon_0}\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|^3}$$

replacing $dq'$ with the differential found in Step 1, $dq' = \lambda dx'\sqrt{1+4x'^2}$, and using the reduced versions of $\mathbf{r}$ and $\mathbf{r}'$ in Step 2. Noting that

$$\mathbf{r}-\mathbf{r}'=z\hat{\mathbf{z}}-\big(x'\hat{\mathbf{x}}+z'\hat{\mathbf{z}}\big)$$

which can be rewritten as

$$\mathbf{r}-\mathbf{r}'=-x'\hat{\mathbf{x}}+(z-z')\hat{\mathbf{z}}$$

The magnitude is

$$|\mathbf{r}-\mathbf{r}'|=\sqrt{(-x')^2 + (z-z')^2}=\sqrt{x'^2 + (z-z')^2}$$

and substitution gives

$$\mathbf{E}_{dq'}(x,y,z) = \frac{\lambda dx'\sqrt{1+4x'^2}}{4\pi\epsilon_0}\frac{-x'\hat{\mathbf{x}}+(z-z')\hat{\mathbf{z}}}{\big(x'^2 + (z-z')^2\big)^{3/2}}$$

Step 4.

The last step is to integrate from $x'=-a$ to $x'=a$ and to replace $z'$, which depends on the integration variable $x'$, using $z'=x'^2$.

$$\mathbf{E}_{\mbox{all }dq's}(x,y,z) = \int_{-a}^{a}\frac{\lambda dx'\sqrt{1+4x'^2}}{4\pi\epsilon_0}\frac{-x'\hat{\mathbf{x}}+(z-x'^2)\hat{\mathbf{z}}}{\big(x'^2 + (z-x'^2)^2\big)^{3/2}}$$

Previously, it was claimed that the $\hat{\mathbf{x}}$-component should be zero and so it is expected that the $\hat{\mathbf{x}}$ integral is zero. That the integral is zero can be seen by noting that that the function

$$f(x') = \frac{x'\sqrt{1+4x'^2}}{\big(x'^2 + (z-x'^2)^2\big)^{3/2}}$$ 

satisfies $f(x')=-f(x')$ so that $f$ is an "odd" function, which integrate to zero over a range from $x'=-a$ to $x'=+a$. You may want to demonstrate this by plotting this function. (The argument here is similar to the argument that the integral of $f(x)=x^3$ is zero - the integral of $f(x)$ for $x<0$ is equal and opposite to the integral for $x>0$ so that the integral over a range $x=-a$ to $x=+a$ is zero.


## Ring of Charge

A ring of charge with charge density of $\lambda$ has a radius $a$, is centered at the origin, and lies in the $x-y$ plane.

1. Find $V$ on the $z$-axis
2. Find $\mathbf{E}$ on the $z$-axis
3. When on the $z$-axis and for $z<<a$, what is expected for $\mathbf{E}$, and why?
4. When $z>>a$, what is expected for $\mathbf{E}$ on the $z$-axis, and why?

All final equations should be expressed in terms of $k,\lambda,a$ using any coordinate system.

## Ring of Charge

Write your answer on a blank sheet of paper of printer paper. 

A ring of charge with charge density of $\lambda$ has a radius $a$, is centered at the origin, and lies in the $x-y$ plane.

1. When $z<<a$, what is expected for $\mathbf{E}$ (magnitude and direction) on the $z$-axis, and why<sup>*</sup>?
2. When $z>>a$, what is expected for $\mathbf{E}$ (magnitude and direction) on the $z$-axis, and why<sup>*</sup>?
3. Find $V$ on the $z$-axis (that is, find $V(z)$). 
4. Find $\mathbf{E}$ on the $z$-axis (that is, find $\mathbf{E}(z)$). 

<sup>*</sup>That is, without doing any integration, what do you expect the answer to be like in these limits. I gave many examples of this in class. 

All final equations should be expressed in terms of $k$ or $\epsilon_0,\lambda$, and $a$ using any coordinate system.

[[Image:ring_of_charge.png|400px]]

**Answer**

1\. Expect $\mathbf{E}=0$ at the origin. One can find a $dq$ on one side of the ring that has a $dq$ on the other side of the ring that produces an electric field equal in magnitude and opposite in direction at the origin. A tiny distance above the origin, the electric field lines are nearly horizontal, so the $z$ component should be nearly zero. So an acceptable answer is that the $z$ component gets close to zero.

2\. Field should be that of a charge $q=2\pi a\lambda$ at the origin, so

$$\mathbf{E} = \frac{1}{4\pi\epsilon_0}\frac{q}{z^2}\hat{\mathbf{z}} = \frac{1}{4\pi\epsilon_0}\frac{2\pi a\lambda}{z^2}\hat{\mathbf{z}} = \frac{1}{2\epsilon_0}\frac{a\lambda}{z^2}\hat{\mathbf{z}}=\frac{2k\pi a\lambda}{z^2}\hat{\mathbf{z}}$$

The equation from part 4. gives this result if $z>>a$.

3\. A clever way of solving this without doing any integration is to note that the work required to move a charge along the $z$-axis against the force due to the ring is the same as if all of the charge, $2\pi a\lambda$ were concentrated at say $x=a$ or $y=a$ because the distance from a $dq$ on the ring to a point on the $z-$axis is the same for all charges on the ring. In this case, the distance of the point charge to a point along the z-axis is $|\mathbf{r}-\mathbf{r}'|=(a^2+z^2)^{1/2}$. So

$$V=\frac{kq}{|\mathbf{r}-\mathbf{r}'|} = \frac{k 2\pi a\lambda}{(a^2+z^2)^{1/2}}=\frac{\lambda a }{2\epsilon_0}\frac{1}{(a^2+z^2)^{1/2}}$$

The regular method of solution is to start with the general equation for electric potential due to a point charge
$$V = \frac{q}{4\pi\epsilon_0}\frac{1}{|\mathbf{r}-\mathbf{r}'|}$$

In terms of a differential charge, this is
$$dV = \frac{dq}{4\pi\epsilon_0}\frac{1}{|\mathbf{r}-\mathbf{r}'|}$$

From the given geometry, the point of interest is
   
$$\mathbf{r} = z\hat{\mathbf{z}}$$

and the location of the charge acting on the point of interest is

$$\mathbf{r}' = a\cos(\phi)\hat{\mathbf{x}}+a\sin(\phi)\hat{\mathbf{y}}$$

so

$$dV = \frac{dq}{4\pi\epsilon_0}\frac{1}{(a^2+z^2)^{1/2}}$$

We want to integrate, so need to write $dq$ in terms of coordinates. On the ring, a small piece has a length of $a d\phi$, so

$dq=\lambda a d\phi$$

where $\phi$ is the polar coordinate angle. This gives

$$V = \int_0^{2\pi}\frac{\lambda a d\phi}{4\pi\epsilon_0}\frac{1}{(a^2+z^2)^{1/2}}$$

factoring out everything that does not depend on $\phi$ gives

$$V = \frac{\lambda a }{4\pi\epsilon_0}\frac{1}{(a^2+z^2)^{1/2}}\int_0^{2\pi}d\phi$$

so the final answer is

$$V = \frac{\lambda a }{2\epsilon_0}\frac{1}{(a^2+z^2)^{1/2}}=\frac{2k\pi\lambda a}{(a^2+z^2)^{1/2}}$$

'''4. Find $\mathbf{E}$ on the $z$-axis (that is, find $\mathbf{E}(z)$)'''

The easy way to get the answer is to use

$$\mathbf{E}=-\nabla V=-\hat{\mathbf{z}}\partial V/\partial z =-\hat{\mathbf{z}}\frac{\partial}{\partial z}\frac{\lambda a }{2\epsilon_0}\frac{1}{(a^2+z^2)^{1/2}}$$

Giving the final answer of
$$\mathbf{E}=\frac{\lambda a}{2\epsilon_0}\frac{z\hat{\mathbf{z}}}{(z^2+a^2)^{3/2}}=2k\pi\lambda a\frac{z\hat{\mathbf{z}}}{(z^2+a^2)^{3/2}}$$

Long answer:

General definition of electric field due to a point charge from Coulomb's Law
$$\mathbf{E} = \frac{q}{4\pi\epsilon_0}\frac{1}{|\mathbf{r}-\mathbf{r}'|^2}\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|}$$

In terms of a differential charge, this is
$$\mbox{(1)  }d\mathbf{E} = \frac{dq}{4\pi\epsilon_0}\frac{1}{|\mathbf{r}-\mathbf{r}'|^2}\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|}$$

From the given geometry, the point of interest is
$$\mathbf{r} = z\hat{\mathbf{z}}$$
and the location of the charge acting on the point of interest is
$$\mathbf{r}' = a\cos(\phi)\hat{\mathbf{x}}+a\sin(\phi)\hat{\mathbf{y}}$$

Subtituting into (1) gives
$$d\mathbf{E}= \frac{dq}{4\pi\epsilon_0}\frac{z\hat{\mathbf{z}}-a\cos(\phi)\hat{\mathbf{x}}-a\sin(\phi)\hat{\mathbf{y}}}{(z^2+a^2)^{3/2}}$$

We want to integrate, so need to write $dq$ in terms of coordinates. On the ring, a small piece has a length of $a d\phi$, so
$$dq=\lambda a d\phi$$

where $\phi$ is the polar coordinate angle. This gives
$$\mathbf{E} = \int_0^{2\pi}\frac{\lambda d\phi}{4\pi\epsilon_0}\frac{z\hat{\mathbf{z}}-a\cos(\phi)\hat{\mathbf{x}}-a\sin(\phi)\hat{\mathbf{y}}}{(z^2+a^2)^{3/2}}$$

Based on the symmetry argument that we can always find another $dq$ that exactly cancels the horizontal component of a given $dq$, we expect the $\hat{\mathbf{x}}$ and $\hat{\mathbf{y}}$ terms to be zero, so we can drop them. Or we can notice that after factoring out everything that does not depend on $\phi$, the integrals for the $\hat{\mathbf{x}}$ and $\hat{\mathbf{y}}$ terms are $\cos\phi\,d\phi$ and $\sin\phi\,d\phi$ from $0$ to $2\pi$, which are both zero.

Keeping only the $\hat{\mathbf{z}}$ term and factoring out everything that does not depend on $\phi$ gives
$$\mathbf{E} =\frac{\lambda a}{4\pi\epsilon_0}\frac{z\hat{\mathbf{z}}}{(z^2+a^2)^{3/2}} \int_0^{2\pi}d\phi$$

Final answer:
$$\mathbf{E} = \frac{\lambda}{2\epsilon_0}\frac{az}{(z^2+a^2)^{3/2}}\hat{\mathbf{z}}$$

To check your answer to part 1., factor out $a$ from the square root to get 

$$\mathbf{E} = \frac{\lambda}{2\epsilon_0}\frac{az}{a^3(1+a^2/z^2)^{3/2}}\hat{\mathbf{z}} = \frac{\lambda}{2a\epsilon_0}\frac{z}{a}\hat{\mathbf{z}}$$

When $z/a \ll 1$, $\mathbf{E} \simeq 0\hat{\mathbf{z}}$.

## Ring of Charge

A ring of charge with charge density of $\lambda$ has a radius $a$, is centered at the origin, and lies in the $x-y$ plane.

1\. Find $V$ in the $x-y$ plane in terms of a constant times one or more integrals.
2\. Find $\mathbf{E}$ in the $x-y$ plane in terms of a constants and integrals.
3\. At $x^2+y^2=0$ and $z=0$, what is expected for $\mathbf{E}$, and why?
4\. When $x^2+y^2\simeq a^2$ and $z=0$, what is expected for $\mathbf{E}$, and why?
5\. When $x^2+y^2>>a^2$ and $z=0$, what is expected for $\mathbf{E}$, and why?

All final equations should be expressed in terms of $k,\lambda,a$ using any coordinate system.

## Half Ring of Charge

A half ring of charge with charge density of $\lambda$ has a radius $a$, is centered at the origin, lies in the $x-y$ plane, and has its endpoints at $y=\pm a$.

1. Find $V$ at the origin.
2. Find $\mathbf{E}$ at the origin.
3. At the origin, what is expected for $\mathbf{E}$, and why?
4. When $x^2+y^2>>a^2$, what is expected for $\mathbf{E}$, and why?

All final equations should be expressed in terms of $k$ or $\epsilon_0,\lambda$, and $a$ using any coordinate system.

## Half Ring of Charge

A half ring of charge with charge density of $\lambda$ has a radius $a$, is centered at the origin, lies in the $x-y$ plane, and has its endpoints at $y=\pm a$.

1\. Find $V$ along the $x$-axis in terms of a constant times one or more integrals.
2\. Find $\mathbf{E}$ along the $x$-axis in terms of a constants and integrals.

All final equations should be expressed in terms of $k$ or $\epsilon_0,\lambda$, and $a$ using any coordinate system.

## Disk of Charge

A disk of charge with charge density of $\sigma$ has a radius $a$, is centered at the origin, and lies in the $x-y$ plane.

1. Sketch electric field lines
2. Find $V$ on the $z$-axis in terms of constants times a single integral.
3. Find $\mathbf{E}$ on the $z$-axis in terms of constants times one or more integrals.
4. On the $z$-axis and for $z<<a$, what is expected for $\mathbf{E}$, and why?
5. On the $z$-axis and for $z>>a$, what is expected for $\mathbf{E}$, and why?
6. It does not technically make sense to ask "on the $z$-axis and for large $z$, what is expected for $\mathbf{E}$?". Why?

All final equations should be expressed in terms of $k$ or $\epsilon_0,\sigma$, and $a$ using any coordinate system.

**Answers to 3.-6.**

3\. There are three general ways to do this:

1\. Starting from the basic formula for the electric field due to a charge $dq$ and summing contributions from $dq$s at all locations on the disk. This will involve a double integral.
2\. Integrating over contributions from rings of charge. This will involve a single integral over contributions of rings of different sizes and knowledge of the electric field due to a ring of charge.
3\. Computing $V$ first and using $\mathbf{E}=-\nabla V$.

I'll follow method 1. and I'll note that one of the formulas found as the solution is developed is the same one you would get if you started with 2. Method 3. would be useful if I asked you to solve the integral, which I am not going to do on an exam. (But there is a trick that I have not showed you that you could use on the exam where you can write $V$ in terms of an integral and then differentiate it. If you want to know about this, ask me in person).

General definition of electric field due to a point charge from Coulomb's Law
$$\mathbf{E} = \frac{q}{4\pi\epsilon_0}\frac{1}{|\mathbf{r}-\mathbf{r}'|^2}\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|}$$

In terms of a differential charge, this is
$$\mbox{(1)  }d\mathbf{E} = \frac{dq}{4\pi\epsilon_0}\frac{1}{|\mathbf{r}-\mathbf{r}'|^2}\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|}$$

From the given geometry, the point of interest is
$$\mathbf{r} = z\hat{\mathbf{z}}$$
and the location of the charge acting on the point of interest is
$$\mathbf{r}' = \rho\cos(\phi)\hat{\mathbf{x}}+\rho\sin(\phi)\hat{\mathbf{y}}$$
Note that $\rho$ is used in this equation to make $\mathbf{r}'$ depend on the radial distance of the charge $dq$. In the ring problem, $a$ is used instead of $r$.

Subtituting into (1) gives
$$d\mathbf{E}= \frac{dq}{4\pi\epsilon_0}\frac{z\hat{\mathbf{z}}-\rho\cos(\phi)\hat{\mathbf{x}}-\rho\cos(\phi)\hat{\mathbf{y}}}{(z^2+\rho^2)^{3/2}}$$

We want to integrate, so need to write $dq$ in terms of coordinates. On the disk, a small patch has an area of $(\rho d\phi)(d\rho)$, so
$$dq=\sigma (\rho d\phi)(d\rho)$$

where $\rho$ and $\phi$ are polar coordinates. This gives
$$\mathbf{E} = \int_0^{2\pi}\int_0^a \frac{\sigma \rho d\phi d\rho}{4\pi\epsilon_0}\frac{z\hat{\mathbf{z}}-\rho\cos(\phi)\hat{\mathbf{x}}-\rho\cos(\phi)\hat{\mathbf{y}}}{(z^2+\rho^2)^{3/2}}$$

Based on the symmetry argument that we can always find another $dq$ that exactly cancels the horizontal component of a given $dq$, we expect the $\hat{\mathbf{x}}$ and $\hat{\mathbf{y}}$ terms to be zero, so we can drop them. Or we can notice that after factoring out everything that does not depend on $\phi$, the integrals for the $\hat{\mathbf{x}}$ and $\hat{\mathbf{y}}$ terms are $\cos\phi\,d\phi$ and $\sin\phi\,d\phi$ from $0$ to $2\pi$, which are both zero. Note that if a 1/2 disk was given, the integral limits would be from $0$ to $\pi$, and one of the integrals would not be zero.

$$\mbox{(2)  }\mathbf{E} = \int_0^{2\pi}\int_0^a \frac{\sigma \rho d\phi d\rho}{4\pi\epsilon_0}\frac{z\hat{\mathbf{z}}}{(z^2+\rho^2)^{3/2}}$$

Equation (2) is an acceptable answer for this problem. Equation (2) is the equation that you would get if you integrated the contributions from rings of various radii. 

If you have other problems to work on, do them first before reading the following.

----

In the following, I'll fill in the steps required in order to verify that the result of (2) matches the predictions for $z<<a$ and $z>>a$, which is not something that would be asked on an exam. On an exam, you should be able to recognize that for $z<<a$, the final answer should be the same as that for a sheet of charge and for $z>>a$, the final answer should be the same as if all of the charge on the disk was concentrated at the origin. Part of the motivation of identifying how the solution should behave in limiting cases is that a lot can go wrong while developing the solution. These limits give you a way to check your final answer.

Factoring out the constants in (2) gives
$$\mathbf{E} = \frac{\sigma z\hat{\mathbf{z}}}{4\pi\epsilon_0} \int_0^{2\pi}\int_0^a \frac{\rho d\phi d\rho}{(z^2+\rho^2)^{3/2}}$$

Nothing in the integrand depends on $\phi$, so the $\phi$ integral redues to $2\pi$
$$\mathbf{E} = \frac{2\pi\sigma z\hat{\mathbf{z}}}{4\pi\epsilon_0} \int_0^a \frac{\rho d\rho}{(z^2+\rho^2)^{3/2}}$$

The result of the integration gives the final answer (to integrate, use a substitution of $u^2=\rho^2+z^2$ and remember that $\sqrt{z^2}=|z|$).
$$\mbox{(3)  }\mathbf{E} = \frac{\sigma z}{2\epsilon_0} \left(\frac{1}{|z|}-\frac{1}{\sqrt{a^2+z^2}}\right)\hat{\mathbf{z}}$$

For $z<<a$, only the first term in parenthesis is large
$$\mathbf{E} = \frac{\sigma}{2\epsilon_0}\frac{z}{|z|}\hat{\mathbf{z}}$$

Notice how the $\frac{z}{|z|}$ term tells use the direction of the electric field. When $z>0$, this term is $+1$. When $z<0$, this term is $-1$.

For $z>>a$, we need to do a bit more work on the second term in parentheses in (3). Factor out a $z$ from the square root to get
$$\mathbf{E} = \frac{\sigma z}{2\epsilon_0} \left(\frac{1}{|z|}-\frac{1}{|z|\sqrt{1+a^2/z^2}}\right)\hat{\mathbf{z}}$$

Because $a/z << 1$, we can use the binomial expansion to get
$$\mathbf{E} \simeq \frac{\sigma z}{2\epsilon_0} \left[\frac{1}{|z|}-\frac{1}{|z|}\left(1-\frac{a^2}{2z^2}\right)\right]\hat{\mathbf{z}}$$

Simplifying gives
$$\mathbf{E} \simeq \frac{\sigma}{2\epsilon_0} \frac{a^2}{2z^2}\frac{z}{|z|}\hat{\mathbf{z}}$$

To show that in this limit the result is the same as if all of the charge was at the origin, we need to compute the charge on the disk, which is
$$q=\sigma\pi a^2$$

Subtituing for $\sigma$ gives
$$\mathbf{E} \simeq \frac{\sigma}{2\epsilon_0} \frac{a^2}{2z^2}\frac{z}{|z|}\hat{\mathbf{z}}$$

Simplifying gives
$$\mathbf{E} \simeq \frac{q}{4\pi\epsilon_0} \frac{1}{z^2}\frac{z}{|z|}\hat{\mathbf{z}}$$

4\. At points close to the center of the disk and just above and below it the disk "looks" like an infinite sheet. So we expect the solution to be the same as an infinite sheet of charge, for which $\mathbf{E}=\sigma\hat{\mathbf{z}}/(2\epsilon_0)$.

5\. On the $z$-axis and for $z>>a$, what is expected for $\mathbf{E}$, and why?

Very far away from the disk (with respect to $a$, of course), the disk "looks" like a small point charge at the origin. The total charge on the disk is $q=\sigma\pi a^2$, so one expects $\mathbf{E}=kq\hat{\mathbf{z}}/z^2=k\sigma\pi a^2\hat{\mathbf{z}}/z^2$.

6\. It does not technically make sense to ask "on the $z$-axis and for large $z$, what is expected for $\mathbf{E}$?". Why?

An ant's "large" $z$, say 12 inches, could be the same $z$ as what a whale would call a "small" $z$. This is why one always writes equations that indicate what "large" is relative to, e.g., $z>>a$.

## Cylinder of Charge

A hollow cylinder of radius $a$ has its axis along the $z$-axis, extends from $z=0$ to $z=-L$, and has a surface charge of $\sigma_0$.

1. If $L<<a$, what is expected for $\mathbf{E}$ at $z=0$?
2. At $z=-L/2$, what is expected for $\mathbf{E}$?
3. Find $V(z)$
4. Find $\mathbf{E}(z)$
## Disk of Charge

A disk of charge with a charge density of $\sigma$ has a radius $a$, is centered at the origin, and lies in the $x-y$ plane. 

1. What is the expected direction of $\mathbf{E}(z)$ for $z>0$ and for $z < 0$?
2. For $z >> a$, what should $\mathbf{E}(z)$ approach? (Give exact equation in terms of the parameters and coordinate system given in the problem.)
3. For $z << a$, what should $\mathbf{E}(z)$ approach? (Give exact equation in terms of the parameters and coordinate system given in the problem.)
4. Find the integral for $\mathbf{E}(z)$, solve it, and verify that the solution satisfies your answers to 1. , 2., and 3. Solve this problem using [[F19/Notes#Continuous_Charge_Distributions|the steps in the notes]]. There is a simplification for this problem that is given in textbook solutions (similar to the ring of charge problem) - do not use this simplification. Eventually, I'll ask you for the electric field at points off of the $z$-axis, and this simplification won't work.

**Answer**

1. $\mathbf{E}(z)$ should be in $+\hat{\mathbf{z}}$ direction for $z>0$ and in $-\hat{\mathbf{z}}$ direction for $z>0$.

2. For $z>>a$, looks like a point charge at the origin with electric field magnitude of $E=kq/z^2$ with a direction given by the answer to 1. In terms of the parameters given in the problem, $q=\pi a^2 \sigma$, so $E=(\sigma a^2/4\epsilon_o)/z^2$.

3. For $z<<a$, looks like an infinite sheet of charge, for which $E=\sigma/2\epsilon_o$ and direction given by the answer to 1.

4. The set-up for this part is similar to the ring of charge.

In the ring of charge, the charges were on a small line segment with $dl' = ads'd\phi'$ so that $dq'=\lambda dl'$

In this problem, the charges are on a patch of area with $dA=s'ds'd\phi'$.

In the ring of charge, $\mathbf{r}'=a\cos\phi\hat{\mathbf{x}}+a\sin\phi\hat{\mathbf{y}}$.

In this problem, the distance to the $dq'$s is not fixed at $a$, but rather depends on $s$ according to $\mathbf{r}'=s'\cos\phi'\hat{\mathbf{x}}+s'\sin\phi'\hat{\mathbf{y}}$.

After some algebra, you should get

$$\mathbf{E}(z) = \frac{\sigma z\hat{\mathbf{z}}}{4\pi\epsilon_0} \int_0^{2\pi}\int_0^a \frac{s' d\phi' ds'}{(z^2+s'^2)^{3/2}}$$

Nothing in the integrand depends on $\phi'$, so the $\phi'$ integral reduces to $2\pi$

$$\mathbf{E}(z) = \frac{2\pi\sigma z\hat{\mathbf{z}}}{4\pi\epsilon_0} \int_0^a \frac{s' ds'}{(z^2+s'^2)^{3/2}}$$

The result of the integration gives the final answer (to integrate, use a substitution of $u^2=s'^2+z^2$ and remember that $\sqrt{z^2}=|z|$).

$$\mbox{(1)}\qquad\mathbf{E}(z) = \frac{\sigma z}{2\epsilon_0} \left(\frac{1}{|z|}-\frac{1}{\sqrt{a^2+z^2}}\right)\hat{\mathbf{z}}$$

I gave full credit if you were able to get this equation.

The point of questions 1.-3. was to provide a check to your math for part 4. These checks were not asked for but are given below.

For $z<<a$, only the first term in parenthesis is large

$$\mathbf{E} = \frac{\sigma}{2\epsilon_0}\frac{z}{|z|}\hat{\mathbf{z}}$$

Notice how the $\frac{z}{|z|}$ term tells use the direction of the electric field. When $z>0$, this term is $+1$. When $z<0$, this term is $-1$. Also note how this matches the answer to question 3.

For $z>>a$, we need to do a bit more work on the second term in parentheses in (1). Factor out a $z$ from the square root to get

$$\mathbf{E} = \frac{\sigma z}{2\epsilon_0} \left(\frac{1}{|z|}-\frac{1}{|z|\sqrt{1+a^2/z^2}}\right)\hat{\mathbf{z}}$$

Because $a/z << 1$, we can use the binomial expansion to get

$$\mathbf{E} \simeq \frac{\sigma z}{2\epsilon_0} \left[\frac{1}{|z|}-\frac{1}{|z|}\left(1-\frac{a^2}{2z^2}\right)\right]\hat{\mathbf{z}}$$

Simplifying gives

$$\mathbf{E} \simeq \frac{\sigma}{2\epsilon_0} \frac{a^2}{2z^2}\frac{z}{|z|}\hat{\mathbf{z}}$$

which matches the prediction from 2.

## Shell of Charge

A shell centered at the origin and having a radius of $a$ has a charge $Q$ uniformly spread over it.

Although $\mathbf{E}$ and $V$ can be computed using Gauss' Law, answer the first two problems using the method used for computing the electric potential and electric field that you would use for the previous charged disk problem.

1\. Find $V$ on the $z$-axis in terms of constants times a single integral.
2\. Find $\mathbf{E}$ on the $z$-axis in terms of constants and optionally times one or more integrals.
3\. At the origin, what is expected for $\mathbf{E}$, and why?
4\. On the $z$-axis and for $z\lesssim a$, what is expected for $\mathbf{E}$, and why?
5\. On the $z$-axis and for $z\gtrsim a$, what is expected for $\mathbf{E}$, and why?
6\. On the $z$-axis and for $z>> a$, what is expected for $\mathbf{E}$, and why?
7\. If this question was modified to ask you for answers along the $x$ or $y$ axis, how would your answers change?

All final equations should be expressed in terms of $k$ or $\epsilon_0,Q$, and $a$ using any coordinate system.

## Square of Charge

A square non-conducting sheet of charge with side length $w$ has a uniform charge density of $\sigma_o$, lies in the $x-y$ plane, and is centered on the origin.

1\. Find an integral or integrals that must be evaluated to find $\mathbf{E}(z)$, the electric field on the $z$-axis.
2\. Evaluate the integral or integrals and show that for $z/w\ll 1$, $\mathbf{E}(z)$ reduces to the equation for an infinite non-conducting sheet of charge.

**Solution**

There are several ways to solve this problem. On can first find the field for a line of charge with a charge density of $\lambda$ and length $w$ that lies on the $x$-axis and is centered on the origin - the result is (see Griffiths 4th Edition example 2.2):

$$\mathbf{E}(z)=\frac{k\lambda w}{z\sqrt{z^2+w^2/4}}\hat{\mathbf{z}}$$

Then integrate the field due to differential lines of charges. One needs to account for the fact that the $z$ in this equation will not be the same as the $z$ in this problem. If the differential lines of charge are in the $x$-$y$ plane and lie on the line $x=x'$, then replace the $z$ with $z^2+x'^2$ and use $\lambda = \sigma_odx'$, You can check your answer for this approach by using the result of the following approach after integration with respect to $x'$. 

$$\mathbf{E}_{dq'}(x,y,z) = \frac{dq'}{4\pi\epsilon_0}\frac{\hat{\textbf{\char"0509}}}{\unicode{x0509}^2}$$

A second approach requires two integrations. Start with

$$\mathbf{E}_{dq'}(x,y,z) = \frac{dq'}{4\pi\epsilon_0}\frac{\hat{\textbf{\char"0509}}}{{\char"0509}^2}$$

which expands to

$$\mathbf{E}_{dq'}(x,y,z) =\frac{dq'}{4\pi\epsilon_0}\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|^3}$$

(A third approach is to find the potential $\Psi_{dq'}(x,y,z) = dq'/(4\pi\epsilon_0{\char"0509})$ and then use $\mathbf{E}=-\nabla \Psi$.)

and the general definitions

$$\mathbf{r}=x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}$$

$$\mathbf{r}'=x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}+z'\hat{\mathbf{z}}$$

In this problem, $z'=0$ because all charges are in the $x-y$ plane. Using $dq' = \sigma_odx'dy'$, gives

$$\mathbf{E}(x,y,z) = \int_{-w/2}^{w/2}\int_{-w/2}^{w/2}\frac{ \sigma_odx'dy'}{4\pi\epsilon_0}\frac{(x-x')\hat{\mathbf{x}}+(y-y')\hat{\mathbf{y}}+z\hat{\mathbf{z}}}{\big((x-x')^2+(y-y')^2+z^2\big)^{3/2}}$$

$\mathbf{E}(z)$ is obtained by setting $x=y=0$:

$$\mathbf{E}(z) = \int_{-w/2}^{w/2}\int_{-w/2}^{w/2}\frac{ \sigma_odx'dy'}{4\pi\epsilon_0}\frac{-x'\hat{\mathbf{x}}+-y'\hat{\mathbf{y}}+z\hat{\mathbf{z}}}{\big(x'^2+y'^2+z^2\big)^{3/2}}$$

The $\hat{\mathbf{x}}$ and $\hat{\mathbf{y}}$ integrals are zero because their integrands are odd functions. Many students argued they are zero "by symmetry". The word "symmetry" is too general because there are many types of symmetry. It is better to state what kind of symmetry: consider differential charges at $(x,y)$ and $(-x,-y)$ - their horizontal electric fields exactly cancel (ideally provide a diagram). The sheet of charge can be constructed by placing charges with canceling horizontal components and so the horizontal electric field is zero.

To simplify the integration for the $\hat{\mathbf{y}}$ term, define

$$I = \int_{-w/2}^{w/2}dy'\int_{-w/2}^{w/2}\frac{dx'}{(x'^2+a^2)^{3/2}}$$

where $a^2\equiv y'^2+z^2$ and then $E_z(z)=k\sigma_ozI$. This integral can be looked up or found using Mathematica or Wolfram Alpha. Some students reported "computation time exceeded" with Wolfram Alpha. This was probably caused by entering the double integral instead of doing a single integral at a time.

Integration with respect to $x'$ gives

$$I= \int\_{-w/2}^{w/2}dy'\frac{x'}{a^2(x'^2+a^2)^{1/2}}\Bigg|\_{-w/2}^{w/2}=\int\_{-w/2}^{w/2}dy'\frac{w}{a^2(a^2+w^2/4)^{1/2}}$$

Using the earlier definition $a^2\equiv y'^2+z^2$ and a new definition $b^2\equiv z^2+w^2/4$ gives

$$I=\int_{-w/2}^{w/2}\frac{wdy'}{(y'^2+z^2)\sqrt{y'^2+b^2}}$$

This integral can be looked up and the result is (using $\tan^{-1}(u)=-\tan^{-1}(u)$)

$$I=\frac{4}{z}\tan^{-1}\left[\frac{w^2}{4z}\frac{1}{\sqrt{z^2+w^2/2}}\right]$$

The final result, using $E_z(z)=k\sigma_ozI$ defined earlier, is 

$$E_z(z)=\frac{\sigma_o}{\pi \epsilon_o}\tan^{-1}\left[\frac{w^2}{4z}\frac{1}{\sqrt{z^2+w^2/2}}\right]$$

For $z\ll w$, the argument to the inverse tangent is

$$\frac{w^2}{4z}\frac{1}{\sqrt{z^2+w^2/2}}\simeq \frac{w}{z}\frac{\sqrt{2}}{4}$$

so for $z \gt 0$ and $z\ll w$

$$E_z(z)\rightarrow\frac{\sigma_o}{\pi\epsilon_o}\tan^{-1}(+\infty) = \frac{\sigma_o}{2\epsilon_o}$$

For $z \lt 0$ and $z\ll w$

$$E_z(z)\rightarrow\frac{\sigma_o}{\pi\epsilon_o}\tan^{-1}(-\infty) = -\frac{\sigma_o}{2\epsilon_o}$$

and so the solution matches that for an infinite sheet of charge. Another problem one could ask is to show that for $z\gg w$, $E_z\rightarrow k\sigma_ow^2/z^2$ (far away, the sheet of charge appears as a charge $\sigma_ow^2$ at the origin). To show this, one would need to Taylor series expand the argument of the inverse tangent for small $w/z$.

## Quarter circle

Compute $\mathbf{E}$ at the center of quarter circle.

