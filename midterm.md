**PHYS 305 Midterm Exam**

October 18th, 2021

**Instructions**:

* Solve problem 1.
* Solve _two of_ problems 2., 3., and 4. Turn in **only two** of these problems. If more than two of these problems are turned in, I will grade only the first two.

# Gauss's Law (10 pts)

1. If a Gaussian sphere encloses no charge, does it follow that $\mathbf{E}=0$ on the surface of the Gaussian sphere? Justify your answer with 1--2 sentences.

2. Charge is uniformly distributed on the surface of a non--conducting spherical shell. The sphere is then dented. Is the electric field inside of the shell different after it is dented? Justify your answer with 1--2 sentences.

# Charge on Cylinder (20 pts)

Charge is uniformly distributed on the curved surface of a cylinder of length $h$ and radius $R$. The cylinder is centered on the origin, aligned with the $z$--axis, and has a charge density of $\sigma_o$.

<img src="figures/Continuous-Charge-Densities-Cylinder.svg"/>

Find an equation for $\mathbf{E}$ on the $z$--axis in terms of a single integral with an integrand that depends only on $dz'$, $z'$, $z$, and $R$. You do not need to evaluate the integral.

\newpage

# Conductors (20 pts)

The following figure shows the cross--section of a spherical conductor of radius $2R$ with a spherical cavity of radius $R$, both of which are centered on the origin. The net charge on the conductor is $q$.

There is a nonconducting spherical shell that is also centered on the origin, has $-2q$ uniformly distributed on its surface, and a radius of $3R$. At the origin, there is a charge $q$. 

<img src="figures/Conductors_Sphere_with_Cavity_with_Shell_II.svg"/>

1. Find and plot $E_r$ vs. $r$ from $r=R$ to $\infty$
2. If $V(R)=0$, find and plot $V(r)$ from $r=R$ to $\infty$

# Boundary Value Problem (20 pts)

The cross--section of a long conducting duct is shown in the following figure. Three of the sides are held at $V=0$ and the bottom side is held at $V=V_o$.

<img src="figures/Boundary_Value_Problems_2D_Bottom.svg"/>

Find a non--zero equation for $V(x,y)$ that satisfies three of the four boundary conditions.

----

Recall that for arbitrary constants $A,B,C,D,$ and $m$ the following four equations satisfy Laplace's equation in 2-D cartesian coordinates.

1. $V(x,y) = \big(A\cosh mx+B\sinh mx\big)\big(C\cos my+D\sin my\big)$
2. $V(x,y) = \big(A\cos mx+B\sin mx)(C\cosh my+D\sinh my\big)$
3. $V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos my+D\sin my\big)$
4. $V(x,y) = \big(A\cos mx+B\sin mx\big)\big(Ce^{my}+De^{-my}\big)$

----

\newpage


# Study Guide

The midterm exam will have three problems.

For additional problems to practice on, I suggest the problems in the notes linked to below and examples and in--chapter problems in Griffiths related to the topics mentioned below.

Problem 1. will be a short answer problem involving one or more of: [electric flux](flux.md!#electric-flux), [symmetry](symmetry.html), and [Gauss's law](gauss_law.html).

Problems 2. and 3. will involve two of

* Finding an integral for $\mathbf{E}$ for a continuous charge distribution (the integral will not need to be evaluated; you will need to be able to do all of the other steps). See problems in [Continuous Charge Distributions](continuous_charge_distributions.html).
* Finding $\mathbf{E}$, $V$, and $\sigma$ for charge distributions and conductor shapes for which Gauss's law can be used. See problems in [Gauss's law](gauss_law.html).
* 1--D boundary value problems -- Derive the general equation for $V$ in cartesian, cylindrical, and spherical. See problems in [1-D Boundary Value Problems](boundary_value_problems.html#1-d). Find $V$ given boundary conditions. Find $\sigma$ given $V$ (as was done in [HW 5.2](hw5.html#1-d-boundary-value-problem)). Also, solving a problem using only Gauss's law (as was done in [HW 5.1](hw5.md!#spherical-capacitor)).
* 2--D cartesian boundary value problems (either find an equation that satisfies 3 of the 4 boundary conditions or given an equation that satisfies 3 of the four boundary conditions, find $V$ using Fourier's trick). For this, review examples 3.3 and 3.4 of Griffith's, the homework problems, and variations on the homework problem ($V_o$ at all possible sides, for example). See also [2-D Boundary Value Problems](boundary_value_problems.html#1-2-cartesian).
* Finding the exact equation for $\mathbf{E}$ and $V$ for a discrete charge distribution and using the binomial expansion equation to find an approximation at large distances from the charges.
* Using the general [monopole expansion equation](monopole_expansion.html) to find an approximate expression for $V$ due to one or more point charges.


The equations that you should understand and know without reference are

* The general equation for Coulomb's Law for a point charge and charge densities;
* The general equation for electric potential due to a point charge;
* Gauss' Law in integral and differential form with an understanding of the meaning of all terms;
* Integral and differential relationship between electric field and electric potential;
* Gradient, divergence, and Laplacian in cartesian coordinates;
* "Basic" derivatives and integrals; and
* Any equations not in this list will be given as needed.

I will pay particular attention to notation. For example,

1. equations for scalars should not be written with unit vectors on the right-hand-side and
2. integrals over a closed surface should be written as $\oint$.


%A -- Can explain at a conceptual level how to solve HW problems and Griffiths example problems correctly and can justify all of the steps. Evidence for this is solutions to exam problems with correct justifications, most of the needed justifications addressed, and few algebraic errors. In addition, when the final solution does not make sense, the reason is stated.

%C -- Difficulties solving problems that were covered in a freshman--level physics course. Weak understanding of the justifications and motivations for steps in HW problems and Griffiths example problems. 

%F -- A lack of understanding of fundamental concepts covered in freshman--level physics course. Evidence for this includes writing equations that are correct but not related to the problem, writing solutions that are clearly wrong based on basic concepts without an explanation why the solution is clearly wrong.
