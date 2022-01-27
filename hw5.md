Due on Thursday, September 30th at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. Use a file name of `Yourlastname_PHYS305_HW5.pdf` (one file only, please). Capitalize the first letter in your last name and use caps and underscores as indicated. **Include your name on the first sheet**.

This homework covers [Capacitance](capacitance.html) and [Boundary Value Problems](boundary_value_problems.html). See also the sections of Griffiths referenced in these notes.

# Spherical Capacitor

% Copied to notes

Charge is uniformly distributed on two concentric spherical conducting shells, the cross-section of which is shown. Both shells have a thickness of $t$. The inner shell has an outer radius of $a$ and net charge of $-Q$. The outer shell has an inner radius of $b$ and a net charge of $+Q$. 

<img src="figures/Spherical.svg"/>

1a. Use Gauss's law to show that there can be no charge on the inner surface of the inner conductor. 

1b. Use Gauss's law to show that the charge on the inner surface of the outer conductor is $+Q$. 

2\. What is the electric field in each of the 5 labeled regions? Region $1.$ is the empty volume inside of the inner conductor, region $2.$ is the volume of the inner conductor, region $3.$ is the empty volume between the conductors, region $4.$ is the volume of the outer conductor, and region $5.$ is the region outside of the outer conductor.

%3\. How much work will it take to move a charge $q_o$ from the outer surface of the inner shell to the inner surface of the outer shell? Said another way, what is the difference in potential energy, $PE_b-PE_a$, for this charge?

3\. What is the potential difference, $V(b)-V(a)$?

4\. Write the capacitance in terms of $\epsilon_o$, $a$, and $b$.

% In the future, remove Q from diagram as some thought it meant +Q was on outer part of outer shell.

**Answer**:

A common error was assuming that $+Q$ was on the outer surface of the outer conductor because of the position of the label on the diagram. As will be shown, this is not possible.

The system is invariant with respect to rotation about any axis. As a result, the charge density on any surface must be uniform and any field must be radial. Any electric field must also be invariant with respect to rotation about any axis.

1a. A Gaussian sphere centered on the origin with a radius $a-t\lt r\lt a$ will have $E=0$ on its surface because its surface is inside a conductor. In this case, $\Phi_E=0$. Thus, $Q_{encl}=0$. All of the charges on the inner conductor must be on its surface, so $Q$ at $r=a-t$ must be zero. As a result, all of the net $-Q$ on the inner conductor must be on its outer surface.

1b. A Gaussian sphere centered on the origin with radius $b \lt r\lt b+t$ will have no charge enclosed, so $\Phi_E=0$. Because the field is radial, the flux integral simplifies to $\Phi_E=E_r 4\pi r^2$. Thus, $\Phi_E=0$ implies that $E_r=0$ and so $Q_{encl}=0$. The total charge enclosed is the charge on the inner conductor and the charge on the inner surface of the outer is $Q_{encl}=0=-Q + q(r=b)$. From this it follows that the charge on the inner surface of the outer conductor is $+Q$.

2.

Region 1: A Gaussian sphere centered on the origin with radius $0 \lt r\lt a-t$ will have no charge enclosed, so $\Phi_E=0$. Because the field is radial, the flux integral simplifies to $\Phi_E=E_r 4\pi r^2$. Thus, $\Phi_E=0$ implies that $E_r=0$.for $r\ne 0$. At $r=0$, $E_r$ must be zero because if it were non-zero, it would not be invariant with respect to rotation about any axis. From this it follows that $\mathbf{E}=0$.

A common error was to state that because no charge is enclosed, $\mathbf{E}$. This statement is not true in general. A Gaussian sphere with a point charge outside of it will have no charge enclosed, but $\mathbf{E}$ is not zero everywhere on the Gaussian surface.

Region 2: Zero because inside a conductor.

Region 3: Due to the symmetry argument, the flux integal similifies to $\Phi_E=E_r4\pi r^2$. The enclosed charge is $-Q$, so $E_r=-Q/4\pi \epsilon_o r^2$ and $\mathbf{E}=-Q\hat{\mathbf{r}}/4\pi \epsilon_o r^2$ because the symmetry argument tells use that $\mathbf{E}$ may only have a radial component.

Region 4: Zero because inside a conductor.

Region 5: $Q_{encl}=0$ and the flux integral simplifies to $E_r4\pi r^2$ due to the symmetry arguments. From this it follows that $E_r=0$ and $\mathbf{E}=0$.

