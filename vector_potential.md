
# Introduction

For electrostatic fields, we found from Coulomb's law that there is a scalar function such that $\mathbf{E}=-\boldsymbol{\nabla}V$. For charge distributions that are finite in extent (e.g., not an infinite line or plane of plane), we can compute $\mathbf{E}$ by first computing

$$\displaystyle V(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int \frac{\rho(\mathbf{r}')}{\char"0509}d\tau' + \int \frac{\sigma(\mathbf{r}')}{\char"0509}dA' + \int \frac{\lambda(\mathbf{r}')}{\char"0509}dl'\right)$$

and then using $\mathbf{E}=-\boldsymbol{\nabla}V$. (In most problems, only one of the charge densities in the above equation was not zero; this is the most general equation.) Given that the integrands are scalars, it is often easier to use this approach rather than computing $\mathbf{E}$ directly using Coulomb's Law:

$$\displaystyle \mathbf{E}(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int \frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}\rho(\mathbf{r}')d\tau' + \int \frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}\sigma(\mathbf{r}')dA' + \int \frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}\lambda(\mathbf{r}')dl'\right)$$

The reason that we can find $V$ for which $\mathbf{E}=-\boldsymbol{\nabla}V$ is because electrostatic fields (field due to static charges) have the property that $\boldsymbol{\nabla}\times \mathbf{E}=0$.

We can always compute $\mathbf{B}$ using the Biot--Savart law:

$$\displaystyle \mathbf{B}(\mathbf{r})=\frac{\mu_o}{4\pi}\left(\int \frac{d\mathbf{l}'\times\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}J(\mathbf{r}')d\tau' + \int \frac{d\mathbf{l}'\times\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}K(\mathbf{r}')dA' + \int \frac{d\mathbf{l}'\times\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}I(\mathbf{r}')dl'\right)$$

From the Biot--Savart law, it can be shown that  $\boldsymbol{\nabla}\times \mathbf{B}=\mu_o\mathbf{J}$. Because $\boldsymbol{\nabla}\times \mathbf{B}\ne 0$ in general, we cannot in general find a scalar function $V_m$ such that $\mathbf{B}=-\nabla V_m$.

However, we can find a vector function $\mathbf{A}$ for which $\mathbf{B}=\boldsymbol{\nabla}\times \mathbf{A}$. This vector is called the "vector potential" and it applies to magnetic fields only.

A natural question is why we introduce this vector potential (see also [15-4 in the Feynman Lectures on Physics](https://www.feynmanlectures.caltech.edu/II_15.html)). One of the reasons that $V$ is useful is that it is a scalar and so instead of discussing the vector function $\mathbf{E}$ we can discuss the scalar function $V$. In addition, $V$ has a physical interpretation and use -- for example, it can be used to find the work required to assemble a charge distribution. The vector potential $\mathbf{A}$ does not have these two advantages. There are, however, several uses for $\mathbf{A}$. One is that the equations finding it look similar to that for $V$:

$$\displaystyle \mathbf{A}(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\left(\int \frac{\mathbf{J}(\mathbf{r}')}{\char"0509}d\tau' + \int \frac{\mathbf{K}(\mathbf{r}')}{\char"0509}dA' + \int \frac{\mathbf{I}(\mathbf{r}')}{\char"0509}dl'\right)$$

As a result, some of the techniques used in computing $V$ can be used in computing $\mathbf{A}$. In addition, some of the integrals found for $V$ can be re--used when they appear in integrals required to compute $\mathbf{A}$. Recall that we used the expansion of $1/\char"0509$ to find the multipole expansion of $V$ (so as to avoid having to do integration to find $V$ at points for which $r>r'$). The integrals for $\mathbf{A}$ have a $1/\char"0509$, and so we can use the multipole expansion to find an equation for $\mathbf{A}$  that allows us to avoid having to do integration to find $\mathbf{A}$ (and also $\mathbf{B}$, because it can be computed from $\mathbf{A}$).

A second reason that $\mathbf{A}$ is useful is that we can write $\nabla^2\mathbf{A}=-\mu_o\mathbf{J}$, which is the analog to the Poisson equation $\nabla^2V=-\rho/\epsilon_o$. Sometimes we can use the boundary value techniques for solving Poisson's equation for solving $\nabla^2\mathbf{A}=-\mu_o\mathbf{J}$ (which is actually three equations, each which have the form of Poisson's equation: $\nabla^2A_x=-\mu_oJ_x$, $\nabla^2A_y=-\mu_oJ_y$, $\nabla^2A_z=-\mu_oJ_z$.)

Finally, the vector potential appears as a natural quantity in the Lagrangian in classical mechanics and in many equations in quantum mechanics.

## Example -- Magnetic Dipole $\mathbf{A}$ Derivation

Starting with

$$\mathbf{A} = \frac{\mu_o}{4\pi}\int \frac{\mathbf{I}dl'}{\char"0509}$$

set up the integral that must be solved to find $\mathbf{A}(x,y,z)$ due to a loop with current $I$ of radius $b$ that lies in the $x--y$ plane and is centered on the origin. 

There is not a closed-form solution to this integral. Use the approximation $r \gg b$ to show that the integrand can be re-written using a Taylor series expansion and that the result can be integrated to give

$$\mathbf{A}(x,y,z) \simeq \frac{\mu_o}{4\pi}\frac{I\pi b^2}{r^2}\left(-\frac{y}{r}\hat{\mathbf{x}}+\frac{x}{r}\hat{\mathbf{y}}\right)$$

where $r^2=x^2+y^2+z^2$.

**Answer**

$\mathbf{A} = \frac{\mu_o}{4\pi}\int \frac{\mathbf{I}dl'}{\char"0509}$

$\mathbf{I}=I\hat{\boldsymbol{\phi}}$

$dl'= bd\phi'$

$\mathbf{r}'=b\hat{\mathbf{s}}$

$\mathbf{r}=x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}$

To do the integration, we need to convert non-cartesian unit vectors to cartesian unit vectors (as covered on an earlier homework problem).

$\mathbf{r}'=b\hat{\mathbf{s}}=b\cos\phi'\hat{\mathbf{x}}+b\sin\phi'\hat{\mathbf{y}}$

$\mathbf{I}=I(-\sin\phi'\hat{\mathbf{x}}+\cos\phi'\hat{\mathbf{y}})$

$\char"0509=|\mathbf{r}-\mathbf{r}'|=\sqrt{(x-b\cos\phi')^2+(y-b\sin\phi')^2+z^2}$

Using these results in

$\displaystyle \mathbf{A} = \frac{\mu_o}{4\pi}\int \frac{\mathbf{I}dl'}{\char"0509}$

gives

$\displaystyle\mathbf{A} = \frac{\mu_oIa}{4\pi}\int_0^{2\pi} \frac{d\phi'(-\sin\phi'\hat{\mathbf{x}}+\cos\phi'\hat{\mathbf{y}})}{\sqrt{(x-a\cos\phi')^2+(y-a\sin\phi')^2+z^2}}$

This equation would be the answer to a "set up the integral problem".

This integral does not have a closed-form solution. If we assume that \(r\gg a\), we can find an approximate solution.

The denominator can be expanded out to

$\displaystyle\sqrt{x^2+y^2+z^2-2bx\cos\phi'-2by\sin\phi'+b^2}$

noting that $r^2=x^2+y^2+z^2$ and factoring out $r$ gives

$\sqrt{x^2+y^2+z^2-2bx\cos\phi'-2by\sin\phi'+b^2}=r\sqrt{1+\delta}$

where

$\displaystyle\delta = -\frac{2bx}{r^2}\cos\phi'-\frac{2by}{r^2}\sin\phi'+\frac{b^2}{r^2}$

We need to provide an argument for why $\delta \ll 1$ when $r\gg b$, which corresponds to points far away from the current loop. Clearly $b^2/r^2$ is small for this limit. The first term can be written as

$\displaystyle\frac{2bx}{r^2}\cos\phi'=2\frac{a}{r}\frac{x}{r}\cos\phi'$

\(\cos\phi'\) varies between \(-1\) and \(1\) and \(a/r\) is small. What is left is to justify that \(x/r\) is small. That this is true can be seen by noting that \(x=r\sin\theta\cos\phi\), or \(x/r=\sin\theta\cos\phi\). Therefore, \(x/r\) varies between \(-1\) and \(1\) and the term

$\displaystyle 2\frac{b}{r}\frac{x}{r}\cos\phi'\ll 1$

A similar argument applies to the $2by/r^2\sin\phi'$ term. Thus, we can conclude that $\delta$ will be small when $b\ll r$.

Using the approximation

$\displaystyle\frac{1}{(1+\delta)^{1/2}}\simeq 1 - \frac{\delta}{2}$

which follows from a Taylor Series expansion, the integral can be written as

$\displaystyle\mathbf{A} = \frac{\mu_oIa}{4\pi r}\int_0^{2\pi} d\phi'(-\sin\phi'\hat{\mathbf{x}}+\cos\phi'\hat{\mathbf{y}})\left(1-\frac{\delta}{2}\right)$

The $1-\delta/2$ term can be replaced with $-\delta/2$ because the integral of the first parenthetical term in the integrand is zero.

To finish the problem, replace $\delta$ with $ -\frac{2bx}{r^2}\cos\phi'-\frac{2by}{r^2}\sin\phi'+\frac{b^2}{r^2}$

and multiply through, note that terms of $\cos\phi'\sin\phi'$, $\cos\phi'$ and $\sin\phi'$ appear in the integrand that integrate to zero and the only non-zero parts of the integral involve $\sin^2\phi'$ and $\cos^2\phi'$, both which integrate to $\pi$.

## Example -- Magnetic Dipole $\mathbf{B}$ Derivation

Compute \(\mathbf{B}(x,y,z)\) using the curl equation \(\boldsymbol{\nabla}\times\mathbf{A}\) and \(\mathbf{A}\) from the previous problem.

Do this using the cartesian form of the curl. Keep in mind that \(r^2\) must be written as \(x^2+y^2+z^2\) before any derivatives are performed.

**Answer**

$$\mathbf{B}=\boldsymbol{\nabla}\times\mathbf{A}=-\hat{\mathbf{x}}\frac{\partial A_y}{\partial z}+\hat{\mathbf{y}}\frac{\partial A_x}{\partial z}+\hat{\mathbf{z}}\left(\frac{\partial A_y}{\partial x}-\frac{\partial A_x}{\partial y}\right)$$

The two terms in curl involving the derivative of \(A_z\) are zero because \(A_z=0\).

It is important to realize that \(r\) depends on \(x,y\), and \(z\) before evaluating the partial derivative.

$$\frac{\partial A_y}{\partial z}=\frac{\mu_oI\pi a^2}{4\pi}\frac{\partial}{\partial z}\left(\frac{x}{(x^2+y^2+z^2)^{3/2}}\right)=\frac{\mu_oI\pi a^2}{4\pi}\frac{3xz}{(x^2+y^2+z^2)^{5/2}}$$

etc.

$$B_x=\frac{\mu_oI\pi a^2}{4\pi}\frac{3xz}{(x^2+y^2+z^2)^{5/2}}=\frac{\mu_oI\pi a^2}{4\pi}\frac{3xz}{r^5}$$

$$B_y=\frac{\mu_oI\pi a^2}{4\pi}\frac{3yz}{r^5}$$

$$B_z=\frac{\mu_oI\pi a^2}{4\pi}\frac{3z^2-r^2}{r^5}$$

I did not cancel the \(\pi\) in these equations because \(I\pi a^2\) is the dipole moment and it looks more familiar in this form.
