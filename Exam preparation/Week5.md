### **Q1**

Let R1 and R2 be relations on the set {1,2,3,4}.

R1 = {(1,3),(2,1),(2,4),(3,2)}

R2 = {(1,2),(2,3),(3,1),(4,4)}

Find:

1. R1 $\cup$ R2
    
2. R1 $\cap$ R2
    
3. R1 $\circ$ R2
    

Present your answers as relation matrices.

---

### **Solution**

First, let's represent the relations $R1$ and $R2$ as relation matrices ($M_{R1}$ and $M_{R2}$).

For a set with 4 elements, the relation matrix is a $4 \times 4$ matrix where the entry in row $i$, column $j$ is **$1$** if $(i,j)$ is in the relation, and **$0$** otherwise.

**Matrix for R1 ($M_{R1}$):**

- (1,3) $\rightarrow$ row 1, col 3 is 1
    
- (2,1) $\rightarrow$ row 2, col 1 is 1
    
- (2,4) $\rightarrow$ row 2, col 4 is 1
    
- (3,2) $\rightarrow$ row 3, col 2 is 1
    
    $$M_{R1} = \begin{pmatrix} 0 & 0 & 1 & 0 \\ 1 & 0 & 0 & 1 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}$$
    

**Matrix for R2 ($M_{R2}$):**

- (1,2) $\rightarrow$ row 1, col 2 is 1
    
- (2,3) $\rightarrow$ row 2, col 3 is 1
    
- (3,1) $\rightarrow$ row 3, col 1 is 1
    
- (4,4) $\rightarrow$ row 4, col 4 is 1
    
    $$M_{R2} = \begin{pmatrix} 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}$$
    

#### **1) R1 $\cup$ R2 (Union)**

To find the matrix for the union, perform a **logical OR** (Boolean addition) on corresponding elements of the two matrices ($1 \lor 0 = 1$, $1 \lor 1 = 1$, $0 \lor 0 = 0$).

$$M_{R1 \cup R2} = M_{R1} \lor M_{R2} = \begin{pmatrix} 0\lor0 & 0\lor1 & 1\lor0 & 0\lor0 \\ 1\lor0 & 0\lor0 & 0\lor1 & 1\lor0 \\ 0\lor1 & 1\lor0 & 0\lor0 & 0\lor0 \\ 0\lor0 & 0\lor0 & 0\lor0 & 0\lor1 \end{pmatrix}$$

**Answer 1:**

$$M_{R1 \cup R2} = \begin{pmatrix} 0 & 1 & 1 & 0 \\ 1 & 0 & 1 & 1 \\ 1 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}$$

#### **2) R1 $\cap$ R2 (Intersection)**

To find the matrix for the intersection, perform a **logical AND** (element-wise multiplication) on corresponding elements ($1 \land 1 = 1$, everything else is $0$). Since $R1$ and $R2$ share no common pairs, the resulting matrix will be all zeros.

$$M_{R1 \cap R2} = M_{R1} \land M_{R2} = \begin{pmatrix} 0\land0 & 0\land1 & 1\land0 & 0\land0 \\ 1\land0 & 0\land0 & 0\land1 & 1\land0 \\ 0\land1 & 1\land0 & 0\land0 & 0\land0 \\ 0\land0 & 0\land0 & 0\land0 & 0\land1 \end{pmatrix}$$

**Answer 2:**

$$M_{R1 \cap R2} = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}$$

#### **3) R1 $\circ$ R2 (Composition)**

_(Note: Assuming the standard discrete math convention where $R1 \circ R2$ means applying relation R1 first, followed by R2. If your specific class uses the reverse function-composition notation, the matrices would be multiplied in reverse order)._

To find the matrix for the composition $R1 \circ R2$, perform a **Boolean matrix multiplication** ($M_{R1} \odot M_{R2}$). This is like standard matrix multiplication, but you use logical AND instead of multiplication, and logical OR instead of addition.

Let's calculate the rows by dotting the rows of $M_{R1}$ with the columns of $M_{R2}$:

- **Row 1:** (0, 0, 1, 0) dots with columns of $M_{R2}$. It only hits the $1$ in column 1. Result: (1, 0, 0, 0)
    
- **Row 2:** (1, 0, 0, 1) dots with columns of $M_{R2}$. It hits the $1$ in column 2 and the $1$ in column 4. Result: (0, 1, 0, 1)
    
- **Row 3:** (0, 1, 0, 0) dots with columns of $M_{R2}$. It hits the $1$ in column 3. Result: (0, 0, 1, 0)
    
