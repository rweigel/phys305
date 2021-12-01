# Introduction

In [Continuous Electric Dipole Distributions](continuous_electric_dipole_distributions.html), the problem of finding the electric field due to an object that had a polarization $\mathbf{P}$ "frozen in" was considered.

The approach was to find the bound charge densities that result from this polarization. Then the electric field due to the bound charge densities was computed.

Consider an object that is unpolarized ($\mathbf{P}=0$), but is placed in an external electric field, $\mathbf{E}_{ext}$. In response to this electric field, atomic--sized dipoles will tend to form. Thes induced dipoles create an electric field, which called an induced electric field.

The total field is then

$\mathbf{E}\_{total}=\mathbf{E}\_{external} + \mathbf{E}_{induced}$

By convention, we drop the "total" subscript and abbreviate "external" as "ext". Given that the induced field is can be computed from bound charge densities, we can use $\mathbf{E}\_b$ in place of $\mathbf{E}\_{induced}$ to emphasize this point. In this notation, we have

$\mathbf{E}=\mathbf{E}\_{ext} + \mathbf{E}_{b}$

It is important to note that $\mathbf{E}_b$ depends on $\mathbf{E}$.

Without additional information, it is not possible to compute $\mathbf{E}$ -- we need to know how much $\mathbf{P}$ is generated given $\mathbf{E}$. Once we have $\mathbf{P}$, we can compute the bound charge densities and then $\mathbf{E}_b$.

For many materials, the relationship between $\mathbf{P}$ and $\mathbf{E}$ is linear:

$\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$

where the constant $\chi_e$ is the **electric susceptibility**.

A constant that often appears in induced polarization problems is $\epsilon_o(1+\chi_e)$, which is called **permittivity** or the **dielectric constant**:

$\epsilon\equiv \epsilon_o(1+\chi_e)$

## Example -- Infinite Slab

An object with an electric susceptibility of $\chi_e$ is in the region $|z| \le t$. The object is infinite in extent in the $x$ and $y$ directions.

There is an external electric field of $E_o\zhat$.

Find $\mathbf{E}$

**Answer**

$\mathbf{E}=\mathbf{E}\_{ext} + \mathbf{E}_{b}$

$E_z = E_{ext\text{ z}} + E_{b\text{ z}}$

$E_z = E_o + E_{b\text{ z}}$

At this point, $E_z$ and $E_{b\text{ z}}$ are unknown. We know that $E_{b\text{ z}}$ is related to $P_z$, which is in turn related to $E_z$.

The bound surface densities are $\sigma_b=\pm P_z$ on the top/bottom surfaces of the slab. The polarization is related to $E_z$ by $P_z = \epsilon_o\chi_e E_z$, so $\sigma_b=\pm \epsilon_o\chi_e E_z$.

$\rho_b=0$. This can be seen by taking the divergence of both sides of $\mathbf{E} = \mathbf{E}\_{ext} + \mathbf{E}_{b}$, which gives $\boldsymbol{\nabla}\bfcdot\mathbf{E} = 0 + \rho_b$. Using $\rho_b=-\epsilon_o\boldsymbol{\nabla}\bfcdot\mathbf{P}$ and $\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$ results in $\rho_b=0$.

% This need to be justified. See notes where rho_b is related to rho_f.

As a result of $\sigma_b$, the $E_{b\text{ z}}=-P_z/\epsilon_o=-\chi_e E_z$ in the slab and $E_{b\text{ z}}=0$ outside of the slab.

Thus, inside the slab

$E_z = E_o + E_{b\text{ z}}=E_o-\chi_e E_z$

Solving for $E_z$ gives

$\displaystyle E_z=\frac{E_o}{1+\chi_e}$

Outside the slab, $E_z=E_o$.

Inside the slab, the induced polarization opposes the external electric field and causes the field to be smaller. Outside the slab, the induced electric field has no effect.

## Example -- Dielectric Around a Charged Sphere

In Example 4.5 of Griffiths, he finds the total electric field when a dielectric (polarizable material) is wrapped around a spherical shell with a net charge. 

The total electric field is the sum of the field due to the induced polarization and the charges on the spherical shell.

Verify the equations for the total electric field stated in the solution to Example 4.5 by computing it using

$\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$

