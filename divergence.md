# Definition

See 1.2.4 of Griffiths.

The divergence of a vector field is is a scalar defined to be

$$\text{div}(\mathbf{U})=\lim_{\Delta \tau\rightarrow 0}\frac{\oint \mathbf{U}\bfcdot d\mathbf{A}}{\Delta \tau}$$

at any point in space, where $\Delta \tau$ is a differential volume that surrounds the point. The numerator is a flux, so the physical interpretation is that it represents the net flux into or out of a vanishingly small volume.

In general, this formula will not be used to compute divergence. However, it is important to understand its meaning.

## Example

If $\mathbf{U}=U_x(x)\xhat$ 

1\. Compute $\text{div}(\mathbf{U})$ that applies for any point $x$.

2\. Evaluate $\text{div}(\mathbf{U})$ when $U_x(x)=U_o$

**Answer**

A side view of a cube with sides of $\Delta x$, $\Delta y$, and $\Delta z$ is shown in the following figure.

1\. 
Only two of the six sides contribute to the flux $\oint \mathbf{U}\bfcdot d\mathbf{A}$. The right side contributes $+U_x(x+\Delta x/2)\Delta y\Delta z$ and the left side contributes $-U_x(x-\Delta x/2)\Delta y\Delta z$. The differential volume is $\Delta \tau = \Delta x\Delta y\Delta z$. As a result, 

$\displaystyle\text{div}(\mathbf{U})=\lim_{\Delta \tau\rightarrow 0}\frac{\oint \mathbf{U}\bfcdot d\mathbf{A}}{\Delta \tau}=\lim_{\Delta \tau\rightarrow 0}\frac{+U_x(x+\Delta x/2)\Delta y\Delta z-U_x(x-\Delta x/2)\Delta y\Delta z}{\Delta x\Delta y\Delta z}$

This simplifies to

$\displaystyle\text{div}(\mathbf{U})=\lim_{\Delta x\rightarrow 0}\frac{U(x+\Delta x/2)-U(x-\Delta x/2)}{\Delta x}$

which is the definition of the derivate of $U_x(x)$. We conclude that

$\displaystyle\text{div}(\mathbf{U})=\frac{dU_x(x)}{dx}$

2\. When $U_x(x)=0$, $\displaystyle\frac{dU_x(x)}{dx}=0$, so $\text{div}(\mathbf{U})=0$.

----

If $\partial U_x/\partial x$, $\partial U_y/\partial y$, and $\partial U_z/\partial z$ all exist, then we do not need to evaluate a surface integral and take a limit to compute $\text{div}(\mathbf{U})$. In this case, in cartesian coordinates, 

$$\text{div}(\mathbf{U}) = \boldsymbol{\nabla}\bfcdot\mathbf{U}=\frac{\partial U_x}{\partial x}+\frac{\partial U_y}{\partial y}+\frac{\partial U_z}{\partial z}$$

The definition

$$\boldsymbol{\nabla} \equiv  \xhat\frac{\partial }{\partial x}+\yhat\frac{\partial }{\partial y}+\zhat\frac{\partial f}{\partial z}$$

was used. If $\mathbf{U}=U_x(x)\xhat$ as in the previous problem, we get $\boldsymbol{\nabla}\bfcdot\mathbf{U}=\frac{\partial U_x(x)}{\partial x}=\frac{d U_x(x)}{d x}$, which is the same result found using the definition of $\text{div}(\mathbf{U})$ involving the flux in the previous problem. In general, we will compute divergences using the formula $\boldsymbol{\nabla}\bfcdot\mathbf{U}$ instead of equation that defines $\text{div}(\mathbf{U})$.

> Caution: It is easy to mix up the gradient and divergence. 
> The gradient involves multiplying the vector operator $\boldsymbol{\nabla}$ by a scalar function $f(x,y,z)$, so the result is a vector:
>
>$\displaystyle\boldsymbol{\nabla}f(x,y,z)=\frac{\partial f}{\partial x}\xhat+\frac{\partial f}{\partial y}\yhat+\frac{\partial f}{\partial z}\zhat$
>
> The divergence involves dotting the vector operator $\boldsymbol{\nabla}$ with a vector function $\mathbf{U}(x,y,z)$, so the result is a scalar:
>
> $\displaystyle\boldsymbol{\nabla}\bfcdot\mathbf{U}=\frac{\partial U_x(x,y,z)}{\partial x}+\frac{\partial U_y(x,y,z)}{\partial y}+\frac{\partial U_z(x,y,z)}{\partial z}$


## Example

If $\mathbf{U}=U_o\xhat$, compute $\text{div}(\mathbf{U})$ using $\boldsymbol{\nabla}\bfcdot\mathbf{U}$.

**Answer**:

Here $U_x=U_o$ and $U_y=U_z=0$ so

$\displaystyle\boldsymbol{\nabla}\bfcdot\mathbf{U}=\frac{\partial U_x(x,y,z)}{\partial x}+\frac{\partial U_y(x,y,z)}{\partial y}+\frac{\partial U_z(x,y,z)}{\partial z}=\frac{\partial U_o}{\partial x}=0$

which is the same result found in the previous example using the definition of $\text{div}(\mathbf{U})$

## Example

