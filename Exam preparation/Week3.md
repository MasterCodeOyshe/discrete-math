### **1. Solve the following recurrence relations.**

**Question (a)**
$$y_{n+2} - 4y_{n+1} + 3y_n = 0$$

**Solution:**

This is a linear homogeneous recurrence relation with constant coefficients.

1. **Find the characteristic equation:** Let $y_n = r^n$. Substituting this into the recurrence relation gives:
$$r^2 - 4r + 3 = 0$$
2. **Solve for the roots:** Factor the quadratic equation:
$$(r - 3)(r - 1) = 0$$
The roots are $r_1 = 3$ and $r_2 = 1$. Since the roots are real and distinct, the general solution takes the form:$$y_n = c_1(r_1)^n + c_2(r_2)^n$$
3. **Write the general solution:** Substitute the roots back into the general form:$$y_n = c_1(3)^n + c_2(1)^n$$
    Since $1^n = 1$ for all $n$, we can simplify this to:$$y_n = c_1 \cdot 3^n + c_2$$
    _(where $c_1$ and $c_2$ are arbitrary constants)_


**Question (b)**

$$4y_{n+2} - 5y_{n+1} + y_n = 0, \quad y_0 = 1, y_1 = 2$$

**Solution:**

1. **Find the characteristic equation:**$$4r^2 - 5r + 1 = 0$$
2. **Solve for the roots:** Factor the quadratic equation:$$4r^2 - 4r - r + 1 = 0$$$$4r(r - 1) - 1(r - 1) = 0$$$$(4r - 1)(r - 1) = 0$$
    The roots are $r_1 = \frac{1}{4}$ and $r_2 = 1$.

    
3. **Write the general solution:** Since the roots are distinct, the general form is:$$y_n = c_1(1)^n + c_2\left(\frac{1}{4}\right)^n$$$$y_n = c_1 + c_2\left(\frac{1}{4}\right)^n$$
4. **Apply the initial conditions:** We need to find the specific values for $c_1$ and $c_2$ using the given conditions $y_0 = 1$ and $y_1 = 2$.
    - **For $n = 0$:**$$y_0 = c_1 + c_2\left(\frac{1}{4}\right)^0$$$$1 = c_1 + c_2 \quad \text{--- (Equation 1)}$$
    - **For $n = 1$:**$$y_1 = c_1 + c_2\left(\frac{1}{4}\right)^1$$$$2 = c_1 + \frac{1}{4}c_2 \quad \text{--- (Equation 2)}$$
5. **Solve the system of equations:** From Equation 1, we know $c_1 = 1 - c_2$. Substitute this into Equation 2:$$2 = (1 - c_2) + \frac{1}{4}c_2$$$$2 = 1 - \frac{3}{4}c_2$$$$1 = -\frac{3}{4}c_2$$$$c_2 = -\frac{4}{3}$$
Now substitute $c_2$ back into $c_1 = 1 - c_2$:
$$c_1 = 1 - \left(-\frac{4}{3}\right)$$$$c_1 = 1 + \frac{4}{3}$$$$c_1 = \frac{7}{3}$$
6. **Write the final particular solution:**$$y_n = \frac{7}{3} - \frac{4}{3}\left(\frac{1}{4}\right)^n$$

### **2. Solve the following nonhomogeneous recurrence relations.**

**Question (a)**

$$y_{n+2} - 4y_{n+1} + 4y_n = 2^n$$

**Solution:**

The general solution is the sum of the homogeneous solution ($y_h^{(n)}$) and the particular solution ($y_p^{(n)}$).

1. **Find the homogeneous solution:** Set the right side to 0.
    
    $$y_{n+2} - 4y_{n+1} + 4y_n = 0$$
    
    The characteristic equation is:
    
    $$r^2 - 4r + 4 = 0$$
    
    $$(r - 2)^2 = 0$$
    
    This gives a repeated root of $r = 2$.
    
    The homogeneous solution is:
    
    $$y_h^{(n)} = (c_1 + c_2n)2^n$$
    
1. **Find the particular solution:** The right-hand side is $f(n) = 2^n$. Since $r = 2$ is a root of the characteristic equation with multiplicity 2, our guess for the particular solution must be multiplied by $n^2$.
	![[Pasted image 20260422085949.png]]
    
    Let $y_p^{(n)} = An^2 2^n$. Substitute this back into the original recurrence relation:
    
    $$A(n+2)^2 2^{n+2} - 4A(n+1)^2 2^{n+1} + 4An^2 2^n = 2^n$$
    
    Divide the entire equation by $2^n$:
    
    $$A(n+2)^2 \cdot 4 - 4A(n+1)^2 \cdot 2 + 4An^2 = 1$$
    
    $$4A(n^2 + 4n + 4) - 8A(n^2 + 2n + 1) + 4An^2 = 1$$
    
    Expand and group the terms:
    
    $$4An^2 + 16An + 16A - 8An^2 - 16An - 8A + 4An^2 = 1$$
    
    Notice that the $n^2$ and $n$ terms cancel out:
    
    $$(4A - 8A + 4A)n^2 + (16A - 16A)n + (16A - 8A) = 1$$
    
    $$8A = 1 \implies A = \frac{1}{8}$$
    
    So, the particular solution is:
    
    $$y_p^{(n)} = \frac{1}{8}n^2 2^n$$
    
