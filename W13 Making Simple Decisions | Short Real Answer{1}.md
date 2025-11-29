## Part 2: Model Answers

1.  **Why must a rational agent adhere to the Maximization of Expected Utility (MEU) principle, rather than relying solely on logical goal attainment, when operating in uncertain environments?**
    MEU provides a continuous range of values for states (utility), allowing the agent to choose the best action outcome by balancing the likelihood (probability theory) against the importance (utility) of achieving various uncertain goals. A logical agent, limited by a binary goal/non-goal distinction, lacks a formal way to decide rationally under uncertainty.

2.  **What is the fundamental implication of satisfying the axioms of utility theory (like transitivity and continuity) for an agent's preferences?**
    Satisfying these axioms ensures that the agent's preferences can be represented by a **utility function**. This further establishes that any rational agent must behave as if it is maximizing the expected value of this utility function.

3.  **How does a Decision Network or Influence Diagram integrate probabilistic reasoning with utility theory to solve a decision problem?**
    Decision networks combine Bayesian networks (chance nodes) with **decision nodes** (actions) and **utility nodes** (preferences). The decision problem is solved by calculating the **expected utility** for each possible action, treating the selected decision node value like evidence in the network, and choosing the action that maximizes this value.

4.  **Explain the utility of stochastic dominance in multiattribute decision-making, particularly in scenarios where the exact utility function is unknown.**
    Stochastic dominance allows an agent to discard one uncertain option if another is statistically superior across their cumulative probability distributions, regardless of the agent's precise utility function. This is useful for narrowing down the field of choices when only partial or qualitative utility information is available.

5.  **What is the critical implication of the theorem stating that the Expected Value of Information (VPI) is always non-negative?**
    This non-negativity property means that information has a positive expected value. The critical implication is that a rational agent should always be willing to gather information if the cost is zero, as VPI measures the maximum expected gain in utility from having the information before acting.

6.  **How does a rational agent decide whether to perform an information-gathering action, such as a medical test, when considering VPI alongside the cost of obtaining the information?**
    The agent uses a myopic approach, selecting the observation $E_j$ that maximizes the ratio of expected utility gain per unit cost, $\text{VPI}(E_j) / C(E_j)$. Information gathering stops if the VPI of the next observation is less than its cost, $C(E_j)$.

7.  **What is the significance of the observation that humans are "predictably irrational," in contrast to the normative theory of expected utility?**
    The term highlights that human behavior frequently deviates from the expectations set by **normative theory** (how a rational agent *should* act). This suggests that factors like problem framing, rather than just objective utility and probability, can influence human choices.

8.  **Why is decomposing a multiattribute utility function into an additive value function often highly desirable, even if the strict independence assumption is sometimes violated?**
    An additive value function requires assessing only $n$ one-dimensional utility functions, achieving an exponential reduction in the preference experiments needed. This approximation is often used successfully because violations of multiattribute preference independence (MPI) frequently occur only in attribute ranges that are unlikely in practice.

9.  **In the context of unknown preferences (e.g., a robot interacting with a human), explain why a rational machine might choose to defer to the human or allow itself to be switched off.**
    The incentive to defer arises from the robot's uncertainty about the human's true preferences. By allowing the human to switch it off, the robot receives information about the human's objective, and this expected gain in utility makes deference the rational choice under preference uncertainty.

10. **The VPI of a sequence of observations is order independent. What computational advantage does this property offer to an agent designing an information-gathering strategy?**
    The order independence property means that the total VPI gained from a sequence of sensing actions is the same regardless of the order in which they are performed. This simplifies the problem of calculating the value of a sequence of sensing actions by eliminating the need to search over all possible permutations of observations.
