# Introduction

Capacitance is a property of any two isolated conductors; conductors are isolated when there can be no flow of charges betwee them. Capacitance is a quantity that can be used to answer any of these three questions.

1. If I put $+Q$ on one of the conductors and $-Q$ on the other, what will be the difference in electric potential, $\Delta V$, between the conductors?
2. If I put $+Q$ on one of the conductors and $-Q$ on the other, how much energy will it take to move a test charge $q_o$ from one conductor to the other?
3. If I have a battery with an electric potential difference $\Delta V$ between its terminals and I connect each terminal to different conductors, how much charge will appear on the conducting surfaces? As will be discussed, due to charge conservation, an equal and opposite amount of charge will appear on the conductors.

The reason that we can answer these questions is that the amount of positive charge $Q$ and potential difference $\Delta V$ are related by

$$C=\frac{Q}{|\Delta V|}$$

where $C$ is called capacitance and represents a capacity to hold charge. Said another way, when connected to a 1 $V$ battery, the capacitor that has more capacitance will have more charge appear on each of its conductors.

This italicized $C$ in $C=Q/|\Delta V|$ is different from an un-italicised C, which is the SI abbreviation for a Coulomb. (In E&M, we often run out of symbols and make confusing notation choices; another example is that electric potential is denoted by $V$ and the units of electric potential are V for Volts.)

The SI units of capacitance are Coulombs/Volt; this ratio is defined to be a Farad (F).

By definition, capacitance is always a positive number.

Various different forms of the equation for capacitance are used, for example $C={Q}/{V}$, $C={Q}/{\Delta V}$, $C={Q}/{|\Delta V|}$, and $C=|Q|/|\Delta V|$. 

* In the equation $C={Q}/{V}$, it is implied that $V$ means the difference in potential between the positively charged conductor and the negatively charged conductor $V \equiv V_{+} - V_{-}$ (as opposed to $V \equiv V_{-} - V_{+}$). In this case, $V$ is positive.

* In the equation $C={Q}/{\Delta V}$, it is implied that $\Delta V \equiv V_{+} - V_{-}$ (as opposed to $\Delta V \equiv V_{-} - V_{+}$). In this case, $V$ is positive.

* In the equation $C={Q}/{|\Delta V|}$, the absolute value of the potential difference between the conductors is taken. The reason for this is that $V$ and $\Delta V$ alone is ambiguous -- they could mean $V_{+} - V_{-}$ or $V_{-}-V_{+}$. With the absolute value, it does not matter which is used -- the computed capacitance will be the same.

# Common Capacitors

The only ingredients needed to form a capacitor are two isolated conductors. The two conductors do not need to have the same shape and size. Several types of capacitors are shown in the following diagram.

%\begin{center}
%\input{Capacitance/figures/Capacitor_Examples}
%\end{center}

The capacitance of two conductors depends on how far they are separated and their shape (physical dimensions). As an example, the capacitance of a parallel plate capacitor (b.) depends on the plate area and their separation distance $d$. The capacitance of concentric spherical conducting shells (d.) depends on the outer radius of the inner shell and the inner radius of the outer shell.

# Capacitor Applications

There are two general uses of capacitors, mechanical and electrical.

## Mechanical

* Conversion of mechanical energy to electrical energy

    In the diagram, when the key is pressed down the separation between the plates decreases and the voltmeter registers an increase in the voltage.

* Conversion of electrical energy to mechanical

    If you change the separation distance between the conductors that form a capacitor, the capacitance will change. If the charge on the conductors is constant, $C={Q}/{|\Delta V|}$ implies that there will be change in potential.

## Electrical

* Conversion of electrical energy to thermal energy

    Suppose that you charge a capacitor using a battery. If you disconnect the battery, you will have energy stored in the capacitor.

    If you later connect a resistor between two charged surfaces, current will flow and the wire will heat up. In this case, the electrical energy has been converted into thermal energy (and thermal energy involves the motion of particles).

* Modifying the characteristic of a waveform

# Calculating Capacitance

To measure capacitance, one needs to place $-Q$ on one conductor and $+Q$ on the other and then measure the potential difference $\Delta V$ between the conductors. The capacitance is then $Q/|\Delta V|$. An alternative is to connect each initially uncharged conductor the terminals of a battery and then (somehow) measure the amount of charge that appears on either one of the conductors. By conservation of charge, the amount of charge that appears on one conductor will be equal and opposite to what appears on the other.

In general computing capacitance requires solving a partial differential equation either analytically or numerically. The reason is that if we charge up a capacitor, we need to know the electric field that results, and this requires knowledge of how the charges are distributed on the two conductors that form the capacitor.

