### **Question 1**

Determine whether $p$ is congruent to $q \pmod m$.

1. p = 134, q=88 and m = 6;
    
2. p=1573, q=12850, m=7;
    
3. p=245, q=125, m=10;
    

---

### **Solutions**

**Concept:** Two integers $p$ and $q$ are congruent modulo $m$ (written mathematically as $p \equiv q \pmod m$) if their difference $(p - q)$ is perfectly divisible by $m$. This means the result of $\frac{p - q}{m}$ must be an integer with no remainder. Alternatively, you can check if both numbers have the same remainder when divided by $m$.

**1. $p = 134$, $q = 88$, and $m = 6$**

- **Calculate the difference:** $134 - 88 = 46$
    
- **Check for divisibility:** $\frac{46}{6} = 7$ with a remainder of 4.
    
- **Conclusion:** Since 6 does not evenly divide 46, 134 is **not congruent** to 88 mod 6.
    
    _(Alternative check: $134 \bmod 6 = 2$, and $88 \bmod 6 = 4$. Since $2 \neq 4$, they are not congruent.)_
    

**2. $p = 1573$, $q = 12850$, and $m = 7$**

- **Calculate the difference:** $12850 - 1573 = 11277$ (You can subtract in either direction)
    
- **Check for divisibility:** $\frac{11277}{7} = 1611$ (an exact integer).
    
- **Conclusion:** Since 7 divides the difference evenly, 1573 **is congruent** to 12850 mod 7.
    
    _(Alternative check: $1573 \bmod 7 = 5$, and $12850 \bmod 7 = 5$. Since the remainders match, they are congruent.)_
    

**3. $p = 245$, $q = 125$, and $m = 10$**

- **Calculate the difference:** $245 - 125 = 120$
    
- **Check for divisibility:** $\frac{120}{10} = 12$ (an exact integer).
    
- **Conclusion:** Since 10 divides the difference evenly, 245 **is congruent** to 125 mod 10.
    
    _(Alternative check: Both numbers end in 5, meaning $245 \bmod 10 = 5$ and $125 \bmod 10 = 5$. Since the remainders match, they are congruent.)_

### **Questions 2**

Determine whether the ISBN is valid in the following books;

1. Author: Simo Särkkä
    
    Title: Differential Equations
    
    ISBN: 978-1-316-51008-7
    
2. Author: Benjamin Foreback
    
    Title: Extreme Air Pollution Events in Beijing
    
    ISBN: 978-952-7507-69-8
    
3. Taiwo Adedipe
    
    Atmospheric boundary layer characteristics and their significance in wind energy and urban air quality assesment
    
    978-952-335-981-9 / 978-952-335-982-6
    

---

### **Solutions**

**Concept: How to validate an ISBN-13**

To determine if an ISBN-13 is valid, you multiply each digit by an alternating weight of 1 and 3 (starting with 1). Then, you sum all these products together. If the total sum is a multiple of 10 (i.e., `Sum mod 10 = 0`), the ISBN is valid.

**1. ISBN: 978-1-316-51008-7**

- **Digits:** 9, 7, 8, 1, 3, 1, 6, 5, 1, 0, 0, 8, 7
    
- **Calculation:**
    
    = (9×1) + (7×3) + (8×1) + (1×3) + (3×1) + (1×3) + (6×1) + (5×3) + (1×1) + (0×3) + (0×1) + (8×3) + (7×1)
    
    = 9 + 21 + 8 + 3 + 3 + 3 + 6 + 15 + 1 + 0 + 0 + 24 + 7
    
    = 100
    
- **Result:** 100 is perfectly divisible by 10.
    
- **Conclusion:** This ISBN is **valid**.
    

**2. ISBN: 978-952-7507-69-8**

- **Digits:** 9, 7, 8, 9, 5, 2, 7, 5, 0, 7, 6, 9, 8
    
- **Calculation:**
    
    = (9×1) + (7×3) + (8×1) + (9×3) + (5×1) + (2×3) + (7×1) + (5×3) + (0×1) + (7×3) + (6×1) + (9×3) + (8×1)
    
    = 9 + 21 + 8 + 27 + 5 + 6 + 7 + 15 + 0 + 21 + 6 + 27 + 8
    
    = 160
    
- **Result:** 160 is perfectly divisible by 10.
    
- **Conclusion:** This ISBN is **valid**.
    

**3. First ISBN: 978-952-335-981-9**

- **Digits:** 9, 7, 8, 9, 5, 2, 3, 3, 5, 9, 8, 1, 9
    
- **Calculation:**
    
    = (9×1) + (7×3) + (8×1) + (9×3) + (5×1) + (2×3) + (3×1) + (3×3) + (5×1) + (9×3) + (8×1) + (1×3) + (9×1)
    
    = 9 + 21 + 8 + 27 + 5 + 6 + 3 + 9 + 5 + 27 + 8 + 3 + 9
    
    = 140
    
- **Result:** 140 is perfectly divisible by 10.
    