3. **General Solution:** Add the homogeneous and particular solutions.
    
    $$y_n = y_h^{(n)} + y_p^{(n)}$$
    
    $$y_n = (c_1 + c_2n)2^n + \frac{1}{8}n^2 2^n$$
    

---

**Question (b)**

$$y_{n+2} - 4y_{n+1} + 4y_n = 7$$

**Solution:**

1. **Find the homogeneous solution:** The left side is identical to part (a).
    
    $$y_h^{(n)} = (c_1 + c_2n)2^n$$
    
2. **Find the particular solution:** The right-hand side is a constant, $f(n) = 7$. Since $r = 1$ is _not_ a root of the characteristic equation, we can guess a constant for the particular solution.
    
    Let $y_p^{(n)} = A$. Substitute this into the recurrence relation:
    
    $$A - 4A + 4A = 7$$
    
    $$A = 7$$
    
    So, the particular solution is $y_p^{(n)} = 7$.
    
3. **General Solution:** Add the solutions together.
    
    $$y_n = (c_1 + c_2n)2^n + 7$$
    

---

**Question (c)**

$$y_{n+3} - 4y_{n+2} - y_{n+1} + 4y_n = 3n$$

**Solution:**

1. **Find the homogeneous solution:** Set the right side to 0.
    
    $$y_{n+3} - 4y_{n+2} - y_{n+1} + 4y_n = 0$$
    
    The characteristic equation is:
    
    $$r^3 - 4r^2 - r + 4 = 0$$
    
    Factor by grouping:
    
    $$r^2(r - 4) - 1(r - 4) = 0$$
    
    $$(r^2 - 1)(r - 4) = 0$$
    
    $$(r - 1)(r + 1)(r - 4) = 0$$
    
    The roots are distinct: $r_1 = 1$, $r_2 = -1$, and $r_3 = 4$.
    
    The homogeneous solution is:
    
    $$y_h^{(n)} = c_1(1)^n + c_2(-1)^n + c_3(4)^n = c_1 + c_2(-1)^n + c_3(4)^n$$
    
2. **Find the particular solution:** The right-hand side is a linear polynomial, $f(n) = 3n$. A standard guess would be $An + B$. However, since $r = 1$ is a root of the characteristic equation with multiplicity 1 (represented by the constant term $c_1$ in the homogeneous solution), we must multiply our guess by $n$.
    
    Let $y_p^{(n)} = n(An + B) = An^2 + Bn$.
    
    Substitute $y_p^{(n)}$ into the recurrence relation:
    
    $$[A(n+3)^2 + B(n+3)] - 4[A(n+2)^2 + B(n+2)] - [A(n+1)^2 + B(n+1)] + 4[An^2 + Bn] = 3n$$
    
    Expand the terms:
    
    - $y_{n+3}: A(n^2 + 6n + 9) + B(n + 3)$
        
    - $-4y_{n+2}: -4A(n^2 + 4n + 4) - 4B(n + 2)$
        
    - $-y_{n+1}: -A(n^2 + 2n + 1) - B(n + 1)$
        
    - $4y_n: 4An^2 + 4Bn$
        
    
    Combine and group by powers of $n$:
    
    - **$n^2$ terms:** $(A - 4A - A + 4A)n^2 = 0n^2$ (This cancels out, as expected).
        
    - **$n$ terms:** $(6A + B - 16A - 4B - 2A - B + 4B)n = (-12A)n$
        
    - **Constant terms:** $9A + 3B - 16A - 8B - A - B = -8A - 6B$
        
    
    Equating the coefficients to the right side ($3n + 0$):
    
    $$-12A = 3 \implies A = -\frac{1}{4}$$
    
    $$-8A - 6B = 0 \implies -8\left(-\frac{1}{4}\right) - 6B = 0 \implies 2 - 6B = 0 \implies 6B = 2 \implies B = \frac{1}{3}$$
    
    So, the particular solution is:
    
    $$y_p^{(n)} = -\frac{1}{4}n^2 + \frac{1}{3}n$$
    
3. **General Solution:** Add the homogeneous and particular solutions together.
    
    $$y_n = c_1 + c_2(-1)^n + c_3(4)^n - \frac{1}{4}n^2 + \frac{1}{3}n$$
### **Question 3(a)**

