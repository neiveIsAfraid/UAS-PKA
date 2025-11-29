## Part 1: The Questions

### Chapter 13: Probabilistic Reasoning

1.  Why is designing a Bayesian network by ordering nodes such that **"causes precede effects"** crucial for achieving a compact and easily specifiable representation?
2.  How does the **Variable Elimination** algorithm utilize the distributive property of multiplication over summation to overcome the exponential time complexity faced by simple enumeration inference?
3.  What is the implication of general probabilistic inference in Bayesian networks being classified as **\#P-hard**?
4.  In approximate inference, how does **Likelihood Weighting** handle the issue of conditioning on evidence, and what is its main efficiency risk when evidence is "downstream"?
5.  Explain the conceptual advantage of using a **Noisy-OR** canonical distribution model over a full CPT when a node has numerous parents ($k>1$).
6.  Why is the **Markov blanket** central to the operation of the **Gibbs sampling** algorithm for approximate inference?
7.  The core semantics of a Bayes net guarantees that the parameters $\theta(x_i | \text{parents}(X_i))$ *are exactly* the conditional probabilities $P(x_i | \text{parents}(X_i))$ implied by the joint distribution. What does this semantic relationship guarantee about the robustness and ease of specification of the model?
8.  How do **Causal Networks**, using the **do-operator**, formally distinguish an external intervention from a mere passive observation within a probability model?
9.  If a knowledge engineer attempts to use a node ordering that places *effects before causes* (a diagnostic model), what potential problem arises in terms of specifying probabilities and the network's compactness?
10. What critical factor determines the time and space complexity of the **Variable Elimination** algorithm, and how is this complexity related to the structure of the network?

### Chapter 14: Probabilistic Reasoning over Time

11. In the context of temporal probabilistic models, why is the **Markov property** essential for ensuring that the model remains computationally tractable over a long sequence of time steps?
12. Contrast the primary objectives of the **Filtering** task ($P(X_t|e_{1:t})$) versus the **Smoothing** task ($P(X_k|e_{1:t})$ for $k<t$) in temporal probabilistic reasoning.
13. Why are **Dynamic Bayesian Networks (DBNs)** necessary for modeling complex, real-world systems compared to **Hidden Markov Models (HMMs)**?
14. If an agent wants to determine the **most likely sequence** of states ($x_{1:t}$) rather than just the most likely state at each individual time step, why is standard smoothing insufficient, necessitating the **Viterbi algorithm**?
15. **Kalman Filters** rely on assuming a **Linear Dynamical System**. What is the key implication of this assumption for how the belief state is represented and updated?
16. In Dynamic Bayesian Networks, why does the accuracy of **Likelihood Weighting** degrade significantly, and how does **Particle Filtering** address this limitation?
17. The DBN representation is said to scale linearly, rather than exponentially, with the number of state variables. How does the **factored representation** of the state achieve this dramatic scaling improvement?
18. What is the importance of assuming **time-homogeneity** in the transition and sensor models for solving temporal reasoning inference tasks?
19. Explain how the **Particle Filtering** update cycle—specifically, the **resampling** step—ensures that the set of samples remains focused on high-probability regions of the state space.
20. In what way can a DBN model be used to distinguish between a *transient sensor failure* (a temporary glitch) and a *persistent sensor failure* (a permanent change in reliability)?

[This is the answers](https://github.com/neiveIsAfraid/UAS-PKA/blob/main/W12%20Bayesian%20Reasoning%20%7C%20Short%20Questions%20Answer%20%7B1%7D.md)
