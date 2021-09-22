# Boundary Value Problems

Many laws of physics are expressed as either ordinary differential equations or partial differential equations.

Recall from mechanics that the equation for the position of a particle in a uniform gravitational field is given by the ordinary differential equation

$$m\frac{d^2x}{dt^2}=-mg$$

A general solution for $x(t)$ that satisfies this equation has the form

$$x(t)=C_1+C_2t-gt^2/2$$

where $C_1$ and $C_2$ are two constants.

To use this equation to find $x(t)$ for a mass, the values of the two constants must be known. Usually these two constants are given based on the initial values of $x$ and $dx/dt$. For example, if $x(t=0)=0$ and $v(t=0)=0$, then $C_1=C_2=0$ and the trajectory of the mass is given by $x(t)=-gt^2/2$.

This type of problem is called an **initial value problem** -- given a differential equation for the position of the mass and it's initial values of $x$ and $v$, we arrive at a solution for $x$ for all $t$. Another example of an inital value problem is for the position $x$ of a mass on a spring. The differential equation for $x$ is $d^2x/dt^2-\omega_o^2x=0$. A general solution is $x(t)=C_1\sin(\omega_o t)+C_2\cos(\omega_o t)$.

A **boundary value problem** involves first finding a general solution to a partial differential equation with respect to the position (instead of time). The solution will have constants whose values are determined by the conditions at the boundary. For example, in electrostatics

$$\frac{\partial^2 V}{\partial x^2}=0$$

is a partial differential equation for $V$ for a system where the symmetry is such that the potential only depends on $x$. If we want to know $V(x)$, we need to know a general solution to this equation. It is

$$V(x)=C_1 + C_2x$$

The values for $C_1$ and $C_2$ are determined based on boundary conditions. For example, $V(x=0)=0$ and $V(x=L)=V_o$.

