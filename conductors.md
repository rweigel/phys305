# Insulators vs. conductors
\label{section:insulators_vs_conductors}

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Insulators versus conductors]
1. Describe the difference between what happens to a net charge placed on an insulator versus a conductor. 
\ifsolutions
\\
\\
{\bf Answer}: Charge placed on an insulator will not move. Charge placed on a conductor will quickly spread out on its surface in a configuration that makes the electric field zero everywhere inside of it. Unlike a conducting sphere, an arbitrarily shaped conductor will have a non-uniform charge density on its surface. The video \url{https://youtu.be/22hdENUMry0} shows several experiments on a conductor and an insulator that clearly demonstrate their behavior when a they are given a net charge in a certain location.
\\
\\
\else
\\[1.5cm]
\fi
2. What happens to the charges in an insulator that is placed in an electric field? Draw an insulator in an electric field.
\ifsolutions
\\
\\
{\bf Answer}: The molecules within the insulator can't move, but they will align with the field. Figure 24.19 in your book provides a nice illustration of this since an insulator in an electric field is a dialectric which we will get to in that chapter. 
\\
\\
\else
\\[1.5cm]
\fi
3. What happens to the charges in a conductor that is placed in an electric field? Draw a conductor in an electric field.
\ifsolutions
\\
\\
{\bf Answer}: For a conductor in an electric field the charges will separate with the positive charges moving as far away from the negative charges as they can along the field lines. See Figure 22.27 in the textbook for an illustration.
\else\\[1.5cm]
\fi
\end{tcolorbox}

# Gauss's law and conductors
\label{gausss_law_and_conductors}

Despite the complexity of conductors over insulators noted previously, Gauss's law can still be used for  some types of conductor problems.

Conductors have two properties:
\begin{enumerate}
    \item all excess charge is on the surface, and
    \item the electric field inside is zero.
\end{enumerate}

Suppose a charge $Q$ is arbitrarily distributed within a solid spherical conductor. Independent of where this charge was placed initially, the charge will quickly move to the surface of the sphere due to self-repulsion. We can show that as a result, items 1. and 2. are related via Gauss's law.

In the following figure, the cross section of a solid spherical conductor is shown along with a spherical Gaussian surface.

\input{Gauss/figures/Spherical_Conductor}

Gauss's law in its most general form is

\begin{equation}
\oint \mathbf{E}\cdot d\mathbf{A}=\frac{Q_{encl}}{\epsilon_o}
\end{equation}

Due to 1., the electric field on the Gaussian surface is zero, so the integral is zero

\begin{equation}
\oint 0dA=0=\frac{Q_{encl}}{\epsilon_o}\quad\Rightarrow\quad Q_{encl} = 0
\end{equation}

We can conclude that there is no charge for any $r$ smaller than the radius of the sphere. In this case, we derived 2. from 1. and Gauss's law.

Next, consider a solid conductor with an empty spherical cavity. 

\input{Gauss/figures/Spherical_Conductor_With_Cavity}

As before, suppose a charge $Q$ is arbitrarily distributed on the conductor. Conductor property 1. only tells us that a total charge of $Q$ will reside on the surface. But in this case, there is also an inner surface. Gauss's law can be used to determine how much charge is on each surface. First, split $Q$ into charge on the inner ($Q_i$) and outer ($Q_o$) surface

$$Q=Q_{i} + Q_o$$

Next, consider a spherical Gaussian surface that is inside the conductor. In this case, $Q_{encl}=Q_i$. As before, conductor property 1. tells us that the electric field is zero on the Gaussian surface because it is fully inside the conductor. From Gauss's law,
\begin{equation}
\oint \mathbf{E}\cdot d\mathbf{A}=\oint 0dA=0=\frac{Q_i}{\epsilon_o}\,,
\end{equation}

so $Q_i=0$. Plugging this into 

$$Q=Q_i + Q_o$$

gives $Q_o=Q$. That is, all of the charge placed on the conductor must be on the outer surface.

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,height fill,title=Problem 5.1 - Conductor with a cavity]

A spherical conductor has a spherical cavity with the same center point. At the center of the cavity there is a point charge of $q$.

