# Biot-Savart for Straight Wire

1. Find $\mathbf{B}$ at the origin due to the rectangular current loop shown in the following figure. (The loop is centered on the origin.)
2. If $a$ is increased while $b$ is fixed, such that $a\gg b$, we expect the field at the origin to be approximately the field due to infinitely long wires at $y=b/2$ and $y=-b/2$. Compute $\mathbf{B}$ at the origin using this assumption. You may do this by taking your answer from 1. and applying the limit $a\gg b$ or by simply using the formula for the field due to a long straight wire in introductory textbooks.

<img src="figures/Lorentz_Force_Law_Rectangular_Loop.svg"/>

**Answer**

1\. Griffiths gives the equation $B=\frac{\mu_o I}{4\pi s}(\sin\theta_2-\sin\theta_1)$. This equation can be applied to the given problem. For the bottom wire, the initial angle is $\sin\theta_1=a/\sqrt{a^2+b^2}$ and the final angle is $\sin\theta_2=-a/\sqrt{a^2+b^2}$. Therefore,

Bottom: $\displaystyle B_z=\frac{\mu_o I}{4\pi (b/2)}\frac{-2a}{\sqrt{a^2+b^2}}=-\frac{\mu_o I}{\pi b}\frac{a}{\sqrt{a^2+b^2}}$ 

The top wire contributes the same field as the bottom, so.

Top: $\displaystyle B_z=-\frac{\mu_o I}{\pi b}\frac{a}{\sqrt{a^2+b^2}}$ 

The field for the left and right wire can be found by swapping $a$ and $b$ in the above equation.

Left: $\displaystyle B_z=-\frac{\mu_o I}{\pi a}\frac{b}{\sqrt{a^2+b^2}}$ 

Right: $\displaystyle B_z=-\frac{\mu_o I}{\pi a}\frac{b}{\sqrt{a^2+b^2}}$ 

Griffiths' solution uses a short--cut that applies to this particular problem. In class, I encouraged you to solve this problem using the more general method, which is as follows.

$\mathbf{r}=\mathbf{0}$

$\mathbf{r}'=x'\xhat + y'\yhat=x'\xhat -(b/2)\yhat$

$d\mathbf{l}' = -dx'\xhat$

Substitution of the above into

