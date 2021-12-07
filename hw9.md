Due on Thursday, November 4th at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. Use a file name of `Yourlastname_PHYS305_HW9.pdf` (one file only, please). Capitalize the first letter in your last name and use caps and underscores as indicated. **Include your name on the first sheet**.

# Polarized Sphere

% Copied to notes

A sphere of radius $R_o$ has a spherical cavity of radius $R_i$. The sphere and cavity are centered on the origin. The region $R_i\le r\le R_o$ has a polarization $\mathbf{P}=(P_or^2/R_i^2)\hat{\mathbf{r}}$.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(r)$, which is the electric field due to the bound charge densities found in part 1. of this problem.

**Answer**

1. $\sigma_b=-P_o$ at $r=R_i$ and $\sigma_b=P_oR_o^2/R_i^2$ at $r=R_o$. $\rho_b=-4P_o r/R_i^2$.

2. One can use Gauss's law with the above charge densities to find: $\mathbf{E}=0$ for $r\lt R_i$ and $r\gt R_o$ and $\mathbf{E}=-P_r(r)\hat{\mathbf{r}}/\epsilon_o$, where $P_r(r) = P_o r^2/R_i^2$. It is easier to use Gauss's law for dielectrics. Inside the sphere, there is no free charge, so $\oint\mathbf{D}\bfcdot d\mathbf{A}=0$. From symmetry arguments (what are they?), we can write $\mathbf{D}=D_r(r)\hat{\mathbf{r}}$ and so the integral reduces to $D_r 4\pi r^2=0 \Rightarrow D_r=0$ for all $r\gt 0$.  Using the definition of $\mathbf{D}=\epsilon_o\mathbf{E}+\mathbf{P}$ with $\mathbf{P}=0$ for $0\lt r\lt R_i$ and $r\gt R_o$ gives $\mathbf{E}=0$ in these regions. $E_r=0$ at $r=0$ from a symmetry argument (what is it?). Inside the sphere, $\mathbf{P}$ is non--zero and $D_r=0 \Rightarrow E_r + P_r/\epsilon_0\Rightarrow E_r=-P_r/\epsilon_o$ as before.

# Polarized Cylinder

A long solid cylinder of radius $R$ has a polarization $\mathbf{P}=P_o\hat{\mathbf{s}}$. The cylinder is centered on the origin and aligned with the $z$--axis.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(s)$, which is the electric field due to the bound charge densities found in part 1. of this problem.

**Answer**

% Copied to notes

1. $\sigma_b=P_o$ (at $s=R$) and $\sigma_b=0$ on caps. $\rho_b=-P_o/s$.
2. Gauss's law with these charge densities gives $\mathbf{E}=-(P_o/\epsilon_o)\hat{\mathbf{s}}$ inside and $0$ outside. A common error was to not use integration to find $Q_{encl}$, which is required if $\rho$ is not constant. Using Gauss's law for dielectrics gives the same result and requires less calculation.

# Induced Polarization

% Copied to notes

In Example 4.5 of Griffiths, he finds the total electric field when a dielectric (polarizable material) is wrapped around a spherical shell with a net charge. 

The total electric field is the sum of the field due to the induced polarization and the charges on the spherical shell.

Verify the equations for the total electric field stated in the solution to Example 4.5 by computing it using

$\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$

where $\mathbf{E}_b$ is the field due to the bound surface charge densities on the inner and outer surface of the dielectric, and $\mathbf{E}_Q$ is the field due to the charges on the surface of the sphere.

**Answer**

Use Gauss's law to find the electric field as a function of $r$ due to three surface charges: $\sigma_Q = Q/4\pi a^2$ on a sphere of radius $a$, $\sigma_{bi}=-\epsilon_o\chi_eQ/4\pi\epsilon a^2$ at $r=a$, and $\sigma_{bo}=\epsilon_o\chi_eQ/4\pi\epsilon a^2$ at $r=b$

$\sigma_Q$ creates $\mathbf{E}_Q$, which is zero for $r\lt a$ and $Q/4\pi\epsilon_o r^2$ for $r\gt a$.

$\sigma_{bi}$ creates $\mathbf{E}\_{bi}$, which is zero for $r\lt a$ and $4\pi a^2\sigma_{bi}/4\pi\epsilon_o r^2$ for $r\gt a$.

$\sigma_{bo}$ creates $\mathbf{E}\_{bo}$, which is zero for $r\lt b$ and $4\pi b^2\sigma_{bo}/4\pi\epsilon_o r^2$ for $r\gt b$.

The sum of the fields due to the three surface charge densities $\mathbf{E}\_{bi} + \mathbf{E}\_{bo} + \mathbf{E}\_Q$ gives $\mathbf{E}$ given in Example 4.5.

# Extra Credit

% Copied to notes

Example 4.5 of Griffiths can be solved without using Gauss's law by using the approach that I used in class to find the electric field inside a dielectric slab when it is in an external electric field. The procedure is to start with

$\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$

and then find $\mathbf{E}_b$ by finding the surface charge densities on the inner and outer surface. These surface charge densities are $\sigma_b(R_i)=\mathbf{P}(R_i)\bfcdot\hat{\mathbf{n}}$ and $\sigma_b(R_o)=\mathbf{P}(R_o)\bfcdot\hat{\mathbf{n}}$. To find $\mathbf{E}_b$, use the relationship $\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$.

Once $\mathbf{E}_b$ is found, $\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$ can be used to solve for $\mathbf{E}$.

Hint: Inside the dielectric, the equation for $\mathbf{E}$ should depend on $E_r(R_i)$, $r$, and constants. To finish the problem, one needs to solve for the unknown $E(R_i)$. This can be done by setting $r=R_i$ in the equation for $\mathbf{E}$.

**Answer**

Inside the dielectric, the field is due to $\sigma_b(a)=-P(a)$ and the uniform charge on the conducting surface. The net field inside is then

$\displaystyle E_r(r) = k\frac{Q}{r^2}+k\frac{\sigma_b(a)4\pi a^2}{r^2} = k\frac{Q}{r^2}-\frac{a^2}{r^2}P(a)$

We don't know $P(a)$ yet. However, for a linear dielectric, the polarization $P_r$ is related $E_r$ by $P_r=\chi_eE_r$. Substitution gives

$\displaystyle E_r(r)=k\frac{Q}{r^2}-\frac{a^2}{r^2}\chi_e E_r(a)$

To finish the problem, set $r=a$, solve for $E_r(a)$, and then substitute the found value of $E_r(a)$ into the above equation.

Setting $r=a$ gives

$\displaystyle E_r(a)=k\frac{Q}{a^2}-\chi_e E_r(a)\Rightarrow E_r(a)=\frac{kQ}{(1+\chi_e)a^2}$

Substitution gives

$\displaystyle E_r(r)=k\frac{Q}{r^2}-\frac{a^2}{r^2}\chi_e \frac{kQ}{(1+\chi_e)a^2}$

This simplifies to

$\displaystyle E_r(r)=\frac{k}{1+\chi_e}\frac{Q}{r^2}$

With $k=4\pi\epsilon_o$ and the definition $\epsilon=\epsilon_o(1+\chi_e)$, this is

$\displaystyle E_r(r)=\frac{1}{4\pi\epsilon}\frac{Q}{r^2}$

Note that the electric field is reduced in the dielectric ($\chi_e\gt 0$), as expected.