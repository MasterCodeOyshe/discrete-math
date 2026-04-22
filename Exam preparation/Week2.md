### **Section A**
### **Question**

**1. Simplify the Boolean expression:** $F = p \cdot q + p \cdot q'$
### **Solution**
To simplify the given Boolean expression, we can use the standard laws of Boolean algebra.
**Given expression:**
$$F = p \cdot q + p \cdot q'$$
**Step-by-step simplification:**
1. **Distributive Law:** Factor out the common variable $p$ from both terms.$$F = p \cdot (q + q')$$
2. **Complement Law:** In Boolean algebra, a variable ORed with its complement is always equal to 1 (True). Therefore, $q + q' = 1$.$$F = p \cdot (1)$$
3. **Identity Law:** A variable ANDed with 1 is always equal to the variable itself.$$F = p$$
**Final Answer:**
The simplified Boolean expression is **$F = p$**.

### **Question**

**2. Use DeMorgan Law to re-write $(p + q)'$**
### **Solution**
De Morgan's Laws for Boolean algebra define how to distribute a complement (NOT) across an OR ($+$) or AND ($\cdot$) operation.
The specific law needed here states that the complement of a sum is equal to the product of the individual complements:
$$(x + y)' = x' \cdot y'$$

Applying this rule to the given expression:
1. **Given:** $(p + q)'$
2. **Apply De Morgan's:** Distribute the complement to both variables and change the operation from OR ($+$) to AND ($\cdot$).
3. **Result:** $p' \cdot q'$
**Final Answer:**
The re-written expression is **$p' \cdot q'$**.

### **Question 3**

**3. How many rows are required in a truth table for a Boolean function with 3 variables?**
### **Solution**
To determine the number of rows required in a truth table, use the formula **$2^n$**, where $n$ is the number of variables.
1. **Identify the variables:** The problem states there are 3 variables ($n = 3$).
2. **Apply the formula:** Calculate $2^3$.
3. **Calculate:** $2 \times 2 \times 2 = 8$.
**Answer:**
**8 rows** are required.
### **Question 4**

**4. How many rows are required for a Boolean function with 4 variables?**
### **Solution**
Using the same formula (**$2^n$**):
1. **Identify the variables:** The problem states there are 4 variables ($n = 4$).
2. **Apply the formula:** Calculate $2^4$.
3. **Calculate:** $2 \times 2 \times 2 \times 2 = 16$.
**Answer:**
**16 rows** are required.

### **Question 5**

**5. What is the value of $p + p'$ ?**
### **Solution for 5**
The value is **1**.
**Explanation:**
This is defined by the Boolean **Complement Law** for the OR operation ($+$). A variable ORed with its complement (inverse) will always evaluate to 1 (True).
- If $p = 1$, then $p' = 0$, and $1 + 0 = 1$.
- If $p = 0$, then $p' = 1$, and $0 + 1 = 1$.
### **Question 6**

**6. What is the value of $p \cdot p'$ ?**
### **Solution for 6**
The value is **0**.
**Explanation:**
This is defined by the Boolean **Complement Law** for the AND operation ($\cdot$). A variable ANDed with its complement will always evaluate to 0 (False), because a variable and its inverse can never both be true simultaneously.
- If $p = 1$, then $p' = 0$, and $1 \cdot 0 = 0$.
- If $p = 0$, then $p' = 1$, and $0 \cdot 1 = 0$.

### **Question**

**7. When are two circuits said to be equivalent?**
### **Solution**
Two logical circuits are said to be equivalent if they produce the **exact same output for every possible combination of inputs**.
In practical terms, this means:
- They have perfectly identical **truth tables**.
- The Boolean expressions representing the two circuits are logically equivalent (one can be simplified or manipulated to equal the other using the laws of Boolean algebra).
- They perform the exact same overall logical function, even if they are constructed using a completely different arrangement or number of logic gates.

### **Question**

**8. A Karnaugh map for three variables contains how many cells?**
### **Solution**

To determine the number of cells in a Karnaugh map (K-map), you use the same formula used to find the number of rows in a truth table: **$2^n$**, where $n$ is the number of variables.

1. **Identify the variables:** The problem states there are 3 variables ($n = 3$).
2. **Apply the formula:** Calculate $2^3$.
3. **Calculate:** $2 \times 2 \times 2 = 8$.
**Answer:**
A Karnaugh map for three variables contains **8 cells**.

### **Question**

**9. If a function is 1 for input combinations 001, 010, and 100, how many terms does the SOP form contains?**
### **Solution**
The SOP (Sum of Products) form contains **3 terms**.
**Explanation:**
In a standard (canonical) Sum of Products expression, every input combination that produces an output of 1 corresponds to exactly one product term, which is called a _minterm_.

Since the problem explicitly lists three input combinations (001, 010, and 100) that result in a 1, the unsimplified SOP expression will be the sum of exactly 3 product terms.

**Example for context:**

If your three variables are $A$, $B$, and $C$, the specific terms would be constructed by taking the complement (NOT) of the variable if its value is 0, and the variable itself if its value is 1:
- **001** $\rightarrow$ $A'B'C$
- **010** $\rightarrow$ $A'BC'$
- **100** $\rightarrow$ $AB'C'$
The final SOP expression would be:
$$A'B'C + A'BC' + AB'C'$$

### **Section B**
### **Truth Table Data**

![[Pasted image 20260421074127.png]]

For reference, based on the image provided, here are the minterms (where $F=1$) and maxterms (where $F=0$):

- **Minterms ($F=1$):** 001 ($m_1$), 011 ($m_3$), 100 ($m_4$), 101 ($m_5$), 111 ($m_7$)
- **Maxterms ($F=0$):** 000 ($M_0$), 010 ($M_2$), 110 ($M_6$)

### **Question 10**

**10. Given the truth table above, construct the Karnaugh map and determine the simplest SOP form.**

**Solution:**

First, let's map the outputs ($F$) onto a 3-variable Karnaugh map. The columns represent variables $B$ and $C$, and the rows represent variable $A$. Note the Gray code ordering of the columns (00, 01, 11, 10).

|**A \ BC**|**00**|**01**|**11**|**10**|
|---|---|---|---|---|
|**0**|0|**1**|**1**|0|
|**1**|**1**|**1**|**1**|0|

To find the simplest Sum of Products (SOP), we group the adjacent 1s in powers of 2 (1, 2, 4, 8):

1. **Group 1 (Red/Size 4):** There is a block of four 1s covering columns 01 and 11 (cells $m_1, m_3, m_5, m_7$). In this block, $A$ changes (0 to 1) and $B$ changes (0 to 1), so they drop out. $C$ remains constant at 1.
    - Term = **$C$**

2. **Group 2 (Blue/Size 2):** There is a pair of 1s in row 1, columns 00 and 01 (cells $m_4, m_5$). In this pair, $C$ changes (0 to 1) and drops out. $A$ remains 1, and $B$ remains 0.
    - Term = **$AB'$**

Combining these terms gives the simplest SOP expression:
**$F = C + AB'$**

### **Question 11**

**11. How many cells does the Karnaugh map contain?**

**Solution:**

The number of cells is $2^n$, where $n$ is the number of variables. Since there are 3 variables ($A, B, C$):
$2^3 = 2 \times 2 \times 2 = 8$
The Karnaugh map contains **8 cells**.

### **Question 12**

**12. Determine the simplest POS form.**

**Solution:**

To find the simplest Product of Sums (POS), we group the 0s on the Karnaugh map instead of the 1s.

|**A \ BC**|**00**|**01**|**11**|**10**|
|---|---|---|---|---|
|**0**|**0**|1|1|**0**|
|**1**|1|1|1|**0**|

We group the 0s:

1. **Group 1 (Size 2):** Cells $m_0$ and $m_2$ (row 0, columns 00 and 10). Because K-maps wrap around, these are adjacent. $A$ is 0, $C$ is 0, and $B$ changes. For POS, a 0 is the uncomplemented variable and 1 is the complemented variable.
    - Term = **$(A + C)$**
2. **Group 2 (Size 2):** Cells $m_2$ and $m_6$ (rows 0 and 1, column 10). $B$ is 1, $C$ is 0, and $A$ changes.
    - Term = **$(B' + C)$**

Combining these terms as a product gives the simplest POS expression:

**$F = (A + C)(B' + C)$**

### **Question 13**

**13. Formulate a logic function that fulfills the truth table using minterms (SOP-form).**

**Solution:**

This asks for the _canonical_ (unsimplified) Sum of Products. We create a product term for every row where $F=1$, using the variable if it's 1 and its complement if it's 0, then sum them together.

- Row 001 $\rightarrow A'B'C$
- Row 011 $\rightarrow A'BC$
- Row 100 $\rightarrow AB'C'$
- Row 101 $\rightarrow AB'C$
- Row 111 $\rightarrow ABC$

**$F = A'B'C + A'BC + AB'C' + AB'C + ABC$**

### **Question 14**

**14. Formulate a logic function that fulfills the truth table using maxterms (POS-form).**

**Solution:**

This asks for the _canonical_ (unsimplified) Product of Sums. We create a sum term for every row where $F=0$, using the variable if it's 0 and its complement if it's 1, then multiply them together.

- Row 000 $\rightarrow (A + B + C)$
- Row 010 $\rightarrow (A + B' + C)$
- Row 110 $\rightarrow (A' + B' + C)$

**$F = (A + B + C)(A + B' + C)(A' + B' + C)$**

### **Section C**

Finnish company Fazer produces popular Domino-cookies in their factory. The cookies are made on a machine that fills the space between cookie halves with vanilla filling, presses the halves together and wraps ready cookies in plastic wrap for packaging purposes. The machine is used by two operators.

Operator 1 is allowed to have a coffee break a) when the machine has plastic wrap but no cookie halves or b) when the machine has cookie halves but no vanilla filling.

Operator 2 is allowed to have a coffee break a) when the machine has plastic wrap but no vanilla filling, or b) when the machine has vanilla filling but no cookie halves.

Both operators know their right very well and never miss a coffee break when they are allowed to have one. The factory manager wants to have his room equipped with an indicator light which lits up every time when both operators are having a coffee break at the same time.

Use variables:
- c = cookie halves available
- p = plastic wrap available
- v = vanilla filling available
- 
_(Note: In Boolean logic, a prime symbol ($'$) denotes NOT. So, $c'$ means "no cookie halves", $p'$ means "no plastic wrap", etc.)_

### **Question 15**

**15. Write the logical expression for when operator 1 can take a break**

**Solution:**

a) the machine has plastic wrap ($p$) AND no cookie halves ($c'$). This is written as **$p \cdot c'$**.

OR

b) the machine has cookie halves ($c$) AND no vanilla filling ($v'$). This is written as **$c \cdot v'$**.

Combining these with an OR ($+$) gives the expression:

**Answer:** $O_1 = p \cdot c' + c \cdot v'$

### **Question 16**

**16. Write the logic expression for operator 2 break condition**

**Solution:**

a) the machine has plastic wrap ($p$) AND no vanilla filling ($v'$). This is written as **$p \cdot v'$**.

OR

b) the machine has vanilla filling ($v$) AND no cookie halves ($c'$). This is written as **$v \cdot c'$**.

Combining these with an OR ($+$) gives the expression:

**Answer:** $O_2 = p \cdot v' + v \cdot c'$

### **Question 17**

**17. When will the manager's indicator light turn on?**

**Solution:**

The manager's light turns on "every time when both operators are having a coffee break at the same time." This requires a logical AND ($\cdot$) between Operator 1's condition and Operator 2's condition.

Substitute the expressions found in Q15 and Q16:

**Answer:** $L = (p \cdot c' + c \cdot v') \cdot (p \cdot v' + v \cdot c')$

### **Question 18**

**18. Write the simplest form of when will the manager's indicator light turn on?**

**Solution:**

To find the simplest form, we need to multiply out (distribute) the expression from Q17 and apply the laws of Boolean algebra.

**Step 1: Start with the unsimplified expression.**

$L = (pc' + cv')(pv' + vc')$

**Step 2: Distribute (FOIL method).**

$L = (pc')(pv') + (pc')(vc') + (cv')(pv') + (cv')(vc')$

**Step 3: Simplify each term.**

- _Term 1:_ $p \cdot c' \cdot p \cdot v' \rightarrow$ Since $p \cdot p = p$ (Idempotent Law), this simplifies to **$pc'v'$**.

- _Term 2:_ $p \cdot c' \cdot v \cdot c' \rightarrow$ Since $c' \cdot c' = c'$, this simplifies to **$pc'v$**.

- _Term 3:_ $c \cdot v' \cdot p \cdot v' \rightarrow$ Since $v' \cdot v' = v'$, this simplifies to **$pcv'$**.

- _Term 4:_ $c \cdot v' \cdot v \cdot c' \rightarrow$ Since $v \cdot v' = 0$ and $c \cdot c' = 0$ (Complement Law), this term is **$0$**.

Now rewrite the equation:

$L = pc'v' + pc'v + pcv'$

**Step 4: Factor and simplify.**

Factor out $pc'$ from the first two terms:

$L = pc'(v' + v) + pcv'$

Since a variable ORed with its complement is 1 ($v' + v = 1$), the first part becomes $pc'(1)$, or just $pc'$:

$L = pc' + pcv'$

Factor out $p$ from both remaining terms:

$L = p(c' + cv')$

Apply the Redundancy Law (also known as the absorption law variant $X' + XY = X' + Y$):

$L = p(c' + v')$

_(Optional: You can also distribute the $p$ back in to write it as $pc' + pv'$. Both are considered simplest forms)._

**Answer:** $L = p(c' + v')$ (or $p \cdot c' + p \cdot v'$)

_(In plain English: The light turns on whenever there is plastic wrap AND they are out of either cookie halves or vanilla filling)._



