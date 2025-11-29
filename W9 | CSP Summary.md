**Constraint Satisfaction Problems (Chapter 5)**

### Main Objective

The primary purpose of this chapter is to introduce **Constraint Satisfaction Problems (CSPs)**, a framework that leverages a **factored representation** for states—a set of variables, each with a value—to solve problems more efficiently than traditional atomic state-space search methods. CSP algorithms capitalize on the internal structure of states and constraints to prune large portions of the search space, using general rather than domain-specific heuristics.

### Key Arguments

The chapter outlines the definition of CSPs, mechanisms for inference (constraint propagation), algorithms for finding solutions (search), and methods for exploiting problem structure:

1.  **Defining Constraint Satisfaction Problems (Section 5.1):** A CSP is formally defined by a set of variables ($X$), a set of domains ($D$) specifying allowable values for each variable, and a set of constraints ($C$) that define allowable combinations of values. A **solution** is a consistent, complete assignment of values to all variables. CSPs naturally represent a wide range of problems and allow solvers to quickly prune the search space by identifying combinations that violate constraints.
2.  **Constraint Propagation: Inference in CSPs (Section 5.2):** This topic focuses on enforcing **local consistency** (such as node, arc, and path consistency) throughout the **constraint graph** to eliminate inconsistent values from variable domains. The **AC-3 algorithm** (for arc consistency, or 2-consistency) iteratively revises variable domains until no further inconsistencies can be found or an empty domain signals that no solution exists. Special-purpose inference algorithms are also discussed for handling **global constraints**, such as *Alldiff* and resource constraints.
3.  **Backtracking Search for CSPs (Section 5.3):** Backtracking search is a specialized form of depth-first search that operates on partial assignments. Because CSPs exhibit **commutativity** (the order of actions does not affect the outcome), the search space is significantly reduced by only considering a single variable assignment at each depth level. The core algorithm is enhanced by several **domain-independent heuristics**, including techniques for variable ordering, value ordering, and propagation mechanisms like **forward checking**. Techniques like **backjumping** and constraint learning improve efficiency by allowing the search to retreat more than one step to a relevant point of conflict.
4.  **Local Search for CSPs (Section 5.4):** Local search algorithms, which operate over **complete assignments**, are highly effective for many CSPs. The **min-conflicts heuristic** is introduced, which works by iteratively selecting a conflicted variable and reassigning it the value that results in the minimum number of violated constraints.
5.  **The Structure of Problems (Section 5.5):** The tractability of a CSP is highly dependent on the structure of its constraint graph. If the constraint graph is a **tree** (meaning any two variables are connected by only one path), the CSP can be solved in time linear in the number of variables using **directional arc consistency (DAC)** and a topological sort. More complex graphs can be simplified using **cutset conditioning** (finding a **cycle cutset** $S$ whose removal leaves a tree) or **tree decomposition** (transforming the CSP into a tree of subproblems).

### Core Concepts

*   **Constraint Satisfaction Problem (CSP):** A problem defined by a set of variables ($X$), associated domains ($D$), and a set of constraints ($C$).
*   **Domain:** The set of allowable values for a variable.
*   **Constraint Graph:** A graphical representation where nodes are variables and an edge exists between any two variables that participate in a constraint.
*   **Unary Constraint:** Restricts the value of a single variable.
*   **Binary Constraint:** Relates exactly two variables. A problem with only unary and binary constraints is a **binary CSP**.
*   **Global Constraint:** A constraint involving an arbitrary number of variables, such as *Alldiff* (requiring all variables to have distinct values) or resource constraints (like *Atmost*).
*   **Arc Consistency (2-consistency):** A condition where an arc $(X_i, X_j)$ is consistent if every value in the domain $D_i$ is consistent with some value in $D_j$. The **AC-3** algorithm achieves this.
*   **K-consistency:** A stronger notion of consistency; a CSP is $k$-consistent if a consistent value can always be assigned to any $k^{th}$ variable, given a consistent assignment to $k-1$ variables.
*   **Min-Conflicts Heuristic:** A heuristic used in local search to select a value for a conflicted variable that minimizes the number of violated constraints.
*   **Cycle Cutset:** A subset of CSP variables ($S$) whose removal leaves the constraint graph as a tree.
*   **Tree Width:** A measure of the structural complexity of a graph; CSPs with constraint graphs of bounded tree width are solvable in polynomial time.

### Evidence/Examples

*   **Map Coloring (Australia):** Used to introduce the basic CSP formulation, illustrating variables (states/territories), domains (colors), and constraints (neighbors must have different colors), as well as the **constraint graph**.
*   **Job-Shop Scheduling:** Provides a real-world example where variables represent task start times (integers) and constraints involve precedence and resources.
*   **Cryptarithmetic Puzzles (e.g., TWO + TWO = FOUR):** Used to demonstrate **global constraints** (like *Alldiff* for distinct letters) and n-ary constraints, visualized using a **constraint hypergraph**.
*   **Sudoku:** A popular puzzle used as a detailed case study to show how inference mechanisms like **arc consistency** and checks for *Alldiff* constraints can rapidly reduce the domain size of variables, sometimes solving the problem completely without search.
*   **N-Queens Problem:** Used to illustrate the power of **local search** and the **min-conflicts heuristic**, which can solve problems like the million-queens problem extremely quickly.

### Conclusion

The chapter concludes that CSPs offer a powerful alternative to atomic state-space search by explicitly representing the world using **variable/value pairs**. The effectiveness of CSP solvers relies heavily on integrating **inference techniques** (consistency checking) with search strategies (backtracking or local search) to eliminate inconsistent assignments early. Crucially, the **complexity of solving a CSP is strongly related to the structure of its constraint graph**. Highly structured problems, such as **tree-structured CSPs**, can be solved in linear time, while techniques like **cutset conditioning** and **tree decomposition** allow generalized problems to be transformed for efficient solution based on the smallness of the cycle cutset or the tree width.