- **Row 4:** (0, 0, 0, 0) dots with columns of $M_{R2}$. Result: (0, 0, 0, 0)
    

**Answer 3:**

$$M_{R1 \circ R2} = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}$$
### **Q2**

Define the ordered pairs of the following relations.

1). Let's define relation R in set {1,2,3,4} in following fashion: $(x, y) \in R$ if $x^2 \ge y$

2). Let R be a relation on {1,2,3,4} defined by each of the following:

i. $(x,y) \in R$ if $x+y$ is even

ii. $(x,y) \in R$ if $x \cdot y \le 6$

Define the ordered pairs of this relations

---

### **Solutions**

For all problems, the set we are working with is $A = \{1, 2, 3, 4\}$. This means that both $x$ and $y$ must be chosen from the numbers 1, 2, 3, or 4.

#### **1) Relation R where $x^2 \ge y$**

To find the ordered pairs, we test each possible value of $x$ from the set and see which values of $y$ from the set satisfy the condition.

- **If $x = 1$:** $1^2 = 1$. The condition is $1 \ge y$. The only $y$ from the set that satisfies this is $1$.
    
    - Pairs: $(1, 1)$
        
- **If $x = 2$:** $2^2 = 4$. The condition is $4 \ge y$. The values of $y$ from the set that satisfy this are $1, 2, 3,$ and $4$.
    
    - Pairs: $(2, 1), (2, 2), (2, 3), (2, 4)$
        
- **If $x = 3$:** $3^2 = 9$. The condition is $9 \ge y$. All values of $y$ from the set ($1, 2, 3, 4$) satisfy this.
    
    - Pairs: $(3, 1), (3, 2), (3, 3), (3, 4)$
        
- **If $x = 4$:** $4^2 = 16$. The condition is $16 \ge y$. All values of $y$ from the set ($1, 2, 3, 4$) satisfy this.
    
    - Pairs: $(4, 1), (4, 2), (4, 3), (4, 4)$
        

**Answer:**

$R = \{(1,1), (2,1), (2,2), (2,3), (2,4), (3,1), (3,2), (3,3), (3,4), (4,1), (4,2), (4,3), (4,4)\}$

---

#### **2) Relation R defined by:**

**i. $(x,y) \in R$ if $x+y$ is even**

The sum of two integers is even if and only if both integers are even, or both integers are odd.

- Odd numbers in our set: $1, 3$
    
- Even numbers in our set: $2, 4$
    

Therefore, we pair the odd numbers with each other, and the even numbers with each other:

- **Odd + Odd:** $(1, 1), (1, 3), (3, 1), (3, 3)$
    
- **Even + Even:** $(2, 2), (2, 4), (4, 2), (4, 4)$
    

**Answer:**

$R = \{(1,1), (1,3), (2,2), (2,4), (3,1), (3,3), (4,2), (4,4)\}$

**ii. $(x,y) \in R$ if $x \cdot y \le 6$**

Again, we test each value of $x$ against the set to see which products are less than or equal to 6.

- **If $x = 1$:** $1 \cdot y \le 6$. True for $y = 1, 2, 3, 4$. (Products are $1, 2, 3, 4$).
    
    - Pairs: $(1, 1), (1, 2), (1, 3), (1, 4)$
        
- **If $x = 2$:** $2 \cdot y \le 6$. True for $y = 1, 2, 3$. (Products are $2, 4, 6$).
    
    - Pairs: $(2, 1), (2, 2), (2, 3)$
        
- **If $x = 3$:** $3 \cdot y \le 6$. True for $y = 1, 2$. (Products are $3, 6$).
    
    - Pairs: $(3, 1), (3, 2)$
        
- **If $x = 4$:** $4 \cdot y \le 6$. True for $y = 1$. (Product is $4$).
    
    - Pairs: $(4, 1)$
        

**Answer:**

$R = \{(1,1), (1,2), (1,3), (1,4), (2,1), (2,2), (2,3), (3,1), (3,2), (4,1)\}$


### **Q3**

For the following questions,

a) Write the reflexive closure of R.

b) Write the transitive closure of R.

c) Write the symmetric closure of R.

Write the result as a set of ordered pairs.

**1.** Let $X = \{0,1,2,3\}$ and $R = \{(0,1), (1,1), (1,2), (2,0), (2,2), (3,0)\}$.

**2.** Let $X = \{0,1,2,3\}$ and $R = \{(0,2),(1,0),(1,1),(2,3),(3,1)\}$.