However, there are a few capacitors for which a simple method can be used to compute the capacitance. These capacitors have a geometry such that a symmetry argument and Gauss's law can be used to determine the distribution of charges and the electric field between the two conductors that form the capacitor. In this case, we can find the potential difference by integrating the electric field from one conductor to the other to find the potential difference $\Delta V$. The capacitance is then $Q/|\Delta V|$.

In the Gauss's law tutorial, the electric field was found for certain types of charge distributions such as charges uniformly distributed on a plane, a cylindrical shell, and a spherical shell. In this tutorial, we'll use Gauss's law to find the electric field between conductors that have these shapes. The electric field will then be used to compute the potential difference between the conductors and this potential difference will be used to compute the capacitance.

The general technique for computing capacitance when Gauss's law applies is:

1. Place an equal an opposite amount of charge on the conductors.
2. Use Gauss's law to compute the electric field between the conductors.
3. Use $\Delta V=-\int \mathbf{E}\cdot d\mathbf{l}$ to find the potential difference between the conductors. The integration is along any path that starts on the negatively charged surface and ends on the positively charged surface. Although any path can be used, there will be a path for evaluation of the integral is easy.
4. Compute $C$ using the definition $C = Q/|\Delta V|$.

%In the previous tutorial, $\Delta V$ was computed between points in a region where there was a constant electric field or a region where there was an electric field due to a single charge.

%If there are multiple charges, $\Delta V$ could still be computed by considering the potential due to each charge individually and then summing the results.

%In general, it is difficult to compute the electric field between two charged conductors. To compute the total $\Delta V$, one needs to compute the $\Delta V$ due to each and every charge on the conductors.

%It would seem that to compute $\Delta V$ for the diagram shown, we would need to know the position of the charges on the surface and then find the $\Delta V$ due to each charge and then sum the result.

\newpage

## Example

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=blue!50!blue,colback=white,title=Example 2.1,height fill]

An equal and opposite amount of charge is placed on two conducting and parallel plates as shown on the left. On the right, a side view of the plates is shown. The area of the plates, $A=lw$, is much larger than shown such that the width, $w$, and height, $h$, are both much larger than the separation distance, $d$.

\input{Capacitance/figures/Parallel_Plates_Example}

1. How will the charges distribute on each of the plates? That is, how much charge is on each of the four faces of area $A=lw$? Assume that no charge appears on the other (narrow) faces of the plates, which have a much smaller area. \\

2. What is the electric field in each region - outside of the plates, inside the conductors, and between the plates? (Hint: Use the equation for the field outside of a large and uniformly charged sheet and account for the field due to the charges on the surface of each plate.) \\

3a. How much work would it take to move a charge $q_o$ from the left plate to the right plate (i.e., the distance $d$ shown)? Said another way, what is the difference in electric potential energy, $U_r-U_l$, between the right and left plate? \\

3b. How much work does it take to move a charge $q_o$ from the outer face of a plate to the inner face of the same plate? (Hint: What is the electric field inside of the plates?)

4a. What is the electric potential difference, $V_{r}-V_{l}$, between the left and right plate? \\

4b. What is the difference in electric potential between the inner and outer faces of one of the plates? \\

5a. Write the capacitance in terms of $\epsilon_o$, $A$, and $d$. \\

5b. Explain why the thickness of the plates does not appear in the equation for capacitance.\\
\vspace{2 cm}
%6. Plot $E(x)$ and $V(x)$. Use $V(0)=0$.

%\vspace{-1.5em}
%\begin{center}\rule{2cm}{0.4pt}\end{center}
%\vspace{-1em}


{\bf Answers:}

1. How will the charges distribute on each of the plates? That is, how much charge is on each of the four faces of area $A=lw$? Assume that no charge appears on the other (narrow) faces of the plate, which have a much smaller area.

All of the negative charges will spread themselves out over the right face of the left plate. All of the positive charges will spread themselves out over the left face of the right plate. This configuration produces zero electric field inside both conductors as expected by Gauss's Law. Any other configuration of charges will lead to a non-zero electric field inside the conductors.

2. What is the electric field in each of the regions (Hint: Use the equation for the field outside of a large and uniformly charged sheet and account for the field due to the charges on the surface of each plate.)?

\input{Capacitance/figures/Parallel_Plates_Example_Answer}

%\scalebox{0.75}{
%}

