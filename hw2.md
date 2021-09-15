Due on Thursday, September 9th at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. Use a file name of `Yourlastname_PHYS305_HW2.pdf`. If you do not have a scanner, use a smartphone PDF scanning app such as Genius Scan or Adobe Scan. **Do not send photos of your assignment.** If you have difficulty with this, feel free to contact me for help.

You are welcome to ask questions about homework problems on Discord. I will not give direct answers, but I will give hints. I will also first ask you for your solution to a related problem that was covered in class or in the notes. You are welcome to answer questions from other students on Discord, but please only give suggestions and hints.

This homework involves topics covered in [Flux](flux.html), [Divergence](divergence.html), [Binomial Expansion](binomial_expansion.html), and [Symmetry](symmetry.html).

**Comments on grading**: If I wrote in blue pen, it is a comment. If I wrote in red or circled something I wrote in red, it is something that I took points off for. Each problem was worth 5 points.

# Particle Flux in Plane

1\. Explain why the flux through a closed line of arbitrary shape is also equal to the flux through a circle centered on the source when particles are emitted from a source with a uniform speed $v_s$ in a plane. 

<img src="figures/Flux-1D-7a.svg" width="100%"/>

2\. Explain why the flux is zero through a circle that is outside a source that emits particles uniformly in all directions with a speed $v_s$ in a plane. 

<img src="figures/Flux-1D-7b.svg" width="100%"/>

3\. Does result 2\. hold for a source that is outside of a closed loop of arbitrary shape? Briefly justify your answer.

**Answer**