\input{Gauss/figures/Point_Charge_in_Spherical_Conductor}

If a total charge of $Q$ is placed on the conductor, what is

1. $Q_i$, the total charge on the inner surface of the conductor?

\ifsolutions
{\bf Answer}: Consider a Gaussian sphere centered on $q$ and with radius such that its surface is inside of the conductor. The electric field inside of a conductor is zero and so the electric field on the Gaussian surface is zero as is the left-hand side of Equation~\ref{eqn:simple2}:
$
0A = \frac{Q_{encl}}{\epsilon_o}
$
The enclosed charge can be split into the charge at the origin and the charge on the inner surface:
$
0 = \frac{Q_i + q}{\epsilon_o}
$
As a result, $Q_i = -q$.
\else
\\[2cm]
\fi

2. $Q_o$, the total charge on the outer surface of the conductor?

\ifsolutions
{\bf Answer}: If the total charge on the conductor is $Q$ and $Q_i$ is on the inner surface, then $Q_o=Q-Q_i=Q+q$.
\else
\\[2cm]
\fi



3. If the cavity has a radius of $a$ and the conductor has a radius of $b$, what is the surface charge density on the inner surface of the conductor?

\ifsolutions
{\bf Answer}: $\sigma_i = \frac{Q_i}{4\pi a^2} = -\frac{q}{4\pi a^2}$
\else
\\[2cm]
\fi

4. The outer surface of the conductor?

\ifsolutions
{\bf Answer}: $\sigma_o = \frac{Q_o}{4\pi b^2} = \frac{Q+q}{4\pi b^2}$
\else
\\[2cm]
\fi

5. Assume that the charges on the inner and outer surface are uniformly distributed. Draw the electric field lines on the diagram. (You may want to review the rules for field lines in the Field Lines tutorial.)

\ifsolutions
{\bf Answer}:

\scalebox{0.5}{
    \input{Gauss/figures/Point_Charge_in_Spherical_Conductor_Field_Lines}
}
\else
\fi
\end{tcolorbox}

\end{document}

= Conductors =

== Notes ==

* A conductor in isolation with a net charge will have all excess charge on its surface. 
* A conductor in an external electric field that started with a net charge will have all excess charge on its surface. 
* A conductor in an external electric field that started with zero net charge (neutral) will have all excess charge on its surface.

In general, the surface charge density on a conductor is not uniform. (Regions with high curvature, especially sharp angles, tend to have a higher charge density.)

The surface charge density is not in general uniform; it is configured in such a way as to make the total field, due to the external field + the field due to the surface charges, equal to zero. Computing the exact charge density usually requires solving a boundary value problem.

