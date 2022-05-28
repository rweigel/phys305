# Legendre polynomials

$${\displaystyle {\begin{array}{r|r}n&P_{n}(x)\\\hline 0&1\\1&x\\2&{\tfrac {1}{2}}\left(3x^{2}-1\right)\\3&{\tfrac {1}{2}}\left(5x^{3}-3x\right)\\4&{\tfrac {1}{8}}\left(35x^{4}-30x^{2}+3\right) \end{array}}}$$

# Coordinate Transformation

## Cartesian $\leftrightarrow$ Cylindrical
$$\begin{bmatrix}\hat{\mathbf{r}} \\ \boldsymbol{\hat{\phi}} \\ \hat{\mathbf{z}}\end{bmatrix}  = \begin{bmatrix}\cos \phi & \sin \phi & 0 \\ -\sin \phi &\cos \phi & 0 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix}\hat{\mathbf{x}} \\ \hat{\mathbf{y}} \\ \hat{\mathbf{z}}\end{bmatrix}$$

$$\begin{bmatrix}\hat{\mathbf{x}} \\ \hat{\mathbf{y}} \\ \hat{\mathbf{z}}\end{bmatrix}  = \begin{bmatrix}\cos \phi & -\sin \phi & 0 \\ \sin \phi &\cos \phi & 0 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix}\hat{\mathbf{r}} \\ \boldsymbol{\hat{\phi}} \\ \hat{\mathbf{z}}\end{bmatrix}$$

# Cartesian $\leftrightarrow$ Spherical

$$\begin{bmatrix}{\hat{\boldsymbol{r}}} \\ {\hat{\boldsymbol{\theta }}} \\ {\hat{\boldsymbol{\varphi }}}\end{bmatrix} = \begin{bmatrix}\sin \theta\cos \varphi & \sin\theta \sin\varphi & \cos\theta \\ \cos\theta \cos\varphi & \cos\theta \sin\varphi & -\sin\theta \\ -\sin\varphi & \cos\varphi & 0 \end{bmatrix} \begin{bmatrix}{\hat{\mathbf{x}}} \\ {\hat{\mathbf{y}}} \\{\hat{\mathbf{z}}}\end{bmatrix}$$

$$\begin{bmatrix}\hat{\mathbf{x}} \\ \hat{\mathbf{y}} \\ \hat{\mathbf{z}}\end{bmatrix} = \begin{bmatrix} \sin\theta\cos\varphi & \cos\theta\cos\varphi & -\sin\varphi \\ \sin\theta\sin\varphi & \cos\theta\sin\varphi &  \cos\varphi \\ \cos \theta & -\sin\theta & 0 \end{bmatrix} \begin{bmatrix}\hat{\boldsymbol{r}} \\ \hat{\boldsymbol{\theta}} \\ \hat{\boldsymbol{\varphi}}\end{bmatrix}$$

=== Problems ===

* Convert \(\) to 
* Convert \(\) to
* Convert \(\) to 

=== Problems ===

Derive the matrix transformation equations using a diagram.

**Notes**

See any Calculus Textbook. These transformations can always be looked up, but if you are able to easily derive them, typical coordinate transformation problems that can't be looked up will be easy.

# Vector Equations

## Cartesian

Gradient for scalar function $f(x, y, z)$

$$
\nabla f = 
{\partial f \over \partial x}\xhat
+
{\partial f \over \partial x}\yhat
+
{\partial f \over \partial x}\zhat
$$

Divergence of a vector function $\mathbf{U}(x, y, z)$

$$
\boldsymbol{\nabla}\cdot\mathbf{U} =
{\partial U_x \over \partial x}
+
{\partial U_y \over \partial y}
+
{\partial U_z \over \partial z}
$$

Curl for vector function $\mathbf{U}(x,y,z)$

$$
\boldsymbol{\nabla}\times \mathbf{U} = 
\left(\frac{\partial U_z }{\partial y}
-
\frac{\partial U_y }{\partial z} \right)\xhat
+
\left(\frac{\partial U_x }{\partial z}
-
\frac{\partial U_z }{\partial x} \right)\yhat
+
\left(\frac{\partial U_y }{\partial x}
-
\frac{\partial U_x }{\partial y} \right)\zhat
$$

