# 1 
![[Pasted image 20260318123200.png]]
To solve the recurrence relation $y_{n+2} - 5y_{n+1} + 6y_n = 0$, we follow the standard method for linear homogeneous recurrences.

### 1. The Characteristic Equation

Assuming a solution of the form $y_n = r^n$, we substitute it into the relation to get the characteristic equation:

$$r^2 - 5r + 6 = 0$$

### 2. Factor the Quadratic

We need to find two numbers that multiply to $6$ and add to $-5$:

$$(r - 2)(r - 3) = 0$$

The roots are:

- $r_1 = 2$
    
- $r_2 = 3$
    

### 3. General Solution

For distinct real roots $r_1$ and $r_2$, the general solution is $y_n = A(r_1)^n + B(r_2)^n$. Substituting our roots gives the final result.

---

### **The Answer**

**$y_n = A * 2^n + B * 3^n$**

# 2
![[Pasted image 20260318123222.png]]
To solve the nonhomogeneous recurrence relation $y_{n+2} - 5y_{n+1} + 6y_n = 2^n$, we need to find the **homogeneous solution** and the **particular solution**.

---

### **1. Find the Homogeneous Solution ($y_h$)**

The homogeneous equation is $y_{n+2} - 5y_{n+1} + 6y_n = 0$.

The characteristic equation is:

$$r^2 - 5r + 6 = 0$$

- **Factoring:** $(r - 2)(r - 3) = 0$
    
- **Roots:** $r_1 = 2$, $r_2 = 3$
    

This gives us:

$y_h = A * 2^n + B * 3^n$

---

### **2. Find the Particular Solution ($y_p$)**

The nonhomogeneous part is $f(n) = 2^n$. Usually, we would guess $y_p = A * 2^n$.

**However**, note that $r = 2$ is already a root of our characteristic equation. To find a linearly independent particular solution, we must multiply our guess by $n$:

$y_p = A * n * 2^n$

Now, substitute $y_p$ back into the original recurrence:

$A * (n+2) * 2^{n+2} - 5(A * (n+1) * 2^{n+1}) + 6(A * n * 2^n) = 2^n$

Divide every term by $2^n$:

$A * (n+2) * 4 - 5A * (n+1) * 2 + 6An = 1$

$4An + 8A - 10An - 10A + 6An = 1$

$-2A = 1$

**A = -1/2**

So, the particular solution is:

**$y_p = (-1/2) * n * 2^n$** (which is also **$-n * 2^(n-1)$**)

---

### **3. General Solution**

Combine the two parts ($y_n = y_h + y_p$):

**$y_n = c_1 * 2^n + c_2 * 3^n - (1/2) * n * 2^n$**

---

### **The Answer**

**$y_n = c_1 * 2^n + c_2 * 3^n - n * 2^(n-1)$**

Would you like to see how the solution would differ if the right side was $5^n$ instead of $2^n$?

# 3
![[Pasted image 20260318125046.png]]

To solve for the terms $p_1$ through $p_5$, we apply the recursive rule $p_{n+1} = (p_n)^2 / 2$ step-by-step.

### Step-by-Step Calculation

- **p_1**: Substitute $n=0$ into the formula.
    
    $$p_1 = (p_0)^2 / 2$$
    
    **$p_1 = p_0^2 / 2$**
    
- **p_2**: Square $p_1$ and divide by 2.
    
    $$p_2 = (p_0^2 / 2)^2 / 2 = (p_0^4 / 4) / 2 = p_0^4 / 8$$
    
    **$p_2 = p_0^4 / 2^3$**
    
- **p_3**: Square $p_2$ and divide by 2.
    
    $$p_3 = (p_0^4 / 2^3)^2 / 2 = (p_0^8 / 2^6) / 2 = p_0^8 / 2^7$$
    
    **$p_3 = p_0^8 / 2^7$**
    
- **p_4**: Square $p_3$ and divide by 2.
    
    $$p_4 = (p_0^8 / 2^7)^2 / 2 = (p_0^{16} / 2^{14}) / 2 = p_0^{16} / 2^{15}$$
    
    **$p_4 = p_0^16 / 2^15$**
    