[https://link.springer.com/chapter/10.1007/978-3-319-40871-2_2 Conductors in Equilibrium] from [https://link.springer.com/book/10.1007/978-3-319-40871-2 A Course in Classical Physics 3 — Electromagnetism]

== Surface Charge Density ==

The surface charge density is not in general uniform on a conductor - give an example of a situation for which it will be uniform.

== Surface Charge ==

The magnitude of the electric field due to an infinite non-conducting sheet with charge density \(\sigma\) is \(\sigma/(2\epsilon_0)\).

The electric field outside of an infinite conducting sheet with charge density \(\sigma\) is \(\sigma/\epsilon_0\). (And this is also true just outside the surface of any conductor.)

Explain the factor-of-two difference.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|

The short answer is that the equation for a sheet of charge is for the electric field '''due to the sheet'''. In the equation for the electric field outside of a conductor, the electric field is that '''due to everything''', which includes surface charges on conductors and external electric fields. So perhaps it is not surprising that the equations are different.

If this was not clear in class, I suggest that you draw out what I say in words below and see if you follow the logic. 

Note that a "sheet of charge" is the same thing as a "non-conducting sheet with a surface charge density". "Sheet of charge" is ambiguous because one could be talking about a bunch of charges glued to a non-conducting sheet or a bunch of charges on the surface of a conducting sheet, so "sheet of charge" is only used when we are not talking about conductors because it is shorter to write. 

In class I did this:
# Considered a sheet of charge and showed using Gauss' Law that the electric field points away from it and has a magnitude of \(\sigma/(2\epsilon_0)\).
# Considered a conducting sheet placed in an external electric field. One side of the sheet would have a charge density of \(+\sigma\) and the other side \(-\sigma\) in order to create an induced electric field that cancels the external electric field in the region inside the conductor. I then used Gauss' Law with one end of a Gaussian pillbox inside the conductor and the other side outside of the conductor. I found that it gave an electric field outside of the conductor of \(\sigma/\epsilon_0\). Someone asked what would happen if the Gaussian pillbox had both ends outside of the conductor; In that case, the charge enclosed would be zero and one would only be able to conclude that \(E_{left}=E_{right}\) and that the electric field on the left and right pointed in the same direction (corresponding to the direction of the external electric field).
# Considered a conducting sheet with a net charge placed on it (and no external electric field). In that case, half the excess charge would end up on one side of the sheet and half would be on the other. Call the excess charge density on each side \(+\sigma\); both sides need to have positive and equal charge densities in order for their fields to cancel each other inside the conductor. Using Gauss' Law with one end of a Gaussian pillbox inside the conductor, I found the electric field outside of the conductor to be \(\sigma/\epsilon_0\). When the Gaussian pillbox has both ends outside of the conductor, Gauss' Law gives, that the electric field magnitude outside the conductor is \(\sigma/\epsilon_0\).

Another way to look at this: Think of the surface charge on a conducting sheet as creating an electric field of (\sigma/(2\epsilon_0)\), just like that of a non-conducting sheet. It is just a collection of charges on a plane, so the electric field that it creates is the same as that of a sheet of charge. Its electric field points outward on both sides of the sheet. On the side of the sheet corresponding to the inside of the conductor, there must be another electric field due to other sources that cancels it (and has a magnitude of \(\sigma/\epsilon_0\). Outside of the conductor, this "other source" electric field adds to the electric field created by the surface charge on the conductor to create a net electric field of \(\sigma/(2\epsilon_0) + \sigma/(2\epsilon_0) = \sigma/\epsilon_0\). '''Draw this out!'''
|}

== Surface Charge ==

# A net charge is placed on a solid conducting sphere. 
# A net charge is placed on a solid conducting cube.
# A charge is uniformly distributed on the surface of a non-conducting shell. 
# A charge is uniformly distributed on the surface of a non-conducting hollow box. 

For case 1. and 2., is the surface charge density uniform? 

For each of the four cases, is the electric field inside zero everywhere inside the object or non-zero?

== Surface Charge ==

# A net charge is placed on a conducting shell.
# A net charge is placed on a conducting hollow box.
# A charge is uniformly distributed on the surface of a non-conducting shell. 
# A charge is uniformly distributed on the surface of a non-conducting hollow box. 

For case 1. and 2., is the surface charge density uniform?

For each of the four cases, is the electric field inside zero everywhere or non-zero?

== Dented Sphere ==

Write your answer on this sheet of paper. Justify all answers.

A non-conducting spherical shell is covered with charge uniformly on its surface. It is then dented. 

<blockquote>"The electric field near the center of the shell is zero because a Gaussian sphere centered at the origin and fully inside of the shell will have zero enclosed charge."</blockquote>

* True
* False

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

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Nope. Gauss' Law is generally only useful for computing \(\mathbf{E}\) when it can be pulled out of the integral. Here we don't have a symmetry argument that would allow this. To compute the electric field, you would need to do an integral like the ones done for continuous charge distributions. And it would be complicated.
|}

If the shell magically becomes conducting after it is dented, what is the electric field that would be measured at 

* the center of the shell?
*# Zero
*# Non-zero

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Zero. The electric field inside a conductor is zero. This is why people wear tin hats. The electric field inside the hat is almost zero and so electromagnetic waves won't hit the brain. (One would need to be fully enclosed in tin foil to make the electric field inside zero. So to fully protect your brain you would need to remove your head.
|}

* inside of the shell in general?
*# Zero
*# Non-zero

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Zero. Same argument as above.
|}

== Sphere with Cavity ==

A conducting sphere of radius \(2R\) centered on the origin has a spherical cavity of radius \(R\) that is also centered on the origin.

