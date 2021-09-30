# Introduction

See also 3.1 of Griffiths.

## Overview

Many laws of physics are expressed as either ordinary differential equations or partial differential equations.

Recall from mechanics that the equation for the position of a particle in a uniform gravitational field is given by the ordinary differential equation

$$m\frac{d^2x}{dt^2}=-mg$$

This equation does not explicitly give the position of a mass versus time. To determine, one must first obtain a solution to this equation.

A general solution for $x(t)$ has the form

$$x(t)=C_1+C_2t-gt^2/2$$

where $C_1$ and $C_2$ are two constants.

To use this equation to find $x(t)$ for a mass, the values of the two constants must be known. Usually these two constants are determined based on the initial values of $x$ and $dx/dt$. For example, if $x(t=0)=0$ and $v(t=0)=0$, then $C_1=C_2=0$ and the trajectory of the mass is given by $x(t)=-gt^2/2$.

This type of problem is called an **initial value problem** -- given a differential equation for the position of the mass and it's initial values of $x$ and $v$, we arrive at a solution for $x$ for all $t$. Another example of an inital value problem is for the position $x$ of a mass on a spring. The differential equation for $x$ is $d^2x/dt^2-\omega_o^2x=0$. A general solution is $x(t)=C_1\sin(\omega_o t)+C_2\cos(\omega_o t)$.

A **boundary value problem** involves first finding a general solution to a partial differential equation with respect to the position (instead of time). The solution will have constants whose values are determined by the conditions at the boundary. For example, in electrostatics

$$\frac{\partial^2 V}{\partial x^2}=0$$

is a partial differential equation for $V$ for a system where the symmetry is such that the potential only depends on $x$. If we want to know $V(x)$, we need to know a general solution to this equation. It is

$$V(x)=C_1 + C_2x$$

The values for $C_1$ and $C_2$ are determined based on boundary conditions. For example, $V(x=0)=0$ and $V(x=L)=V_o$.

In this course, you will only be required to know how to derive the general solution for partial differential equations in 1--D for cartesian, cylindrical, and spherical coordinates.  Derivations are given in the [1--D section](#1-d).

For 2-- and 2--D partial differential equations, you will be given the general solution and asked to find the unknown constants given boundary value information.

## Finding $V$

There are generally two types of problems involving $V$ in electrostatics:
1. given the locations of charges, compute the electric potential and electric field at all locations in space; and
2. given the electric potential at certain locations in space, compute the electric potential and electric field at all locations in space.

### Type 1 Problems

For problems of type 1., we can compute $V$ using

$$V(\mathbf{r})=\sum_{i=1}^{N} \frac{kq\_{i}}{|\mathbf{r}-\mathbf{r}\_{i}'|}$$

for $N$ discrete charges, or the continuous approximation 

$$V(\mathbf{r})=\int \frac{kdq}{|\mathbf{r}-\mathbf{r}'|}$$

along with a given line, surface, or volume charge density ($\lambda, \sigma$, or $\rho$, respectively).

In many problems, we don't know the locations of the charges in the system. Consider the scenario shown in the following figure in which a net charge of $Q$ is placed on a conductor. 

<img src="figures/Boundary_Value_Problems.svg"/>

The charges on the conductor will distribute themselves so that the electric field in the conductor is zero. In general, we don't know what the distribution will be -- we only know that whatever it is, it is such that the electric field is zero inside.

If the top cap is centered on the origin and in the $x$--$y$ plane, to compute the potential due to the top cap outside of the conductor, we may be tempted to start with

$$V(\mathbf{r})= \int_0^{2\pi}\int_0^R \frac{k\sigma(s')}{|\mathbf{r}-s'\hat{\mathbf{s}}|}s'ds'd\phi'$$

which was the approach used to find the potential due to charges distributed on a disk with a given $\sigma(s)$. However, in this case, we don't know $\sigma(s)$ and so we are stuck. A brute-force method of computing $\sigma$ uses the fact that the $V$ must be constant on the conductor: guess $\sigma$ the top, bottom, and side surfaces, compute $V$ using integration, and then repeat until a $V$ is found that is constant on the conductor.

In summary, we can only use the integral formula for $V$ if the charge densities are known. In general, if we place a net charge on a conductor, we do not know how it will distribute on its surface.

### Type 2 Problems

Problems of type 2. are called **boundary value problems** and are generally solved by finding solutions to a partial differential equation called Poisson's equation:

$$\nabla^2 V= -\frac{\rho}{\epsilon_0}$$

$\nabla^2$ is a new form of operator. It involves operation on a scalar function $f$ and results in a scalar function. In cartesian coordinates, 

$$\displaystyle \nabla^2f=\frac{\partial^2 f}{\partial x^2}+\frac{\partial^2 f}{\partial y^2}+\frac{\partial^2 f}{\partial z^2}$$

Therefore, Poisson's equation in cartesian coordinates is

$$\frac{\partial^2 V}{\partial x^2}+\frac{\partial^2 V}{\partial y^2}+\frac{\partial^2 V}{\partial z^2}=-\frac{\rho}{\epsilon_0}$$

Similar to the divergence and gradient operators, the $\nabla^2$ operator (also called the Laplacian or "del squared") has different forms for each coordinate system. These are given on the second--to last page of Griffiths.

Laplace's equation is Poisson's equation with $\rho=0$:

$$\nabla^2 V = 0$$

In cartesian coordinates, it is

$$\frac{\partial^2 V}{\partial x^2}+\frac{\partial^2 V}{\partial y^2}+\frac{\partial^2 V}{\partial z^2}=0$$

### Deriving Poisson's Equation

Poisson's Equation, $\nabla^2 V= -{\rho}/{\epsilon_0}$, follows directly from inserting the definition of the electric potential $\mathbf{E}=-\nabla V$ into Gauss' Law in differential form $\nabla\bfcdot\mathbf{E}=\rho/\epsilon_0$.

Gauss's law in differential form is

$$\nabla\bfcdot\mathbf{E}=\frac{\rho}{\epsilon_0}$$

Using $\mathbf{E}=-\boldsymbol{\nabla}V$, this is

$$\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)=\frac{\rho}{\epsilon_0}$$

To evaluate $\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)$, first write $\boldsymbol{\nabla}V$ in cartesian

$$\boldsymbol{\nabla}V=\xhat\frac{\partial V}{\partial x}+\yhat\frac{\partial V}{\partial y}+\zhat\frac{\partial V}{\partial z}$$

Then

$$\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)=\boldsymbol{\nabla}\bfcdot\left(-\xhat\frac{\partial V}{\partial x}-\yhat\frac{\partial V}{\partial y}-\zhat\frac{\partial V}{\partial z}\right)$$

Using the definition of divergence of a vector function $\mathbf{U}$, which is

$$\boldsymbol{\nabla}\bfcdot\mathbf{U}=\xhat\frac{\partial U_x}{\partial x}+\yhat\frac{\partial U_y}{\partial y}+\zhat\frac{\partial U_z}{\partial z}$$

with $U_x=-\partial V/\partial x$, $U_y=-\partial V/\partial y$, $U_z=-\partial V/\partial z$ gives

$$\boldsymbol{\nabla}\bfcdot\left(-\xhat\frac{\partial V}{\partial x}-\yhat\frac{\partial V}{\partial y}-\zhat\frac{\partial V}{\partial z}\right)=-\frac{\partial^2 V}{\partial x^2}-\frac{\partial^2 V}{\partial y^2}-\frac{\partial^2 V}{\partial z^2}$$

and so 

$$\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)=-\frac{\partial^2 V}{\partial x^2}-\frac{\partial^2 V}{\partial y^2}-\frac{\partial^2 V}{\partial z^2}$$

and

$$-\frac{\partial^2 V}{\partial x^2}-\frac{\partial^2 V}{\partial y^2}-\frac{\partial^2 V}{\partial z^2}=\frac{\rho}{\epsilon_0}$$

Moving the negative sign and using the definition of the Laplacian $\nabla^2$, gives Poisson's equation

$$\nabla^2V=-\frac{\rho}{\epsilon_0}$$

### Problem

Outside of a solid sphere of radius $R$ with uniformly distributed charge $Q$, the field is

$\displaystyle V(r)=kQ\frac{1}{r}$

inside, it is

$\displaystyle V(r)=\frac{kQ}{2R}\left[1-\frac{r^2}{R^2}\right]$