In this course, you will only be required to know how to derive the general solution for partial differential equations in 1--D. Derivations are given in the [1--D section](#1-d).

For 2-- and 2--D partial differential equations, you will be given the general solution and asked to find the unknown constants given boundary value information.

# Finding $V$

There are generally two types of problems involving $V$ in electrostatics:
1. given the locations of charges, compute the electric potential and electric field at all locations in space; and
2. given the electric potential at certain locations in space, compute the electric potential and electric field at all locations in space.

## Type 1

For problems of type 1., we can compute $V$ using

$$V(\mathbf{r})=\sum_{i=1}^{N} \frac{kq\_{i}}{|\mathbf{r}-\mathbf{r}\_{i}'|}$$

for $N$ discrete charges, or the continuous approximation 

$$V(\mathbf{r})=\int \frac{kdq}{|\mathbf{r}-\mathbf{r}'|}$$

along with a given line, surface, or volume charge density ($\lambda(x'), \sigma(x',y')$, or $\rho(r')$, respectively).

In many problems, we don't know the locations of the charges in the system. Consider the scenario shown in Figure X in which a net charge of $Q$ is placed on a conductor. The charges on the conductor will distribute themselves so that the electric field in the conductor is zero. In general, we don't know what the distribution will be -- we only know that whatever it is, it is such that the electric field is zero inside.

To compute the potential, we may be tempted to start with

$$V(\mathbf{r})= \int_0^{2\pi}\int_0^R \frac{k\sigma(s')}{|\mathbf{r}-s'\hat{\mathbf{s}}|}s'ds'd\phi'$$

which was the approach used to find the potential due to charges distributed on a disk with a given $\sigma(s)$. However, in this case, we don't know $\sigma(s)$ and so we are stuck. A brute-force method of computing $\sigma(s)$ uses the fact that the $V$ must be constant on the conductor -- one could guess $\sigma(s)$ until these conditions are satisfied.

In summary, we can only use the integral formula for $V$ if the charge densities are known. In general, if we place a net charge on a conductor, we do not know how it will distribute on its surface.

## Type 2


Problems of type 2. are called **boundary value problems** and are generally solved by finding solutions to a partial differential equation called Poisson's equation:

$$\nabla^2 V= -\frac{\rho}{\epsilon_0}$$

$\nabla^2$ is a new form of operator. It involves operation on a scalar function $f$ and results in a scalar function. In cartesian coordinates, 

$$\displaystyle \nabla^2f=\frac{\partial^2 f}{\partial x^2}+\frac{\partial^2 f}{\partial y^2}+\frac{\partial^2 f}{\partial z^2}$$

Threfore, Poisson's equation in cartesian coordinates is

$$\frac{\partial^2 V}{\partial x^2}+\frac{\partial^2 V}{\partial y^2}+\frac{\partial^2 V}{\partial z^2}=-\frac{\rho}{\epsilon_0}$$

Similar to the divergence and gradient operators, the $\nabla^2$ operator (also called the Laplacian) has different forms for each coordinate system. 

Laplace's equation is Poisson's equation with $\rho=0$:

$$\nabla^2 V = 0$$

In cartesian coordinates, it is

$$\frac{\partial^2 V}{\partial x^2}+\frac{\partial^2 V}{\partial y^2}+\frac{\partial^2 V}{\partial z^2}=0$$

## Deriving Poisson's Equation

Poisson's Equation, $\nabla^2 V= -{\rho}/{\epsilon_0}$, follows directly from inserting the definition of the electric potential $\mathbf{E}=-\nabla V$ into Gauss' Law in differential form $\nabla\bfcdot\mathbf{E}=\rho/\epsilon_0$.

Gauss's law in differential form is

$$\nabla\bfcdot\mathbf{E}=\frac{\rho}{\epsilon_0}$$

Using $\mathbf{E}=-\boldsymbol{\nabla}V$, this is

$$\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)=\frac{\rho}{\epsilon_0}$$

To evaluate $\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)$, first write $\boldsymbol{\nabla}V$ in cartesian

$$\boldsymbol{\nabla}V=\xhat\frac{\partial V}{\partial x}+\yhat\frac{\partial V}{\partial y}+\zhat\frac{\partial V}{\partial z}$$

Then

$$\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)=\boldsymbol{\nabla}\bfcdot\left(-\xhat\frac{\partial V}{\partial x}-\yhat\frac{\partial V}{\partial y}-\zhat\frac{\partial V}{\partial z}\right)$$

Using

$$\boldsymbol{\nabla}\bfcdot\mathbf{U}=\xhat\frac{\partial U_x}{\partial x}+\yhat\frac{\partial U_y}{\partial y}+\zhat\frac{\partial U_z}{\partial z}$$

with $U_x=-\partial V/\partial x$, $U_y=-\partial V/\partial y$, $U_z=-\partial V/\partial z$ gives

$$\boldsymbol{\nabla}\bfcdot\left(-\xhat\frac{\partial V}{\partial x}-\yhat\frac{\partial V}{\partial y}-\zhat\frac{\partial V}{\partial z}\right)=-\frac{\partial^2 V}{\partial x^2}-\frac{\partial^2 V}{\partial y^2}-\frac{\partial^2 V}{\partial z^2}$$

and so 

$$\boldsymbol{\nabla}\bfcdot(-\boldsymbol{\nabla}V)=-\frac{\partial^2 V}{\partial x^2}-\frac{\partial^2 V}{\partial y^2}-\frac{\partial^2 V}{\partial z^2}$$

and

$$-\frac{\partial^2 V}{\partial x^2}-\frac{\partial^2 V}{\partial y^2}-\frac{\partial^2 V}{\partial z^2}=\frac{\rho}{\epsilon_0}$$

Moving the negative sign and using the definition of the Laplacian $\nabla^2$, gives Poisson's equation

$$\nabla^2V=-\frac{\rho}{\epsilon_0}$$

## Problem

In the empty space between two infinite sheets of charge, the potenial is ...

# 1-D

## Cartesian

Suppose that we connect a battery with potential difference $V_o$ to two large conducting plates. We want to know how $V$ varies between the plates.

This problem can be solved using two approaches.
1. By assuming the potential causes equal and opposite amount of charge to be uniformly distribute on the plates. This approach can only be used becasue we know (or assume) how the charges will distribute on the surfaces. If the plates were not large, we could not use this method.
2. By using the boundary value method.
 
### Charge Method


Assume charges of $\pm Q$ appear on the plates when the battery is connected so that the surface charge densities are $\pm Q/A$ and use the method demonstrated in the [capacitance notes](capacitance.html) notes to find $V$.

The electric field between the plates is $\mathbf{E}=-\sigma/\epsilon_o\xhat$. Using $V(x)=V(a)-\int_a^x\mathbf{E}\bfcdot d\mathbf{l}$ with $a=0$ and $d\mathbf{l}=dx'\xhat$

$\displaystyle V(x)=V(0)-\int_0^x -\frac{\sigma}{\epsilon_o}dx'$

Integration gives

$\displaystyle V(x) = V(0)+\frac{\sigma}{\epsilon_o}x$

We are not done because we we need to write $\sigma$ in terms of $V_o$. To compute $\sigma$, plug in $x=d$ to get

$\displaystyle V(d)-V(0)=\frac{\sigma}{\epsilon_o}d$

The difference in potential $V(d)-V(0)$ was given as $V_o$. Substitution gives

$\displaystyle V_o=\frac{\sigma}{\epsilon_o}d\quad\Rightarrow\quad \sigma=\epsilon_o\frac{V_o}{d}$

Plugging this $\sigma$ into $\displaystyle V(x) = V(0)+\frac{\sigma}{\epsilon_o}x$ gives

$\displaystyle V(x)=V(0)+V_o\frac{x}{d}$

### Laplace's Equation Method

This problem may also be solved using Laplace's eqaation.

Between the plates, there are no charges, so $\rho=0$ and laplace's equation applies. If the plates are large, then the potential will only vary in the $x$--direction, in which case Laplace's equation in cartesian components simplifies to:

$$\nabla^2V = \frac{\partial^2 V}{\partial x^2} = 0$$

This can be written as 

$$\nabla^2V = \frac{d^2 V}{dx^2} = 0$$

because $V$ only depends on $x$. This equation can be integrated twice to give

$$V(x)=ax+b$$

where $a$ and $b$ are constants. The interpretation of this equation is that in a configuration where it can be argued that potential only depends on $x$, the potential must increase or decrease linearly. A configuration that is approximately 1-dimensional is two large conducting plates separated by a distance $d$ and connected to a batter with potential $V_o$. In this example, the two boundary conditions are

1. $V(x=0)=0$
2. $V(x=d)=V_o$

which give two equations that can be solved to find the unknown constants $a$ and $b$:

$$V(x=0)=0=a\cdot 0+b \Rightarrow b = 0$$

$$V(x=d)=V_o=ad+b=ad+0 \Rightarrow a=V_o/d$$

so the solution is

$$V(x) = \frac{V_o}{d}x$$

After developing a solution to Laplace's equation, one should always verify that the solution matches the boundary conditions, in this case by plugging in the coordinates of the boundary:

1. $V(x) = \frac{V_o}{d}x \Rightarrow V(0)=0$ so the solution matches the $x=0$ boundary condition
2. $V(x) = \frac{V_o}{d}x \Rightarrow V(d)=V_o$ so the solution matches the $x=d$ boundary condition

1-D examples are deceptively simple. As will be seen when 2- and 3-D problems are considered, typically one cannot find a single equation that satisfies all boundary conditions by following this method; a function can be found that satisfies some but not all of the boundary conditions. To fully solve the problem, one has to rely on the so-called "Fourier Trick" to find a solution. This method is described in the section on 2-D Cartesian.

### Problems

#### 

In one dimension, Laplace's Equation is $\partial^2 V/\partial x^2 = 0$.  As described in the textbook, a general equation that satisfies this is

$V = ax+b$

where $a$ and $b$ are constants that are determined by boundary conditions.  You can verify that $V = ax+b$ satisfies $\partial^2 V/\partial x^2 = 0$ by differentiating it twice with respect to $x$.

Suppose that we have two infinite plates oriented so that their normals are parallel to the x-axis and then we connect the plates with a wire to a static voltage source (battery).  This configuration is 1-dimensional since there can only be variations in potential in the x-direction.  To find the potential between the plates, we need to do to things: Find an equation that satisfies (1) Laplace's equation and (2) the boundary conditions.  Part (1) has been done already.

1. Suppose the boundary conditions are that at $x=0$, $V=0$ and at $x=d$, $V=V_o$.  (The left plate is at $x=0$ and the right plate is at $x=d$). Find $a$ and $b$ such that $V$ satisfies these boundary conditions. Once you have $V$ such that when you plug in $x=0$ and $x=d$, you have solved your first "boundary value problem"! 
2. Suppose the boundary conditions are that at $x=-d$, $V=-V_o$ and at $x=d$, $V=+V_o$. (The left plate is at $x=-d$ and the right plate is at $x=d$). Find $a$ and $b$ such that $V$ satisfies these boundary conditions.
3. Find the electric field between the plates for both configurations.
4. In order to create an electric field, charges are needed.  These charges appear on the plates.  What is the charge density on each plate?
5 You have calculated the electric field between the plates.  What is the electric field in the other regions? (Hint: Think of how you would answer this given infinite sheets of charge having the charge density that you just computed. You can also use a Gaussian pillbox on the right plate that goes from just to the left to just to the right of the right plate; you know the field on the left cap and need to compute the field on the right cap.)

####

Two infinite conducting plates are oriented so that their normals are parallel to the $x$-axis and connected to a battery with a potential of $V_o$.  The left plate is in the $x=0$ plane and has $V=0$; the right plate is in the $x=d$ plane and has $V=V_o$.

1. Find the electric potential at locations $x<0$, $0\le x\le d$, and $x>d$.
2. Find the electric field magnitude and direction (the x-axis is positive to the right) at locations  $x<0$, $0\le x\le d$, and $x>d$.
3. Find the surface charge density on each plate in terms of $V_o$ and $d$.
4. A student came up with the following equation for the potential between the plates: $V(x)/V_o = e^{\tan^{-1}(x+1/2)} + x^3 - 1/\sqrt{x^2-1} + \tanh(1/\sqrt{e^x}+4\pi)$.  Without doing a calculation, we know this is wrong or the expression simplifies to $V(x)=V_ox/d$. Why?

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
1. This configuration is like a capacitor for which the electric field outside is zero and so the potential does not change as you move away from the plates in the outer regions, so the potential for $x<0$ is 0 and for $x>d$ is $V_o$. Another way to see this is to note that the plates will have an equal and opposite amount of charge. In the outer regions, the sum of the electric field due from the plates is zero because they both cancel (draw this out to confirm!) and the electric field for an infinite sheet of charge does not depend on the distance from the sheet. In 1-D, the most general equation that satisfies Laplace's Equation is $V(x) = ax+b$. The left boundary condition gives $V(0)=0=a0+b\Rightarrow b=0$.The right boundary condition gives $V(0)=V_o=ad\Rightarrow a=V_o/d$. So between the plates, $V(x)=V_ox/d$.
   1. $x<0, V(x) = 0$
   2. $0\le x\le d, V(x)=V_o/d$
   3. $x>d, V(x)=V_o$
2. We expect the electric field to point to the left based on the fact that the plate on the right has a higher potential than the one on the left. $\mathbf{E}=-\nabla V = \hat{\mathbf{x}}\partial V/\partial x$ gives $-\hat{\mathbf{x}}V_o/d$.
   1. $x<0, \mathbf{E} = 0$
   2. $0\le x\le d, \mathbf{E} =  -\hat{\mathbf{x}}V_o/d$
   3. $x>d, \mathbf{E}=0$
3. The formula for finding the surface charge on a conductor is $\sigma = -\epsilon_0 \nabla V \cdot \hat{\mathbf{n}}$, where $\hat{\mathbf{n}}$ is the unit normal vector to the surface at the location where $\sigma$ is to be computed (Equation 2.37 of Griffiths). To the right of the left plate, $V(x)=V_ox/d$ and $\hat{\mathbf{n}}=\hat{\mathbf{x}}$ so that  $\sigma_{Left} = -\epsilon_0 \nabla V \cdot \hat{\mathbf{n}}$ =  $\sigma = -(\epsilon_0 V_o/d)\hat{\mathbf{x}} \cdot \hat{\mathbf{n}} = -\epsilon_0 V_o/d$. To the left of the right plate, $\hat{\mathbf{n}}=-\hat{\mathbf{x}}$, giving $\sigma_{Right} = \epsilon_0 V_o/d$. Use of this formula is a bit of overkill when the normal direction to the surface is along a coordinate axis - it is often easier to just note that the magnitude of $\sigma$ will be $\epsilon_0 |\mathbf{E}|$, where $\mathbf{E}$ is the electric field due to all charges in the system, not just the charges on the conductor, and figure out the sign on $\sigma$ by thinking about the problem. Also note that in this problem we only needed to compute $\sigma_{Left}$. Give the set-up, all charges removed from one plate had to appear on the other plate. A battery does work in moving charges from one plate to another and does not internally store any of the charges removed from a plate.
   1. $\sigma_{Left} = -\epsilon_0 V_o/d$
   2. $\sigma_{Right} = \epsilon_0 V_o/d$
4. You have computed $V$ that satisfied Laplace's Equation and the boundary conditions. This solution is unique. Some students noted that the cubic term would not be zero after differentiating it twice and so the potential would not satisfy Laplace's Equation. But, this term could have been canceled by another term that appeared after taking the second derivative. The point of this problem was to make sure that you understood the uniqueness theorem, which is import for image problems.
|}