For which smallest integer $n$ is

$$\frac{1}{\sqrt{1}} + \frac{1}{\sqrt{2}} + \dots + \frac{1}{\sqrt{n}} > \sqrt{n}$$

true for all larger integers?

### **Solution**

Let the sum be denoted as $S_n = \sum_{k=1}^n \frac{1}{\sqrt{k}}$. We want to find the smallest integer $n$ for which $S_n > \sqrt{n}$, and then verify that it remains true for all integers larger than $n$.

**Step 1: Test small values of $n$**

- **For $n = 1$:**
    
    $$S_1 = \frac{1}{\sqrt{1}} = 1$$
    
    The inequality asks if $1 > \sqrt{1}$. Since $1 = 1$, the inequality is **false**.
    
- **For $n = 2$:**
    
    $$S_2 = \frac{1}{\sqrt{1}} + \frac{1}{\sqrt{2}} = 1 + \frac{\sqrt{2}}{2} \approx 1 + 0.707 = 1.707$$
    
    The right side is $\sqrt{2} \approx 1.414$.
    
    Since $1.707 > 1.414$, the inequality is **true** for $n=2$.
    

So, $n=2$ is our candidate for the smallest integer. Now, we must prove that the inequality holds for all integers $n \ge 2$.

**Step 2: Prove it holds for all $n \ge 2$ using Mathematical Induction**

- **Base Case:** We have already shown it holds for $n=2$.
    
- **Inductive Hypothesis:** Assume the inequality is true for some arbitrary integer $k \ge 2$. That is, assume:
    
    $$S_k = \frac{1}{\sqrt{1}} + \frac{1}{\sqrt{2}} + \dots + \frac{1}{\sqrt{k}} > \sqrt{k}$$
    
- **Inductive Step:** We need to show it is true for $k+1$. That is, we must show:
    
    $$S_{k+1} > \sqrt{k+1}$$
    
    We can write $S_{k+1}$ as $S_k + \frac{1}{\sqrt{k+1}}$.
    
    Using our inductive hypothesis ($S_k > \sqrt{k}$), we can set up the following inequality:
    
    $$S_{k+1} = S_k + \frac{1}{\sqrt{k+1}} > \sqrt{k} + \frac{1}{\sqrt{k+1}}$$
    
    Now, we need to prove that this right-hand side is strictly greater than $\sqrt{k+1}$:
    
    $$\sqrt{k} + \frac{1}{\sqrt{k+1}} > \sqrt{k+1}$$
    
    To verify this, let's manipulate the inequality. Multiply both sides by the positive term $\sqrt{k+1}$:
    
    $$\sqrt{k}\sqrt{k+1} + 1 > \sqrt{k+1}\sqrt{k+1}$$
    
    $$\sqrt{k(k+1)} + 1 > k + 1$$
    
    Subtract 1 from both sides:
    
    $$\sqrt{k^2+k} > k$$
    
    Since $k$ is a positive integer ($k \ge 1$), we know that $k^2 + k > k^2$.
    
    Taking the square root of both sides (which preserves the inequality for positive numbers):
    
    $$\sqrt{k^2+k} > \sqrt{k^2} = k$$
    
    This statement is clearly true. Working backward, this proves that $\sqrt{k} + \frac{1}{\sqrt{k+1}} > \sqrt{k+1}$.
    
    Combining this with our earlier step:
    
    $$S_{k+1} > \sqrt{k} + \frac{1}{\sqrt{k+1}} > \sqrt{k+1}$$
    
    $$S_{k+1} > \sqrt{k+1}$$
    

The inductive step holds.

**Conclusion:**

By mathematical induction, the inequality is true for all integers $n \ge 2$. The smallest integer for which this is true is **$n = 2$**.

### **Question 4**

Consider the recursively defined sequence

$$p_{n+1} = \frac{(p_n)^2}{2}$$

where the first term is $p_0$.

(a) Compute the next five terms $p_1, p_2, p_3, p_4, p_5$ in terms of $p_0$.

(b) Based on the first terms of the sequence, suggest a closed form expression for $p_n$ in terms of $p_0$ and $n$.

---

### **Solution**

#### **Part (a): Compute the next five terms**

We will substitute each term into the recursive formula to find the next, expressing the denominators as powers of 2 to make pattern recognition easier for part (b).

1. **For $p_1$ (let $n = 0$):**
    
    $$p_1 = \frac{(p_0)^2}{2} = \frac{p_0^2}{2^1}$$
    
2. **For $p_2$ (let $n = 1$):**
    
    $$p_2 = \frac{(p_1)^2}{2} = \frac{\left(\frac{p_0^2}{2}\right)^2}{2} = \frac{\frac{p_0^4}{4}}{2} = \frac{p_0^4}{8} = \frac{p_0^4}{2^3}$$
    