Laplacian for scalar function $f(x,y,z)$

$$\nabla^2f=\boldsymbol{\nabla}\cdot(\boldsymbol{\nabla}f) =
{\partial^2 f \over \partial x^2}
+
{\partial^2 f \over \partial y^2}
+
{\partial^2 f \over \partial z^2}
$$
 
## Cylindrical

Gradient for scalar function $f(s, \phi, z)$

$$
\nabla f = 
{\partial f \over \partial \rho}\hat{\boldsymbol \rho}
+
{1 \over \rho}{\partial f \over \partial \phi}\hat{\boldsymbol \phi}
+
{\partial f \over \partial z}\hat{\mathbf z}
$$

$$
\nabla f = 
{\partial f \over \partial s}\hat{\boldsymbol s}
+
{1 \over s}{\partial f \over \partial s}\hat{\boldsymbol \phi}
+
{\partial f \over \partial z}\hat{\mathbf z}
$$


Divergence of a vector function $\mathbf{U}(s, \phi, z)$

$$
\boldsymbol{\nabla}\cdot\mathbf{U} =
{1 \over \rho}{\partial \left( \rho U_\rho  \right) \over \partial \rho}
+
{1 \over \rho}{\partial U_\phi \over \partial \phi}
+
{\partial U_z \over \partial z}
$$

$$
\boldsymbol{\nabla}\cdot\mathbf{U} = 
{1 \over s}{\partial \left( s U_s  \right) \over \partial s}
+
{1 \over s}{\partial U_\phi \over \partial \phi}
+
{\partial U_z \over \partial z}
$$

Curl of a vector function $\mathbf{U}(x,y,z)$

$$
\boldsymbol{\nabla}\times \mathbf{A} = 
\left({\frac {1}{\rho }}{\frac {\partial A_{z}}{\partial \phi }}-{\frac {\partial A_{\phi }}{\partial z}}\right) {\hat {\boldsymbol {\rho }}}
+
\left({\frac {\partial A_{\rho }}{\partial z}}-{\frac {\partial A_{z}}{\partial \rho }}\right) {\hat {\boldsymbol {\phi }}}
+
{\frac {1}{\rho }}\left({\frac {\partial \left(\rho A_{\phi }\right)}{\partial \rho }}-{\frac {\partial A_{\rho }}{\partial \phi }}\right) {\hat {\mathbf {z} }}$$

$$\boldsymbol{\nabla}\times \mathbf{U} = 
\left({\frac {1}{s }}{\frac {\partial U_{z}}{\partial \phi }}-{\frac {\partial U_{\phi }}{\partial z}}\right) {\hat {\boldsymbol {s }}}
+
\left({\frac {\partial U_{s}}{\partial z}}-{\frac {\partial U_{z}}{\partial s}}\right) {\hat {\boldsymbol {\phi }}}
+
{\frac {1}{s}}\left({\frac {\partial \left(s U_{\phi }\right)}{\partial s}}-{\frac {\partial U_{s}}{\partial \phi }}\right) {\hat {\mathbf {z} }}$$


$$\boldsymbol{\nabla}\times \mathbf{B} = 
\left({\frac {1}{s }}{\frac {\partial B_{z}}{\partial \phi }}-{\frac {\partial B_{\phi }}{\partial z}}\right) {\hat {\boldsymbol {s }}}
+
\left({\frac {\partial B_{s}}{\partial z}}-{\frac {\partial B_{z}}{\partial s}}\right) {\hat {\boldsymbol {\phi }}}
+
{\frac {1}{s}}\left({\frac {\partial \left(s B_{\phi }\right)}{\partial s}}-{\frac {\partial B_{s}}{\partial \phi }}\right) {\hat {\mathbf {z} }}
$$

Laplacian for scalar function $f = f(\rho,\theta,\phi)$

$$
\nabla^2f =
\boldsymbol{\nabla}\cdot(\boldsymbol{\nabla}f) = 
{1 \over \rho}{\partial \over \partial \rho}\left(\rho {\partial f \over \partial \rho}\right)
+
{1 \over \rho^2}{\partial^2 f \over \partial \phi^2} + {\partial^2 f \over \partial z^2}
$$

## Spherical

