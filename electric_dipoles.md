= Electric Dipoles =

== Electric Dipole Equation ==

The equation for the potential due to two point charges \(\pm q\) forming a dipole moment of \(\mathbf{p}\) centered on the origin is

$$V=k\frac{\mathbf{p}\cdot\hat{\mathbf{r}}}{r^2}$$

where \(r\) is the distance from the origin.

# Is this equation an approximation?
# What is \(\mathbf{p}\)? Use a diagram if necessary.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Electric dipoles are covered in section 3.4 of the textbook.

This equation is an approximation. In section 3.4, he starts with the exact equation for the potential for two charges \(\pm q\) separated by a distance \(d\) (similar to what you did for computing the potential for the point charge configurations in the previous section of this page). Then he asks what the potential will be if it was measured at a distance that is large relative to \(d\) and arrives at the dipole equation. I did something similar in class except that I did it is a less general way.

The dipole moment \(\mathbf{p}\) is \(q\) times the vector drawn from the \(-q\) charge to the \(+q\) charge. So if the \(+q\) charge is at \((x,y,z)=(0,0,d/2)\) and the \(-q\) charge is at \((x,y,z)=(0,0,-d/2)\), then \(\mathbf{p}=qd\hat{\mathbf{z}}\).

You should be able to come up with an equation for the dipole moment in terms of \(q, a, b, c\) given a \(+q\) charge is at \((x,y,z)=(a,b,c)\) and the \(-q\) charge is at \((x,y,z)=(-a,-b,-c)\).
|}

== Electric Dipole Equation ==

The potential for an electric dipole centered on the origin is

$$V_d=k\frac{\mathbf{p}\cdot\hat{\mathbf{r}}}{r^2}$$

The potential due to a point charge \(q\) located at position \(\mathbf{r}'\) is

$$V_p=k\frac{q}{|\mathbf{r}-\mathbf{r}'|}$$

Given a \(+Q\) charge at \((x,y,z)=(0,0,-a)\) and a \(-Q\) charge at \((x,y,z)=(0,0,a)\), compute 

# \(V_d(x,y,z)\)
# \(V_p(x,y,z)\) for the \(+Q\) charge.
# \(V_p(x,y,z)\) for the \(+Q\) charge.
# Under what conditions will \(V_d\) give approximately the same answer as \(V_{+Q} + V_{-Q}\)?
# At the origin, which is larger,  \(V_d(y,z)\) or \(V_{+Q} + V_{-Q}\)?
# Compute (\(V_{+Q}+V_{-Q})/V_d\) when \((x,y,z)=(0,1,0)\). Your answer should only involve numbers and square roots.
# Compute (\(V_{+Q}+V_{-Q})/V_d\) when \((x,y,z)=(0,10,0)\). Your answer should only involve numbers and square roots.
# If you had a calculator, which ratio is expected to be closer to 1.0, and why?

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Hints
|-
|
\(\mathbf{p}=-2Qa\hat{\mathbf{z}}\) (see previous problem)

\(\hat{\mathbf{r}}=\mathbf{r}/r=(x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}})/r\)

\(r=\sqrt{x^2+y^2+z^2}\) (by definition)

\(\mathbf{r}'=-a\hat{\mathbf{z}}\) for the \(+Q\) charge.

\(V_{+Q}={{kQ}\over\sqrt{x^2+y^2+(z+a)^2}}\)

\(V_{-Q}={{-kQ}\over\sqrt{x^2+y^2+(z-a)^2}}\)

$$V_d=k\frac{\mathbf{p}\cdot\hat{\mathbf{r}}}{r^2}$$

\(\mathbf{p}=-2Qa\hat{\mathbf{z}}\)

\(\hat{\mathbf{r}}=\mathbf{r}/r=(x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}})/r\)

so \(\mathbf{p}\cdot \hat{\mathbf{r}} = -2Qaz/r\) and

$$V_d=\frac{-2kQaz}{r^3}=\frac{-2kQaz}{(x^2+y^2+z^2)^{3/2}}$$

At the origin, \(V_d\rightarrow \infty\) and \(V_{+Q} + V_{-Q}=0\), so \(V_d\) is larger.

|}

== Derivation ==

We seek to have an equation for the potential far away from a dipole that is located at an arbitrary position in space, as shown in the figure.

In general, the potential at \(\mathbf{r}=x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}\) for a point charge \(q'\) located at \(\mathbf{r}'=x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}+z'\hat{\mathbf{z}}\), the potential is