**3.** Let $X = \{0,1,2,3\}$ and $R = \{(0,0),(0,3),(1,2),(2,1),(3,2)\}$.

---

### **Solutions**

**Definitions Refresher:**

- **Reflexive closure:** Add all missing diagonal pairs $(x,x)$ for every element $x$ in the set $X$.
    
- **Symmetric closure:** For every pair $(x,y)$ in the relation, ensure its reverse $(y,x)$ is also included.
    
- **Transitive closure:** If $(x,y)$ and $(y,z)$ are in the relation, add $(x,z)$. Repeat this until no new pairs can be added (essentially finding all reachable paths).
    

#### **1. Let $X = \{0,1,2,3\}$ and $R = \{(0,1), (1,1), (1,2), (2,0), (2,2), (3,0)\}$**

- **a) Reflexive closure:** We need $(0,0), (1,1), (2,2), (3,3)$. The pairs $(1,1)$ and $(2,2)$ are already in $R$. We add $(0,0)$ and $(3,3)$.
    
    **Answer:** $\{(0,0), (0,1), (1,1), (1,2), (2,0), (2,2), (3,0), (3,3)\}$
    
- **b) Transitive closure:** We trace the paths. $0 \to 1 \to 2 \to 0$ forms a cycle, meaning elements $0, 1,$ and $2$ can all reach each other (and themselves). $3 \to 0$, so $3$ can reach $0$, and through $0$, it can reach $1$ and $2$.
    
    - From $0$ reaches: $1, 2, 0$ $\implies (0,1), (0,2), (0,0)$
        
    - From $1$ reaches: $1, 2, 0$ $\implies (1,1), (1,2), (1,0)$
        
    - From $2$ reaches: $0, 1, 2$ $\implies (2,0), (2,1), (2,2)$
        
    - From $3$ reaches: $0, 1, 2$ $\implies (3,0), (3,1), (3,2)$
        
        **Answer:** $\{(0,0), (0,1), (0,2), (1,0), (1,1), (1,2), (2,0), (2,1), (2,2), (3,0), (3,1), (3,2)\}$
        
- **c) Symmetric closure:**
    
    Add the reverse of every pair: $(1,0)$ for $(0,1)$, $(2,1)$ for $(1,2)$, $(0,2)$ for $(2,0)$, and $(0,3)$ for $(3,0)$.
    
    **Answer:** $\{(0,1), (1,0), (1,1), (1,2), (2,1), (2,0), (0,2), (2,2), (3,0), (0,3)\}$
    

---

#### **2. Let $X = \{0,1,2,3\}$ and $R = \{(0,2),(1,0),(1,1),(2,3),(3,1)\}$**

- **a) Reflexive closure:**
    
    We need to add $(0,0), (2,2), (3,3)$ since $(1,1)$ is the only reflexive pair currently present.
    
    **Answer:** $\{(0,0), (0,2), (1,0), (1,1), (2,2), (2,3), (3,1), (3,3)\}$
    
- **b) Transitive closure:**
    
    Tracing the paths gives us a continuous cycle encompassing all elements: $1 \to 0 \to 2 \to 3 \to 1$. Because every element can reach every other element in the set (including itself by completing the loop), the transitive closure contains every possible combination of pairs in $X \times X$.
    
    **Answer:** $\{(0,0), (0,1), (0,2), (0,3), (1,0), (1,1), (1,2), (1,3), (2,0), (2,1), (2,2), (2,3), (3,0), (3,1), (3,2), (3,3)\}$
    
- **c) Symmetric closure:**
    
    Add the reverse of every pair.
    
    **Answer:** $\{(0,2), (2,0), (1,0), (0,1), (1,1), (2,3), (3,2), (3,1), (1,3)\}$
    

---

#### **3. Let $X = \{0,1,2,3\}$ and $R = \{(0,0),(0,3),(1,2),(2,1),(3,2)\}$**

- **a) Reflexive closure:**
    
    Add $(1,1), (2,2), (3,3)$ to the existing $(0,0)$.
    
    **Answer:** $\{(0,0), (0,3), (1,1), (1,2), (2,1), (2,2), (3,2), (3,3)\}$
    
