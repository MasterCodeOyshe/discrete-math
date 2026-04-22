## **Question 1: Draw an expression tree for the following expressions.**

### **1. $a - b / ((c + d) * f)$**

The subtraction is the final operation performed.

Plaintext

```
      -
     / \
    a   /
       / \
      b   *
         / \
        +   f
       / \
      c   d
```

---

### **2. $(a + b) / (c + d)$**

The division is the final operation, splitting the two parenthetical sums.

Plaintext

```
      /
     / \
    +   +
   / \ / \
  a  b c  d
```

---

### **3. $(a - b) + c * d$**

The addition connects the result of the subtraction and the multiplication.

Plaintext

```
      +
     / \
    -   *
   / \ / \
  a  b c  d
```

---

### **4. $(a + b) * ((c - d) / (e + f))$**

The multiplication is the root, joining the left sum with the right complex fraction.

Plaintext

```
        *
      /   \
     +     /
    / \   / \
   a   b -   +
        / \ / \
       c  d e  f
```

---

### **5. $(a * (b + c) - d) / (e - f * g)$**

The division is the final operation, separating the large numerator expression from the denominator.

Plaintext

```
           /
        /     \
       -       -
      / \     / \
     * d   e   *
    / \         / \
   a   +       f   g
      / \
     b   c
```

### **Question**

![[Pasted image 20260422052225.png]]

Interpret the expression tree on the right. Which arithmetic expression does this tree represent, and what number do we get if we calculate the expression?

---

### **Solution**

To find the arithmetic expression, we read the tree from the bottom up, grouping the leaves (numbers) with their parent nodes (operators):

**1. Identify the arithmetic expression:**

- **Bottom Left Subtree:** The division operator `/` connects $40$ and $5$, creating the expression $(40 / 5)$.
    
- **Middle Left Subtree:** The multiplication operator `*` connects the result of the division to $3$, creating the expression $((40 / 5) * 3)$.
    
- **Right Subtree:** The subtraction operator `-` connects $8$ and $7$, creating the expression $(8 - 7)$.
    
- **Root:** The addition operator `+` at the very top combines the entire left side and the right side.
    

Putting it all together, the full arithmetic expression is:

**$((40 / 5) * 3) + (8 - 7)$**

**2. Calculate the expression:**

Now, we evaluate the expression step-by-step following the order of operations:

- First, evaluate the division: $40 / 5 = 8$
    
- Next, evaluate the multiplication: $8 * 3 = 24$
    
- Then, evaluate the subtraction on the right side: $8 - 7 = 1$
    
- Finally, add the two results together at the root: $24 + 1 = 25$
    

The final calculated number is **25**.

### **Question**

![[Pasted image 20260422052517.png]]

Define the minimal spanning tree for the weighted graph on the left. Use Prim’s algorithm in matrix form. Also state the total weight.

---

### **Solution**

To find the Minimal Spanning Tree (MST) using Prim's Algorithm in matrix form, we first represent the graph as an adjacency matrix. The rows and columns represent the nodes (A through I), and the values represent the edge weights. If there is no direct edge between two nodes, the value is $\infty$ (represented here by `-`).

**Initial Adjacency Matrix ($M$):**

|   | A  | B  | C  | D  | E  | F  | G  | H  | I  |
|---|----|----|----|----|----|----|----|----|----|
| A | -  | 22 | 9  | 12 | -  | -  | -  | -  | -  |
| B | 22 | -  | 11 | -  | -  | 36 | -  | 34 | -  |
| C | 9  | 11 | -  | 4  | 65 | 42 | -  | -  | -  |
| D | 12 | -  | 4  | -  | 33 | -  | -  | -  | 30 |
| E | -  | -  | 65 | 33 | -  | 18 | 23 | -  | -  |
| F | -  | 36 | 42 | -  | 18 | -  | 39 | 24 | -  |
| G | -  | -  | -  | -  | 23 | 39 | -  | 25 | 21 |
| H | -  | 34 | -  | -  | -  | 24 | 25 | -  | 19 |
| I | -  | -  | -  | 30 | -  | -  | 21 | 19 | -  

#### **Prim's Algorithm Execution (Matrix Form)**

_Rules: Start at an arbitrary node (we will use **A**). In each step, examine the rows of all currently visited nodes. Select the minimum weight from these rows that belongs to a column of an unvisited node. Cross out the column of the newly visited node to prevent cycles._

- **Step 1:** Start at **A**.
    
    - Examine row A. The minimum weight is **9** (column **C**).
        
    - _Action:_ Add edge **(A, C)**. Mark **C** as visited.
        
