# Galois Theory

---

We have a fundamental problem in algebra, which is this: how can we solve polynomials?

An nth degree polynomial $P(X) = a_nx^n + a_{n-1}x^{n-1} + a_{n-2}x^{n-2} + ... + a_2n^2 + a_1x^1 + a_0$

We want to find an equation which gives us the roots of the equation in terms of the coefficients.

Quadratic formula for $y = ax^2 + bx + c$ :
$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$

We could think of the quadratic formula as giving us $x$ values, or we could think of it as an algebraic expression for $x$. Say that $r^2 = b^2 - 4ac$. Then
$x_1 = \frac{-b + r}{2a}$
$x_1 = \frac{-b - r}{2a}$

We can think of $\sqrt{2}$ as either

- a number, so that $\sqrt{2}$ is equal to approximately 1.414
- a symbol, so that $\sqrt{2}$ has the property that: $(\sqrt{2})^2 = 2$

The first way is more numerical and "analytic", while the second is more "algebraic". Similarly, we can think of the quadratic formula as being more analytic vs more algebraic.

Say we have a quartic equation $x^4 + px^2 + qx + r = 0$. Assume that we've eliminated the $x^3$ term with some type of substitution.

We can factor the equation into $(x^2 + ax + b)(x^2 + cx + d) = 0$

We could expand that equation and compare the coefficients to the original quartic to get that:

- $0 = a + c$
- $p = b + d + ac$
- $q = ad + bc$
- $r = bd$

We'd want to solve for $c$, $b$, and $d$ in terms of $a$, which would allow us to obtain an equation only in terms of $a$:

$a^6 + 2pa^4 + (p^2 - 4r)a^2 - q^2 = 0$

This is a cubic equation in terms of $a^2$, which we can solve and take the square root to find $a$. Then you get that the quartic equation factors as:

$(x^2 + ax + (\frac{a^2}{2} + \frac{p}{2} - \frac{q}{2a}))\cdot(x^2 - ax + (\frac{a^2}{2} + \frac{p}{2} + \frac{q}{2a}))$



---