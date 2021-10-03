Due on Thursday, October 7th at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. Use a file name of `Yourlastname_PHYS305_HW6.pdf` (one file only, please). Capitalize the first letter in your last name and use caps and underscores as indicated. **Include your name on the first sheet**.

This homework covers [Boundary Value Problems](boundary_value_problems.html). See also the sections of Griffiths referenced in these notes.

# Integrals

1. Show that $\displaystyle\int_0^\pi \sin 2x \sin x dx$ = 0. (Note that without any calculation, this is expected from a plot of $\sin x$ and $\sin 2x$ and thinking about the area under the curve for their product.)

2. Show that $\displaystyle \int_0^\pi \sin nx \sin lx dx$ = 0 for integer $n$ and $l$ if $l\ne n$ by explicitly evaluating the integral.

3. Compute $\displaystyle\int_0^\pi \sin^2 nx dx$ for
   1. any $n\ne 0$ and
   2. for integer $n$.

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

# &nbsp;2-D Boundary Value Problem

Find the potential $V(x,y)$ inside of a long rectangular duct, $0 \le x\le b$; $0 \le y\le a$, with boundary conditions

1. $V(0,y) = V_o$ (left)
1. $V(b,y) = 0$ (right)
1. $V(x,0) = 0$ (bottom)
1. $V(x,a) = 0$ (top)

<img src="figures/Boundary_Value_Problems_2D_Left.svg"/>

Note that this is a rectangular duct, so your solution should have an $a$ and $b$.

Do this by following the steps that I used in class, which are also in the notes.

# Extra Credit 1.

Show that your answer to the previous problem is consistent with the solution for Griffiths Example 3.3 in the limit that $a/b\rightarrow 0$

# Extra Credit 2.

In problem 2., you will find the $C_n$s in

$\displaystyle V(x,y)=\sum_{n=0}^\infty C_n \sin \left(\frac{n\pi}{a} x \right)\sinh \left(\frac{n\pi}{a} y\right)$

Use this equation with the values of $C_n$ found in your solution and plot $V(x,a)$ vs. $x$ in the range $x=0$ to $x=a$. Plot only the terms in the sum for $n\le 10$.

# Extra Credit 3.

Use the equation for $V(x,y)$ found in problem 2. along with the equation that relates the electric field just outside of a conductor to $\sigma$ to find the surface charge density on the conductor at a potential of $V_o$. Plot $\sigma(x,a)$ vs. $x$ in the range $x=0$ to $x=a$. Plot only the terms in the sum for $n\le 10$.

