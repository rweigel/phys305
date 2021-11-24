
# Introduction

For electrostatic fields, we found from Coulomb's law that there is a scalar function such that $\mathbf{E}=-\boldsymbol{\nabla}V$. For charge distributions that are finite in extent (e.g., not an infinite line or plane), we can compute $\mathbf{E}$ by first computing

$$\displaystyle V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int \frac{\rho(\mathbf{r}')}{\char"0509}d\tau' + \int \frac{\sigma(\mathbf{r}')}{\char"0509}dA' + \int \frac{\lambda(\mathbf{r}')}{\char"0509}dl'\right)$$

and then use $\mathbf{E}=-\boldsymbol{\nabla}V$. (In most problems, only one of the charge densities in the above equation was not zero; the equation above is the most general equation.) Given that the integrands are scalars, it is often easier to use this approach rather than computing $\mathbf{E}$ directly using Coulomb's Law:

$$\displaystyle \mathbf{E}(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int \frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}\rho(\mathbf{r}')d\tau' + \int \frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}\sigma(\mathbf{r}')dA' + \int \frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}\lambda(\mathbf{r}')dl'\right)$$

The reason that we can find $V$ for which $\mathbf{E}=-\boldsymbol{\nabla}V$ is electrostatic fields (field due to non--moving charges) have the property that $\boldsymbol{\nabla}\times \mathbf{E}=0$.

We can always compute $\mathbf{B}$ using the Biot--Savart law:

$$\displaystyle \mathbf{B}(\mathbf{r})=\frac{\mu_o}{4\pi}\left(\int d\mathbf{l}'\times\frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}J(\mathbf{r}')d\tau' + \int d\mathbf{l}'\times\frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}K(\mathbf{r}')dA' + \int d\mathbf{l}'\times\frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}I(\mathbf{r}')dl'\right)$$

(I've written the integrands in a slightly different way so that it looks more like the integrands for $\mathbf{E}$.)

From the Biot--Savart law, it can be shown that  $\boldsymbol{\nabla}\times \mathbf{B}=\mu_o\mathbf{J}$. Because $\boldsymbol{\nabla}\times \mathbf{B}\ne 0$, we cannot in general find a scalar function $V_m$ such that $\mathbf{B}=-\nabla V_m$. ($V_m$ has some use; it can be used for solving boundary value problems in current--free regions and also [when fitting measurements](https://www.ngdc.noaa.gov/IAGA/vmod/igrf.html) from current--free regions.)

However, we can find a vector function $\mathbf{A}$ for which $\mathbf{B}=\boldsymbol{\nabla}\times \mathbf{A}$. This vector is called the "vector potential," and it applies to magnetic fields only.

A natural question is why we introduce this vector potential (see also [15-4 in the Feynman Lectures on Physics](https://www.feynmanlectures.caltech.edu/II_15.html)). One of the reasons that $V$ is useful is that it is a scalar, and so instead of discussing the vector function $\mathbf{E}$, we can discuss the scalar function $V$. Also, $V$ has a physical interpretation and use -- for example, it can be used to find the work required to assemble a charge distribution. Neither of these is true for the vector potential $\mathbf{A}$. There are, however, several uses for $\mathbf{A}$. One is that the equations for finding it look similar to that for $V$:

$$\displaystyle \mathbf{A}(\mathbf{r})=\frac{\mu_o}{4\pi}\left(\int \frac{\mathbf{J}(\mathbf{r}')}{\char"0509}d\tau' + \int \frac{\mathbf{K}(\mathbf{r}')}{\char"0509}da' + \int \frac{\mathbf{I}(\mathbf{r}')}{\char"0509}dl'\right).$$

As a result, some of the techniques used in computing $V$ can be used in computing $\mathbf{A}$. In addition, some of the integrals found for $V$ can be re--used when they appear in integrals required to compute $\mathbf{A}$. Recall that the expansion of $1/\char"0509$ was used to find the multipole expansion of $V$ in Chapter 3.4 of Griffiths (so as to avoid having to integrate to find $V$ at points for which $r>r'$). The integrals for $\mathbf{A}$ have a $1/\char"0509$, and so we can use the multipole expansion to find an equation for $\mathbf{A}$  that allows us to avoid having to integrate to find $\mathbf{A}$ (and also $\mathbf{B}$ because it can be computed from $\mathbf{A}$).

A second reason that $\mathbf{A}$ is useful is that we can write $\nabla^2\mathbf{A}=-\mu_o\mathbf{J}$, which is the analog to the Poisson equation $\nabla^2V=-\rho/\epsilon_o$. Sometimes we can use the boundary value techniques for solving Poisson's equation for solving $\nabla^2\mathbf{A}=-\mu_o\mathbf{J}$ (which is actually three equations, each which have the form of Poisson's equation: $\nabla^2A_x=-\mu_oJ_x$, $\nabla^2A_y=-\mu_oJ_y$, $\nabla^2A_z=-\mu_oJ_z$.)

Finally, the vector potential appears as a natural quantity in the Lagrangian in classical mechanics and in many equations in quantum mechanics. This is discussed in detail in [15-4 in the Feynman Lectures on Physics](https://www.feynmanlectures.caltech.edu/II_15.html).

# Computing $\mathbf{B}$ given $\mathbf{A}$

Computing $\mathbf{B}$ given $\mathbf{A}$ requires only the evaluation of the curl of $\mathbf{A}$.

## Example -- $\mathbf{A}\sim \sin\theta \hat{\boldsymbol{\phi}}/{r^2}$

If $\displaystyle\mathbf{A}=\alpha \frac{\sin\theta \hat{\boldsymbol{\phi}}}{r^2}$, where $\alpha$ is a constant, find $\mathbf{B}$

**Answer**

Prior to computing the curl, it is useful to write out the scalar compoents of the vector to be curled, which are $A_r=0$, $A_\theta=0$, and $A_\phi=\alpha \sin\theta/r^2$.

The curl of a vector $\mathbf{A}$ in spherical coordinates is

$\boldsymbol{\nabla}\times \mathbf{A} =
{\frac {1}{r\sin \theta }}\left({\frac {\partial }{\partial \theta }}\left(A_{\phi }\sin \theta \right)
-
{\frac {\partial A_{\theta }}{\partial \phi }}\right) {\hat {\mathbf {r} }}
+
{\frac {1}{r}}\left({\frac {1}{\sin \theta }}{\frac {\partial A_{r}}{\partial \phi }}
-
{\frac {\partial }{\partial r}}\left(rA_{\phi }\right)\right) {\hat {\boldsymbol {\theta }}}
+
{\frac {1}{r}}\left({\frac {\partial }{\partial r}}\left(rA_{\theta }\right)
-
{\frac {\partial A_{r}}{\partial \theta }}\right) {\hat {\boldsymbol {\phi }}}$

Of the six terms involving partial derivatives, only two are non--zero.

$\boldsymbol{\nabla}\times \mathbf{A} =
{\frac {1}{r\sin \theta }}\left({\frac {\partial }{\partial \theta }}\left(A_{\phi }\sin \theta \right)
-
0\right) {\hat {\mathbf {r} }}
+
{\frac {1}{r}}\left(0
-
{\frac {\partial }{\partial r}}\left(rA_{\phi }\right)\right) {\hat {\boldsymbol {\theta }}}
+
{\frac {1}{r}}\left(0
-
0\right){\hat {\boldsymbol {\phi }}}$

Evaluation gives

$\mathbf{B}=\displaystyle\boldsymbol{\nabla}\times \mathbf{A} = \frac{\alpha}{r^3}\left(2\cos\theta{\hat {\mathbf {r} }}+\sin\theta\hat{\boldsymbol{\theta}}\right)$

This $\mathbf{B}$ has the same form as a [magnetic dipole](magnetic_dipoles.html) in spherical coordinates and unit vectors; we can conclude that this vector potential is that for a magnetic dipole for which the current system is a small loop of area $A$ centered on the origin in the $x$--$y$ plane if $\alpha = \mu_oIA/4\pi$.

## Problem --  $\mathbf{A}\sim \hat{\boldsymbol{\phi}}$

If $\mathbf{A}= \alpha\hat{\boldsymbol{\phi}}$, where $\alpha$ is a constant, what is $\mathbf{B}$?

% Answer: See 5.24 of Griffiths

## Problem -- $\mathbf{A}\sim |y|\zhat$

If $\mathbf{A} = -\alpha y \xhat$ for $y\gt 0$ and $\mathbf{A} = +\alpha y \xhat$ for $y\lt 0$, where $\alpha$ is a constant,

1. find $\mathbf{B}$ and
2. plot $B_x(y)$.
3. Based on the plot for 2., what is the current system that produced this $\mathbf{B}$?

% Answer: See 5.27 of Griffiths

# Computing $\mathbf{A}$

There are two general types of problems related to computing $\mathbf{A}$

1. if $\mathbf{B}$ is known, and
2. if $\mathbf{B}$ is not known

If $\mathbf{B}$ is known, we can sometimes (a.) find $\mathbf{A}$ by guessing what $\mathbf{A}$ will give $\mathbf{B}=\boldsymbol{\nabla}\times \mathbf{A}$, (b.) use $\mathbf{B}=\boldsymbol{\nabla}\times \mathbf{A}$, and (c.) and additional information, or using $\oint \mathbf{A}\bfcdot d\mathbf{l}=\int \mathbf{B}\bfcdot d\mathbf{l}$. As an example of (c.), see Example 5.12 of Griffiths.

If $\mathbf{B}$ is not known, we can always use direct integration to find $\mathbf{A}$. Often the integral encountered will be one that was previously used to find $V$ using direct integration. Most generally, the integral will not have a closed--form solution, and we will write the integrant of $\mathbf{A}$ as a power series as was done in the monopole expansion for $V$.

## Example -- Infinitely Long and Straight Wire

Suppose that we know $\mathbf{B}$ for an infinitely long wire along the $z$--axis with $\mathbf{I}=I\zhat$. It can be argued using symmetry that for a certain choice of integration path for the line integral that

$\displaystyle\oint \mathbf{A}\bfcdot d\mathbf{l}=\int \mathbf{B}\bfcdot d\mathbf{a}$

simplifies to

$\displaystyle A_z(s)L-A(s_o)L = L\int_{s_o}^{s} B_{\phi} ds'$

Using $\displaystyle B_\phi = \frac{\mu_o}{2\pi}\frac{I}{s}$ gives

$\displaystyle A_z(s)=A_z(s_o)-\frac{\mu_oI}{2\pi}\ln\frac{s}{s_o}$

Suppose $\mathbf{B}$ was not known. We can solve for $\mathbf{A}$ by analogy. For a finite wire along the $z$ axis that is centered on the origin and has a length $L$, the vector potential is

$\displaystyle \mathbf{A}=\int \frac{\mathbf{I}(\mathbf{r}')}{\char"0509}dl'$

Here, $dl'=dz'$ (the $dl'$ here is the differential length along the wire; in $\oint \mathbf{A}\bfcdot d\mathbf{l}$ used above, $dl$ is a path of integration). Using $\mathbf{I}=I\zhat$, we have

$\displaystyle A_z=\frac{\mu_o}{4\pi}\int_{-L/2}^{L/2} \frac{I}{\char"0509}dz'$

We have encountered an integral like this before. If, instead of a wire, we have a uniformly charged line of charge density $\lambda$, then

$\displaystyle V=\frac{1}{4\pi\epsilon_o}\int_{-L/2}^{L/2}\frac{\lambda}{\char"0509}dz'$

From this, we can conclude that we can take the answer for $V$ and replace $\lambda/\epsilon_o$ with $\mu_oI$ to get $A_z$.

For an infinitly long wire, we can't actually use the above equation to find $V$. We can only compute the potential difference $V(s)-V(s_o)=-\int_{s_o}^{s}\mathbf{E}\bfcdot d\mathbf{\hat{s}}$. For an infinite wire, $\mathbf{E}=(\lambda/2\pi\epsilon_o)\mathbf{\hat{s}}/s$ and integration gives $V(s)-V(s_o)=-(\lambda/2\pi\epsilon_o)\ln(s/s_o)$. Using the replacement of $\lambda/\epsilon_o$ with $\mu_oI$ gives

$\displaystyle A_z(s)=A_z(s_o)-\frac{\mu_oI}{2\pi}\ln\frac{s}{s_o}$

as found earlier.

## Problem -- $\mathbf{A}$ due to a finite wire segment

For a segment of wire that extends from $-L/2$ to $L/2$ on the $z$--axis with a current that flows in the $+z$ direction, find $\mathbf{A}(s)$.

## Example -- Magnetic Dipole $\mathbf{A}$ Derivation

Starting with

$$\mathbf{A} = \frac{\mu_o}{4\pi}\int \frac{\mathbf{I}dl'}{\char"0509}$$

set up the integral that must be solved to find $\mathbf{A}(x,y,z)$ due to a loop with current $I$ of radius $b$ that lies in the $x--y$ plane and is centered on the origin. 

**Answer**

$\mathbf{I}=I\hat{\boldsymbol{\phi}}$

$dl'= bd\phi'$

$\mathbf{r}'=b\hat{\mathbf{s}}$

$\mathbf{r}=x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}$

To do the integration, we need to convert non-cartesian unit vectors to cartesian unit vectors.

$\mathbf{r}'=b\hat{\mathbf{s}}=b\cos\phi'\hat{\mathbf{x}}+b\sin\phi'\hat{\mathbf{y}}$

$\mathbf{I}=I(-\sin\phi'\hat{\mathbf{x}}+\cos\phi'\hat{\mathbf{y}})$

$\char"0509=|\mathbf{r}-\mathbf{r}'|=\sqrt{(x-b\cos\phi')^2+(y-b\sin\phi')^2+z^2}$

Substitution of these three equations into

$\displaystyle \mathbf{A} = \frac{\mu_o}{4\pi}\int \frac{\mathbf{I}dl'}{\char"0509}$

gives

$\displaystyle\mathbf{A} = \frac{\mu_oIb}{4\pi}\int_0^{2\pi} \frac{d\phi'(-\sin\phi'\hat{\mathbf{x}}+\cos\phi'\hat{\mathbf{y}})}{\sqrt{(x-b\cos\phi')^2+(y-b\sin\phi')^2+z^2}}$

This equation would be the answer to a "set up the integral problem".


## Problem

1\. Use the binomial expansion on $1/\sqrt{(x-b\cos\phi')^2+(y-b\sin\phi')^2+z^2}$ to show that to leading order in $1/r$

$$\mathbf{A}(x,y,z) \simeq \frac{\mu_o}{4\pi}\frac{I\pi b^2}{r^2}\left(-\frac{y}{r}\hat{\mathbf{x}}+\frac{x}{r}\hat{\mathbf{y}}\right)$$

where $r^2=x^2+y^2+z^2$.

2\. Use the above equation for $\mathbf{A}$ to compute $\mathbf{B}$.

3\. What is $\boldsymbol{\nabla}\times\mathbf{B}$ at $r=2b$? (You can answer this without doing any partial derivatives.)

%**Answer**

%The denominator can be expanded out to

%$\displaystyle\sqrt{x^2+y^2+z^2-2bx\cos\phi'-2by\sin\phi'+b^2}$

%noting that $r^2=x^2+y^2+z^2$ and factoring out $r$ gives

%$\sqrt{x^2+y^2+z^2-2bx\cos\phi'-2by\sin\phi'+b^2}=r\sqrt{1+\delta}$

%where

%$\displaystyle\delta = -\frac{2bx}{r^2}\cos\phi'-\frac{2by}{r^2}\sin\phi'+\frac{b^2}{r^2}$

%We need to provide an argument for why $\delta \ll 1$ when $r\gg b$, which corresponds to points far away from the current loop. Clearly, $b^2/r^2$ is small for this limit. The first term can be written as

%$\displaystyle\frac{2bx}{r^2}\cos\phi'=2\frac{a}{r}\frac{x}{r}\cos\phi'$

%$\cos\phi'$ varies between $-1$ and $1$ and $a/r\ll 1$. What is left is to justify that \(x/r\) is small. That this is true can be seen by noting that $x=r\sin\theta\cos\phi$, or $x/r=\sin\theta\cos\phi$. Therefore, $x/r$ varies between $-1$ and $1$ and the term

%$\displaystyle 2\frac{b}{r}\frac{x}{r}\cos\phi'\ll 1$

%A similar argument applies to the $2by/r^2\sin\phi'$ term. Thus, we can conclude that $\delta$ will be small when $b\ll r$.

%Using the approximation

%$\displaystyle\frac{1}{(1+\delta)^{1/2}}\simeq 1 - \frac{\delta}{2}$

%which follows from a Taylor Series expansion, the integral can be written as

%$\displaystyle\mathbf{A} = \frac{\mu_oIa}{4\pi r}\int_0^{2\pi} d\phi'(-\sin\phi'\hat{\mathbf{x}}+\cos\phi'\hat{\mathbf{y}})\left(1-\frac{\delta}{2}\right)$

%The $1-\delta/2$ term can be replaced with $-\delta/2$ because the integral of the first parenthetical term in the integrand is zero.

%To finish the problem, replace $\delta$ with $ -\frac{2bx}{r^2}\cos\phi'-\frac{2by}{r^2}\sin\phi'+\frac{b^2}{r^2}$

%and multiply through, note that terms of $\cos\phi'\sin\phi'$, $\cos\phi'$ and $\sin\phi'$ appear in the integrand that integrate to zero and the only non-zero parts of the integral involve $\sin^2\phi'$ and $\cos^2\phi'$, both which integrate to $\pi$.

%There is not a closed-form solution to this integral. Use the approximation $r \gg b$ to show that the integrand can be re-written using a Taylor series expansion and that the result can be integrated to give

%$$\mathbf{A}(x,y,z) \simeq \frac{\mu_o}{4\pi}\frac{I\pi b^2}{r^2}\left(-\frac{y}{r}\hat{\mathbf{x}}+\frac{x}{r}\hat{\mathbf{y}}\right)$$

%where $r^2=x^2+y^2+z^2$.

%Compute \(\mathbf{B}(x,y,z)\) using the curl equation \(\boldsymbol{\nabla}\times\mathbf{A}\) and \(\mathbf{A}\) from the previous problem.

%Do this using the cartesian form of the curl. Keep in mind that \(r^2\) must be written as \(x^2+y^2+z^2\) before any derivatives are performed.

%**Answer**

%$$\mathbf{B}=\boldsymbol{\nabla}\times\mathbf{A}=-\hat{\mathbf{x}}\frac{\partial A_y}{\partial z}+\hat{\mathbf{y}}\frac{\partial A_x}{\partial z}+\hat{\mathbf{z}}\left(\frac{\partial A_y}{\partial x}-\frac{\partial A_x}{\partial y}\right)$$

%The two terms in curl involving the derivative of \(A_z\) are zero because \(A_z=0\).

%It is important to realize that \(r\) depends on \(x,y\), and \(z\) before evaluating the partial derivative.

%$$\frac{\partial A_y}{\partial z}=\frac{\mu_oI\pi a^2}{4\pi}\frac{\partial}{\partial z}\left(\frac{x}{(x^2+y^2+z^2)^{3/2}}\right)=\frac{\mu_oI\pi a^2}{4\pi}\frac{3xz}{(x^2+y^2+z^2)^{5/2}}$$

%etc.

%$$B_x=\frac{\mu_oI\pi a^2}{4\pi}\frac{3xz}{(x^2+y^2+z^2)^{5/2}}=\frac{\mu_oI\pi a^2}{4\pi}\frac{3xz}{r^5}$$

%$$B_y=\frac{\mu_oI\pi a^2}{4\pi}\frac{3yz}{r^5}$$

%$$B_z=\frac{\mu_oI\pi a^2}{4\pi}\frac{3z^2-r^2}{r^5}$$

%I did not cancel the \(\pi\) in these equations because \(I\pi a^2\) is the dipole moment, and it looks more familiar in this form.
