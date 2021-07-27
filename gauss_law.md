= Gauss' Law =

== Overview ==

Gauss' Law states that the integral of electric flux, \(\Phi_E\) over a closed surface, \(S\), is related to the amount of charge inside the surface.

$$\Phi_E\equiv\oint_{S} \mathbf{E}\cdot d\mathbf{a} = Q_{Inside\,S}/\epsilon_0$$

There are two ways to prove this, mathematically and visually.

Unlike Coulomb's Law for the electric field, in which the electric field stands alone on the left-hand-side of an equation, in Gauss' Law, the electric field is buried in an integral. As a result, using Gauss' Law to compute the electric field is generally only easier than using Coulomb's Law when the electric field can be factored out of the integral (usually by a symmetry argument). Gauss' Law is also useful when one can find a surface on which the electric field is always zero - in this case, one can conclude the amount of charge inside the surface is zero. Finally, Gauss' Law is useful if you are given the electric field on a surface and want to calculate the amount of charge enclosed. These three cases are shown in the following images.

Figure 1: A Gaussian sphere is centered on a point charge \(q\). Due to Coulomb's Law, one can conclude that the electric field will be perpendicular to the surface. So we can write

$$\oint_{S} \mathbf{E}\cdot d\mathbf{a} = \oint_{SS} |\mathbf{E}| da$$

In addition, Coulomb's Law states that the electric field depends only on the distance from a point charge, so \(|\mathbf{E}|\) does not depend on the location \(da\), so it can be factored out of the integral

$$\oint_{SS} |\mathbf{E}| da=|\mathbf{E}| \oint_{SS} da$$

Finally, the surface area of a sphere is \(4\pi r^2\), giving

$$|\mathbf{E}| \oint_{SS} da = |\mathbf{E}|4\pi r^2$$

So equation (1) simplifies to

$$\Phi_E=|\mathbf{E}|4\pi r^2 = q/\epsilon_0$$

Solving for \(|\mathbf{E}|\) gives

$$|\mathbf{E}|=\frac{q}{4\pi\epsilon_0}\frac{1}{r^2}$$

This equation can be re-written to account for the argument that the electric field is radial, which was used in its derivation

$$\mathbf{E}=\frac{q}{4\pi\epsilon_0}\frac{\hat{\mathbf{r}}}{r^2}$$

As may have been expected, use of Gauss' Law using arguments from Coulomb's Law to simplify the integral has resulted in an electric field equation for a point charge at the origin at a distance \(r\) from the point charge. Coulomb's Law for the electric field is

$$\mathbf{E} = \frac{q'}{4\pi\epsilon_0}\frac{1}{|\mathbf{r}-\mathbf{r}'|^2}\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|}$$

If \(q'\) is at the origin, then \(\mathbf{r}'=0\), giving

$$\mathbf{E}=\frac{q}{4\pi\epsilon_0}\frac{\hat{\mathbf{r}}}{r^2}$$

In this case, starting with Coulomb's Law got us an answer in one step. But the power of Gauss' Law is that it can give an answer for charge configurations when use of Coulomb's Law would be much more difficult.

Figure 2: Closely spaced charges are placed on a very long line. At the center of the line, a Gaussian surface, in the form of a cylinder is drawn. The electric field on the caps and side of the cylinder is zero - for each charge on the left of the cylinder, one can find a charge to the right of the cap that exactly cancels its horizontal component.
As a result, (1) the electric field is expected to be perpendicular to the side of the cylinder.  In addition, (2) the magnitude of the electric field is expected to be constant on the surface of the cylinder if the height of the cylinder is small enough.

Statement (1) allows the first step and statement (2) the second step

$$\oint_{S} \mathbf{E}\cdot d\mathbf{a} = \oint_{Cylinder\,side} |\mathbf{E}| da =  |\mathbf{E}| \oint_{Cylinder\,side} da$$

The surface area of the side of a cylinder with radius \(\rho\) and height \(h\) is \(2\pi rh\). So from Gauss' Law we can conclude

$$|\mathbf{E}|2\pi \rho h = Q_{Inside}/\epsilon_0$$

This equation can be re-written if we know the spacing of the charges along the line. If the spacing is, say, N electrons over a distance \(h\), then \(Q_{Inside}=10e/h\), which gives

$$|\mathbf{E}| = \frac{10e}{2\pi\epsilon_0}\frac{1}{\rho}$$

More generally, if the charge per length is \(\lambda\), then the electric field a distance \(r\) from the line is

$$|\mathbf{E}| = \frac{\lambda}{2\pi\epsilon_0}\frac{1}{\rho}$$

We argued that the electric field will be perpendicular to the line, so we can also write

$$|\mathbf{E}|_{\perp} = \frac{\lambda}{2\pi\epsilon_0}\frac{1}{\rho}$$

or

$$\mathbf{E} = \frac{\lambda}{2\pi\epsilon_0}\frac{\hat{\mathbf{\rho}}}{\rho}$$

