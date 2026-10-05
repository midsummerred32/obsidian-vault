
## Core Inverse Trigonometric Integration Formulas

$$\int \frac{1}{\sqrt{a^2 - u^2}} \, du = \arcsin\left(\frac{u}{a}\right) + C$$

$$\int \frac{1}{a^2 + u^2} \, du = \frac{1}{a}\arctan\left(\frac{u}{a}\right) + C$$

$$\int \frac{1}{|u|\sqrt{u^2 - a^2}} \, du = \frac{1}{a}\operatorname{arcsec}\left(\frac{|u|}{a}\right) + C$$

---

## Page 1: Introduction to Inverse Trig Integrals

### Example 1.1: $\int \frac{1}{\sqrt{16 - 3x^2}} \, dx$
- Rewrite denominator in the form $\sqrt{a^2 - u^2}$:
  $$\int \frac{1}{\sqrt{4^2 - (\sqrt{3}x)^2}} \, dx$$
- Let $a = 4$, $u = \sqrt{3}x \implies du = \sqrt{3} \, dx \implies dx = \frac{1}{\sqrt{3}} \, du$
- Substitute:
  $$\frac{1}{\sqrt{3}} \int \frac{1}{\sqrt{4^2 - u^2}} \, du = \frac{1}{\sqrt{3}}\arcsin\left(\frac{u}{4}\right) + C$$
  $$= \frac{1}{\sqrt{3}}\arcsin\left(\frac{\sqrt{3}x}{4}\right) + C$$

---

### Example 1.2: $\int \frac{1}{4 + 25x^2} \, dx$
- Rewrite denominator as $a^2 + u^2$:
  $$\int \frac{1}{2^2 + (5x)^2} \, dx$$
- Let $a = 2$, $u = 5x \implies du = 5 \, dx \implies dx = \frac{1}{5} \, du$
- Substitute:
  $$\frac{1}{5} \int \frac{1}{2^2 + u^2} \, du = \frac{1}{5} \cdot \left(\frac{1}{2}\arctan\left(\frac{5x}{2}\right)\right) + C$$
  $$= \frac{1}{10}\arctan\left(\frac{5x}{2}\right) + C$$

---

### Example 1.3: $\int \frac{x^5 + 5x^2}{x^6 + 1} \, dx$
- Split into two separate integrals:
  $$\int \frac{x^5}{x^6 + 1} \, dx + \int \frac{5x^2}{(x^3)^2 + 1} \, dx$$

1. **First term ($u$-substitution for logarithmic form):**
   - Let $u = x^6 + 1 \implies du = 6x^5 \, dx \implies x^5 \, dx = \frac{1}{6} \, du$
   $$\frac{1}{6} \int \frac{1}{u} \, du = \frac{1}{6}\ln|x^6 + 1|$$

2. **Second term (inverse tangent form):**
   - Let $u = x^3 \implies du = 3x^2 \, dx \implies 5x^2 \, dx = \frac{5}{3} \, du$
   $$\frac{5}{3} \int \frac{1}{u^2 + 1} \, du = \frac{5}{3}\arctan(x^3)$$

- **Combined Result:**
  $$= \frac{1}{6}\ln|x^6 + 1| + \frac{5}{3}\arctan(x^3) + C$$

---

## Page 2: Textbook Practice (p. 359) & Basic Substitution

### Left Column: p. 359 Practice

#### Exercise 3: $\int \frac{1}{x\sqrt{4x^2 - 1}} \, dx$
- Rewrite denominator:
  $$\int \frac{1}{x\sqrt{(2x)^2 - 1}} \, dx = \int \frac{2}{2x\sqrt{(2x)^2 - 1}} \, dx$$
- Let $u = 2x, du = 2 \, dx$:
  $$= \operatorname{arcsec}|2x| + C$$

