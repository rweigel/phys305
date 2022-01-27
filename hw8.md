Due on Thursday, October 28th at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. Use a file name of `Yourlastname_PHYS305_HW8.pdf` (one file only, please). Capitalize the first letter in your last name and use caps and underscores as indicated. **Include your name on the first sheet**.

The is HW covers [monopole expansion](monopole_expansion.html) (Griffiths 3.4) and polarization (Griffiths 4.1--4.2).

# Perfect Dipole on $x$--axis

% Copied to notes

In class, I showed how one can use the equation

$\displaystyle V = \frac{kq}{\char"0509} = \frac{kq}{r}\sum_{n=0}^\infty\left(\frac{r'}{r}\right)^nP_n(\cos\alpha)$

to find an approximation for $V(\mathbf{r})$ for charges $\pm q$ at $z=\pm d/2$ and keeping only the $n=0$ and $n=1$ terms. I then showed how the equation

$\displaystyle V(\mathbf{r})=k\frac{\mathbf{p}\bfcdot\hat{\mathbf{r}}}{r^2}$

gives the same result.

1\. Follow the procedure used in class to find $V(\mathbf{r})$ for charges $\pm q$ at $x=\pm d/2$ using the $n=0$ and $n=1$ terms of

$\displaystyle V = \frac{kq}{\char"0509} = \frac{kq}{r}\sum_{n=0}^\infty\left(\frac{r'}{r}\right)^nP_n(\cos\alpha)$

and also

$\displaystyle V(\mathbf{r})=k\frac{\mathbf{p}\bfcdot\hat{\mathbf{r}}}{r^2}$

2\. Find $\mathbf{E}$ with spherical coordinates and unit vectors using the $V(\mathbf{r})$ that you computed in part 1.

**Answer**

1\.

$\displaystyle V\_+=\frac{kq}{r}\left[1+\frac{r'\_+}{r}\cos\alpha\_+ + ...\right]$

$\displaystyle V\_-=\frac{kq}{r}\left[1+\frac{r'\_-}{r}\cos\alpha\_- + ...\right]$

In this problem, $\alpha_+$, the angle between $\mathbf{r}$ and $\mathbf{r}'_+$ is not simply the polar angle $\theta$ in spherical coordinates. It can be computed from the definition of the dot product:

$\displaystyle \cos\alpha\_+=\frac{\mathbf{r}\bfcdot\mathbf{r}'\_+}{r'
_+ r}$

Using $\mathbf{r}'\_+=(d/2)\xhat$ and $\mathbf{r}=x\xhat + y\yhat + z\zhat$ gives

$\displaystyle \cos\alpha\_+=\frac{x}{r}$

which can be written in spherical coordinates using $x=r\sin\theta\cos\phi$ (you should know this formula or be able to derive it from a diagram). Then,

$\displaystyle \cos\alpha\_+=\sin\theta\cos\phi$

Checks: For $\theta=0$ and $\phi=0$, this gives $\alpha\_+=0$ as expected. For $\theta=90^\circ$ and $\phi=0$, this gives $\alpha\_+=90^\circ$ as expected.

Similar calculation (or using $\pi =\alpha\_+ + \alpha_\-$, which applies to this problem but not in general) gives

$\displaystyle \cos\alpha\_-=-\sin\theta\cos\phi$

Finally, using $V=V\_+ + V\_-$, we get

$\displaystyle V = \frac{kqd}{r^2}\sin\theta\cos\phi$

To compute the potential using

$\displaystyle V(\mathbf{r})=k\frac{\mathbf{p}\bfcdot\hat{\mathbf{r}}}{r^2}$

use $\mathbf{p}=q(\mathbf{r}'\_+-\mathbf{r}'\_-)=qd\xhat$ and $\hat{\mathbf{r}}=(x\xhat + y\yhat + z\zhat)/r$

2\.

Use

$\displaystyle V(r,\theta) = \frac{kqd}{r^2}\sin\theta\cos\phi$ and $\mathbf{E}=-\mathbf{\nabla}V$ with $\mathbf{\nabla}$ in spherical coordinates. This requires evaluation of the partials in

$\displaystyle \mathbf{E}(r,\theta)=-{\partial V \over \partial r}\hat{\mathbf r} - {1 \over r}{\partial V \over \partial \theta}\hat{\boldsymbol \theta} - {1 \over r\sin\theta}{\partial V \over \partial \phi}\hat{\boldsymbol \phi}$

$\displaystyle \mathbf{E}(r,\theta) = \frac{kqd}{r^3}(2\sin\theta\cos\phi\hat{\mathbf{r}}-\cos\theta\cos\phi\hat{\boldsymbol{\theta}}+\sin\phi\hat{\boldsymbol{\phi}})$

Checks: For $\phi=0$ and $\theta=\pi/2$, expect field to be in $+\hat{\mathbf{r}}$ direction. For $\phi=\pi/2$ and $\theta=\pi/2$, expect $+\hat{\boldsymbol{\phi}}$. For $\phi=\pi$ and $\theta=\pi/2$, expect $-\hat{\mathbf{r}}$.

Note that an alternative approach to solving both 1. and 2. problem is to take the solution for the dipole along the $z$ axis and rotate the coordinate system around the $y$--axis.

# Slab of Charge

% Copied to notes

In 4.2 of Griffiths, he models a polarized sphere by using two uniformly charged spheres with centers that are separated by a small distance $d$. One sphere has a postive charge and the other a negative charge. He then computes the electric field in the overlap region and in the region outside of both spheres where there is no overlap.

In this problem, a polarized slab will be modeled by using two slabs of charge with uniform and opposite charge density that are displaced by a small distance $d$.

1. Find $\mathbf{E}(y)$ for the slab with uniform charge density $\rho_o$ shown in the following figure. Assume that the slab is infinite in extent in the $\pm z$ and $\pm x$ directions so that Gauss's law can be used. (This slab can be thought of as being composed of thin sheets of charge stacked together and so an alternative to using Gauss's law is to sum the electric field due to sheets of charge.)

   <img src="figures/Gausss_Law_Uniform_Slab.svg"/>

2. Plot $\mathbf{E}(y)$ vs $y$.

3. Next, compute and plot $\mathbf{E}(y)$ for the same slab if it had charge density of $-\rho_o$ and was shifted by $-d$ in the $y$--direction. Assume that $d\ll t$.

4. Compute $\mathbf{E}$ in the region of overlap of the $+\rho_o$ and $-\rho_o$ slabs.

**Answer**

Details on how to solve this problem were given in class and so only a summary is given here.

1\. Gauss's law can be used to find the field for $|y|\ge t/2$ (a cylinder centered on the origin or with its bottom cap at $y=0$ can both be used). This gives $E\_y=\pm \rho_o t/2\epsilon_o$, where the $+$ corresponds to above the slab. Inside the slab, we know $E=0$ at $y=0$ because the field due to the upper part of the slab cancels that due to the lower part. We also expect that inside the slab, $E\_y(y)$ field will increase linearly. From this, we can write $E\_y(y)=\rho_o y/\epsilon_o$. This equation gives zero at the origin and matches the outer field at $y=\pm t/2$. Alternatively, we can also use Gauss's law. For a cylinder centered on the origin and height $2y$, the charge enclosed is $\rho_o 2y$.

2\.

3\. Invert the plot from 2. and then translate it by $d$ in the $y$ direction. Inside the negatively charged slab, the field will be $E\_y(y)=-\rho_o (y+d)/\epsilon_o$. (This gives $E_y=0$ when $y=-d$, corresponding to the center of the negatively charged slab.)

4\. In the region of overlap we need to sum

$E\_y(y) = E^+\_y(y) + E^-\_y(y)$

Using $E^+\_y(y)=\rho_o y/\epsilon_o$ and $E^-\_y(y)=-\rho_o (y+d)/\epsilon_o$ gives

$E\_y(y) = -\rho_od/\epsilon_o$

This is the same field one would get if we had a positive sheet of charge at $y=t/2$ and a negative sheet at $y=-t/2$ if the sheets had a charge density of $\rho_o d$. If one draws the charge density when the two slabs are superimposed, the system appears to be two such sheets of charge.
