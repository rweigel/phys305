Due on Thursday, November 4th at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. Use a file name of `Yourlastname_PHYS305_HW9.pdf` (one file only, please). Capitalize the first letter in your last name and use caps and underscores as indicated. **Include your name on the first sheet**.

# Polarized Sphere

A sphere of radius $R_o$ has a spherical cavity of radius $R_i$. The sphere and cavity are centered on the origin. The region $R_i\le r\le R_o$ has a polarization $\mathbf{P}=(P_or^2/R_i^2)\hat{\mathbf{r}}$.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(r)$, which is the electric field due to the bound charge densities found in part 1. of this problem.

# Polarized Cylinder

A long solid cylinder of radius $R$ has a polarization $\mathbf{P}=P_o\hat{\mathbf{s}}$. The cylinder is centered on the origin an aligned with the $z$--axis.

1. Find $\sigma_b$ and $\rho_b$.
2. Find $\mathbf{E}_b(s)$, which is the electric field due to the bound charge densities found in part 1. of this problem.

# Induced Polarization

In Example 4.5 of Griffiths, he finds the total electric field when a dielectric (polarizable material) is wrapped around a spherical shell with a net charge. 

The total electric field is the sum of the field due to the induced polarization and the charges on the spherical shell.

Verify the equations for the total electric field stated in the solution to Example 4.5 by computing it using

$\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$

where $\mathbf{E}_b$ is the field due to the bound surface charge densities on the inner and outer surface of the dielectric, and $\mathbf{E}_Q$ is the field due to the charges on the surface of the sphere.

# Extra Credit

Example 4.5 of Griffiths can be solved without using Gauss's law by using the approach that I used in class to find the electric field inside a dielectric slab when it is in an external electric field. The procedure is to start with

$\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$

and then find $\mathbf{E}_b$ by finding the surface charge densities on the inner and outer surface. These surface charge densities are $\sigma_b(R_i)=\mathbf{P}(R_i)\bfcdot\hat{\mathbf{n}}$ and $\sigma_b(R_o)=\mathbf{P}(R_o)\bfcdot\hat{\mathbf{n}}$. To find $\mathbf{E}_b$, use the relationship $\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$.

Once $\mathbf{E}_b$ is found, $\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$ can be used to solve for $\mathbf{E}$.

Hint: Inside the dielectric, the equation for $\mathbf{E}$ should depend on $E_r(R_i)$, $r$, and constants. To finish the problem, one needs to solve for the unknown $E(R_i)$. This can be done by setting $r=R_i$ in the equation for $\mathbf{E}$.