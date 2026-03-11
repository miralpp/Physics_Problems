# Section 0: Mathematical Foundations - Comprehensive Solutions

---

## 1. Vector Algebra: 3D Spatial Analysis
Given vectors: $\vec{a} = [2, 1, -3]$ and $\vec{b} = [4, -2, 1]$.

### a) Vector Magnitudes (Euclidean Norm)
The magnitude represents the "length" of the vector from the origin to its tip. It is calculated using a 3D version of the Pythagorean theorem: $|\vec{v}| = \sqrt{x^2 + y^2 + z^2}$.
* **For $\vec{a}$:** $|\vec{a}| = \sqrt{2^2 + 1^2 + (-3)^2} = \sqrt{4 + 1 + 9} = \mathbf{\sqrt{14}} \approx 3.74$ units.
* **For $\vec{b}$:** $|\vec{b}| = \sqrt{4^2 + (-2)^2 + 1^2} = \sqrt{16 + 4 + 1} = \mathbf{\sqrt{21}} \approx 4.58$ units.

### b) Dot Product (Scalar Product)
The dot product measures how much one vector projects onto another. The result is a **scalar** (a single number), not a vector.
* $\vec{a} \cdot \vec{b} = (a_x \cdot b_x) + (a_y \cdot b_y) + (a_z \cdot b_z)$
* $\vec{a} \cdot \vec{b} = (2 \cdot 4) + (1 \cdot -2) + (-3 \cdot 1) = 8 - 2 - 3 = \mathbf{3}$
* *Insight:* Since the result is positive, the angle between the vectors is acute ($< 90^\circ$).

### c) Cross Product (Vector Product)
The cross product creates a new vector that is perfectly perpendicular (orthogonal) to both $\vec{a}$ and $\vec{b}$. This is essential in physics for calculating torque or magnetic forces.

$$
\vec{a} \times \vec{b} = \det \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & 1 & -3 \\ 4 & -2 & 1 \end{vmatrix}
$$
* **i component:** $(1 \cdot 1) - (-3 \cdot -2) = 1 - 6 = -5$
* **j component:** $-[(2 \cdot 1) - (-3 \cdot 4)] = -(2 + 12) = -14$
* **k component:** $(2 \cdot -2) - (1 \cdot 4) = -4 - 4 = -8$
* **Resulting Vector:** $\mathbf{[-5, -14, -8]}$

### d) Angle Between Vectors
Using the geometric identity $\vec{a} \cdot \vec{b} = |\vec{a}| |\vec{b}| \cos(\theta)$:
* $\cos(\theta) = \frac{3}{\sqrt{14} \cdot \sqrt{21}} = \frac{3}{\sqrt{294}} \approx 0.175$
* $\theta = \arccos(0.175) \approx \mathbf{79.9^\circ}$

---

## 2. Systems of Linear Equations
Solve for $x$ and $y$:
1. $2x + 3y = 12$
2. $x - y = 1$

**Method: Substitution**
From the second equation, we isolate $x$: $x = y + 1$.
Substitute this into the first equation:
$2(y + 1) + 3y = 12 \implies 2y + 2 + 3y = 12 \implies 5y = 10 \implies \mathbf{y = 2}$
Now, find $x$: $x = 2 + 1 = \mathbf{3}$.
* **Geometric Meaning:** These two lines intersect at the point $(3, 2)$ on a Cartesian plane.

---

## 3. Universal Law of Gravitation (Proportionality)
Formula: $F = G \frac{m_1 m_2}{r^2}$

**Applying the Changes:**
* Masses are halved: $m_1 \to \frac{m_1}{2}$, $m_2 \to \frac{m_2}{2}$ (The numerator becomes $1/4$ of the original).
* Distance is doubled: $r \to 2r$. Because $r$ is squared, the denominator becomes $(2r)^2 = 4r^2$ (The denominator is 4 times larger).