$$V(\mathbf{r}) = \frac{kq'}{|\mathbf{r}-\mathbf{r}'|} = \frac{kq'}{\sqrt{(x-x')^2 + (y-y')^2 + (z-z')^2}}$$

For charges \(q'\) and \(-q'\) located at \(\mathbf{r}'_+\) and \(\mathbf{r}'_-\), respectively, the potential is the sum of the individual potentials

$$V(\mathbf{r}) = V_+ + V_- = \frac{kq'}{|\mathbf{r}-\mathbf{r}'_+|} + \frac{-kq'}{|\mathbf{r}-\mathbf{r}'_-|}$$

or

$$V(\mathbf{r}) = \frac{kq'}{\sqrt{(x-x'_+)^2 + (y-y'_+)^2 + (z-z'_+)^2}} + \frac{-kq'}{\sqrt{(x-x'_-)^2 + (y-y'_-)^2 + (z-z'_-)^2}}$$

It can be shown that at distances far away from center of the dipole and distances large compared to the charge separation, this simplifies to

$$V(\mathbf{r}) \simeq \frac{k\mathbf{p}'\cdot\hat{\mathbf{r}}}{r^2}$$

where

$$\mathbf{p}'\equiv q'(\mathbf{r}_+'-\mathbf{r}'_-)\equiv q'\mathbf{d'}$$

The advantage of this approximate potential equation is that it no longer involves the location of the two charges (primed coordinates); one only need to know the vector that connects the negative charge to the positive charge, \(\mathbf{d}'\). There is a clean separation between information about the dipole, contained in \(\mathbf{p}'\), and the location where we want to know the potential of the dipole, \(\mathbf{r}\) and is much easier to handle mathematically. And although it is an approximation, it is a good approximation. To see why, consider the following plot, which shows the potential for a pure dipole and the dipole for an electron separated by a proton by a distance of X on a scale that spans XXX mm. The plots look identical. It is not until we change the scale to XXX nm that we see the difference. So in applications where we measure differences in the potential over distances much longer than XXX nm, there is not a measurable error in the approximation. As a result, we typically only say "dipole potential" instead of the more accurate "approximate dipole potential". 

The potential for "pure dipole" is a phrase that is sometimes used informally.  But a "pure" dipole cannot exist - for the approximation to be exact, one needs to be an infinite distance away from the dipole (where the potential is zero and it seems that no dipole exists) or the separation of the charges must be zero (so there is no charge separation and the potential is again zero). So when speaking of the "pure dipoles potential", make sure to air quotes to communicate to your audience that you know it is a contradictory phrase. Or say "the dipole approximation potential" instead of the "the pure dipole potential".

A key feature of the dipole potential 

