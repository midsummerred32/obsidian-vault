

---

## Page 1: Differential Equations & Slope Fields Analysis

### Problem 1: Consider $\frac{dy}{dx} = \frac{x+1}{y}$

#### (a) Slope Field Table & Sketch (12 Indicated Points)

| $(x, y)$ | Slope $\frac{dy}{dx} = \frac{x+1}{y}$ | $(x, y)$ | Slope $\frac{dy}{dx} = \frac{x+1}{y}$ |
|:---:|:---:|:---:|:---:|
| $(-1, 1)$ | $\frac{-1+1}{1} = 0$ | $(-1, -1)$ | $\frac{-1+1}{-1} = 0$ |
| $(0, 1)$ | $\frac{0+1}{1} = 1$ | $(0, -1)$ | $\frac{0+1}{-1} = -1$ |
| $(1, 1)$ | $\frac{1+1}{1} = 2$ | $(1, -1)$ | $\frac{1+1}{-1} = -2$ |
| $(-1, 2)$ | $\frac{-1+1}{2} = 0$ | $(-1, -2)$ | $\frac{-1+1}{-2} = 0$ |
| $(0, 2)$ | $\frac{0+1}{2} = \frac{1}{2}$ | $(0, -2)$ | $\frac{0+1}{-2} = -\frac{1}{2}$ |
| $(1, 2)$ | $\frac{1+1}{2} = 1$ | $(1, -2)$ | $\frac{1+1}{-2} = -1$ |

*Note on sketch:* Passes through $(0, -1)$ with slope $-1$, concaved downward in quadrant IV for $-1 < x < 1$.

---

#### (b) Describe all points $(x, y)$ with $y \neq 0$ for which $\frac{dy}{dx} = -1$:
$$\frac{x + 1}{y} = -1 \implies y = -(x + 1) = -x - 1$$
- **Description:** All points on the line $y = -x - 1$ where $y \neq 0$ (e.g., $(0, -1)$, $(1, -2)$).

---

#### (c) Particular Solution $y = f(x)$ with Initial Condition $f(0) = -2$:
1. **Separate variables:**
   $$y \, dy = (x + 1) \, dx$$
2. **Integrate both sides:**
   $$\int y \, dy = \int (x + 1) \, dx$$
   $$\frac{y^2}{2} = \frac{x^2}{2} + x + C_1$$
   $$y^2 = x^2 + 2x + C$$
3. **Apply initial condition $(0, -2)$:**
   $$(-2)^2 = 0^2 + 2(0) + C \implies C = 4$$
4. **Solve explicitly for $y$:**
   $$y = \pm \sqrt{x^2 + 2x + 4}$$
   Since $y(0) = -2 < 0$, choose the negative root:
   $$y = -\sqrt{x^2 + 2x + 4}$$

---

## Page 2: Euler's Method & Population Models

### Problem 2: Euler's Method for $y' = e^{xy}$, $y(0) = 1$, Step size $h = 0.1$
Formula: $y_{n+1} = y_n + h \cdot f(x_n, y_n)$

| $n$ | $x_n$ | $y_n$ | Slope $\frac{dy}{dx} = e^{x_n y_n}$ | $\Delta y = h \cdot \frac{dy}{dx}$ | $y_{n+1} = y_n + \Delta y$ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| $0$ | $0.0$ | $1.00000$ | $e^{(0)(1)} = 1.00000$ | $(0.1)(1) = 0.1$ | $1.10000$ |
| $1$ | $0.1$ | $1.10000$ | $e^{(0.1)(1.1)} \approx 1.11628$ | $(0.1)(1.11628) \approx 0.11163$ | $1.21163$ |
| $2$ | $0.2$ | $1.21163$ | $e^{(0.2)(1.21163)} \approx 1.27421$ | $(0.1)(1.27421) \approx 0.12742$ | $1.33905$ |
| $3$ | $0.3$ | $1.33905$ | $e^{(0.3)(1.33905)} \approx 1.49439$ | $(0.1)(1.49439) \approx 0.14944$ | $1.48848$ |
| $4$ | $0.4$ | $1.48848$ | — | — | — |

**Final Approximation:**
$$y(0.4) \approx 1.48848$$

---

### Problem 3: Carrying Capacity Limit
Logistic equation:
$$\frac{dP}{dt} = P\left(3 - \frac{P}{4000}\right) = 3P\left(1 - \frac{P}{12000}\right)$$
- Carrying capacity $L = 12000$.
- For any initial population $P_0 > 0$:
  $$\lim_{t \to \infty} P(t) = 12000$$

---

