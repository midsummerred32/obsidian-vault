

## Core Formula
$$\int u \, dv = uv - \int v \, du$$

---

## Strategy for Choosing $u$: The ILATE Rule

When selecting which function to set as $u$, prioritize functions higher on this list (differentiate $u$, integrate $dv$):

1. **I** – Inverse Trigonometric ($\arcsin(x)$, $\operatorname{arccot}(x)$, etc.)
2. **L** – Logarithmic ($\ln(x)$, $\log(x)$)
3. **A** – Algebraic ($x$, $x^2$, $\sqrt{x}$, etc.)
4. **T** – Trigonometric ($\sin(x)$, $\cos(x)$, etc.)
5. **E** – Exponential ($e^x$, $e^{-2x}$, etc.)

*Mnemonic:* "I Like A Tasty Elephant"

---

## Page 1 (Notes & Introduction)

### Example 1: $\int \sqrt{x}\ln(x) \, dx$

- **Choose parts:**
  $$u = \ln(x) \implies du = \frac{1}{x} \, dx$$
  $$dv = \sqrt{x} \, dx = x^{1/2} \, dx \implies v = \frac{2}{3}x^{3/2}$$

- **Apply formula:**
  $$\int \sqrt{x}\ln(x) \, dx = (\ln(x))\left(\frac{2}{3}x^{3/2}\right) - \int \left(\frac{2}{3}x^{3/2}\right)\left(\frac{1}{x} \, dx\right)$$
  $$= \frac{2}{3}x^{3/2}\ln(x) - \frac{2}{3}\int x^{1/2} \, dx$$
  $$= \frac{2}{3}x^{3/2}\ln(x) - \frac{2}{3}\left(\frac{2}{3}x^{3/2}\right) + C$$
  $$= \frac{2}{3}x^{3/2}\ln(x) - \frac{4}{9}x^{3/2} + C$$

---

### Example 2: $\int x\cos(x) \, dx$

- **Choose parts:**
  $$u = x \implies du = dx$$
  $$dv = \cos(x) \, dx \implies v = \sin(x)$$

- **Apply formula:**
  $$\int x\cos(x) \, dx = x\sin(x) - \int \sin(x) \, dx$$
  $$= x\sin(x) + \cos(x) + C$$

---

## Page 2

### Example 3: $\int \ln(x) \cdot x^{-2} \, dx$

- **Choose parts:**
  $$u = \ln(x) \implies du = \frac{1}{x} \, dx$$
  $$dv = x^{-2} \, dx \implies v = \frac{x^{-1}}{-1} = -\frac{1}{x}$$

- **Apply formula:**
  $$\int \ln(x) \cdot x^{-2} \, dx = -\frac{\ln(x)}{x} - \int \left(-\frac{1}{x}\right)\left(\frac{1}{x}\right) dx$$
  $$= -\frac{\ln(x)}{x} + \int x^{-2} \, dx$$
  $$= -\frac{\ln(x)}{x} - x^{-1} + C = -\frac{\ln(x) + 1}{x} + C$$

---

### Example 4: $\int_0^1 \operatorname{arccot}(x) \, dx$

- **Choose parts:**
  $$u = \operatorname{arccot}(x) \implies du = -\frac{1}{1+x^2} \, dx$$
  $$dv = dx \implies v = x$$

- **Apply formula:**
  $$\int_0^1 \operatorname{arccot}(x) \, dx = \left[x \operatorname{arccot}(x)\right]_0^1 - \int_0^1 x\left(-\frac{1}{1+x^2}\right) dx$$
  $$= \left(1\cdot \operatorname{arccot}(1) - 0\right) + \int_0^1 \frac{x}{1+x^2} \, dx$$
  $$= \frac{\pi}{4} + \int_0^1 \frac{x}{1+x^2} \, dx$$

- **Evaluate inner integral using $w$-substitution:**
  $$w = 1 + x^2 \implies dw = 2x \, dx \implies x \, dx = \frac{1}{2} \, dw$$
  *Limits:* $x = 0 \to w = 1$; $x = 1 \to w = 2$
  $$\frac{1}{2}\int_1^2 \frac{1}{w} \, dw = \frac{1}{2}\left[\ln|w|\right]_1^2 = \frac{1}{2}(\ln(2) - \ln(1)) = \frac{1}{2}\ln(2)$$