- **Conclusion:** This ISBN is **valid**.
    

**3. Second ISBN: 978-952-335-982-6**

- **Digits:** 9, 7, 8, 9, 5, 2, 3, 3, 5, 9, 8, 2, 6
    
- **Calculation:**
    
    = (9×1) + (7×3) + (8×1) + (9×3) + (5×1) + (2×3) + (3×1) + (3×3) + (5×1) + (9×3) + (8×1) + (2×3) + (6×1)
    
    = 9 + 21 + 8 + 27 + 5 + 6 + 3 + 9 + 5 + 27 + 8 + 6 + 6
    
    = 140
    
- **Result:** 140 is perfectly divisible by 10.
    
- **Conclusion:** This ISBN is **valid**.

### **Questions 3**

**1. Use the Euclidean algorithm to find the greatest common divisor of m and n.**

**m = 247, n = 117**

**What is gcd(m,n)?**

**Solution:**

The Euclidean algorithm involves repeated division. You divide the larger number by the smaller number, and then replace the larger number with the smaller number and the smaller number with the remainder. You repeat this until the remainder is 0.

- $247 = 117 \times 2 + 13$
    
- $117 = 13 \times 9 + 0$
    

Since the remainder is now 0, the last non-zero remainder is our answer.

**$\text{gcd}(247, 117) = 13$**

---

**2. Use the Euclidean algorithm to find the greatest common divisor of m and n.**

**m = 1479, n = 272**

**What is gcd(m,n)?**

**Solution:**

Apply the same repeated division process:

- $1479 = 272 \times 5 + 119$
    
- $272 = 119 \times 2 + 34$
    
- $119 = 34 \times 3 + 17$
    
- $34 = 17 \times 2 + 0$
    

The last non-zero remainder is 17.

**$\text{gcd}(1479, 272) = 17$**

---

**3. Use the Euclidean algorithm to find the greatest common divisor of m and n.**

**m = 360, n = 84**

**What is gcd(m,n)?**

**Solution:**

Follow the steps of the algorithm:

- $360 = 84 \times 4 + 24$
    
- $84 = 24 \times 3 + 12$
    
- $24 = 12 \times 2 + 0$
    

The last non-zero remainder is 12.

**$\text{gcd}(360, 84) = 12$**

### **Questions 4**

**1. Find out, using gcd, whether the equation $3157x + 656y = 2173$ is solvable in integers x and y. If yes, find one solution.**

**Solution:**

A linear Diophantine equation $ax + by = c$ has an integer solution if and only if $\text{gcd}(a, b)$ divides $c$.

- **Step 1: Find $\text{gcd}(3157, 656)$ using the Euclidean Algorithm.**
    
    $$3157 = 656 \times 4 + 533$$
    
    $$656 = 533 \times 1 + 123$$
    
    $$533 = 123 \times 4 + 41$$
    
    $$123 = 41 \times 3 + 0$$
    
    The last non-zero remainder is 41, so $\text{gcd}(3157, 656) = 41$.
    
- **Step 2: Check for solvability.**
    
    Does 41 divide 2173?
    
    $$2173 \div 41 = 53$$
    
    Yes, since 41 divides 2173 evenly, **the equation is solvable**.
    
- **Step 3: Find a particular solution using the Extended Euclidean Algorithm.**
    
    Work backwards from the Euclidean algorithm steps to express 41 as a linear combination of 3157 and 656:
    
    $$41 = 533 - (123 \times 4)$$
    
    Substitute $123 = 656 - (533 \times 1)$:
    
    $$41 = 533 - 4(656 - 533)$$
    
    $$41 = 5 \times 533 - 4 \times 656$$
    
    Substitute $533 = 3157 - (656 \times 4)$:
    
    $$41 = 5(3157 - 656 \times 4) - 4 \times 656$$
    
    $$41 = 5 \times 3157 - 20 \times 656 - 4 \times 656$$
    
    $$41 = 3157(5) + 656(-24)$$
    
- **Step 4: Scale the solution.**
    
    We have $3157(5) + 656(-24) = 41$. We need the right side to be 2173. Multiply the entire equation by 53 (since $41 \times 53 = 2173$):
    
    $$3157(5 \times 53) + 656(-24 \times 53) = 41 \times 53$$
    
    $$3157(265) + 656(-1272) = 2173$$
    

**Answer:** Yes, it is solvable. One solution is $x = 265, y = -1272$.

---

**2. Find the integer solution for the equation $84x + 30y = 18$,**

**Solution:**

- **Step 1: Find $\text{gcd}(84, 30)$ using the Euclidean Algorithm.**
    
    $$84 = 30 \times 2 + 24$$
    
    $$30 = 24 \times 1 + 6$$
    
    $$24 = 6 \times 4 + 0$$
    
    $\text{gcd}(84, 30) = 6$.
    
- **Step 2: Check for solvability.**
    
    Does 6 divide 18? Yes ($18 \div 6 = 3$). The equation is solvable.
    
