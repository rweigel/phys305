# Equations

## Cartesian

$$\boldsymbol{\nabla}\times \mathbf{A} = \left(\frac{\partial A_z }{\partial y} - \frac{\partial A_y }{\partial z} \right)\xhat +  \left(\frac{\partial A_x }{\partial z} - \frac{\partial A_z }{\partial x} \right)\yhat +  \left(\frac{\partial A_y }{\partial x} - \frac{\partial A_x }{\partial y} \right)\zhat $$


## Cylindrical

Gradient for scalar function $f = f(\rho,\theta,\phi)$
$$\nabla f = {\partial f \over \partial \rho}\hat{\boldsymbol \rho}+ {1 \over \rho}{\partial f \over \partial \phi}\hat{\boldsymbol \phi}+ {\partial f \over \partial z}\hat{\mathbf z}$$

Divergence for vector function expressed as $\mathbf{A}=A_{\rho}(\rho, \theta, \phi)\hat\boldsymbol{\rho} + A_{\theta}(\rho, \theta, \phi)\hat\boldsymbol{\theta} + A_{\phi}(\rho, \theta, \phi)\hat\boldsymbol{\phi}$

$$\boldsymbol{\nabla}\cdot\mathbf{A}={1 \over \rho}{\partial \left( \rho A_\rho  \right) \over \partial \rho}+{1 \over \rho}{\partial A_\phi \over \partial \phi}+{\partial A_z \over \partial z}$$

Curl for vector function expressed as $\mathbf{A}=A_{\rho}(\rho, \theta, \phi)\hat\boldsymbol{\rho} + A_{\theta}(\rho, \theta, \phi)\hat\boldsymbol{\theta} + A_{\phi}(\rho, \theta, \phi)\hat\boldsymbol{\phi}$

$$\boldsymbol{\nabla}\times \mathbf{A} = \left({\frac {1}{\rho }}{\frac {\partial A_{z}}{\partial \phi }}-{\frac {\partial A_{\phi }}{\partial z}}\right) {\hat {\boldsymbol {\rho }}}+\left({\frac {\partial A_{\rho }}{\partial z}}-{\frac {\partial A_{z}}{\partial \rho }}\right) {\hat {\boldsymbol {\phi }}}+{\frac {1}{\rho }}\left({\frac {\partial \left(\rho A_{\phi }\right)}{\partial \rho }}-{\frac {\partial A_{\rho }}{\partial \phi }}\right) {\hat {\mathbf {z} }}$$

Laplacian for scalar function $f = f(\rho,\theta,\phi)$
$$\boldsymbol{\nabla}\cdot(\boldsymbol{\nabla}f) = \nabla^2f={1 \over \rho}{\partial \over \partial \rho}\left(\rho {\partial f \over \partial \rho}\right) + {1 \over \rho^2}{\partial^2 f \over \partial \phi^2}+ {\partial^2 f \over \partial z^2}$$

## Spherical

$$\mathbf{\nabla} f = {\partial f \over \partial r}\hat{\mathbf r}+ {1 \over r}{\partial f \over \partial \theta}\hat{\boldsymbol \theta}+ {1 \over r\sin\theta}{\partial f \over \partial \phi}\hat{\boldsymbol \phi}$$

$$\boldsymbol{\nabla}\cdot\mathbf{A}={1 \over r^2}{\partial \left( r^2 A_r \right) \over \partial r} + {1 \over r\sin\theta}{\partial \over \partial \theta} \left(  A_\theta\sin\theta \right) + {1 \over r\sin\theta}{\partial A_\phi \over \partial \phi}$$

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

$$\nabla^2f={ {1 \over r^{2}}{\partial  \over \partial r}\left(r^{2}{\partial f \over \partial r}\right)+{1 \over r^{2}\sin \theta }{\partial  \over \partial \theta }\left(\sin \theta {\partial f \over \partial \theta }\right)+{1 \over r^{2}\sin ^{2}\theta }{\partial ^{2}f \over \partial \phi ^{2}}}$$

# Equations you should know

## Undergraduate

1. Gradient, divergence, and Laplacian; how to quickly derive the curl.
2. An example problem where gradient, divergence, curl, Laplacian is used in cartesian, cylindrical, and spherical.
3. $(1+\delta)^n$ for small $\delta$; same for $\ln(1+\delta)$, $\sin(\delta)$, $\cos(\delta)$, $e^{\delta}$ (all can be derived using a Taylor series; a plot can help - e.g., $\cos\delta$ near $\delta=0$ appears to be a concave-down parabola):
   1. $(1+\delta)^n \simeq 1 + n\delta$
   2. $\ln(1+\delta) \simeq \delta$
   3. $\cos\delta \simeq 1 - \delta^2/2$
   4. $\sin\delta \simeq \delta$
   5. $e^\delta \simeq 1 + \delta$
4. $e^{i\theta}=\cos\theta + i\sin\theta$
5. Field near surface of conductor is $\sigma/2\epsilon\_0$; Field near center of and near surface of sheet of charge is $\sigma/\epsilon\_0$. Why these differ (conductor equation accounts for _all_ charges, including those on conductor; sheet equation accounts only for charges on sheet).

## Graduate

* \((1+\delta)^n\) to first order in \(\delta\); same for \(\ln(1+\delta)\), \(\sin(\delta)\), \(\cos(\delta)\), \(e^{\delta}\)
* \(e^{i\theta}=\cos\theta + i\sin\theta\) and how to get formulas from \(\sinh x\) and \(\cosh x\) from it. How to derive trig identities using it.
* Radial component of \(\nabla^2f\) in cylindrical and spherical (can reason out by using know problem solution as guide)
* Radial component of \(\boldsymbol{\nabla}\boldsymbol{\cdot}\mathbf{A}\)
* Divergence theorem (can reason out by using know problem solution as guide)
* Stokes theorem (can reason out by using know problem solution as guide)