- **Total:**
  $$= \frac{\pi}{4} + \frac{1}{2}\ln(2)$$

---

## Page 3

### Example 5: $\int x e^{4x} \, dx$

- **Choose parts:**
  $$u = x \implies du = dx$$
  $$dv = e^{4x} \, dx \implies v = \frac{1}{4}e^{4x}$$

- **Apply formula:**
  $$\int x e^{4x} \, dx = \frac{1}{4}x e^{4x} - \int \frac{1}{4}e^{4x} \, dx$$
  $$= \frac{1}{4}x e^{4x} - \frac{1}{16}e^{4x} + C$$

---

### Example 6: $\int x^3 e^x \, dx$ *(Single Step Setup)*

- **Choose parts:**
  $$u = x^3 \implies du = 3x^2 \, dx$$
  $$dv = e^x \, dx \implies v = e^x$$
- **First step:**
  $$\int x^3 e^x \, dx = x^3 e^x - \int 3x^2 e^x \, dx$$

---

### Example 7: $\int t \ln(t + 1) \, dt$

- **Choose parts:**
  $$u = \ln(t + 1) \implies du = \frac{1}{t + 1} \, dt$$
  $$dv = t \, dt \implies v = \frac{1}{2}t^2$$

- **Apply formula:**
  $$\int t \ln(t + 1) \, dt = \frac{1}{2}t^2 \ln(t + 1) - \frac{1}{2}\int \frac{t^2}{t + 1} \, dt$$

- **Polynomial division of $\frac{t^2}{t + 1}$:**
  $$\frac{t^2}{t + 1} = t - 1 + \frac{1}{t + 1}$$
  $$\int \left(t - 1 + \frac{1}{t + 1}\right) dt = \frac{1}{2}t^2 - t + \ln|t + 1|$$

- **Combining terms:**
  $$= \frac{1}{2}t^2 \ln(t + 1) - \frac{1}{2}\left[\frac{1}{2}t^2 - t + \ln|t + 1|\right] + C$$
  $$= \frac{1}{4}\left[2(t^2 - 1)\ln|t + 1| - t^2 + 2t\right] + C$$

---

### Example 8: $\int \frac{(\ln(x))^2}{x} \, dx$ *(Direct $u$-substitution)*

- **Choose substitution:**
  $$u = \ln(x) \implies du = \frac{1}{x} \, dx$$
- **Integrate:**
  $$\int u^2 \, du = \frac{1}{3}u^3 + C = \frac{1}{3}(\ln(x))^3 + C$$

---

## Page 4

### Example 9: $\int \frac{x e^{2x}}{(2x + 1)^2} \, dx$

- **Choose parts:**
  $$u = x e^{2x} \implies du = (2x e^{2x} + e^{2x}) \, dx = e^{2x}(2x + 1) \, dx$$
  $$dv = (2x + 1)^{-2} \, dx \implies v = -\frac{1}{2(2x + 1)}$$

- **Apply formula:**
  $$\int \frac{x e^{2x}}{(2x + 1)^2} \, dx = -\frac{x e^{2x}}{2(2x + 1)} - \int \left(-\frac{1}{2(2x + 1)}\right) e^{2x}(2x + 1) \, dx$$
  $$= -\frac{x e^{2x}}{2(2x + 1)} + \frac{1}{2}\int e^{2x} \, dx$$
  $$= -\frac{x e^{2x}}{2(2x + 1)} + \frac{e^{2x}}{4} + C$$

---

### Example 10: $\int x\sqrt{x - 5} \, dx$

- **Choose parts:**
  $$u = x \implies du = dx$$
  $$dv = (x - 5)^{1/2} \, dx \implies v = \frac{2}{3}(x - 5)^{3/2}$$

- **Apply formula:**
  $$\int x(x - 5)^{1/2} \, dx = \frac{2}{3}x(x - 5)^{3/2} - \frac{2}{3}\int (x - 5)^{3/2} \, dx$$
  $$= \frac{2}{3}x(x - 5)^{3/2} - \frac{2}{3}\left(\frac{2}{5}(x - 5)^{5/2}\right) + C$$
  $$= \frac{2}{3}x(x - 5)^{3/2} - \frac{4}{15}(x - 5)^{5/2} + C$$

