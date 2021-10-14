Due on Thursday, October 7th at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. Use a file name of `Yourlastname_PHYS305_HW6.pdf` (one file only, please). Capitalize the first letter in your last name and use caps and underscores as indicated. **Include your name on the first sheet**.

This homework covers [Boundary Value Problems](boundary_value_problems.html). See also the sections of Griffiths referenced in these notes.

# Integrals

1. Show that $\displaystyle\int_0^\pi \sin 2x \sin x dx$ = 0. (Note that without any calculation, this is expected from a plot of $\sin x$ and $\sin 2x$ and thinking about the area under the curve for their product.)

2. Show that $\displaystyle \int_0^\pi \sin nx \sin lx dx$ = 0 for integer $n$ and $l$ if $l\ne n$ by explicitly evaluating the integral.

3. Compute $\displaystyle\int_0^\pi \sin^2 nx dx$ for
   1. any $n\ne 0$ and
   2. for integer $n$.

**Answer**

1\. There are two ways to approach this.
1. Use trig identity $2\sin(nx)\sin(lx)=\cos(nx-lx)+\cos(nx+lx)$ and integrate. Note that this identity can be derived by writing $\sin$ in terms of complex exponentials, multiplying, and then re-writing the resulting four complex exponential terms in terms of $\sin$ and $\cos$.

   $\displaystyle I=\frac{1}{2}\left[\frac{\sin((n-l)x)}{n-l}+\frac{\sin((n+l)x)}{n+l}\right]_0^\pi=0$ because $n-l$ and $n+l$ are integer and $\sin m\pi=0$ for integer $m$. 

2. Using symmetry by defining $u=x-\pi/2$ so that we need to integrate $\int_{-\pi/2}^{\pi/2} \sin(2u+\pi)\sin(u+\pi/2)$. The first term is an even function on the integration interval. The second term is odd. The integral of the product of an even and odd function is zero.

2\. The result follows from the integration used in part 1. of this answer.

3\. Using the trig identity $2\sin(nx)\sin(lx)=\cos(nx-lx)+\cos(nx+lx)$ with $l=n$, we have $2\sin^2(nx)=1+\cos(2nx)$ and so
1. $I=\frac{1}{2}\left[x + \frac{\sin(2nx)}{2n}\right]_0^\pi=\frac{\pi}{2}+\frac{\sin(2n\pi)}{2n}$
2. $I=\frac{\pi}{2}$ because $\sin(m\pi)$ is zero for integer $m$ and $2n$ is integer.

# &nbsp;2-D Boundary Value Problem

In class, I started the problem of finding the potential $V(x,y)$ inside of a long square duct with boundary conditions

1. $V(0,y) = 0$ (left)
1. $V(a,y) = 0$ (right)
1. $V(x,0) = 0$ (bottom)
1. $V(x,a) = V_o$ (top)

<img src="figures/Boundary_Value_Problems_2D_Square_Top.svg"/>

Finish this problem. That is, find the coefficients $C_n$ in the equation

$\displaystyle V(x,y)=\sum_{n=0}^\infty C_n \sin \left(\frac{n\pi}{a} x \right)\sinh \left(\frac{n\pi}{a} y\right)$

I recommend that you do the full problem, but you may start the problem by beginning with the equation that I ended with after addressing the third boundary condition.

**Answer**

$\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty \sin(n\pi x/a)\frac{\sinh(n\pi y/a)}{\sinh(n\pi)}$

# &nbsp;2-D Boundary Value Problem

Find the potential $V(x,y)$ inside of a long rectangular duct, $0 \le x\le b$; $0 \le y\le a$, with boundary conditions

1. $V(0,y) = V_o$ (left)
1. $V(b,y) = 0$ (right)
1. $V(x,0) = 0$ (bottom)
1. $V(x,a) = 0$ (top)

<img src="figures/Boundary_Value_Problems_2D_Left.svg"/>

Note that this is a rectangular duct, so your solution should have an $a$ and $b$.

Do this by following the steps that I used in class, which are also in the notes.

**Answer**

$\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\left(\cosh(n\pi x/a)-\frac{\sinh(n\pi x/a)}{\tanh(n\pi b/a)}\right)\sin(n\pi y/a)$

This can be simplified to

$\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b-x)/a]}{\sinh(n\pi b/a)}\right)\sin(n\pi y/a)$

_Short--cut solution_

One could have started assuming an equation of the form

$V(x,y) = A\sinh(mx-B)[C\sin(mx)+D\cos(mx)]$

which can be shown to be related to any of the four forms that were given in the noted. BCs 3. and 4. give $D=0$ and $m=n\pi/a$, leaving

$V(x,y) = AC\sinh(n\pi x/a-B)[\sin(n\pi y/a)]$

To satisfy BC 2., one needs $\sinh(n\pi x/a-B)=0$, so $B=n\pi b/a$ and replacing $AC$ with $C$

$V(x,y) = C\sinh(n\pi(x-b)/a)[\sin(n\pi y/a)]$

To satisfiy BC 2., we use

$V(0,y) = C_1\sinh(-\pi b/a)\sin(\pi y/a)+C_2\sinh(-2\pi b/a)\sin(2\pi y/a)+...$

and Fourier's trick as usual. In this case, we arrive at the simplified form given above.

# Extra Credit 1.

Show that your answer to the previous problem is consistent with the solution for Griffiths Example 3.3 in the limit that $a/b\rightarrow 0$.

# Extra Credit 2.

In problem 2., you will find the $C_n$s in

$\displaystyle V(x,y)=\sum_{n=0}^\infty C_n \sin \left(\frac{n\pi}{a} x \right)\sinh \left(\frac{n\pi}{a} y\right)$

Use this equation with the values of $C_n$ found in your solution and plot $V(x,a)$ vs. $x$ in the range $x=0$ to $x=a$. Plot only the terms in the sum for $n\le 10$.

# Extra Credit 3.

Use the equation for $V(x,y)$ found in problem 2. along with the equation that relates the electric field just outside of a conductor to $\sigma$ to find the surface charge density on the conductor at a potential of $V_o$. Plot $\sigma(x,a)$ vs. $x$ in the range $x=0$ to $x=a$. Plot only the terms in the sum for $n\le 10$.