### Problem 4: Gorilla Population Model
Differential equation:
$$\frac{dP}{dt} = 0.0004P(250 - P) = 0.1P\left(1 - \frac{P}{250}\right)$$
- Carrying capacity $L = 250$, growth parameter $k = 0.1$.
- Logistic general solution:
  $$P(t) = \frac{L}{1 + b e^{-kt}} = \frac{250}{1 + b e^{-0.1t}}$$

#### (a) Formula for Gorilla Population $P(t)$ with $P(0) = 28$:
$$28 = \frac{250}{1 + b} \implies 1 + b = \frac{250}{28} = \frac{125}{14} \implies b = \frac{111}{14} \approx 7.9286$$
$$P(t) = \frac{250}{1 + \frac{111}{14}e^{-0.1t}}$$

#### (b) When will population reach carrying capacity?
$$250 = \frac{250}{1 + \frac{111}{14}e^{-0.1t}} \implies 1 + \frac{111}{14}e^{-0.1t} = 1 \implies \frac{111}{14}e^{-0.1t} = 0$$
- Since $e^{-0.1t} \to 0$ only as $t \to \infty$, the population theoretically **approaches $250$ asymptotically as $t \to \infty$** (never reaches exactly $250$ in finite continuous time).

---

## Page 3: Topic 7.9 – Logistic Models Reference

### Standard Forms
- **Differential Equation Form:**
  $$\frac{dy}{dt} = ky\left(1 - \frac{y}{L}\right)$$
- **Solution Function Form:**
  $$y = \frac{L}{1 + b e^{-kt}}$$
- **Properties:**
  - $L$ is the carrying capacity: $\lim_{t \to \infty} y(t) = L$.
  - The growth rate $\frac{dy}{dt}$ is maximized at the inflection point, when:
    $$y = \frac{L}{2}$$

---

### Example 1: Multiple Choice
Given $\frac{dy}{dt} = 2y(10 - y)$ with $y(0) = 1$:
1. Rewrite in standard form:
   $$\frac{dy}{dt} = 20y\left(1 - \frac{y}{10}\right) \implies L = 10, \; k = 20$$
2. General solution:
   $$y(t) = \frac{10}{1 + b e^{-20t}}$$
3. Use $y(0) = 1$:
   $$1 = \frac{10}{1 + b} \implies 1 + b = 10 \implies b = 9$$
   $$y(t) = \frac{10}{1 + 9e^{-20t}}$$
- **Correct Choice:** **(B)**

---

## Page 4: Logistic Growth Multiple Choice & Free Response

### Example 2 (MC): Phytoplankton Population
- For logistic models, the rate is proportional to both the population and the room left to grow:
  $$\frac{dP}{P(1780 - P)} = 0.035 \, dt$$
- **Correct Option:** **(D)**

---

### Example 3 (MC): Infection Spread
Given $P(t) = \frac{800}{1 + 16e^{-0.5t}}$:
- The rate of spread is greatest at half the carrying capacity:
  $$P = \frac{L}{2} = \frac{800}{2} = 400$$
- **Correct Choice:** **(C)** $400$

---

### Example 4 (MC): Natural Gas Extraction
Given $\frac{dG}{dt} = 0.04G\left(1 - \frac{G}{64}\right)$:
- Extraction rate is increasing fastest at:
  $$G = \frac{L}{2} = \frac{64}{2} = 32$$
- **Correct Choice:** **(B)** $32$

---

### Example 5 (FRQ): Panther Conservation
Initial release: $P(0) = 30$. After 3 years: $P(3) = 50$. Carrying capacity: $L = 150$.

- **(a) Find $L$:**
  $$L = 150$$

- **(b) Find $b$:**
  $$30 = \frac{150}{1 + b} \implies 1 + b = 5 \implies b = 4$$

- **(c) Find exact $k$:**
  $$50 = \frac{150}{1 + 4e^{-3k}} \implies 1 + 4e^{-3k} = 3 \implies 4e^{-3k} = 2 \implies e^{-3k} = \frac{1}{2}$$
  $$-3k = \ln\left(\frac{1}{2}\right) = -\ln(2) \implies k = \frac{1}{3}\ln(2)$$

- **(d) Model equation:**
  $$P(t) = \frac{150}{1 + 4e^{-\frac{1}{3}\ln(2)t}} = \frac{150}{1 + 4\left(\frac{1}{2}\right)^{t/3}}$$

- **(e) Estimate at $t = 12$ years:**
  $$P(12) = \frac{150}{1 + 4\left(\frac{1}{2}\right)^4} = \frac{150}{1 + 4\left(\frac{1}{16}\right)} = \frac{150}{1 + \frac{1}{4}} = \frac{150}{\frac{5}{4}} = 120 \text{ panthers}$$