3. **For $p_3$ (let $n = 2$):**
    
    $$p_3 = \frac{(p_2)^2}{2} = \frac{\left(\frac{p_0^4}{2^3}\right)^2}{2} = \frac{\frac{p_0^8}{2^6}}{2} = \frac{p_0^8}{2^7}$$
    
4. **For $p_4$ (let $n = 3$):**
    
    $$p_4 = \frac{(p_3)^2}{2} = \frac{\left(\frac{p_0^8}{2^7}\right)^2}{2} = \frac{\frac{p_0^{16}}{2^{14}}}{2} = \frac{p_0^{16}}{2^{15}}$$
    
5. **For $p_5$ (let $n = 4$):**
    
    $$p_5 = \frac{(p_4)^2}{2} = \frac{\left(\frac{p_0^{16}}{2^{15}}\right)^2}{2} = \frac{\frac{p_0^{32}}{2^{30}}}{2} = \frac{p_0^{32}}{2^{31}}$$
    

---

#### **Part (b): Suggest a closed-form expression for $p_n$**

To find the closed-form expression, let's analyze the pattern in the terms we just calculated:

- $p_1 = \frac{p_0^2}{2^1}$
    
- $p_2 = \frac{p_0^4}{2^3}$
    
- $p_3 = \frac{p_0^8}{2^7}$
    
- $p_4 = \frac{p_0^{16}}{2^{15}}$
    
- $p_5 = \frac{p_0^{32}}{2^{31}}$
    

Notice the relationship between the index $n$, the exponent of $p_0$, and the exponent of the denominator $2$:

- **Exponent of $p_0$:** It doubles with each step ($2, 4, 8, 16, 32$). This can be written as $2^n$.
    
- **Exponent of the denominator $2$:** It is always one less than the exponent of $p_0$ ($1, 3, 7, 15, 31$). Since the exponent of $p_0$ is $2^n$, the exponent of the denominator is $2^n - 1$.
    

Putting this together, the closed-form expression for $p_n$ is:

$$p_n = \frac{p_0^{2^n}}{2^{2^n - 1}}$$

_(Note: This can also be rewritten in a slightly more elegant form by factoring out a 2: $p_n = 2\left(\frac{p_0}{2}\right)^{2^n}$, which confirms the same relationship)._

### **Question 5**

Consider the recursively defined sequence

$$a_{n+1} = 3(a_n)^2$$

with first term $a_0$. Compute a closed form expression based on the first terms of the sequence.

---

### **Solution**

To find the closed-form expression, we need to compute the first few terms of the sequence to identify an emerging pattern. We will express each term based solely on $a_0$.

**Step 1: Compute the first few terms**

1. **For $n = 0$:**
    
    $$a_1 = 3(a_0)^2 = 3^1 \cdot a_0^2$$
    
2. **For $n = 1$:**
    
    $$a_2 = 3(a_1)^2 = 3\left(3 a_0^2\right)^2 = 3 \left(3^2 \cdot a_0^4\right) = 3^3 \cdot a_0^4$$
    
3. **For $n = 2$:**
    
    $$a_3 = 3(a_2)^2 = 3\left(3^3 a_0^4\right)^2 = 3 \left(3^6 \cdot a_0^8\right) = 3^7 \cdot a_0^8$$
    
4. **For $n = 3$:**
    
    $$a_4 = 3(a_3)^2 = 3\left(3^7 a_0^8\right)^2 = 3 \left(3^{14} \cdot a_0^{16}\right) = 3^{15} \cdot a_0^{16}$$
    

**Step 2: Analyze the patterns**

Let's look closely at the exponents for each term:

- **$a_1 = 3^1 \cdot a_0^2$**
    
- **$a_2 = 3^3 \cdot a_0^4$**
    
- **$a_3 = 3^7 \cdot a_0^8$**
    
- **$a_4 = 3^{15} \cdot a_0^{16}$**
    

We can break down the pattern into two parts based on the index $n$:

1. **The exponent of $a_0$:** The sequence is $2, 4, 8, 16$. This represents powers of $2$, exactly doubling each time. For any given $n$, the exponent is $2^n$.
    
2. **The exponent of $3$:** The sequence is $1, 3, 7, 15$. Notice that each of these numbers is exactly one less than the corresponding exponent of $a_0$. Since the exponent of $a_0$ is $2^n$, the exponent of $3$ is $2^n - 1$.
    

**Step 3: Write the closed-form expression**

Combining these two patterns, we get the final closed-form expression for the $n$-th term:

$$a_n = 3^{2^n - 1} \cdot a_0^{2^n}$$

_(Note: If you want to write this in a slightly more compact way by grouping the terms, you can pull out a factor of $\frac{1}{3}$ to match the exponents: $a_n = \frac{1}{3} (3a_0)^{2^n}$. Both forms are mathematically equivalent.)_