Each of the inner faces looks like a large, infinitely thin, sheet of charge. The electric field of a sheet of charge has a magnitude of $\sigma/2\epsilon_o$. You can show this using Gauss's Law. The direction of the electric field due to the charges on each plate for each region is shown in the diagram. In all regions except for 3., the total field is zero, so $\mathbf{E}_1=\mathbf{E}_2=\mathbf{E}_4=\mathbf{E}_5=0$. The total electric field between the plates is to the left and is twice the field from a single large sheet of charge:

$$\mathbf{E}_3=-2\frac{\sigma}{2\epsilon_0}\ihat=-\frac{Q}{A\epsilon_o}\ihat$$

3a. How much work would it take to move a charge $q_o$ from the left plate to the right plate (i.e., the distance $d$ shown)? Said another way, what is the difference in electric potential energy, $U_r-U_l$, between the right and left plate?

From the previous tutorial, the work required to move a charge in a constant electric field is $W=\pm |\mathbf{F}|L$. The magnitude of the force on a test charge between the plates is $q_oE$. The force on the test charge is to the left and so it will take positive work to move it to the right. The work is then:

$$W=+q_oEd=\frac{q_oQd}{A\epsilon_o}$$

The change in potential energy due to this move is the same as the work required for the move.

$$U_r-U_l=\frac{q_oQd}{A\epsilon_o}$$

3b. How much work does it take to move a charge $q_o$ from the outer face of a plate to the inner face of the same plate? (Hint: What is the electric field inside of the plates?)

The electric field inside of the conductors is zero, so no work is required to move a charge inside of it.

4a. What is the electric potential difference, $V_{r}-V_{l}$, between the left and right plate?

$$\Delta V = \frac{\Delta U}{q_o} = \frac{Qd}{A\epsilon_o}$$

4b. What is the difference in electric potential between the inner and outer faces of one of the plates?

Zero. If it takes no work to move a charge $q_o$ inside of the conductor, the change in potential energy, $\Delta U$ is zero and the change in potential $\Delta U/q_o$ associated with this movement is zero. 

5. Write the capacitance in terms of $\epsilon_o$, $A$, and $d$.

$$\Delta V = \frac{\Delta U}{q_o} = \frac{Qd}{A\epsilon_o}$$

$$C=\frac{Q}{|\Delta V|} = \frac{A\epsilon_o}{d}$$

As expected, the capacitor only depends on the geometry of the conductors (via the area $A$ in this case) and the separation distance $d$.

%6. Plot $E(x)$ and $V(x)$. Use $V(0)=0$.

\end{tcolorbox}

\newpage

## Problem

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 2.1,height fill]

Charge is uniformly distributed on two spherical conducting shells, the cross-section of which is shown. Both shells have a thickness of $t$. The inner shell has an outer radius of $a$. The outer shell has an inner radius of $b$.

\input{Capacitance/figures/Spherical}

1a. Use Gauss's law to show that there can be no charge on the inner surface of the inner conductor. 

\ifsolutions
{\bf Answer}: Consider a Gaussian sphere with the same center as the shells and a radius between \(a-t\) and \(a\) (i.e., inside the inner conductor). The electric field at any point on the Gaussian sphere will be zero because the surface is inside a conductor. From Gauss's law, it follows that the charge enclosed by the Gaussian sphere is zero. Because it is a conductor, the charges on the inner shell must be on either its inner surface or its outer surface; as a result, the total enclosed charge for this Gaussian sphere (which must be zero from Gauss's law) is the charge on the inner surface, so the charge on the inner surface must be zero. From this we can conclude that all of the $-Q$ on the inner shell resides on its outer surface. (You did a problem similar to this on another tutorial - the difference was that there was a point charge at the center of the shell; in that problem, there was charge on the inside surface of the shell.)
\else
\vspace{1.2cm}
\fi

1b. Use Gauss's law again to show that the charge on the inner surface of the outer conductor is $+Q$. 

\ifsolutions
{\bf Answer}: A Gaussian sphere with the same center as the shells and a radius between \(b\) and \(b+t\) (i.e., inside the outer conductor) will have an electric field of zero everywhere on its surface. From Gauss's law, it follows that the charge enclosed by this surface is zero. We know that $-Q$ is enclosed by this surface -- this is the net charge on the inner shell. The other enclosed charge is the charge on the inner surface of the outer shell. The charge on this surface has to be $+Q$ for the net enclosed charge to be zero and for Gauss's law to be satisfied.
\else
\vspace{1.2cm}
\fi

1c. Show that there is no charge on the outer surface of the outer conductor.