$\displaystyle \mathbf{B}(\mathbf{r}) = \frac{\mu_0I}{4\pi}\int\frac{d\mathbf{l}'\times (\mathbf{r} - \mathbf{r}')}{|\mathbf{r} - \mathbf{r}'|^3}$

Gives

$\displaystyle \mathbf{B} = \frac{\mu_0I}{4\pi}\int\frac{-dx'\xhat\times (-x'\xhat + (b/2)\yhat)}{\left(x'^2 + (b/2)^2\right)^{3/2}}$

After evaluating the cross products, we are left with

$\displaystyle \mathbf{B} = -\zhat\frac{\mu_o}{4\pi}\frac{Ib}{2}\int_{-a/2}^{a/2}\frac{dx'}{\left(x'^2 + (b/2)^2\right)^{3/2}}$

Let $x'=(b/2)\tan u$, then $dx'=b du/2\cos^2u$ and the integrand is

$\displaystyle\frac{\left(\frac{b}{2}\right)\frac{du}{\cos^2u}}{\left(\frac{b}{2}\right)^3(\tan^2u+1)^{3/2}}$

Dividing $\sin^2u+\cos^2u=1$ by $\cos^2u$ gives $\tan^2u+1=1/\cos^2u$, so the integrand can be written

$\displaystyle\frac{\left(\frac{b}{2}\right)\frac{du}{\cos^2u}}{\left(\frac{b}{2}\right)^3|1/\cos u|^3}=\left(\frac{2}{b}\right)^2|\cos u|du$

The limits of integration are from $u_o=\tan^{-1}(-a/b)$ to $u_f=\tan^{-1}(a/b)$

$\displaystyle \mathbf{B} = -\zhat\frac{\mu_o}{4\pi}\frac{I2}{b}\int_{u_o}^{u_f}|\cos u|du$

Within these limits of integration, $\cos u$ is positive<sup>\*</sup>, so we can drop the absolute value and integrate. (<sup>\*</sup>this requires some thought and a diagram to show.)

$\displaystyle \mathbf{B} = -\zhat\frac{\mu_o}{4\pi}\frac{I2}{b}(\sin u_f-\sin u_o)$

If $u_o=\tan^{-1}(-a/b)$, then $\tan u_o=-a/b$. This corresponds to a right triangle in the fourth quadrant with sides of $a$ and $b$, which has a hypotenuse of $\sqrt{a^2+b^2}$ and for which $\sin u_o = -a/\sqrt{a^2+b^2}$. Similarly, $\sin u_f = a/\sqrt{a^2+b^2}$. Substitution gives

$\displaystyle \mathbf{B} = -\zhat\frac{\mu_oI}{b}\frac{a}{\sqrt{a^2+b^2}}$

2\. For an infinite wire, $B=\mu_o I/2\pi s$, where $s$ is the perpendicular distance from the wire; the magnitude is determined from the right--hand rule. The top and bottom wires will create a field with this magnitude in the $-\zhat$ direction (from the right-hand rule). For both wires, the perpendicular distance is $b/2$. Therefore, $B_z=-2\mu_o I/\pi b$.

The field from the top and bottom wires from part 1. is

$\displaystyle B_z=-\frac{2\mu_o I}{\pi b}\frac{a}{\sqrt{a^2+b^2}}$

Factoring out $a$ gives

$\displaystyle B_z=-\frac{2\mu_o I}{\pi b}\frac{1}{\sqrt{1+b^2/a^2}}$

For $b \lt a$, we can expand

$\displaystyle B_z = -\frac{2\mu_o I}{\pi b}\left(1-\frac{1}{2}\frac{b^2}{a^2}+...\right)$

For $a\gg b$,

$\displaystyle B_z \simeq -\frac{2\mu_o I}{\pi b}$

# Biot-Savart for Curved Wire

A segment of a closed current loop is shown in the following figure. Compute the magnetic field at the center of the semi--circle due to the straight and curved segments shown.

<img src="figures/Lorentz_Force_Law_Hemisphere.svg"/>

(Technically, to use the Biot--Savart law for currents in a wire, the current must be constant, and the wire must form a closed loop. As a result, there will be a contribution to the magnetic field at the origin due to the parts of the closed loop that are not shown. However, here we assume that the not--shown part of the loop is far enough away that they can be neglected.)

**Answer**

For the magnitude, one can use 1/2 of equation 5.41 of Griffiths with $z=0$. The direction can be determined from the right-hand rule. (Equation 5.41 is for a circular loop offset in the $z$ direction.)

If the origin is the center of the circle, $x$ is up, and $y$ is to the right, then $\mathbf{I}=I\hat{\boldsymbol{\phi}}$, $dl'=Rd\phi'$, $\mathbf{r}=\mathbf{0}$, and $\mathbf{r}'=R\hat{\mathbf{s}}$. Substitution of these into

$\displaystyle \mathbf{B}(\mathbf{r}) = \frac{\mu_0}{4\pi}\int dl'\frac{\mathbf{I}\times (\mathbf{r} - \mathbf{r}')}{|\mathbf{r} - \mathbf{r}'|^3}$

gives

$\displaystyle \mathbf{B}=\frac{\mu_o}{4\pi}\int_{-\pi/2}^{\pi/2}Rd\phi' \frac{\hat{\boldsymbol{\phi}}\times (-R\hat{\mathbf{s}})}{R^3}=\zhat\frac{\mu_o}{4\pi}\frac{1}{R}\int_{-\pi/2}^{\pi/2}d\phi'=\frac{\mu_oI}{4R}\zhat$

# Follow--up

Find $\mathbf{B}(z)$ for the previous problem, where the $z$--axis passes through the center of the semi--circle and is perpendicular to the page. Assume positive $z$ is out of the page.

**Comments**

The contributions from the straight segments can be found using 

$\displaystyle B=\frac{\mu_o I}{4\pi s}(\sin\theta_2-\sin\theta_1)$

and a diagram to determine $\theta_1$ and $\theta_2$.

The contribution from the semi--circle can be found using 1/2 of equation 5.41 of Griffiths.

# Square Current Loop

Use equation 5.35 Griffiths 3rd edition to find the magnetic field at $(x,y)=(a,a/2)$ due to a square current loop carrying a current $I$ with corners at $(x,y)=(0,0),(0,2a),(2a,2a),(2a,0)$.

Write your answer in a form that does not require the use of a calculator that can calculate trigonometric functions. That is, the numbers in your solution, besides $\pi$ and $\mu_o$, should be whole numbers or square roots of whole numbers.

# Wire Segment

A segment of wire carrying a current $I\hat{\mathbf{y}}$ extends from $y=-a$ to $y=a$.

Consider the magnetic field that this current produces in the $y$-$z$ plane, $\mathbf{B}(y,z)$.

1. What is general direction $\mathbf{B}$ at $(y,z)=(-a,a)$? Sketch the wire and the magnetic field vector.
2. What is general direction $\mathbf{B}$ at $(y,z)=(a,a)$? Sketch the wire and the magnetic field vector.
3. Explain why the direction of the magnetic field is in the $\hat{\mathbf{x}}$ direction only on the $z$-axis.

# Wire Segment

A segment of wire carrying a current $I\hat{\mathbf{y}}$ extends from $y=-a$ to $y=a$.

Show that the integral that needs to be solved is

$$\mathbf{B}(z)=\frac{\mu_0Iz}{4\pi}\mathbf{\hat{x}}\int_{-a}^{a}\frac{dy'}{(z^2+y'^2)^{3/2}}$$