If a charge of \(+q\) is at the origin, what is the net charge on 
# the outer surface and
# inner surface of the sphere.

Justify your answers.

Plot the electric field as a function of distance from the origin.

== Cube with Cavity ==

A conducting cube with sides of length \(2L\) centered on the origin has a cubical cavity with side length \(L\) that is also centered on the origin.

If a charge of \(+q\) is at the origin, what is the net charge on 
# the outer surface and
# inner surface of the cube.

Justify your answers.

== Sphere with Cavity ==

A conducting sphere of radius \(3R\) centered on the origin has a spherical cavity of radius \(R\) that is centered on \((x,y,z)=(R,0,0)\).

If a charge of \(+q\) is at \((x,y,z)=(R,0,0)\), what is the net charge on 

# the outer surface and
# inner surface of the sphere.

Justify your answers.

== Cube with Cavity ==

A conducting cube with sides of length \(3L\) centered on the origin has a cubical cavity with side length \(L\) that is centered on \((x,y,z)=(L,0,0)\).

If a charge of \(+q\) is at the origin, what is the net charge on 
# the outer surface and
# inner surface of the cube.

Justify your answers.

== Infinite Sheets ==

An infinite non-conducting sheet in the \(x=d\) plane has a charge density of \(-\sigma_0\); An infinite non-conducting sheet in the \(x=-d\) plane has a charge density of \(+\sigma_0\), where \(\sigma_0>0\). (That is, the sheet in the \(x=d\) plane is negatively charged and the sheet in the \(x=-d\) plane is positively charged.)

=== ===
Label key points on your plots in terms of \(\sigma_0, d\), and \(\epsilon_0\). A diagram is given on the board.

# Plot the electric field as a function of \(x\) from \(x=-2d\) to \(x=+2d\). <span style="background-color:yellow">+3</span>
# Plot the electric potential as a function of \(x\) from \(x=-2d\) to \(x=+2d\). Set the electric potential to zero at \(x=0\). <span style="background-color:yellow">+3</span>

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Each sheet produces an electric field with magnitude \(\sigma_o/(2\epsilon_0)\). The direction of the electric field is outwards for a positive sheet and inwards for a negative sheet. The electric field does not depend on distance for an infinite sheet.