Consider how we would calculate the electric field using Coulomb's Law for this problem. Each charge \(q'_i\) is located at a position \(x'_i\hat{\mathbf{x}}\), so we would need to sum over all \(N\) charges using

$$\mathbf{E} = \sum_{i=0}^{N}\frac{q'_i}{4\pi\epsilon_0}\frac{1}{|\mathbf{r}-x'_i\hat{\mathbf{x}}|^2}\frac{\mathbf{r}-x'_i\hat{\mathbf{x}}}{|\mathbf{r}-x'_i\hat{\mathbf{x}}|}$$

In the section on continuous charge distributions, it is shown how this sum can be evaluated, but even then, finding the electric field associated with a long line of charges is much more difficult than using Gauss' Law.

A common usage error is to draw a Gaussian surface that has no net charge inside of it and conclude that the electric field is zero on the surface. Without any other information, if the net charge inside a surface is zero, you can only conclude the electric flux, \(\Phi_E\) is zero. 

Figure X shows the electric field \(\mathbf{E}=E_o\cos(\theta)\hat{\mathbf{r}}\) vectors on the surface of a spherical Gaussian surface centered at \(r=0\) having radius \(a\).

$$\oint_{S} \mathbf{E}\cdot d\mathbf{a} = \oint_{Sphere\,surface} |\mathbf{E}| da = \int_{\theta=0}^{pi}\int_{\phi=0}^{2\pi}E_o\cos(\theta)\left(a\sin(\theta)d\phi d\theta\right)=0$$

This electric field has a surface integral of zero, but was not generally zero on the Gaussian surface. The most that we can conclude is that inside this Gaussian surface, the net charge is zero. (This type of electric field occurs on the surface of a conductor placed in a region with a constant electric field, for example, a small spherical conductor between the plates of a large capacitor.)

== Use ==

== Mis-use ==

== Problems ==

=== Conceptual ===

In another universe, the electric field created by a charge \(q\) is found to be \(\mathbf{E} = k'q/r^3\)

where \(k'\) is a constant with appropriate units.  Which of the following are true in this universe?

* Gauss' Law in integral form
* Gauss' Law in differential form

=== Use ===

Consider a dipole. One can find the electric field everywhere using superposition.

Can a single Gaussian surface be used to find the electric field everywhere?

Can a single Gaussian surface be used to find the approximate electric field far away from the dipole? What approximation(s) is/are required?

=== Use ===

Consider an infinite line of charge with a uniform surface charge density. Explain why one can conclude that the electric field, if calculated, will point radially outward.


=== Infinite Line of Charge ===

In general, in cylindrical coordinates, the electric field has the form

$$\mathbf{E}(s,\phi,z)=E_s(s,\phi,z)\hat{\mathbf{s}}+E_{\phi}(s,\phi,z)\hat{\boldsymbol{\phi}}+E_z(s,\phi,z)\hat{\mathbf{z}}$$

where \(s\) is the radial coordinate in cylindrical coordinates.

Consider an infinite line of charge with a uniform charge per unit length of \(\lambda_o\) on the \(z\)-axis. The typical approach to finding that the equation for the electric field is

$$\mathbf{E}(s)=\frac{\lambda_o}{2\pi\epsilon_o}\frac{\hat{\mathbf{s}}}{s}$$

is to use a cylindrical Gaussian surface and Gauss' law. When using Gauss' law, one must make arguments for why

1. \(E_s\) does not depend on \(\phi\) and \(z\)

2. \(E_z=0\)

With these two justifications and Gauss' law, one arrives at only an equation for the radial component of the electric field, \(E_s\). To complete the solution, one also needs to provide an argument for why 

3. \(E_{\phi}=0\).

Derive the equation given above for the electric field using Gauss' law and explicitly state arguments for 1.-3.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Solution
|-
|
I gave this problem because I have come to realize that students can use Gauss' law to find the electric field, but can't often answer conceptual questions about justifications for the steps needed to get the solution. The problem is that most textbooks don't emphasize the arguments or provide follow-up questions to test their understanding of the arguments and so students don't think too deeply about them.

Understanding the reasoning for this problem is critical for understanding the boundary condition equations

$$(\mathbf{E}_2-\mathbf{E}_1)\cdot \hat{\mathbf{n}} = \mathbf{E}_{2\perp}-\mathbf{E}_{1\perp} = \left[-\frac{\partial \Psi_2}{\partial n}+\frac{\partial \Psi_1}{\partial n}\right]_{n=0}=\frac{\sigma}{\epsilon_o}$$

$$\mathbf{E}_{2\parallel}-\mathbf{E}_{2\parallel}=(\mathbf{E}_2-\mathbf{E}_1)\cdot \hat{\mathbf{t}}=0$$

where \(n\) is the coordinate that is perpendicular to the boundary surface and outward to the volume enclosed by the boundary surface; \(t\) is any coordinate parallel to the surface.

Several students used the solution for \(\mathbf{E}\) given for arguments 1.-3., but this is circular reasoning. The point of the problem is to justify all of the steps needed to get to the solution.

I did not expect a solution with the level of detail in what follows. I generally looked for arguments or words that seemed close to something said below. I did not write extended comments on your solutions for statements that were wrong - you should be able to determine what was wrong by reading the following solution.

1. \(E_s\) does not depend on \(z\) because the charge distribution does not change if we shift the origin of \(z\). Said another way, two people who solve this problem using a different location for \(z=0\) should get the same result. \(E_s\) does not depend on \(\phi\) because if we rotate the charge distribution around the \(z\)-axis by \(\phi\), the charge distribution does not change. Said another way, two people who solve the problem using a different \(\phi=0\) line perpendicular to the line of charge should get the same answer. The same argument can be used to argue that \(E_z\) and \(E_{\phi}\) do not depend on \(\phi\) and \(z\), but this is not needed because in 2. and 3. they are found to be zero.

2. \(E_z=0\) - Assume the line extends from \(z=\pm L\). Adding the electric field due to a differential charge at \(z\) to that from a differential charge at \(-z\) gives an electric field that points in the \(\hat{\mathbf{s}}\) direction in the \(x-y\) plane. An infinite line of charge can be created by letting \(L\rightarrow\infty\). Or, for very small \(s\), in the \(x-y\) plane the line of charge appears infinite.

3. \(E_{\phi}=0\) by the same argument as 2.

'''Detailed solution using 1.-3. and Gauss' law'''

$$\mathbf{E}(s,\phi,z)=E_s(s,\phi,z)\hat{\mathbf{s}}+E_{\phi}(s,\phi,z)\hat{\boldsymbol{\phi}}+E_z(s,\phi,z)\hat{\mathbf{z}}$$

A Gaussian cylinder of radius \(s\) and a height \(h\) and centerline along the \(z\)-axis has three surfaces, with normals of \(\hat{\mathbf{z}}\) on the top cap, \(-\hat{\mathbf{z}}\) on the bottom cap, and \(\hat{\mathbf{s}}\) on the curved side.

$$\oint \mathbf{E}\cdot \hat{\mathbf{n}}da = \int_{top\,cap} \mathbf{E}\cdot \hat{\mathbf{z}} da +  \int_{bottom\,cap} \mathbf{E}\cdot (-\hat{\mathbf{z}}) da + \int_{side}\mathbf{E}\cdot \hat{\mathbf{s}} da$$

\(\mathbf{E}\cdot \hat{\mathbf{z}} = E_z(s,\phi,z)\) and we have argued that \(E_z=0\), so the first two integrals are zero.

\(\mathbf{E}\cdot \hat{\mathbf{s}} = E_s(s,\phi,z)\), so the last integral is, using \(da=sdzd\phi\),

$$\int_{side}\mathbf{E}\cdot \hat{\mathbf{s}} da = \int_{z=-h/2}^{h/2}\int_{\phi=0}^{2\pi} E_s(s,\phi,z) sdz\,d\phi$$

Because \(E_s\) is independent of \(z\), we can write

$$\int_{z=-h/2}^{h/2}\int_{\phi=0}^{2\pi} E_s(s,\phi,z) sdz\,d\phi=\int_{z=-h/2}^{h/2}\int_{\phi=0}^{2\pi} E_s(s,\phi) sdz\,d\phi=h\int_{\phi=0}^{2\pi} E_s(s,\phi) sd\phi$$

Because \(E_s\) is independent of \(\phi\), we can write

$$h\int_{\phi=0}^{2\pi} E_s(s,\phi) sd\phi=h\int_{\phi=0}^{2\pi} E_s(s) sd\phi$$

Because \(s\) and \(\phi\) are orthogonal,

$$h\int_{\phi=0}^{2\pi} E_s(s) sd\phi=hE_s(s) s\int_{\phi=0}^{2\pi} d\phi=hE_s(s) s2\pi$$

Note that Gauss' law only gave us \(E_s\) - we had to argue why \(E_{\phi}\) and \(E_z\) were zero. In addition, in order to do the integration in Gauss' law, we needed to provide additional justification for why \(E_s\) could only depend on \(s\). So this Gauss' law problem had two separate components: 1. arguments that reduce and simplify the general solution

$$\mathbf{E}(s,\phi,z)=E_s(s,\phi,z)\hat{\mathbf{s}}+E_{\phi}(s,\phi,z)\hat{\boldsymbol{\phi}}+E_z(s,\phi,z)\hat{\mathbf{z}}$$

and then 2. evaluation of the integral in Gauss' law. I find that students that don't understand 1. are not able to articulate why a given Gaussian surface can't be used to find the electric field. For example, their answer to why a Gaussian sphere could not be used to find the electric field in this problem typically only involves an ambiguous statement about symmetry; "symmetry" is ambiguous because both a Gaussian sphere and a Gaussian cylinder have symmetry).
|}

=== Thin Cylinder of Charge ===

Use Gauss' law and other arguments to find the electric field for an infinitely long cylinder of radius \(b\) with a charge per unit length of \(\lambda_o\) on its surface and its centerline along the \(z\)-axis. As in the previous problem, state all arguments needed to arrive at the final equation.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Solution
|-
|
1. Same argument as the previous problem.

2. Assume the cylinder is created by placing infinite lines of charge parallel to the \(z\)-axis on the surface of a cylinder. One can use a diagram to show that at an arbitrary point in space, either inside or outside of the cylinder, one can find two lines of charge which have an electric field that sums to give an electric field that points in the \(\hat{\mathbf{s}}\) direction.  A diagram should be given to show this.

3. \(E_{\phi}=0\) by the same argument as 2.

A common error is to note that Gauss' law with a Gaussian cylinder with radius less than \(b\) has no charge enclosed, so

$$\oint \mathbf{E}\cdot d\mathbf{a} = 0 \Rightarrow \mathbf{E}=0$$

inside the cylinder. The fact that the integral of a vector is zero does not imply the vector is zero. And without additional words, I can't tell if you understand that. The above claim is equivalent to the statement

$$\int f(x)\,dx = 0 \Rightarrow f(x)=0$$

A better solution is to state that from 1.-3., we know \(\mathbf{E}=E_s(s)\hat{\mathbf{s}}\). Using \(d\mathbf{a}=\mathbf{\hat{s}}sdz\,d\phi\) gives

$$\oint \mathbf{E} \cdot d\mathbf{a} = 0 + 0 + \int_{side} \mathbf{E} \cdot d\mathbf{a} =  \int_{side} E_s(s)\hat{\mathbf{s}}\cdot \hat{\mathbf{s}}sd\phi=2\pi h s E_s(s)$$

where the two zero terms are due to the fact that we have argued \(\mathbf{E}=E_s(s)\hat{\mathbf{s}}\) and so the dot product of this with the normal direction on the top and bottom caps is zero (see solution for the line of charge for full details).

For \(s\lt b\), \(\oint \mathbf{E} \cdot d\mathbf{a}\) is zero, so for \(s\ne 0\), \(E_s(s)=0\). Gauss' law does not provide an answer for \(s=0\) because we get \(E_s=0/0\), but one can argue using pairs of lines of charge that the radial field must be zero for \(s=0\). It is interesting to note that there is a purely geometrical approach to showing that the radial field is zero inside the cylinder. It is similar to the approach Newton used to show that the net force inside of a shell of mass is zero (he did not use calculus!).

To find \(E_s\) outside of the cylinder, use

$$2\pi h s E_s(s) = \frac{Q_{encl}}{\epsilon_o} = \frac{\lambda_o h}{\epsilon_o}$$
|}


=== Use ===

Consider an infinite plane of charge with a uniform surface charge density. Explain why one can conclude that the electric field, if calculated, will be perpendicular and away from to the plane.

=== Use ===

Consider an infinite line of charge with a uniform surface charge density. Which of the following Gaussian surfaces can be used to compute the electric field:

1. A cylinder with its caps parallel to the line.
2. A cylinder with its caps perpendicular to the line.
3. A sphere
4. A square box
5. A rectangular box
6. A plane perpendicular to the surface

=== Use ===

Consider an infinite plane with a uniform surface charge density. Which of the following Gaussian surfaces can be used to compute the electric field:

1. A cylinder with its caps parallel to the surface.
2. A cylinder with its caps perpendicular to the surface.
3. A sphere
4. A square box
5. A rectangular box
6. A plane perpendicular to the surface

=== Use ===

Consider an infinite plane with a uniform surface charge density. Set up the integral that needs to be solved to compute the electric flux through a sphere with half of its volume above the plane.

=== Use ===

Consider sphere with a surface charge density of \(\sigma_o\cos\theta\). Sketch the sphere and surface charges and indicate where the density is largest. Sketch the field lines.

Can a sphereical Gaussian surface be used to find the electric field 
1. inside the sphere?
2. outside the sphere?

=== Use ===

Consider long tube with a square cross-section with a uniform surface charge density on its surfaces. Sketch the tube and surface charges.

Can a Gaussian surface be used to find the electric field 
1. inside the tube?
2. outside the tube?

=== Use ===

A non-conducting spherical shell is covered with charge uniformly on its surface. It is then dented.

<blockquote>"The electric field near the center of the shell is zero because a Gaussian sphere centered at the origin and fully inside of the shell will have zero enclosed charge."</blockquote>

* True
* False

Justify your answer.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
False. It is only the electric flux, \(\Phi_E\) through the Gaussian sphere that is zero, because 

$$\Phi_E\equiv\oint \mathbf{E}\cdot d\mathbf{a} = Q_{Inside\,S}/\epsilon_0 = 0$$.

But \(\mathbf{E}\) can't be pulled out of the integral so we can't say  \(\mathbf{E}=0\). All we can say is that if we were to compute the electric field by other means, integral would be zero. 
|}

