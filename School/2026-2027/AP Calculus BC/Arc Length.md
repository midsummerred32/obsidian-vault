## Core Formulas

### Arc Length of a Curve $y = f(x)$ from $x = a$ to $x = b$:
$$L = \int_{a}^{b} \sqrt{1 + \left[f'(x)\right]^2} \, dx$$

### Arc Length of a Curve $x = g(y)$ from $y = c$ to $y = d$:
$$L = \int_{c}^{d} \sqrt{1 + \left[g'(y)\right]^2} \, dy$$

---

## Page 1: Linear Arc Length Example

### Example: Find the Arc Length of a Line
- **Function:** 
  $$y = \frac{1}{5}(12x - 7) = \frac{12}{5}x - \frac{7}{5}$$
- **Interval:** from $(1, 1)$ to $(6, 13)$  $\implies a = 1, \; b = 6$
- **Derivative:** 
  $$y' = \frac{12}{5}$$
  $$(y')^2 = \left(\frac{12}{5}\right)^2 = \frac{144}{25}$$

### Integration Setup:
$$L = \int_{1}^{6} \sqrt{1 + \left(\frac{12}{5}\right)^2} \, dx$$
$$L = \int_{1}^{6} \sqrt{1 + \frac{144}{25}} \, dx$$
$$L = \int_{1}^{6} \sqrt{\frac{169}{25}} \, dx = \int_{1}^{6} \frac{13}{5} \, dx$$

### Evaluation:
$$L = \left[ \frac{13}{5}x \right]_{1}^{6} = \frac{13}{5}(6) - \frac{13}{5}(1) = \frac{13}{5}(6 - 1) = \frac{13}{5}(5) = 13$$

---

## Page 2: Algebraic Simplification & Perimeter of a Region

### Problem 1: $f(x) = \frac{x^3}{6} + \frac{1}{2x}$ on $\left[\frac{1}{2}, 2\right]$
- Rewrite function:
  $$f(x) = \frac{1}{6}x^3 + \frac{1}{2}x^{-1}$$
- Differentiate:
  $$f'(x) = \frac{1}{2}x^2 - \frac{1}{2x^2} = \frac{1}{2}\left(x^2 - x^{-2}\right)$$
- Square the derivative:
  $$\left[f'(x)\right]^2 = \frac{1}{4}\left(x^4 - 2 + x^{-4}\right)$$
- Form $1 + [f'(x)]^2$:
  $$1 + \left[f'(x)\right]^2 = 1 + \frac{1}{4}x^4 - \frac{1}{2} + \frac{1}{4}x^{-4} = \frac{1}{4}x^4 + \frac{1}{2} + \frac{1}{4}x^{-4} = \left(\frac{1}{2}x^2 + \frac{1}{2}x^{-2}\right)^2$$
- Take the square root:
  $$\sqrt{1 + [f'(x)]^2} = \frac{1}{2}x^2 + \frac{1}{2x^2}$$

### Arc Length Integral:
$$L = \int_{1/2}^{2} \left(\frac{1}{2}x^2 + \frac{1}{2}x^{-2}\right) dx = \left[ \frac{x^3}{6} - \frac{1}{2x} \right]_{1/2}^{2}$$
$$= \left(\frac{8}{6} - \frac{1}{4}\right) - \left(\frac{1}{48} - 1\right) = \frac{33}{16}$$

---

### Problem 2: Total Perimeter of Region $R$
Region bounded by:
- Vertical segment along the $y$-axis from $y = 0$ to $y = 2$ (length $= 2$)
- Upper curve: $f(x) = -\frac{4}{3}x + 2$ from $x = 0$ to $x = 1$ (intersects at $(1, \frac{2}{3})$)
- Lower curve: $g(x) = \frac{2}{3}x^{3/2}$ from $x = 0$ to $x = 1$ (intersects at $(1, \frac{2}{3})$)

### Total Perimeter Setup:
$$\text{Perimeter} = 2 + \int_{0}^{1} \sqrt{1 + [f'(x)]^2} \, dx + \int_{0}^{1} \sqrt{1 + [g'(x)]^2} \, dx$$
$$\approx 4.986 \text{ units}$$

---

## Page 3: Integration with Respect to $y$ & Trig Form

### Problem 1: $x^2 = (y - 1)^3$ on $y \in [1, 5]$
- Solve for $x$ (positive branch):
  $$x = (y - 1)^{3/2}$$
- Differentiate with respect to $y$:
  $$f'(y) = \frac{3}{2}(y - 1)^{1/2}$$
  $$\left[f'(y)\right]^2 = \frac{9}{4}(y - 1)$$
- Setup integral:
  $$L = \int_{1}^{5} \sqrt{1 + \frac{9}{4}(y - 1)} \, dy = \int_{1}^{5} \sqrt{\frac{9}{4}y - \frac{5}{4}} \, dy$$

### $u$-Substitution:
- Let $u = \frac{9}{4}y - \frac{5}{4} \implies du = \frac{9}{4} \, dy \implies dy = \frac{4}{9} \, du$
- Bounds:
  - $y = 1 \implies u = \frac{9}{4}(1) - \frac{5}{4} = 1$
  - $y = 5 \implies u = \frac{9}{4}(5) - \frac{5}{4} = \frac{40}{4} = 10$

$$L = \frac{4}{9} \int_{1}^{10} u^{1/2} \, du = \frac{4}{9} \left[ \frac{2}{3} u^{3/2} \right]_{1}^{10} = \frac{8}{27} \left(10^{3/2} - 1\right)$$

---

### Textbook p. 444, Problem 11: $f(x) = \ln(\sin(x))$ on $\left[\frac{\pi}{4}, \frac{3\pi}{4}\right]$
- Differentiate:
  $$f'(x) = \frac{1}{\sin(x)} \cdot \cos(x) = \cot(x)$$
- Form radical:
  $$\sqrt{1 + [f'(x)]^2} = \sqrt{1 + \cot^2(x)} = \sqrt{\csc^2(x)} = \csc(x)$$

### Integral:
$$L = \int_{\pi/4}^{3\pi/4} \csc(x) \, dx = \left[ -\ln|\csc(x) + \cot(x)| \right]_{\pi/4}^{3\pi/4}$$
- Upper limit ($x = \frac{3\pi}{4}$):
  $$\csc\left(\frac{3\pi}{4}\right) = \sqrt{2}, \quad \cot\left(\frac{3\pi}{4}\right) = -1 \implies -\ln|\sqrt{2} - 1|$$
- Lower limit ($x = \frac{\pi}{4}$):
  $$\csc\left(\frac{\pi}{4}\right) = \sqrt{2}, \quad \cot\left(\frac{\pi}{4}\right) = 1 \implies -\ln|\sqrt{2} + 1|$$

### Result:
$$L = -\ln|\sqrt{2} - 1| + \ln|\sqrt{2} + 1|$$

---

## Page 4: Textbook p. 444 (Problems 15 & 63)

### Problem 15: $x = \frac{1}{3}(y^2 + 2)^{3/2}$ on $0 \le y \le 4$
- Differentiate with respect to $y$:
  $$x' = \frac{1}{3} \cdot \frac{3}{2}(y^2 + 2)^{1/2} \cdot 2y = y(y^2 + 2)^{1/2}$$
- Square the derivative:
  $$(x')^2 = y^2(y^2 + 2) = y^4 + 2y^2$$
- Form the radical:
  $$\sqrt{1 + (x')^2} = \sqrt{1 + y^4 + 2y^2} = \sqrt{(y^2 + 1)^2} = y^2 + 1$$

### Evaluate Integral:
$$L = \int_{0}^{4} (y^2 + 1) \, dy = \left[ \frac{1}{3}y^3 + y \right]_{0}^{4}$$
$$L = \frac{1}{3}(4)^3 + 4 = \frac{64}{3} + \frac{12}{3} = \frac{76}{3}$$

---

### Problem 63: Derivative Setup / Scratchwork
- Expression:
  $$\frac{d}{dx}\left[2\sin(\sqrt{x})\right] = 2\cos(\sqrt{x}) \cdot \frac{1}{2\sqrt{x}} = \frac{\cos(\sqrt{x})}{\sqrt{x}}$$