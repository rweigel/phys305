Due on Thursday, October 14th at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. Use a file name of `Yourlastname_PHYS305_HW7.pdf` (one file only, please). Capitalize the first letter in your last name and use caps and underscores as indicated. **Include your name on the first sheet**.

This homework covers the [method of images](method_of_images.html) and the [monopole expansion](monopole_expansion.html). See also Griffiths 3.2 and 3.4.

# Method of Images

1. Write down the potential $V(x,y,z)$ due to a point charge $q_i$ at $z=z_i$ and $q_o$ at $z=z_o$ (assume $z_o \gt z_i$ for your diagram).

2. Show that the choices of $q_i=-q_o(R/z_o)$ and $z_i=R^2/z_o$ give $V(r=R)=0$. That is, with these choices for $q_i$ and $z_i$, this potential is zero on a sphere centered on the origin and with a radius $R$.

    Once you have found $V(x,y,z)$ due this two--charge problem, you have solved another problem: The potential due to a point charge outside of a grounded ($V=0$) conducting sphere of radius $R$ that is centered on the origin. The boundary conditions for the conductor problem is that $V$ is zero on the surface of the sphere and approaches zero as $r\rightarrow \infty$. The $V$ for the two--charge problem matches these boundary conditions and so the two--charge $V$ must be the same as the $V$ for the conductor problem.

3. **Extra Credit**: A point charge at $z=z_o$ is outside of a grounded conducting sphere that is centered on the origin and has a radius of $R$. Use your answer for $V(x,y,z)$ from 2. to find the surface charge density on the conducting sphere, which should depend only on $\theta$.

**Answer**

1\.

$\displaystyle V(x,y,z)=\frac{kq_o}{\sqrt{x^2+y^2+(z-z_o)^2}}+\frac{kq_i}{\sqrt{x^2+y^2+(z-z_i)^2}}$

or

$\displaystyle V(x,y,z)=\frac{kq_o}{\sqrt{x^2+y^2+z^2-2zz_o+z_o^2}}+\frac{kq_i}{\sqrt{x^2+y^2+z^2-2zz_i+z_i^2}}$

2\.

At $r=R$, $x^2+y^2+z^2=R^2$, so

$\displaystyle V(r=R)=\frac{kq_o}{\sqrt{R^2-2zz_o+z_o^2}}+\frac{kq_i}{\sqrt{R^2-2zz_i+z_i^2}}$

Substitution of $q_i=-q_o(R/z_o)$ and $z_i=R^2/z_o$ gives

$\displaystyle V(r=R)=\frac{kq_o}{\sqrt{R^2-2zz_o+z_o^2}}-\frac{kq_oR/z_o}{\sqrt{R^2-2zR^2/z_o+(R^2/z_o)^2}}$

The second term can be re--written by absorbing $z_o/R$ into the square root:

$\displaystyle \frac{kq_o}{\frac{z_o}{R}\sqrt{R^2-2zR^2/z_o+(R^2/z_o)^2}}=\displaystyle \frac{kq_o}{\sqrt{(\frac{z_o}{R})^2(R^2-2zR^2/z_o+(R^2/z_o)^2})}=\frac{kq_o}{\sqrt{z_o^2-2zz_o+R^2}}$

And so $V(R)=0$.

3\.

First, write $V$ in spherical coordinates using $z=r\cos\theta$ in

$\displaystyle V(r,\theta)=\frac{kq_o}{\sqrt{r^2-2zz_o+z_o^2}}+\frac{kq_i}{\sqrt{r^2-2zz_i+z_i^2}}$

Then, compute $\mathbf{E}(r,\theta)=-\mathbf{\nabla}V(r,\theta)$ using the gradient operator ($\mathbf{\nabla}$) in spherical coordinates. (A common error was not converting $z$ to spherical and treating it as a constant when computing the partials of $r$ and $\theta$.)

Then, use $\sigma(\theta)=\epsilon_o \mathbf{E}(R,\theta)\cdot\hat{\mathbf{n}}$ where $\hat{\mathbf{n}}=\hat{\mathbf{r}}$ for this problem.

Finally, use $q_i=-q_o(R/z_o)$ and $z_i=R^2/z_o$. The final result is

$\displaystyle \sigma(\theta) = kq_ou\frac{u^2-1}{\left(1+u^2-2u\cos\theta\right)^{3/2}}$

where $u\equiv R/z_o$. Note that because $u\lt 1$, $\sigma \lt 0$, as expected because the point charge draws negative charges towards it. As $u\rightarrow 0$, corresponding to $q_o$ far from the sphere, $\sigma$ approaches zero -- no negative charges are pulled from the ground onto the sphere because the field due to $q_o$ is near zero on the sphere.

# Monopole Expansion

For a point charge $q$ at $z=d$,

1. Find the exact equation for $V(z)$, the potential on the $z$ axis.

2. Use the [binomial expansion](binomial_expansion.html) and the assumption that $z\gg d$ to find a formula for $V(z)$ in the form

   $\displaystyle V(z) \simeq \frac{kq}{z}\left(1+\frac{A_1}{z} + \frac{A_2}{z^2}\right)$
   
   That is, find the coefficients $A_1$ and $A_2$. (As a check, when $d\rightarrow 0$, you should get a familiar formula.)
3. In Chapter 3.4 of Griffiths, he derives the formula

   $\displaystyle \frac{1}{\char"0509} = \frac{1}{r}\sum_{n=0}^\infty\left(\frac{r'}{r}\right)^nP_n(\cos\alpha)$

   where $\alpha$ is the angle between $\mathbf{r}$ and $\mathbf{r}'$ and $r'\lt r$. Equations for $P_n$ are given on page 142.

   Based on this, the potential due to a point charge at $\mathbf{r}'$ at any location in space where $r\gt r'$ can be written as
   
   $\displaystyle V = \frac{kq}{\char"0509} = \frac{kq}{r}\sum_{n=0}^\infty\left(\frac{r'}{r}\right)^nP_n(\cos\alpha)$
   
   Show that this formula applied to the problem of finding $V(z)$ due to a point charge $q$ at $z=d$ gives the same result for $A_1$ and $A_2$ as found in part 2. of this problem.

**Answer**

1\. $\displaystyle V(z)=\frac{kq}{|z-d|}$

2\. $A_1=d$ and $A_2=d^2$. See [Example 3.1](monopole_expansion.html).

3\. See [Example 3.1](monopole_expansion.html).

# Extra Credit

If $\mathbf{r}'=b\xhat$, find $\cos\alpha$ in cartesian coordinates, where $\alpha$ is the angle between $\mathbf{r}$ and $\mathbf{r}'$.

If $q$ is at $\mathbf{r}'=b\xhat$, find $V$ in cartesian coordinates using the first three terms of the sum in

   $\displaystyle V = \frac{kq}{r}\sum_{n=0}^\infty\left(\frac{r'}{r}\right)^nP_n(\cos\alpha)$


   