To calculate the electric field near the center of the shell, Gauss' Law could be easily used
* True
* False

Justify your answer.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Nope. Gauss' Law is generally only useful for computing \(\mathbf{E}\) when it can be pulled out of the integral. Here we don't have a symmetry argument that would allow this. To compute the electric field, you would need to do an integral like the ones done for continuous charge distributions. And it would be complicated.
|}

If the dent is inward (so sphere was punched from the outside), will the electric field at the origin be larger or smaller than that for the un-dented sphere?

=== Derivation ===

To compute the electric field for a point charge at the origin using the integral equation for Gauss' Law, the following steps are made

$$\oint_S \mathbf{E}\cdot d\mathbf{a} = \int_S |\mathbf{E}|da = |\mathbf{E}|\int_S da = |\mathbf{E}|4\pi r^2$$

Justify each step and explain all terms.  Provide a diagram.

=== Use ===

The electric field was measured at the locations in space shown. A table of the measurements is given in the table.

\(\theta\) \(E_r\) (\E_\phi\)

The measurements were repeated by rotating the half ring 360 degrees around the \(z\)-axis in increments of 10 degrees. It was found that the table did not change much, so data were not recorded.

Estimate the charge enclosed in the sphere swept out by rotating the half ring 360 degrees.

=== Derivation ===

To compute the electric field due to an infinite line of charge using the integral equation for Gauss' Law, the following steps are made

$$\oint_S \mathbf{E}\cdot d\mathbf{a} = \int_S |\mathbf{E}|da = |\mathbf{E}|\int_S da = |\mathbf{E}|2\pi r L$$

\(Q_{Enclosed} = \lambda_o L\)

Justify each step and explain all terms.  Provide a diagram.

=== Derivation ===

When a single point charge \(q\) is placed at the center of a spherical shell, the electric flux through the shell's surface, \(SS\), can be computed, using Coulomb's Law and the definition of electric flux, as

$$\oint_{SS}\mathbf{E}\cdot d\mathbf{a}= \int_{\phi=0}^{2\pi}\int_{\theta=0}^{\pi}(kq/r^2)(r^2\sin\theta\,d\theta\,d\phi) = q_{At\,origin}/\epsilon_0$$

Gauss' Law is 

$$\oint_{Any\,S}\mathbf{E}\cdot d\mathbf{a} = Q_{Inside\,S}/\epsilon_0.$$

Explain the arguments that allow for the generalization from \(SS\) to \(Any\,S\) and \(q_{At\,origin}\) to \(Q_{Inside\,S}\).

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
See also class notes and description given in Griffiths (3rd Edition) on page 68.

We can think of flux as proportional to the number of field lines that pass through a surface (positive flux for exiting lines, negative flux for entering lines).  If the same number of field lines exit one closed surface also exit another closed surface, the flux through both surfaces is the same (and flux through both is positive since all lines exiting).

1. Based on the above statement, charges outside of \(S\) or \(SS\) result in zero net flux (flux due to lines going in is equal to flux due to lines going out).  This explains the subscript "inside S" or "inside SS" on \(Q\).
2. We can replace \(q_{At\,origin}\) with \(Q_{Inside\,S}\) by considering a spherical Gaussian surface that is (1) centered on an off-center charge and (2) has a radius small enough so it is fully enclosed by \(SS\).  The flux leaving the small Gaussian surface is \(q/\epsilon_0\) based on the given equation above.  Any flux leaving the small Gaussian surface leaves \(SS\).  So \(q\) can be anywhere inside of the outer shell and the flux through \(SS\) is the same as when \(q\) is at the origin. 
3. We can apply argument 2. to each charge inside of \(SS\) and thus replace \(q_{Inside\,S}\) with \(Q_{Inside\,SS}\), where \(Q\) is the sum of all charges inside, provided superposition applies - the electric field (and flux into or out of \(SS\)) due to one charge does not change in the presence of other charges.