\ifsolutions
{\bf Answer}: In 1b., it was established that $+Q$ must be on the inner surface of the outer conductor. If the outer conductor has a net charge of $+Q$, then all of the charge is on the inner surface and the charge on the outer surface must be zero.
\else
\vspace{1.2cm}
\fi

2. What is the electric field in each of the 5 labeled regions? Region $1.$ is the empty volume inside of the inner conductor, region $2.$ is the volume of the inner conductor, region $3.$ is the empty volume between the conductors, region $4.$ is the volume of the outer conductor, and region $5.$ is the region outside of the outer conductor. (Hint: Use Gauss's law several times.)

\ifsolutions
{\bf Answer}: Regions 2. and 4. are inside of a conductor, so the electric field must be zero. To find the electric field in the other region, consider an equivalent problem. A charge of $-Q$ is uniformly distributed on the surface of a sphere of radius $a$ and a charge of $+Q$ is uniformly distributed on the surface of a sphere of radius $b$. 

In the previous tutorial, Gauss's law was used to show that (1) outside a uniformly charged spherical surface, the field is the same as if all of the charge was at the origin and (2) inside the surface, the field is zero. 

Based on (2), we can conclude that the field in Region 1. is zero. 

Region 3. is inside of the outer shell, so the field due to the charges on the outer shell is zero because of (2). In Region 3., the field due to the -Q charge on the inner shell is inwards with a magnitude of $kQ/r^2$, which follows from (1). 

In Region 5., the field due to the inner shell is equal and opposite to the field due to the outer shell (the field is that of two equal and opposite charges at the origin). As a result, the field in Region 5. is zero.
\else
\vspace{1.7cm}
\fi

3. How much work will it take to move a charge $q_o$ from the outer surface of the inner shell to the inner surface of the outer shell? Said another way, what is the difference in electric potential, $U_b-U_a$?

\ifsolutions
{\bf Answer}: The electric field in region 3. is inwards with a magnitude of $kQ/r^2$. This is equivalent to the electric field due to $-Q$ at the origin. From the previous tutorial, the change in potential energy of a test charge $q_o$ when it is moved a radius of $a$ to $b$ when there is a charge $q$ at the origin is

$$U_b-U_a=kqq_o\left(\frac{1}{b}-\frac{1}{a}\right)$$

In this problem, the charge at the origin is $-Q$, so

$$U_b-U_a=-kQq_o\left(\frac{1}{b}-\frac{1}{a}\right)$$

Note that moving a positive charge in this direction corresponds to an increase in its potential energy (this is equivalent to moving a positive charge away from a negative charge at the origin). This is consistent with the equation above, which is positive ($a<b$, so the term in parenthesis is negative making the right-hand side positive).
\else
\vspace{1.2cm}
\fi

4. What is the potential difference, $V_{b}-V_{a}$?

\ifsolutions
{\bf Answer}:

$$V_{b}-V_{a} = \frac{U_{b}-U_{a}}{q_o} = -kQ\left(\frac{1}{b}-\frac{1}{a}\right)= kQ\left(\frac{1}{a}-\frac{1}{b}\right)$$
\else
\vspace{1.2cm}
\fi

5. Write the capacitance in terms of $\epsilon_o$, $a$, and $b$.

\ifsolutions
{\bf Answer}:

$$C = \frac{Q}{|\Delta V|} = \frac{Q}{kQ(\frac{1}{a}-\frac{1}{b})}=\frac{1}{k}\frac{1}{\frac{1}{a}-\frac{1}{b}}=\frac{4\pi\epsilon_o}{\frac{1}{a}-\frac{1}{b}}$$
\else
\fi
\end{tcolorbox}

# Combinations of Capacitors

In the following, justifications are given for the equations

$$\frac{1}{C_{eq}} = \frac{1}{C_1}+\frac{1}{C_2}\quad\quad \text{capacitors in series}$$

and

$$C_{eq}=C_1+C_2\quad\quad\text{capacitors in parallel}$$

used to compute the equivalent capacitance for capacitors.

It is important to note that these equations assume that the electric field created by the charges on $C_1$ do not affect the distribution of charges on $C_2$. If this is not the case, there will be additional "cross-coupling" term in the equations for $C_{eq}$. To see why additional term are needed in the equations, consider the following two capacitors separated by small and large disances.

In the case on the left, the electric field created by the charges on $C_1$ is small at the location of $C_2$. As a result, the assumption that the charge distribution on $C_2$ is still valid. In the case on the left, the charges on $C_1$ cause the charges on $C_2$ to no longer be uniforimly distributed, and vice-versa. As a result, the assumptions used to compute $C_1$ and $C_2$ are no longer valid. In order to compute the capacitance for this case, one would need to compute six capacitances, one for each pair of conductors. Using $u$ for the upper and $l$ for the lower plates, the pairs are

1. $C_{1u}$ and $C_{1l}$
2. $C_{2u}$ and $C_{2l}$
3. $C_{1u}$ and $C_{2u}$
4. $C_{1u}$ and $C_{2l}$
4. $C_{1l}$ and $C_{2u}$
6. $C_{1l}$ and $C_{2l}$

In general, capacitance decreases with the separation distance between conductors. As the distance between $C_1$ and $C_2$ increases, the extra capacitances 3.-6. decrease.

In the following, as in most circuit applications considered at the introductory level, we will assume that the capacitors are far enough apart that the two formulas for $C_{eq}$ given above apply.

## Capacitors in Series

So far we have only considered single capacitors. Here we consider two capacitors which are comprised of a total of four conductors. If two of the conductors are touching or connected via a wire as shown in the diagram, the capacitors are considered to be in series. The touching capacitors can be made to touch either by physically touching the conductors or by connecting them with a conducting wire which has the same effect.

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=blue!50!blue,colback=white,title=Example 3.1,height fill]