Evaluate this integral and show how it gives

$$\mathbf{B}(z)=\frac{\mu_0I}{2\pi z}\mathbf{\hat{x}}$$

for $z/a<<1$.

**Answer**

$$\mathbf{r}=z\hat{\mathbf{z}}$$
$$\mathbf{r}'=y'\hat{\mathbf{y}}$$
$$d\mathbf{l}' = dy'\hat{\mathbf{y}}$$

$$\mathbf{B}(\mathbf{r}) = \frac{\mu_0I}{4\pi}\int\frac{d\mathbf{l}'\times (\mathbf{r} - \mathbf{r}')}{|\mathbf{r} - \mathbf{r}'|^3}$$

$$\mathbf{B}(\mathbf{r}) = \frac{\mu_0I}{4\pi}\int\frac{dy'\hat{\mathbf{y}}\times (z\hat{\mathbf{z}} - y'\hat{\mathbf{y}})}{(y^2+z^2)^{3/2}}$$

$$\mathbf{B}(z)=\frac{\mu_0Iz}{4\pi}\mathbf{\hat{x}}\int_{-a}^{a}\frac{dy'}{(z^2+y'^2)^{3/2}}$$

$$\int_{-a}^{a}\frac{dy'}{(z^2+y'^2)^{3/2}}=\frac{y}{z^2\sqrt{y^2+z^2}}\Bigm|_{-a}^a=\frac{2a}{z^2\sqrt{a^2+z^2}}=\frac{2}{z^2}\frac{1}{\sqrt{1+(a/z)^2}}$$

$$\mathbf{B}(z)=\mathbf{\hat{x}}\frac{\mu_0I}{2\pi z}\frac{1}{\sqrt{1+(a/z)^2}}$$

for $a/z \ll 1$, this can be approximated as

$$\mathbf{B}(z)\simeq\mathbf{\hat{x}}\frac{\mu_0I}{2\pi z}\left(1-2(a/z)^2\right)$$

so as $a/z\rightarrow 0$, the equation becomes that for an infinite wire.

# Wire Segment

1. Compute the magnetic field on the $x$-axis (that is, compute $\mathbf{B}(x)$) due to an infinite straight wire carrying a current that lies along the line $y=x$, $\mathbf{I}=I_o(\hat{\mathbf{x}}+\hat{\mathbf{y}})/\sqrt{2}$.

2. Compute the magnetic field on the $x$-axis (that is, compute $\mathbf{B}(x)$) due to wire carrying a current that lies along the line $y=x$, $\mathbf{I}=I_o(\hat{\mathbf{x}}+\hat{\mathbf{y}})/\sqrt{2}$ that extends from $(x,y)=(-a,a)$ to $(x,y)=(a,a)$.

