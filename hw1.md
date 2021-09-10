Due on Thursday, September 2nd at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. If you do not have a scanner, use a smartphone PDF scanning app such as Genius Scan or Adobe Scan. **Do not send photos of your assignment.** If you have difficulty with this, feel free to contact me for help.

You are welcome to ask questions about homework problems on Discord. I will not give direct answers, but I will give hints. I will also first ask you for your solution to a related problem that was covered in class or in the notes. You are welcome to answer questions from other students on Discord, but please only give suggestions and hints.

This homework involves topics covered in [Vectors](vectors.html), [Vector Fields](vector_fields.html), [Field Lines](field_lines.html), and  [Equipotentials](equipotentials.html). 
 
# Vector Notation

Given $\mathbf{r}$ is a vector from the origin to the point $(x,y,z)$ and $\mathbf{r}'$ is a vector from the origin to the point $(x',y',z')$ and a scalar function $f$ defined according to

$$f = \frac{1}{|\mathbf{r}-\mathbf{r}'|^2}$$

1. Write $f$ in cartesian coordinates.

2. Show that $|\mathbf{r}-\mathbf{r}'|^2$ can be written as $r^2+r'^2-2\mathbf{r}\cdot\mathbf{r}'$

3. Compute $\boldsymbol{\nabla}\left(\frac{1}{|\mathbf{r}-\mathbf{r}'|}\right)$, where $\boldsymbol{\nabla}f(x,y,z)=\frac{\partial f}{\partial x}\xhat+\frac{\partial f}{\partial y}\yhat+\frac{\partial f}{\partial z}\zhat$

4. If $\textbf{\char"0509} \equiv \mathbf{r}-\mathbf{r}'$

    a. Show that

    $$\frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}=\frac{\phantom{|}\mathbf{r}-\mathbf{r}'\phantom{|^3}}{|\mathbf{r}-\mathbf{r}'|^3}$$

    b. Write $\hat{\textbf{\char"0509}}/{\char"0509^2}$ in cartesian coordinates with cartesian unit vectors.

**Answer**

1. $\displaystyle f = \frac{1}{(x-x')^2+(y-y')^2+(z-z')^2}$
2. There are several ways of doing this.

   1. Use the law of cosines. If $\varphi$ is the angle between two lines of length $r$ and $r'$ with both having an endpoint at the origin, then from the law of cosines, 
    $C^2=r^2 + r'^2 - 2rr'\cos\varphi$.

    From the definition of the dot product, $2rr'\cos\varphi=2\mathbf{r}\bfcdot \mathbf{r}'$, giving 
    
    $C^2=r^2+r'^2-2\mathbf{r}\bfcdot \mathbf{r}'$.
    
    In this equation $C^2 = |\mathbf{r}-\mathbf{r}'|^2$ from vector addition, so finally
    
    $|\mathbf{r}-\mathbf{r}'|^2=r^2+r'^2-2\mathbf{r}\bfcdot \mathbf{r}'$

   2. Use $|\mathbf{r}-\mathbf{r}'|^2=(\mathbf{r}-\mathbf{r}')\bfcdot (\mathbf{r}-\mathbf{r}')$ with $\mathbf{r}=x\xhat + y\yhat + z\zhat$ and $\mathbf{r}'=x'\xhat + y'\yhat + z'\zhat$. This gives

      $x^2+y^2+z^2 + x'^2+y'^2+z'^2 - 2(xx' + yy' + zz') = r^2+r'^2-2\mathbf{r}\bfcdot\mathbf{r}'$

   3. Use $|\mathbf{r}-\mathbf{r}'|^2=(\mathbf{r}-\mathbf{r}')\bfcdot (\mathbf{r}-\mathbf{r}')$. This expands to $ \mathbf{r}\bfcdot\mathbf{r}-2\mathbf{r}\bfcdot\mathbf{r}'+\mathbf{r}'\bfcdot\mathbf{r}'=r^2+r'^2-2\mathbf{r}\bfcdot\mathbf{r}'$. You can get the correct answer using sloppy notation and this method. Some students wrote that the dot product gives $r^2+r'^2-2rr'$ and then replaced $2rr'$ with $2\mathbf{r}\bfcdot\mathbf{r}'$, which is not valid.
    

3. &nbsp;

   Let $\displaystyle g = \frac{1}{|\mathbf{r}-\mathbf{r}'|} =\left[(x-x')^2+(y-y')^2+(z-z')^2\right]^{-1/2}$

   $\displaystyle \xhat\frac{\partial g}{\partial x} =\xhat\frac{\partial}{\partial x} \left[(x-x')^2+(y-y')^2+(z-z')^2\right]^{-1/2}$

   Using the chain rule, this is
   
   $\displaystyle \phantom{ \xhat\frac{\partial g}{\partial x}} = \frac{-\frac{1}{2}2(x-x')}{\left[(x-x')^2+(y-y')^2+(z-z')^2\right]^{3/2}}\xhat$

   $\displaystyle \phantom{ \xhat\frac{\partial g}{\partial x}} = -\frac{(x-x')}{\left[(x-x')^2+(y-y')^2+(z-z')^2\right]^{3/2}}\xhat$

   Other terms have the same denominator with variables and unit vector in numerator changed.

   $\displaystyle \yhat\frac{\partial g}{\partial y} = -\frac{(y-y')}{\left[(x-x')^2+(y-y')^2+(z-z')^2\right]^{3/2}}\yhat$
  
   $\displaystyle \zhat\frac{\partial g}{\partial z} = -\frac{(z-z')}{\left[(x-x')^2+(y-y')^2+(z-z')^2\right]^{3/2}}\zhat$

   The sum of the above three terms is an acceptable answer but note that it simplifies to

   $\boldsymbol{\nabla}\left(\frac{1}{|\mathbf{r}-\mathbf{r}'|}\right)=\displaystyle -\frac{\phantom{|}\mathbf{r}-\mathbf{r}'\phantom{|^3}}{|\mathbf{r}-\mathbf{r}'|^3}=-\frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}$
  
   because the denominator in each term is $|\mathbf{r}-\mathbf{r}'|^3$. This can also be written as $-\mathbf{\hat{r}}/r^2$

   Now that you've done this the hard way to practice notation, I'll tell you the easier way. Use $\boldsymbol{\nabla}t$ in spherical coordinates (see second--to--last page of Griffiths). Only the $\mathbf{\hat{r}}$ term is non--zero when $t=t(r)$ and so $\boldsymbol{\nabla}t(r)=\mathbf{\hat{r}}\partial t/\partial r=-\mathbf{\hat{r}}/r^2$. We were actually given $t=t(\char"0509)$, so we must evaluate $\boldsymbol{\nabla}t(\char"0509)=\hat{\textbf{\char"0509}}\partial t/\partial \char"0509=-{\hat{\textbf{\char"0509}}\phantom{^2}}/{\char"0509^2}$.

4. &nbsp;
 
   a. Substitute $\char"0509=|\mathbf{r}-\mathbf{r}'|$ and $\displaystyle {\hat{\textbf{\char"0509}}}=\frac{\phantom{|}\mathbf{r}-\mathbf{r}'\phantom{|}}{|\mathbf{r}-\mathbf{r}'|}$ into $\displaystyle \frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}$

   b. Use $\mathbf{r}=x\xhat+y\yhat+z\zhat$ and $\mathbf{r}'=x'\xhat+y'\yhat+z'\zhat$ to get

      $\displaystyle \frac{\hat{\textbf{\char"0509}}}{\char"0509^2} = \frac{(x-x')\xhat+(y-y')\yhat+(z-z')\zhat}{\left[(x-x')^2+(y-y')^2+(z-z')^2\right]^{3/2}}$

# Tangent Vectors

An object is moved along the path $y=x^2$ from $x=0$ to $x=x_o$ when there is an external force of $\mathbf{F}=-mg\yhat$.

1\. Compute the force tangent to the path at $x_o/2$ and $x_o$.

2\. Compute the force perpendicular to the path at $x_o/2$ and $x_o$.

3\. (Extra credit) Compute $\int_{\mathcal{L}}\mathbf{F}\cdot d\mathbf{l}$ where $\mathcal{L}$ is the path along $y=x^2$ from $x=0$ to $x=x_o$.

**Answer**

For 1. and 2., The problem statement does indicate if the answer should be a vector or scalar. I accepted either.
 
1\.

$\displaystyle \mathbf{\hat{t}}=\frac{\xhat + 2x\yhat}{\sqrt{1+4x^2}}$

$\displaystyle F_{\parallel} = \mathbf{F}\bfcdot \mathbf{\hat{t}} = (-mg\yhat)\bfcdot \frac{\xhat + 2x\yhat}{\sqrt{1+4x^2}}= -\frac{2mgx}{\sqrt{1+4x^2}}$

This is a scalar b/c of the dot product. It is the component of force in the direction of chosen $\mathbf{\hat{t}}$. The negative is there because the component of $\mathbf{F}$ is in the opposite direction of the chosen $\mathbf{\hat{t}}$.

$\displaystyle \mathbf{F}_{\parallel} = F_\parallel \mathbf{\hat{t}}= -\frac{2mgx}{\sqrt{1+4x^2}}\frac{\xhat + 2x\yhat}{\sqrt{1+4x^2}}=-\frac{2mgx}{1+4x^2}(\xhat + 2x\yhat)$

For $x>0$, the direction of this vector is down and to the left, as expected.

2\.

$\displaystyle \mathbf{\hat{n}}=\frac{-2x\xhat+\yhat}{\sqrt{1+4x^2}}$

$\displaystyle F_{\perp} = \mathbf{F}\bfcdot \mathbf{\hat{n}}=\frac{-mg}{\sqrt{1+4x^2}}$

This is a scalar b/c of the dot product. It is the component of force in the direction of chosen $\mathbf{\hat{n}}$. The negative is there because the component of $\mathbf{F}$component of $\mathbf{F}$ is the opposite direction of the chosen $\mathbf{\hat{n}}$.

$\displaystyle \mathbf{F}_{\perp} = F_\perp \mathbf{\hat{n}}=\frac{mg}{1+4x^2}(2x\xhat-\yhat)$

For $x>0$, the direction of this vector is to the right and down, as expected.

Could also compute $\mathbf{F}_\perp$ using $\mathbf{F}_\perp = \mathbf{F}-\mathbf{F}_\parallel$.

3\. The problem asks to integrate along the line. For the path given, $dl = dx\sqrt{1+2x^2}$ and  $d\mathbf{l}=\mathbf{\hat{t}}dl$, so $\mathbf{F}\bfcdot d\mathbf{l} = -mgdx$. The integral is then $\int_{0}^{x_o}(-2mgxdx)=-mgx_o^2$. The integral corresponds to the work done moving the object a height $h=x_o^2$. The easier way to solve this is to to note that $\mathbf{F}$ is a conservative force and simply write $mgh$ and then plug in $h=x_o^2$. (Ideally I would have given the equation as $y=x^2/x_o$ so $h$ would not look like it is the square of a distance. Technically the problem statement is still correct because impicitly $x_o$ is dimensionless.)1.2.3.

# Normal Vectors

A plane has corners at $(x,y,z)=(0,0,0)$, $(x,y,z)=(1,0,0)$, $(x,y,z)=(0,1,1)$, and $(x,y,z)=(1,1,1)$. 

1\. Sketch the plane with a 3--dimensional diagram.

2\. Sketch the plane in the $y$--$z$ plane. (That is, what you would see if you looked toward the origin from a point with large $x$.)

3\. Find a vector normal to the plane that has a positive $z$--component.

4\. There is a force acting on the plane of $\mathbf{F}=F_x\xhat+F_y\yhat+F_z\zhat$. Find the component of force perpendicular to the plane.

**Partial Answer**

3\. $\mathbf{\hat{n}}=(-\yhat + \zhat)/\sqrt{2}$; this can be computed using the diagram or by using the $\mathbf{u}\times \mathbf{v}$ method.

4\. $F_\perp = \mathbf{F}\bfcdot \mathbf{\hat{n}}=-F_y+F_z$ and $\mathbf{F}_\perp=F_\perp\mathbf{\hat{n}}=(-F_y+F_z)(-\yhat + \zhat)/\sqrt{2}$. Ideally you drew $\mathbf{F}$ and $\mathbf{\hat{n}}$ on the diagram for 2. to make sure that the direction of $\mathbf{F}_\perp$ made sense by plugging in, say, $F_y=F_z=1$ and $F_y=0$ and $F_z=1$. 

# Notation and Vector Fields

A positive charge $q$ is placed at $(x,y)=(x_o,0)$ and a negative charge $-q$ at $(x,y)=(-x_o,0)$.

The force on a charge $Q$ due to $q$ and $-q$ is

$$\mathbf{F}=kqQ\frac{\hat{\textbf{\char"0509}}\_+}{\char"0509^2\_+}-kqQ\frac{\hat{\textbf{\char"0509}}\_{-}}{\char"0509^2\_{-}}$$

where $\textbf{\char"0509}\_+=\mathbf{r}-\mathbf{r\_+}$, $\textbf{\char"0509}\_-=\mathbf{r}-\mathbf{r\_-}$, $\mathbf{r}=x\xhat + y\yhat$, $\mathbf{r\_+}$ is the vector from the origin to the positive charge, and $\mathbf{r\_-}$ is the vector from the origin to the negative charge.

Find $\mathbf{F}$ in cartesian coordinates with cartesian unit vectors in terms of the constants given at

% TODO: Change to (2x_o, 0) and (0, 2x_o)

1\. $(x,y)=(2,0)$

2\. $(x,y)=(0,2)$

It may help to solve this by using the techniques from Physics 260 first. This is a straightforward problem that is written in the notation used by Griffiths.

**Answer**

$\displaystyle\mathbf{F}(x,y) = kqQ\left[\frac{(x-x_o)\xhat+y\yhat}{\left[(x-x_o)^2+y^2\right]^{3/2}}-\frac
{(x+x_o)\xhat+y\yhat}{\left[(x+x_o)^2+y^2\right]^{3/2}}\right]$

1\. $\displaystyle\mathbf{F}(x,y) = kqQ\left[\frac{2-x_o}{|2-x_o|^3}-\frac
{2+x_o}{|2+x_o|^3}\right]\xhat=kqQ\left[\frac{1}{(2-x_o)^2}-\frac
{1}{(2+x_o)^2}\right]\xhat$

2\. $\displaystyle\mathbf{F}(x,y) = kqQ\left[\frac{-x_o\xhat+2\yhat}{\left[x_o^2+2^2\right]^{3/2}}-\frac
{x_o\xhat+2\yhat}{\left[x_o^2+2^2\right]^{3/2}}\right] = -kqQ2x_o\left[\frac{1}{\left[x_o^2+2^2\right]^{3/2}}\right]\xhat$

# Field Lines and Equipotentials

1\. Draw field lines associated with the two starting points shown in the diagram for $\mathbf{A}=-\sin\phi\xhat + \cos\phi\yhat$. Draw the field lines until they encounter the $-x$--axis.

2\. Sketch four equipotential lines.

<img src="figures/Field_Lines_3.svg" width=100%/>

1\. Field lines are circles.

2\. "Equipotentials" are radial lines that intersect the origin. As noted in class, this is not a conservative field and so it does not make sense to draw equipotentials. I meant to ask you to draw lines that are always perpendicular to the field lines. This vector field is not conservative because the integral $\int_{\mathcal{L}}\mathbf{A}\bfcdot d\mathbf{l}$ is not the same for all paths that have the same starting and ending points. For example, if $\mathcal{L}_1$ is a single circle with a radius of $1$, the integral is $2\pi$. If $\mathcal{L}_2$ is $\mathcal{L}_1$ repeated twice, the integral is $4\pi$.