$$
\mathbf{\nabla} f = 
{\partial f \over \partial r}\hat{\mathbf r}
+
{1 \over r}{\partial f \over \partial \theta}\hat{\boldsymbol \theta}
+
{1 \over r\sin\theta}{\partial f \over \partial \phi}\hat{\boldsymbol \phi}
$$

$$
\boldsymbol{\nabla}\cdot\mathbf{A} =
{1 \over r^2}{\partial \left( r^2 A_r \right) \over \partial r}
+
{1 \over r\sin\theta}{\partial \over \partial \theta} \left(  A_\theta\sin\theta \right)
+
{1 \over r\sin\theta}{\partial A_\phi \over \partial \phi}
$$

$$
\boldsymbol{\nabla}\cdot\mathbf{U} = 
{1 \over r^2}{\partial \left( r^2 U_r \right) \over \partial r}
+
{1 \over r\sin\theta}{\partial \over \partial \theta} \left(  U_\theta\sin\theta \right)
+
{1 \over r\sin\theta}{\partial U_\phi \over \partial \phi}
$$

$\displaystyle
\boldsymbol{\nabla}\times \mathbf{U} =
{\frac {1}{r\sin \theta }}\left({\frac {\partial }{\partial \theta }}\left(U_{\phi }\sin \theta \right)
-
{\frac {\partial U_{\theta }}{\partial \phi }}\right) {\hat {\mathbf {r} }}
+
{\frac {1}{r}}\left({\frac {1}{\sin \theta }}{\frac {\partial U_{r}}{\partial \phi }}
-
{\frac {\partial }{\partial r}}\left(rU_{\phi }\right)\right) {\hat {\boldsymbol {\theta }}}
+
{\frac {1}{r}}\left({\frac {\partial }{\partial r}}\left(rU_{\theta }\right)
-
{\frac {\partial U_{r}}{\partial \theta }}\right) {\hat {\boldsymbol {\phi }}}$

$\displaystyle
\boldsymbol{\nabla}\times \mathbf{A} =
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

$\displaystyle
\nabla^2f={ {1 \over r^{2}}{\partial  \over \partial r}\left(r^{2}{\partial f \over \partial r}\right)+{1 \over r^{2}\sin \theta }{\partial  \over \partial \theta }\left(\sin \theta {\partial f \over \partial \theta }\right)+{1 \over r^{2}\sin ^{2}\theta }{\partial ^{2}f \over \partial \phi ^{2}}}$$

# First--Order Approximations

For $\delta \ll 1$,

$$(1+\delta)^n \simeq 1 + n\delta$$

$$\ln(1+\delta) \simeq \delta$$

$$\cos\delta \simeq 1 - \delta^2/2$$

$$\sin\delta \simeq \delta$$

$$e^\delta \simeq 1 + \delta$$

# Other

$$e^{i\theta}=\cos\theta + i\sin\theta$$


# Equations you should know

## Undergraduate

1. Cartesian gradient, divergence, and Laplacian; how to quickly derive the curl.
2. A 1--D example problem where gradient, divergence, curl, Laplacian is used in cartesian, cylindrical, and spherical.
3. $(1+\delta)^n$ for small $\delta$; same for $\ln(1+\delta)$, $\sin(\delta)$, $\cos(\delta)$, $e^{\delta}$ (all can be derived using a Taylor series; a plot can help - e.g., $\cos\delta$ near $\delta=0$ appears to be a concave-down parabola):
   1. $(1+\delta)^n \simeq 1 + n\delta$
   2. $\ln(1+\delta) \simeq \delta$
   3. $\cos\delta \simeq 1 - \delta^2/2$
   4. $\sin\delta \simeq \delta$
   5. $e^\delta \simeq 1 + \delta$
4. $e^{i\theta}=\cos\theta + i\sin\theta$
5. Field near surface of conductor is $\sigma/2\epsilon\_0$; Field near center of and near surface of sheet of charge is $\sigma/\epsilon\_0$. Why these differ (conductor equation accounts for _all_ charges, including those on conductor; sheet equation accounts only for charges on sheet).

## Graduate

* Divergence theorem (can reason out by using know problem solution as guide)
* Stokes theorem (can reason out by using know problem solution as guide)