- **p_5**: Square $p_4$ and divide by 2.
    
    $$p_5 = (p_0^{16} / 2^{15})^2 / 2 = (p_0^{32} / 2^{30}) / 2 = p_0^{32} / 2^{31}$$
    
    **$p_5 = p_0^32 / 2^31$**
    

---

### Summary of Values

Using the requested notation:

| **Term**  | **Value**                                      |
| --------- | ---------------------------------------------- |
| **$p_1$** | **$p_0^2 / 2$**                                |
| **$p_2$** | **$p_0^4 / 8$** (or $p_0^4 / 2^3$)             |
| **$p_3$** | **$p_0^8 / 128$** (or $p_0^8 / 2^7$)           |
| **$p_4$** | **$p_0^16 / 32768$** (or $p_0^16 / 2^15$)      |
| **$p_5$** | **$p_0^32 / 2147483648$** (or $p_0^32 / 2^31$) |

### The General Pattern

The closed-form expression for this sequence is:

**$p_n = p_0^(2^n) / 2^(2^n - 1)$**


# 4
![[Pasted image 20260318124033.png]]
To find the closed-form expression for the sequence $c_{n+1} = 25(c_n)^2$, let’s track the growth of the exponents for both the constant 25 and the initial term $c_0$.

### Iteration Steps

- **$c_0$** = $c_0$
    
- **$c_1$** = $25 * c_0^2$
    
- **$c_2$** = $25 * (25 * c_0^2)^2 = 25 * 25^2 * c_0^4 = 25^3 * c_0^4$
    
- **$c_3$** = $25 * (25^3 * c_0^4)^2 = 25 * 25^6 * c_0^8 = 25^7 * c_0^8$
    

---

### Exponent Patterns

- **Exponent of $c_0$:** Follows the sequence $2, 4, 8...$, which is **$2^n$**.
    
- **Exponent of $25$:** Follows the sequence $1, 3, 7...$. This is a geometric progression sum $2^n - 1$.
    

---

### **The Answer**

Using your requested formatting:

**$c_n = 25^(2^n - 1) * c_0^(2^n)$**

---

### **Simplified Form**

Since $25 = 5^2$, you can also write this as:

**$c_n = (1/25) * (25 * c_0)^(2^n)$**

# 5
![[Pasted image 20260318125415.png]]

To determine the correct form for $y_n$ in the recurrence relation $y_{n+3} - 4y_{n+2} - y_{n+1} + 4y_n = 3n$, we need to find both the **homogeneous solution** ($y_h$) and the **particular solution** ($y_p$).

---

### **1. The Homogeneous Solution ($y_h$)**

The homogeneous equation is $y_{n+3} - 4y_{n+2} - y_{n+1} + 4y_n = 0$.

The characteristic equation is:

$$r^3 - 4r^2 - r + 4 = 0$$

We can factor this by grouping:

$r^2(r - 4) - 1(r - 4) = 0$

$(r^2 - 1)(r - 4) = 0$

$(r - 1)(r + 1)(r - 4) = 0$

**Roots:** $r_1 = 1$, $r_2 = -1$, $r_3 = 4$.

$y_h = c_1 * 1^n + c_2 * (-1)^n + c_3 * 4^n = c_1 + c_2 * (-1)^n + c_3 * 4^n$

---

### **2. The Particular Solution ($y_p$)**

The nonhomogeneous part is $f(n) = 3n$, which is a polynomial of degree 1.

Usually, we would guess $y_p = An + B$.

**However**, note that $r = 1$ is a root of the characteristic equation. When the constant term of the polynomial is a root, we must multiply the entire guess by $n$.

Therefore, the form for $y_p$ is:

$y_p = n * (An + B) = An^2 + Bn$

---

### **3. The Correct General Form**

Combining both parts ($y_n = y_h + y_p$):

$y_n = c_1 + c_2 * (-1)^n + c_3 * 4^n + An^2 + Bn$