Another argument:
* If the surface was not spherical, then \(r\) would depend on \(\theta\) and \(\phi\).  But because of the cancellation of \(r\) in the integral, the integral does not depend on the shape of the surface.  This implies that we can replace \(SS\) with any \(S\) and the charge \(q\) can be at any location inside.

In your solution I was looking for a direct response to two questions:
1. Why can we replace \(SS\) with \(Any\,S\)?
2. Why can we replace \(q_{At\,origin}\) with \(Q_{Inside\,S}\)?

Many students made statements that were true, e.g., "superposition applies", but did not give specifics, e.g., when multiple charges are in the shell the electric field from one charge does not change and so neither does its flux through a small Gaussian surface surrounding it. On this quiz, I was fairly lenient on grading when vague statements were made; I assumed that you understood, but were not able to put your thoughts fully into words.  As time goes on, I will get less so. It is important for you to understand all aspects of the equations we use and why each step in certain derivations are allowed.
|}

=== Derivation ===

A point charge \(q\) is at the origin.  To compute the electric flux through a spherical Gaussian surface \(SS\) of radius \(a\) that is centered at the origin, the following steps are made:

\(\int_S \mathbf{E}\cdot d\mathbf{a} =  \int_{SS} |\mathbf{E}|da = |\mathbf{E}|\int_{SS} da = |\mathbf{E}|4\pi a^2 = 4\pi kq\)

Provide a brief justification for each step after the first equation.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
1. \(\int_S \mathbf{E}\cdot d\mathbf{a} =  \int_{SS} |\mathbf{E}|da\) - Electric field due to charge at origin is parallel to \(d\mathbf{a}\) on \(SS\).
2. \(\int_{SS} |\mathbf{E}|da = |\mathbf{E}|\int_{SS} da\) - Electric field is constant on surface of \(SS\).
3. \(|\mathbf{E}|\int_{SS} da = |\mathbf{E}|4\pi a^2\) - Surface area of a sphere of radius \(a\) is \(4\pi a^2\).
4. \(|\mathbf{E}|4\pi a^2 = 4\pi kq\) - At distance \(a\) electric field is \(kq/a^2\) and \(k=1/(4\pi\epsilon_0)\).
It is important to note that these steps only apply in special situations. In many problems, Gauss' Law can't be used to easily compute the electric field. The charge configurations where Gauss' Law can be used to compute \(E\) include a point charge, an infinite line or cylinder of charge, an infinite sheet of charge, a uniformly charged shell or sphere.  You should be able to derive the electric field for all of these charge configurations using Gauss' Law and also be able to justify each step as you did above.
|}

=== Infinite Line of Charge ===

Write down the formal version of the integral equation for Gauss' Law and define all terms in the equation. Show how it can be used to compute the electric field for ...

Justify all steps and use a diagram that defines any unit vector used in your equation for \(\mathbf{E}\). Draw a sketch of \(\mathbf{E}\) versus distance from the center of the axis.

=== Infinite Lines of Charge ===

Lines of charge are glued to the surface of a long tube.

=== Near-Infinite Line of Charge ===

=== Ring of Charge ===

Consider a ring of charge and Gaussian cylinder with a very small height. 

Use Gauss' Law to find the electric field for \(z\simeq=0\) for \(\rho < a\) and \(rho > a). Provide details that justify each step in your derivation.

Compare your answer with that found using the continuous charge distribution method.

=== Rings of Charge ===

Consider an infinite stack of rings of charge.

(Note this is the same question as the Infinite Lines of Charge problem.)

=== Infinite Sheet of Charge ===

Write down the formal version of the integral equation for Gauss' Law and define all terms in the equation. Show how it can be used to compute the electric field for ...

Justify all steps and use a diagram that defines any unit vector used in your equation for \(\mathbf{E}\). Draw a sketch of \(\mathbf{E}\) versus distance from the center of the axis.

=== Near-Infinite Sheet of Charge ===

=== Infinite Sheets of Charge ===

The electric field created by an individual sheet of charge is ...

Consider two sheets of charge.

1. Find the electric field between and outside using superposition of the fields of both sheets
2. Use Gauss' Law with Gaussian surfaces as shown. Treat the electric field from each sheet individually as unknowns.

=== Circular vs. Square Sheet of Charge ===

# Point Charges

1. A point charge is placed outside of a spherical shell.  What is the electric flux through its surface due to the point charge?
2. A point charge is placed at the center of a spherical shell. What is the electric flux through the shell's surface due to the point charge?
3. A point charge is placed just inside of a spherical shell. What is the electric flux through the shell's surface due to the point charge?

Justify your answers.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
1. Zero.  
2. <math>q/\epsilon_0</math>, where <math>q</math> is the amount of charge placed at center.
3. <math>q/\epsilon_0</math>, where <math>q</math> is the amount of charge placed at center.

We can think of flux as proportional to the number of field lines that pass through a surface.  Lines going in provide negative flux, lines out positive.  If you draw field lines due to a point charge through a closed surface that does not enclose the point charge, all of the point charge's field lines going into the surface must exit.

The answer for 2. and 3. follow from Gauss' Law in integral form: \(\Phi_E = \oint_{S} \mathbf{E}\cdot d\mathbf{a} = Q_{inside\mbox{ }S}/\epsilon_0\). In both cases a \(q\) is the total charge inside of the surface on which we want to know the electric flux, \(\Phi_E\). The integral would be very difficult to compute for 1. and 3.  However, Gauss' Law tells you the answer - no complicated integration is needed. In addition, note that in cases 1. and 3., Gauss' Law would not be useful in computing the electric field. Gauss' Law is useful for computing the electric field when (1) it is constant on the surface of interest and (2) its angle with respect to the surface normal is constant, in which case it can be factored out of the integral.
|}


# Introduction

## Background

In Chapter 22, your textbook has an excellent description of Gauss's law along with many useful figures. This tutorial was written with the assumption that you have read Sections 22.1-22.4. Many of the problems here are similar to those given in the text; they were written to ensure that you understood the very brief arguments and mathematical steps given. Quite often students think that they understand a problem because they understand a solution. However, you won't understand a problem at the level required for an exam question unless you can also solve the problem without looking at the solution.

Last week's tutorial involved deriving the electric field for a continuous charge distribution. These derivations require careful set-up and integration of vector components of the field. This week we will show that it is much easier to get an answer for _some_ continuous charge distributions using Gauss's law. 

Gauss's law is derived from Coulomb's law, so they are both equally valid. Coulomb's law can always be used to find the electric field due to a continuous charge distribution when the charge density is known. Gauss's law is only useful for computing the electric field for certain continuous charge distributions. The list includes:

* near the center of a long and uniformly charged line,
* near the center of a long and uniformly charged cylindrical shell,
* at any location for a uniformly charged spherical shell, and
* near the center of a large and uniformly charged sheet.

Gauss's law can also be used to find the electric field due to a uniformly charged solid cylinder and a uniformly charged solid sphere because they can be created by nesting shells together and using a superposition argument.

%The key reason that Gauss's law can be used to find the electric field in these cases is a surface can be imagined for which the electric field is perpendicular and has a constant magnitude (including a zero magnitude).

Gauss’s law states that the total electric flux through any closed surface is proportional to the total charge inside the surface.