3.

In general,

$\displaystyle V(r)=V(a)-\int_a^r \mathbf{E}\bfcdot d\mathbf{l}$

If we choose $d\mathbf{l}=dr'\hat{\mathbf{r}}$, then

$\displaystyle V(r)=V(a)+\frac{Q}{4\pi}\int_a^r \frac{1}{r'^2}dr'$

and

$\displaystyle V(r)=V(a)+\frac{Q}{4\pi\epsilon_o}\left(\frac{1}{a}-\frac{1}{r}\right)$

When $r=b$, we have

$\displaystyle V(b)-V(a)=\frac{Q}{4\pi\epsilon_o}\left(\frac{1}{a}-\frac{1}{b}\right)$

Note that $V(b)-V(a)$ is positive, which is expected because moving from $a$ to $b$ we are moving against the direction of $\mathbf{E}$.

4.

In this problem, we put a charge of $\pm Q$ on the capacitor surfaces and a potential difference of $V(b)-V(a)$ was the result. Thus,

$\displaystyle C=\frac{Q}{V(b)-V(a)} = \frac{4\pi\epsilon_o}{\frac{1}{a}-\frac{1}{b}}$

----

In preparation for the next problem, note that using this equation, we can re--write

$\displaystyle V(r)=V(a)+\frac{Q}{4\pi\epsilon_o}\left(\frac{1}{a}-\frac{1}{r}\right)$

as

$\displaystyle V(r)=V(a)+\frac{V(b)-V(a)}{\frac{1}{a}-\frac{1}{b}}\left(\frac{1}{a}-\frac{1}{r}\right)$

As a check of the algebra, plugging in $r=a$ gives $V(a)$ and $r=b$ gives $V(b)$.

If we choose to define $V(b)=V_o$ and $V(a)=0$, we have

$\displaystyle V(r)=\frac{V_o}{\frac{1}{a}-\frac{1}{b}}\left(\frac{1}{a}-\frac{1}{r}\right)$

which will be useful for checking the answer in the next problem.

# 1-D Boundary Value Problem

% Copied to Notes

In spherical coordinates, the Laplacian is

$$\nabla^2V = { {1 \over r^{2}}{\partial  \over \partial r}\left(r^{2}{\partial V \over \partial r}\right)+{1 \over r^{2}\sin \theta }{\partial  \over \partial \theta }\left(\sin \theta {\partial V \over \partial \theta }\right)+{1 \over r^{2}\sin ^{2}\theta }{\partial ^{2}V \over \partial \phi ^{2}}}$$

If $V=V(r)$, then this reduces to

$$\nabla^2V = { {1 \over r^{2}}{\partial  \over \partial r}\left(r^{2}{\partial V \over \partial r}\right)}$$

1\. Find $V(r)$ that satisfies

$${ {1 \over r^{2}}{\partial  \over \partial r}\left(r^{2}{\partial V \over \partial r}\right)}=0$$

in terms of $r$ and two unknown constants <strike>a and b</strike>. Follow the steps given [in the notes](boundary_value_problems.html#cylindrical) for the cylindrical problem.

2\. Two concentric spherical conducting shells are connected to a battery such that the inner shell is at a potential of $0$ and the outer shell is at a potential of $V_o$. The inner shell has an outer radius of $a$. The outer shell has an inner radius of $b$. Use your equation from part 1. and these boundary conditions to find $V(r)$ between the conductors in terms of $V_o$, $a$, and $b$.

3\. In section 2.5.3 of Griffiths, the equation for the electric field immediately outside of a conductor is stated to be $\mathbf{E}=(\sigma/\epsilon_o)\hat{\mathbf{n}}$. Use the potential $V(r)$ found in part 2. to find the electric field $\mathbf{E}(r)$ between $a$ and $b$ and then evaluate this electric field at $a$ and $b$. Use these electric fields to find the surface charge densities at $a$ and $b$.

(Hint: To check your answer, use the capacitance equation fround in problem 1.4. to eliminate $V_o$ from the surface charge densities. You should find that the surface charge densities on the inner and outer conductors are $-Q/4\pi a^2$ and $Q/4\pi b^2$, respectively.)

**Answer**:

1\. In spherical coordinates, the Laplacian is 

$\displaystyle \nabla^2V={ {1 \over r^{2}}{\partial  \over \partial r} \left(r^{2}{\partial V \over \partial r}\right) + {1 \over r^{2} \sin \theta }{\partial  \over \partial \theta } \left(\sin \theta {\partial V \over \partial \theta }\right) + {1 \over r^{2} \sin ^{2}\theta }{\partial ^{2}V \over \partial \varphi ^{2}}}$

 Because the system is invariant with rotation by $\phi$ and $\theta$, the potential must be independent of $\theta$ and $\phi$; as a result, the second two terms are zero. Therefore, we need to solve

$\displaystyle \nabla^2V={1 \over r^{2}}{\partial \over \partial r} \left(r^{2}{\partial V \over \partial r}\right)=0$

Becuase $V$ depends only on $r$, we can replace the partial derivative with the total derivative

$\displaystyle \nabla^2V={1 \over r^{2}}{d \over d r} \left(r^{2}{d V \over d r}\right)=0$

To solve the ODE, note that the following must hold

$\displaystyle r^2{dV\over dr} = c_1$

where $C_1$ is a constant.  Direct integration gives

$\displaystyle V(r) = {c_1 \over r} + c_2$

2\. The two unknowns are solved for by using the boundary conditions $V(a)=V_o$ and $V(b)=0$:

$\displaystyle V(a) = 0 = {c_1 \over a} + c_2$

$\displaystyle V(b) = V_o = {c_1 \over b} + c_2$

Solving for $c_1$ and $c_2$ gives

$\displaystyle c_1 = {V_o \over \left({1\over b}-{1\over a}\right)}$

$\displaystyle c_2 = -{{V_o/a}\over{\left({1\over b}-{1\over a}\right)}}$

and subsitution of these constants into $V(r) = {c_1/r} + c_2$ gives

$\displaystyle V(r) = {V_o \over \left({1\over a}-{1\over b}\right)}{\left({1\over a}-{1\over r}\right)}$

As a check of the algebraic steps, plug in $r=a$ and $r=b$ into this equation and verify that the boundary conditions used, $V(a)=V_o$ and $V(b)=0$, are satisfied. Also note that this is the same result obtained in problem 1.4.

3\. The electric field can be found using $\mathbf{E}=-\nabla V$. In spherical coordinates, when $V$ depends only on $r$,

$\displaystyle \boldsymbol{\nabla} V={\partial V \over \partial r} \hat{\mathbf{r}}$

giving

$\displaystyle \mathbf{E}=-{V_o \over \left({1\over a}-{1\over b}\right)}{1\over r^2}\hat{\mathbf{r}}$

This field points outward radially inward as expected given the potential on the outer surface is higher than that on the inner surface.

This field can be written in terms of $Q$ using $C=Q/V_o$ and the equation for capacitance found in problem 1.3:

$\displaystyle C=\frac{4\pi\epsilon_o}{\frac{1}{a}-\frac{1}{b}}$

This gives

$\displaystyle \mathbf{E}=-\frac{Q}{4\pi\epsilon_o}{1 \over r^2}\hat{\mathbf{r}}$

At $r=a$, 

$\displaystyle \mathbf{E}(a)=-\frac{Q/4\pi a^2}{\epsilon_o}\hat{\mathbf{r}}$

This is consistent with the formula $\mathbf{E}=(\sigma/\epsilon_o)\hat{\mathbf{n}}$ because at $r=a$, $\hat{\mathbf{n}}=\hat{\mathbf{r}}$ and $\sigma=-Q/4\pi a^2$.

At $r=b$, 

$\displaystyle \mathbf{E}(a)=-\frac{Q/4\pi b^2}{\epsilon_o}\hat{\mathbf{r}}$

This is consistent with the formula $\mathbf{E}=(\sigma/\epsilon_o)\hat{\mathbf{n}}$ because at $r=b$, $\hat{\mathbf{n}}=-\hat{\mathbf{r}}$ and $\sigma=+Q/4\pi a^2$.

# 2--D Laplacian

% Copied to notes

Laplace's equation in cartesian coordinates when $V=V(x,y)$ is

$$\nabla^2V = \frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} = 0$$

For arbitrary constants $A,B,C,D,$ and $m$ the following four equations satisfy it

1. $V(x,y) = \big(A\cosh mx+B\sinh mx\big)\big(C\cos my+D\sin my\big)$
2. $V(x,y) = \big(A\cos mx+B\sin mx)(C\cosh my+D\sinh my\big)$
3. $V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos my+D\sin my\big)$
4. $V(x,y) = \big(A\cos mx+B\sin mx\big)\big(Ce^{my}+De^{-my}\big)$