- **Step 2:** Visited nodes are {A, C}.
    
    - Examine rows A and C. The available minimum is **4** (row C, column **D**).
        
    - _Action:_ Add edge **(C, D)**. Mark **D** as visited.
        
- **Step 3:** Visited nodes are {A, C, D}.
    
    - Examine rows A, C, and D. The available minimum is **11** (row C, column **B**).
        
    - _Action:_ Add edge **(B, C)**. Mark **B** as visited.
        
- **Step 4:** Visited nodes are {A, B, C, D}.
    
    - Examine rows A, B, C, and D. The available minimum to an unvisited node is **30** (row D, column **I**).
        
    - _Action:_ Add edge **(D, I)**. Mark **I** as visited.
        
- **Step 5:** Visited nodes are {A, B, C, D, I}.
    
    - Examine active rows. The available minimum is **19** (row I, column **H**).
        
    - _Action:_ Add edge **(H, I)**. Mark **H** as visited.
        
- **Step 6:** Visited nodes are {A, B, C, D, H, I}.
    
    - Examine active rows. The available minimum is **21** (row I, column **G**).
        
    - _Action:_ Add edge **(G, I)**. Mark **G** as visited.
        
- **Step 7:** Visited nodes are {A, B, C, D, G, H, I}.
    
    - Examine active rows. The available minimum is **23** (row G, column **E**).
        
    - _Action:_ Add edge **(E, G)**. Mark **E** as visited.
        
- **Step 8:** Visited nodes are {A, B, C, D, E, G, H, I}.
    
    - Examine active rows. The only remaining unvisited node is F. The minimum connecting edge is **18** (row E, column **F**).
        
    - _Action:_ Add edge **(E, F)**. Mark **F** as visited.
        

All nodes have now been visited.

#### **Final Answer**

**Edges of the Minimal Spanning Tree:**

- (A, C) = 9
    
- (C, D) = 4
    
- (B, C) = 11
    
- (D, I) = 30
    
- (H, I) = 19
    
- (G, I) = 21
    
- (E, G) = 23
    
- (E, F) = 18
    

**Total Weight:**

$$9 + 4 + 11 + 30 + 19 + 21 + 23 + 18 = 135$$

### **Question**

An investor is thinking whether he/she should make an investment on a new smartphone application. If the investor says ”No” and invests the money in an ETF fund, he/she estimates that this will yield a profit of 40 k€. For the application, he/she sees two options with 50/50 odds: either the app will be moderately popular (10 k€ profit) or really popular (60 k€ profit). There’s one catch: if the application becomes really popular, the investors can think of including micropayments to the application. This change could either bring huge profits (500 k€) with a probability of 30 % but also it could infuriate the users, collapse the user pool and make the whole 100 k€ investment obsolete. On the right there’s an illustration of the decision tree. Analyze what the investor should do based on expected utility hypothesis.

![[Pasted image 20260422053012.png]]

---

### **Solution**

To solve this using the expected utility hypothesis (or Expected Monetary Value, EMV), we analyze the decision tree from right to left, calculating the expected value at each chance node (circles) and choosing the maximum value at each decision node (squares).

**1. Analyze the far right chance node (micropayments decision):**

If the investor reaches the point of deciding on micropayments, they face a gamble:

- 30% chance ($0.3$) of a $500\text{k}$ profit.
    
- 70% chance ($0.7$) of losing the $100\text{k}$ investment (represented as $-100\text{k}$).
    

Expected Value (EV) of this chance node:

$$\text{EV}_{\text{micropayments}} = (0.3 \times 500) + (0.7 \times -100)$$

$$\text{EV}_{\text{micropayments}} = 150 - 70 = 80$$

The expected value here is **$80\text{k}$**.

**2. Analyze the second decision node (whether to add micropayments):**

If the app is really popular, the investor must choose between:

- Doing nothing and taking a guaranteed profit of **$60\text{k}$**.
    
- Adding micropayments, which has an expected value of **$80\text{k}$**.
    

Since $80 > 60$, a rational investor maximizing expected utility will choose to add micropayments. Therefore, the value of this decision node becomes **$80\text{k}$**.

**3. Analyze the first chance node (initial app investment):**

Now we calculate the expected value of investing in the app, knowing that if it's "really popular," the value of that branch is $80\text{k}$ (because the investor will choose the optimal path of adding micropayments).

The gamble is:

- 50% chance ($0.5$) of moderate popularity (profit = **$10\text{k}$**).
    
- 50% chance ($0.5$) of extreme popularity (expected value = **$80\text{k}$**).
    

Expected Value (EV) of the app investment:

$$\text{EV}_{\text{app}} = (0.5 \times 10) + (0.5 \times 80)$$

$$\text{EV}_{\text{app}} = 5 + 40 = 45$$

