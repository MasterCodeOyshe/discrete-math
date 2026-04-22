## 1.

### (a) $y_{n+2} - 4y_{n+1} + 3y_n = 0$

**Characteristic Equation:** $r^2 - 4r + 3 = 0$.
**Factor:** $(r-3)(r-1) = 0$, so roots are $r_1 = 3$ and $r_2 = 1$.
**General Solution:** $y_n = c_1(3^n) + c_2(1^n)$
 $y_n = c_1 3^n + c_2$
### (b) $4y_{n+2} - 5y_{n+1} + y_n = 0$ with $y_0 = 1, y_1 = 2$

**Characteristic Equation:** $4r^2 - 5r + 1 = 0$.
**Factor:** $(4r-1)(r-1) = 0$, so roots are $r_1 = \frac{1}{4}$ and $r_2 = 1$.
**General Solution:** $y_n = c_1(1)^n + c_2(\frac{1}{4})^n = c_1 + c_2(\frac{1}{4})^n$.
**Initial Conditions:**
- $n=0: c_1 + c_2 = 1$
- $n=1: c_1 + \frac{1}{4}c_2 = 2$

Subtracting the second from the first: $\frac{3}{4}c_2 = -1 \Rightarrow c_2 = -\frac{4}{3}$. Then $c_1 = 1 + \frac{4}{3} = \frac{7}{3}$.
$y_n = \frac{7}{3} - \frac{4}{3}(\frac{1}{4})^n$

---

## 3.

1.  $n=1$: $\frac{1}{\sqrt{1}} = 1$. Is $1 > \sqrt{1}$? No, $1 = 1$.
    
2. $n=2$:  $1 + \frac{1}{\sqrt{2}} \approx 1 + 0.707 = 1.707$. Is $1.707 > \sqrt{2} \approx 1.414$? **Yes.**
- **Smallest integer $n$:** **2**
    

---

## 4.

### (a) Compute the next five terms:


- $p_1 = \frac{p_0^2}{2^1}$
    
- $p_2 = \frac{(p_1)^2}{2} = \frac{(p_0^2 / 2^1)^2}{2} = \frac{p_0^4 / 2^2}{2} = \mathbf{\frac{p_0^4}{2^3}}$
    
- $p_3 = \frac{(p_2)^2}{2} = \frac{(p_0^4 / 2^3)^2}{2} = \frac{p_0^8 / 2^6}{2} = \mathbf{\frac{p_0^8}{2^7}}$
    
- $p_4 = \frac{(p_3)^2}{2} = \frac{(p_0^8 / 2^7)^2}{2} = \frac{p_0^{16} / 2^{14}}{2} = \mathbf{\frac{p_0^{16}}{2^{15}}}$
    
- $p_5 = \frac{(p_4)^2}{2} = \frac{(p_0^{16} / 2^{15})^2}{2} = \frac{p_0^{32} / 2^{30}}{2} = \mathbf{\frac{p_0^{32}}{2^{31}}}$
    

### (b) Closed form expression:

Notice the patterns:

- The power of $p_0$ is $2^n$.
    
- The denominator follows $2^1, 2^3, 2^7, 2^{15}, 2^{31}$.
    
- The exponent of the denominator is $2^n - 1$.
    
- **Final Answer:** $p_n = \frac{p_0^{2^n}}{2^{2^n - 1}} = \mathbf{2 \left( \frac{p_0}{2} \right)^{2^n}}$
    

---

## 5.


- $a_1 = 3a_0^2$
    
- $a_2 = 3(3a_0^2)^2 = 3(3^2 a_0^4) = 3^3 a_0^4$
    
- $a_3 = 3(3^3 a_0^4)^2 = 3(3^6 a_0^8) = 3^7 a_0^8$
    
- $a_4 = 3(3^7 a_0^8)^2 = 3(3^{14} a_0^{16}) = 3^{15} a_0^{16}$
    

- The power of $a_0$ is $2^n$.
    
- The power of $3$ is $1, 3, 7, 15...$ which is $2^n - 1$.
    
- **Final Answer:** $a_n = 3^{2^n - 1} \cdot a_0^{2^n}$