(Someone noted that they expected the electric field to decrease with distance from the sheet. This seems reasonable because, in reality, there is no such thing as an infinite sheet; if you get far enough away, say, any finite by large sheet will look like a point charge. But for \(-2d\le x \le 2d\), we can say it is constant and this is what the formula \(\sigma_o/(2\epsilon_0)\) claims. The lines on your graph for the electric field won't be strictly horizontal in reality becuase an infinite sheet is not possible to create. But they will be so near horizontal that you would not be able to tell.)

Read superscript "-" as "just less than" and "+" as "just greater than".

'''1. Answer'''
* \(x=-2d\) to \(x=-d^-\): \(\mathbf{E}=0\). The electric fields are equal in magnitude and opposite in direction.
* \(x=-d^+\) to \(x=+d^-\): \(\mathbf{E}=\sigma_o\hat{\mathbf{x}}/\epsilon_0\). The electric fields are equal in magnitude and in the same direction.
* \(x=d^+\) to \(x=+2d\): \(\mathbf{E}=0\). The electric fields are equal in magnitude and opposite in direction.

I'll get the answer for \(V\) in two ways. Based on a diagram of the electric field between the sheets, I expect the potential to only change between the sheets. This is the only location where there is an electric field and so moving a test charge in this region would take work. As I move from the positively charged sheet to the negatively charged sheet, the electric potential should decrease. The electric field is constant and so \(-\nabla V=-\hat{\mathbf{x}}\partial V/\partial x\) must be a constant. This is satisfied if \(V\) is linear in \(x\). At this point, we can just guess \(V\) so that it gives the correct electric field using \(\mathbf{E}=-\nabla V\) and has the property that it is continuous.

'''2. Answer'''
* \(x=-2d\) to \(x=-d^-\):  \(V=\sigma_0d/\epsilon_0\).
* \(x=-d^+\) to \(x=+d^-\): \(V=-\sigma_0x/\epsilon_0\).
* \(x=d^+\) to \(x=+2d\): \(V=-\sigma_0d/\epsilon_0\).

Check: These all give the correct electric field using \(\mathbf{E}=-\nabla V\).

The second way of answering this is to use

$$V(b)-V(a)=-\int_a^b\mathbf{E}\cdot d\hat{\mathbf{l}}$$

\(d\hat{\mathbf{l}} = \hat{\mathbf{x}}dl\) and between the sheets \(\mathbf{E}=\sigma_o\hat{\mathbf{x}}/\epsilon_0\) so

$$V(b)-V(a)=-\int_a^b\sigma_o/\epsilon_0\hat{\mathbf{x}}\cdot\hat{\mathbf{x}}dx=-\sigma_o/\epsilon_0\int_a^b dx$$

In the last step, I have changed the integration variable from \(x\) to \(x'\) so that I can use \(x\) in my integration limits. Starting at \(x=0\) and integrating to some point \(x\) gives

$$V(x)-V(0) = -\sigma_o/\epsilon_0\int_0^x dx$$

Giving 

$$V(x) = -\sigma_ox/\epsilon_0$$

The electric potential will be continuous, so plug in values of \(x\pm d\) into this equation to get the potentials for \(x>d\) and \(x<d\), respectively.
|}

=== ===
Label key points on your plots in terms of \(\sigma_0, d,\epsilon_0\), and \(t\).

An uncharged and neutral infinite conducting sheet with thickness \(t\) is placed in the \(x=0\) plane between the two non-conducting sheets. 

# Plot the electric field as a function of \(x\) from \(x=-2d\) to \(x=+2d\). <span style="background-color:yellow">+3</span>
# Plot the electric potential as a function of \(x\) from \(x=-2d\) to \(x=+2d\). Set the electric potential to zero at \(x=0\). <span style="background-color:yellow">+3</span>
# What is the surface charge density on
## the left side of the conducting sheet?; <span style="background-color:yellow">+2</span>
## the right side of the conducting sheet? <span style="background-color:yellow">+2</span>

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
# Electric field plot will be the same as part 1. except it will be zero for \(-t/2<x<t/2\).
# Electric potential plot will be the same shape as part 1. except it will be zero for \(-t/2<x<t/2\) and \(V(x)=-\sigma_0(x+t/2)/\epsilon_0\) for \(-d^+<x<-t/2\) and \(V(x)=-\sigma_0(x-t/2)/\epsilon_0\) for \(t/2<x<d^-\). (Slope is same, but intercept not the same on both sides).
#
## \(-\sigma_0\)
## \(+\sigma_0\)
|}

== Infinite Sheets ==

An infinite non-conducting sheet is in the \(x=d\) plane and has a charge density of \(\sigma_0\), where \(\sigma_0>0\).

# Plot the electric field as a function of \(x\) from \(x=-d\) to \(x=+2d\). Add appropriate axis labels.
# Plot the electric potential as a function of \(x\) from \(x=-d\) to \(x=+2d\). Add appropriate axis labels and set the electric potential to zero at \(x=0\).

An uncharged and neutral infinite conducting sheet with thickness \(t<d/2\) is placed in the \(x=0\) plane (parallel to the non-conducting sheet). 

# Plot the electric field as a function of \(x\) from \(x=-d\) to \(x=+2d\). Add appropriate axis labels.
# Plot the electric potential as a function of \(x\) from \(x=-d\) to \(x=+2d\). Add appropriate axis labels and set the electric potential to zero at \(x=0\).
# What is the surface charge density on
## the left side of the conducting sheet?;
## the right side of the conducting sheet?

== Infinite Sheets ==

Two infinite non-conducting sheets are in the  \(x=\pm d\) plane and have charge densities of \(\pm \sigma_0\), respectively, where \(\sigma_0>0\).

# Plot the electric field as a function of \(x\) from \(x=-2d\) to \(x=+2d\). Add appropriate axis labels.
# Plot the electric potential as a function of \(x\) from \(x=-2d\) to \(x=+2d\). Add appropriate axis labels and set the electric potential to zero at \(x=0\).