Four conducting plates are configured as shown. The surface area of the two plates on the left is $A_1$ and the area for the two plates on the right is $A_2$.

All of the conductors initially have a net charge of zero, and then charges are placed on the two outer conducting plates as shown in the diagram.

\scalebox{0.75}{
    \input{Capacitance/figures/Series_Parallel_Plates}
}

1. In order for the electric field to be zero inside of the inner two conductors, what charges need to be spread over the surfaces of the two inner plates? (There are a total of four surfaces -- two with area $A_1$ and two with area $A_2$)?

{\bf Answer:} The charges will distribute as shown in the following diagram. The net charge on the inner two conductors is zero -- because of conservation of charge you cannot have a net charge if you have not placed any charge on those plates. In response to the electric field that forms when charges are placed on the outer two conductors, the charges move to make the net electric field inside of all of the conductors zero. 

\scalebox{0.75}{
    \input{Capacitance/figures/Series_Parallel_Plates_Answer}
}

2. What is the electric field in all of the regions of space?

{\bf Answer:} If you look at the superposition of the electric fields from the positive and negative plates for each conductor (remember that for a sheet the field is not dependent on distance), they will cancel outside of the conductors as described in Example 2.1. In the configuration shown, the electric field outside of the region spanned by $d_1$ is zero due to the charges on the left two conductors; the charges on the right two conductors create a zero electric field outside of the region spanned by $d_2$.

In the region spanned by $d_1$, the electric field is due to only to the surfaces labeled 1. and 2. As described in Example 2.1, this field is $\mathbf{E}=-(Q/\epsilon_o A) \ihat$. 

Similarly, the electric field in the region spanned by $d_2$ is $\mathbf{E}=-(Q/\epsilon_o A ) \ihat$ and is only due to the charges on surfaces 3. and 4. In all other regions, the electric field is zero.

3. How much work is required to move a charge $q_o$ from surface 1. to surface 4.?

{\bf Answer:} To move from surface 1. to 2. takes $W=+q_oEd={q_oQd_1}/{A_1\epsilon_o}$ (draw the field lines and make sure that the $+$ makes sense). To move from surface 2. to 3. takes no work because the electric field is zero inside of a conductor. To move from surface 3. to 4. takes $W=+q_oEd={q_oQd_2}/{A_2\epsilon_o}$. The total work is:

$$W=\frac{q_oQd_1}{A_1\epsilon_o}+\frac{q_oQd_2}{A_2\epsilon_o}$$

4. What is the difference in potential energy of the charge $q_o$ between surface 1. and 4.?

{\bf Answer:} The difference in potential energy is the same as the amount of work required to move a charge from surface 1. to 4:

$$U_4-U_1=\frac{q_oQd_1}{A_1\epsilon_o}+\frac{q_oQd_2}{A_2\epsilon_o}$$

5. What is the difference in potential between surface 1. and 4.?

{\bf Answer:} $$V_4-V_1=\frac{U_4-U_1}{q_o}=\frac{Qd_1}{A_1\epsilon_o}+\frac{Qd_2}{A_2\epsilon_o}$$

6. The capacitance of this configuration is the amount of charge placed on the outer surfaces divided by the potential difference between the outer surfaces. What is this capacitance?

{\bf Answer:} 