Compute $\nabla^2 V$ and verify that $\nabla^2V=-\frac{\rho}{\epsilon_0}$ inside and outside of the sphere. You may use the formula for $\nabla^2$ in any coordinate system. 

# 1-D

See also 3.2 of Griffiths.

## Cartesian

Suppose that we connect a battery with a potential difference $V_o$ to two large conducting plates. We want to know how $V$ varies between the plates.

<img src="figures/Parallel_Plates_Example.svg"/>

This problem can be solved using two approaches.
1. By assuming the potential causes equal and opposite amount of charge to be uniformly distributed on the plates. This approach can only be used because we know (or assume) how the charges will distribute on the surfaces. If the plates were not large, we could not use this method.
2. By using the boundary value method.
 
### Charge Method


Assume charges of $\pm Q$ appear on the plates when the battery is connected so that the surface charge densities are $\pm Q/A$ and use the method demonstrated in the [capacitance notes](capacitance.html) notes to find $V$.

The electric field between the plates is $\mathbf{E}=-\sigma/\epsilon_o\xhat$. Using $V(x)=V(a)-\int_a^x\mathbf{E}\bfcdot d\mathbf{l}$ with $a=0$ and $d\mathbf{l}=dx'\xhat$

$\displaystyle V(x)=V(0)-\int_0^x -\frac{\sigma}{\epsilon_o}dx'$

Integration gives

$\displaystyle V(x) = V(0)+\frac{\sigma}{\epsilon_o}x$

We are not done because we need to write $\sigma$ in terms of $V_o$. To compute $\sigma$, plug in $x=d$ to get

$\displaystyle V(d)-V(0)=\frac{\sigma}{\epsilon_o}d$

The difference in potential $V(d)-V(0)$ was given as $V_o$. Substitution gives

$\displaystyle V_o=\frac{\sigma}{\epsilon_o}d\quad\Rightarrow\quad \sigma=\epsilon_o\frac{V_o}{d}$

Plugging this $\sigma$ into $\displaystyle V(x) = V(0)+\frac{\sigma}{\epsilon_o}x$ gives

$\displaystyle V(x)=V(0)+V_o\frac{x}{d}$

### Laplace's Equation Method

This problem may also be solved using Laplace's equation.

Between the plates, there are no charges, so $\rho=0$ and Laplace's equation applies. If the plates are large, then the potential will only vary in the $x$--direction, in which case Laplace's equation in cartesian components simplifies to:

$\displaystyle\nabla^2V = \frac{\partial^2 V}{\partial x^2} = 0$

This can be written as 

$\displaystyle\nabla^2V = \frac{d^2 V}{dx^2} = 0$

because $V$ only depends on $x$. This equation can be integrated twice to give

$\displaystyle V(x)=ax+b$

where $a$ and $b$ are constants. You can verify that $V = ax+b$ satisfies $\partial^2 V/\partial x^2 = 0$ by differentiating it twice with respect to $x$.

The interpretation of this equation is that in a configuration where it can be argued that potential only depends on $x$, the potential must increase or decrease linearly. In this example, the two boundary conditions are

1. $V(x=0)=0$
2. $V(x=d)=V_o$

These two conditions give two equations that can be solved to find the unknown constants $a$ and $b$:

$\displaystyle V(x=0)=0=a\cdot 0+b \Rightarrow b = 0$

$\displaystyle V(x=d)=V_o=ad+b=ad+0 \Rightarrow a=V_o/d$

so the solution is

$\displaystyle V(x) = \frac{V_o}{d}x$

This is the same result found using the charge method if we set $V(0)=0$ in the charge method equation to be consistent with what was used in Laplace's equation method.

After developing a solution to Laplace's equation, one should always verify that the solution matches the boundary conditions, in this case by plugging in the coordinates of the boundary:

1. $V(x) = \frac{V_o}{d}x \Rightarrow V(0)=0$ so the solution matches the $x=0$ boundary condition
2. $V(x) = \frac{V_o}{d}x \Rightarrow V(d)=V_o$ so the solution matches the $x=d$ boundary condition

1-D examples are simple. As will be seen when 2- and 3-D problems are considered, typically, one cannot find a single equation that satisfies all boundary conditions by following this method; a function can be found that satisfies some but not all of the boundary conditions. To fully solve the problem, one has to rely on the so-called "Fourier Trick" to find a solution. This method is described in the section on 2-D Cartesian.

### Problems

#### Checking Solution

A student came up with the following equation for the potential between the plates: $V(x)/V_o = e^{\tan^{-1}(x+1/2)} + x^3 - 1/\sqrt{x^2-1} + \tanh(1/\sqrt{e^x}+4\pi)$.  Without doing a calculation, we know this is wrong or the expression simplifies to $V(x)=V_ox/d$. Why?

%4. You have computed $V$ that satisfied Laplace's Equation and the boundary conditions. This solution is unique. Some students noted that the cubic term would not be zero after differentiating it twice and so the potential would not satisfy Laplace's Equation. But, this term could have been canceled by another term that appeared after taking the second derivative. The point of this problem was to make sure that you understood the uniqueness theorem, which is import for image problems.

## Cylindrical

Two long conducting cylinders of radius $a$ and $b$ are configured as shown in the following figure.

<img src="figures/Boundar_Value_Problems_Cylinder.svg"/>

Assume the potential on the inner cylinder is $V_o$ and that on the outer cylinder is $0$.

The cylinders are conductors, and if they are long relative to their radius, the charges that appear on them will be approximately uniformly distributed on their surfaces. If the charge distribution is independent of $\phi$ and $z$, the potential will not depend on $\phi$ and $z$. So $V=V(s)$.

In cylindrical coordinates, the Laplacian is 

$$\nabla^2V={1 \over s}{\partial \over \partial s}\left(s {\partial V \over \partial s}\right) + {1 \over s^2}{\partial^2 V \over \partial \phi^2} + {\partial^2 V \over \partial z^2}$$

if $V=V(s)$, the derivatives in the second and third terms are zero, and so 

$$\nabla^2 V={1 \over s}{\partial \over \partial s}\left(s {\partial V \over \partial s}\right)$$

Because $V$ depends only on $s$, we can replace the partial derivative with the total derivative to obtain the ODE

$$\nabla^2 V={1 \over s}{d \over d s}\left(s {d V \over d s}\right)=0$$

The boundary conditions are

1. $V(a)=V_o$
2. $V(b)=0$

To solve the ODE, note that because $1/s$ is not zero, the only way for the left-hand side of

$${1 \over s}{d \over d s}\left(s {d V \over d s}\right)=0$$

to be zero is if

$$s {d V \over d s}=C_1$$

where $C_1$ is a constant. Direct integration of this equation gives

$$V(s) = {C_1 \ln s} + C_2$$

The two unknowns are solved for by using the boundary conditions

$$V(b) = 0 = {C_1 \ln b} + C_2 \Rightarrow C_2=-C_1\ln b$$

$$V(a) = V_o = {C_1 \ln a} + C_2\Rightarrow V_o=C_1(\ln a-\ln b)=C_1\ln(a/b)$$

Solving for $C_1$ and $C_2$ gives

$$C_1 = {V_o \over \ln(a/b)}$$
$$C_2 = -{{V_o / \ln b} \over \ln(a/b)}$$

Subsitution of these constants into $V(s) = {C_1 \ln s} + C_2$ gives

$$V(s) = {V_o \over \ln(a/b)}\left(\ln s - \ln b \right)$$

as a check of the algebraic steps, plug in $s=a$ and $s=b$ into this equation and verify that the boundary conditions used, $V(a)=V_o$ and $V(b)=0$ are satisfied.

The electric field can be found using $\mathbf{E}=-\nabla V$. In cylindrical coordinates, when $V$ depends only on $s$, the negative of the gradient of $V$ is given by

$$-\nabla V=-{\partial V \over \partial s} \hat{\mathbf{s}}$$

Evaluation of the derivative gives

$$\mathbf{E}=-{V_o \over \ln(a/b)}{1 \over s}\hat{\mathbf{s}}$$

Using $-\ln(a/b)=\ln(b/a)$, this can also be written as

$$\mathbf{E}={V_o \over \ln(b/a)}{1 \over s}\hat{\mathbf{s}}$$

This field points from $a$ to $b$ (in $+\hat{\mathbf{s}}$ direction) as expected because the potential on the inner surface is higher than that on the outer surface.

### Problem

For the example given, find $\mathbf{E}(s)$ between the cylinders using the charge method.

