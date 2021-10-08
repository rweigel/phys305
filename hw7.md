Due on Thursday, October 14th at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. Use a file name of `Yourlastname_PHYS305_HW7.pdf` (one file only, please). Capitalize the first letter in your last name and use caps and underscores as indicated. **Include your name on the first sheet**.

This homework covers the method of images and the monopole expansion. See also Griffiths 3.2 and 3.4.

# Method of Images

1. Write down the potential $V(x,y,z)$ due to a point charge $q_i$ at $z=z_i$ and $q_o$ at $z=z_o$ (assume $z_o \gt z_i$ for your diagram).

2. Show that the choices of $q_i=-q_o(R/z_o)$ and $z_i=R^2/z_o$ give $V(r=R)=0$. That is, with these choices for $q_i$ and $z_i$, this potential is zero on a sphere centered on the origin and with a radius $R$.

    Once you have found $V(x,y,z)$ due this two--charge problem, you have solved another problem: The potential due to a point charge outside of a grounded ($V=0$) conducting sphere of radius $R$ that is centered on the origin. The boundary conditions for the conductor problem is that $V$ is zero on the surface of the sphere and approaches zero as $r\rightarrow \infty$. The $V$ for the two--charge problem matches these boundary conditions and so the two--charge $V$ must be the same as the $V$ for the conductor problem.

3. **Extra Credit**: A point charge at $z=z_o$ is outside of a grounded conducting sphere that is centered on the origin and has a radius of $R$. Use your answer for $V(x,y,z)$ from 2. to find the surface charge density on the conducting sphere, which should depend only on $\theta$.

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

# Extra Credit

If $\mathbf{r}'=b\xhat$, find $\cos\alpha$ in cartesian coordinates, where $\alpha$ is the angle between $\mathbf{r}$ and $\mathbf{r}'$.

If $q$ is at $\mathbf{r}'=b\xhat$, find $V$ in cartesian coordinates using the first three terms of the sum in

   $\displaystyle V = \frac{kq}{r}\sum_{n=0}^\infty\left(\frac{r'}{r}\right)^nP_n(\cos\alpha)$


   