The word "flux" means "flow". Before there was an understanding of electrical phenomena, Faraday and Maxwell would draw electric field lines and speak of "electricity" flowing along them in the same way that fluid flows along a streamline (if you put dye in a flowing fluid, you'll see the path of a streamline). In Chapter 22.2, there is a discussion of the flux of fluid through a rectangle. This type of fluid flow analogy was used by Faraday and Maxwell to understand electrical phenomena. As emphasised in the previous tutorial, **nothing flows along an electric field line**. A field line only tells you the direction of force on a positively charged particle placed on it.

Somehow, even though the fluid flow analogy is wrong because there is nothing flowing along an electric field line, the analogy helped Faraday and Maxwell to get the right answers. 

## The discovery of Gauss's law

Here is what lead to Gauss discovering his law (maybe). See also Figure 22.1 in the textbook

Imagine wrapping a small spherical shell of radius $r_{small}$ around a point charge $Q_{c}$ that is at the center of the shell. The electric field everywhere on the surface of the shell will be $kQ_c/r_{small}^2$ because all points on the shell are a distance of $r_{small}$ from the charge. For lack of a better word (or vanity) call this imaginary surface a Gaussian surface.

Now multiply this field by the surface area of the shell, which is $4\pi r_{small}^2$:

$$\left(\frac{kQ_c}{r_{small}^2}\right)4\pi r_{small}^2=\frac{Q_c}{\epsilon_o},$$


Now imagine wrapping a large spherical shell of radius $r_{large}$ around the same point charge and multiply the area times the field on its surface:

$$\left(\frac{kQ_c}{r_{large}^2}\right)4\pi r_{large}^2=\frac{Q_c}{\epsilon_o}$$

In both cases, the radius of the shell cancels.

**Gauss's Conclusion**: If somehow I could measure the electric field on a spherical shell, found it to be constant, and knew the radius of the shell, I could state how much charge is at the center of the shell. The radius of the spherical shell does not matter. In equation form, the expected experimental result is

$$
E_{ss}A_{ss} = \frac{Q_{center}}{\epsilon_o}
$$
\label{eqn:simple}

where $ss$ means a spherical shell centered on a point charge $Q_{center}$. The product of an electric field and an area is called electric flux or $\Phi_E$ (that is a capital phi).

Gauss's innovation is that he took this equation and asked what would happen if the surface was not spherical and the charge was not a single point charge. He showed that you could still figure out how much charge was enclosed. Gauss's law is

$$
\oint \mathbf{E}\cdot d\mathbf{A}=\frac{Q_{encl}}{\epsilon_o}\qquad\text{Gauss's law}
$$
\label{eqn:general}

\include{Gauss/figures/Flux_Differential}


We'll break down this equation later after a simpler version is used. In words, this equation means that if you measure the electric field perpendicular ($E_{\perp}$) to each small patch of area $dA$ on a closed surface, and sum the product of $E_{\perp}dA$  for each patch, you can assert that the amount of charge inside of the surface is proportional to this sum. As will be discussed, the quantity $E_{\perp}dA$ is equal to $\mathbf{E}\cdot d\mathbf{A}$. The circle on the integral sign means that the sum must be taken over a closed surface (if you put water inside of the surface, there would be no leaks).

Gauss's law is a compact equation with many nuances. This tutorial will examine the calculation of the different components of it.  We'll use a slight generalization of Equation~\ref{eqn:simple} (or a simplification of Equation~\ref{eqn:general}) that does not require integration:

$$
EA = \frac{Q_{encl}}{\epsilon_o}
$$
\label{eqn:simple2}

**Restriction**: \mathbf{E} is always perpendicular ($\perp$) to the closed surface, $A$ and the electric field, $E$, does not change over the surface, $A$. In addition, the electric field either always points either outwards or inwards from the surface the volume encloses.

**Exception**: If $E$ is parallel to part of the surface, omit its area from $A$.

**If we can imagine a Gaussian surface on which the electric field is constant and always perpendicular or zero, Equation~\ref{eqn:simple2} can be used.** You may recall from the previous tutorials that there was an emphasis on the direction of the electric field. This is why -- if we can make an argument for why the electric field is perpendicular to a surface, we have the right to use Gauss's law in the form of Equation~\ref{eqn:simple2} to find the electric field.

----

In the following section, you are asked to review the difference between an insulator and a conductor.

Section~\ref{section:using_gausss_law} involves the calculations required for using Equation~\ref{eqn:simple2} to find the electric field due to a charge distribution. Once you have mastered this, you'll be ready to learn how to use the general equation for Gauss's law (Equation~\ref{eqn:general}) in Section~\ref{section:computing_electric_flux}. (However, as noted earlier, Equation~\ref{eqn:general} is only useful for computing the electric field created by certain charge distributions. It turns out that for all of the charge distributions for which Equation~\ref{eqn:general} can be used to easily compute the electric field, Equation~\ref{eqn:simple2} applies.)

Finally, in Section~\ref{gausss_law_and_conductors} Gauss's law is used to solve problems involving conductors.



# Using Gauss's Law
\label{section:using_gausss_law}

In this section, only charge distributions for which Equation~\ref{eqn:simple2} applies are considered and all charges are on an insulator. Think of the charges on an insulator as glued so they can't move. 
%In general, if charges are placed uniformly on or within a conductor, the charges will quickly redistribute on the conductor's surface. In this case, the charge density would not be constant, which would further complicate matters.

The first part of using Gauss's law in the form of Equation~\ref{eqn:simple2} involves finding the amount of charge enclosed by a Gaussian surface. This is done in Section~3.1.

The last two parts are (a) Justifying why the electric field satisfies the restriction on Equation~\ref{eqn:simple2} and (b) solving for $E$. This is done in Section~3.2.

\clearpage

## Finding enclosed charge

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=blue!50!blue,colback=white,height fill,title=Example: Line of charge]

A total of $+3Q$ is uniformly distributed on an insulator that is a line of length $L$. The blue Gaussian cylinder shown has a length $l$, radius $r$, and the same center line as the insulator.

\tcsidebyside{
    \includegraphics[scale=0.3]{Gauss/figures/Line_and_Gaussian_Cylinder.png}
}{
\begin{tikzpicture}
    \draw[step=0.4cm,gray,very thin] (0,0) grid (6.4,2.4)
\end{tikzpicture}
}

1. Find the charge density on the line.

2. Find the amount of charge enclosed by the Gaussian cylinder when it has radii of
$r=/100$, $r=l/2$, $r=l$, and $r=2l$. The enclosed charge should be in terms of one or more of $\epsilon_o$, numbers, and the parameters given ($Q$, $L$, $l$).

3. Plot the four values of enclosed charge calculated above versus the radius of the Gaussian cylinder. 

4. Find an equation that relates $Q_{encl}$ to $r$. Plot this equation on the graph above.

\vspace{-2em}
\begin{center}\rule{2cm}{0.4pt}\end{center}
\vspace{-1em}

{\bf 1. Answer}: Because the charge is uniformly distributed on the line, the the charge density is simply the total charge divided by the length: $\lambda={3Q}/{L}$.

{\bf 2. Answer}:  The dashed line in the figure is the part of the line inside of the Gaussian cylinder. The length of the dashed line is $l$. The charge enclosed for all four cases is $Q_{encl}=\lambda l=3Q{l}/{L}$. In retrospect, one could have obtained this equation without considering the charge density - the charge enclosed is the total charge $\times$ the ratio $l/L$. 

The equation for the charge enclosed does not depend on the radius of the Gaussian cylinder. Visually, this is expected. If the radius of the cylinder increases, the length of the line inside of the cylinder does not change. 

Check: As $l\rightarrow 0$, we expect from the diagram that the amount of charge enclosed should approach zero. This equation also says that as the ratio $l/L\rightarrow 0$, $Q_{encl}\rightarrow 0$. Does this make sense?

{\bf 3. Answer:}

\include{Gauss/figures/Line_and_Gaussian_Cylinder_Graph}

{\bf 4. Answer}: As noted in the answer to part 2., the enclosed charge does not change as the radius of the Gaussian cylinder changes. So $Q_{encl}(r)=3Q{l}/{L}=const$, corresponding to the straight line on the graph.

\end{tcolorbox}

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=blue!50!blue,colback=white,height fill,title=Example: Hollow Cylinder]