## Spherical

### Problem

Two conducting and concentric spherical shells with radius $a$ and $b$ (assume $b>a$) are at potential $V_o$ and $0$, respectively.

1. Find $V(r)$ between the spheres using Laplace's equation method.
2. Find $\mathbf{E}(r)$ between the spheres using the charge method.

# 2--D Cartesian

See also 3.3.1 of Griffiths.

## General Solution

Laplace's equation in 2-D cartesian coordinates is 

$$\nabla^2V = \frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} = 0$$

For arbitrary constants $A,B,C,D,$ and $m$ the following four equations satisfy it

1. $V(x,y) = \big(A\cosh mx+B\sinh mx\big)\big(C\cos my+D\sin my\big)$
2. $V(x,y) = \big(A\cos mx+B\sin mx)(C\cosh my+D\sinh my\big)$
3. $V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos my+D\sin my\big)$
4. $V(x,y) = \big(A\cos mx+B\sin mx\big)\big(Ce^{my}+De^{-my}\big)$

(This can be shown using the method of Separation of Variables covered in Chapter 3 of Griffiths. I use $m$ on this page instead of $k$ as is done in the text because I have been using $k$ for $1/(4\pi\epsilon_0)$.) 

All four forms are equivalent in the sense that the constants in one equation can be written in terms of constants in any of the other equations. For example, if we write form 3. as $V(x,y) = \big(A'e^{m'x}+Be^{-m'x})(C'\cos m'y+D'\sin m'y\big)$, then one can show that $A=(A'+B')/2$, $B=(A'-B')/2$, $C=C'$, $D=D'$, and $m=m'$.


The reason that all four forms are listed is that for certain problems, a certain choice of the form to start with leads to less algebra. 

The general solution steps are

1. Start with one of the forms 1.--4. and use the boundary conditions to find an equation that satisfies some of the four boundary conditions. There is no general rule about which form to start with beyond considering a few boundary conditions and looking at which equation will give coefficients that are zero immediately.
2. Use superposition and Fourier's trick to find an equation that satisfies all four boundary conditions.

## Solution Step 1.

Start with one of the forms 1.--4. and use the boundary conditions to find an equation that satisfies some of the boundary conditions. 
 
%In examples 3.3 and 3.4 of Griffiths, which are 2-D cartesian problems, he comes up with an equation for $V(x,y)$ that satisfies three of the four boundary conditions and has one unknown constant:

%Example 3.3: 

%$$V(x,y) = Ce^{-n\pi x/a}\sin(n\pi y/a)\mbox{ with } n=1,2,...$$

%Example 3.4:

%$$V(x,y) = C\cosh(n\pi x/a)\sin(n\pi y/a)\mbox{ with } n=1,2,...$$

%The capital letter used for the leading constant can be $A,B,C,$ or $D$ or a combination of them (the product of constants is a constant); in the derivation of the above two equations, Griffiths notes that the $C$ in the final equations is not the same as the $C$ in the original equations (one of forms 1.--4.). Technically it would be better to use something like $C'$ in the final equation to emphasize this point, but to keep the notation simple, he redefines $C$.

In Examples 3.3 and 3.4, Griffiths happens to choose

1. The best form 1.--4. to start with
2. The best order of boundary conditions to address

The problem students have with solving other problems is when they don't happen to choose the "best" way to get to the answer. In the following, I go through examples 3.3 and 3.4 by addressing the boundary conditions in a different order than Griffiths did. In doing so, I highlight some of the actual complications one will encounter if the "best" order of addressing the boundary conditions is not selected.

Prior to reading the following two examples, read Griffiths' solutions to Example 3.3 and 3.4.

### Example 3.3

The boundary conditions are

1. $V = 0$ when $y = 0$
2. $V = 0$ when $y = a$
3. $V = V_o(y)$ when $x = 0$ -- (Griffiths starts with $V_o(y)$ and then gives the solution for $V=V_o=const$)
4. $V\rightarrow 0$ as $x\rightarrow\infty$

Griffiths starts with form 3.

$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos my+D\sin my\big)$

and boundary condition 4. Here I am going to start with form 3. but boundary condition 1.

**BC 1.**: $V = 0$ when $y = 0$

Plugging $V = 0$ and $y = 0$ into

$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos my+D\sin my\big)$

gives

$0 = \big(Ae^{mx}+Be^{-mx})(C\cos m0+D\sin m0\big)$

or

$0 = \big(Ae^{mx}+Be^{-mx}\big)C$

There are two ways for this equation to be true for any $x \ge 0$

1. Both $A$ and $B$ are zero. We reject this option because then form 3. reduces to $V(x,y)=0$, which satisfies Laplace's equation, but can't satisfy all of the boundary conditions.
2. $C=0$.

If $C=0$, we are left with

$V(x,y) = \big(Ae^{mx}+Be^{-mx}\big)D\sin my$

or, defining $A'=AD$ and $B'=BD$,

$V(x,y) = \big(A'e^{mx}+B'e^{-mx}\big)\sin my$

**BC 2.**: $V = 0$ when $y = a$

Plugging these values into the equation we left off with after addressing boundary condition 1. gives

$0 = \big(A'e^{mx}+B'e^{-mx}\big)\sin ma$

There are two ways for this equation to be true for any $x \ge 0$:

1. Both $A'$ and $B'$ are zero. We reject this option because then we are left with $V(x,y)=0$, which satisfies Laplace's equation, but can't satisfy all of the boundary conditions.
2. $\sin ma=0$.

The only way for $\sin ma=0$ to be true generally is if $ma=0,\pm \pi,\pm 2\pi,...$. 

From this, we conclude

$m=\frac{n\pi}{a}$ with $n$ constrained to be $0, \pm 1, \pm 2, ...$

This leaves

$V(x,y) = \big(A'e^{n\pi x/a}+B'e^{-n\pi x/a}\big)\sin n\pi y/a$

Inspection of this equation allows us to reject the possibility that $n=0$; if $n=0$, this equation reduces to $V(x,y)=0$, which cannot satisfy all of the boundary conditions.

**BC 3.**: $V = V_o$ when $x = 0$

Plugging these values into the equation we left off with after addressing boundary condition 2. gives

$V_o = \big(A'e^{n\pi 0/a}+B'e^{-n\pi 0/a}\big)\sin n\pi y/a$

or, because $e^0=1$,

$V_o = \big(A'+B'\big)\sin n\pi y/a$


This equation is true but is not immediately useful for simplifying our equation for $V(x,y)$. So we move on to the next boundary condition.

**BC 4.**: $V = 0$ when $x \rightarrow \infty$

Plugging these values into the equation we left off with after addressing boundary condition 2. gives

$0 = \big(A'e^{n\pi \infty/a}+B'e^{-n\pi \infty/a}\big)\sin n\pi y/a$

or, because $e^{-\infty}=0$,

$0 = \big(A'e^{n\pi \infty/a}\big)\sin n\pi y/a$

There is only one way for this equation to be true: $A'=0$. (There is technically a mathematical issue that I am ignoring because zero times infinity is indeterminate; there is a way around this issue, but for now, it is not important and I'll use this dubious notation.)

This leaves

$V(x,y) = B'e^{-n\pi x/a}\sin n\pi y/a$

which the same as equations 3.28 and 3.29 with one exception. In the above I concluded $n$ could be $\pm 1, \pm 2, ...$ where Griffiths concludes $n=1, 2, 3, ...$. The equivalence of these two conclusions will be shown when $B'$ is computed.

The final step is determining $B'$. This would seem to be impossible because boundary condition 3., $V = V_o$ when $x = 0$, gives

$V_o = B'e^{-n\pi 0/a}\sin n\pi y/a=B'\sin(n\pi y/a)$

and this equation needs to hold true for any $0\le y \le a$. Another way to show that finding a $B'$ that satisfies boundary condition 3. is impossible, suppose $y=a/2$ and $n=1$, then we have

$V_o = B'e^{-n\pi 0/a}\sin n\pi y/a=B'\sin(\pi/2)$

Giving $B'=V_o$. Now suppose $y=a/4$ and $n=1$, then

$V_o = B'e^{-n\pi 0/a}\sin n\pi y/a=B'\sin(\pi/4)$

Giving $B'=\sqrt{2}V_o$. One can repeat this for all allowed values and $n$ and you will come to the conclusion that there is no single value of $B'$ that can satisfy this equation for any $0\le y \le a$.

