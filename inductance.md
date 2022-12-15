# Inductance Calculation

In the last HW, problem 4.6e was assigned. In the problem, it was stated that the internal inductances per length to use were

$$\frac{L_{ia}}{2\pi a}\,\,\text{and}\,\,\frac{L_{ib}}{2\pi b}$$

1. Derive the formula for the internal inductances per unit length assuming current is uniformly distributed throughout the cross-section of the conductors. Then derive the inductances per unit length assuming that the current is distributed uniformly only to a depth of \(\delta\) and compare the result with the two equations given above.

**Answer**

The internal inductance of the outer cylinder of length \(l\) with an inner radius \(b\) and an outer radius \(c\) of a co-axial cable is derived in Example 2.17 (page 108) of Ramo.  The energy method was used. The result is

$$\mathcal{L}_{ib}=\frac{\mu l}{2\pi}\left[\frac{c^4\ln c/b}{(c^2-b^2)^2}-\frac{b^2-3c^2}{4(c^2-b^2)}\right]$$

The dimensionless term in square braces is better written in terms of the dimensionless ratio \(c/b\):

$$\mathcal{L}_{ib}=\frac{\mu l}{2\pi}\left[\frac{(c/b)^4\ln c/b}{[(c/b)^2-1]^2}-\frac{1-3(c/b)^2}{4[(c/b)^2-1]}\right]$$

Note that this differs from the internal inductance of a cylindrical shell with inner radius \(b\) and outer radius \(c\) because the return current that flows in the opposite direction along the axis of the cylinder reduces the magnetic field.

To write \(\mathcal{L}_{ib}\) in terms of \(\delta\), define \(\delta = c-b\). 

Defining \(x\equiv \delta/b\) gives \(c/b=1+x\) and

$$\mathcal{L}_{ib}=\frac{\mu l}{2\pi}\left[\frac{(1+x)^4\ln x}{[(1+x)^2-1]^2}-\frac{1-3(1+x)^2}{4[(1+x)^2-1]}\right]$$

The series expansion of this around \(x=0\) can be found using \(\ln(1+x) = 1+x+ ...\) and \(1+x^n = 1+nx + ...\) or a program such as WolframAlpha 

