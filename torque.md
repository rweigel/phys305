
In the previous section, you considered forces on the current loops when $\mathbf{B}=B_o\hat{\mathbf{z}}$. The forces on all of the current loops that you drew in Problem 1.1 should have been such that the loop did not translate or rotate (the net force should have been zero).

A current loop in a constant magnetic field will never experience a net force, and you should have found in the previous section that the net force on each loop was zero. The explanation for this is not covered in your textbook, but you will or have probably encountered this in your Calculus class.

To see why a current loop in a constant magnetic field will never experience a net force, rewrite: 

$$\mathbf{F}=I\int d\mathbf{l}\times\mathbf{B}$$

using the vector identity $\mathbf{U}\times\mathbf{V}=-\mathbf{V}\times \mathbf{U}$

$$\mathbf{F}=-I\int \mathbf{B}(\mathbf{l})\times d\mathbf{l}$$

where the dependence of $\mathbf{B}$ on $\mathbf{l}$ has been made explicit; that is, in general the magnetic field depends on the position $\mathbf{l}$ along the wire. {\bf If} the magnetic field is independent of $\mathbf{l}$, it can be factored out of the integral

$$\mathbf{F}=-I\mathbf{B}\times\int d\mathbf{l}$$

Recall that this is similar to a key step that was used in Gauss's law -- when the electric field did not vary over the closed surface of integration and its direction relative to the surface's normal did not change, we could factor the electric field out of the integral: $\oint \mathbf{E}\cdot d\mathbf{A}=E\oint dA=EA$. Only when this step was possible was Gauss's law useful in finding the electric field, and this step was only possible for certain charge configurations.

If the loop is closed, we replace $\int$ with $\oint$, so we have

$$\mathbf{F}=-I\mathbf{B}\times\oint d\mathbf{l}$$

The integral is zero. To see that this is reasonable, consider the vectors for $\mathbf{L}$ that you found for loops a. and b. In Problem 1.1. They summed to zero. In the above integral, we are adding differential vectors around a loop. Break the differential vector into horizontal and vertical components. To go in a loop, for every step to the right, you have to have had made a step to the left. Same for up/down. Therefore $\oint d\mathbf{l}=0$ and so $\mathbf{F}=0$.

The general equation for computing the torque on a current loop that lies in a plane is:

$$\boldsymbol{\tau} = \boldsymbol{\mu}\times\mathbf{B}$$

where $\boldsymbol{\mu}$ is the magnetic moment defined as $\boldsymbol{\mu}=I\mathbf{A}$ and $\mathbf{A}$ is the area vector for a loop. The magnitude of the area vector is simply the area of the loop. The direction of the area vector is determined by a right-hand-rule: wrap your fingers along the direction of current and your thumb points in the direction of the area vector.

The equation $\boldsymbol{\tau} = \boldsymbol{\mu}\times\mathbf{B}$ predicts that when $\mathbf{A}$ is perpendicular to $\mathbf{B}$, the torque magnitude is the largest. To see this, note that $\boldsymbol{\mu}\times\mathbf{B}$ can be equivalently written as $\mu A\sin\phi$, where $\phi$ is the angle between $\boldsymbol{\mu}$ and $\mathbf{B}$. When $\phi = \pm 90^\circ$, the cross product will have the largest magnitude.
