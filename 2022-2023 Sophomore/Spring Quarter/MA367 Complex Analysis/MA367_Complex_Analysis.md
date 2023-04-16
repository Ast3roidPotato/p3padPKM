---
excalidraw-default-mode: view
---

```toc

```

^TOC

<[[|previous]] | [[|next]]>

## Day 1 - 2023-03-06
### Why Complex Numbers
Integer $\mathbb{Z}$
Rational $\mathbb{Q} = \{\frac{p}{q}:p,q\in\mathbb{Z}, q\neq0\}$
Real: $\mathbb{R}=(-\infty,\infty)$
Complex: $\mathbb{C}=\{a+b\cdot i:a,b\in\mathbb{R}\}$

> All sets of numbers are supersets of their predecessors - called <span style='color: orange;'>set containments</span>
> $$\mathbb{Z}\subset\mathbb{Q}\subset\mathbb{R}\subset\mathbb{C}$$

Complex numbers arose from when solutions to cubic equations were found with negative numbers inside the radicals. (Check this??)

### Complex Number Review

$$i=\sqrt{-1}$$
Normal complex number: $z=a+bi$
Modulus: $|z| = \sqrt{a^2 + b^2}$
Complex Conjugate: $z = a + bi \to \bar{z} = a - bi$

**Division:**
When dividing two complex numbers, $\frac{z}{w}$, multiply the fraction by $\frac{\overline{w}}{\overline{w}}$ to make the denominator a real number.

**Example:**
$$\frac{2+i}{3-4i} \to \frac{2+i}{3-4i}\cdot\frac{3+4i}{3+4i}\to \frac{6+8i+3i-4}{9+12i-12i+16}\to\boxed{\frac{2}{25}+\frac{11i}{25}}$$

#### Useful Facts/Identities
$$|z|^2=z\bar{z}$$
$$z+\bar{z} = 2\text{Re}(z)$$
$$z-\bar{z} = 2\text{Im}(z)$$
$$|z\cdot w|=|z|\cdot|w|$$
$$|z/w|=|z|/|w|$$
$$|z^n|=|z|^n$$

### Polar form and Geometry of Complex Numbers
$z=a+bi$ is the point on the complex plane with points $(a,b)$.

**Euler Identity:** $e^{i\theta}=\cos(\theta)+i\sin(\theta)$

The polar or Euler form of a complex number is generally easier to work with due to being able to take advantage of power rules.

![[Pasted image 20230309131051.png]]

#### Example:
> Find the polar form of $z=-1+\sqrt3i$ where $-\pi<\theta\leq\pi$

First, find radius $r$
$$r=|z|=\sqrt{1+3}$$
$$r=2$$

Then find angle $\theta$
$$\tan(\theta) = \frac{\sqrt{3}}{-1}$$
$$\theta = \tan^{-1}(-\sqrt3)$$
><span style='color: orange;'>Important!</span>  The range of arctan is $(-\frac{\pi}{2},\frac{\pi}{2})$, so it can output an answer in the wrong quadrant. That is why it is important to think about which direction the actual vector is pointing so you can determine if you need to add $\pi$ to the result so you can get it into the correct quadrant.

![[Pasted image 20230309134342.png]]
$$\tan^{-1}(-\sqrt3)=-\frac{\pi}{3}$$
This is in the wrong quadrant, so we add $\pi$ to correct for this.
$$\theta = \frac{2\pi}{3}$$
$$\boxed{z=2e^{\frac{2\pi i}{3}}}$$

#### Example 2:
> Compute $(1+i)^{10}$

Draw a picture of the starting number:
![[Pasted image 20230326172455.png]]
Find radius $r:$
$$r = sqrt(2)$$
Find angle $\theta :$
$$\theta = \arctan(1)$$
$$\theta = \frac{\pi}{4}$$
<span style='color: orange;'>Make sure that this value of $\theta$ makes sense!</span>
In this case it does, so we don't need to add $\pi$.

$$(\sqrt2e^{\frac{\pi i}{4}})^{10}$$
$$(2^{\frac{1}{2}})^{10}\cdot e^{\frac{10\pi i}{4}}$$
$$2^5\cdot e^{\frac{5\pi i}{2}}$$
$$32i$$


#### Property
> Multiplying complex numbers:
> 	Radii multiply - angles add

### Nth Roots
> Find the 3rd roots of 8.

Want $z^3 = 8$

First draw a picture!
![[Pasted image 20230326173803.png]]

Then express the target number in exponential form and solve:
$$z^3 = 8=8e^{i\cdot2\pi k}\quad k\in\mathbb{Z}$$
$$z = (8e^{i\cdot2\pi k})^\frac{1}{3}$$
$$z = 2e^{\frac{2\pi ik}{3}}$$
For Nth roots of a number, there will be N unique values for $k$. In this case, $k=0,1,2.$
$$k = 0, z = \boxed{2}$$
$$k = 0, z = 2e^\frac{2\pi i}{3} = \boxed{-1+\sqrt3}$$
$$k = 0, z = 2e^\frac{4\pi i}{3} = \boxed{-1-\sqrt3}$$


>  **Note:** Nth roots form regular polygons over the complex plane.


## Reading Pages 1-10
Instead of F.O.I.L, F.L.O.I generally groups terms better for complex multiplication.
Division is done by multiplying be 1 in a clever way.

To divide 2 complex numbers $\frac{z}{w}$, multiple the fraction by $\frac{\overline{w}}{\overline{w}}$ in order to realize the denominator.

When approaching a complex point, you can approach it from any direction on the complex plane. This is called the <span style='color: violet;'>Argand Plane</span>.

## Day 2 - 2023-03-07

For normal real valued numbers, we can compare them with inequalities. This is <u>not</u> the case with complex numbers.
$$\mathbb{C}\,\text{is not an ordered field}$$
Distance between 2 complex numbers of the modulus of the difference between the points.
### Property:
> **Note:** The sum of conjugates is the conjugate of sums

$$ {\over (z+w)} = \bar{z}+ \bar{w}$$

### The Triangle Inequality
This is very important! "Complex analysis is basically applications of the triangle inequality."

It is defined by:
$$\forall z,w \in\mathbb{C}:|z+w|\leq|z|+|w|$$