1. If we imagine each dot as a person in a line walking radially outwards, every time a person passes the circle, another person passes the outer curve. (Some students mentioned that there may be a delay between when a person passes the inner line and a person passes the outer line due to the gaps. One needs to imagine that the people are packed very closesly together so that if there is a delay, it is nearly zero. Alternatively, one can state that the long--term average of the number per second of people that pass the outer and inner lines will be the same.)

  Several students attempted to provided advanced arguments that omitted key parts. In general, if a diagram was given to accompany their arguements, the flaw or missing part of their argument would have been clear. The more advanced argument requires the use of Approach II mentioned in the [Flux notes](flux.html#through-a-closed-line).

2. Argument 1. applies here.

3. To prove that the flux is the same for both closed loops in 1. is the same, one would need to use [Approach II](http://localhost:9001/flux.md!#through-a-closed-line) in the notes on flux. The same approach will work in showing that the flux through the circle (or any closed loop shape) is zero when the source is outside of the closed loop.

# $\Phi_E$ Through Cube Faces

Find the flux through each of the faces of the cube with side length $a$ when the electric field is at an angle of $60^\circ$ with respect to the $+z$-axis towards the $+x$-axis.

<img src="figures/Flux-2D-E-Field-5a.svg"/>

{\bf Answer}:

$\Phi_E^1=E_oA\sin 60^\circ = E_oa^2\sin 60^\circ$

$\Phi_E^2=0$

$\Phi_E^3=E_oA\cos 60^\circ = E_oa^2\cos 60^\circ$

$\Phi_E^4=-E_oA\cos 60^\circ = -E_oa^2\cos 60^\circ$

$\Phi_E^5=0$

$\Phi_E^6=-E_oA\sin 60^\circ = -E_oa^2\sin 60^\circ$

The total flux is zero, as expected using the flow analogy.

# $\Phi_E$ Through a Half Cylinder

A cylindrical shell (like a toilet paper roll with caps added to ends) is sliced in half as shown on the left of the following figure; on the right, a view from the +$x$--axis is shown.

<img src="figures/Flux-2D-E-Field-Half-Cylinder.svg"/>

If $\mathbf{E}=E_o\yhat$,

1\. compute the magnitude of the electric flux through the surface using $\Phi_E = \int_{\mathcal{A}} \mathbf{E}\cdot d\mathbf{A}$. Justify all of your steps for the three integrals that must be evaluated (two caps and curved surface). Recall that a differential element of area on the curved surface of a cylinder of radius $R$ is $Rd\phi dz$ and a differential element on a disk is $sdsd\phi$; and

2\. what is the magnitude of the electric flux through a full cylindrical shell with caps? Justify your answer if you answer without doing a calculation.

**Answer**:

$\Phi_E = \int_{\mathcal{A}} \mathbf{E}\cdot d\mathbf{A}$

For the top, $\mathbf{\hat{n}}=\zhat$, so $d\mathbf{A}=\zhat dA$. As a result the integrand is zero becuase $\mathbf{E}\cdot d\mathbf{A}=E_o\yhat\bfcdot \zhat dA=0$.

For the bottom, $\mathbf{\hat{n}}=-\zhat$, so $d\mathbf{A}=-\zhat dA$. As a result the integrand is zero becuase $\mathbf{E}\cdot d\mathbf{A}=E_o\yhat\bfcdot (-\zhat) dA=0$.

For the curved surface, $\mathbf{\hat{n}}=\mathbf{\hat{s}}$. To do a dot product of this with $\yhat$, we either need to write $\mathbf{\hat{s}}$ in cartesian or $\yhat$ in cylindrical. Using $\mathbf{\hat{s}}=\cos\phi\xhat + \sin\phi\yhat$, gives the dot product $\mathbf{\hat{s}}\bfcdot \yhat=\sin\phi$. The integrand can be written as $\mathbf{E}\cdot d\mathbf{A}=E_o\yhat\bfcdot \mathbf{\hat{s}}dA=E_o\sin\phi dA$. Using $dA=Rdzd\phi$, we need to perform the integral

$\displaystyle \Phi_E=\int_{0}^R\int_0^{\pi} E_o\sin\phi Rdzd\phi = -E_oRh\cos\phi\big|_0^\pi = -EoRh(\cos\pi-\cos 0) = 2E_ohR$

This flux is expected because it is also the flux through the open rectangular area, which has an area of $2Rh$. The field does not change between this rectangular area and the curved surface, and so the flux through each must be the same.

# Divergence Due to Solid Sphere of Charge

Outside of a solid sphere of radius $R$ with uniformly distributed charge $Q$, the field is

$\displaystyle\mathbf{E}(r)=kQ\frac{1}{r^2}\boldsymbol{\hat{r}}$

inside, it is

$\displaystyle\mathbf{E}(r)=kQ\frac{r}{R^3}\boldsymbol{\hat{r}}$

Compute $\boldsymbol{\nabla}\bfcdot\mathbf{E}$ using any coordinate system and plot it versus $r$.

**Answer**:

In spherical coordinates

$\displaystyle\boldsymbol{\nabla}\cdot\mathbf{E}={1 \over r^2}{\partial \left( r^2 E_r \right) \over \partial r} + {1 \over r\sin\theta}{\partial \over \partial \theta} \left(  E_\theta\sin\theta \right) + {1 \over r\sin\theta}{\partial E_\phi \over \partial \phi}$

Here we have $E_\theta=E_\phi=0$ inside and outside of the sphere.

Inside, $E_r=kQr/R^3$, so

$\displaystyle\boldsymbol{\nabla}\cdot\mathbf{E}=\frac{kQ}{R^3}\frac{1}{r^2}\frac{\partial r^3}{\partial r}=\frac{3kQ}{R^3}$

Using $k=1/4\pi\epsilon_o$, and $\rho_o=Q/(4/3)\pi R^3$, this can be written as 

$\displaystyle\boldsymbol{\nabla}\cdot\mathbf{E}=\frac{\rho_o}{\epsilon_o}$

Outside, $E_r=kQ/r^2$, so

$\displaystyle\boldsymbol{\nabla}\cdot\mathbf{E}=kQ\frac{1}{r^2}\frac{\partial r^2 (1/r^2)}{\partial r}=kQ\frac{1}{r^2}\frac{\partial (1)}{\partial r}=0\text{ for } r\ne0$

The plot is a horizontal line of amplitude $\rho_o/\epsilon_o$ for $r\lt R$ and zero for $r \gt R$. (If I ask you to plot something, I expect to see a plot even if in the solutions I sometimes don't provide a plot.)

# Symmetry

Identify at least one (a) geometrical and (b) cancellation symmetries to make statements about the electric field in the $x$--$y$ plane that results from infinite lines of charge that are parallel to the $z$--axis as shown in the following figure. The equation for the electric field due to a line of charge is $\mathbf{E}(s')=2k\lambda \mathbf{\hat{s}}'/s'$, where $s'$ is the perpendicular distance from the line as shown in the diagram.

Use a diagram to justify any statements made for (b).

<img src="figures/Symmetry-3a.svg" width="100%"/>

# Binomial Expansion

Approximate ${1}/{\sqrt{a + x}}$ using the binomial expansion to first order in $x$. Check your answer by using plugging $a=1$ and $x=0.1$ into the given equation and your approximation. They should be close.

**Answer**:

To do the expansion, we need to write the equation in the form $1/(1+\delta)^n$, where $\delta \ll 1$.

$\displaystyle \frac{1}{\sqrt{a+x}}=\frac{1}{\sqrt{a(1+\frac{x}{a})}} = \frac{1}{a^{1/2}}\frac{1}{\left(1+\frac{x}{a}\right)^{1/2}}$

From this, we identify $\delta=x/a$ and $n=1/2$, so using $1/(1+\delta)^n\simeq 1-n\delta$ gives

$\displaystyle \frac{1}{\sqrt{a+x}}\simeq \frac{1}{\sqrt{a}}\left(1 - \frac{1}{2}\frac{x}{a}\right)$

