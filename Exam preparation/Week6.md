### **Question 1**

Let’s examine the graph. (Note: numbers are edge numbers, not weights.).

![[Pasted image 20260422053930.png]]

1. Define the adjacency matrix
2. Define the Incidence matrix
3. Define the degree matrix
4. Define the Laplace matrix for the graph
---
### **Solution**

First, let's map out the connections from the image to ensure accuracy.

- **Vertices ($V$):** A, B, C, D, E, F
    
- **Edges ($E$):** * **1:** connects A and B

    - **2:** connects A and C
    - **3:** connects A and D
    - **4:** connects A and F
    - **5:** connects B and C
    - **6:** connects B and E
    - **7:** connects C and F
    - **8:** connects D and E
---

#### **1. Adjacency Matrix ($A$)**

This is a square matrix where the rows and columns represent the vertices. A value of `1` indicates an edge exists between the two vertices, and `0` indicates no direct edge.

#### 1. Adjacency Matrix ($A$)

|   | A | B | C | D | E | F |
|---|---|---|---|---|---|---|
| **A** | 0 | 1 | 1 | 1 | 0 | 1 |
| **B** | 1 | 0 | 1 | 0 | 1 | 0 |
| **C** | 1 | 1 | 0 | 0 | 0 | 1 |
| **D** | 1 | 0 | 0 | 0 | 1 | 0 |
| **E** | 0 | 1 | 0 | 1 | 0 | 0 |
| **F** | 1 | 0 | 1 | 0 | 0 | 0 |


---

#### **2. Incidence Matrix ($M$)**

This matrix shows the relationship between vertices (rows) and edges (columns). A value of `1` indicates the vertex is an endpoint of that specific edge, and `0` indicates it is not.
#### 2. Incidence Matrix ($M$)

|   | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|---|---|---|---|---|---|---|---|---|
| **A** | 1 | 1 | 1 | 1 | 0 | 0 | 0 | 0 |
| **B** | 1 | 0 | 0 | 0 | 1 | 1 | 0 | 0 |
| **C** | 0 | 1 | 0 | 0 | 1 | 0 | 1 | 0 |
| **D** | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 1 |
| **E** | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 1 |
| **F** | 0 | 0 | 0 | 1 | 0 | 0 | 1 | 0 |

---

#### **3. Degree Matrix ($D$)**

This is a diagonal matrix where the elements on the main diagonal represent the degree (number of connecting edges) of each vertex. All off-diagonal elements are `0`.

_(Degrees: A=4, B=3, C=3, D=2, E=2, F=2)_
#### 3. Degree Matrix ($D$)

|   | A | B | C | D | E | F |
|---|---|---|---|---|---|---|
| **A** | 4 | 0 | 0 | 0 | 0 | 0 |
| **B** | 0 | 3 | 0 | 0 | 0 | 0 |
| **C** | 0 | 0 | 3 | 0 | 0 | 0 |
| **D** | 0 | 0 | 0 | 2 | 0 | 0 |
| **E** | 0 | 0 | 0 | 0 | 2 | 0 |
| **F** | 0 | 0 | 0 | 0 | 0 | 2 |

---

#### **4. Laplace Matrix ($L$)**

The Laplace matrix is calculated by subtracting the Adjacency matrix from the Degree matrix ($L = D - A$). The main diagonal contains the vertex degrees, and the off-diagonal entries are `-1` if an edge exists, and `0` otherwise.
#### 4. Laplace Matrix ($L$)

|   | A | B | C | D | E | F |
|---|---|---|---|---|---|---|
| **A** | 4 | -1 | -1 | -1 | 0 | -1 |
| **B** | -1 | 3 | -1 | 0 | -1 | 0 |
| **C** | -1 | -1 | 3 | 0 | 0 | -1 |
| **D** | -1 | 0 | 0 | 2 | -1 | 0 |
| **E** | 0 | -1 | 0 | -1 | 2 | 0 |
| **F** | -1 | 0 | -1 | 0 | 0 | 2 |

### **Question 2**

Use the graph in question 1 to answer these set of questions.
![[Pasted image 20260422055027.png]]

1. In how many ways can we travel from node A to node B using exactly three steps?
    
2. In how many ways can we travel from node A to node B using not more than three steps?
    
3. If we start from node C, how many exactly 3-step long path options do we have?

---

First, let's establish the connections (edges) for each node based on the graph, as this will guide our path counting:

- **Node A connects to:** B, C, D, F
    
- **Node B connects to:** A, C, E
    
- **Node C connects to:** A, B, F
    