$$C = \frac{Q}{|V_4-V_1|} = \frac{Q}{\frac{Qd_1}{A_1\epsilon_o}+\frac{Qd_2}{A_2\epsilon_o}}=\frac{1}{\frac{d_1}{A_1\epsilon_o}+\frac{d_2}{A_2\epsilon_o}}$$

We have derived the formula for how capacitors add in series. To see this, invert the previous formula

$$\frac{1}{C} = \frac{d_1}{A_1\epsilon_o}+\frac{d_2}{A_2\epsilon_o} = \frac{1}{C_1}+\frac{1}{C_2}$$ 

where $C_1={A_1\epsilon_o}/{d_1}$ and $C_2={A_1\epsilon_o}/{d_1}$.


\end{tcolorbox}

\newpage

### Problem

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 3.1,height fill]

The cross-section of three conducting shells is shown in the following diagram. All shells have a thickness $t$. The inner shell has an outer radius of $a$. The middle shell has an outer radius of $b$. The outer shell has an inner radius of $c$.

All of the shells are initially uncharged. A charge of $-Q$ is placed on the inner shell and a charge of $+Q$ is placed on the outer shell.

\input{Capacitance/figures/Spherical_Series}

1. In order for the electric field to be zero inside all of the conductors, how will the charges distribute on the six conducting surfaces (each shell has an inner and outer surface)?

\ifsolutions
{\bf Answer}:

Inner-most shell: Inner surface has no charge; Outer surface has $-Q$.

Middle shell: Inner surface has $+Q$; Outer surface has $-Q$.

Outer shell: Inner surface has $+Q$; Outer surface has zero.
\else
\vspace{2cm}
\fi

2. What will the electric field be in each of the 7 regions shown?

\ifsolutions
{\bf Answer}:

$\mathbf{E}=0$ in Regions 2., 4., and 6. (inside conductor).

$\mathbf{E}=-kQ\hat{\mathbf{r}}/r^2$ in Region 3. 

$\mathbf{E}=-kQ\hat{\mathbf{r}}/r^2$ in Region 5. 

$\mathbf{E}=0$ in Region 7.
\else
\vspace{2cm}
\fi

3. What is the difference in potential $V_c-V_a$?

\ifsolutions
{\bf Answer}:

There is a change in potential when going from a radius of $a$ to a radius of $b-t$ of $V_{b-t}-V_a$. Moving from $b-t$ to $b$, there is no change in potential (a conductor is an equipotential). There is a change in potential in going from $b$ to $c$ of $V_c-V_b$.

$$V_c-V_a=(V_c-V_b) + (V_{b-t}-V_a)$$

In Regions 3. and 5. the electric field is the same as if a charge $-Q$ was at the origin.

$$V_c-V_b=-kQ\left(\frac{1}{c}-\frac{1}{b}\right)$$

$$V_{b-t}-V_a=-kQ\left(\frac{1}{b-t}-\frac{1}{a}\right)$$

$$V_c-V_a=(V_c-V_b) + (V_{b-t}-V_a)=-kQ\left(\frac{1}{c}-\frac{1}{b}\right)-kQ\left(\frac{1}{b-t}-\frac{1}{a}\right)$$
\else
\vspace{2cm}
\fi

4. What is the capacitance of this configuration?

\ifsolutions
{\bf Answer}:

$$C=\frac{Q}{|\Delta V|} = \frac{4\pi\epsilon_o}{\left(\frac{1}{b}-\frac{1}{c}\right)+\left(\frac{1}{a}-\frac{1}{b-t}\right)}$$

Notice that this answer is what you would get if you added the capacitance of two capacitors in series -- one capacitor has an inner shell at $a$ and an outer shell at $b-t$. Another capacitor has an inner shell at $b$ and an outer shell at $c$. The equivalent capacitance for two capacitors in series is found using the sum of the inverses:

$$\frac{1}{C_{eq}} = \frac{1}{C_{inner}} + \frac{1}{C_{outer}}$$

From earlier, the capacitance of two shells is

$$C=\frac{4\pi\epsilon_o}{\frac{1}{r_i}-\frac{1}{r_o}}$$

where $r_o$ and $r_i$ are the inner and outer radius, respectively. Thus,

$$C_{outer} = \frac{4\pi\epsilon_o}{\frac{1}{b}-\frac{1}{c}}$$

$$C_{inner} = \frac{4\pi\epsilon_o}{\frac{1}{a}-\frac{1}{b-t}}$$