#### Exercise 5: $\int \frac{1}{\sqrt{1 - (x + 1)^2}} \, dx$
- Form: $\int \frac{1}{\sqrt{a^2 - u^2}} \, dx$ with $a = 1$, $u = x + 1$, $du = dx$
  $$= \arcsin(x + 1) + C$$

#### Exercise 7: $\int \frac{t}{t^4 + 25} \, dt$
- Rewrite denominator: $\int \frac{t}{(t^2)^2 + 5^2} \, dt$
- Let $u = t^2 \implies du = 2t \, dt \implies t \, dt = \frac{1}{2} \, du$; $a = 5$
  $$= \frac{1}{2} \cdot \frac{1}{5}\arctan\left(\frac{t^2}{5}\right) + C = \frac{1}{10}\arctan\left(\frac{t^2}{5}\right) + C$$

#### Exercise 9: $\int \frac{1}{x^2 - 6x + 13} \, dx$
- **Complete the square on $x^2 - 6x + 13$:**
  $$(x - 3)^2 - 9 + 13 = (x - 3)^2 + 4 = (x - 3)^2 + 2^2$$
- Let $u = x - 3$, $du = dx$, $a = 2$:
  $$\int \frac{1}{(x - 3)^2 + 2^2} \, dx = \frac{1}{2}\arctan\left(\frac{x - 3}{2}\right) + C$$

---

### Right Column: Review Integrals

#### Definite Trig Integral: $\int_0^{\pi/2} -3\sin(x) \, dx$
$$\left[ 3\cos(x) \right]_0^{\pi/2} = 3\cos\left(\frac{\pi}{2}\right) - 3\cos(0) = 3(0) - 3(1) = -3$$

#### Exponential Integral: $\int (e^x - e) \, dx$
- *Note:* $e$ is a constant.
  $$= e^x - ex + C$$

#### Trig with Substitution: $\int 5x^2 \sec^2(x^3 - 8) \, dx$
- Let $u = x^3 - 8 \implies du = 3x^2 \, dx \implies 5x^2 \, dx = \frac{5}{3} \, du$:
  $$\frac{5}{3} \int \sec^2(u) \, du = \frac{5}{3}\tan(u) + C = \frac{5}{3}\tan(x^3 - 8) + C$$

#### Definite Exponential: $\int_1^8 7e^{4x - 7} \, dx$
- Let $u = 4x - 7 \implies du = 4 \, dx \implies dx = \frac{1}{4} \, du$
- *Bounds:* $x = 1 \to u = -3$; $x = 8 \to u = 25$
  $$\frac{7}{4}\int_{-3}^{25} e^u \, du = \frac{7}{4}\left[e^u\right]_{-3}^{25} = \frac{7}{4}\left(e^{25} - e^{-3}\right)$$

---

## Page 3: Completing the Square & Polynomial Division

### Left Column: Polynomial Long Division

#### Problem: $\int \frac{x + 1}{x + 2} \, dx$
- Divide:
  $$\frac{x + 1}{x + 2} = 1 - \frac{1}{x + 2}$$
- Integrate term-by-term:
  $$\int \left(1 - \frac{1}{x + 2}\right) dx = x - \ln|x + 2| + C$$

---

### Right Column: Completing the Square Practice

#### Problem 1: $\int \frac{1}{x^2 - 12x + 160} \, dx$
- Complete the square:
  $$x^2 - 12x + 160 = (x - 6)^2 - 36 + 160 = (x - 6)^2 + 124$$
- Let $u = x - 6$, $a = \sqrt{124} = 2\sqrt{31}$:
  $$\int \frac{1}{(x - 6)^2 + (\sqrt{124})^2} \, dx = \frac{1}{\sqrt{124}}\arctan\left(\frac{x - 6}{\sqrt{124}}\right) + C$$