- **Node D connects to:** A, E
    
- **Node E connects to:** B, D
    
- **Node F connects to:** A, C
    

---

### **1. In how many ways can we travel from node A to node B using exactly three steps?**

**Answer: 8 ways**

**Step-by-step breakdown:**

To find a 3-step path from A to B, the route must look like this: **A → [Node 1] → [Node 2] → B**.

This means [Node 2] _must_ be a direct neighbor of B (which are A, C, or E).

Let's trace all possibilities starting from A's direct neighbors for [Node 1]:

- **If Step 1 is A → B:**
    
    From B, we must go to a neighbor of B, and then back to B.
    
    - A → B → A → B (1)
        
    - A → B → C → B (2)
        
    - A → B → E → B (3)
        
- **If Step 1 is A → C:**
    
    From C, we must step to a node that connects to B. The neighbors of C are A, B, F. Only A connects to B.
    
    - A → C → A → B (4)
        
- **If Step 1 is A → D:**
    
    From D, we must step to a node that connects to B. The neighbors of D are A and E, both of which connect to B.
    
    - A → D → A → B (5)
        
    - A → D → E → B (6)
        
- **If Step 1 is A → F:**
    
    From F, we must step to a node that connects to B. The neighbors of F are A and C, both of which connect to B.
    
    - A → F → A → B (7)
        
    - A → F → C → B (8)
        

### **2. In how many ways can we travel from node A to node B using not more than three steps?**

**Answer: 10 ways**

**Step-by-step breakdown:**

We need to sum all the valid paths that take 1 step, 2 steps, and 3 steps.

- **1-step paths (A → B):** There is exactly **1** direct edge from A to B.
    
- **2-step paths (A → [Node] → B):** The middle node must be connected to both A and B. Looking at our list, Node C is the only node connected to both. So, there is **1** path: A → C → B.
    
- **3-step paths:** As calculated in the previous question, there are **8** paths.
    

Total ways = 1 (1-step) + 1 (2-step) + 8 (3-step) = 10.

### **3. If we start from node C, how many exactly 3-step long path options do we have?**

**Answer: 26 paths**

**Step-by-step breakdown:**

To find all 3-step paths starting from C, a great trick is to use the number of connections (degrees) each node has:

- A has 4 connections
    
- B has 3 connections
    
- C has 3 connections
    
- D has 2 connections
    
- E has 2 connections
    
- F has 2 connections
    

From Node C, our 1st step can go to **A, B, or F**. Let's calculate the subsequent paths for each branch:

- **Path starting C → A:**
    
    From A, you can go to 4 different nodes (B, C, D, F). From _those_ nodes, the number of 3rd step options is just their total number of connections.
    
    - If C → A → B: 3 options for the 3rd step
        
    - If C → A → C: 3 options for the 3rd step
        
    - If C → A → D: 2 options for the 3rd step
        
    - If C → A → F: 2 options for the 3rd step
        
        _(Total for this branch = 3 + 3 + 2 + 2 = 10 paths)_
        
- **Path starting C → B:**
    
    From B, you can go to A, C, or E.
    
    - If C → B → A: 4 options for the 3rd step
        
    - If C → B → C: 3 options for the 3rd step
        
    - If C → B → E: 2 options for the 3rd step
        
        _(Total for this branch = 4 + 3 + 2 = 9 paths)_
        
- **Path starting C → F:**
    
    From F, you can go to A or C.
    
    - If C → F → A: 4 options for the 3rd step
        
    - If C → F → C: 3 options for the 3rd step
        
        _(Total for this branch = 4 + 3 = 7 paths)_
        

Total 3-step paths from C = 10 + 9 + 7 = 26.

### **Question 3**

Let’s examine the graph on the left. (Note: numbers are edge numbers, not weights.)

![[Pasted image 20260422084710.png]]

1. Define the **Adjacency Matrix** ($A$).
2. Define the **Incidence Matrix** ($M$).
3. Define the **Degree Matrix** ($D$).
4. Define the **Laplacian Matrix** ($L$).
---

### 1. Adjacency Matrix ($A$)

For a directed graph, the entry $a_{ij} = 1$ if there is an edge from vertex $i$ to vertex $j$, and $0$ otherwise.
### 1. Adjacency Matrix ($A$)

$$A = \begin{pmatrix} 0 & 1 & 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 & 0 \\ 1 & 1 & 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 & 1 & 0 \end{pmatrix}$$

---

### 2. Incidence Matrix ($M$)

In an incidence matrix for a directed graph, rows represent vertices and columns represent edges.

