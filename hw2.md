Due on Thursday, September 9th at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. Use a file name of `Yourlastname_PHYS305_HW2.pdf`. If you do not have a scanner, use a smartphone PDF scanning app such as Genius Scan or Adobe Scan. **Do not send photos of your assignment.** If you have difficulty with this, feel free to contact me for help.

You are welcome to ask questions about homework problems on Discord. I will not give direct answers, but I will give hints. I will also first ask you for your solution to a related problem that was covered in class or in the notes. You are welcome to answer questions from other students on Discord, but please only give suggestions and hints.

This homework involves topics covered in [Flux](flux.html), [Divergence](divergence.html), [Binomial Expansion](binomial_expansion.html), and [Symmetry](symmetry.html).

# Particle Flux in Plane

1\. Explain why the flux through a closed line of arbitrary shape is also equal to the flux through a circle centered on the source when particles are emitted from a source with a uniform speed $v_s$ in a plane. 

<img src="figures/Flux-1D-7a.svg" width="100%"/>

2\. Explain why the flux is zero through a circle that is outside a source that emits particles uniformly in all directions with a speed $v_s$ in a plane. 

<img src="figures/Flux-1D-7b.svg" width="100%"/>

3\. Does result 2\. hold for a source that is outside of a closed loop of arbitrary shape? Briefly justify your answer.

In answering these questions, you do not need to do a derivation -- just use a diagram and/or a few sentences to justify the statement or answer.

# $\Phi_E$ Through Cube Faces

Find the flux through each of the faces of the cube with side length $a$ when the electric field is at an angle of $60^\circ$ with respect to the $+z$-axis towards the $+x$-axis.

<img src="figures/Flux-2D-E-Field-5a.svg"/>

%{\bf Answer}:

%$\Phi_E^1=E_oA\sin 60^\circ = E_oa^2\sin 60^\circ$

%$\Phi_E^2=0$

%$\Phi_E^3=E_oA\cos 60^\circ = E_oa^2\cos 60^\circ$

%$\Phi_E^4=-E_oA\cos 60^\circ = -E_oa^2\cos 60^\circ$

%$\Phi_E^5=0$

%$\Phi_E^6=-E_oA\sin 60^\circ = -E_oa^2\sin 60^\circ$

# $\Phi_E$ Through a Half Cylinder

A cylindrical shell (like a toilet paper roll with caps added to ends) is sliced in half as shown on the left of the following figure; on the right, a view from the +$x$--axis is shown.

<img src="figures/Flux-2D-E-Field-Half-Cylinder.svg"/>

If $\mathbf{E}=E_o\yhat$,

1\. compute the magnitude of the electric flux through the surface using $\Phi_E = \int_{\mathcal{A}} \mathbf{E}\cdot d\mathbf{A}$. Justify all of your steps for the three integrals that must be evaluated (two caps and curved surface). Recall that a differential element of area on the curved surface of a cylinder of radius $R$ is $Rd\phi dz$ and a differential element on a disk is $sdsd\phi$; and

2\. what is the magnitude of the electric flux through a full cylindrical shell with caps? Justify your answer if you answer without doing a calculation.

# Divergence Due to Solid Sphere of Charge

Outside of a solid sphere of radius $R$ with uniformly distributed charge $Q$, the field is

$\displaystyle\mathbf{E}(r)=kQ\frac{1}{r^2}\boldsymbol{\hat{r}}$

inside, it is

$\displaystyle\mathbf{E}(r)=kQ\frac{r}{R^3}\boldsymbol{\hat{r}}$

Compute $\boldsymbol{\nabla}\bfcdot\mathbf{E}$ using any coordinate system and plot it versus $r$.

# Symmetry

Identify at least one (a) geometrical and (b) cancellation symmetries to make statements about the electric field in the $x$--$y$ plane that results from infinite lines of charge that are parallel to the $z$--axis as shown in the following figure. The equation for the electric field due to a line of charge is $\mathbf{E}(s')=2k\lambda \mathbf{\hat{s}}'/s'$, where $s'$ is the perpendicular distance from the line as shown in the diagram.

Use a diagram to justify any statements made for (b).

<img src="figures/Symmetry-3a.svg" width="100%"/>

# Binomial Expansion

Approximate ${1}/{\sqrt{a + x}}$ using the binomial expansion to first order in $x$. Check your answer by using plugging $a=1$ and $x=0.1$ into the given equation and your approximation. They should be close.