####

Three infinite conducting plates are oriented so that their normals are parallel to the $x$-axis. Plate 0 is is in the $x=0$ plane and is at potential $V_0=0$, Plate 1 is in the  $x=d$ plane and is at potential $V_1=V_b$, and Plate 2 is in the $x=2d$ plane and is at potential $V_2=2V_b$.

1. Plot the electric potential from $x=-d$ to $x=3d$. Add appropriate axis labels that depend on  $V_b$, $d$, and $\epsilon_0$.
2. Plot the electric field from $x=-d$ to $x=3d$. Add appropriate axis labels.
3. Find the surface charge density on the both sides of each plate in terms of $V_b$ and $d$:
   1. $\sigma_{0Left}$
   2. $\sigma_{0Right}$ 
   3. $\sigma_{1Left}$
   4. $\sigma_{1Right}$ 
   5. $\sigma_{2Left}$
   6. $\sigma_{2Right}$

## Cylindrical

Assume the potential on the inner cylinder is $V_o$ and that on the outer cylinder is $0$. Note that this choice is arbitrary. The inner an outer spheres can be at arbitrary potentials $V_i$ and $V_o$ and the same answer will result.

The cylinders are conductors, so the charges that appear on them will distribute uniformly on the surfaces and the distribution will be independent of $\phi$ and $z$. As a result, the potential will not depend on $\phi$ and $z$. So $V=V(\rho)$.

In cylindrical coordinates, the Laplacian is 

$$\nabla^2V={1 \over \rho}{\partial \over \partial \rho}\left(\rho {\partial V \over \partial \rho}\right) + {1 \over \rho^2}{\partial^2 V \over \partial \phi^2}
+ {\partial^2 V \over \partial z^2}$$

and the derivatives in the second and third terms are zero because $V$ does not depend on $\phi$ and $z$. 

$$\nabla^2 V={1 \over \rho}{\partial \over \partial \rho}\left(\rho {\partial V \over \partial \rho}\right)$$

Becuase $V$ depends only on $\rho$, we can replace the partial derivative with the total derivative

$$\nabla^2 V={1 \over \rho}{d \over d \rho}\left(\rho {d V \over d \rho}\right)$$

subject to the boundary conditions

$$V(a)=V_o$$

$$V(b)=0$$

To solve the ODE, note that $1/\rho$ is not zero, so the only way for left-hand-side to be zero is if

$$\rho {d V \over d \rho}=C_1$$

where $C_1$ is a constant.

Direct integration of this equation gives

$$V(\rho) = {C_1 \ln\rho} + C_2$$

The two unknowns are solved for by using the boundary conditions

$$V(b) = 0 = {C_1 \ln b} + C_2 \Rightarrow C_2=-C_1\ln b$$

$$V(a) = V_o = {C_1 \ln a} + C_2\Rightarrow V_o=C_1(\ln a-\ln b)=C_1\ln(a/b)$$

Solving for $C_1$ and $C_2$ gives

$$C_1 = {V_o \over \ln(a/b)}$$
$$C_2 = -{{V_o / \ln b} \over \ln(a/b)}$$

Subsitution of these constants into $V(\rho) = {C_1 \ln\rho} + C_2$ gives

$$V(\rho) = {V_o \over \ln(a/b)}\left(\ln\rho - \ln b \right)$$

as a check of the algebraic steps, plug in $r=a$ and $r=b$ into this equation and verify that the boundary conditions used, $V(a)=V_o$ and $V(b)=0$ are satisfied.

Next, find the electric field using $\mathbf{E}=-\nabla V$. In cylindrical coordinates when $V$ depends only on $\rho$,