An insulating and hollow cylinder of radius $R$ and length $L$ has a charge of $+3Q$ distributed \emph{on its curved surface}. The blue Gaussian cylinder shown has a length $l$ and radius $r$ and has the same center line as the charged cylinder.

\tcsidebyside{
    \includegraphics[scale=0.13]{Gauss/figures/Cylindrical_Shell_and_Gaussian_Cylinder.png}
}{
\hspace{1cm}
\begin{tikzpicture}
    \draw[step=0.4cm,gray,very thin] (0,0) grid (6.4,2.4)
\end{tikzpicture}
}

1. Find the charge density on the curved part of the insulating cylinder.

2. Find the amount of charge enclosed in Gaussian cylinder of radii $r=0$, $r=R/2$, $r=2R$, and $r=4R$.

3. Plot the four values of enclosed charge calculated above versus the radius of the Gaussian cylinder.

4. Find an equation that relates $Q_{encl}$ and $r$ for $r<R$. Plot this equation on the graph above.

5. Find an equation that relates $Q_{encl}$ and $r$ for $r>R$. Plot this equation on the graph above.

\vspace{-2em}
\begin{center}\rule{2cm}{0.4pt}\end{center}
\vspace{-1em}

{\bf 1. Answer}: The surface is an area, so the appropriate charge density will be a surface charge density, which has units of charge per length$^2$. The area of the curved surface is the circumference $\times L = 2\pi RL$. The charge is uniformly distributed, so the charge density is simply the total charge divided by the area: $\sigma={3Q}/{2\pi RL}$.

{\bf 2. Answer}: Imagine that the blue Gaussian cylinder was fully inside of the hollow cylinder. There would be no charge inside of it. As a result, the charge enclosed for $r=0$ and $r=R/2$ is zero. Once the Gaussian cylinder's radius is larger than the hollow cylinder's radius, the total charge inside of the Gaussian cylinder does not change. To find the charge enclosed in this case, we need to find the area of the hollow cylinder enclosed. It is $2\pi R l$. The charge enclosed is the charge density computed in part 1. times this area: $Q_{encl}=\sigma (2\pi R l) = 3Q{l}/{L}$. In retrospect, one could have obtained this equation without considering the surface charge density - the charge enclosed is the total charge $\times$ the ratio $l/L$.

Check: Visually, as the length of the Gaussian cylinder shrinks to zero, the enclosed charge should approach zero. The equation for $Q_{\encl}$ is consistent with this observation.

{\bf 3. Answer}: 

\include{Gauss/figures/Cylindrical_Shell_and_Gaussian_Cylinder_Graph}

{\bf 4. Answer}: The enclosed charge is zero for $r<R$, so $Q_{\encl}(r)=0$.

{\bf 5. Answer}: The enclosed charge is constant for $r>R$, so, $Q_{\encl}(r)=3Q{l}/{L}=const$.

\end{tcolorbox}

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,height fill,title=Solid cylinder]

A solid insulating cylinder of radius, $R$ and length, $L$ has a charge of $+3Q$ uniformly distributed within it. The Gaussian cylinder shown has the same center line as the insulating cylinder, length $l$, and radius $r$.

\tcsidebyside{
    \includegraphics[scale=0.27]{Gauss/figures/Solid_Cylinder_and_Gaussian_Cylinder.png}
}{
\hspace{1cm}
\begin{tikzpicture}
    \draw[step=0.4cm,gray,very thin] (0,0) grid (6.4,2.4)
\end{tikzpicture}
}

1. Find the charge density in the insulating cylinder.
\ifsolutions
\\
\\
{\bf Answer:} The insulating cylinder is a volume. The volume of a cylinder is its cross-sectional area time its height, $\pi R^2 L$. The charge density is charge/volume, $\rho=3Q/(\pi R^2 L)$.
\else
\\[2cm]
\fi

2. Find the amount of charge enclosed in a Gaussian cylinder of radius $r=0$, $r=R/2$, $r=2R$, and $r=4R$.

\ifsolutions
{\bf Answer}: When $r<R$, the Gaussian cylinder is fully inside of the insulating cylinder. The charge in the Gaussian cylinder is the charge density of the insulating cylinder times the volume of the Gaussian cylinder: $Q_{encl}=\rho \pi r^2 l = 3Q(r^2/R^2)(l/L)$.

For any $r\ge R$, the amount of charge inside the Gaussian cylinder does not change with $r$. The amount of charge depends on volume of insulator inside of the Gaussian cylinder, which is $\pi R^2 l$, so $Q_{encl}=\rho \pi R^2 l = 3Q(l/L)$. When $l=L$, $Q_{encl}=3Q$, which makes sense because all of the insulator is inside of the Gaussian cylinder.

\else
\\[2cm]
\fi

3. Plot the four values of enclosed charge  calculated above versus the radius of the Gaussian cylinder.

\ifsolutions
{\bf Answer}: For $r<R$, the curve will be a parabola because of the $r^2$. For $r>R$, curve will be a horizontal line that intersects with the parabola at $r=R$. For values outside of the cylinder, r $>$ R, the enclosed charge will be constant.

\else
\\[2cm]
\fi

4. Find an equation that relates $Q_{encl}$ and $r$ for $r<R$. Plot this equation on the graph above.

\ifsolutions
{\bf Answer}: As noted in part 2, the charge enclosed is $Q_{encl}=\rho \pi r^2 l = 3Q(r^2/R^2)(l/L)$. Because of the dependence on r$^2$ the curve is parabolic. 

\else
\\[2cm]
\fi


5. Find an equation that relates $Q_{encl}$ and $r$ for $r>R$. Plot this equation on the graph above.

\ifsolutions
{\bf Answer}: As noted in part 2, the charge enclosed is $Q_{encl}=3Q$ so it is constant. 

\else
\\[2cm]
\fi

\end{tcolorbox}

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,height fill,title=Spherical shell]

An insulating sphere of radius $R$ has a charge of $+3Q$ distributed \emph{on its surface}. The cross-section of the sphere is shown along with a dashed line representing the surface of a Gaussian sphere, which has the same center as the charged sphere and a radius $r$.

\tcsidebyside{
    \input{Gauss/figures/Spherical_Shell_with_Gaussian_Sphere}
}{
\hspace{2cm}
\begin{tikzpicture}
    \draw[step=0.4cm,gray,very thin] (0,0) grid (6.4,2.4)
\end{tikzpicture}
}

1. Find the surface charge density on the insulating sphere.

\ifsolutions
{\bf Answer}: $\sigma = 3Q/4\pi R^2$
\else
\\[2cm]
\fi

2. Find the amount of charge enclosed in Gaussian sphere of radii $r=0$, $r=R/2$, $r=2R$, and $r=4R$.

\ifsolutions
{\bf Answer}: When $r < R$, $Q_{encl}=0$. When $r\ge R$, $Q_{encl}=3Q$ because all of the charge is enclosed.
\else
\\[2cm]
\fi

3. Plot the four values of enclosed charge calculated above versus the radius of the Gaussian sphere.
\\[2cm]