#### Problem 2: $\int_0^1 \frac{1}{4x^2 + 9} \, dx$
- Form: $\int \frac{1}{(2x)^2 + 3^2} \, dx$
- Let $u = 2x \implies du = 2 \, dx \implies dx = \frac{1}{2} \, du$; $a = 3$
- *Bounds:* $x = 0 \to u = 0$; $x = 1 \to u = 2$
  $$\frac{1}{2} \int_0^2 \frac{1}{u^2 + 3^2} \, du = \frac{1}{2} \left[ \frac{1}{3}\arctan\left(\frac{u}{3}\right) \right]_0^2 = \frac{1}{6}\left[\arctan\left(\frac{2}{3}\right) - \arctan(0)\right] = \frac{1}{6}\arctan\left(\frac{2}{3}\right)$$

#### Problem 3: $\int_2^5 \frac{x}{4x^2 + 9} \, dx$
- Let $u = 4x^2 + 9 \implies du = 8x \, dx \implies x \, dx = \frac{1}{8} \, du$
- *Bounds:* $x = 2 \to u = 4(4) + 9 = 25$; $x = 5 \to u = 4(25) + 9 = 109$
  $$\frac{1}{8}\int_{25}^{109} \frac{1}{u} \, du = \frac{1}{8}\left[\ln|u|\right]_{25}^{109} = \frac{1}{8}\left(\ln(109) - \ln(25)\right) = \frac{1}{8}\ln\left(\frac{109}{25}\right)$$

---

## Page 4: Advanced Definite & Algebraic Integrals

### Left Column: p. 359 Odd Exercises

#### Exercise 21: $\int \frac{\cos(x)}{9 + \sin^2(x)} \, dx$
- Let $u = \sin(x) \implies du = \cos(x) \, dx$; $a = 3$
  $$\int \frac{1}{3^2 + u^2} \, du = \frac{1}{3}\arctan\left(\frac{\sin(x)}{3}\right) + C$$

#### Exercise 23: $\int_0^{1/6} \frac{3}{\sqrt{1 - 9x^2}} \, dx$
- Let $u = 3x \implies du = 3 \, dx$
- *Bounds:* $x = 0 \to u = 0$; $x = \frac{1}{6} \to u = \frac{1}{2}$
  $$\int_0^{1/2} \frac{1}{\sqrt{1 - u^2}} \, du = \left[\arcsin(u)\right]_0^{1/2} = \arcsin\left(\frac{1}{2}\right) - \arcsin(0) = \frac{\pi}{6} - 0 = \frac{\pi}{6}$$

#### Exercise 25: $\int_0^{\sqrt{3}/2} \frac{1}{1 + 4x^2} \, dx$
- Let $u = 2x \implies du = 2 \, dx \implies dx = \frac{1}{2} \, du$; $a = 1$
- *Bounds:* $x = 0 \to u = 0$; $x = \frac{\sqrt{3}}{2} \to u = \sqrt{3}$
  $$\frac{1}{2} \int_0^{\sqrt{3}} \frac{1}{1 + u^2} \, du = \frac{1}{2}\left[\arctan(u)\right]_0^{\sqrt{3}} = \frac{1}{2}\left(\arctan(\sqrt{3}) - 0\right) = \frac{1}{2}\left(\frac{\pi}{3}\right) = \frac{\pi}{6}$$

#### Exercise 33: $\int_3^6 \frac{1}{25 + (x - 3)^2} \, dx$
- Let $u = x - 3 \implies du = dx$; $a = 5$
- *Bounds:* $x = 3 \to u = 0$; $x = 6 \to u = 3$
  $$\int_0^3 \frac{1}{5^2 + u^2} \, du = \left[\frac{1}{5}\arctan\left(\frac{u}{5}\right)\right]_0^3 = \frac{1}{5}\arctan\left(\frac{3}{5}\right)$$

---

### Right Column: Definite and Rational Inverse Trig Forms