An uncharged and neutral infinite conducting sheet with thickness \(t<d/2\) is placed in the \(x=0\) plane (parallel to and between the two non-conducting sheets). 

# Plot the electric field as a function of \(x\) from \(x=-2d\) to \(x=+2d\). Add appropriate axis labels.
# Plot the electric potential as a function of \(x\) from \(x=-2d\) to \(x=+2d\). Add appropriate axis labels and set the electric potential to zero at \(x=0\).
# What is the surface charge density on
## the left side of the conducting sheet?;
## the right side of the conducting sheet?

== Infinite Sheets ==

An uncharged and neutral infinite conducting sheet is placed between two infinite sheets of charge. All sheets are parallel to each other.

The sheet of charge on the right has a charge density of \(\sigma_0\) and the sheet of charge on the left has a charge density of -\(\sigma_0\), where \(\sigma_0>0\).

# Find the charge density on the surfaces of the conducting sheet.
# Find the electric field everywhere.

Use diagrams as needed.
{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
This is a simplified version of the homework problem in which the sheets had different charge densities.  The homework problem was an extension of the example that I did in class in which there was no second sheet of charge.
# \(\sigma\) on right face of the conductor is \(-\sigma_0\).  On the left face of the conductor, it is \(\sigma_0\). (Note: Earlier version of answer had signs reversed, which does not make sense.)
# To the left and right of the sheets of charge, the electric field is zero.  To see this, draw the electric field direction for each charged surface in these regions.  There is exact cancellation.  (Because these are infinite sheets, the electric field for each charged surface does not depend on the distance from it.) Between the sheets, except in the conductor, the electric field is \(-\hat{\mathbf{x}}\sigma_o/\epsilon_0\).  In the conductor, the electric field is zero.
|}

== Infinite Sheets ==

Two infinite non-conducting sheets have their normals parallel to the \(x\)-axis.  The sheet of charge on the right is in the \(x=d\) plane and has a charge density of \(\sigma_R\); the sheet of charge on the left is in the \(x=-d\) plane and has a charge density of -\(\sigma_R\), where \(\sigma_R>0\) and  \(\sigma_L>0\).  An uncharged (neutral) infinite conducting sheet with thickness \(t<d/2\) is centered at \(x=0\) (parallel to and between the two non-conducting sheets). 

# Plot the electric field as a function of \(x\) from \(x=-2d\) to \(x=+2d\). Add appropriate axis labels.
# Plot the electric potential as a function of \(x\) from \(x=-2d\) to \(x=+2d\). Add appropriate axis labels and set the electric potential to zero at \(x=0\).
# What is the surface charge density on
## the left side of the conducting sheet?;
## the right side of the conducting sheet?

== Conceptual ==

# Explain why the electric field inside of a conductor is zero. <span style="background-color:yellow">+1 for correct answer.</span>
# Explain why the charge density inside of a conductor is zero. <span style="background-color:yellow">+1 for correct answer.</span>

<div style="background-color:#E8E8E8">
# The gives an explanation for this and I gave several explanations for this in class.  Either answer was accepted. '''Several students stated that the surface charge density on a conductor is constant but still received credit because another part of their answer was correct and the statement was not needed. The surface charge on an arbitrary conductor is not constant. It will vary with position and locations with high curvature will have a higher charge density.'''  Recall that my explanation was to suppose a conductor had a non-zero electric field that persisted.  This electric field would drive a current.  This would mean that excess charge placed inside of a conductor would lead to non-zero current for a long time, in violation of conservation of energy (current in a conductor would create heat).  The technical explanation of this is that inside a conductor, any excess charge at a given location will decay exponentially with a time constant of \(\sigma\epsilon_0\), where \(\sigma\) is the conductivity.  This decay constant is on the order of \(10^{-16}\) seconds for typical conductors.  So the question would have been more technically correct if it said "why the electric field inside of a conductor is zero ... eventually".  But practically, because of this time constant, it is reasonable to omit the "... eventually".
# The easiest argument is using \(\nabla\cdot \mathbf{E} = \rho/\epsilon_0\).  If \(\mathbf{E}=0\), then \(\rho=0\).
</div>
