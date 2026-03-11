# Section 1: Mechanics I - Solutions

## 1. Projectile Motion
**Given:** $v_0 = 100 \text{ m/s}$, $\theta = 37^\circ$, $g \approx 9.8 \text{ m/s}^2$
*(Note: $\sin 37^\circ \approx 0.6, \cos 37^\circ \approx 0.8$)*

* **Differential Equations of Motion:**
    Horizontal: $\frac{d^2x}{dt^2} = 0$
    Vertical: $\frac{d^2y}{dt^2} = -g$
* **Time of Flight ($T$):**
    $y(t) = (v_0 \sin \theta)t - \frac{1}{2}gt^2 = 0$
    $$T = \frac{2v_0 \sin \theta}{g} = \frac{2(100)(0.6)}{9.8} \approx \mathbf{12.24 \text{ s}}$$
* **Maximum Height ($H$):**
    $$H = \frac{(v_0 \sin \theta)^2}{2g} = \frac{60^2}{19.6} \approx \mathbf{183.67 \text{ m}}$$
* **Range ($R$):**
    $$R = \frac{v_0^2 \sin(2\theta)}{g} = \frac{100^2 \sin(74^\circ)}{9.8} \approx \mathbf{980.9 \text{ m}}$$



---

## 2. Range Optimization
To find the maximum of $R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}$:
$$\frac{dR}{d\theta} = \frac{v_0^2}{g} \cdot 2\cos(2\theta) = 0$$
Since $v_0, g \neq 0$, then $\cos(2\theta) = 0$.
$2\theta = 90^\circ \implies \mathbf{\theta = 45^\circ}$.

---

## 3. Path Intersection
* **Alice:** $A(t) = (2+t, 8-3t)$
* **Bob:** $B(s) = (2s-1, 2s+2)$

**Intersection Check:**
Set $x_A = x_B \implies 2+t = 2s-1 \implies t = 2s-3$.
Substitute into $y$: $8 - 3(2s-3) = 2s+2 \implies 17-6s = 2s+2 \implies 8s = 15$.
Result: $\mathbf{s = 1.875, t = 0.75}$.
**Conclusion:** The paths intersect at $(2.75, 5.75)$. However, since $t \neq s$, they reach that point at different times. **No collision occurs.**

---

## 4. Vector Calculus
Given $\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}$:
* **Velocity:** $\vec{v}(t) = \frac{d\vec{r}}{dt} = \mathbf{(6t)\hat{i} + (5 - 16t)\hat{j}}$
* **Acceleration:** $\vec{a}(t) = \frac{d\vec{v}}{dt} = \mathbf{6\hat{i} - 16\hat{j}}$

---

## 5. Relative Velocity
River velocity $v_r = 2 \text{ m/s}$ (East). Boat speed $v_b = 5 \text{ m/s}$.
To go North, the horizontal component of the boat must cancel the river:
$\sin \alpha = \frac{2}{5} \implies \alpha = \arcsin(0.4) \approx \mathbf{23.58^\circ}$ **West of North.**

**Time to cross:**
$v_{north} = 5 \cos(23.58^\circ) \approx 4.58 \text{ m/s}$
$t = \frac{200}{4.58} \approx \mathbf{43.6 \text{ s}}$

---

## 6. Variable Velocity
$v(t) = t^2 + 2t - 5$ and $x(0) = 4$.
* **Position ($x$):** $x(t) = \int v(t)dt = \frac{1}{3}t^3 + t^2 - 5t + 4$.
    At $t=3$: $x(3) = 9 + 9 - 15 + 4 = \mathbf{7 \text{ m}}$.
* **Acceleration ($a$):** $a(t) = \frac{dv}{dt} = 2t + 2$.
    At $t=3$: $a(3) = \mathbf{8 \text{ m/s}^2}$.

---

## 7. Elimination of Time
$x = 2t^2 \implies t^2 = x/2$.
$y = 3t^3 \implies y^2 = 9t^6 = 9(t^2)^3$.
**Trajectory Equation:** $\mathbf{y^2 = \frac{9}{8}x^3}$

* **Vectors:**
    $\vec{v}(t) = (4t, 9t^2) \implies |\vec{v}(t)| = \mathbf{t\sqrt{16+81t^2}}$
    $\vec{a}(t) = (4, 18t) \implies |\vec{a}(t)| = \mathbf{\sqrt{16+324t^2}}$
* **Constant Acceleration?** No, it depends on $t$.

---

## 28. Circular Motion
$a_c = \omega^2 R = (\frac{2\pi}{T})^2 R$
$R = 6,378,000 \text{ m}$, $T = 86,400 \text{ s}$.
$a_c \approx \mathbf{0.0337 \text{ m/s}^2}$

---

## 9. Momentum Comparison
$p = mv$
* **Fly:** $0.002 \text{ kg} \times 10 \text{ m/s} = 0.02 \text{ kg}\cdot\text{m/s}$
* **Tennis Ball:** $0.060 \text{ kg} \times 1 \text{ m/s} = 0.06 \text{ kg}\cdot\text{m/s}$
**The tennis ball** has greater momentum.

---

## 10. Kinematics (Helical Motion)
$\vec{r}(t) = (a \cos(\omega t), b \sin(\omega t), bt)$

* **a) Trajectory:** In the $xy$-plane, it describes an ellipse: $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$. With the $z$-component increasing linearly, the path is an **Elliptical Helix**.
* **b) Path Length ($s$):**
    $s = \int_{0}^{t_0} \sqrt{(-a\omega \sin \omega t)^2 + (b\omega \cos \omega t)^2 + b^2} dt$
* **c) Python Visualization:**
    Special cases: If $a=b$, it is a circular helix. If $\omega=0$, it is a straight vertical line.

```python
import numpy as np
import matplotlib.pyplot as plt

t = np.linspace(0, 10, 500)
a, b, w = 2, 1, 2
x, y, z = a*np.cos(w*t), b*np.sin(w*t), b*t

fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot(x, y, z, label='Elliptical Helix')
ax.set_xlabel('X'); ax.set_ylabel('Y'); ax.set_zlabel('Z')
plt.show()