#### Problem 1: $\int_0^2 \frac{1}{x^2 - 2x + 2} \, dx$
- Complete the square: $x^2 - 2x + 2 = (x - 1)^2 + 1$
- Let $u = x - 1 \implies du = dx$
- *Bounds:* $x = 0 \to u = -1$; $x = 2 \to u = 1$
  $$\int_{-1}^1 \frac{1}{u^2 + 1^2} \, du = \left[\arctan(u)\right]_{-1}^1 = \arctan(1) - \arctan(-1) = \frac{\pi}{4} - \left(-\frac{\pi}{4}\right) = \frac{\pi}{2}$$

#### Problem 2: Exercise 35: $\int \frac{2x}{x^2 + 6x + 13} \, dx$
- Complete the square for denominator:
  $$x^2 + 6x + 13 = (x + 3)^2 + 4$$
- Split numerator: $2x = 2(x + 3) - 6$
  $$\int \frac{2(x + 3) - 6}{(x + 3)^2 + 4} \, dx = \int \frac{2(x + 3)}{(x + 3)^2 + 4} \, dx - 6\int \frac{1}{(x + 3)^2 + 2^2} \, dx$$
  $$= \ln|(x + 3)^2 + 4| - 6\left(\frac{1}{2}\arctan\left(\frac{x + 3}{2}\right)\right) + C$$
  $$= \ln|x^2 + 6x + 13| - 3\arctan\left(\frac{x + 3}{2}\right) + C$$

---

## Page 5: Mixed Forms & Rational Integrands

### Left Column

#### Problem 1: $\int \frac{1}{x\ln(x)} \, dx$
- Let $u = \ln(x) \implies du = \frac{1}{x} \, dx$
  $$\int \frac{1}{u} \, du = \ln|u| + C = \ln|\ln(x)| + C$$

#### Problem 2: $\int_2^5 \frac{\ln(x)}{x} \, dx$
- Let $u = \ln(x) \implies du = \frac{1}{x} \, dx$
  $$\int_{\ln(2)}^{\ln(5)} u \, du = \left[\frac{1}{2}u^2\right]_{\ln(2)}^{\ln(5)} = \frac{1}{2}(\ln(5))^2 - \frac{1}{2}(\ln(2))^2$$

#### Problem 3: $\int \frac{x}{x^4 + 36} \, dx$
- Rewrite: $\int \frac{x}{(x^2)^2 + 6^2} \, dx$
- Let $u = x^2 \implies du = 2x \, dx \implies x \, dx = \frac{1}{2} \, du$; $a = 6$
  $$\frac{1}{2}\int \frac{1}{u^2 + 6^2} \, du = \frac{1}{2} \cdot \frac{1}{6}\arctan\left(\frac{u}{6}\right) + C = \frac{1}{12}\arctan\left(\frac{x^2}{6}\right) + C$$

#### Problem 4: $\int \frac{x^3}{x^2 + 1} \, dx$
- Long division: $\frac{x^3}{x^2 + 1} = x - \frac{x}{x^2 + 1}$
- Integrate:
  $$\int x \, dx - \int \frac{x}{x^2 + 1} \, dx = \frac{1}{2}x^2 - \frac{1}{2}\ln|x^2 + 1| + C$$

---

### Right Column

#### Completing the Square: $\int \frac{1}{x^2 - 4x + 7} \, dx$
- Complete the square:
  $$x^2 - 4x + 7 = (x - 2)^2 - 4 + 7 = (x - 2)^2 + 3 = (x - 2)^2 + (\sqrt{3})^2$$
- Form with $u = x - 2$, $a = \sqrt{3}$:
  $$\int \frac{1}{(x - 2)^2 + (\sqrt{3})^2} \, dx = \frac{1}{\sqrt{3}}\arctan\left(\frac{x - 2}{\sqrt{3}}\right) + C$$