- **(f) Limit as $t \to \infty$:**
  $$\lim_{t \to \infty} P(t) = 150$$

---

## Page 5: Additional Euler's Method Practice Tables

### Table 1: $\frac{dy}{dx} = y$, $y(0) = 3$, $h = 0.2$
| $x$ | $y$ | $\frac{dy}{dx} = y$ | $y_{\text{new}} = y + h \cdot \frac{dy}{dx}$ |
|:---:|:---:|:---:|:---:|
| $0.0$ | $3$ | $3$ | $3 + 0.2(3) = 3.6$ |
| $0.2$ | $3.6$ | $3.6$ | $3.6 + 0.2(3.6) = 4.32$ |
| $0.4$ | $4.32$ | $4.32$ | $4.32 + 0.2(4.32) = 5.184$ |
| $0.6$ | $5.184$ | $5.184$ | $5.184 + 0.2(5.184) = 6.2208$ |
| $0.8$ | $6.2208$ | — | — |

---

### Table 2: $\frac{dy}{dx} = \frac{x}{y}$, $y(0) = 2$, $h = 0.2$
| $x$ | $y$ | $\frac{dy}{dx} = \frac{x}{y}$ | $y_{\text{new}} = y + 0.2 \cdot \frac{dy}{dx}$ |
|:---:|:---:|:---:|:---:|
| $0.0$ | $2.0000$ | $0.0000$ | $2.0000$ |
| $0.2$ | $2.0000$ | $0.1000$ | $2.0200$ |
| $0.4$ | $2.0200$ | $0.1980$ | $2.0596$ |
| $0.6$ | $2.0596$ | $0.2913$ | $2.1179$ |
| $0.8$ | $2.1179$ | $0.3777$ | $2.1934$ |
| $1.0$ | $2.1934$ | — | — |

---

### Table 3: $\frac{dy}{dx} = y - 6x$, $(0, -1)$, Step size $h = 0.2$
| $x$ | $y$ | $\frac{dy}{dx} = y - 6x$ | $y_{\text{next}} = y + 0.2\left(\frac{dy}{dx}\right)$ |
|:---:|:---:|:---:|:---:|
| $0.0$ | $-1.000$ | $-1 - 0 = -1$ | $-1 + 0.2(-1) = -1.2$ |
| $0.2$ | $-1.200$ | $-1.2 - 6(0.2) = -2.4$ | $-1.2 + 0.2(-2.4) = -1.68$ |
| $0.4$ | $-1.680$ | $-1.68 - 6(0.4) = -4.08$ | $-1.68 + 0.2(-4.08) = -2.496$ |
| $0.6$ | **$-2.496$** | — | — |

$$f(0.6) \approx -2.496$$

---

## Page 6: Euler's Method Guided Worksheet (Topic 7.5)

### Example 1: $y' = xy$, passing through $(0, 1)$ with $h = 0.2$

| $x$ | $y$ | $\frac{dy}{dx} = xy$ | Tangent Line Equation / Calculation | $dy = \left(\frac{dy}{dx}\right)h$ |
|:---:|:---:|:---:|:---:|:---:|
| $0.0$ | $1.0000$ | $0.0000$ | $y - 1 = 0(x - 0) \implies y = 1$ | $0$ |
| $0.2$ | $1.0000$ | $0.2000$ | $y - 1 = 0.2(x - 0.2)$ | $0.2(0.2) = 0.04$ |
| $0.4$ | $1.0400$ | $0.4160$ | $y - 1.04 = 0.416(x - 0.4)$ | $0.416(0.2) = 0.0832$ |
| $0.6$ | $1.1232$ | $0.6739$ | $y - 1.1232 = 0.6739(x - 0.6)$ | $0.6739(0.2) \approx 0.1348$ |
| $0.8$ | **$1.257984$** | — | — | — |

**Approximation:**
$$y(0.8) \approx 1.257984$$

---

## Page 7: Slope Field Matching

### Problem 3
- **Observation:** Slopes depend only on $y$ (horizontal rows are constant). When $y = 0$, slopes are horizontal ($0$). Slopes are positive everywhere $y \neq 0$.
- **Matching Equation:** 
  $$\frac{dy}{dx} = y^2$$
- **Correct Choice:** **(D)**

---

### Problem 4
- **Observation:** Slopes are zero along the line $y = x$ (diagonal running through the origin). In the region where $x > y$, slopes are positive.
- **Matching Equation:** 
  $$\frac{dy}{dx} = x - y$$
- **Correct Choice:** **(B)**