
---

## 1. Area Between Curves

### Formulations
- **Vertical slices ($dx$):** 
  $$\text{Area} = \int_{a}^{b} (\text{Top} - \text{Bottom}) \, dx = \int_{a}^{b} \left(f(x) - g(x)\right) dx$$
- **Horizontal slices ($dy$):** 
  $$\text{Area} = \int_{c}^{d} (\text{Right} - \text{Left}) \, dy = \int_{c}^{d} \left(f(y) - g(y)\right) dy$$

---

### Example 1: Area Between Curves ($dx$)
- **Curves:** 
  - $y_{\text{top}} = 2x^2 - 8x + 10$
  - $y_{\text{bottom}} = \frac{x^2}{2} - 2x - 1$
- **Interval:** $x \in [1, 3]$

#### Setup & Evaluation:
$$\text{Area} = \int_{1}^{3} \left[(2x^2 - 8x + 10) - \left(\frac{x^2}{2} - 2x - 1\right)\right] dx$$
$$\text{Area} = \int_{1}^{3} \left(\frac{3}{2}x^2 - 6x + 11\right) dx$$
$$\text{Area} = \left[ \frac{1}{2}x^3 - 3x^2 + 11x \right]_{1}^{3}$$
- At $x = 3$: $\frac{1}{2}(27) - 3(9) + 11(3) = 13.5 - 27 + 33 = 19.5$
- At $x = 1$: $\frac{1}{2}(1) - 3(1) + 11(1) = 0.5 - 3 + 11 = 8.5$
$$\text{Area} = 19.5 - 8.5 = 11$$

---

### Example 2: Area Between Curves ($dy$)
- **Curves:** 
  - $x_{\text{right}} = -\frac{y^2}{2} - 4y - 10$
  - $x_{\text{left}} = 2y^2 + 12y + 19$
- **Interval:** $y \in [-3, -2]$

#### Setup & Evaluation:
$$\text{Area} = \int_{-3}^{-2} (\text{Right} - \text{Left}) \, dy$$
$$\text{Area} = \int_{-3}^{-2} \left[\left(-\frac{y^2}{2} - 4y - 10\right) - (2y^2 + 12y + 19)\right] dy$$
$$\text{Area} = \int_{-3}^{-2} \left(-\frac{5}{2}y^2 - 16y - 29\right) dy \approx 4.8\overline{3} = \frac{29}{6}$$

---

## 2. Volume of Solids of Revolution

| Situation | Variable | Axis of Revolution |
| :--- | :---: | :--- |
| Perpendicular to horizontal line | $dx$ | Horizontal line (e.g., $x$-axis, $y = k$) |
| Perpendicular to vertical line | $dy$ | Vertical line (e.g., $y$-axis, $x = h$) |

### Method Rules:
- **Disk Method (No gaps between region and axis):**
  $$V = \pi \int_{a}^{b} [R(x)]^2 \, dx \quad \text{or} \quad \pi \int_{c}^{d} [R(y)]^2 \, dy$$

- **Washer Method (Gaps between region and axis):**
  $$V = \pi \int_{a}^{b} \left( [R(x)]^2 - [r(x)]^2 \right) dx \quad \text{or} \quad \pi \int_{c}^{d} \left( [R(y)]^2 - [r(y)]^2 \right) dy$$
  - $R =$ Outer Radius (distance from axis to farther curve)
  - $r =$ Inner Radius (distance from axis to closer curve)

---

## 3. Practice Problems: Disk vs. Washer

### Problem 1: Revolved around $x$-axis (Disk)
- **Region:** $y = -x^2 + 1$, bounded by $y = 0$ from $x = -1$ to $x = 1$
- **Setup:**
  $$V = \pi \int_{-1}^{1} (-x^2 + 1)^2 \, dx \approx 3.351 \quad \left(\frac{16\pi}{15}\right)$$

---

### Problem 2: Revolved around $x$-axis (Washer)
- **Curves:** $y = 2x + 2$ (top), $y = x^2 + 2$ (bottom)
- **Intersection bounds:** $x = 0$ to $x = 2$
- **Setup:**
  $$V = \pi \int_{0}^{2} \left[ (2x + 2)^2 - (x^2 + 2)^2 \right] dx \approx 30.159 \quad \left(\frac{48\pi}{5}\right)$$