$$V \simeq \frac{k\mathbf{p}'\cdot\hat{\mathbf{r}}}{r^2}$$

is that it decreases with distance faster (by \(1/r\)) than that for a point charge \(q'\) at the origin:

$$V \simeq \frac{kq'}{r}$$

'''Example'''

A positive charge \(+Q\) is located at \((x,y,z)=(a,2a,3a)\). A negative charge \(-Q\) is located at  \((x,y,z)=(-a,-2a,-3a)\).

Find the potential at \((x,y,z)=(10a,20a,30a)\) using the dipole approximation and compare with the exact answer.

''Dipole Approximation''

\(\mathbf{r}_+' = a\hat{\mathbf{x}}+2a\hat{\mathbf{y}}+3a\hat{\mathbf{z}}\)

\(\mathbf{r}'_- = -a\hat{\mathbf{x}}-2a\hat{\mathbf{y}}-3a\hat{\mathbf{z}}\)

\(\mathbf{d} = \mathbf{r}_+'-\mathbf{r}'_- = 2a\hat{\mathbf{x}}+4a\hat{\mathbf{y}}+6a\hat{\mathbf{z}}\)

\(\mathbf{r} = 10a\hat{\mathbf{x}}+20a\hat{\mathbf{y}}+30a\hat{\mathbf{z}}\)

\(\hat{\mathbf{r}} = \frac{10a\hat{\mathbf{x}}+20a\hat{\mathbf{y}}+30a\hat{\mathbf{z}}}{\sqrt{(10a)^2+(20a)^2+(30a)^2}}\)

''Exact''
$$
\begin{align}
V = & \frac{kQ}{\sqrt{(x-x'_+)^2 + (y-y'_+)^2 + (z-z'_+)^2}} + \frac{-kQ}{\sqrt{(x-x'_-)^2 + (y-y'_-)^2 + (z-z'_-)^2}}\\
= & \frac{kQ}{\sqrt{(10a-a)^2 + (20a-2a)^2 + (30a-3a)^2}} + \frac{-kQ}{\sqrt{(10a+a)^2 + (20a+2a)^2 + (30a+3a)^2}}
\end{align}
$$

== A Derivation ==

We'll start with a simple configuration with two equal and opposite charges at \(z=\pm d\) and work through the math before attempting the full derivation for the more general case of a dipole that is not at the origin and not aligned with the \(z\)-axis. The only assumption \(r>>d\)

The potential is exactly

$$
\begin{align}
V = &\quad\frac{kq'}{|\mathbf{r}-\mathbf{r}'_{+}|} & + &\quad\frac{-kq'}{|\mathbf{r}-\mathbf{r}'_{-}|}\\
= &\quad\frac{kq'}{\sqrt{x^2 + y^2 + (z-d)^2}} & + &\quad\frac{-kq'}{\sqrt{x^2 + y^2 + (z+d)^2}}
\end{align}
$$

where \(\mathbf{r}'_{+}=(d/2)\hat{\mathbf{z}}\) and \(\mathbf{r}'_{-}=-(d/2)\hat{\mathbf{z}}\).

The key to the derivation is factoring out \(r^2=x^2+y^2+z^2\):

$$\sqrt{x^2 + y^2 + (z-d)^2}=\sqrt{x^2+y^2+z^2}\sqrt{1-\frac{2zd}{x^2+y^2+z^2}+\frac{d^2}{x^2+y^2+z^2}}=\sqrt{r}\sqrt{1-2(z/r)(d/r)+d^2/r^2}$$

In the last step, we wrote the middle term as \(2(z/r)(d/r)\) instead of \(2(zd/r^2\) because we are assuming \(r>>d\). Defining \(\delta=r/d\), where \(\delta << 1\), gives

$$\sqrt{x^2 + y^2 + (z-d)^2}=r\sqrt{1-2(z/r)\delta+\delta^2}$$

Similarly, we can write

$$\sqrt{x^2 + y^2 + (z+d)^2}=\sqrt{r}\sqrt{1+2(z/r)\delta+\delta^2}$$

So we have

$$V = \frac{kq'}{r\sqrt{1-2(z/r)\delta+\delta^2}}+\frac{-kq'}{r\sqrt{1+2(z/r)\delta+\delta^2}}$$

The final step is to note that \(z/r\) is between \(\pm 1\) so that \(-2(z/r)\delta+\delta^2\) and \(-2(z/r)\delta+\delta^2\) are also small if \(\delta\) is small.

Defining another small number, \(\Delta=2(z/r)\delta+\delta^2\) gives

$$V = \frac{kq'}{r\sqrt{1-\Delta}}+\frac{-kq'}{r\sqrt{1+\Delta}}$$

Next, use the fact that \(1/\sqrt{1+\Delta}\simeq 1 - \Delta/2\) (from a Taylor series approximation) giving

$$V \simeq \frac{kq'}{r}(1+\Delta/2)+\frac{-kq'}{\sqrt{r}}(\sqrt{1-\Delta/2})$$

Simplifying and replacing \(\Delta\) with \(2(z/r)\delta+\delta^2\) gives

$$V\simeq\frac{kq'}{r}\Delta = \frac{kq'}{\sqrt{r}}(2(z/r)\delta+\delta^2)$$

Because \(\delta\) is small, \(\delta^2\) is much smaller, so we drop it. Then, using \(\delta=d/r\), we have

$$V\simeq\frac{kq'}{r}\Delta = \frac{kq'}{r}(2(z/r)(d/r))$$

and finally

$$V\simeq \frac{kq'(2d)(z/r)}{r^2}$$

Far from the origin relative to \(d\), the potential for this configuration is approximately

$$V \simeq \frac{kq'd\hat{\mathbf{z}}\cdot (\hat{\mathbf{x}}+\hat{\mathbf{y}}+\hat{\mathbf{z}})}{x^2 + y^2 + z^2}$$

which can be re-written as

$$V \simeq \frac{k\mathbf{p}'\cdot\hat{\mathbf{r}}}{r^2}$$

where \(\mathbf{p}'=q'\hat{\mathbf{z}}\). This may not look much like an improvement of the exact expression.