- **Step 3: Use the Extended Euclidean Algorithm.**
    
    Express 6 as a combination of 84 and 30:
    
    $$6 = 30 - 24 \times 1$$
    
    Substitute $24 = 84 - 30 \times 2$:
    
    $$6 = 30 - 1(84 - 30 \times 2)$$
    
    $$6 = 30 - 84 + 30 \times 2$$
    
    $$6 = 84(-1) + 30(3)$$
    
- **Step 4: Scale the solution.**
    
    We need the right side to be 18. Multiply the equation by 3 (since $6 \times 3 = 18$):
    
    $$84(-1 \times 3) + 30(3 \times 3) = 6 \times 3$$
    
    $$84(-3) + 30(9) = 18$$
    

**Answer:** One integer solution is $x = -3, y = 9$.

---

**3. Find out, using gcd, whether the equation $56x + 98y = 35$ is solvable in integers x and y.**

**Solution:**

- **Step 1: Find $\text{gcd}(56, 98)$ using the Euclidean Algorithm.**
    
    $$98 = 56 \times 1 + 42$$
    
    $$56 = 42 \times 1 + 14$$
    
    $$42 = 14 \times 3 + 0$$
    
    The last non-zero remainder is 14, so $\text{gcd}(56, 98) = 14$.
    
- **Step 2: Check for solvability.**
    
    Does 14 divide 35?
    
    $$35 \div 14 = 2.5$$
    
    Since 14 does not divide 35 evenly (it does not result in an integer), there are no integer solutions for $x$ and $y$.
    

**Answer:** No, the equation is **not solvable** in integers.

### **Questions 5**

**1. Petri plays Scrabble with his friend from abroad. They have agreed that Petri can formulate Finnish words and his friend can formulate English words. In the end of the game, Petri notices that he’s in a bad situation: he’d have to figure out at least a six-letter word out of his letters RAARALL. Luckily Petri is from the region of Savo, so he is able to invent an explanation for any possible “word” he forms. Considering future games, he anyhow tries to come up with a solution that is as believable as possible, leaving his friend with as little doubt of foul play as possible. How many different “word” options does he have, so that he can evaluate what’s the best?**

**Solution:**

Petri needs to form words of "at least a six-letter word" using the 7 letters in **RAARALL**. This means we need to find the total number of 7-letter combinations AND 6-letter combinations.

- **Count the letters:** We have 3 A's, 2 R's, and 2 L's.
    
- **Case 1: 7-letter words (using all letters)**
    
    The number of unique permutations of a set with repeating items is found by dividing the factorial of the total number of letters by the factorials of the counts of each repeating letter.
    
    $$\frac{7!}{3!2!2!} = \frac{5040}{6 \times 2 \times 2} = \frac{5040}{24} = 210$$
    
    There are 210 possible 7-letter words.
    
- **Case 2: 6-letter words (leaving exactly one letter out)**
    
    To make a 6-letter word, Petri must discard one letter. There are three sub-cases depending on which letter is discarded:
    
    - **Discard one 'A':** He is left with 2 A's, 2 R's, 2 L's.
        
        Permutations: $\frac{6!}{2!2!2!} = \frac{720}{8} = 90$
        
    - **Discard one 'R':** He is left with 3 A's, 1 R, 2 L's.
        
        Permutations: $\frac{6!}{3!1!2!} = \frac{720}{12} = 60$
        
    - **Discard one 'L':** He is left with 3 A's, 2 R's, 1 L.
        
        Permutations: $\frac{6!}{3!2!1!} = \frac{720}{12} = 60$
        
    
    Total 6-letter words = $90 + 60 + 60 = 210$
    
- **Total Word Options:** $210 \text{ (7-letter words)} + 210 \text{ (6-letter words)} = 420$
    

Petri has **420** different "word" options.

---

**2. A player has the letters MISSISSIPPI.**

**How many different 11-letter “words” can be formed using all the letters?**

**Solution:**

We use the same permutation formula for repeating items.

- **Total letters:** 11
    
- **Letter counts:** M (1), I (4), S (4), P (2)
    

Plug these into the formula:

$$\frac{11!}{1!4!4!2!} = \frac{39,916,800}{1 \times 24 \times 24 \times 2} = \frac{39,916,800}{1152} = 34,650$$

There are **34,650** different 11-letter words that can be formed.

---

**3. Anna is playing Scrabble and gets the letters BANANAS. She is allowed to invent words, but they must look realistic, so she decides to use all her letters.**

**How many different 7-letter “words” can she form?**

**Solution:**

Again, use the permutation formula for repeating items since she must use all 7 letters.

- **Total letters:** 7
    
- **Letter counts:** B (1), A (3), N (2), S (1)
    

Plug these into the formula:

$$\frac{7!}{1!3!2!1!} = \frac{5040}{1 \times 6 \times 2 \times 1} = \frac{5040}{12} = 420$$

Anna can form **420** different 7-letter words.