The expected value of investing in the app is **$45\text{k}$**.

**4. Analyze the initial decision node (App vs. ETF):**

The investor's primary choice is between:

- Investing in the ETF for a guaranteed **$40\text{k}$**.
    
- Investing in the app, which has an expected value of **$45\text{k}$**.
    

**Conclusion:**

Since the expected value of the app investment ($45\text{k}$) is greater than the guaranteed profit from the ETF ($40\text{k}$), **the investor should choose to invest in the smartphone application.**

_Note: This assumes the investor is strictly risk-neutral and only wants to maximize expected monetary value. A risk-averse investor might prefer the guaranteed 40k over the gamble._


### **Question**

1. The Walrus family owns several pieces of real estate, which they rent to customers and naturally gather profits from this. By following the condition and rent levels of other similar properties in the city, the wise family members have reasoned that they have 3 options for the next time window:
    

2. Full renovation. This would cost 1.4 million euros, but it would set the apartments in highest quality class at least for the next 10 years. It happens that the government of the country is considering the location of one bureau to this city. If the city would be chosen, this would bring a lot of well-off tenants to the rent market, so there would be a huge demand for quality apartments: in this case the rent prices could be increased and the apartments would produce 2.5 million euros more revenue in a time span of 10 years. If the bureau will not be located in this town ,the additional revenue would be smaller due to lesser demand – only 800k€. The family estimates that the probability of getting the bureau to the city is approximately 40 %.
    
3. Light renovation of surfaces. This would cost less – only 500 k€, but the revenue would not be increased as much. If the bureau is located in our city, the additional revenue would be one million euros. If the bureau goes to some other city, then the additional revenue will be only 400 k€.
    
4. Make no renovations – just the mandatory upkeep duties. The money spent on up-keeping is gathered from tenants as index rises, so no investments are needed, but there’s no way to get any additional revenue.
    

a) Draw a decision tree of the situation.

b) Perform decision analysis based on expected utility hypothesis. Which option would be the wisest?

---

### **Solution**

First, let's establish the net payoffs (Revenue - Cost) for each branch of the decision in thousands of euros (**k€**) to keep the numbers clean.

- **Bureau locates in city Probability:** 40% (0.4)
    
- **Bureau goes elsewhere Probability:** 60% (0.6)
    

**Net Payoffs:**

- **Full Renovation (Cost: 1400 k€):**
    
    - Bureau (0.4): 2500 - 1400 = **+1100 k€**
        
    - No Bureau (0.6): 800 - 1400 = **-600 k€**
        
- **Light Renovation (Cost: 500 k€):**
    
    - Bureau (0.4): 1000 - 500 = **+500 k€**
        
    - No Bureau (0.6): 400 - 500 = **-100 k€**
        
- **No Renovation (Cost: 0 k€):**
    
    - Bureau/No Bureau: **0 k€**
        

#### **a) Decision Tree**

Here is the textual representation of the decision tree, using the calculated net payoffs:

Plaintext

```
                               /--- Bureau (0.4) -------- Net: +1100 k€
                              /
                  /--- Full --*
                 /            \
                /              \--- No Bureau (0.6) ----- Net: -600 k€
               /
              /                /--- Bureau (0.4) -------- Net: +500 k€
             /                /
[Decision] ------- Light -----*
             \                \
              \                \--- No Bureau (0.6) ----- Net: -100 k€
               \
                \              /--- Bureau (0.4) -------- Net: 0 k€
                 \            /
                  \--- None --*
                              \
                               \--- No Bureau (0.6) ----- Net: 0 k€
```

#### **b) Decision Analysis (Expected Utility Hypothesis)**

Assuming the family is risk-neutral, their Expected Utility is equivalent to the Expected Monetary Value (EMV) of each choice. We calculate this by multiplying the probability of each outcome by its net payoff and summing them together.

**1. EMV for Full Renovation:**

$$EMV_{Full} = (0.4 \times 1100) + (0.6 \times -600)$$

$$EMV_{Full} = 440 - 360 = 80 \text{ k€}$$

**2. EMV for Light Renovation:**

$$EMV_{Light} = (0.4 \times 500) + (0.6 \times -100)$$

$$EMV_{Light} = 200 - 60 = 140 \text{ k€}$$

**3. EMV for No Renovation:**

$$EMV_{None} = (0.4 \times 0) + (0.6 \times 0) = 0 \text{ k€}$$

**Conclusion:**

Comparing the expected utilities ($80\text{ k€}$ vs $140\text{ k€}$ vs $0\text{ k€}$), the **Light Renovation** yields the highest Expected Monetary Value. Therefore, based on the expected utility hypothesis, **Light Renovation is the wisest option.**