Plugging these two equations into ${1}/{C_{eq}} = {1}/{C_{inner}} + {1}/{C_{outer}}$ and solving for $C_{eq}$ will give the same answer stated at the start of the answer to this problem.
\else
\vspace{2cm}
\fi

\end{tcolorbox}

## Capacitors in Parallel

Capacitors are said to be in parallel when each conductor in a single capacitor touches directly, or via a wire, another conductor on another capacitor.

### Example

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=blue!50!blue,colback=white,title=Example 4.1,height fill]

In the following diagram, two parallel plate capacitors are connected by a wire as shown. The conductors are initially uncharged and then $-Q$ is placed on the lower-right conductor and $+Q$ is placed on the upper-right conductor.

\input{Capacitance/figures/Parallel_Parallel_Plates_Example}

As in the previous example, all of the charges will spread out over the inside faces of the plates. In this case, the charge $Q$ will be split and some charge will appear on the inner face of the upper left conductor ($1u$) and the rest on the inner face on the top right conductor ($2u$). In equation form, this statement is

$$Q=q_{1u}+q_{2u}$$

It can be shown from Gauss's law that $q_{1l} = -q_{1u}$ and $q_{2u} = -q_{2u}$.

Because the two conductors on the top are at the same potential and the two conductors on the bottom are at the same potential (why?), the potential differences between the upper and lower plates of the capacitors must be the same: 

$$\Delta V_1=\Delta V_2$$

For the full system:

$$Q = C \Delta V$$

For each of the capacitors, $C_1 = q_1/\Delta V_1$ and $C_2 = q_2/\Delta V_2$. These can be re-written as $q_1 = C_1 \Delta V_1$ and $q_2 = C_2 \Delta V_2$. Plugging these equations into $Q = q_1 + q_2$ gives

$$C\Delta V = Q = q_1 + q_2 = C_1 \Delta V_1 + C_2 \Delta V_2$$

Because $\Delta V=\Delta V_1=\Delta V_2$, we conclude that the net capacitance of this configuration is

$$C = C_1 + C_2$$

which is expected because the capacitors are connected in parallel.

\end{tcolorbox}

\clearpage

### Problem

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 4.1,height fill]

\includegraphics[scale=0.3]{Capacitance/Q24.17_fig.png}

1a. Which of the plates in the $C_1$, $C_2$, $C_3$ group are at the same potential? How do those potentials relate to the potentials $V_a$ and $V_d$?

\ifsolutions
{\bf Answer}: The left plate of $C_1$ is at the same potential as the left plate of $C_3$. These plates have a potential of $V_a$. The right plate of $C_2$ is at the same potential as the right plate of $C_3$. These plates have a potential of $V_d$.
\else
\vspace{1.7 cm}
\fi

2. What is the charge on the right-hand plate of $C_1$ relative to the left-hand plate of $C_2$? Why?

\ifsolutions
{\bf Answer}: They are equal and opposite. If the capacitors were initially uncharged and a battery is connected to $a$ and $d$, charge will appear on both of the surfaces mentioned; by conservation of charge, the sum of the charges on both surfaces must be zero, so the charge on each surface must be equal and opposite.
\else
\vspace{1.7 cm}
\fi

3. Which of the capacitors in this network are in series and which are in parallel? Explain how you know. 
\ifsolutions

%In the following diagram, the reduction steps used in this paragraph are shown. In the first step, capacitor $C_4$ was moved to make the circuit look a bit more familiar.

%\begin{center}
%\includegraphics[width=0.75\textwidth]{Capacitance/figures/Problem_4_1_Solution.jpg}
%\end{center}

{\bf Answer}: $C_1$ and $C_2$ are in series. They are connected and the charge on their surfaces are equal in magnitude. 

There are no other {\it individual} capacitors that are in series or parallel. However, if the capacitors $C_1$ and $C_2$ are replaced with a capacitor having capacitance $C_{12}$ found using 

$1/C_{12}=1/C_1+1/C_2,$

then $C_{12}$ is in parallel with $C_3$. The combination of $C_{12}$ and $C_3$ is equivalent to a capacitor $C_{123}$ with a capacitance computed by adding $C_{12}$ and $C_{3}$ in parallel: 

$C_{123} = C_{12} + C_{3}.$

The capacitor $C_{123}$ is in series with $C_{4}$. Thus, 

$1/C_{1234}=1/C_{123}+1/C_4.$

\else
\vspace {1.7cm}
\fi

4. If each of the capacitors has the same capacitance, $C = 4.00~\mu$F, and  $V_a$ - $V_b = +28.0$ V, what is the potential across each of the capacitors? Justify your answers. 