#### Multiple Choice / Worksheet (p. 460)
- **Problem 91:** $\int \frac{x}{\sqrt{x^2 - 4}} \, dx$
  - Let $u = x^2 - 4 \implies du = 2x \, dx \implies x \, dx = \frac{1}{2} \, du$
  $$\int \frac{\frac{1}{2}}{\sqrt{u}} \, du = \frac{1}{2}\int u^{-1/2} \, du = u^{1/2} + C = \sqrt{x^2 - 4} + C$$
  - **Option selected:** **B**
- **Problem 92:** Selected **A**
- **Problem 93:** Selected **C**
- **Problem 94:** Selected **C**

---

## Page 6: Comparison of Denominator Radical Forms

### Left Column: Contrasting $\int \frac{2x}{\dots} \, dx$ and Combined Forms

#### 1. Form: $\int \frac{2}{\sqrt{1 - x^2}} \, dx$
$$= 2\arcsin(x) + C$$

#### 2. Form: $\int \frac{2x}{1 - x^2} \, dx$
- Let $u = 1 - x^2 \implies du = -2x \, dx \implies -du = 2x \, dx$
  $$-\int \frac{1}{u} \, du = -\ln|u| + C = -\ln|1 - x^2| + C$$

#### 3. Form: $\int \frac{2x}{\sqrt{1 - x^2}} \, dx$
- Let $u = 1 - x^2 \implies du = -2x \, dx \implies -du = 2x \, dx$
  $$-\int u^{-1/2} \, du = -2u^{1/2} + C = -2\sqrt{1 - x^2} + C$$

#### 4. Splitting Numerator: $\int_0^4 \frac{x - 7}{x^2 + 16} \, dx$
- Split into:
  $$\int_0^4 \frac{x}{x^2 + 16} \, dx - 7\int_0^4 \frac{1}{x^2 + 4^2} \, dx$$
- Evaluate term 1 ($u = x^2 + 16 \implies du = 2x \, dx$; bounds $16 \to 32$):
  $$\frac{1}{2}\int_{16}^{32} \frac{1}{u} \, du = \frac{1}{2}\left[\ln|u|\right]_{16}^{32} = \frac{1}{2}(\ln(32) - \ln(16)) = \frac{1}{2}\ln(2)$$
- Evaluate term 2 ($a = 4$):
  $$-7 \left[ \frac{1}{4}\arctan\left(\frac{x}{4}\right) \right]_0^4 = -\frac{7}{4}(\arctan(1) - \arctan(0)) = -\frac{7}{4}\left(\frac{\pi}{4}\right) = -\frac{7\pi}{16}$$
- **Final Result:**
  $$= \frac{1}{2}\ln(2) - \frac{7\pi}{16}$$

---

### Right Column: General Substitution Review

#### Problem 1: $\int \sin(x) \cdot e^{-3\cos(x)} \, dx$
- Let $u = -3\cos(x) \implies du = 3\sin(x) \, dx \implies \sin(x) \, dx = \frac{1}{3} \, du$
  $$\frac{1}{3}\int e^u \, du = \frac{1}{3}e^u + C = \frac{1}{3}e^{-3\cos(x)} + C$$

#### Problem 2: $\int \frac{2(\ln(x))^2}{3x} \, dx$
- Let $u = \ln(x) \implies du = \frac{1}{x} \, dx$
  $$\frac{2}{3}\int u^2 \, du = \frac{2}{3} \cdot \frac{1}{3}u^3 + C = \frac{2}{9}(\ln(x))^3 + C$$

#### Problem 3: $\int \frac{1}{\sqrt{9 - 4x^2}} \, dx$
- Rewrite: $\int \frac{1}{\sqrt{3^2 - (2x)^2}} \, dx$
- Let $u = 2x \implies du = 2 \, dx \implies dx = \frac{1}{2} \, du$; $a = 3$
  $$\frac{1}{2}\int \frac{1}{\sqrt{3^2 - u^2}} \, du = \frac{1}{2}\arcsin\left(\frac{2x}{3}\right) + C$$