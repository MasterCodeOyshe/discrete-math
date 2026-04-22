### **Question**

**1. Construct the truth table for the expression:**

$\neg p \land q$

### **Solution**

To construct the truth table for $\neg p \land q$ (read as "not $p$ and $q$"), we need to evaluate the expression for all possible true (T) and false (F) combinations of the variables $p$ and $q$.

Here is the step-by-step truth table:

|**p**|**q**|**¬p**|**¬p∧q**|
|---|---|---|---|
|T|T|F|**F**|
|T|F|F|**F**|
|F|T|T|**T**|
|F|F|T|**F**|

**Explanation of the steps:**

- **Columns $p$ and $q$:** List all four possible combinations of True and False for the two variables.
- **Column $\neg p$:** This is the negation of $p$. It simply flips the truth value of $p$ (True becomes False, and False becomes True).
- **Column $\neg p \land q$:** This is the logical AND conjunction. It is only True when _both_ $\neg p$ and $q$ are True (which only happens in the third row).

### **Question**

**2. How many rows are needed for the truth table of $p \lor (q \Rightarrow r)$?**

### **Solution**

To find the number of rows needed for a truth table, you use the formula **$2^n$**, where $n$ is the number of distinct logical variables in the expression.

1. **Identify the variables:** In the expression $p \lor (q \Rightarrow r)$, there are three distinct variables: $p$, $q$, and $r$.
2. **Apply the formula:** Since $n = 3$, calculate $2^3$.
3. **Calculate:** $2 \times 2 \times 2 = 8$.

**Answer:**

**8 rows** are needed for the truth table.

### **Question**

**3. When is the implication $p \Rightarrow q$ FALSE? Create the truth table to show your answer.**

### **Solution**

The implication $p \Rightarrow q$ (read as "if $p$, then $q$") is **FALSE** only in one specific case: **when the hypothesis ($p$) is TRUE, but the conclusion ($q$) is FALSE.** In all other scenarios, the implication is considered true.

Here is the truth table demonstrating this:

|**p (Hypothesis)**|**q (Conclusion)**|**p⇒q (Implication)**|
|---|---|---|
|T|T|T|
|**T**|**F**|**F**|
|F|T|T|
|F|F|T|

As shown in the second row, a true statement cannot imply a false statement.

### **Question**

**4. Which expression using ONLY Peirce's arrow ($\downarrow$) equals $\neg p$?**
A. $p \downarrow p$
B. $p \downarrow q$
C. $(p \downarrow q) \downarrow p$
D. $(p \downarrow p) \downarrow p$

### **Solution**

The correct answer is **A. $p \downarrow p$**.

**Explanation:**

Peirce's arrow ($p \downarrow q$) represents the logical **NOR** operation. By definition, $p \downarrow q$ is equivalent to "neither $p$ nor $q$", which can be written as $\neg(p \lor q)$.

Let's evaluate the first option:

1. Substitute $p$ for both arguments in the Peirce's arrow expression:    $$p \downarrow p$$
2. Apply the definition of the NOR operator:    $$\neg(p \lor p)$$
3. Apply the idempotent law of logic, which states that $p \lor p$ is logically equivalent to just $p$:$$\neg(p)$$
Therefore, $p \downarrow p \equiv \neg p$.

### **Question**

**5. Which expression using ONLY $\downarrow$ equals $p \land q$?**
A. $(p \downarrow q) \downarrow (p \downarrow q)$
B. $p \downarrow p$
C. $p \downarrow (q \downarrow q)$
D. $(p \downarrow p) \downarrow q$

### **Solution**

There appears to be an error in the options provided for this question. Under standard logic definitions, **none of the given options are equivalent to $p \land q$ (logical AND)**.

Here is a breakdown of why, assuming $\downarrow$ represents Peirce's arrow (the logical **NOR** operation, defined as $\neg(p \lor q)$):

**1. The correct expression for $p \land q$:**