---

### Example 11: $\int x\cos(x) \, dx$
$$\int x\cos(x) \, dx = x\sin(x) + \cos(x) + C$$

---

### Example 12: $\int x^3 \sin(x) \, dx$ *(Setup)*

- **Choose parts:**
  $$u = x^3 \implies du = 3x^2 \, dx$$
  $$dv = \sin(x) \, dx \implies v = -\cos(x)$$
- **Setup:**
  $$\int x^3 \sin(x) \, dx = -x^3\cos(x) - \int -\cos(x) \cdot 3x^2 \, dx = -x^3\cos(x) + 3\int x^2\cos(x) \, dx$$

---

## Page 5 (AP / Test Prep Style Questions)

### Problem 7: $\int_1^2 (3x^2 - 2x + 1)\ln(x) \, dx$

- **Choose parts:**
  $$u = \ln(x) \implies du = \frac{1}{x} \, dx$$
  $$dv = (3x^2 - 2x + 1) \, dx \implies v = x^3 - x^2 + x$$

- **Apply formula:**
  $$\int_1^2 (3x^2 - 2x + 1)\ln(x) \, dx = \left[(x^3 - x^2 + x)\ln(x)\right]_1^2 - \int_1^2 \frac{x^3 - x^2 + x}{x} \, dx$$
  $$= \left[(x^3 - x^2 + x)\ln(x)\right]_1^2 - \int_1^2 (x^2 - x + 1) \, dx$$
  - At $x = 2$: $(8 - 4 + 2)\ln(2) = 6\ln(2)$
  - At $x = 1$: $(1 - 1 + 1)\ln(1) = 0$
  - Definite integral of polynomial:
    $$\left[\frac{x^3}{3} - \frac{x^2}{2} + x\right]_1^2 = \left(\frac{8}{3} - 2 + 2\right) - \left(\frac{1}{3} - \frac{1}{2} + 1\right) = \frac{8}{3} - \frac{5}{6} = \frac{11}{6}$$
- **Final Result:**
  $$= 6\ln(2) - \frac{11}{6}$$

---

### Problem 8: $\int x^3 e^x \, dx$ via Tabular Method

| Sign | Derivative ($u$) | Integral ($dv$) |
| :---: | :---: | :---: |
| $(+)$ | $x^3$ | $e^x$ |
| $(-)$ | $3x^2$ | $e^x$ |
| $(+)$ | $6x$ | $e^x$ |
| $(-)$ | $6$ | $e^x$ |
| $(+)$ | $0$ | $e^x$ |

$$\int x^3 e^x \, dx = x^3 e^x - 3x^2 e^x + 6x e^x - 6e^x + C$$

---

### Problem 9: Tabular Values Integration
Given:
$$\int_0^3 f'(x)g(x) \, dx = 6$$

| $x$ | $f(x)$ | $f'(x)$ | $g(x)$ | $g'(x)$ |
|:---:|:---:|:---:|:---:|:---:|
| $0$ | $1$ | $5$ | $-4$ | $3$ |
| $3$ | $5$ | $-3$ | $3$ | $2$ |

Find $\int_0^3 f(x)g'(x) \, dx$:
- By product rule integration by parts:
  $$\int_0^3 f(x)g'(x) \, dx = \left[f(x)g(x)\right]_0^3 - \int_0^3 f'(x)g(x) \, dx$$
  $$= (f(3)g(3) - f(0)g(0)) - 6$$
  $$= ((5)(3) - (1)(-4)) - 6 = (15 + 4) - 6 = 19 - 6 = 13$$

---

### Problem 10: Repeated Integration from Table
Given $f$ is twice-differentiable:

| $x$ | $f(x)$ | $f'(x)$ | $f''(x)$ |
|:---:|:---:|:---:|:---:|
| $0$ | $2$ | $-2$ | $5$ |
| $3$ | $5$ | $7$ | $-2$ |

Evaluate $\int_0^3 x f''(x) \, dx$:
- Tabular integration:
  - $u = x \implies du = dx \implies 0$
  - $dv = f''(x) \, dx \implies v = f'(x) \implies f(x)$