To satisfy this last boundary condition, superposition and "Fourier's Trick" is needed, which is covered in [step 2](#solution-step-2).

### Example 3.4

The boundary conditions are

1. $V = 0$ when $y = 0$
2. $V = 0$ when $y = a$
3. $V = V_o$ when $x = b$
4. $V = V_o$ when $x = -b$

Griffiths starts with form 3.

$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos my+D\sin my\big)$

and a symmetry argument to conclude $A=B$. Here I am going to start with form 3. but boundary condition 1. In addition, I won't make use of the symmetry argument.

**BC 1.**: $V = 0$ when $y = 0$

**BC 2.**: $V = 0$ when $y = a$

The starting form 3. and boundary conditions 1. and 2. are identical to that from example 3.3, so we can re-use the result concluded from addressing them:

$V(x,y) = \big(A'e^{n\pi x/a}+B'e^{-n\pi x/a}\big)\sin n\pi y/a$

with $n$ constrained to be $0, \pm 1, \pm 2, ...$.

**BC 3.**: $V = V_o$ when $x = b$

Plugging the boundary values into the equation we left off with after addressing boundary condition 2. gives

$V_o = \big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)\sin n\pi y/a$

Now we seem stuck. How does one constrain $A'$ and $B'$ for this equation to hold? We have one other boundary condition to address, so hopefully, it provides some insight.

**BC 4.**: $V = V_o$ when $x = -b$

$V_o = \big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin n\pi y/a$

Here we would seem to be stuck again. However, notice that the equation here can be combined with that from BC 3:

$\big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)\sin n\pi y/a=\big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin n\pi y/a$

The $\sin n\pi y/a$ term appears on both sides and can be dropped, leaving

$\big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)=\big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)$

which simplifies to

$A'\big(e^{n\pi b/a}-e^{-n\pi b/a}\big)=B'\big(e^{n\pi b/a}-e^{-n\pi b/a}\big)$

The terms in parentheses are identical, so we conclude

$A'=B'$

Therefore, the equation we ended with when addressing BC 2.,

$V(x,y) = \big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin n\pi y/a$

simplifies to

$V(x,y) = A'\big(e^{-n\pi x/a}+e^{n\pi x/a}\big)\sin n\pi y/a$

This can be futher simplified using the definition $\cosh z=(e^z+e^{-z})/2$

$V(x,y) = 2A'\cosh(n\pi x/a)\sin(n\pi y/a)$

This equation is equivalent to Griffiths' 3.41 if $2A'$ is replaced with a constant labeled $C$. As with example 3.3, we ended up with one constant that is still unknown. 

Note that $n=0$ would give $V(x,y)=0$, which does not satisfy all of the boundary conditions. As a result, the allowed values of $n$ are $\pm 1, \pm 2, ...$. 

As was the case in my solution to example 3.3, above I concluded $n$ could be $\pm 1, \pm 2, ...$ where Griffiths concludes $n=1, 2, 3, ...$. The equivalence of these two conclusions will be shown when $A'$ is computed in [step 2.](#solution-step-2).

## Step 2 preparation

### Integrals

1. Show that $\int_0^\pi \sin 2x \sin x dx$ = 0. Note that without any calculation, this is expected from a plot of $\sin x$ and $\sin 2x$ and thinking about the area under the curve for their product.

2. Show that $\int_0^\pi \sin nx \sin lx dx$ = 0 if $l\ne n$ by explicitly evaluating the integral.

3. Compute $\int_0^\pi \sin^2 nx dx$ for (a) any $n\ne 0$ and (b) for integer $n$.


**Comment**:

The motivation for giving you these problems is to help you remember that

$\int_0^\pi \sin nx \sin lx dx = 0$ if $l\ne n$ which is important for Fourier sum problems.

A way to reason this out without doing a calculation is by considering a plot of the integrand $\sin nx\sin lx$ over the interval $0\le x\le \pi$ by plotting two $\sin$ curves for $l\ne m$ and thinking about what the product of the curves looks like; over half interval the product will be positive and over the other half of the interval it will be negative, so the integral will be zero.

When $l=m$, the integrand is $\sin^2 mx$, which is always positive, so its integral is not zero over any interval of $x$.

%**Answer**

%3\. For $n \gt 0$, $\frac{\pi}{2}-\frac{\sin(2\pi n)}{4n}$

### Series sums

Show that

$V(x,y) = C_1e^{-\pi x/a}\sin\pi y/a + C_2e^{-2\pi x/a}\sin 2\pi y/a + C_3e^{-3\pi x/a}\sin 3\pi y/a + ... $

satisfies Laplace's equation.

% and the boundary conditions of Example 3.3.

**Answer**

From a previous problem, we know that equations of this form of each term satisfy Laplace's equation. Here will show this again. Define these terms as

$V_n=C_ne^{-n\pi x/a}\sin n\pi y/a$

Then for any $n$,

\begin{aligned}
\nabla^2 V_n = & \\
= & \text{ } \nabla^2\big(C_ne^{-n\pi x/a}\sin [n\pi y/a]\big) \\
= & \text{ } C_n\sin [n\pi y/a]\frac{\partial^2 e^{-n\pi x/a}}{\partial x^2} + C_ne^{-n\pi x/a}\frac{\partial^2 \sin [n\pi y/a]}{\partial y^2} \\
= & \text{ } C_n \sin [n\pi y/a] (-n\pi x/a)(-n\pi x/a)e^{-n\pi x/a} + C_n e^{-n\pi x/a}(n\pi x/a)(-n\pi x/a)\sin [n\pi y/a] \\
= & \text{ } 0
\end{aligned}

The Laplacian of a sum can be written as the sum of Laplacians

$\displaystyle\nabla^2 (V_1+V_2+...) = \nabla^2 V_1 + \nabla^2 V_2 + ...$

Because $\nabla^2 V_n=0$, we conclude

$\displaystyle\nabla^2 (V_1+V_2+...) = 0 + 0 + ... = 0$

## Solution Step 2.

In this step, we start with an equation that satisfies two or three of the boundary conditions, but cannot satisfy the remaining one(s). Then,

1. Re--write one of the remaining boundary conditions as a sum of equations that satisfy the other boundary conditions and
2. Apply Fourier' trick: Multiply the equation from 1. by a $\sin$ or $\cos$ function and integrate.

### Example 3.3

The equation

$V(x,y) = Ce^{-n\pi x/a}\sin n\pi y/a$ with $n=0, \pm 1, ...$

satisfied three of the four boundary conditions in Example 3.3 but there is no $C$ or $n$ that can satisfy the last boundary condition $V(0,y)=V_o$:

$V_o = Ce^{-n\pi 0/a}\sin n\pi y/a=C\sin n\pi y/a$

As a result, we try a sum of terms with $n=1, 2, ...$

$V_o = C_1\sin \pi y/a + C_2\sin 2\pi y/a + C_3\sin 3\pi y/a + ... $

Multiplying this by $dy\sin l\pi y/a$ and integrating from $y=0$ to $y=a$ gives

**Equation A**:

$\displaystyle \int_0^a V_ody \sin (l\pi y/a) =$

$\displaystyle \phantom{\int_0^a V_ody \sin (l\pi y/a)
=}\phantom{+}C_1\int_0^a dy \sin (l\pi y/a) \sin (\pi y/a)$

$\displaystyle \phantom{\int_0^a V_ody \sin (l\pi y/a) =}+C_2\int_0^a dy\sin( l\pi y/a) \sin (2\pi y/a)$

$\displaystyle \phantom{\int_0^a V_ody \sin (l\pi y/a) =}+C_3\int_0^a dy \sin (l\pi y/a) \sin (3\pi y/a)$

$\displaystyle\phantom{\int_0^a V_ody \sin (l\pi y/a) =}+ ...$

To show that $C_1, C_2,$ and $C_3$ are

* $\displaystyle C_1=\frac{4V_o}{1\pi}$

* $\displaystyle C_2=0$

* $\displaystyle C_3=\frac{4V_o}{3\pi}$

set $l=1$ in Equation A and evaluate all of the integrals. This will give you $C_1$. Next, set $l=2$ in Equation A and evaluate all of the integrals.  This will give you $C_2$. Finally, set $l=3$ in Equation A and evaluate all of the integrals to get $C_3$.

%Do you see why the limits of integration were chosen to be $[0,a]$? If not, try finding $C_1,C_2,C_3$ using integration limits of $[0,a/3]$.