4. Find an equation that relates $Q_{encl}$ and $r$ for $r<R$. Plot this equation on the graph above. \
\ifsolutions

{\bf Answer}: $Q_{encl}=0$
\else
\\[2cm]
\fi

5. Find an equation that relates $Q_{encl}$ and $r$ for $r>R$. Plot this equation on the graph above.\

\ifsolutions
{\bf Answer}: Plot should be a horizontal line between $r$ and $R$ at y = 0 and a horizontal line for $r\ge R$ at y = $3Q$.
\else
\\[2cm]
\fi
\end{tcolorbox}

%\clearpage

%\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,height fill,title=Solid sphere]

%An insulating sphere of radius $R$ has a charge of +3Q distributed uniformly \emph{throughout} it. The cross-section of the sphere is shown along with a dashed line representing the surface of a Gaussian sphere, which has the same center as the charged sphere and a radius $r$.

%\tcsidebyside{
%    \input{Gauss/figures/Solid_Sphere_with_Gaussian_Sphere}
%}{
%\hspace{2cm}
%\begin{tikzpicture}
%    \draw[step=0.4cm,gray,very thin] (0,0) grid (6.4,2.4)
%\end{tikzpicture}
%}

%1. Find the charge density in the sphere.
%\\[2cm]

%2. Find the amount of charge enclosed in Gaussian sphere of radii $r=0$, $r=R/2$, $r=2R$, and $r=4R$.
%\\[2cm]

%3. Plot the four values of enclosed charge calculated above versus the radius of the Gaussian sphere.
%\\[2cm]

%4. Find an equation that relates $Q_{encl}$ and $r$ for $r<R$. Plot this equation on the graph above.
%\\[2cm]

%5. Find an equation that relates $Q_{encl}$ and $r$ for %$r>R$. Plot this equation on the graph above.

%\end{tcolorbox}

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,height fill,title=Large sheet]

An insulator in the form of a square sheet with side length $L$ has a charge of $+3Q$ distributed uniformly on it. The blue Gaussian cylinder has a height $h$ and radius $r$ and half of it is above the sheet.

\tcsidebyside{
    \includegraphics[scale=0.27]{Gauss/figures/Plane_and_Gaussian_Cylinder.png}
}{
\hspace{1cm}
\begin{tikzpicture}
    \draw[step=0.4cm,gray,very thin] (0,0) grid (6.4,2.4)
\end{tikzpicture}
}

1. Find the charge density on the sheet.
\ifsolutions
{\bf Answer}: $\sigma=3Q/L^2$
\else
\\[2cm]
\fi

2. Find the amount of charge enclosed in Gaussian cylinder of radii $r=0$, $r=R/2$, $r=2R$, and $r=4R$.

\ifsolutions
{\bf Answer}: As noted in class, no $R$ was given in the problem statement. The question should have asked for the charge enclosed for $r=L/32$, $r=L/16$, $r=L/8$, $r=L/4$. We are not interested in larger $r$ because Gauss's law can't be used unless the Gaussian cylinder is small relative to the sheet. This is discussed in the large sheet solution in the next section.

The amount of charge enclosed for $r<L$ is $Q_{encl}=\sigma \pi r^2 = 3Q r^2/L^2$.
\else
\\[2cm]
\fi

3. Plot the four values of enclosed charge calculated above versus the radius of the Gaussian cylinder.
\\[2cm]

4. Find an equation that relates $Q_{encl}$ and $r$ for $r<R$. Plot this equation on the graph above.
\\[2cm]

5. Find an equation that relates $Q_{encl}$ and $r$ for $r>R$. Plot this equation on the graph above.

\ifsolutions
{\bf Answer}: The line should be a parabola that passes through the origin.
\else
\\[2cm]
\fi

\end{tcolorbox}

\newpage

## Justifying Equation~\ref{eqn:simple2} and solving for $E$

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=blue!50!blue,colback=white,height fill,title=Line of charge]

For the charged line in the previous section,

1. Explain why the electric field satisfies the constraints of Equation~\ref{eqn:simple2}.

2. In terms of $\lambda$, $\epsilon_o$, and $r$, what is the electric field at all distances from the line?

\vspace{-2em}
\begin{center}\rule{2cm}{0.6pt}\end{center}
\vspace{-1em}

{\bf Answer to 1.} In the Field Lines tutorial, the electric field lines associated with a line of charge were drawn. It was found that near the center of the line of charge, the field lines were near radial and that the field lines became straighter near the center as the length of the line of charge increased. A side view of the Gaussian cylinder and field lines near the center of a long charged line is shown below.
\vspace{-0.5em}
\input{Gauss/figures/Line_and_Gaussian_Cylinder_Field}

Suppose the Gaussian cylinder is very small in both height and radius. The field lines that pass through it are near radial -- they are parallel to the end caps of the cylinder (perpendicular to the area vector for the caps) and perpendicular to the curved surface (parallel to the area vector for the cylinder). In addition, the electric field is not changing over the surface. As a result, the constraints on Equation~\ref{eqn:simple2} are satisfied. 

{\bf Answer to 2.} Given our answer to 1., we can now use

$EA={Q_{encl}}/{\epsilon_o}$

The curved area of the Gaussian surface is $2\pi rl$. The end cap areas of $\pi r^2$ each are part of the surface area of the Gaussian cylinder are ignored because the field is parallel to the end caps. 

The charge enclosed which was found previously is $3Ql/L$. 

$E(2\pi rl)=\frac{3Ql/L}{\epsilon_o}\quad\Rightarrow\quad E = \frac{3Q}{2\pi\epsilon_o Lr}$

Technically, this equation applies at the center of a finite-length charged line. If the line becomes ``infinite'', then the equation applies everywhere because the field lines are everywhere perpendicular to the line. This is the reason books often refer to the field of an infinite line of charge - it is a statement that the electric field lines are radially outward from the line everywhere.

Using $\lambda=3Q/L$ found previously,

$E = \frac{\lambda}{2\pi\epsilon_o}\frac{1}{r}$

This is the magnitude of the electric field near the center of a long and uniformly charged line. The direction is radial, but the direction cannot be obtained from Gauss's law. Instead, it was obtained by drawing a sketch of the field lines based on consideration of individual charges and superposition arguments. 

Once we were able to justify using Equation~\ref{eqn:simple2}, this result was obtained using only a few equations. In contrast, in the previous tutorial in which Coulomb's law was used, finding the solution required integration.

\end{tcolorbox}

\newpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,height fill,title=Hollow cylinder]
For the charged hollow cylinder in the previous section,

1. Explain why the electric field satisfies the constraints of Equation~\ref{eqn:simple2}.

\ifsolutions
{\bf Answer}: The cylinder can be thought of as an arrangement of long lines of charge such that we can always find pairs of infinitely long charged lines that produce electric fields that sum to be perpendicular to the Gaussian surface. In addition, many pairs of long charged lines  will result in a uniformly charged cylindrical shell. As a result of these arguments, the net field due to the insulating cylinder will be perpendicular to the Gaussian surface and thus parallel to the area vector.

Hint: Assume that the cylinder is infinitely long. A surface charge can be created by gluing infinitely long charged lines lengthwise on the surface of the charged cylinder. In the following figure, two such lines are shown with open circles along with the electric field that each creates at a point on the curved part of the Gaussian cylinder. (The lines 1 and 2 extend into the page.)

In addition, the electric field is not changing over the surface. 

\input{Gauss/figures/Cylindrical_Shell_and_Gaussian_Cylinder_Centerline_View}


\else
\fi

2. What is the electric field at all distances from its center line?