- $-1$ if the edge leaves the vertex (source).
    
- $1$ if the edge enters the vertex (sink).
    
- $0$ otherwise.
    

_Note: Edges are labeled 1-7 in red._

_(Rows represent vertices 0-5, columns represent edges 1-7)_

$$M = \begin{pmatrix} 0 & 0 & 0 & 1 & 0 & 0 & -1 \\ 0 & 0 & 0 & 0 & -1 & 1 & 1 \\ 0 & 0 & 1 & -1 & 1 & -1 & 0 \\ 0 & 0 & -1 & 0 & 0 & 0 & 0 \\ 1 & -1 & 0 & 0 & 0 & 0 & 0 \\ -1 & 1 & 0 & 0 & 0 & 0 & 0 \end{pmatrix}$$

---

### 3. Degree Matrix ($D$)

For directed graphs, the Degree Matrix usually represents the **Out-Degree** (number of edges leaving a vertex).

$$D = \begin{pmatrix} 1 & 0 & 0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 & 0 & 0 \\ 0 & 0 & 2 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 0 & 1 \end{pmatrix}$$

---

### 4. Laplacian Matrix ($L$)

The Laplacian matrix for a graph is defined as $L = D - A$. It captures the relationship between the degree of the vertices and their connectivity.

$$L = \begin{pmatrix} 1 & -1 & 0 & 0 & 0 & 0 \\ 0 & 1 & -1 & 0 & 0 & 0 \\ -1 & -1 & 2 & 0 & 0 & 0 \\ 0 & 0 & -1 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 & -1 & 1 \end{pmatrix}$$


To find the minimum time in which the construction project can be completed, we need to perform a **Critical Path Analysis**. This involves doing a "forward pass" to calculate the Earliest Start (ES) and Earliest Finish (EF) times for each task.

The minimum project completion time is equal to the length of the **Critical Path**, which is the longest sequence of dependent tasks in the project.

### 1. Forward Pass Analysis

To calculate the times, we use these rules:

- **Earliest Start (ES):** The maximum Earliest Finish (EF) of all immediately preceding tasks. If a task has no predecessors, its ES is 0.
    
- **Earliest Finish (EF):** The Earliest Start (ES) + Task Time.
    

|**Task**|**Time**|**Preceding Tasks**|**Earliest Start (ES)**|**Earliest Finish (EF = ES + Time)**|
|---|---|---|---|---|
|**A**|6|None|0|0 + 6 = **6**|
|**D**|8|None|0|0 + 8 = **8**|
|**H**|9|None|0|0 + 9 = **9**|
|**B**|9|A, D|Max(6, 8) = **8**|8 + 9 = **17**|
|**I**|6|D, H|Max(8, 9) = **9**|9 + 6 = **15**|
|**C**|10|B, I|Max(17, 15) = **17**|17 + 10 = **27**|
|**E**|9|B|17|17 + 9 = **26**|
|**F**|13|I|15|15 + 13 = **28**|
|**G**|5|C, E, F|Max(27, 26, 28) = **28**|28 + 5 = **33**|

---

### 2. Minimum Completion Time

Task G is the final task in the network (all other tasks eventually lead to it). Its Earliest Finish time determines the completion time of the entire project.

- **Minimum Project Time = 33 days**
    

---

### 3. The Critical Path

To verify this and find the bottleneck of the project, we can look at the lengths of the different paths from start to finish. The critical path is the longest path; any delay on this path will delay the entire project.

- Path 1 (A $\rightarrow$ B $\rightarrow$ C $\rightarrow$ G): 6 + 9 + 10 + 5 = **30 days**
    
- Path 2 (A $\rightarrow$ B $\rightarrow$ E $\rightarrow$ G): 6 + 9 + 9 + 5 = **29 days**
    
- Path 3 (D $\rightarrow$ B $\rightarrow$ C $\rightarrow$ G): 8 + 9 + 10 + 5 = **32 days**
    
- Path 4 (D $\rightarrow$ I $\rightarrow$ C $\rightarrow$ G): 8 + 6 + 10 + 5 = **29 days**
    
- Path 5 (D $\rightarrow$ I $\rightarrow$ F $\rightarrow$ G): 8 + 6 + 13 + 5 = **32 days**
    
- Path 6 (H $\rightarrow$ I $\rightarrow$ F $\rightarrow$ G): 9 + 6 + 13 + 5 = **33 days**
    

The sequence **H $\rightarrow$ I $\rightarrow$ F $\rightarrow$ G** takes the longest (33 days). Therefore, it is the critical path.

Show me the visualization