**Calculating the New Force ($F'$):**
$$F' = G \frac{(m_1/2)(m_2/2)}{(2r)^2} = G \frac{m_1 m_2 / 4}{4r^2} = \frac{1}{16} \left( G \frac{m_1 m_2}{r^2} \right) = \frac{1}{16}F$$
* **Conclusion:** The gravitational force decreases by a factor of **16**. Distance has a much stronger impact than mass due to the inverse-square relationship.

---

## 4. Rearranging the Pendulum Formula
Isolate $g$ from the period formula: $T = 2\pi \sqrt{\frac{L}{g}}$

1. Divide by $2\pi$: $\frac{T}{2\pi} = \sqrt{\frac{L}{g}}$
2. Square both sides to remove the radical: $\frac{T^2}{4\pi^2} = \frac{L}{g}$
3. Invert both sides (or cross-multiply): $\frac{4\pi^2}{T^2} = \frac{g}{L}$
4. Multiply by $L$: $\mathbf{g = \frac{4\pi^2 L}{T^2}}$

---

## 5. Trigonometric Component Analysis
A vector $\vec{A}$ with magnitude $15$ at an angle of $60^\circ$ from the horizontal.

* **Horizontal Component ($A_x$):** Since it is the adjacent side, we use cosine. $15 \cdot \cos(60^\circ) = 15 \cdot 0.5 = \mathbf{7.5}$
* **Vertical Component ($A_y$):** Since it is the opposite side, we use sine. $15 \cdot \sin(60^\circ) = 15 \cdot \frac{\sqrt{3}}{2} \approx \mathbf{12.99}$

---

## 6. Function Analysis & Calculus Optimization
Function: $f(x) = 3x^2 - 12x + 7$

1. **Find Critical Points:** Take the first derivative and set it to zero.
   $f'(x) = 6x - 12$. Setting $f'(x) = 0 \implies 6x = 12 \implies \mathbf{x = 2}$.
2. **Determine the Nature (Second Derivative Test):**
   $f''(x) = 6$. Since the second derivative is positive ($> 0$), the function is concave up at this point. This confirms $x = 2$ is a **Local Minimum**.
3. **Find the Value:** $f(2) = 3(2)^2 - 12(2) + 7 = 12 - 24 + 7 = \mathbf{-5}$.

---

## 7. The Fly and the Bicycle (Relative Motion Logic)
This is a classic logic puzzle often associated with John von Neumann. While it looks like an infinite series problem, the "time-based" approach is much faster.

* **Total Time:** The bicycle travels 10 meters at 1 m/s. It will hit the wall in $t = 10 / 1 = \mathbf{10\text{ seconds}}$.
* **The Fly's Journey:** The fly travels at a constant speed of $2\text{ m/s}$ for the entire 10 seconds, regardless of how many times it turns around.
* **Total Distance:** $Distance = Speed \cdot Time = 2\text{ m/s} \cdot 10\text{ s} = \mathbf{20\text{ meters}}$.

---

## 8. Definite Integral (Area Under Curve)
Calculate the area under $f(x) = \sin(x)$ from $x = 0$ to $x = \pi$:

$$Area = \int_{0}^{\pi} \sin(x) dx = [-\cos(x)]_{0}^{\pi}$$
* Evaluate at upper limit: $-\cos(\pi) = -(-1) = 1$
* Evaluate at lower limit: $-\cos(0) = -(1) = -1$
* Subtract: $1 - (-1) = \mathbf{2}$ square units.

---

## 9. Geometric Optimization
Maximize the area $A = x \cdot y$ for a rectangle under the curve $y = 3 - x^2$ in the first quadrant.
1. **Area Function:** $A(x) = x(3 - x^2) = 3x - x^3$
2. **Differentiate:** $A'(x) = 3 - 3x^2$
3. **Find Roots:** $3(1 - x^2) = 0 \implies x = 1$ (since $x$ must be positive).
4. **Find Height:** $y = 3 - (1)^2 = \mathbf{2}$.
5. **Dimensions:** The rectangle with the maximum area has a **width of 1 and a height of 2**.

---

## 10. Infinite Series (The Ant's Final Position)
We decompose the ant's movement into independent $x$ (East/West) and $y$ (North/South) components.

* **Horizontal ($x$-axis):** $1 - 1/3 + 1/5 - 1/7 \dots$
  This is the **Leibniz formula for $\pi$**. The series converges to $\mathbf{\frac{\pi}{4}}$.
* **Vertical ($y$-axis):** $1/2 - 1/4 + 1/6 - 1/8 \dots$
  Factor out $1/2$: $\frac{1}{2}(1 - 1/2 + 1/3 - 1/4 \dots)$.
  The series in the parentheses is the alternating harmonic series, which converges to $\ln(2)$.
  Therefore, $y = \mathbf{\frac{\ln(2)}{2}}$.

**Final Coordinate:** $(\frac{\pi}{4}, \frac{\ln(2)}{2}) \approx \mathbf{(0.785, 0.346)}$