\ifsolutions
{\bf Answer}: 

Using $C_1=C_2=C_3=C_4=C$, the equations from the answer to question 3. give

1/C_{12}=1/C_1+1/C_2\quad\Rightarrow\quad C_{12}=\frac{C}{2}$

$C_{123} = C_{12} + C_{3}=\frac{C}{2}+C\quad\Rightarrow\quad C_{123}=\frac{3}{2}C$

$1/C_{1234}=1/C_{123}+1/C_4=\frac{1}{\frac{3}{2}C}+\frac{1}{C}\quad\Rightarrow\quad C_{1234}=\frac{3}{5}C$

The charge on the surfaces of the equivalent capacitor is found using:

%$Q_{1234} = C_{1234}(V_d-V_a)$
$Q_{1234} = C_{1234}(V_b-V_a) = (3/5)(4\muF) \times (28V) = 67.2 \muC$
    
This is the charge on capacitor 4 so:

$V_4 = Q_{1234}/C_4 = 67.2 \muC/4\muF = 16.8$V

The voltage drop across $V_{123}$ is 28V - 16.8V = 11.2V. Since capacitor 3 is in parallel with capacitors 1 and 2, $V_3 = 11.2$V which is also the potential across $C_{12}$. 

$C_{12} = C/2 = Q_{12}/V_{123} \Rightarrow Q_{12} = 22.4 \muC$

$V_1 = V_2 = Q_{12}/C = 5.6$V
%This equation has two unknowns, the charge and the potential difference.


%In the last diagram below of the figure above, the capacitor $C_{1234}$ is split back into $C_{123}$ and $C_4$ in series. Because they are in series, the magnitude of the charge on each surface is still $Q_{1234}$. The given potential difference applies to the capacitor on the left, $C_{123}$: 

%$V_b-V_a=Q_{1234}/C_{123}$

%Solving for $Q_{1234}$ gives

%$Q_{1234}=(V_b-V_a)C_{123} = 28\left(\frac{3}{5}C\right)$

%This value of $Q_{1234}$ can be used to find $V_d-V_b$ using 

%$Q_{1234} = C_{4}(V_d-V_b)$

%Solving for $V_d-V_b$ gives

%$V_d-V_b=\frac{Q_{1234}}{C_{4}}=\frac{28\left(\frac{3}{5}C\right)}{C}= 28\left(\frac{3}{5}\right)~\mbox{V}$

%which is the potential across $C_4$. This equation along with the given $V_b-V_a$ can be used to answer the following question.

%The potential across $C_3$ is $V_b-V_a$, which was given.

%The potential across $C_{12}$ is also $V_b-V_a$. The potential across $C_1$ added to the potential across $C_2$ must be equal to $V_b-V_a$. To find these potentials, we first need to find the charge on $C_{12}$.

%$Q_{12}=C_{12}(V_b-V_a)=\frac{C}{2}28$

%$Q_{12}$ can be used to compute the potential across each of $C_1$ and $C_2$. Both capacitors will have a charge of $Q_{12}$ on them because they are in series.

%$V_1=Q_{12}/C_1=(\frac{C}{2}28)/C=14~\mbox{V}$

%$V_2=Q_{12}/C_2=14~\mbox{V}$

%The fact that $V_1=V_2$ is expected because $C_1=C_2$.

%The potential across $C_3$ is $V_b-V_a$, which was given.

%$V_3=V_b-V_a=28~\mbox{V}$

%The potential across $C_4$ is $V_d-V_b$, which was found earlier:

%$V_4=V_d-V_b=\frac{Q_{1234}}{C_{4}}=28\frac{3}{5}~\mbox{V}$

%The fact that the potential across the three capacitors on the left is larger than that across $C_4$ is consistent with the fact that the equivalent capacitance of the three capacitors on the left, $C_{123}=3C/2$, is larger than that of $C_4=C$.
\else
\vspace {1.7cm}
\fi

5. What is $V_d$ - $V_a$? What is $V_b - V_d$? Explain. 

%$$V_d-V_a = (V_d-V_b) + (V_b-V_a)=V_3+V_4=28\left(\frac{3}{5}+1\right)=28\frac{8}{5}~\mbox{V}$$

$V_d-V_a = V_{123} = 11.2$V as shown above.

$V_b - V_d = V_4 = 16.8$V as shown above.

%The first term in parenthesis was computed in part 4. The second term was given as $28$~V. This equation states that the potential across the capacitors between $a$ and $b$ added to the potential across $C_4$ is the total potential difference across the capacitor network.