- **b) Transitive closure:**
    
    Let's trace the possible chains:
    
    - $1 \leftrightarrows 2$ forms a mini-cycle. Both $1$ and $2$ can reach $\{1, 2\}$.
        
    - $3 \to 2$, and since $2$ reaches $1$, $3$ can reach $\{1, 2\}$.
        
    - $0 \to 3$, and since $3$ reaches $\{1, 2\}$, $0$ can reach $\{0, 1, 2, 3\}$.
        
        Let's map out the final reachable sets:
        
    - From $0$: $\{0, 1, 2, 3\}$ $\implies (0,0), (0,1), (0,2), (0,3)$
        
    - From $1$: $\{1, 2\}$ $\implies (1,1), (1,2)$
        
    - From $2$: $\{1, 2\}$ $\implies (2,1), (2,2)$
        
    - From $3$: $\{1, 2\}$ $\implies (3,1), (3,2)$
        
        **Answer:** $\{(0,0), (0,1), (0,2), (0,3), (1,1), (1,2), (2,1), (2,2), (3,1), (3,2)\}$
        
- **c) Symmetric closure:**
    
    Add the reverse for $(0,3)$, $(1,2)$, and $(3,2)$. Notice $(2,1)$ is already the reverse of $(1,2)$, so they cover each other.
    
    **Answer:** $\{(0,0), (0,3), (3,0), (1,2), (2,1), (3,2), (2,3)\}$

### **Q4**

For the following questions, determine

a). if R reflexive, symmetric, and transitive. Justify your answer.

b). If we extend R to an equivalence relation, what groups (equivalence classes) are formed?

**1. Let $X = \{1,2,3,4,5\}$ and $R = \{(1,1), (2,3), (3,3), (3,4)\}$
**2. Let $X = \{1,2,3,4,5\}$ and $R = \{(1,2),(2,1),(3,4)\}$**
**3. Let $X = \{1,2,3,4,5\}$ and $R = \{(1,1),(2,2),(3,3),(4,4),(5,5),(1,2),(2,1)\}$

---

### **Solutions**

**1. Let $X = \{1,2,3,4,5\}$ and $R = \{(1,1), (2,3), (3,3), (3,4)\}$**

- **a) Properties:**
    
    - **Reflexive:** **No.** For $R$ to be reflexive, every element $x \in X$ must have $(x,x)$ in $R$. This relation is missing $(2,2)$, $(4,4)$, and $(5,5)$.
        
    - **Symmetric:** **No.** For $R$ to be symmetric, if $(x,y) \in R$, then $(y,x)$ must also be in $R$. We have $(2,3) \in R$, but $(3,2) \notin R$. We also have $(3,4) \in R$ but $(4,3) \notin R$.
        
    - **Transitive:** **No.** For $R$ to be transitive, if $(x,y) \in R$ and $(y,z) \in R$, then $(x,z)$ must be in $R$. We have $(2,3) \in R$ and $(3,4) \in R$, but $(2,4) \notin R$.
        
- **b) Equivalence Classes:**
    
    If we extend $R$ to be an equivalence relation, we must add the missing pairs to make it reflexive, symmetric, and transitive.
    
    - Adding symmetry for $(2,3)$ and $(3,4)$ links the elements $2 \leftrightarrow 3$ and $3 \leftrightarrow 4$.
        
    - Adding transitivity connects them all into a single group: $2 \leftrightarrow 3 \leftrightarrow 4$.
        
    - Adding reflexivity ensures isolated elements ($1$ and $5$) relate to themselves.
        
    - **The equivalence classes are:** $\{1\}$, $\{2, 3, 4\}$, and $\{5\}$.
        

---

**2. Let $X = \{1,2,3,4,5\}$ and $R = \{(1,2),(2,1),(3,4)\}$**

- **a) Properties:**
    
    - **Reflexive:** **No.** It is missing $(1,1), (2,2), (3,3), (4,4),$ and $(5,5)$.
        
    - **Symmetric:** **No.** While $(1,2)$ and $(2,1)$ are symmetric to each other, the pair $(3,4) \in R$ does not have its reverse $(4,3) \in R$.
        
    - **Transitive:** **No.** We have $(1,2) \in R$ and $(2,1) \in R$, which would require $(1,1) \in R$ for transitivity. Since $(1,1) \notin R$, it is not transitive.
        
- **b) Equivalence Classes:**
    
    Extending $R$ to an equivalence relation requires:
    
    - Symmetry will add $(4,3)$, creating the link $3 \leftrightarrow 4$.
        
    - The pairs $(1,2)$ and $(2,1)$ already form the link $1 \leftrightarrow 2$.
        
    - Reflexivity will add self-loops to all elements, including the completely isolated $5$.
        
    - **The equivalence classes are:** $\{1, 2\}$, $\{3, 4\}$, and $\{5\}$.
        

---

