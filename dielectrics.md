# Introduction

Dielectrics (Polarizable Material)

When there is only one dipole in a constant electric field, it is easy to compute the modified electric field.

When there are many dipoles, each induced dipole modifies the total electric field, and the total electric field is what determines how large $\mathbf{P}$ is.

In response to an external electric field, $\mathbf{E}_o$, the molecules in a dielectric material reconfigure so as to produce a generally opposing electric field inside the material. In general, the electric field outside of the dielectric is also modified from $\mathbf{E}_o$.

This is similar to what happens in a conductor in an external electric field, with the difference being that in the conductor, free electrons can move to the surface of the conductor in such a way as to completely cancel the electric field inside the material. In a dielectric, electrons are bound and can only shift their position slightly. This shift creates an induced dipole. The large-scale electric field inside a dielectric material is the external electric field plus the electric field created by all of the induced dipoles.

There are two general types of dielectric materials:

1. materials that have molecules that have no net electric field - these are referred to as non-polar molecules; and
2. materials that have molecules that each have a net intrinsic electric field but are randomly oriented so on average the electric field is zero. These are referred to as polar molecules.

In simple dielectrics, the amount of polarization in a small volume is given by

$$\mathbf{P}(x,y,z)=\epsilon_0\chi_e\mathbf{E}(x,y,z)$$

where $\chi_e$ is a dimensionless proportionality constant and $\mathbf{E}$ is the net electric field at the location of the small volume.

In the following two examples, we give a physical justification for this equation for non-polar and polar dielectrics.

The interpretation of this equation is that in a given volume in the dielectric, the induced polarization is proportional to the electric field, $\mathbf{E}$, at that location. The electric field at a given location in the material depends on the external electric field, $\mathbf{E}_o$, ''and'' the electric field created by all of the other induced dipoles in the material. This fact makes the calculation of the electric field inside of a dielectric complicated. This complication is highlighted in an example below.

## Mental Model for Non-Polar Dielectrics

At the atomic level, the creation of a dipole when an atom is exposed to an external electric field can be understood from a simple model of the atom.

## Mental Model for Polar Dielectrics

A simple model for understanding polar molecules involves considering only the torque exerted on the polar molecule and ignoring the shift of the electron orbits considered for the non-polar molecule.

## Calculation of Electric Field

It was noted that calculation of the net electric field inside and outside of a dielectric is complicated by the fact that at a given location the electric field is that due to external sources plus that due to all of the induced dipoles at other locations in the material. Here we give an example of how this could be handled mathematically. This is ''not'' a good way of computing the electric field, but serves to justify the "complicated" claim. This example is based on Example XX in Griffiths, 1989.

Asking a given location in a material to report on its polarization is akin to calling for a vote among a group of humans where everyone prefers to vote only after hearing how everyone else is going to vote.

$$\mathbf{P}(x,y,z)=\epsilon_0\chi_e\mathbf{E}(x,y,z)$$
# Fundamental Dielectric Example

In reality, the "pure" dipoles are not created by gluing dipoles into and onto an object - they are induced. The charges in an atom or molecule separate due to a local electric field and a dipole is induced. The dipole is "bound" in the sense that the charges that make up the dipole are bound to the atom or molecule.

An external electric field, $\mathbf{E}\_{ext}=E_{ext}\hat{\mathbf{x}}$ is created by two non-conducting sheets of charge.

A dielectric slab is placed between the sheet.

Find $\mathbf{E}_b$ and $\mathbf{E}$ inside the dielectric slab assuming that the dipole density induced in the slab depends on the electric field in the slab according to $\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$, where $\mathbf{E}$ is the total electric field, which is due to the induced bound charge densities and the external electric field.

The result is $\mathbf{E}=\frac{1}{1+\chi_e}E_{ext}\hat{\mathbf{x}}$. The key steps are

$$\mathbf{E} = \mathbf{E}_{ext} + \mathbf{E}_b$$

$$\mathbf{P} = \epsilon_o\chi_e\mathbf{E}$$

The key to this problem is realizing that $\mathbf{P}$ depends directly on $\mathbf{E}$ in this way and not on $\mathbf{E}_{ext}$.  That is, $\mathbf{P}$ depends on the electric field due to both bound charges that are induced and external charges (the charges on the sheets).

$$\sigma_b\equiv\mathbf{P}\cdot\hat{\mathbf{n}}=\epsilon_o\chi_e\mathbf{E}\cdot\hat{\mathbf{n}}$$

On the right/left face of the dielectric $\hat{\mathbf{n}}=\pm\hat{\mathbf{x}}$, so the right/left face has a bound surface charge density of

$$\sigma_b = \pm\epsilon_o\chi_eE$$

%$\rho_b=\left(\frac{\epsilon_o}{\epsilon}-1\right)\rho_f=-\left(\frac{\chi_e}{1+\chi_e}\right)\rho_f$ for reasons explained in the next section.

The electric field due to the bound surface charge densities can be found by finding the electric field due to $\sigma_b$ on an infinite sheet of charge. 

Inside the dielectric, the electric field $\mathbf{E}_b$, which is due to $\sigma_b$, is $\mathbf{E}_b=-(\sigma_b/\epsilon_o)\hat{\mathbf{x}}$. Using $\sigma_b=\pm\epsilon_o\chi_eE$ found above gives

$$\mathbf{E}_b = -\chi_eE\hat{\mathbf{x}}$$

Inside the dielectric, the total field is

$$\mathbf{E} = E\hat{\mathbf{x}} = \mathbf{E}\_{ext} + \mathbf{E}\_b=E_{ext}\hat{\mathbf{x}} - \chi_eE\hat{\mathbf{x}}$$

Solving for $E$ gives

$$E=\frac{1}{1+\chi_e}E_{ext}$$

Note that if you solved this problem by (wrongly) assuming $\mathbf{P} = \epsilon_o\chi_e\mathbf{E}$, you would have found

$$E=(1-\chi_e)E_{ext}\qquad\mbox{(wrong answer)}$$

To see why this is wrong, consider the physical implications of this equation when $\chi_e>1$ (for example, for water).