# Introduction

See also 3.1 of Griffiths.

## Overview

Many laws of physics are expressed as either ordinary differential equations or partial differential equations.

Recall from mechanics that the equation for the position of a particle in a uniform gravitational field is given by the ordinary differential equation

$$m\frac{d^2x}{dt^2}=-mg$$

This equation does not explicitly give the position of a mass versus time. To determine, one must first obtain a solution to this equation.

A general solution for $x(t)$ has the form

$$x(t)=C_1+C_2t-gt^2/2$$

where $C_1$ and $C_2$ are two constants.

To use this equation to find $x(t)$ for a mass, the values of the two constants must be known. Usually these two constants are determined based on the initial values of $x$ and $dx/dt$. For example, if $x(t=0)=0$ and $v(t=0)=0$, then $C_1=C_2=0$ and the trajectory of the mass is given by $x(t)=-gt^2/2$.

This type of problem is called an **initial value problem** -- given a differential equation for the position of the mass and it's initial values of $x$ and $v$, we arrive at a solution for $x$ for all $t$. Another example of an inital value problem is for the position $x$ of a mass on a spring. The differential equation for $x$ is $d^2x/dt^2-\omega_o^2x=0$. A general solution is $x(t)=C_1\sin(\omega_o t)+C_2\cos(\omega_o t)$.

A **boundary value problem** involves first finding a general solution to a partial differential equation with respect to the position (instead of time). The solution will have constants whose values are determined by the conditions at the boundary. For example, in electrostatics

$$\frac{\partial^2 V}{\partial x^2}=0$$

is a partial differential equation for $V$ for a system where the symmetry is such that the potential only depends on $x$. If we want to know $V(x)$, we need to know a general solution to this equation. It is

$$V(x)=C_1 + C_2x$$

The values for $C_1$ and $C_2$ are determined based on boundary conditions. For example, $V(x=0)=0$ and $V(x=L)=V_o$.

In this course, you will only be required to know how to derive the general solution for partial differential equations in 1--D for cartesian, cylindrical, and spherical coordinates.  Derivations are given in the [1--D section](#1-d).

For 2-- and 2--D partial differential equations, you will be given the general solution and asked to find the unknown constants given boundary value information.

## Finding $V$

There are generally two types of problems involving $V$ in electrostatics:
1. given the locations of charges, compute the electric potential and electric field at all locations in space; and
2. given the electric potential at certain locations in space, compute the electric potential and electric field at all locations in space.

### Type 1 Problems

For problems of type 1., we can compute $V$ using

$$V(\mathbf{r})=\sum_{i=1}^{N} \frac{kq\_{i}}{|\mathbf{r}-\mathbf{r}\_{i}'|}$$

for $N$ discrete charges, or the continuous approximation 

$$V(\mathbf{r})=\int \frac{kdq}{|\mathbf{r}-\mathbf{r}'|}$$

along with a given line, surface, or volume charge density ($\lambda, \sigma$, or $\rho$, respectively).

In many problems, we don't know the locations of the charges in the system. Consider the scenario shown in the following figure in which a net charge of $Q$ is placed on a conductor. 

<img src="figures/Boundary_Value_Problems.svg"/>

The charges on the conductor will distribute themselves so that the electric field in the conductor is zero. In general, we don't know what the distribution will be -- we only know that whatever it is, it is such that the electric field is zero inside.

If the top cap is centered on the origin and in the $x$--$y$ plane, to compute the potential due to the top cap outside of the conductor, we may be tempted to start with

$$V(\mathbf{r})= \int_0^{2\pi}\int_0^R \frac{k\sigma(s')}{|\mathbf{r}-s'\hat{\mathbf{s}}|}s'ds'd\phi'$$

which was the approach used to find the potential due to charges distributed on a disk with a given $\sigma(s)$. However, in this case, we don't know $\sigma(s)$ and so we are stuck. A brute-force method of computing $\sigma$ uses the fact that the $V$ must be constant on the conductor: guess $\sigma$ the top, bottom, and side surfaces, compute $V$ using integration, and then repeat until a $V$ is found that is constant on the conductor.

In summary, we can only use the integral formula for $V$ if the charge densities are known. In general, if we place a net charge on a conductor, we do not know how it will distribute on its surface.

### Type 2 Problems

Problems of type 2. are called **boundary value problems** and are generally solved by finding solutions to a partial differential equation called Poisson's equation:

$$\nabla^2 V= -\frac{\rho}{\epsilon_0}$$

$\nabla^2$ is a new form of operator. It involves operation on a scalar function $f$ and results in a scalar function. In cartesian coordinates, 

$$\displaystyle \nabla^2f=\frac{\partial^2 f}{\partial x^2}+\frac{\partial^2 f}{\partial y^2}+\frac{\partial^2 f}{\partial z^2}$$

Therefore, Poisson's equation in cartesian coordinates is

$$\frac{\partial^2 V}{\partial x^2}+\frac{\partial^2 V}{\partial y^2}+\frac{\partial^2 V}{\partial z^2}=-\frac{\rho}{\epsilon_0}$$

Similar to the divergence and gradient operators, the $\nabla^2$ operator (also called the Laplacian or "del squared") has different forms for each coordinate system. These are given on the second--to last page of Griffiths.

Laplace's equation is Poisson's equation with $\rho=0$:

$$\nabla^2 V = 0$$

In cartesian coordinates, it is

$$\frac{\partial^2 V}{\partial x^2}+\frac{\partial^2 V}{\partial y^2}+\frac{\partial^2 V}{\partial z^2}=0$$

### Deriving Poisson's Equation

Poisson's Equation, $\nabla^2 V= -{\rho}/{\epsilon_0}$, follows directly from inserting the definition of the electric potential $\mathbf{E}=-\nabla V$ into Gauss' Law in differential form $\nabla\bfcdot\mathbf{E}=\rho/\epsilon_0$.

Gauss's law in differential form is

$$\nabla\bfcdot\mathbf{E}=\frac{\rho}{\epsilon_0}$$

Using $\mathbf{E}=-\boldsymbol{\nabla}V$, this is

$$\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)=\frac{\rho}{\epsilon_0}$$

To evaluate $\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)$, first write $\boldsymbol{\nabla}V$ in cartesian

$$\boldsymbol{\nabla}V=\xhat\frac{\partial V}{\partial x}+\yhat\frac{\partial V}{\partial y}+\zhat\frac{\partial V}{\partial z}$$

Then

$$\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)=\boldsymbol{\nabla}\bfcdot\left(-\xhat\frac{\partial V}{\partial x}-\yhat\frac{\partial V}{\partial y}-\zhat\frac{\partial V}{\partial z}\right)$$

Using the definition of divergence of a vector function $\mathbf{U}$, which is

$$\boldsymbol{\nabla}\bfcdot\mathbf{U}=\xhat\frac{\partial U_x}{\partial x}+\yhat\frac{\partial U_y}{\partial y}+\zhat\frac{\partial U_z}{\partial z}$$

with $U_x=-\partial V/\partial x$, $U_y=-\partial V/\partial y$, $U_z=-\partial V/\partial z$ gives

$$\boldsymbol{\nabla}\bfcdot\left(-\xhat\frac{\partial V}{\partial x}-\yhat\frac{\partial V}{\partial y}-\zhat\frac{\partial V}{\partial z}\right)=-\frac{\partial^2 V}{\partial x^2}-\frac{\partial^2 V}{\partial y^2}-\frac{\partial^2 V}{\partial z^2}$$

and so 

$$\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)=-\frac{\partial^2 V}{\partial x^2}-\frac{\partial^2 V}{\partial y^2}-\frac{\partial^2 V}{\partial z^2}$$

and

$$-\frac{\partial^2 V}{\partial x^2}-\frac{\partial^2 V}{\partial y^2}-\frac{\partial^2 V}{\partial z^2}=\frac{\rho}{\epsilon_0}$$

Moving the negative sign and using the definition of the Laplacian $\nabla^2$, gives Poisson's equation

$$\nabla^2V=-\frac{\rho}{\epsilon_0}$$

### Problem

Outside of a solid sphere of radius $R$ with uniformly distributed charge $Q$, the field is

$\displaystyle V(r)=kQ\frac{1}{r}$

inside, it is

$\displaystyle V(r)=\frac{kQ}{2R}\left[1-\frac{r^2}{R^2}\right]$