If $\mathbf{U}=U_o\hat{\mathbf{s}}$, compute  $\text{div}(\mathbf{U})$ using $\boldsymbol{\nabla}\bfcdot\mathbf{U}$.

**Answer**:

To compute $\frac{\partial U_x(x,y,z)}{\partial x}+\frac{\partial U_y(x,y,z)}{\partial y}+\frac{\partial U_z(x,y,z)}{\partial z}$

we need to first write $\mathbf{\hat{s}}$ fully in cartesian coordinates. From [Vectors](vectors.md#cylindrical), $\hat{\mathbf{s}} = \cos\phi\xhat + \sin\phi\yhat$, $\cos\phi = x/\sqrt{x^2+y^2}$, and $\sin\phi = x/\sqrt{x^2+y^2}$, so

$$\hat{\mathbf{s}}=\frac{x}{\sqrt{x^2+y^2}}\xhat + \frac{y}{\sqrt{x^2+y^2}}\yhat$$

and thus $U_x=U_ox/\sqrt{x^2+y^2}$, $U_y = U_o y/\sqrt{x^2+y^2}$.

An easier way to solve this is to use the vector operator $\boldsymbol{\nabla}$ written in cylindrical coordinates. The equation is given on the second--to--last page of Griffiths and is

$$\boldsymbol{\nabla}\cdot\mathbf{U}={1 \over s}{\partial \left( s U_s  \right) \over \partial s}+{1 \over s}{\partial U_\phi \over \partial \phi}+{\partial U_z \over \partial z}$$

For $\mathbf{U}=U_o\hat{\mathbf{s}}$, $U_s=U_o$ and $U_\phi=U_z=0$ and so the last two terms are zero and the first term is straight--forward to calculate:

$$\boldsymbol{\nabla}\cdot\mathbf{U}={1 \over s}{\partial \left( s U_s  \right) \over \partial s}=\frac{1}{s}\frac{\partial (sU_o)}{\partial s}=U_o$$


## Problem

$\mathbf{U}=U_o\hat{\mathbf{r}}$, compute  $\text{div}(\mathbf{U})$ using $\boldsymbol{\nabla}\bfcdot\mathbf{U}$ in two ways

1\. Using the equation for $\boldsymbol{\nabla}$ fully in cartesian coordinates.

2\. Using the equation for $\boldsymbol{\nabla}$ in spherical coordinates.

## Problem

If $\mathbf{U}=\hat{\mathbf{r}}/r^2$ show that  

$\boldsymbol{\nabla}\bfcdot\mathbf{U}=0$ if $r\ne 0$

and

$\boldsymbol{\nabla}\bfcdot\mathbf{U}=\frac{0}{0}$ if $r=0$. 

You may do this using any coordinate system.

## Problem

Outside of a solid and long cylinder of radius $R$ with a uniform linear charge density of $\lambda$, the field is

$\displaystyle\mathbf{E}(s)=2k\lambda\frac{\boldsymbol{\hat{s}}}{s}$

inside, it is

$\displaystyle\mathbf{E}(s)=2k\lambda\frac{s}{R^2}\boldsymbol{\hat{s}}$

Compute $\boldsymbol{\nabla}\bfcdot\mathbf{E}$ using any coordinate system and plot it versus $s$.

## Problem

Outside of a solid sphere of radius $R$ with uniformly distributed charge $Q$, the field is

$\displaystyle\mathbf{E}(r)=kQ\frac{1}{r^2}\boldsymbol{\hat{r}}$

inside, it is

$\displaystyle\mathbf{E}(r)=kQ\frac{r}{R^3}\boldsymbol{\hat{r}}$

Compute $\boldsymbol{\nabla}\bfcdot\mathbf{E}$ using any coordinate system and plot it versus $r$.

# The Divergence Theorem

See 1.3.4 of Griffiths.

$$\int_{\mathcal{V}} \text{div}(\mathbf{U}) d\tau=\oint_{\mathcal A} \mathbf{U}\cdot d\mathbf{A}$$

In general, the defining equation for divergence involving a limit will not be used and instead $\text{div}(\mathbf{U})=\boldsymbol{\nabla}\bfcdot\mathbf{U}$ is used. In this case,

$$\int_{\mathcal{V}} (\boldsymbol{\nabla}\bfcdot\mathbf{U}) d\tau=\oint_{\mathcal A} \mathbf{U}\cdot d\mathbf{A}$$

This is a key vector calculus theorem that is used to derive Gauss's law. The interpretation is that if we add up all of the divergences within a volume $\mathcal{V}$, we will get the same result if we compute the flux through the closed surface $\mathcal{A}$ that encloses the volume.

## Example

Test the divergence theorem using $\mathbf{U}=\hat{\mathbf{r}}$ and a sphere of radius $R$ centered on the origin.

## Problem

Test the divergence theorem using $\mathbf{U}=r\hat{\mathbf{r}}$ and a sphere of radius $R$ centered on the origin.

## Example

Test the divergence theorem using $\mathbf{U}=\hat{\mathbf{r}}/r^2$ and a sphere of radius $R$ centered on the origin.

## Problem 

If $\mathbf{U}=\hat{\mathbf{r}}/r^2$, use the divergence theorem to find the flux $\Phi_U$ through a sphere of radius $R$ centered on $z=2R$.