Our original recurrence relation is:

$$y_{n+3} - 4y_{n+2} - y_{n+1} + 4y_n = 3n$$

Our safe guess for the particular solution is:

$$y_p(n) = An^2 + Bn$$

Before we can plug this in, we need to figure out what $y_p$ looks like for the $n+1$, $n+2$, and $n+3$ terms. We do this by replacing every $n$ in our guess with those specific shifts:

- **For $y_n$:** $An^2 + Bn$
    
- **For $y_{n+1}$:** $A(n+1)^2 + B(n+1) = A(n^2 + 2n + 1) + Bn + B$
    
    - _Simplified:_ $An^2 + (2A + B)n + (A + B)$
        
- **For $y_{n+2}$:** $A(n+2)^2 + B(n+2) = A(n^2 + 4n + 4) + Bn + 2B$
    
    - _Simplified:_ $An^2 + (4A + B)n + (4A + 2B)$
        
- **For $y_{n+3}$:** $A(n+3)^2 + B(n+3) = A(n^2 + 6n + 9) + Bn + 3B$
    
    - _Simplified:_ $An^2 + (6A + B)n + (9A + 3B)$
        

---

### **Step 2: Plug Everything In**

Now we substitute those simplified blocks back into the massive left side of our original equation.

$$[An^2 + (6A+B)n + 9A+3B] - 4[An^2 + (4A+B)n + 4A+2B] - [An^2 + (2A+B)n + A+B] + 4[An^2 + Bn] = 3n$$

It looks terrifying, but we are going to tame it by grouping the terms by their powers of $n$.

---

### **Step 3: Group by Powers of $n$**

We will gather all the $n^2$ pieces, all the $n$ pieces, and all the constant (number-only) pieces.

**1. The $n^2$ Terms:**

$$An^2 - 4An^2 - An^2 + 4An^2 = (1 - 4 - 1 + 4)An^2 = 0$$