Compute $\nabla^2 V$ and verify that $\nabla^2V=-\frac{\rho}{\epsilon_0}$ inside and outside of the sphere. You may use the formula for $\nabla^2$ in any coordinate system. 

# 1-D

See also 3.2 of Griffiths.

## Cartesian

Suppose that we connect a battery with a potential difference $V_o$ to two large conducting plates. We want to know how $V$ varies between the plates.

<img src="figures/Parallel_Plates_Example.svg"/>

This problem can be solved using two approaches.
1. By assuming the potential causes equal and opposite amount of charge to be uniformly distributed on the plates. This approach can only be used because we know (or assume) how the charges will distribute on the surfaces. If the plates were not large, we could not use this method.
2. By using the boundary value method.
 
### Charge Method


Assume charges of $\pm Q$ appear on the plates when the battery is connected so that the surface charge densities are $\pm Q/A$ and use the method demonstrated in the [capacitance notes](capacitance.html) notes to find $V$.

The electric field between the plates is $\mathbf{E}=-\sigma/\epsilon_o\xhat$. Using $V(x)=V(a)-\int_a^x\mathbf{E}\bfcdot d\mathbf{l}$ with $a=0$ and $d\mathbf{l}=dx'\xhat$

$\displaystyle V(x)=V(0)-\int_0^x -\frac{\sigma}{\epsilon_o}dx'$

Integration gives

$\displaystyle V(x) = V(0)+\frac{\sigma}{\epsilon_o}x$

We are not done because we need to write $\sigma$ in terms of $V_o$. To compute $\sigma$, plug in $x=d$ to get

$\displaystyle V(d)-V(0)=\frac{\sigma}{\epsilon_o}d$

The difference in potential $V(d)-V(0)$ was given as $V_o$. Substitution gives

$\displaystyle V_o=\frac{\sigma}{\epsilon_o}d\quad\Rightarrow\quad \sigma=\epsilon_o\frac{V_o}{d}$

Plugging this $\sigma$ into $\displaystyle V(x) = V(0)+\frac{\sigma}{\epsilon_o}x$ gives

$\displaystyle V(x)=V(0)+V_o\frac{x}{d}$

### Laplace's Equation Method

This problem may also be solved using Laplace's equation.

Between the plates, there are no charges, so $\rho=0$ and Laplace's equation applies. If the plates are large, then the potential will only vary in the $x$--direction, in which case Laplace's equation in cartesian components simplifies to:

$\displaystyle\nabla^2V = \frac{\partial^2 V}{\partial x^2} = 0$

This can be written as 

$\displaystyle\nabla^2V = \frac{d^2 V}{dx^2} = 0$

because $V$ only depends on $x$. This equation can be integrated twice to give

$\displaystyle V(x)=ax+b$

where $a$ and $b$ are constants. You can verify that $V = ax+b$ satisfies $\partial^2 V/\partial x^2 = 0$ by differentiating it twice with respect to $x$.

The interpretation of this equation is that in a configuration where it can be argued that potential only depends on $x$, the potential must increase or decrease linearly. In this example, the two boundary conditions are

1. $V(x=0)=0$
2. $V(x=d)=V_o$

These two conditions give two equations that can be solved to find the unknown constants $a$ and $b$:

$\displaystyle V(x=0)=0=a\cdot 0+b \Rightarrow b = 0$

$\displaystyle V(x=d)=V_o=ad+b=ad+0 \Rightarrow a=V_o/d$

so the solution is

$\displaystyle V(x) = \frac{V_o}{d}x$

This is the same result found using the charge method if we set $V(0)=0$ in the charge method equation to be consistent with what was used in Laplace's equation method.

After developing a solution to Laplace's equation, one should always verify that the solution matches the boundary conditions, in this case by plugging in the coordinates of the boundary:

1. $V(x) = \frac{V_o}{d}x \Rightarrow V(0)=0$ so the solution matches the $x=0$ boundary condition
2. $V(x) = \frac{V_o}{d}x \Rightarrow V(d)=V_o$ so the solution matches the $x=d$ boundary condition

1-D examples are simple. As will be seen when 2- and 3-D problems are considered, typically, one cannot find a single equation that satisfies all boundary conditions by following this method; a function can be found that satisfies some but not all of the boundary conditions. To fully solve the problem, one has to rely on the so-called "Fourier Trick" to find a solution. This method is described in the section on 2-D Cartesian.

### Problems

#### Checking Solution

A student came up with the following equation for the potential between the plates: $V(x)/V_o = e^{\tan^{-1}(x+1/2)} + x^3 - 1/\sqrt{x^2-1} + \tanh(1/\sqrt{e^x}+4\pi)$.  Without doing a calculation, we know this is wrong or the expression simplifies to $V(x)=V_ox/d$. Why?

%4. You have computed $V$ that satisfied Laplace's Equation and the boundary conditions. This solution is unique. Some students noted that the cubic term would not be zero after differentiating it twice and so the potential would not satisfy Laplace's Equation. But, this term could have been canceled by another term that appeared after taking the second derivative. The point of this problem was to make sure that you understood the uniqueness theorem, which is import for image problems.

## Cylindrical

Two long conducting cylinders of radius $a$ and $b$ are configured as shown in the following figure.

<img src="figures/Boundar_Value_Problems_Cylinder.svg"/>

Assume the potential on the inner cylinder is $V_o$ and that on the outer cylinder is $0$.

The cylinders are conductors, and if they are long relative to their radius, the charges that appear on them will be approximately uniformly distributed on their surfaces. If the charge distribution is independent of $\phi$ and $z$, the potential will not depend on $\phi$ and $z$. So $V=V(s)$.

In cylindrical coordinates, the Laplacian is 

$$\nabla^2V={1 \over s}{\partial \over \partial s}\left(s {\partial V \over \partial s}\right) + {1 \over s^2}{\partial^2 V \over \partial \phi^2} + {\partial^2 V \over \partial z^2}$$

if $V=V(s)$, the derivatives in the second and third terms are zero, and so 

$$\nabla^2 V={1 \over s}{\partial \over \partial s}\left(s {\partial V \over \partial s}\right)$$

Because $V$ depends only on $s$, we can replace the partial derivative with the total derivative to obtain the ODE

$$\nabla^2 V={1 \over s}{d \over d s}\left(s {d V \over d s}\right)=0$$

The boundary conditions are

1. $V(a)=V_o$
2. $V(b)=0$

To solve the ODE, note that because $1/s$ is not zero, the only way for the left-hand side of

$${1 \over s}{d \over d s}\left(s {d V \over d s}\right)=0$$

to be zero is if

$$s {d V \over d s}=C_1$$

where $C_1$ is a constant. Direct integration of this equation gives

$$V(s) = {C_1 \ln s} + C_2$$

The two unknowns are solved for by using the boundary conditions

$$V(b) = 0 = {C_1 \ln b} + C_2 \Rightarrow C_2=-C_1\ln b$$

$$V(a) = V_o = {C_1 \ln a} + C_2\Rightarrow V_o=C_1(\ln a-\ln b)=C_1\ln(a/b)$$

Solving for $C_1$ and $C_2$ gives

$$C_1 = {V_o \over \ln(a/b)}$$
$$C_2 = -{{V_o / \ln b} \over \ln(a/b)}$$

Subsitution of these constants into $V(s) = {C_1 \ln s} + C_2$ gives

$$V(s) = {V_o \over \ln(a/b)}\left(\ln s - \ln b \right)$$

as a check of the algebraic steps, plug in $s=a$ and $s=b$ into this equation and verify that the boundary conditions used, $V(a)=V_o$ and $V(b)=0$ are satisfied.

The electric field can be found using $\mathbf{E}=-\nabla V$. In cylindrical coordinates, when $V$ depends only on $s$, the negative of the gradient of $V$ is given by

$$-\nabla V=-{\partial V \over \partial s} \hat{\mathbf{s}}$$

Evaluation of the derivative gives

$$\mathbf{E}=-{V_o \over \ln(a/b)}{1 \over s}\hat{\mathbf{s}}$$

Using $-\ln(a/b)=\ln(b/a)$, this can also be written as

$$\mathbf{E}={V_o \over \ln(b/a)}{1 \over s}\hat{\mathbf{s}}$$

This field points from $a$ to $b$ (in $+\hat{\mathbf{s}}$ direction) as expected because the potential on the inner surface is higher than that on the outer surface.

### Problem

For the example given, find $\mathbf{E}(s)$ between the cylinders using the charge method.