Show that the computed magnetic field $\mathbf{B}(x)$ matches that from the previous question in the limit that $x/a\ll 1$.

# Circular Current Loop

A loop of radius $a$ lies in the $x$-$y$ plane and is centered on the origin. 

## On Axis

Find $B_z(z)$ following the method covered in class in which one writes down equations for $d\mathbf{l}', \mathbf{r}$, and $\mathbf{r}'$ and then evaluates the Biot-Savart formula

$$\mathbf{B}(\mathbf{r}) = \frac{\mu_0I}{4\pi}\int\frac{d\mathbf{l}'\times (\mathbf{r} - \mathbf{r}')}{|\mathbf{r} - \mathbf{r}'|^3}$$

In addition, make sure that you understand how this version of the Biot-Savart formula is related to equation 5.32 of Griffiths, which has a unit vector in the numerator.

The solution to this problem is given in example 5.6 of Griffiths in which a different method is used.

## Off Axis 

1. Write the integrals that must be solved to find each of the components of $\mathbf{B}$ at a point in the $y$-$z$ plane (for a loop of radius $a$ that lies in the x-y plane and is centered on the origin.)

2. Evaluate the integral for $B_x$ and explain why it was expected to be zero.

3. The integrals for $B_y$ and $B_z$ do not have an analytic solution. If we assume $a^2 << y^2+z^2$, they can be simplified to a form that is easy to integrate.  Show that

$$\frac{1}{(y^2+z^2-2ay\sin\phi+a^2)^{3/2}}$$

can be written as

$$\frac{1}{r^{3}}\frac{1}{(1-2\sin\phi (y/r)\delta+\delta^2)^{3/2}}$$

where $r^2=y^2+z^2$ and $\delta = a/r$.

Use the fact that $1/(1+\Delta)^{3/2}\simeq 1 - 3\Delta/2$ (from the Taylor series approximation) for $\Delta << 1$ and the assumption that $a^2 << y^2+z^2$ to write the integrals for $B_y$ and $B_z$ in a form that can be integrated and then evaluate the integrals.

If you would like to check your answer, note that in this approximation you are computing the magnetic field due to a magnetic dipole.

4. What is $\mathbf{B}$ in the $x$-$z$ plane due to a current loop assuming the magnetic field was measured far away from the origin? (Hint: Re-use your solution to 1.)

5. Show that your equation for $\mathbf{B}$ in the $y$-$z$ plane is consistent with Figure 5.55a of Griffiths 3rd edition given below (identify 3 features in the figure and show that your equations have these features; for example, one feature is that the magnetic field is in the $z$-direction for $y=0$.).

6. Show that your computed magnetic field in cartesian coordinates is consistent with the magnetic field due to a magnetic dipole:

$$\mathbf{B}=\frac{\mu_0}{4\pi}\frac{m}{r^3}\left(2\cos\theta\hat{r}+\sin\theta\hat{\theta}\right)$$

by either converting this equation to cartesian or by converting your cartesian equation to spherical.

[[Image:Dipole.png|500px]]

**Answer**

$$\mathbf{r}=y\hat{\mathbf{y}}+z\hat{\mathbf{z}}$$
$$\mathbf{r}'=a\cos\phi\hat{\mathbf{x}}+a\sin\phi\hat{\mathbf{y}}$$
$$d\mathbf{l} = ad\phi\hat{\phi} = ad\phi(-\sin\phi\hat{\mathbf{x}}+\cos\phi\hat{\mathbf{y}})$$

1.

The integrals that need to be solved are

$$B_x=\frac{\mu_0Iaz}{4\pi}\int_0^{2\pi}\frac{1}{r^{3}}\frac{\cos\phi\,d\phi}{(1-2\sin\phi (y/r)\delta+\delta^2)^{3/2}}$$

$$B_y=\frac{\mu_0Iaz}{4\pi}\int_0^{2\pi}\frac{1}{r^{3}}\frac{\sin\phi\,d\phi}{(1-2\sin\phi (y/r)\delta+\delta^2)^{3/2}}$$

$$B_z=\frac{\mu_0Ia}{4\pi}\int_0^{2\pi}\frac{1}{r^{3}}\frac{(a-y\sin\phi)d\phi}{(1-2\sin\phi (y/r)\delta+\delta^2)^{3/2}}$$

2.

The $B_x$ integral evaluates to zero, which is expected based on the configuration of the loop. The other two are [https://en.wikipedia.org/wiki/Elliptic_integral elliptic integrals], which cannot be written in terms of [https://en.wikipedia.org/wiki/Elementary_function elementary functions].

Using the approximation, the integration needed is now

3.

$$B_y=\frac{\mu_0Iaz}{4\pi}\frac{1}{r^{3}}\int_0^{2\pi}d\phi\left(\sin\phi\right)\left(1+3\sin\phi (y/r)\delta\right)$$

$$B_z=\frac{\mu_0Ia}{4\pi}\frac{1}{r^{3}}\int_0^{2\pi}d\phi\left(a-y\sin\phi\right)\left(1+3\sin\phi (y/r)\delta\right)$$

$$B_y=\frac{\mu_0Iaz}{4\pi}\frac{1}{r^{3}} 3\pi (y/r)\delta = \frac{\mu_0I \pi a^2}{4\pi}\frac{3yz}{r^{5}}$$

$$B_z=\frac{\mu_0I\pi a^2}{4\pi}\frac{2z^2-y^2}{r^{5}}$$

Note that the $\delta^2$ term was omitted as it is much smaller than $\delta$.

4.

To solve for $\mathbf{B}$ in the (\x$-$z$ plane, note that a dipole is symmetric with respect to rotation about the $z$-axis. So to compute the field in the (\x$-$z$ plane, replace $y$ with $x$ in the equations above.

5.

* For $z=0$, field decreases as $|y|$ increases. Equations for this case are

$$B_y=\frac{\mu_0I \pi a^2}{4\pi}\frac{3y0}{r^{5}}=0$$

So field in y-direction is always zero.

$$B_z=\frac{\mu_0I\pi a^2}{4\pi}\frac{0^2-y^2}{r^5}=-\frac{\mu_0I\pi a^2}{4\pi}\frac{1}{|y|^3}$$

Absolute value because $r=\sqrt{x^2+y^2+z^2}=|y|$. So magnitude of $\mathbf{B}$ decreases with increasing $y$.

* For $z=0$, field in $-z$ direction for any value of $y$.

See the previous answer where it was shown $B_y=0$ and $B_z$ is always negative.

* For $y=0$, field is positive and in $z$-direction for any value of z.

$$B_y=\frac{\mu_0I \pi a^2}{4\pi}\frac{30z}{r^{5}}=0$$

$$B_z=\frac{\mu_0I\pi a^2}{4\pi}\frac{2z^2}{r^{5}}=\frac{\mu_0I\pi a^2}{4\pi}\frac{2}{|z|^3}$$

So y-component is zero and z-component is always positive.

6.

$$\mathbf{B}=\frac{\mu_0}{4\pi}\frac{m}{r^3}\left(2\cos\theta\hat{r}+\sin\theta\hat{\theta}\right)$$

To convert from spherical to cartesian, use

$$r=sqrt{x^2+y^2+z^2}$$

$$\cos\theta=z/r$$

$$\sin\theta=\sqrt{x^2+y^2}/r$$ 

$$\hat{\mathbf{r}}=\sin \theta\cos \varphi \hat{\mathbf{x}} + \sin\theta \sin\varphi \hat{\mathbf{y}}+\cos\theta\hat{\mathbf{z}}$$

$$\hat{\theta}=\cos\theta\cos\phi\hat{\mathbf{x}}+\cos\theta\sin\phi\hat{\mathbf{y}}-\sin\theta\hat{\mathbf{z}}$$

where

$$\cos\phi=x/\sqrt{x^2+y^2}$$

$$\sin\phi=y/\sqrt{x^2+y^2}$$

You should be able to derive all of these using a diagram (except possibly $\hat{\theta}$).
