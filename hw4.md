Due on Thursday, September 23rd at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. Use a file name of `Yourlastname_PHYS305_HW4.pdf` (one file only, please). Capitalize the first letter in your last name and use caps and underscores as indicated. **Include your name on the first sheet**.

# Gauss's law

1\. Use Gauss's law to find the electric field near the center (from $s=0$ to $s=3R$) of a long solid nonconducting cylinder  of length $L$, radius $R$, and uniform charge density $\rho_o$. Assume $L\gg R$.

<img src="figures/Gauss_Law_Long_Solid_Cylinder.svg"/>

Provide explicit justifications for the symmetry argument (described in [the notes](gauss_law.html#using-charges-on-an-insulator)) required to apply Gauss's law and include supporting diagrams. Also, provide justifications for all steps in evaluating the integral in Gauss's law.

2\. Plot the electric field magnitude as a function of $s$ from $s=0$ to $s=3R$.

**Answer**:

1\. A common error was a lack of justification for $\mathbf{E}=E_s(s)\hat{\mathbf{s}}$. More justification is needed than "because it is long" or "due to symmetry" because the reason is not obvious. There are three ways to justify this.

1. Consider pairs of lines of charge
2. Consider 4 charges
3. Use geometrical symmetry (translational and rotational)

2\. A common error was plugging in a value of $R$ or $3R$. In the flux equation. 
# Conducting Slab Between Charged Sheets

A conducting slab is centered on the origin, has thickness $t$, surface area $A=w^2$, and has a net charge of $Q$. At $x=\pm 5t$ there are large nonconducting sheets with uniform charge density $\pm \sigma_o$. The thickness $t$ of the slab is much smaller than $w$.

<img src="figures/Conductors-Slab-Between-Sheets.svg"/>

1. Find the surface charge density on both faces of the conducting slab, assuming that any charge on it is uniformly distributed.
2. Find and plot $E_x$ versus $x$.
3. Find and plot the electric potential $V$ versus $x$. Assume $V(0)=0$.

**Answer**

Technically you should have provided answers for $E_x$ and $V$ for $x\gt 5t$ and $x\lt -5t$. I gave extra credit if answers were given for these regions.

A common error was issues with signs. In the notes I mentioned that one way of getting the signs right is to assume all unknown surface charges are positive and write the equations for the electric field accordingly.

Another common error was in plotting $V$. $V$ should be continuous and if $E_x$ is flat, $V$ should be linear. If $E_x$ is positive, the slope of $V$ should be negative. To check your $V$ plot, draw vectors for $\mathbf{E}$ with directions given by your $E_x$ plot. If you are moving in the direction of $\mathbf{E}$, $V$ should decrease.

# Conducting Sphere with a Cavity

The following figure shows the cross--section of a spherical conductor of radius $2R$ with a spherical cavity of radius $R$, both of which are centered on the origin. There is a nonconducting spherical shell that is also centered on the origin, has a $3q$ uniformly distributed on its surface, and a radius $3R$. At the origin, there is a charge $q$.

<img src="figures/Conductors_Sphere_with_Cavity_with_Shell.svg"/>

Using Gauss's law, 

1. Find and plot $E$ versus $r$.
2. Find and plot $V$ versus $r$. Assume $V(r=\infty)=0$.

Justify your steps when using Gauss's law.

**Answer**

Not graded.

# Work Required to Assemble Charges

For the following charge distribution, compute 

1. the electric potential at the origin, 
2. the electric potential at any position $x,y$, and
2. the work required to assemble the charge distribution.

<img src="figures/Electric_Potential_3_Charges_on_Triangle.svg"/>

**Answer**

1\. A common error was having a term in $V$ that was $kq_1/(-b)$. The denominator of potential is a length which must be positive. Also, many student wrote answers for 2. that were correct but when $x=y=0$ was plugged in, they did not get the same equation that they wrote for this part.