$$-\nabla V=-{\partial V \over \partial \rho} \hat{\mathbf{\rho}}$$

giving

$$\mathbf{E}=-{V_o \over \ln(a/b)}{1 \over \rho}\hat{\mathbf{\rho}}$$

and using $-\ln(a/b)=\ln(b/a)$

$$\mathbf{E}={V_o \over \ln(b/a)}{1 \over \rho}\hat{\mathbf{\rho}}$$

This field points from $a$ to $b$ (in $+\hat{\mathbf{\rho}}$ direction) as expected given the potential on the inner surface is higher than that on the outer surface.

### Problems

#### 

Two infinitely long conducting hollow cylinders of radius $a$ and $b$ ($a< b$) are oriented along the $z$-axis. The inner cylinder is held at a potential $V_a$ and the outer at $V_b$ by connecting them to a battery. 

1. Use the boundary value method to find the potential between the cylinders
2. Plot the potential as a function of distance from the $z$-axis
3. Compute the surface charge density on each cylinder
4. Use the computed surface charge densities and Gauss' Law to compute the electric field between the cylinders

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Notes
|-
|

1\.

This part is primarily an exercise in repeating the steps in the example, but using different variables. (One could answer this problem quickly by taking the potential from the example and modifying it so that the boundary conditions are satisfied, but that is not the point of the question.)

$$V(\rho) = {(V_a-V_b) \over \ln(a/b)}\left(\ln\rho - \ln b \right)+V_b$$

As a check of the algebraic steps, plug in $r=a$ and $r=b$ into this equation and verify that the boundary conditions used, $V(a)=V_o$ and $V(b)=0$ are satisfied.

Next, find the electric field using $\mathbf{E}=-\nabla V$. In cylindrical coordinates when $V$ depends only on $\rho$,

$$-\nabla V=-{\partial V \over \partial \rho} \hat{\boldsymbol{\rho}}$$

giving

$$\mathbf{E}=-{(V_a-V_b) \over \ln(a/b)}{1 \over \rho}\hat{\boldsymbol{\rho}}$$

and using $-\ln(a/b)=\ln(b/a)$

$$\mathbf{E}={(V_a-V_b) \over \ln(b/a)}{1 \over \rho}\hat{\boldsymbol{\rho}}$$

This field points from $a$ to $b$ (in $+\hat{\mathbf{\rho}}$ direction) as expected given the potential on the inner surface is higher than that on the outer surface.

2\. 

For  $\rho<a$ and $\rho>b$, Gauss' Law can be used to show $\mathbf{E}=0$, so the potential will be constant and $V_o=V_a$ for $\rho<a$ and $V_b$ for $\rho>b$ and change logarithmically in between. The curve should be concave up shape.

3\.

The electric field normal to a conductor is $E_{\perp}=\sigma/\epsilon_o$, which can be used to get the inner surface charge density and then charge conservation can be used to get outer charge density. One could also use $C=QV$ with ${C\over L} = {2\pi\epsilon_0 \over \ln(b/a)}$ to get $Q$ per unit length and then use $A=2\pi a L$ to get the charge density on the inner conductor.

4\.

Use $\sigma$ and Gauss' Law to determine $\mathbf{E}$.
|}

## Spherical

Assume the potential on the inner sphere is $V_o$ and that on the outer sphere is $0$. Note that this choice is arbitrary. The inner an outer spheres can be at arbitrary potentials $V_i$ and $V_o$ and the same answer for resistance will result.

The spheres are conductors, so the charges that appear on them will distribute uniformly on the surfaces and the distribution will be independent of $\theta$ and $\phi$. As a result, the potential will not depend on $\theta$ and $\phi$. In spherical coordinates, the Laplacian is 

$$\nabla^2V={ {1 \over r^{2}}{\partial  \over \partial r}\!\left(r^{2}{\partial V \over \partial r}\right)\!+\!{1 \over r^{2}\!\sin \theta }{\partial  \over \partial \theta }\!\left(\sin \theta {\partial V \over \partial \theta }\right)\!+\!{1 \over r^{2}\!\sin ^{2}\theta }{\partial ^{2}V \over \partial \varphi ^{2}}}$$

and the second two terms are zero. We need to solve

$$\nabla^2V={1 \over r^{2}}{\partial \over \partial r}\!\left(r^{2}{\partial V \over \partial r}\right)=0$$

Becuase $V$ depends only on $r$, we can replace the partial derivative with the total derivative

$$\nabla^2V={1 \over r^{2}}{d \over d r}\!\left(r^{2}{d V \over d r}\right)=0$$

subject to the boundary conditions

$$V(a)=V_o$$

$$V(b)=0$$

To solve the ODE, note that the following must hold

$$r^2{dV\over dr} = C_1$$

where $C_1$ is a constant.  Direct integration gives

$$V(r) = {C_1 \over r} + C_2$$

The two unknowns are solved for by using the boundary conditions

$$V(a) = V_o = {C_1 \over a} + C_2$$

$$V(b) = 0 = {C_1 \over b} + C_2$$

Solving for $C_1$ and $C_2$ gives

$$C_1 = {V_o \over \left({1\over a}-{1\over b}\right)}$$
$$C_2 = -{{V_o/b}\over{\left({1\over a}-{1\over b}\right)}}$$

and subsitution of these constants into $V(r) = {C_1 \over r} + C_2$ gives

$$V(r) = {V_o \over \left({1\over a}-{1\over b}\right)}{\left({1\over r}-{1\over b}\right)}$$

as a check of the algebraic steps, plug in $r=a$ and $r=b$ into this equation and verify that the boundary conditions used,

$$V(a)=V_o$$

$$V(b)=0$$

are satisfied.

Next, find the electric field using $\mathbf{E}=-\nabla V$. In spherical coordinates when $V$ depends only on $r$,

$$\nabla V={\partial V \over \partial r} \hat{\mathbf{r}}$$

giving

$$\mathbf{E}={V_o \over \left({1\over a}-{1\over b}\right)}{1\over r^2}\hat{\mathbf{r}}$$

This field points outward radially as expected given the potential on the inner surface is higher than that on the outer surface.

# 2-D

## Cartesian

Laplace's Equation in 2-D cartesian coordinates is 

$$\nabla^2V = \frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} = 0$$

For arbitrary constants $A,B,C,D,$ and $m$ the following four equations satisfy it

$$\mbox{I}\qquad V(x,y) = \big(A\cosh\,mx+B\sinh\,mx\big)\big(C\cos\,my+D\sin\,my\big)$$

$$\mbox{II}\qquad V(x,y) = \big(A\cos\,mx+B\sin\,mx)(C\cosh\,my+D\sinh\,my\big)$$

$$\mbox{III}\qquad V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos\,my+D\sin\,my\big)$$

$$\mbox{IV}\qquad V(x,y) = \big(A\cos\,mx+B\sin\,mx\big)\big(Ce^{my}+De^{-my}\big)$$

I use $m$ on this page instead of $k$ as is done in the text because I have been using $k$ for $1/(4\pi\epsilon_0)$.

