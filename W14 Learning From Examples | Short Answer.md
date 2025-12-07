## Part 2: Answer Key

1.  **What is the implication of the stationarity assumption on the relationship between an agent's historical observations and its predictions for future examples?**
    The stationarity assumption dictates that future examples will be independent and identically distributed (i.i.d.) from the same fixed probability distribution as the past training examples. The implication is that if a hypothesis minimizes loss on the historical training set, it is statistically likely to minimize the loss on unseen future examples drawn from the same distribution.

2.  **How does the principle of Ockham's razor relate to the bias–variance tradeoff when selecting a hypothesis?**
    Ockham's razor recommends choosing the simplest hypothesis that adequately fits the data. This principle guides model selection toward simpler, lower-capacity models (higher bias, lower variance) to reduce the risk of **overfitting** noise, even if a more complex model (lower bias, higher variance) might fit the training data slightly better.

3.  **Why is the Occur Check necessary in the unification algorithm, and what practical consequence results from omitting it in some systems?**
    The Occur Check ensures that a variable being unified with a complex term does not already occur within that term (e.g., preventing $S(x)$ from unifying with $S(S(x))$). Omitting the Occur Check, as is done in some logic programming systems, allows for unsound inferences, although these rarely cause problems in practice.

4.  **Explain how the decision to use L1 regularization rather than L2 regularization impacts the interpretability and robustness of a multivariable linear regression model.**
    L1 regularization minimizes the sum of absolute values of weights, which tends to produce a **sparse model** where many weights are exactly zero. By effectively selecting only the most important attributes and eliminating others, the model becomes simpler, more robust, and easier for a human to interpret.

5.  **What is the practical risk of Likelihood Weighting when evidence variables are "downstream" from sampled variables in a Bayesian network, and what characteristic of the sampling distribution causes this?**
    The risk is that **most samples will have very low, near-zero weights**. This occurs because the initial nonevidence variables are sampled without being guided by the downstream evidence, leading to samples that bear little resemblance to reality (hallucinations), causing inefficiency and error.

6.  **How does the Expected Value of Information (VPI) formally measure the expected benefit of performing an information-gathering action prior to taking a physical action?**
    VPI is defined as the difference between the expected utility of the best action *with* the new evidence and the expected utility of the best action *without* the evidence. VPI must always be non-negative, meaning information has positive expected value, and the agent should acquire it if the expected gain exceeds the cost.

7.  **In decision theory, why is a utility function typically not proportional to monetary value, particularly for significant amounts of wealth?**
    Utility is usually not linearly proportional to monetary value, especially for large amounts of wealth, because an agent's perceived utility is **risk-averse**; the utility derived from each additional unit of wealth diminishes. This is demonstrated by an agent preferring a sure sum (lower Expected Monetary Value) over a gamble (higher EMV).

8.  **Why is forward checking in CSP solving preferred over simple chronological backtracking in terms of avoiding wasteful search effort?**
    Forward checking immediately enforces consistency whenever a variable is assigned, deleting inconsistent values from the domains of neighboring, unassigned variables. This process detects a domain reduction to zero (a failure) much earlier in the search tree, allowing the algorithm to **backtrack immediately** and avoid exploring fruitless branches of the search space.

9.  **Why does the Minimax algorithm for game search perform a depth-first exploration of the entire game tree, leading to exponential time complexity in depth $m$ and branching factor $b$?**
    Minimax must explore the game tree all the way to the terminal states (or the cutoff depth) to determine the exact utility values before backing them up. Since the number of states grows exponentially as $O(b^m)$, and every state must be visited and evaluated, the complexity is $O(b^m)$.

10. **How do Dynamic Bayesian Networks (DBNs), through their factored representation, overcome the state-space scaling issues inherent in Hidden Markov Models (HMMs) for complex sequential systems?**
    HMMs treat the state as a single, atomic entity, leading to exponential scaling of the transition matrix size $O(d^{2n})$ with the number of variables $n$. DBNs use a factored representation, decomposing the state into multiple individual variables, which exploits conditional independence to constrain parameter growth to scale **linearly** as $O(nd^k)$, where $k$ is the maximum number of parents.