To construct an AND operation using only NOR operations, you must invert both inputs before passing them into a third NOR operation.

- By De Morgan's laws: $p \land q \equiv \neg(\neg p \lor \neg q)$
- Applying the NOR definition: $p \land q \equiv (\neg p) \downarrow (\neg q)$
- Substituting $\neg p$ with $p \downarrow p$: **$p \land q \equiv (p \downarrow p) \downarrow (q \downarrow q)$** _(Note: This correct expression is missing from your options)._

**2. Evaluating the given options:**

- **A. $(p \downarrow q) \downarrow (p \downarrow q)$:** This applies the NOT operation to a NOR, which creates an OR. It evaluates to **$p \lor q$**.
- **B. $p \downarrow p$:** As established in the previous question, this evaluates to **$\neg p$**.
- **C. $p \downarrow (q \downarrow q)$:** This evaluates to $p \downarrow (\neg q)$, which simplifies to **$\neg(p \lor \neg q)$**.
- **D. $(p \downarrow p) \downarrow q$:** This evaluates to $(\neg p) \downarrow q$, which simplifies to **$\neg(\neg p \lor q)$**.

**What likely happened:**

It is very common for textbooks or tests to have typos in these specific logic questions. There are two likely scenarios for what the author intended:

1. They meant to ask _"Which expression... equals **$p \lor q$**?"_ (OR). If so, **A** is the correct answer.
2. They confused Peirce's arrow ($\downarrow$, NOR) with the Sheffer stroke ($\uparrow$, NAND). If the symbol was intended to represent NAND, then option **A** would correctly evaluate to $p \land q$.

### **Question**

**6. Assume $p = T$ and $q = T$. Is the proposition $\neg(\neg(p \Rightarrow \neg q) \lor \neg(q \Rightarrow \neg p))$ true or false?**
### **Solution**

To determine the truth value of the proposition, let's substitute the given values and evaluate the expression step-by-step from the inside out.

**Given:**
- $p = \text{T}$
- $q = \text{T}$

This means:
- $\neg p = \text{F}$
- $\neg q = \text{F}$

**Step-by-step evaluation:**

1. **Substitute the values into the original expression:**   $$\neg(\neg(\text{T} \Rightarrow \text{F}) \lor \neg(\text{T} \Rightarrow \text{F}))$$
2. **Evaluate the inner implications ($\Rightarrow$):**
    Recall that an implication ($\text{T} \Rightarrow \text{F}$) is **False**.
    - $(\text{T} \Rightarrow \text{F}) = \text{F}$   
    Substituting this back into the expression gives:
$$\neg(\neg(\text{F}) \lor \neg(\text{F}))$$
3. **Evaluate the inner negations ($\neg$):**
    - $\neg(\text{F}) = \text{T}$
    Substituting this back gives:
$$\neg(\text{T} \lor \text{T})$$
4. **Evaluate the logical OR ($\lor$):**
    - $\text{T} \lor \text{T} = \text{T}$
    Substituting this back gives:
$$\neg(\text{T})$$
5. **Evaluate the final negation:**
    - $\neg(\text{T}) = \text{F}$
**Answer:**
The proposition is **False**.

### **Question**

**7. Let p = "You marry"; r = "You regret it"**
Create the truth table for the expressions below. Which of them is a tautology?
A. $(p \Rightarrow r) \land (\neg p \Rightarrow r)$
B. $(p \Rightarrow r) \lor (\neg p \Rightarrow r)$
C. $(p \Rightarrow r) \land (\neg p \Rightarrow r) \Rightarrow r$
D. $p \Rightarrow r$

### **Solution**

A **tautology** is a logical expression that is always true, regardless of the truth values of its individual variables. To determine which expression is a tautology, we construct a truth table evaluating all four expressions for every possible combination of $p$ and $r$.

Here is the comprehensive truth table:

|**p**|**r**|**¬p**|**p⇒r**|**¬p⇒r**|**A: (p⇒r)∧(¬p⇒r)**|**B: (p⇒r)∨(¬p⇒r)**|**C: A ⇒r**|**D: p⇒r**|
|---|---|---|---|---|---|---|---|---|
|T|T|F|T|T|**T**|**T**|**T**|**T**|
|T|F|F|F|T|**F**|**T**|**T**|**F**|
|F|T|T|T|T|**T**|**T**|**T**|**T**|
|F|F|T|T|F|**F**|**T**|**T**|**T**|

**Explanation of the Results:**
- **A. Not a tautology.** It is false when $r$ is false.
- **B. Tautology.** As seen in the table, Column B is entirely True. Because either $p$ or $\neg p$ must be false in any given scenario, one of the implications will always have a false hypothesis, making that implication inherently true. Thus, their disjunction ($\lor$) is always true.
- **C. Tautology.** Column C is entirely True. This expression represents the logical rule of _Proof by Cases_. If doing something implies a result ($p \Rightarrow r$), AND not doing it also implies the exact same result ($\neg p \Rightarrow r$), then that result ($r$) is inevitable.
- **D. Not a tautology.** This is a standard implication, which is false when the hypothesis is true but the conclusion is false (Row 2).

**Conclusion:**
Based on the truth table, both expressions **B** and **C** are tautologies because their final columns consist exclusively of "True" values. _(Note: Expression C is the classic intended answer for this specific "Proof by Cases" logic puzzle, but Expression B is mathematically a tautology as well due to the rules of material implication)._

### **Question**
**8. If $p$ = fuel in car**

**$q$ = go to store**
**$r$ = buy cookies**
**$(p \Rightarrow q) \land p \Rightarrow q$**
**Which rule is used?**

### **Solution**

The rule used is **Modus Ponens** (also known as the law of detachment).

**Explanation:**

The logical structure given is formally read as: "If $p$ implies $q$, and $p$ is true, then $q$ is true."

In the context of the English phrases provided:

- **Premise 1 ($p \Rightarrow q$):** If there is fuel in the car, then I go to the store.
- **Premise 2 ($p$):** There is fuel in the car.
- **Conclusion ($q$):** Therefore, I go to the store.

This is the classic definition of the Modus Ponens rule of inference. _(Note: The variable $r$ = "buy cookies" is extra information not used in the logical expression)._

### **Question 9**

**Is the statement $\forall x \in \mathbb{Z}^+ : (1 + x)^2 > 1 + 2x$ True or False?**

### **Solution for 9**
The statement is **True**.
**Explanation:**
1. Let's simplify the inequality. Expand the left side of the equation:$$(1 + x)^2 = 1 + 2x + x^2$$
2. Substitute the expanded form back into the original inequality:$$1 + 2x + x^2 > 1 + 2x$$
3. Subtract $(1 + 2x)$ from both sides to isolate $x^2$:$$x^2 > 0$$
4. The domain specifies $\forall x \in \mathbb{Z}^+$, which means "for all $x$ that are positive integers" (i.e., $x \in \{1, 2, 3, \dots\}$).
5. For any positive integer, its square will always be strictly greater than 0. Therefore, the statement holds true for the entire given domain.

### **Question 10**

**Is the statement $\forall x \in \mathbb{R} : (1 + x)^2 > 1 + 2x$ True or False?**
### **Solution for 10**
The statement is **False**.
**Explanation:**
1. Just as in the previous problem, the inequality simplifies to:$$x^2 > 0$$
2. The domain specifies $\forall x \in \mathbb{R}$, which means "for all $x$ that are real numbers".
3. To prove a "for all" ($\forall$) statement false, we only need to find a single counterexample where the condition fails.
4. The number **0** is a real number ($0 \in \mathbb{R}$). If we let $x = 0$, the simplified inequality becomes $0^2 > 0$, or $0 > 0$, which is **false**.
5. Because there is at least one real number where the inequality is not strictly greater than, the universal statement is false.