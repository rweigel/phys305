= Charge Densities =

* A line of length \(L\) with a charge \(Q\) spread uniformly on it has a charge density of \(\lambda=Q/L\) with units of \([C]/[m]\).  If nonuniform, \(\lambda(x)\) or \(\lambda(\mathbf{r}')\) is used and \(\lambda=dq/dx\).
* A surface with area \(A\) and a charge \(Q\) spread uniformly on it has a charge density of \(\sigma=Q/A\) with units of \([C]/[m^2]\). If nonuniform, \(\sigma(x,y)\) or \(\sigma(\mathbf{r}')\) is used and \(\sigma=dq/dA\).
* A volume with volume \(V\) and a charge \(Q\) spread uniformly in it has a charge density of \(\rho=Q/V\) with units of \([C]/[m^3]\). If nonuniform, \(\rho(x,y,z)\) or \(\rho(\mathbf{r}')\) is used and \(\rho=dq/dV\).

A total charge $Q$ is uniformly distributed within a sphere of radius \(b\) that is centered on the origin.

* Compute the charge density $\rho$.

Answer: 

$$\rho = \frac{Q}{\frac{4}{3}\pi b^3}$$

* Verify that $\int_{\mathcal{V}}\rho\,dv$, where \(\mathcal{V}\) is surface on which there is charge, gives the expected answer.

Answer: The expected result of the integration is $Q$. To do the integral, we need to choose a coordinate system and write the differential $dv$ in this coordinate system. From calculus, in spherical coordinates, $dv=\sin\theta r^2 dr\d\theta d\phi$ and so the integral is
$$
\int_{\mathcal{V}}\rho\,dv=\int_0^{2\pi}\int_0^\pi\int_0^b\rho\sin\theta\,r^2\,dr\,d\theta\,d\phi=\rho \int_0^{2\pi}\int_0^\pi\int_0^b\sin\theta r^2 dr\,d\theta\,d\phi = \rho \frac{4}{3}\pi b^3
$$

In the above $\rho$ was be factored out because it does not depend on $r$, $\theta$, or $\phi$, In part 1., it was found that 

$$\rho = \frac{Q}{\frac{4}{3}\pi b^3}$$

Using this for $\rho$, we conclude

$$
\int_{\mathhcal{V}}\rho\,dv = Q
$$
as expected.

In this problem, the answer was somewhat obvious and so the integration was not really needed. However, later in the semester you will encounter cases where $\rho$ depends on $r$. In this case, integration is required to find the total charge (and the $\rho$ can not be factored out of the integral as it was in the answer to 2).

A total charge $Q$ is uniformly distributed on a square that lies between \(-2b\le x\le 2b\) and \(-2b\le y\le 2b\).

* Compute the charge density $\sigma$ on the square.
* Verify that $\int_{\mathhcal{S}}\sigma\,ds$, where \(\mathcal{S}\) is surface on which there is charge, gives the expected answer.

A total charge $Q$ is uniformly distributed on disk of radius \(b\) that lies in the \(x\)-\(y\) plane and is centered on the origin.

* Compute the charge density $\sigma$ on the square.
* Verify that $\int_{\mathhcal{S}}\sigma\,da$, where \(\mathcal{S}\) is surface on which there is charge, gives the expected answer. (Hint: Use cylindrical coordinates for \(da\)).

== Charge Density ==

A sphere of radius 1 m has 1 C of charge spread uniformly on its surface and 10 C of charge uniformly distributed throughout its volume.

Compute the surface and volume charge densities.

== Charge Density ==

A sphere of radius \(a\) has volume charge density of \(\rho_o\,r^2/a^2\). Compute the total charge.

== Charge Density ==

A sphere of radius \(a\) has a surface charge density of \(\sigma_o\,\cos\theta\), where \(\theta\) is the spherical coordinate polar angle. Compute the total charge on the surface of the sphere.

Compute the total charge.

== Charge Density ==

A 2-meter line of charge of has -10 Coulombs of charge spread uniformly on it.  

# Compute \(\lambda\).
# How many electrons does this correspond to?
# What is the average spacing between the electrons on the line of charge?

== Charge Densities ==

A line of charge of length \(L\) has a linearly increasing charge density, a charge density of zero on the left end, and a total charge \(Q\).  Compute \(\lambda(x)\).

== Charge Densities ==

Lines of charge of length \(L\) and charge density \(\lambda\) are placed side-by-side to form a sheet of charge of width \(w\).  Compute \(\sigma\).