\ifsolutions
{\bf Answer}: The electric field is perpendicular to the curved surface of the cylinder and parallel to its caps. So the area we need to account for is the area of the curved surface of the Gaussian cylinder, which is $2\pi r l$. This area does not change when the Gaussian cylinder radius $r$ is larger than the insulating cylinder radius $R$. Equation~\ref{eqn:simple2} is

$$EA = \frac{Q_{encl}}{\epsilon_o}$$

Plugging in the area gives

$$E2\pi r l = \frac{Q_{encl}}{\epsilon_o}$$

As found previously, the equation for $Q_{encl}$ changes at $r=R$

$$Q_{encl}=\left\{
\begin{array}{ll}
      \displaystyle 0 & r < R \\
      \displaystyle 3Q & r \ge R \\
\end{array} 
\right. $$

so the equation that we need to solve with $E$ will also change at $r=R$:

\[ 
\begin{array}{ll}
      \displaystyle E 2\pi r l = \frac{0}{\epsilon_o} & r < R \\\\
      \displaystyle E 2\pi r l = \frac{3Q}{\epsilon_o} & r \ge R \\
\end{array} 
\]

Solving for $E$ gives

$$E=\left\{
\begin{array}{ll}
      0 & r < R \\\\
      \displaystyle\frac{3Q}{2\pi l r\epsilon_o} & r \ge R \\
\end{array}
\right.
$$

Although the charge is distributed on an area, we can also identify a linear charge density as being the charge per unit length of the cylinder. This linear charge density is $\lambda = 3Q/l$. As a result, we can write

$$E=\left\{
\begin{array}{ll}
      0 & r < R \\\\
      \displaystyle\frac{\lambda}{2\pi r\epsilon_o} & r \ge R \\
\end{array}
\right.
$$

The interpretation of this last set of equations is that outside of the cylinder, the electric field is the same as the field would be if all of the charge on the cylinder was collapsed onto its center line. The reason is that the equation  $\lambda/2\pi r\epsilon_o$ is the same as that for a line of charge. This type of result also occurs with a uniformly charged spherical shell, a solid charged sphere, and a long solid cylinder (when the charge density only varies with radius). In these cases, the field outside the object is the same as if all of the charge was collapsed onto the center of the sphere or the center line of the cylinder. 

\else
\fi

\end{tcolorbox}

%\clearpage

%\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!back,colback=white,height fill,title=Solid cylinder]

%For the charged solid cylinder in the previous section,

%1. Explain why the electric field satisfies the constraints of Equation~\ref{eqn:simple2}.

%2. What is the electric field at all distances from its center line?

%\begin{center}\rule{2cm}{0.4pt}\end{center}


%\end{tcolorbox}

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,height fill,title=Spherical shell]

For the charged spherical shell in the previous section,

1. Explain why the electric field satisfies the constraints of Equation~\ref{eqn:simple2}.

\ifsolutions
{\bf Answer}: Similar to the hollow cylinder, we can always find pairs of charges on the surface of the sphere with electric fields that sum to be radial (try to draw this to convince yourself). These radial field lines will be parallel to the area vector for a region dA on the surface of the spherical Gaussian surface. In addition, the electric field is not changing over the surface. 
\fi

2. What is the electric field at all distances from its center?

\ifsolutions
{\bf Answer}: The area we need to account for is the area of the of the Gaussian sphere, which is $4\pi r^2$. This equation does not change when the Gaussian sphere radius $r$ is larger than the insulating sphere radius $R$. Equation~\ref{eqn:simple2} is $EA = \frac{Q_{encl}}{\epsilon_o}$. Plugging in the area gives:

$$E 4\pi r^2 = \frac{Q_{encl}}{\epsilon_o}$$

As found previously, the equation for $Q_{encl}$ changes at $r=R$:

$$Q_{encl}=\left\{
\begin{array}{ll}
      \displaystyle 0 & r < R \\
      \displaystyle 3Q & r \ge R \\
\end{array} 
\right. $$

so the equation that we need to solve for $E$ using will also change at $r=R$:

\[ 
\begin{array}{ll}
      \displaystyle E 4\pi r^2 = \frac{0}{\epsilon_o} & r < R \\\\
      \displaystyle E 4\pi r^2 = \frac{3Q}{\epsilon_o} & r \ge R \\
\end{array} 
\]

Solving for $E$ gives

$$E=\left\{
\begin{array}{ll}
      0 & r < R \\\\
      \displaystyle\frac{3Q}{4\pi \epsilon_o r^2} & r \ge R \\
\end{array}
\right.
$$

The interpretation of this last set of equations is that outside of the sphere, the electric field is the same as the field would be if all of the charge on the sphere was collapsed onto its center -- if there is a charge $3Q$ at the origin, the the field it creates is $3Q/4\pi \epsilon_o r^2$.

(For those with a careful eye, if $r=0$, the we get $E=0/0$, which is indeterminate. Technically Gauss's law can't tell us the electric field at the origin. But we can argue that it is zero because for every charge on the shell there is another charge that exactly cancels its electric field at $r=0$.)
\fi

3. The equation for the electric field for a line of charge is valid near the center of a long uniformly charged line. Are there any restrictions on the equation that you found in your answer to part 2?

\ifsolutions
{\bf Answer}: There are no restrictions. The electric field due to the charges on the surface will always be perpendicular to the surface of the Gaussian sphere. If the size of the insulating sphere changes, the electric field will will still be perpendicular to the Gaussian sphere.
\fi

\ifsolutions
\else
\begin{center}\rule{2cm}{0.4pt}\end{center}
\fi

\end{tcolorbox}

%\clearpage

%\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,height fill,title=Solid sphere]

%For the charged solid sphere shell in the previous section,

%1. Explain why the electric field satisfies the constraints of Equation~\ref{eqn:simple2}.

%2. What is the electric field at all distances from its center?

%\begin{center}\rule{2cm}{0.4pt}\end{center}

%\end{tcolorbox}

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,height fill,title=Large sheet]

For the charged sheet in the previous section,

1. Explain why the electric field satisfies the constraints of Equation~\ref{eqn:simple2}.
\ifsolutions

{\bf Answer}: As was covered in class, near the center of a finite uniformly charged sheet, the electric field lines are nearly perpendicular to the sheet. As a result, our Gauss's law solution will be valid in this region. Often we say the sheet is ``infinitely large''. Of course, creating an infinitely large sheet is impossible; this statement means that the point of interest is near enough to the center of a finite sheet so that the equation for the electric found using Gauss's law applies (or that the field lines are perpendicular so that Gauss's law can be used to derive the electric field). In addition, the electric field is not changing over the surface. 

We use similar logic for a line of charge. Near the center of a finite line of charge, the field lines are nearly perpendicular to the line, but near the ends the field lines are not perpendicular. So the statement ``infinite line of charge'' means that that the point of interest is near enough to the center of the line of charge that the simple equation for the electric field using Gauss's law applies.
\fi

2. What is the electric field at all distances from its center?

\ifsolutions
{\bf Answer}: The amount of charge enclosed was found to be $3Q \pi r^2/L^2$ as long as $r < L$. The area that applies is the area of the two caps of the cylinder, which is $A=2(\pi r^2)$. In addition, the electric field is not changing over the surface.  The electric field is parallel to the curved surface of the cylinder and thus perpendicular to the area vector so the dot product of the two is zero. As argued above, the equation $EA = Q_{encl}/\epsilon_o$ applies. Plugging in these values give:

$$E = \frac{3Q}{2L^2\epsilon_o}$$

This equation is most often written in terms of the charge density of the sheet, which is $3Q/L^2$. In this case,

$$E = \frac{\sigma}{2\epsilon_o}$$

\fi


%\begin{center}\rule{2cm}{0.4pt}\end{center}


\end{tcolorbox}