One can argue that there are only two forms that we need to consider because (I) and (III) and (II) and (IV) are equivalent if one considers the definitions $\sinh\,z \equiv (e^{mz}-e^{-mz})/2$ and $\cosh\,z\equiv (e^{mz}+e^{-mz})/2$.

In fact, all of the equations are equivalent. If the constant $m$ is imaginary, then it can be shown that form (I) is equivalent to form (II) using Euler's identity: $e^{iz}=\cos\,z+i\sin\,z$.

The reason that all four forms are listed is that for certain problems, a certain choice of the form to start with leads to less algebra. There is no general rule about which form to start with beyond considering a few boundary conditions and looking at which equation will give coefficients that are zero immediately. An example of this will be given later.

Try these problems before continuing to read.

----

### Laplace's Equation

1. Show that $ V(x,y) = \big(A\cosh\,mx+B\sinh\,mx\big)\big(C\cos\,my+D\sin\,my\big) $ satisfies $\nabla^2V = \partial^2 V/\partial x^2 + \partial^2 V/\partial y^2 = 0$.
2. Does $m$ need to be constrained in order for $\nabla^2 V=0$?

### Equivalence of forms (I) and (III)

Show that 

$ V(x,y) = \big(A\cosh\,mx+B\sinh\,mx\big)\big(C\cos\,my+D\sin\,my\big) $

can be written as 

$ V(x,y) = \big(A'e^{mx}+B'e^{-mx})(C\cos\,my+D\sin\,my\big) $

where $A'$ and $B'$ are constants that depend on $A$ and $B$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Starting with

$ f(x) = A\cosh\,mx+B\sinh\,mx $

replace the hyperbolic forms with their corresponding exponential forms, e.g.,

$\cosh\,mx=(1/2)(e^{mx}+e^{-mx})$ and $\sinh\,mx=(1/2)(e^{mx}-e^{-mx})$

giving

$ f(x) = (A/2)(e^{mx}+e^{-mx})+(B/2)(e^{mx}-e^{-mx})

or, after rearrangment,

$ f(x) = ((A+B)/2)e^{mx}+((A-B)/2)e^{-mx}$

or

$ f(x) = A'e^{mx}+B'e^{-mx}$ where $A'\equiv(A+B)/2$ and $B'\equiv(A-B)/2$.
|}

### Equivalence of forms (I) and (II)

Suppose that it is found that $m$ is imaginary, so that it can be written as $im'$, where $m'$ is a real constant and $i=\sqrt{-1}$. Show that forms (I) and (II) are equivalent.

----


In examples 3.3 and 3.4 of Griffiths, which are 2-D cartesian problems, he comes up with an equation for $V(x,y)$ that satisfies three of the four boundary conditions and has one unknown constant:

Example 3.3: 

$$V(x,y) = Ce^{-n\pi x/a}\sin(n\pi y/a)\,\,\mbox{with}\,\, n=1,2,...$$

Example 3.4:

$$V(x,y) = C\cosh(n\pi x/a)\sin(n\pi y/a)\,\,\mbox{with}\,\, n=1,2,...$$

The capital letter used for the leading constant can be $A,B,C,$ or $D$ or a combination of them (the product of constants is a constant); in the derivation of the above two equations, Griffiths notes that the $C$ in the final equations is not the same as the $C$ in the original equations (one of form (I)-(IV)). Technically it would be better to use something like $C'$ in the final equation to emphasize this point, but to keep the notation simple, he redefines $C$.

In examples 3.3 and 3.4, Griffiths happens to choose

1. The best form (I)-(IV) to start with
2. The best order of boundary conditions to address

The problem students have with solving other problems is when they don't happen to choose the "best" way to get to the answer. In the following, I go through examples 3.3 and 3.4 by addressing the boundary conditions in a different order than Griffiths did. The examples highlight many of the actual complications one will encounter if the "best" order of addressing the boundary conditions is not selected.

### Example 3.3

The boundary conditions are

1. $V = 0$ when $y = 0$
2. $V = 0$ when $y = a$
3. $V = V_o$ when $x = 0$ - Griffiths starts by supposing $V_o(y)$ but then assumes $V_o$
4. $V\rightarrow 0$ as $x\rightarrow\infty$

Griffiths starts with form (III)

$$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos\,my+D\sin\,my\big)$$

and boundary condition 4. Here I am going to start with form (III) but boundary condition 1.


'''BC 1.''': $V = 0$ when $y = 0$

Plugging $V = 0$ and $y = 0$ into

$$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos\,my+D\sin\,my\big)$$

gives

$$0 = \big(Ae^{mx}+Be^{-mx})(C\cos\,m0+D\sin\,m0\big)$$

or

$$0 = \big(Ae^{mx}+Be^{-mx}\big)C$$

There are two ways for this equation to be true for any $x \ge 0$

1. Both $A$ and $B$ are zero. We reject this option because then form (III) reduces to $V(x,y)=0$, which satisfies Laplace's equation, but can't satisfy all of the boundary conditions.
2. $C=0$ is the remaining option.

This leaves

$$V(x,y) = \big(Ae^{mx}+Be^{-mx}\big)D\sin\,my$$

or, defining $A'=AD$ and $B'=BD$,

$$V(x,y) = \big(A'e^{mx}+B'e^{-mx}\big)\sin\,my$$


'''BC 2.''': $V = 0$ when $y = a$

Plugging these values into the equation we left off with after addressing boundary condition 1. gives

$$0 = \big(A'e^{mx}+B'e^{-mx}\big)\sin\,ma$$

There are two ways for this equation to be true for any $x \ge 0$:

1. Both $A'$ and $B'$ are zero. We reject this option because then form (III) reduces to $V(x,y)=0$, which satisfies Laplace's equation, but can't satisfy all of the boundary conditions.
2. $\sin\,ma=0$ is only the remaining option.

The only way for $\sin\,ma=0$ to be true generally is if $ma=0,\pm \pi,\pm 2\pi,...$. 

From this we conclude

$m=\frac{n\pi}{a}$ with $n$ constrained to be $0, \pm 1, \pm 2, ...$

This leaves

$$V(x,y) = \big(A'e^{n\pi x/a}+B'e^{-n\pi x/a}\big)\sin\,n\pi y/a$$

Inspection of this equation allows us to reject the possibility that $n=0$ - if $n=0$, this equation reduces to $V(x,y)=0$, which cannot satisfy all of the boundary conditions.

'''BC 3.''': $V = V_o$ when $x = 0$

Plugging these values into the equation we left off with after addressing boundary condition 2. gives

$$V_o = \big(A'e^{n\pi 0/a}+B'e^{-n\pi 0/a}\big)\sin\,n\pi y/a$$

or, because $e^0=1$,

$$V_o = \big(A'+B'\big)\sin\,n\pi y/a$$

There is only one way for this equation to be true for any $0\le y\le a$: 

$$A'+B'=V_o$$

This equation is true but is not immediately useful for simplifying our equation for $V(x,y)$. So we move on to the next boundary condition.


'''BC 4.''': $V = 0$ when $x \rightarrow \infty$

Plugging these values into the equation we left off with after addressing boundary condition 2. gives