**3. Let $X = \{1,2,3,4,5\}$ and $R = \{(1,1),(2,2),(3,3),(4,4),(5,5),(1,2),(2,1)\}$**

- **a) Properties:**
    
    - **Reflexive:** **Yes.** Every element in $X$ relates to itself. $(1,1), (2,2), (3,3), (4,4),$ and $(5,5)$ are all present in $R$.
        
    - **Symmetric:** **Yes.** Every pair has its reverse. The pair $(1,2)$ has $(2,1)$, and all the reflexive pairs (like $(3,3)$) are symmetric to themselves.
        
    - **Transitive:** **Yes.** If we check the non-reflexive links: $(1,2)$ and $(2,1)$ are in $R$, and their transitive conclusion $(1,1)$ is also in $R$. Likewise, $(2,1)$ and $(1,2)$ yield $(2,2)$, which is in $R$.
        
- **b) Equivalence Classes:**
    
    Because $R$ is already reflexive, symmetric, and transitive, it is _already_ an equivalence relation. We just need to group the elements that are related to each other.
    
    - $1$ and $2$ relate to each other.
        
    - $3$, $4$, and $5$ only relate to themselves.
        
    - **The equivalence classes are:** $\{1, 2\}$, $\{3\}$, $\{4\}$, and $\{5\}$.

## Question

For the following questions, show if $R$ satisfies reflexivity, antisymmetry, and transitivity. Thus, is it a total, or partial order?

1. Let $X = \{1, 2, 3\}$ and $R = \{(1, 1), (2, 2), (3, 3), (1, 2), (2, 3), (1, 3)\}$
    
2. Let $X = \{1, 2, 3\}$ and $R = \{(1, 1), (2, 2), (3, 3), (1, 2), (2, 1)\}$
    
3. Let $X = \{1, 2, 3\}$ and $R = \{(1, 1), (2, 2), (3, 3), (1, 2)\}$
    

---

## Solutions

### 1. $R = \{(1, 1), (2, 2), (3, 3), (1, 2), (2, 3), (1, 3)\}$

- **Reflexive:** Yes. For every $a \in X$, $(a, a) \in R$. Specifically: $(1, 1), (2, 2), (3, 3)$ are all present.
    
- **Antisymmetric:** Yes. If $(a, b) \in R$ and $(b, a) \in R$, then $a = b$. Here, we have $(1, 2)$ but not $(2, 1)$, $(2, 3)$ but not $(3, 2)$, and $(1, 3)$ but not $(3, 1)$.
    
- **Transitive:** Yes. If $(a, b) \in R$ and $(b, c) \in R$, then $(a, c) \in R$.
    
    - $(1, 2)$ and $(2, 3)$ are in $R$, and $(1, 3)$ is also in $R$.
        
- **Total or Partial?** Since it is reflexive, antisymmetric, and transitive, it is a **Partial Order**. Furthermore, every pair is comparable (e.g., $1 \le 2$, $2 \le 3$, $1 \le 3$). Therefore, it is a **Total Order**.
    

---

### 2. $R = \{(1, 1), (2, 2), (3, 3), (1, 2), (2, 1)\}$

- **Reflexive:** Yes. $(1, 1), (2, 2), (3, 3)$ are all present.
    
- **Antisymmetric:** **No.** For antisymmetry, if $(1, 2) \in R$ and $(2, 1) \in R$, then $1$ must equal $2$. Since $1 \neq 2$, the relation is not antisymmetric.
    
- **Transitive:** Yes. (e.g., $(1, 2)$ and $(2, 1)$ are in $R$, and $(1, 1)$ is in $R$; $(2, 1)$ and $(1, 2)$ are in $R$, and $(2, 2)$ is in $R$).
    
- **Total or Partial?** It is **neither**. Because it fails antisymmetry, it cannot be a partial order or a total order. (This is actually an _Equivalence Relation_).
    

---

### 3. $R = \{(1, 1), (2, 2), (3, 3), (1, 2)\}$

- **Reflexive:** Yes. $(1, 1), (2, 2), (3, 3)$ are all present.
    
- **Antisymmetric:** Yes. The only distinct pair is $(1, 2)$, and $(2, 1)$ is not in the set.
    
- **Transitive:** Yes. There are no chains $(a, b), (b, c)$ that require a third element other than the ones already satisfied by the reflexive pairs.
    
- **Total or Partial?** It is a **Partial Order**. However, it is **not** a total order because the elements $2$ and $3$ (and $1$ and $3$) are not comparable. There is no $(2, 3)$ or $(3, 2)$ in the set.