## Spherical

### Problem

Two conducting and concentric spherical shells with radius $a$ and $b$ (assume $b>a$) are at potential $V_o$ and $0$, respectively.

1. Find $V(r)$ between the spheres using Laplace's equation method.
2. Find $\mathbf{E}(r)$ between the spheres using the charge method.

# 2--D Cartesian

See also 3.3.1 of Griffiths.

## General Solution

Laplace's equation in 2-D cartesian coordinates is 

$$\nabla^2V = \frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} = 0$$

For arbitrary constants $A,B,C,D,$ and $m$ the following four equations satisfy it

1. $V(x,y) = \big(A\cosh mx+B\sinh mx\big)\big(C\cos my+D\sin my\big)$
2. $V(x,y) = \big(A\cos mx+B\sin mx)(C\cosh my+D\sinh my\big)$
3. $V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos my+D\sin my\big)$
4. $V(x,y) = \big(A\cos mx+B\sin mx\big)\big(Ce^{my}+De^{-my}\big)$

(This can be shown using the method of Separation of Variables covered in Chapter 3 of Griffiths. I use $m$ on this page instead of $k$ as is done in the text because I have been using $k$ for $1/(4\pi\epsilon_0)$.) 

All four forms are equivalent in the sense that the constants in one equation can be written in terms of constants in any of the other equations. For example, if we write form 3. as $V(x,y) = \big(A'e^{m'x}+Be^{-m'x})(C'\cos m'y+D'\sin m'y\big)$, then one can show that $A=(A'+B')/2$, $B=(A'-B')/2$, $C=C'$, $D=D'$, and $m=m'$.


The reason that all four forms are listed is that for certain problems, a certain choice of the form to start with leads to less algebra. 

The general solution steps are

1. Start with one of the forms 1.--4. and use the boundary conditions to find an equation that satisfies some of the four boundary conditions. There is no general rule about which form to start with beyond considering a few boundary conditions and looking at which equation will give coefficients that are zero immediately.
2. Use superposition and Fourier's trick to find an equation that satisfies all four boundary conditions.

## Solution Step 1.

Start with one of the forms 1.--4. and use the boundary conditions to find an equation that satisfies some of the boundary conditions. 
 
%In examples 3.3 and 3.4 of Griffiths, which are 2-D cartesian problems, he comes up with an equation for $V(x,y)$ that satisfies three of the four boundary conditions and has one unknown constant:

%Example 3.3: 

%$$V(x,y) = Ce^{-n\pi x/a}\sin(n\pi y/a)\mbox{ with } n=1,2,...$$

%Example 3.4:

%$$V(x,y) = C\cosh(n\pi x/a)\sin(n\pi y/a)\mbox{ with } n=1,2,...$$

%The capital letter used for the leading constant can be $A,B,C,$ or $D$ or a combination of them (the product of constants is a constant); in the derivation of the above two equations, Griffiths notes that the $C$ in the final equations is not the same as the $C$ in the original equations (one of forms 1.--4.). Technically it would be better to use something like $C'$ in the final equation to emphasize this point, but to keep the notation simple, he redefines $C$.

In Examples 3.3 and 3.4, Griffiths happens to choose

1. The best form 1.--4. to start with
2. The best order of boundary conditions to address

The problem students have with solving other problems is when they don't happen to choose the "best" way to get to the answer. In the following, I go through examples 3.3 and 3.4 by addressing the boundary conditions in a different order than Griffiths did. In doing so, I highlight some of the actual complications one will encounter if the "best" order of addressing the boundary conditions is not selected.

Prior to reading the following two examples, read Griffiths' solutions to Example 3.3 and 3.4.

### Example 3.3

The boundary conditions are

1. $V = 0$ when $y = 0$
2. $V = 0$ when $y = a$
3. $V = V_o(y)$ when $x = 0$ -- (Griffiths starts with $V_o(y)$ and then gives the solution for $V=V_o=const$)
4. $V\rightarrow 0$ as $x\rightarrow\infty$

Griffiths starts with form 3.

$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos my+D\sin my\big)$

and boundary condition 4. Here I am going to start with form 3. but boundary condition 1.

**BC 1.**: $V = 0$ when $y = 0$

Plugging $V = 0$ and $y = 0$ into

$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos my+D\sin my\big)$

gives

$0 = \big(Ae^{mx}+Be^{-mx})(C\cos m0+D\sin m0\big)$

or

$0 = \big(Ae^{mx}+Be^{-mx}\big)C$

There are two ways for this equation to be true for any $x \ge 0$

1. Both $A$ and $B$ are zero. We reject this option because then form 3. reduces to $V(x,y)=0$, which satisfies Laplace's equation, but can't satisfy all of the boundary conditions.
2. $C=0$.

If $C=0$, we are left with

$V(x,y) = \big(Ae^{mx}+Be^{-mx}\big)D\sin my$

or, defining $A'=AD$ and $B'=BD$,

$V(x,y) = \big(A'e^{mx}+B'e^{-mx}\big)\sin my$

**BC 2.**: $V = 0$ when $y = a$

Plugging these values into the equation we left off with after addressing boundary condition 1. gives

$0 = \big(A'e^{mx}+B'e^{-mx}\big)\sin ma$

There are two ways for this equation to be true for any $x \ge 0$:

1. Both $A'$ and $B'$ are zero. We reject this option because then we are left with $V(x,y)=0$, which satisfies Laplace's equation, but can't satisfy all of the boundary conditions.
2. $\sin ma=0$.

The only way for $\sin ma=0$ to be true generally is if $ma=0,\pm \pi,\pm 2\pi,...$. 

From this we conclude

$m=\frac{n\pi}{a}$ with $n$ constrained to be $0, \pm 1, \pm 2, ...$

This leaves

$V(x,y) = \big(A'e^{n\pi x/a}+B'e^{-n\pi x/a}\big)\sin n\pi y/a$

Inspection of this equation allows us to reject the possibility that $n=0$; if $n=0$, this equation reduces to $V(x,y)=0$, which cannot satisfy all of the boundary conditions.

**BC 3.**: $V = V_o$ when $x = 0$

Plugging these values into the equation we left off with after addressing boundary condition 2. gives

$V_o = \big(A'e^{n\pi 0/a}+B'e^{-n\pi 0/a}\big)\sin n\pi y/a$

or, because $e^0=1$,

$V_o = \big(A'+B'\big)\sin n\pi y/a$


This equation is true but is not immediately useful for simplifying our equation for $V(x,y)$. So we move on to the next boundary condition.

**BC 4.**: $V = 0$ when $x \rightarrow \infty$

Plugging these values into the equation we left off with after addressing boundary condition 2. gives

$0 = \big(A'e^{n\pi \infty/a}+B'e^{-n\pi \infty/a}\big)\sin n\pi y/a$

or, because $e^{-\infty}=0$,

$0 = \big(A'e^{n\pi \infty/a}\big)\sin n\pi y/a$

There is only one way for this equation to be true: $A'=0$. (There is technically a mathematical issue that I am ignoring because zero times infinity is indeterminate; there is a way around this issue, but for now, it is not important and I'll use this dubious notation.)

This leaves

$V(x,y) = B'e^{-n\pi x/a}\sin n\pi y/a$

which the same as equations 3.28 and 3.29 with one exception. In the above I concluded $n$ could be $\pm 1, \pm 2, ...$ where Griffiths concludes $n=1, 2, 3, ...$. The equivalence of these two conclusions will be shown when $B'$ is computed.

The final step is determining $B'$. This would seem to be impossible because boundary condition 3., $V = V_o$ when $x = 0$, gives

$V_o = B'e^{-n\pi 0/a}\sin n\pi y/a=B'\sin(n\pi y/a)$

and this equation needs to hold true for any $0\le y \le a$. Another way to show that finding a $B'$ that satisfies boundary condition 3. is impossible, suppose $y=a/2$ and $n=1$, then we have

$V_o = B'e^{-n\pi 0/a}\sin n\pi y/a=B'\sin(\pi/2)$

Giving $B'=V_o$. Now suppose $y=a/4$ and $n=1$, then

$V_o = B'e^{-n\pi 0/a}\sin n\pi y/a=B'\sin(\pi/4)$

Giving $B'=\sqrt{2}V_o$. One can repeat this for all allowed values and $n$ and you will come to the conclusion that there is no single value of $B'$ that can satisfy this equation for any $0\le y \le a$.