$$V_o = \big(A'e^{n\pi \infty/a}+B'e^{-n\pi \infty/a}\big)\sin\,n\pi y/a$$

or, because $e^{-\infty}=0$,

$$V_o = \big(A'e^{n\pi \infty/a}\big)\sin\,n\pi y/a$$

There is only one way for this equation to be true: $A'=0$. (There is technically a mathematical issue that I am ignoring because zero times infinity is indeterminate; there is a way around this issue, but for now, it is not important and I'll use this dubious notation.)

Recall that the result from addressing boundary condition 3. was

$$A'+B'=V_o$$

Given that $A'=0$ is required to satisfy boundary condition 4., we conclude

$$B'=V_o$$

This leaves

$$V(x,y) = B'e^{-n\pi x/a}\sin\,n\pi y/a$$

which the same as equations 3.28 and 3.29 with one exception. In the above I concluded $n$ could be $\pm 1, \pm 2, ...$ where Griffiths concludes $n=1, 2, 3, ...$. The equivalence of these two conclusions will be shown when $B'$ is computed.

The final step is determining $B'$. This would seem to be impossible because boundary condition 3., $V = V_o$ when $x = 0$, gives

$$V_o = B'e^{-n\pi 0/a}\sin\,n\pi y/a=B'\sin(n\pi y/a)$$

and this equation needs to hold true for any $0\le y \le a$. To see that finding a $B'$ that satisfies this is impossible, suppose $y=a/2$ and $n=1$, then we have

$$V_o = B'e^{-n\pi 0/a}\sin\,n\pi y/a=B'\sin(\pi/2)$$

Giving $B'=V_o$. Now suppose $y=a/4$ and $n=1$, then

$$V_o = B'e^{-n\pi 0/a}\sin\,n\pi y/a=B'\sin(\pi/4)$$

Giving $B'=\sqrt{2}V_o$. One can repeat this for all allowed values and $n$ and you will come to the conclusion that there is no value of $B'$ that can satisfy this equation for any $0\le y \le a$.

To satisfy this last boundary condition, superposition and "Fourier's Trick" is needed.

### Example 3.4

The boundary conditions are

1. $V = 0$ when $y = 0$
2. $V = 0$ when $y = a$
3. $V = V_o$ when $x = b$
4. $V = V_o$ when $x = -b$

Griffiths starts with form (III)

$$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos\,my+D\sin\,my\big)$$

and a symmetry argument to conclude $A=B$. Here I am going to start with form (III) but boundary condition 1. In addition, I won't make use of the symmetry argument as it does not apply generally.


'''BC 1.''': $V = 0$ when $y = 0$

'''BC 2.''': $V = 0$ when $y = 0$

The starting form (III) and boundary conditions 1. and 2. are identical to that from example 3.3, so we can re-use the result concluded from addressing them:

$$V(x,y) = \big(A'e^{n\pi x/a}+B'e^{-n\pi x/a}\big)\sin\,n\pi y/a$$

with $n$ constrained to be $0, \pm 1, \pm 2, ...$.

'''BC 3.''': $V = V_o$ when $x = b$

Plugging these values into the equation we left off with after addressing boundary condition 2. gives

$$V_o = \big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)\sin\,n\pi y/a$$

Now we seem stuck. How does one constrain $A'$ and $B') for this equation to hold? We have one other boundary condition to address, so hopefully it provides some insight.

'''BC 4.''': $V = V_o$ when $x = -b$

$$V_o = \big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin\,n\pi y/a$$

Here we would seem to be stuck again. However, notice that the equation here can be combined with that from BC 4:

$$\big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)\sin\,n\pi y/a=\big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin\,n\pi y/a$$

the $\sin\,n\pi y/a$ term appears on both sides and can be dropped, leaving

$$\big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)=\big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)$$

which simplifies to

$$A'\big(e^{n\pi b/a}-e^{-n\pi b/a}\big)=B'\big(e^{n\pi b/a}-e^{-n\pi b/a}\big)$$

The terms in parentheses are identical, so we conclude

$$A'=B'$$

Therefore, the equation we ended with when addressing boundary condition 2.,

$$V(x,y) = \big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin\,n\pi y/a$$

simplifies to

$$V(x,y) = A'\big(e^{-n\pi x/a}+e^{n\pi x/a}\big)\sin\,n\pi y/a$$

This can be futher simplified using the definition $\cosh\,z=(e^z+e^{-z})/2$

$$V(x,y) = 2A'\cosh(n\pi x/a)\sin(n\pi y/a)$$

As with example 3.3, we ended up with one constant that is still unknown. This equation is equivalent to Griffiths' 3.41 if $2A'$ is replaced with a constant labeled $C$.

As was the case in my solution to example 3.3, above I concluded $n$ could be $\pm 1, \pm 2, ...$ where Griffiths concludes $n=1, 2, 3, ...$. The equivalence of these two conclusions will be shown when $A'$ is computed.

### Problems

#### Laplace's Equation

1. Show that $ V(x,y) = \big(A\cosh\,mx+B\sinh\,mx\big)\big(C\cos\,my+D\sin\,my\big) $ satisfies $\nabla^2V = \partial^2 V/\partial x^2 + \partial^2 V/\partial y^2 = 0$.
2. Does $m$ need to be constrained in order for $\nabla^2 V=0$?
3. Where does the equation $\nabla^2V = 0$ come from?
4. Why don't we use the equation $V(x,y)=\int kdq/|\mathbf{r}-\mathbf{r}'|$ to solve for the potential as we did for some problems in chapter 2 and for the image problems in chapter 3.2?
5. $ V(x,y) = \big(A\cosh\,mx+B\sinh\,mx\big)\big(C\cos\,my+D\sin\,my\big) $ satisfies $\nabla^2V = \partial^2 V/\partial x^2 + \partial^2 V/\partial y^2 = 0$. Does $m$ need to be constrained in order for $\nabla^2 V=0$?

#### Equivalence of forms (I) and (III)

Show that 

$ V(x,y) = \big(A\cosh\,mx+B\sinh\,mx\big)\big(C\cos\,my+D\sin\,my\big) $

can be written as 

$ V(x,y) = \big(A'e^{mx}+B'e^{-mx})(C\cos\,my+D\sin\,my\big) $

where $A'$ and $B'$ are constants that depend on $A$ and $B$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Starting with

$ V(x,y) = A\cosh\,mx+B\sinh\,mx $

replace the hyperbolic forms with their corresponding exponential forms, e.g.,

$\cosh\,mx=(1/2)(e^{mx}+e^{-mx})$ and $\sinh\,mx=(1/2)(e^{mx}-e^{-mx})$

giving

$ V(x,y) = (A/2)(e^{mx}+e^{-mx})+(B/2)(e^{mx}-e^{-mx})

or, after rearrangment,

$ V(x,y) = ((A+B)/2)e^{mx}+((A-B)/2)e^{-mx}$

or

$ V(x,y) = A'e^{mx}+B'e^{-mx}$ where $A'\equiv(A+B)/2$ and $B'\equiv(A-B)/2$.
|}

==== Satisfying 3 of the 4 BCs ====