where $\mathbf{E}_b$ is the field due to the bound surface charge densities on the inner and outer surface of the dielectric, and $\mathbf{E}_Q$ is the field due to the charges on the surface of the sphere.

**Answer**

Use Gauss's law to find the electric field as a function of $r$ due to three surface charges: $\sigma_Q = Q/4\pi a^2$ on a sphere of radius $a$, $\sigma_{bi}=-\epsilon_o\chi_eQ/4\pi\epsilon a^2$ at $r=a$, and $\sigma_{bo}=\epsilon_o\chi_eQ/4\pi\epsilon b^2$ at $r=b$

$\sigma_Q$ creates $\mathbf{E}_Q$, which is zero for $r\lt a$ and $Q/4\pi\epsilon_o r^2$ for $r\gt a$.

$\sigma_{bi}$ creates $\mathbf{E}\_{bi}$, which is zero for $r\lt a$ and $4\pi a^2\sigma_{bi}/4\pi\epsilon_o r^2$ for $r\gt a$.

$\sigma_{bo}$ creates $\mathbf{E}\_{bo}$, which is zero for $r\lt b$ and $4\pi b^2\sigma_{bo}/4\pi\epsilon_o r^2$ for $r\gt b$.

The sum of the fields due to the three surface charge densities $\mathbf{E}\_{bi} + \mathbf{E}\_{bo} + \mathbf{E}\_Q$ gives $\mathbf{E}$ given in Example 4.5.

# Problems

## Dielectric Around a Charged Sphere

Solve Example 4.5 of Griffiths without using Gauss's law for dielectrics (which is $\oint\mathbf{D}\bfcdot d\mathbf{A}=Q_{f\text{ }encl})$.

Start with $\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$ and then find $\mathbf{E}_b$ by finding the surface charge densities on the inner and outer surface. These surface charge densities are $\sigma_b(R_i)=\mathbf{P}(R_i)\bfcdot\hat{\mathbf{n}}$ and $\sigma_b(R_o)=\mathbf{P}(R_o)\bfcdot\hat{\mathbf{n}}$. To find $\mathbf{E}_b$, use the relationship $\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$.

Once $\mathbf{E}_b$ is found, $\mathbf{E}=\mathbf{E}_b + \mathbf{E}_Q$ can be used to solve for $\mathbf{E}$.

Hint: Inside the dielectric, the equation for $\mathbf{E}$ should depend on $E_r(R_i)$, $r$, and constants. To finish the problem, one needs to solve for the unknown $E(R_i)$. This can be done by setting $r=R_i$ in the equation for $\mathbf{E}$.

**Answer**

Inside the dielectric, the field is due to $\sigma_b(R_i)=-P(R_i)$ and the uniform charge on the conducting surface. The net field inside is then

$\displaystyle E_r(r) = k\frac{Q}{r^2}+k\frac{\sigma_b(R_i)4\pi a^2}{r^2} = k\frac{Q}{r^2}-\frac{a^2}{r^2}P(R_i)$

We don't know $P(R_i)$ yet. However, for a linear dielectric, the polarization $P_r$ is related $E_r$ by $P_r=\chi_eE_r$. Substitution gives

$\displaystyle E_r(r)=k\frac{Q}{r^2}-\frac{R_i^2}{r^2}\chi_e E_r(R_i)$

To finish the problem, set $r=R_i$, solve for $E_r(R_i)$, and then substitute the found value of $E_r(R_i)$ into the above equation.

Setting $r=R_i$ gives

$\displaystyle E_r(R_i)=k\frac{Q}{R_i^2}-\chi_e E_r(R_i)\quad\Rightarrow\quad E_r(R_i)=\frac{kQ}{(1+\chi_e)R_i^2}$

Substitution into the equation above for $E_r(r)$ gives

$\displaystyle E_r(r)=k\frac{Q}{r^2}-\frac{a^2}{r^2}\chi_e \frac{kQ}{(1+\chi_e)a^2}$

This simplifies to

$\displaystyle E_r(r)=\frac{k}{1+\chi_e}\frac{Q}{r^2}$

With $k=4\pi\epsilon_o$ and the definition $\epsilon=\epsilon_o(1+\chi_e)$, this is

$\displaystyle E_r(r)=\frac{1}{4\pi\epsilon}\frac{Q}{r^2}$

Note that the electric field is reduced in the dielectric ($\chi_e\gt 0$), as expected.