To satisfy this last boundary condition, superposition and "Fourier's Trick" is needed, which is covered in [step 2](#solution-step-2).

### Example 3.4

The boundary conditions are

1. $V = 0$ when $y = 0$
2. $V = 0$ when $y = a$
3. $V = V_o$ when $x = b$
4. $V = V_o$ when $x = -b$

Griffiths starts with form 3.

$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos my+D\sin my\big)$

and a symmetry argument to conclude $A=B$. Here I am going to start with form 3. but boundary condition 1. In addition, I won't make use of the symmetry argument.

**BC 1.**: $V = 0$ when $y = 0$

**BC 2.**: $V = 0$ when $y = a$

The starting form 3. and boundary conditions 1. and 2. are identical to that from example 3.3, so we can re-use the result concluded from addressing them:

$V(x,y) = \big(A'e^{n\pi x/a}+B'e^{-n\pi x/a}\big)\sin n\pi y/a$

with $n$ constrained to be $0, \pm 1, \pm 2, ...$.

**BC 3.**: $V = V_o$ when $x = b$

Plugging the boundary values into the equation we left off with after addressing boundary condition 2. gives

$V_o = \big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)\sin n\pi y/a$

Now we seem stuck. How does one constrain $A'$ and $B'$ for this equation to hold? We have one other boundary condition to address, so perhaps it will provide some insight.

**BC 4.**: $V = V_o$ when $x = -b$

$V_o = \big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin n\pi y/a$

Here we would seem to be stuck again. However, notice that the equation here can be combined with that from BC 3:

$\big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)\sin n\pi y/a=\big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin n\pi y/a$

The $\sin n\pi y/a$ term appears on both sides and can be dropped, leaving

$\big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)=\big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)$

which simplifies to

$A'\big(e^{n\pi b/a}-e^{-n\pi b/a}\big)=B'\big(e^{n\pi b/a}-e^{-n\pi b/a}\big)$

The terms in parentheses are identical, so we conclude

$A'=B'$

Therefore, the equation we ended with when addressing BC 2.,

$V(x,y) = \big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin n\pi y/a$

simplifies to

$V(x,y) = A'\big(e^{-n\pi x/a}+e^{n\pi x/a}\big)\sin n\pi y/a$

This can be futher simplified using the definition $\cosh z=(e^z+e^{-z})/2$

$V(x,y) = 2A'\cosh(n\pi x/a)\sin(n\pi y/a)$

This equation is equivalent to Griffiths' 3.41 if $2A'$ is replaced with a constant labeled $C$. As with example 3.3, we ended up with one constant that is still unknown. 

Note that $n=0$ would give $V(x,y)=0$, which does not satisfy all of the boundary conditions. As a result, the allowed values of $n$ are $\pm 1, \pm 2, ...$. 

As was the case in my solution to example 3.3, above I concluded $n$ could be $\pm 1, \pm 2, ...$ where Griffiths concludes $n=1, 2, 3, ...$. The equivalence of these two conclusions will be shown when $A'$ is computed in [step 2.](#solution-step-2).

## Step 2 preparation

### Integrals

1. Show that $\int_0^\pi \sin 2x \sin x dx$ = 0. Note that without any calculation, this is expected from a plot of $\sin x$ and $\sin 2x$ and thinking about the area under the curve for their product.

2. Show that $\int_0^\pi \sin nx \sin lx dx$ = 0 if $l\ne n$ by explicitly evaluating the integral.

3. Compute $\int_0^\pi \sin^2 nx dx$ for (a) any $n\ne 0$ and (b) for integer $n$.


**Comment**:

The motivation for giving you these problems is to help you remember that

$\int_0^\pi \sin nx \sin lx dx = 0$ if $l\ne n$ which is important for Fourier sum problems.

A way to reason this out without doing a calculation is by considering a plot of the integrand $\sin nx\sin lx$ over the interval $0\le x\le \pi$ by plotting two $\sin$ curves for $l\ne m$ and thinking about what the product of the curves looks like; over half interval the product will be positive and over the other half of the interval it will be negative, so the integral will be zero.

When $l=m$, the integrand is $\sin^2 mx$, which is always positive, so its integral is not zero over any interval of $x$.

%**Answer**

%3\. For $n \gt 0$, $\frac{\pi}{2}-\frac{\sin(2\pi n)}{4n}$

### Series sums

Show that

$V(x,y) = C_1e^{-\pi x/a}\sin\pi y/a + C_2e^{-2\pi x/a}\sin 2\pi y/a + C_3e^{-3\pi x/a}\sin 3\pi y/a + ... $

satisfies Laplace's equation.

% and the boundary conditions of Example 3.3.

**Answer**

From a previous problem, we know that equations of this form of each term satisfy Laplace's equation. Here will show this again. Define these terms as

$V_n=C_ne^{-n\pi x/a}\sin n\pi y/a$

Then for any $n$,

\begin{aligned}
\nabla^2 V_n = & \\
= & \text{ } \nabla^2\big(C_ne^{-n\pi x/a}\sin [n\pi y/a]\big) \\
= & \text{ } C_n\sin [n\pi y/a]\frac{\partial^2 e^{-n\pi x/a}}{\partial x^2} + C_ne^{-n\pi x/a}\frac{\partial^2 \sin [n\pi y/a]}{\partial y^2} \\
= & \text{ } C_n \sin [n\pi y/a] (-n\pi x/a)(-n\pi x/a)e^{-n\pi x/a} + C_n e^{-n\pi x/a}(n\pi x/a)(-n\pi x/a)\sin [n\pi y/a] \\
= & \text{ } 0
\end{aligned}

The Laplacian of a sum can be written as the sum of Laplacians

$\displaystyle\nabla^2 (V_1+V_2+...) = \nabla^2 V_1 + \nabla^2 V_2 + ...$

Because $\nabla^2 V_n=0$, we conclude

$\displaystyle\nabla^2 (V_1+V_2+...) = 0 + 0 + ... = 0$

## Solution Step 2.

In this step, we start with an equation that satisfies two or three of the boundary conditions, but cannot satisfy the remaining one(s). Then,

1. Re--write one of the remaining boundary conditions as a sum of equations that satisfy the other boundary conditions and
2. Apply Fourier' trick: Multiply the equation from 1. by a $\sin$ or $\cos$ function and integrate.

### Example 3.3

The equation

$V(x,y) = Ce^{-n\pi x/a}\sin n\pi y/a$ with $n=0, \pm 1, ...$

satisfied three of the four boundary conditions in Example 3.3 but there is no $C$ or $n$ that can satisfy the last boundary condition $V(0,y)=V_o$:

$V_o = Ce^{-n\pi 0/a}\sin n\pi y/a=C\sin n\pi y/a$

As a result, we try a sum of terms with $n=1, 2, ...$

$V_o = C_1\sin \pi y/a + C_2\sin 2\pi y/a + C_3\sin 3\pi y/a + ... $

Multiplying this by $dy\sin l\pi y/a$ and integrating from $y=0$ to $y=a$ gives

**Equation A**:

$\displaystyle \int_0^a V_ody \sin (l\pi y/a) =$

$\displaystyle \phantom{\int_0^a V_ody \sin (l\pi y/a)
=}\phantom{+}C_1\int_0^a dy \sin (l\pi y/a) \sin (\pi y/a)$

$\displaystyle \phantom{\int_0^a V_ody \sin (l\pi y/a) =}+C_2\int_0^a dy\sin( l\pi y/a) \sin (2\pi y/a)$

$\displaystyle \phantom{\int_0^a V_ody \sin (l\pi y/a) =}+C_3\int_0^a dy \sin (l\pi y/a) \sin (3\pi y/a)$

$\displaystyle\phantom{\int_0^a V_ody \sin (l\pi y/a) =}+ ...$

To show that $C_1, C_2,$ and $C_3$ are

* $\displaystyle C_1=\frac{4V_o}{1\pi}$;

* $\displaystyle C_2=0$; and

* $\displaystyle C_3=\frac{4V_o}{3\pi}$,

set $l=1$ in Equation A and evaluate all of the integrals. This will give you $C_1$. Next, set $l=2$ in Equation A and evaluate all of the integrals.  This will give you $C_2$. Finally, set $l=3$ in Equation A and evaluate all of the integrals to get $C_3$.

%Do you see why the limits of integration were chosen to be $[0,a]$? If not, try finding $C_1,C_2,C_3$ using integration limits of $[0,a/3]$.