1\. Show that equation 1. satisfies $\nabla^2V=0$. Recall that the definitions of the hyperbolic $\sin$ and $\cos$ are $\sinh z = (e^{mz}-e^{-mz})/2$ and $\cosh z = (e^{mz}+e^{-mz})/2$.

2\. Show that equation 1. is related to equation 3. Do this by labeling the constants in equation 3. with primes and finding the constants in equation 1. in terms of the primed constants.

3\. Show that equation 2. is related to equation 4. Do this by labeling the constants in equation 4. with primes and finding the constants in equation 2. in terms of the primed constants.

4\. Show that equation 1. can be derived from equation 2. by using Euler's identity $e^{iz}=\cos z+i\sin z$ and the definitions of the hyperbolic $\sin$ and $\cos$. Do this by labeling the constants in equation 2. with primes and finding the constants in equation 1. in terms of primed constants.

**Answer**:

2\. Form 3. with primed constants is

$V(x,y) = \big(A'e^{m'x}+B'e^{-m'x})(C'\cos my+D'\sin m'y\big)$

Using

$\cosh mx=(1/2)(e^{mx}+e^{-mx})$ and $\sinh mx=(1/2)(e^{mx}-e^{-mx})$

we can write

$e^{m'x}=\cosh m'x+\sinh m'x$ and $e^{-m'x}=\cosh m'x-\sinh m'x$

Inserting these into the equation for $V(x,y)$ gives

$\displaystyle V(x,y) = \Big((A'+B')\cosh m'x+(A'-B')\sinh m'x\Big)(C'\cos my+D'\sin m'y\big)$

and based on comparison with

$V(x,y) = \big(A\cosh mx+B\sinh mx\big)\big(C\cos my+D\sin my\big)$

we conclude 

$A=A'+B'$, $B=A'-B'$, $C=C'$, $D=D'$, and $m=m'$.

As a check, if $A'=B'=1$ and $m'=1$, form 3. is

$V(x,y) = \big(e^{x}+e^{-x})(C'\cos y+D'\sin y\big)=(2\cosh x)(C'\cos y+D'\sin y)$

With $A'=B'=1$, $A=2$, and $B=0$, so form 1. is

$V(x,y) = (2\cosh mx)(C\cos my+D\sin my)$

3\.

$A=A'$, $B=B'$, $C=C'+D'$, $D=C'-D'$, and $m=m'$.

4\.

Euler's identity is

$e^{iz}=\cos z+i\sin z$

Replacing $z$ with $-z$ gives

$e^{-iz}=\cos (-z)+i\sin (-z) = \cos z - i\sin z$

Adding the last two equations gives $\displaystyle \cos z = \frac{e^{iz}+e^{-iz}}{2}$. Subtracting gives $\displaystyle \sin z = \frac{e^{iz}-e^{-iz}}{2i}$.

Comparison of

$\displaystyle \cos z = \frac{e^{iz}+e^{-iz}}{2}$ with $\displaystyle \cosh z=\frac{e^{z}+e^{-z}}{2}$ gives

$\cos z=\cosh iz$ and $\cosh z=\cos (iz)$

Comparison of $\displaystyle \sin z = \frac{e^{iz}-e^{-iz}}{2i}$ with $\displaystyle \sinh z=\frac{e^{z}-e^{-z}}{2}$ gives

$\sin z=-i\sinh i z$ and $\sinh z=-i\sin (iz)$.

Form 2. with primed constants is 

$V(x,y) = \big(A'\cos m'x+B'\sin m'x)(C'\cosh m'y+D'\sinh m'y\big)$

Using the above identities, this can be written as

$V(x,y) = \big(A'\cosh m'ix-iB'\sinh im'x\big)\big(C'\cos (im'y)-iD'\sin (im'y)\big)$

From comparison with form 1.

$V(x,y) = \big(A\cosh mx+B\sinh mx\big)\big(C\cos my+D\sin my\big)$

we conclude

$A=A'$, $B=-iB'$, $C=C'$, $D=-iD'$, and $m=im'$.

or
$A
=A'$, $B=+iB'$, $C=C'$, $D=+iD'$, and $m=-im'$.