---

### Problem 3: Revolved around $y = -1$ (Washer)
- **Curves:** $y = \sqrt{x+1}$, $y = x^2 + 1$
- **Axis:** $y = -1$
- **Radii:**
  $$R(x) = \sqrt{x+1} - (-1) = \sqrt{x+1} + 1$$
  $$r(x) = (x^2 + 1) - (-1) = x^2 + 2$$
- **Setup:**
  $$V = \pi \int_{0}^{1} \left[ (\sqrt{x+1} + 1)^2 - (x^2 + 2)^2 \right] dx$$

---

### Problem 4: Revolved around vertical line $x = -2$ (Washer in $dy$)
- **Curves:** $x = -y^2 + 2$, $x = y$
- **Axis:** $x = -2$
- **Intersection:** $-y^2 + 2 = y \implies y^2 + y - 2 = 0 \implies y = -2, 1$
- **Radii:**
  $$R(y) = (-y^2 + 2) - (-2) = -y^2 + 4$$
  $$r(y) = y - (-2) = y + 2$$
- **Setup & Result:**
  $$V = \pi \int_{-2}^{1} \left[ (-y^2 + 4)^2 - (y + 2)^2 \right] dy \approx 67.858 \quad \left(\frac{108\pi}{5}\right)$$

---

## 4. Free-Response / Calculator Practice

**Given Region $R$:**
- Shaded region in the first quadrant bounded by:
  - Top: $y = 6$
  - Bottom: $y = 4\ln(3 - x)$
  - Right: $x = 2$
  - Left: $y$-axis ($x = 0$)

---

### 1. Find the Area of Region $R$
$$\text{Area} = \int_{0}^{2} \left[ 6 - 4\ln(3 - x) \right] dx \approx 6.187$$

---

### 2. Volume when revolved around the $x$-axis
- **Type:** Washer Method ($dx$)
- **Axis:** $y = 0$
- **Radii:**
  $$R(x) = 6 - 0 = 6$$
  $$r(x) = 4\ln(3 - x) - 0 = 4\ln(3 - x)$$
- **Setup & Evaluation:**
  $$V = \pi \int_{0}^{2} \left[ 6^2 - (4\ln(3 - x))^2 \right] dx = \pi \int_{0}^{2} \left[ 36 - 16(\ln(3 - x))^2 \right] dx \approx 174.463$$

---

### 3. Volume when revolved around the $y$-axis
- **Type:** Washer Method ($dy$)
- **Solve boundary curve for $x$:**
  $$y = 4\ln(3 - x) \implies \frac{y}{4} = \ln(3 - x)$$
  $$e^{y/4} = 3 - x \implies x = 3 - e^{y/4}$$
- **$y$-bounds:**
  - When $x = 0$: $y = 4\ln(3) \approx 4.394$
  - When $x = 2$: $y = 4\ln(1) = 0$
  - Top horizontal line: $y = 6$
- **Radii:**
  - From $y = 0$ to $y = 4\ln(3)$:
    $$R(y) = 2, \quad r(y) = 3 - e^{y/4}$$
  - From $y = 4\ln(3)$ to $y = 6$:
    $$R(y) = 2, \quad r(y) = 0$$
- **Integral Setup:**
  $$V = \pi \int_{0}^{4\ln(3)} \left[ 2^2 - \left(3 - e^{y/4}\right)^2 \right] dy + \pi \int_{4\ln(3)}^{6} 2^2 \, dy$$

---

### 4. Volume when revolved around the line $y = 8$
- **Type:** Washer Method ($dx$)
- **Axis:** $y = 8$ (above region)
- **Radii:**
  $$R(x) = 8 - 4\ln(3 - x) \quad (\text{Outer / Farther})$$
  $$r(x) = 8 - 6 = 2 \quad (\text{Inner / Closer})$$
- **Integral Setup:**
  $$V = \pi \int_{0}^{2} \left[ (8 - 4\ln(3 - x))^2 - 2^2 \right] dx$$