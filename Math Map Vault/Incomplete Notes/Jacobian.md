# Jacobian

---

Linear transformations have three properties:

- the $\vec{0}$ vector is mapped to the $\vec{0}$ vector
- parallel lines stay parallel
- evenly spaced points stay evenly spaced

Linear transformations can be represented using matrices. Any region is scaled by the transformation into a new region, whose length/area/volume is larger by some factor. This factor is the same for all regions, and is the determinant of the matrix which represents the linear transformation.

Given a function $f(x)$ from $\mathbb{R}$ -> $\mathbb{R}$ and a point $a$ in the domain, we could zoom in on the neighborhood around $a$ (and also $f(a)$) so that $f$ appears to be a linear map. In this zoomed-in perspective, the points near $a$ might be scaled at $f(a)$ by some constant factor, which for the sake of example let's suppose is $3$. This is the derivative of $f(x)$ at $a$, or in other words the Jacobian matrix is $[3]$. Depending on the value of $a$, the Jacobian matrix and the derivative will have different values (assuming $f(x)$ isn't a linear function).