The result [https://www.wolframalpha.com/input/?i=series+%281%2F%28%281%2Bx%29%5E2+-+1%29%29+%28+%281%2Bx%29%5E4*ln%281%2Bx%29+%2F+%28%281%2Bx%29%5E2+-+1%29+-+%281%2Bx%29%5E2%2F2+%29+-+1%2F4] is

$$\mathcal{L}_{ib}=\frac{\mu l}{2\pi}\left(\frac{x}{3}-\frac{x^3}{30}+...\right)$$

or

$$\mathcal{L}_{ib}\simeq\frac{\mu (\delta/3)}{2\pi b}l$$

In problem 4.6e, the equation for inductance per unit length for very high frequencies (so \(\delta\) is small) was given as

$$\frac{L_{ib}}{2\pi b}$$

As a result, we have found the origin of this equation and conclude that \(L_{ib}\), referred to as the "internal inductance per square", is \(L_{ib}=\mu \delta/3\).

----

The internal inductance of the inner cylinder is

$$L_{ia}=\frac{\mu}{8\pi}$$

When the current on the inner conductor is confined to radii of \(b-\delta\) to \(b\), its internal inductance is found using the formula for \(L_{ib}\) with the replacement of \(c/b\) with \(a/(a-\delta)=1/(1-x)\), where \(x\equiv \delta/a\).

$$\mathcal{L}_{ia}=\frac{\mu l}{2\pi}\left[\frac{(1-x)^{-4}[\ln (1-x)^{-1}]}{[(1-x)^{-2}-1]^2}-\frac{1-3(1-x)^{-2}}{4[(1-x)^{-2}-1]}\right]$$

In comparison, in terms of the small ratio \(x\equiv\delta/b\),

$$\mathcal{L}_{ib}=\frac{\mu l}{2\pi}\left[\frac{(1+x)^4\ln x}{[(1+x)^2-1]^2}-\frac{1-3(1+x)^2}{4[(1+x)^2-1]}\right]$$

Given that for small \(x\), \((1-x)^{-n}\simeq 1 + nx\) and \((1+x)^{n}\simeq 1 + nx\), the \(L_{ia}\) series expansion for small \(x\) is expected to match to leading order the result for \(\mathcal{L}_{ib}\) for small \(x\). The expansion is [https://www.wolframalpha.com/input/?i=series+%28%28%281-x%29%5E%28-4%29+ln+%281%2F%281-x%29%29%29%29%2F%28%28%281-x%29%5E%28-2%29-1%29%5E2%29+%2B+%281-3*%281-x%29%5E%28-2%29%29%2F%284*%28%281-x%29%5E%28-2%29-1%29%29+at+x%3D0]

$$\mathcal{L}_{ia}=\frac{\mu l}{2\pi}\left[\frac{x}{3} + \frac{x^2}{3} + ...\right]$$

As a result, we conclude that \(L_{ia}=\mu \delta/3\), which is the same as \(L_{ib}\).

----

The statement "internal inductance per square" is opaque. I suspect that it refers to the fact that the internal inductance of one of the two large slabs shown in the top diagram of [https://www.mathcha.io/editor/1lB03iV1HvqhM0zwZgirMVgBxiJgJP1Ki87D7YJ] is \((\mu \delta /3) (l/w)\). If the slabs are square, then \(l=w\).
|}

2. Derive the formula for the external inductance of a coaxial cable.

**Answer**

The external inductance is the familiar formula

$$L=\frac{\mu l}{2\pi}\ln\left(\frac{b}{a}\right)$$

3. When the gap in the coaxial cable is small and the radius \(a\) is large relative to the gap, the magnetic field is nearly constant in the gap region. As a result, it is expected that the external inductance per unit length \(l\) should be related to that for two parallel planes with area \(2\pi a l\). Define the gap distance as \(\delta = b-a\) and assume \(\delta/a \ll 1\) and show that the external inductance in this approximation is related to the external inductance of two parallel planes with areas of \(2\pi a l\) (the current on the planes flows parallel to the direction of \(l\)). 

**Answer**

Schematically, we are to show the inductance for the geometry on the left of the bottom figure at [https://www.mathcha.io/editor/1lB03iV1HvqhM0zwZgirMVgBxiJgJP1Ki87D7YJ] approximates that on the right.

Using\(b=a+\delta\) and plugging this into the result of 2. gives

$$L=\frac{\mu l}{2\pi}\ln\left(\frac{a + \delta}{a}\right)=\frac{\mu l}{2\pi}\ln\left(1+\frac{ \delta}{a}\right)$$

For \(\delta/a \rightarrow 0\), 

$$L=\mu l\frac{\delta}{2\pi a}$$

When the gap is small relative to \(a\), the magnetic field is nearly constant in the volume between the cylinders. Based on the fact that inductance is related to the volume integral of \(B^2\), it is expected that the inductance in this limit should match the inductance of the following configuration.

The internal magnetic field for the bottom right configuration at [https://www.mathcha.io/editor/1lB03iV1HvqhM0zwZgirMVgBxiJgJP1Ki87D7YJ] is \(\mu I/w\). Using the energy method

$$\frac{1}{2}LI^2 = \frac{1}{2\mu}\int B^2 dv = \frac{\mu_o}{2}\frac{l\delta}{w} I^2$$

so that

$$L=\mu l\frac{\delta}{w}$$

This matches the external inductance of the cylinder when \(w=2\pi a\).

# Flux Linkage

The top diagram at [https://www.mathcha.io/editor/K7MwPfWBUm3TXq8oNgtvEkvPecMwO6Oeu45ljV] shows a rectangular duct that carries a net current of \(I_1 = K_1l\) in the direction shown. A series of current supplies along the gap is driving the current. The surface of the duct has a small enough thickness that the current can be treated as flowing on a sheet.

=== === 

Assuming \(w \gg h_1\) and \(l \gg h_1\), use Ampere's law to find the magnetic field inside and outside of the duct. Show the Amperian loop and justify your steps.

**Answer**

As shown in class, Ampere's law can be used to show that the magnetic field due to a large sheet of current is \(\mu_o I/2l\). The key elements of using Ampere's law are

1. providing an argument for (a) why the magnetic field will be horizontal and independent of horizontal position (b) why the magnitude of the field will be the same at equal distances above and below the sheet, and (c) the direction of the field above and below the sheet
2. using Ampere's law to find the magnitude of the field, and
3. putting result from (1) and (2) together to get the total field.

Two parallel sheets with current flowing in the opposing directions will have an additive field in between the sheets and zero field outside of the sheets. So the total magnetic field inside the duct is \(\mu_o I/l\) and outside of the duct, the field is zero.

----

The duct has only an external self-inductance. (External inductance means inductance due to flux through a cross-section where there is no current.) The external self-inductance is due to the magnetic flux through the cross-sectional area \(A_1=h_1w\). The electromotive force across the gap is due to a change in magnetic flux

$$\mathcal{E}_1 = -\frac{\partial \Phi_m}{\partial t}$$

where \(\Phi_m\) is the magnetic flux. Compute this magnetic flux and re-write this equation in the form of

$$\mathcal{E_1} = -L_1 \frac{\partial I_1}{\partial t}$$

so as to find \(L_1\) in terms of \(\mu_o\), \(l\), and the cross-sectional area \(A_1=h_1w\).

**Answer**

$$\Phi_1 = \mu_o I_1 A_1/l$$

$$\mathcal{E}_1 = -\frac{\partial \Phi_1}{\partial t} = -\frac{\mu_o A_1}{l}\frac{\partial I_1}{\partial t}\qquad\Rightarrow\qquad L = \frac{\mu_o A_1}{l}$$
|}

-----

Two ducts are nested as shown in the bottom diagram at [https://www.mathcha.io/editor/K7MwPfWBUm3TXq8oNgtvEkvPecMwO6Oeu45ljV] such that their widths are essentially the same. The cross-sectional areas of each of the ducts are \(A_1=h_1w\) and \(A_2=h_2w\).

Compute \(\mathcal{E}_1\) and \(\mathcal{E}_2\) based on the time rate of change of flux through \(A_1\) and \(A_2\), respectively. Note that the flux through each of the cross-sectional areas includes flux due to the fields created by the current on one or more of the ducts. 

The total EMF that the current supplies need to maintain is 

$$\mathcal{E}=\mathcal{E}_1+\mathcal{E}_2$$

At low frequencies, we can assume that the total current on each of the ducts will be the same and uniformly distributed along \(l\). Call this current \(I\). (The power supplied is at any instant of time is \(\mathcal{E}_1I_1+\mathcal{E}_2I_2=\mathcal{E}I\). You are not asked to consider power in this problem, but it is referenced in the paper by Boykin in the [https://piazza.com/class/ke8nm0fjaej422?cid=59 Pizza thread].)

Find \(\mathcal{E}\) in terms of \(\mu_o\), \(l\), and the cross-sectional areas. Identifiy the inductance of this configuration.

**Answer**

The flux through the inner duct is the total field in the inner duct times the area of the duct. In the inner duct, \(B=2\mu_oI/l\) - the field from the current on the inner and outer duct in \(A_1\) are equal.

$$\Phi_1 = \frac{2\mu_oI}{l}A_1$$

The flux integral through the outer duct needs to be split into two parts to account for the fact that the field is not constant over the cross-section of \(A_2\). Over the \(A_1\) region, the field is \({2\mu_oI/l}\). The area outside of \(A_1\) has area \(A_2-A_1\) and a field \(\mu_oA/l\) that is due to the current on the outer duct only. The flux over the cross-section of \(A_2\) is

$$\Phi_2 = \frac{2\mu_oI}{l}A_1 + \frac{\mu_oI}{l}(A_2-A_1)$$

As instructed, 

$$\mathcal{E}=\mathcal{E_1} + \mathcal{E_2}$$

which simplifies to

$$\mathcal{E}=-\frac{\mu_o}{l}(3A_1+A_2)\frac{\partial I}{\partial t}\qquad \Rightarrow \qquad L = \frac{\mu_o}{l}(3A_1+A_2)$$

This is the non-energy method that Boykin suggests for computing the inductance as an alternative to computing the internal and external fluxes and accounting for "flux linkages".

----

In part 3., the inductance was computed without reference to internal and external inductances. Compute the inductance of this configuration by computing the external inductance using the flux through \(A_1\) due to the field from both of the ducts and then find the internal flux using \(B_{21}(A_2-A_1)\), where \(B_{21}\) is the field in the region between ducts \(1\) and \(2\). (Based on the definition of "external inductance" given in part 2., one could argue that there is no "internal inductance" to be considered in this problem. However, in treating the regions \(A_2-A_1\) as internal, we are anticipating using \(h_2=h_1 + dh\) in the limit \(dh\rightarrow 0\) and then adding more ducts; in this limit, these fluxes would be internal differential fluxes.) 

Using these instructions, compute the inductance of the configuration. You should find that the inductance computed in this way is smaller than the inductance found in part 3. 

**Answer**

On the previous HW, several students attempted to compute the inductance of a co-axial cable by computing the internal inductance and internal inductance separately and then adding the result. This gives the wrong answer. As noted by Boykin, many textbooks get the correct answer by accounting for "flux linkages", but "flux linkages" is not often clearly defined and a physical justification for accounting for it is not provided. In this part, we compute the inductance without accounting for flux linkages and see that we get an answer different from part 3.

The internal inductance is computed using the flux through \(A_1\):

$$L_{int} = \frac{\Phi_{A_1}}{I} = \frac{\frac{2\mu_oI}{l}A_1}{I}=\frac{\mu_oA_1}{l}$$

The external inductance is computed using the flux through \(A_2-A_1\):

$$L_{ext} = \frac{\Phi_{A_2-A_1}}{2I} = \frac{\frac{\mu_oI}{l}(A_2-A_1)}{2I}=\frac{\mu_o(A_2-A_1)}{2l}$$

$$L=L_{int}+L_{ext}=\frac{\mu_o}{l}\frac{(A_1+A_2)}{2}$$

This differs from the answer to 3., which is

$$L = \frac{\mu_o}{l}(3A_1+A_2)$$

----

The inductance computed in 4. is smaller than that from 3. because all of the "flux linkages" were not considered in the calculation in part 4. Based on a comparison of your results in problems 3. and 4., explain what "flux linkage" means and or justify the \(I_{<}\) that I mentioned in the Piazza thread. You may also want to read the paper by Boykin, the scanned book pages in the [https://piazza.com/class/ke8nm0fjaej422?cid=59 Piazza thread], and the textbook where the first use of the term "flux linkage" is on page 189 in a section on mutual inductance. The energy method, using \(LI^2/2=\int B^2/2\mu_o\, dv\), can also be used to find the inductance of this configuration.

**Answer**

In the textbook on page 189 where flux linkages is first discussed, it is in a section on mutual inductance. To account for all of the "flux linkages" when computing the external flux means to account for all of the mutual inductances. The emf around the inner duct depends on the current (and hence field) created by both ducts. The emf around the outer duct also depends on the current (and hence field) created by both ducts. So the total inductance is

$$L = L_1 + L_2 + M_{12} + M_{21} = L_1 + L_2 + 2M_{12}$$

$$L_1 = \frac{\mu_o A_1}{l}$$

$$L_2 = \frac{\mu_o A_2}{l}$$

$$M_{12} = \frac{\Phi_1}{I_2} = \frac{\mu_o A_1}{l}$$

If we identify $$L_1$$ as the internal flux, then the external flux is

$$L_{ext} = L_2 + 2M_{12} = \frac{\mu_o}{l}(A_2 + 2A_1)$$

As a final check, we can use Poynting's theorem, which reduces to:

$$\int \mathbf{J}\cdot \mathbf{E}\, dv = -\frac{1}{2\mu_o}\frac{\partial}{\partial t}\int B^2 dv$$

The left-hand side reduces to \(I\mathcal{E}_1 + I\mathcal{E_2} = I\mathcal{E}\) and the right-hand side is

$$-\frac{\mu_o}{l}(3A_1+A_2)I\frac{\partial I}{\partial t}$$

Equating the two gives

$$\mathcal{E} = -\frac{\mu_o}{l}(3A_1+A_2)\frac{\partial I}{\partial t}$$

from which we conclude 

$$L=\frac{\mu_o}{l}(3A_1+A_2)$$

In summary - on problems with a spatially distributed current, it is easier to use the energy formulation to find inductance. One can appeal to first principles to find the inductance and show that the energy formulation automatically accounts for mutual inductances.
|}

Save your answer in a file named <code>HW9_1.pdf</code>.