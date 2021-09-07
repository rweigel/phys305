# Binomial Expansion Limit

The Binomial Theorem is

$$(x+y)^m = \sum_{k=0}^m {m \choose k}x^{m-k}y^k$$

When $x=1$, it simplifies to

$$(1+y)^m = \sum_{k=0}^m {n \choose k}y^k$$

Written as a power series, it is

$$(1+y)^m = 1 + my + m(m-1)y^2 + ...$$

From this, it follows that

$$\frac{1}{(1+y)^n} = 1 + my + m(m-1)y^2 + ...$$

(This equation can also be derived using the Taylor series expansion around $y=0$.)

In this course, we are going to use this expansion many times when $y$ is small. To emphasize this, $\delta$ will be used instead of $y$ as the variable. 

$$\frac{1}{(1+\delta)^n} = 1 - n\delta + n(n-1)\delta^2+...$$


The actual equation that you will use and should memorize is the truncated expansion to first order in $\delta$:

$$\boxed{\frac{1}{(1+\delta)^n} \simeq 1 - n\delta}$$

> "First--order in $\delta$" means that the highest power in the approximate answer is $\delta$, so only the $n\delta$ terms is kept as in the boxed equation above. "Second--order in $\delta$" means that the $n(n-1)\delta^2$ term is kept.

This equation becomes more and more accurate as $\delta \rightarrow 0$.

We will use this equation repeatedly to check our answers -- typically, we will be able to say, "For large $\delta$, I expect the answer to approach the answer to a similar to the answer for a simpler problem for which I know the answer". For example, if the problem is to compute the electric field for two positive charges $q$ at $x=\pm 1$, we expect the electric field to approach that for a charge of $2q$ at the origin, which is simply $2kq\hat{\mathbf{r}}/r^2$. This statement allows you to check your equation for the electric field -- if for large $r$ your equation matches the equation at the origin, you will be more confident that you solved the problem correctly.

To use this equation, you will typically need to rewrite an equation so that a term of this form appears. This is demonstrated in the following examples.

## Example

Approximate $\frac{1}{12}$ using ${1}/{(1+\delta)^n} \simeq 1 - n\delta$.

**Answer**

$\displaystyle\frac{1}{12}=\frac{1}{10}\frac{1}{1+\frac{2}{10}}$

In this equation, we identify $n=1$ and $\delta = 2/10$, so

$\displaystyle\frac{1}{12}\simeq\frac{1}{10}\left(1-\frac{2}{10}\right)=\frac{1}{10}\frac{8}{10}=\frac{8}{100}=0.08$

This is close to the exact answer of $1/12=0.08\overline{3}$.

## Example

Approximate $\{1}/{(3 + x)^2}$ using the binomial expansion to first order in $x$. Check your answer by using $x=0.1$ in the given equation and your approximation.

**Answer**:

Here $n=2$ and we can rewrite the equation by factoring out the $3$ from the term in the denominator to obtaiin a term of the form ${1}/{(1+\delta)^n}$

$\displaystyle\frac{1}{(3 + x)^2}=\frac{1}{3^2}\frac{1}{(1 + \frac{x}{3})^2}$

In the above, we identify $\delta=x/3$ and so

$\displaystyle\frac{1}{3^2}\frac{1}{(1 + \frac{x}{3})^2}\simeq\frac{1}{3^2}\left[1-2\left(\frac{x}{3}\right)\right]=\frac{1}{3^2}\left(1-\frac{2}{3}x\right)$

When $x=0.1$, the exact answer to four decimal places is $1/(3.1)^2=0.1041$. The approximate answer is $0.1037$

## Problem

Approximate ${1}/{\sqrt{a + x}}$ using the binomial expansion to first order in $x$. Check your answer by using plugging $a=1$ and $x=0.1$ into the given equation and your approximation. They should be close.

## Problem

The exact answer for the electric field in the $y=0$ plane due to a line of charge with charge density $\lambda$ between $\pm L$ on the $x$--axis is

$$\mathbf{E} = \frac{k\lambda}{z}\left[\left(-1+\frac{z}{\sqrt{z^2+L^2}}\right)\hat{\mathbf{x}} + \left(\frac{L}{\sqrt{z^2+L^2}}\right)\hat{\mathbf{z}}\right]$$

Expand the term in square braces to first order in $z$. Note that $\sqrt{z^2}=|z|$.

## Problem

Find the equation for the electric field for two positive charges $q$ at $x=\pm a$. Verify that for large $r/a$, this equation approaches the equation for the electric field for $2q$ at the origin.
