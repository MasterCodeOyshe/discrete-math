**Here is the complete, unified list of ALL the rules you need for solving _linear recurrence relations with constant coefficients_ using the method of characteristic equations + undetermined coefficients.**  
These rules synthesize the standard theory from recurrence‑relation references such as the characteristic‑polynomial method and the general solution structure for distinct vs. repeated roots [Wikipedia](https://en.wikipedia.org/wiki/Linear_recurrence_with_constant_coefficients) [Brilliant](https://brilliant.org/wiki/linear-recurrence-relations/).

---

# ⭐ **MASTER LIST OF RULES FOR SOLVING RECURRENCES**

Below is the full set of rules you’ve been implicitly learning.  
I’m organizing them into **Homogeneous Rules** and **Particular‑Solution Guessing Rules**.

---

# 🟦 **A. RULES FOR THE HOMOGENEOUS PART**

These rules come from the characteristic polynomial method.

### **1. Form the characteristic equation**

For a recurrence: [ y_{n+k} + a_{k-1}y_{n+k-1} + \dots + a_0 y_n = 0 ] the characteristic equation is: [ r^k + a_{k-1}r^{k-1} + \dots + a_0 = 0 ] [Wikipedia](https://en.wikipedia.org/wiki/Linear_recurrence_with_constant_coefficients)

---

### **2. Distinct real roots**

If the characteristic equation has **distinct roots** (r_1, r_2, \dots, r_k), then: [ y_n^{(h)} = c_1 r_1^n + c_2 r_2^n + \dots + c_k r_k^n ] [Brilliant](https://brilliant.org/wiki/linear-recurrence-relations/)

---

### **3. Repeated roots**

If a root (r) has multiplicity (m), then the corresponding homogeneous solutions are: [ r^n,; n r^n,; n^2 r^n,; \dots,; n^{m-1} r^n ] [web.stanford.edu](https://web.stanford.edu/~linkewei/pdf/2020_linearrec.pdf)

Example:  
If root (2) has multiplicity 2 → solutions: (2^n) and (n2^n).

---

### **4. Complex roots**

If the characteristic equation has complex roots (re^{\pm i\theta}), the solutions become: [ r^n \cos(n\theta),\quad r^n \sin(n\theta) ] (This follows from Euler’s formula; standard recurrence theory.)

---

# 🟩 **B. RULES FOR THE PARTICULAR SOLUTION (UND. COEFFICIENTS)**

These rules tell you what _shape_ to guess for the particular solution.

The key principle:

> **Your guess must NOT duplicate any part of the homogeneous solution.**  
> If it does, multiply by (n) enough times to make it independent.

This is the same principle used in differential equations and is supported by the general formula for linear recurrences with repeated roots [web.stanford.edu](https://web.stanford.edu/~linkewei/pdf/2020_linearrec.pdf).

---

## **B1. RHS is an exponential (k^n)**

### **Case 1: (k) is NOT a root of the characteristic equation**

Guess: [ y_n^{(p)} = A k^n ]

### **Case 2: (k) _is_ a root of multiplicity (m)**

Multiply by (n^m): [ y_n^{(p)} = A n^m k^n ]

Example:  
RHS = (2^n), and root (2) has multiplicity 2 → guess: [ y_n^{(p)} = A n^2 2^n ]

---

## **B2. RHS is a polynomial in (n)**

Let the RHS be a polynomial of degree (d): [ P_d(n) = a_d n^d + \dots + a_1 n + a_0 ]

### **Case 1: 1 is NOT a root of the characteristic equation**

Guess a polynomial of degree (d): [ y_n^{(p)} = bn^d + \dots + kn + m ]

### **Case 2: 1 _is_ a root of multiplicity (m)**

Multiply by (n^m): [ y_n^{(p)} = n^m(\text{polynomial of degree } d) ]

Example:  
RHS = (3n) (degree 1), and root (1) has multiplicity 1 → guess degree (1+1=2): [ y_n^{(p)} = an^2 + bn + c ]

---

## **B3. RHS is a constant (K)**

A constant is a polynomial of degree 0.

### If 1 is NOT a root:

Guess: [ y_n^{(p)} = A ]

### If 1 _is_ a root of multiplicity (m):

Guess: [ y_n^{(p)} = A n^m ]

---

## **B4. RHS is a combination (sum) of types**

If RHS = (3n + 5^n), then:

- Solve for (3n) using polynomial rules
- Solve for (5^n) using exponential rules
- Add the two particular solutions

Linearity guarantees this works [Mathematical Institute](https://people.maths.ox.ac.uk/bays/teaching/3u03/notes/11-recurrenceRelations.pdf).

---

# 🟧 **C. FINAL GENERAL SOLUTION**

Always: [ y_n = y_n^{(h)} + y_n^{(p)} ]

Then use initial conditions to solve for the constants (c_1, c_2, \dots).

---

# 🟪 **D. OPTIONAL ADVANCED RULES**

These come from the general theory of linear recurrences:

### **1. If the characteristic polynomial is ((r-1)^k), the solution is a polynomial of degree (k-1)**

(This is the finite‑difference interpretation.)  
[web.stanford.edu](https://web.stanford.edu/~linkewei/pdf/2020_linearrec.pdf)

### **2. Generating functions can solve any linear recurrence**

(But this is a different method.)

### **3. Matrix methods (companion matrix) also solve any recurrence**

(Useful for high‑order recurrences.)

---

# ✅ If you want, I can turn this into a **cheat sheet**, a **flowchart**, or a **visual diagram** so you can memorize it instantly.