_(Notice how they perfectly cancel out to zero! This confirms our math is on the right track, because the right side of the equation, $3n$, doesn't have an $n^2$ term either)._

**2. The $n$ Terms:**

$$(6A + B)n - 4(4A + B)n - (2A + B)n + 4Bn$$

Let's distribute and combine the coefficients:

$$6A + B - 16A - 4B - 2A - B + 4B$$

Group the $A$'s and $B$'s:

$$(6 - 16 - 2)A + (1 - 4 - 1 + 4)B$$

$$-12A + 0B$$

**Result:** $-12A$

**3. The Constant Terms (No $n$):**

$$(9A + 3B) - 4(4A + 2B) - (A + B) + 4(0)$$

Let's distribute and combine:

$$9A + 3B - 16A - 8B - A - B$$

Group the $A$'s and $B$'s:

$$(9 - 16 - 1)A + (3 - 8 - 1)B$$

**Result:** $-8A - 6B$

---

### **Step 4: Equate Coefficients to the Right Side**

After that massive cleanup, the entire left side of our equation simplifies to this beautiful, tiny expression:

$$-12An + (-8A - 6B) = 3n + 0$$

Now, we just match the left side to the right side!

**Match the $n$ terms to find $A$:**

$$-12A = 3$$

$$A = -\frac{3}{12} = -\frac{1}{4}$$

**Match the constant terms to find $B$:**

$$-8A - 6B = 0$$

Substitute our new $A$ value in:

$$-8(-\frac{1}{4}) - 6B = 0$$

$$2 - 6B = 0$$

$$2 = 6B$$

$$B = \frac{2}{6} = \frac{1}{3}$$

---

### **Step 5: The Final Form**

We found them! $A = -1/4$ and $B = 1/3$.

Now we just drop those specific numbers back into the "skeleton" equation from earlier to get our final, fully realized General Solution:

$$y_n = c_1 + c_2(-1)^n + c_3(4)^n - \frac{1}{4}n^2 + \frac{1}{3}n$$

---

Would you like to try setting up the initial homogeneous and particular "guesses" for one more practice equation to test your understanding, or are you ready to move on to initial conditions?
# 6
![[Pasted image 20260318124114.png]]
To determine the smallest integer $n$ for which the inequality $1 + 1/2 + 1/3 + ... + 1/n \ge \ln(n+1)$ holds true for all larger integers, we can compare the harmonic sum to the area under the curve $f(x) = 1/x$.

### **Testing the values**

Let's calculate both sides for the first few values of $n$:

|**n**|**Harmonic Sum (Hn​)**|**ln(n+1)**|**Hn​≥ln(n+1)?**|
|---|---|---|---|
|**1**|$1$|$\ln(2) \approx 0.693$|**True**|
|**2**|$1 + 0.5 = 1.5$|$\ln(3) \approx 1.098$|**True**|
|**3**|$1.5 + 0.333 = 1.833$|$\ln(4) \approx 1.386$|**True**|

---

### **Conceptual Explanation**

This inequality is a fundamental property of the harmonic series related to the **Integral Test**.

The sum $1 + 1/2 + \dots + 1/n$ represents the area of $n$ rectangles with width 1 and heights $1, 1/2, \dots, 1/n$. Because the function $f(x) = 1/x$ is decreasing, the left-endpoint Riemann sum (the harmonic sum) will always be greater than the definite integral of the function over the same interval.

The integral from 1 to $n+1$ is:

$$\int_{1}^{n+1} \frac{1}{x} dx = [\ln(x)]_{1}^{n+1} = \ln(n+1) - \ln(1) = \ln(n+1)$$

Since the rectangles "overhang" the curve $1/x$, the sum is always greater than or equal to the integral for all $n \ge 1$.

### **The Answer**

The inequality is already true at the very first step. Therefore, the smallest integer $n$ is:

**b. 1**

---

Would you like me to show you how this relates to the **Euler-Mascheroni constant** ($\gamma$), which describes the specific gap between these two values as $n$ goes to infinity?


# 7
![[Pasted image 20260318124218.png]]

To solve the nonhomogeneous recurrence relation $y_{n+2} - 5y_{n+1} + 6y_n = 10$, we need to find both the **homogeneous solution** and the **particular solution**.

---

### **1. Homogeneous Solution ($y_h$)**

The homogeneous equation is $y_{n+2} - 5y_{n+1} + 6y_n = 0$. We use the characteristic equation:

$$r^2 - 5r + 6 = 0$$

- **Factoring:** $(r - 2)(r - 3) = 0$
    
- **Roots:** $r_1 = 2, r_2 = 3$
    

The homogeneous part is:

**$y_h = c_1 * 2^n + c_2 * 3^n$**

---

### **2. Particular Solution ($y_p$)**

The nonhomogeneous part is a constant (10). Since $r = 1$ is not a root of our characteristic equation, we assume a constant particular solution:

**$y_p = A$**

Substitute $y_p = A$ into the original recurrence:

$A - 5A + 6A = 10$

$2A = 10$

**A = 5**

So, the particular solution is:

**$y_p = 5$**

---

### **3. General Solution**

We combine the two parts ($y_n = y_h + y_p$):

**$y_n = c_1 * 2^n + c_2 * 3^n + 5$**

---

### **Summary Table**

| **Component**            | **Expression**                        |
| ------------------------ | ------------------------------------- |
| **Characteristic Roots** | 2 and 3                               |
| **Homogeneous Part**     | $c_1 * 2^n + c_2 * 3^n$               |
| **Particular Part**      | 5                                     |
| **General Solution**     | **$y_n = c_1 * 2^n + c_2 * 3^n + 5$** |

Would you like me to find the specific values for $c_1$ and $c_2$ if you have initial conditions like $y_0$ and $y_1$?

# 8
![[Pasted image 20260318124351.png]]

To find the closed-form expression for the sequence $b_{n+1} = 4(b_n)^2$, we can trace the pattern through the first several terms.

### **Step 1: Expand the first few terms**

- $b_0 = b_0$
    
- $b_1 = 4 * b_0^2$
    
- $b_2 = 4 * (b_1)^2 = 4 * (4 * b_0^2)^2 = 4 * 4^2 * b_0^4 = 4^3 * b_0^4$
    
- $b_3 = 4 * (b_2)^2 = 4 * (4^3 * b_0^4)^2 = 4 * 4^6 * b_0^8 = 4^7 * b_0^8$
    

---

### **Step 2: Identify the exponents**

- **The base $b_0$:** The exponent follows the power of 2: $2, 4, 8, \dots$, which is **$2^n$**.
    
- **The base $4$:** The exponent follows the sequence $1, 3, 7, \dots$. This sequence is always one less than a power of 2: **$2^n - 1$**.
    

---

### **The Answer**

Using your requested formatting:

**b_n = 4^(2^n - 1) * b_0^(2^n)**

---

### **Alternative Simplified Form**

Since $4 = 2^2$, you can also combine the bases or rewrite it as:

**b_n = (1/4) * (4 * b_0)^(2^n)**

# 9 
![[Pasted image 20260318124837.png]]

This problem follows the same logic as the previous one, just with a constant of **3** instead of 4.

### Step-by-Step Breakdown

1. **List the terms:**
    
    - $a_0 = a_0$
        
    - $a_1 = 3 * a_0^2$
        
    - $a_2 = 3 * (3 * a_0^2)^2 = 3 * 3^2 * a_0^{2*2} = 3^3 * a_0^4$
        
    - $a_3 = 3 * (3^3 * a_0^4)^2 = 3 * 3^6 * a_0^{2*4} = 3^7 * a_0^8$
        
2. **Identify the pattern:**
    
    - The exponent of $a_0$ is doubling each time: **$2^n$**.
        
    - The exponent of $3$ is following the sequence $1, 3, 7, ...$ which is **$2^n - 1$**.
        

---

### **The Answer**

Using your required formatting:

**$a_n = 3^(2^n - 1) * a_0^(2^n)$**

---

### **Alternative Simplified Form**

You can also express this as:

$a_n = (1/3) * (3 * a_0)^(2^n)$

Would you like to try one where the exponent in the recursion is different, like $a_{n+1} = 3(a_n)^3$?
# 10
![[Pasted image 20260318124442.png]]

To solve the linear homogeneous recurrence relation $4y(n + 2) - 5y(n + 1) + y_n = 0$ with initial conditions $y_0 = 1$ and $y_1 = 2$, we use the characteristic equation method.

### 1. Find the Characteristic Equation

Assume a solution of the form $y_n = r^n$. Substituting this into the recurrence gives:

$$4r^2 - 5r + 1 = 0$$

Now, we factor the quadratic equation:

$$(4r - 1)(r - 1) = 0$$

The roots are:

- $r_1 = 1$
    
- $r_2 = 1/4$
    

### 2. Write the General Solution

Since the roots are distinct and real, the general solution is:

$y_n = c_1 * (1)^n + c_2 * (1/4)^n$

Which simplifies to:

$y_n = c_1 + c_2 * (1/4)^n$

---

### 3. Solve for Constants using Initial Conditions

We use $y_0 = 1$ and $y_1 = 2$ to find the values of $c_1$ and $c_2$:

- **For n = 0:**
    
    $y_0 = c_1 + c_2 * (1/4)^0 = 1$
    
    $c_1 + c_2 = 1$ --- (Equation 1)
    
- **For n = 1:**
    
    $y_1 = c_1 + c_2 * (1/4)^1 = 2$
    
    $c_1 + (1/4) * c_2 = 2$ --- (Equation 2)
    

**Subtract Equation 2 from Equation 1:**

$(c_1 - c_1) + (c_2 - 1/4 * c_2) = 1 - 2$

$(3/4) * c_2 = -1$

$c_2 = -4/3$

**Substitute $c_2$ back into Equation 1:**

$c_1 - 4/3 = 1$

$c_1 = 1 + 4/3$

$c_1 = 7/3$

---

### **The Answer**

Substituting the constants back into the general solution:

**y_n = 7/3 - (4/3) * (1/4)^n**