$$\int_0^3 x f''(x) \, dx = \left[x f'(x) - f(x)\right]_0^3$$
$$= \left(3 f'(3) - f(3)\right) - \left(0 \cdot f'(0) - f(0)\right)$$
$$= (3(7) - 5) - (0 - 2) = (21 - 5) + 2 = 16 + 2 = 18$$

---

## Page 6 (Test Prep Multiple Choice)

### 11. $\int x \cos(2x) \, dx$
- **Parts:**
  $$u = x \implies du = dx$$
  $$dv = \cos(2x) \, dx \implies v = \frac{1}{2}\sin(2x)$$
- **Integral:**
  $$= \frac{1}{2}x\sin(2x) - \frac{1}{2}\int \sin(2x) \, dx = \frac{1}{2}x\sin(2x) + \frac{1}{4}\cos(2x) + C$$
- **Correct Answer:** **(D)**

---

### 12. $\int_1^e x^4 \ln(x) \, dx$
- **Parts:**
  $$u = \ln(x) \implies du = \frac{1}{x} \, dx$$
  $$dv = x^4 \, dx \implies v = \frac{x^5}{5}$$
- **Definite Integral:**
  $$\int_1^e x^4 \ln(x) \, dx = \left[\frac{x^5}{5}\ln(x)\right]_1^e - \int_1^e \frac{x^4}{5} \, dx$$
  $$= \left(\frac{e^5}{5}\ln(e) - 0\right) - \left[\frac{x^5}{25}\right]_1^e$$
  $$= \frac{e^5}{5} - \left(\frac{e^5}{25} - \frac{1}{25}\right) = \frac{5e^5 - e^5 + 1}{25} = \frac{4e^5 + 1}{25}$$
- **Correct Answer:** **(B)**

---

### 13. Given $\int f(x)\cos(x) \, dx = f(x)\sin(x) - \int \frac{1}{2}x^3 \sin(x) \, dx$, which could be $f(x)$?
- By standard IBP formula:
  $$\int f(x)\cos(x) \, dx = f(x)\sin(x) - \int f'(x)\sin(x) \, dx$$
- Matching integrands gives:
  $$f'(x) = \frac{1}{2}x^3 \implies f(x) = \int \frac{1}{2}x^3 \, dx = \frac{1}{8}x^4 + C$$
- **Correct Answer:** **(C)** $\frac{1}{8}x^4$

---

## Page 7 (Tabular Method Practice)

### Example 13: $\int \frac{x^2}{e^{2x}} \, dx = \int x^2 e^{-2x} \, dx$

Using the **Tabular Method**:

| Sign | Differentiate ($u$) | Integrate ($dv$) | Product Term |
| :---: | :---: | :---: | :---: |
| $(+)$ | $x^2$ | $e^{-2x}$ | $-\frac{1}{2}x^2 e^{-2x}$ |
| $(-)$ | $2x$ | $-\frac{1}{2}e^{-2x}$ | $-\frac{1}{2}x e^{-2x}$ |
| $(+)$ | $2$ | $\frac{1}{4}e^{-2x}$ | $-\frac{1}{4}e^{-2x}$ |
| $(-)$ | $0$ | $-\frac{1}{8}e^{-2x}$ | $0$ |

- **Summing terms:**
  $$= -\frac{1}{2}x^2 e^{-2x} - \frac{1}{2}x e^{-2x} - \frac{1}{4}e^{-2x} + C$$
  $$= -\frac{1}{4}e^{-2x}\left(2x^2 + 2x + 1\right) + C$$

---

### Example 14: $\int x\sin(x) \, dx$ via Tabular Method

| Sign | Differentiate ($u$) | Integrate ($dv$) | Product Term |
| :---: | :---: | :---: | :---: |
| $(+)$ | $x$ | $\sin(x)$ | $-x\cos(x)$ |
| $(-)$ | $1$ | $-\cos(x)$ | $+\sin(x)$ |
| $(+)$ | $0$ | $-\sin(x)$ | $0$ |

- **Result:**
  $$\int x\sin(x) \, dx = -x\cos(x) + \sin(x) + C$$