Consider the boundary condition for an infinite conducting tube of
1. $V(x=0,y) = 0$ for $0\le y\le h$
2. $V(x=w,y) = 0$ for $0\le y\le h$
3. $V(x,y=0) = 0$ for $0\le x\le w$
4. $V(x,y=h) = V_0$ for $0\le x\le w$
5. Find an equation that satisfies three of the four boundary conditions and has two unknown constants, one of them being $m$.
6. What is the constraint on the values of $m$ for this problem?

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
$$V(x,y)=C\sin\,mx\,\sinh\,my$$
or
$$V(x,y)=C\sin\,mx\,\left(e^{my}-e^{-my}\right)$$
where $C$ is a constant and $m = n\pi /w$ and $n$ is a positive integer.
|}

#### Satisfying 2 of the 4 BCs

Consider the boundary condition for an infinite conducting tube of

1. $V(x=0,y) = V_o$ for $0\le y\le h$
2. $V(x=w,y) = V_o$  for $0\le y\le h$
3. $V(x,y=0) = 0$  for $0\le x\le w$
4. $V(x,y=h) = 0$  for $0\le x\le w$

This problem is similar to Example 3.4, with the difference being the location of the origin.

1. Find an equation that satisfies two of the four boundary conditions and has two unknown constants, one of them being $m$.
2. What is the constraint on the values of $m$ for this problem?

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
$(Ae^{mx} + Be^{-mx})\sin\,my$

satisfies the last two boundary conditions provided that $m=n\pi/h$, where $n$ is a positive integer.

----

As a prelude to future problems, note that you can relate $A$ and $B$ by using the first two boundary conditions

$V(x=0,y) = V_o = (Ae^{m0} + Be^{-m0})\sin\,my = (A + B)\sin\,my$

and

$V(x=w,y) = V_o = (Ae^{mw} + Be^{-mw})\sin\,my$

Combining these two equations gives $A=B(e^{-mw}-1)/(1-e^{mw})$

so that

$V(x,y) = (Ae^{mx} + Be^{-mx})(\sin\,my) = B(e^{mx}(e^{-mw}-1)/(1-e^{mw}) + e^{-mx})\sin\,my$

Although we have only satisfied two of the four boundary conditions, the equation 

(A) $V(x,y) = B(e^{mx}(e^{-mw}-1)/(1-e^{mw}) + e^{-mx})\sin\,my$

gives the same equation for the first two boundaries at $x=0$ and $x=w$ of 

$V(x=0,y) = V(x=w,y) = B\left[(e^{-mw}-e^{mw})/(1-e^{mw})\right]\sin\,my$, 

which can be shown by subtitution of $x=0$ and $x=w$ into (A) and simplifying.

When doing Fourier's trick, $x$ is replaced with its boundary value. So doing the Fourier Trick for the first boundary condition at $x=0$ using (A) would start with

$V(x=0,y) = V_o = B_1\left[(e^{-mw}-e^{mw})/(1-e^{mw})\right]\sin\,my + B_2\left[(e^{-mw}-e^{mw})/(1-e^{mw})\right]\sin\,my +...$

which is the same as the equation one would start with for the second boundary condition at $x=w$ using (A):

$V(x=w,y) = V_o = B_1\left[(e^{-mw}-e^{mw})/(1-e^{mw})\right]\sin\,my + B_2\left[(e^{-mw}-e^{mw})/(1-e^{mw})\right]\sin\,my+...$

Therefore, even though only the second two boundaries have been matched, the Fourier analysis needed to make the first two match will be identical. So Fourier's trick only needs to be applied once.  (The Fourier analysis involves finding values for $B_1,B_2,...$ such that the equality holds.)
|}

==== Series sum ====

Show that

$V(x,y) = C_1e^{-\pi x/a}\sin\,\pi y/a + C_2e^{-2\pi x/a}\sin\,2\pi y/a + C_3e^{-3\pi x/a}\sin\,3\pi y/a + ... $

satisfies Laplace's equation and the boundary conditions of Example 3.3.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
From a previous problem, we know that equations of the form (I)-(IV) satisfy Laplace's Equation, but explicitly,

$$\nabla^2 \big(C_ne^{-n\pi x/a}\sin\,n\pi y/a\big) = $$

$$C_n\sin\,n\pi y/a\frac{\partial^2 e^{-n\pi x/a}}{\partial x^2} + C_ne^{-n\pi x/a}\frac{\partial^2 \sin\,n\pi y/a}{\partial y^2} = $$

$$C_n \sin\,n\pi y/a\,(-n\pi x/a)(-n\pi x/a)e^{-n\pi x/a} + C_n e^{-n\pi x/a}(n\pi x/a)(-n\pi x/a)\sin\,n\pi y/a = 0$$

|}

==== Integrals ====

1. Show that $\int_0^\pi \sin\,2x\,\sin\,x\,dx$ = 0. Note that you can solve this without doing any calculations.  Just plot $\sin\,x$ and $\sin\,2x$ and think about the area under the curve for their product.
2. Show that $\int_0^\pi \sin\,nx\,\sin\,lx\,dx$ = 0 if $l\ne n$ by explicitly evaluating the integral.
3. Compute $\int_0^\pi \sin\,nx\,\sin\,nx\,dx$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
The motivation for giving you these problems is to help you remember that

$\int_0^\pi \sin\,nx\,\sin\,lx\,dx = 0$ if $l\ne n$

which is important for Fourier sum problems.

A way to reason this out without doing a calculation is by considering a plot of the integrand $\sin\,nx\,\sin\,lx$ over the interval $0\le x\le \pi$ by plotting two $\sin$ curves for $l\ne m$ and thinking about what the product of the curves looks like; over half interval the product will be positive and over the other half of the interval it will be negative, so the integral will be zero.

When $l=m$, the integrand is $\sin^2\,mx$, which is always positive, so its integral is not zero over any interval of $x$.
|}

#### Computing C's

Show that if the last boundary condition in Example 3.3 was $V(x=0,0\le y\le a)=V_o\,\sin(3\pi y/a)$ instead of $V(x=0,0\le y\le a)=V_o$, Fourier's Trick is not needed in order to find an equation that satisfies all four boundary conditions. (Could this last boundary be a conducting plate in this case?)

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
The equation that satisfied three of the boundary conditions in Example 3.3 was

$$V(x,y) = Ce^{-n\pi x/a}\sin\,n\pi y/a$$

To satisfy the last boundary condition, we would need values of $C$ and $n$ such that the following equality held true:

$$V(x=0,y)=V_o\,\sin(3\pi y/a) = Ce^{-n\pi 0/a}\sin\,n\pi y/a = C\sin\,n\pi y/a$$

for $0\le y\le a$. This equation is true if we select $C=V_o$ and $n=3$. One can then verify that

$$V(x,y) = V_oe^{-n\pi x/a}\sin\,3\pi y/a$$

satisfies all of the boundary conditions of Example 3.3 and Laplace's Equation. It does, and therefore we have a unique solution for the electric potential for the problem.
|}

#### Computing C's

The three steps of Fourier's Trick given above applied to the equation from Example 3.3:

$V_o = C_1e^{-\pi x/a}\sin\,\pi y/a + C_2e^{-2\pi x/a}\sin\,2\pi y/a + C_3e^{-3\pi x/a}\sin\,3\pi y/a + ... $

gives

(A) $$\int_0^a V_ody\,\sin\,l\pi y/a = C_1\int_0^a dy\,\sin\,l\pi y/a\,e^{-\pi x/a}\sin\,\pi y/a \:+\: C_2\int_0^a dy\,\sin\,l\pi y/a\,e^{-2\pi x/a}\sin\,2\pi y/a \:+\: C_3\int_0^a dy\,\sin\,l\pi y/a\,e^{-3\pi x/a}\sin\,3\pi y/a \:+\: ...$$

Show the details of the steps needed to get the same values of $C_1, C_2,$ and $C_3$ as Griffiths, which are

*$C_1=\frac{4V_o}{1\pi}$
*$C_2=0$
*$C_3=\frac{4V_o}{3\pi}$

To do this, set $l=1$ in (A) and evaluate all of the integrals. This will give you $C_1$. Next, set $l=2$ in (A) and evaluate all of the integrals.  This will give you $C_2$.
Finally, set $l=3$ in (A) and evaluate all of the integrals to get $C_3$.

Do you see why the limits of integration were chosen to be $[0,a]$? If not, try finding $C_1,C_2,C_3$ using integration limits of $[0,a/3]$.

==== Computing C's ====

Apply the three steps of Fourier's Trick to the equation you found for the problem in which the the boundary conditions were

1. $V(x=0,y) = 0$ for $0\le y\le h$
2. $V(x=w,y) = 0$ for $0\le y\le h$
3. $V(x,y=0) = 0$ for $0\le x\le w$
4. $V(x,y=h) = V_0$ for $0\le x\le w$

to the point that you have an equation similar to the last equation in the Fourier's Trick description above (which was for the problem of Example 3.3<sup>*</sup>)

To this equation,
1. Evaluate the first integral on the right-hand side and choose the integration variable and integration limits so that the result of the integration is only non-zero if $l=1$;
2. Evaluate the second and third integrals on the right-hand-side using the same integration variable and limits and $l=1$;
3. Evaluate the integral on the left-hand side using the same integration variable and limits and $l=1$; and
4. Write down the value for $C_1$ that follows from this procedure.

Note that you can find the values for $C_2$ using the same procedure but using $l=2$ instead of $l=1$, but I am only asking for $C_1$.

<sup>*</sup> The equation for Example 3.3 was

$$\int_0^a V_o\,dy\,\sin\,l\pi y/a = C_1\int_0^a dy\,\sin\,l\pi y/a\,e^{0}\sin\,\pi y/a \:+\: C_2\int_0^a dy\,\sin\,l\pi y/a\,e^{0}\sin\,2\pi y/a \:+\: C_3\int_0^a dy\,\sin\,l\pi y/a\,e^{0}\sin\,3\pi y/a \:+\: ...$$
 
#### 2-D Cartesian

Consider the boundary conditions for an infinite conducting rectangular tube of
1. $V(x=0,y) = 0$ for $0\le y\le h$
2. $V(x=w,y) = 0$ for $0\le y\le h$
3. $V(x,y=0) = 0$ for $0\le x\le w$
4. $V(x,y=h) = V_0$ for $0\le x\le w$

1. Find an equation that satisfies three of the four boundary conditions and has two unknown constants, one of them being $m$. Justify your steps and indicate why some options for satisfying certain boundary conditions are rejected.
2. What is the constraint on the values of $m$?

For reference, $V(x,y) = \big(A\cos\,mx+B\sin\,mx\big)\big(Ce^{my}+De^{-my}\big)$ satisfies Laplace's Equation.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|

For the most part, students were able to get the correct answer. In many cases, it was not clear that there was an understanding for the motivation for each of the steps, which I gave in detail in a previous lecture. This is important - in more complex problems, one has to consider all possibilities when building a solution. I have given a full justification in this solution. I didn't expect this level of detail at this point from you, and in general, I only took off is something was wrong or not-quite-correct.

Procedure: Find values of constants $A,B,C,D,m$ in 

$V(x,y) = \big(A\cos\,mx+B\sin\,mx\big)\big(Ce^{my}+De^{-my}\big)$

so that three of the four boundary conditions are matched.

BC #1: 

$V(x=0,y) = 0 = \big(A\cos\,m0+B\sin\,m0\big)\big(Ce^{my}+De^{-my}\big) = A\big(Ce^{my}+De^{-my}\big)$

This can be satisfied in two ways: (1) if $A=0$ and (2) if $C=D=0$. If we accept (2), then our answer is $V(x,y)=0$ but then we have no hope of matching the last boundary condition. So $A=0$.

BC #2 (using $A=0$):

$V(x=w,y) = 0 = \big(B\sin\,mw\big)\big(Ce^{my}+De^{-my}\big) = B\sin\,mw\,\big(Ce^{my}+De^{-my}\big)$

This BC equation can be satisfied in three ways: if (1) $B=0$, (2) $\sin\,mw=0$, (3) $C=D=0$, and (4) $m=0$. If we accept (1), (3), or (4) then our answer is $V(x,y)=0$ but then we have no hope of matching the last boundary condition. So choose $\sin\,mw=0$, which is satisfied if $mw=n\pi$, where $n=...-2,-1,0,1,2,...$. If $n=0$, then solution is $V(x,y)=0$, so we need to omit it. The negative values are not needed (can't see that here, but would see it when doing Fourier's Trick).

BC #3 (using $A=0$ but not replacing $m$ with $n\pi/w$ so equation is shorter):

$V(x,y=0) = 0 = B\sin\,mx,\big(Ce^{m0}+De^{-m0}\big) = B\sin\,mx\,(C+D)$

$\sin\,mx$ is not zero for all $0\le x\le w$. So this BC equation can be satisfied only if (1) if $B=0$ or (2) $C=-D$. Reject (1) because solution would be $V(x,y)=0$.

In summary,

$V(x,y) = BC\sin(n\pi x/w)\big(e^{n\pi y/w} - e^{-n\pi y/w}\big)$, where $n=1,2,3,...$

or

$V(x,y) = 2BC\sin(n\pi x/w)\,\sinh{n\pi y/w}$, where $n=1,2,3,...$
|}

==== Tube with Variable Potential ====

Consider the boundary condition for an infinite conducting tube of
1. $V(x=0,y) = 0$ for $0\le y\le h$
2. $V(x=w,y) = 0$ for $0\le y\le h$
3. $V(x,y=0) = 0$ for $0\le x\le w$
4. $V(x,y=h) = V_o\sin(3\pi x/w)$ for $0\le x\le w$

1. Find an equation that satisfies the first three boundary conditions and has two unknown constants, one of them being $m$. Justify your steps and indicate why some options for satisfying certain boundary conditions are rejected.
2. What is the constraint on the values of $m$ for this problem?
3. Using the last boundary condition, find the two unknown constants.
4. The boundary with potential that varies as $V_o\sin(3\pi x/w)$ cannot be a conductor. Why?
