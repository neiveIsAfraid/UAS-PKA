## Chapter 15: Making Simple Decisions

### Main Objective:
The primary purpose of Chapter 15 is to detail how **utility theory combines with probability theory** to establish a foundation for a **decision-theoretic agent** capable of making rational decisions in uncertain environments. The chapter centres on the **maximization of expected utility (MEU)** principle, defining the best action as the one that yields the highest expected outcome, balancing likelihood against the importance of various goals,,.

### Key Arguments:
*   **Rationality through Expected Utility:** The MEU principle serves as the definition of rationality in uncertain contexts, replacing the logical agent's binary distinction between good (goal) and bad states with a **continuous range of values (utility)**,. A rational agent chooses the action that maximizes the expected utility of the action outcomes.
*   **The Basis of Utility Theory:** The MEU principle can be derived from a set of constraints (axioms of utility theory, such as orderability, transitivity, continuity, substitutability, monotonicity, and decomposability) that a rational agent's preferences must satisfy,. These constraints establish that any rational agent must behave as if it is maximizing the expected value of a utility function.
*   **Decision Networks as Implementation:** Decision networks (also known as **influence diagrams**) provide a structural framework for implementing decision-theoretic agents by extending Bayesian networks to include action and utility nodes,. The optimal decision is found by evaluating the network for each possible action and returning the one with the highest calculated utility,.
*   **Multiattribute Utility and Dominance:** When outcomes are characterized by multiple attributes (e.g., safety, cost), multiattribute utility theory applies. It introduces **strict dominance** (one option is superior on all attributes) and **stochastic dominance** (one option's outcome is probabilistically superior, even if the expected values are similar) to narrow down choices,.
*   **The Value of Information (VPI):** A rational agent must choose not only actions that change the world but also actions that modify future percepts (information gathering),. **Information value theory** allows the agent to calculate the **Expected Value of Information (VPI)**, which is defined as the difference between the expected utility of the best action *with* the new evidence and the expected utility of the best action *without* it. VPI is always non-negative.
*   **Unknown Preferences and Deference:** Uncertainty about an agent's or a human's true preferences can be modelled by introducing random variables,,. This uncertainty is significant, especially in human-machine interaction, and can lead to the machine choosing to **defer to the human** or allow itself to be switched off if it is uncertain about the human objective,.

### Core Concepts:
*   **Utility Function (U(s)):** A numerical assignment representing the desirability of a state.
*   **Lottery:** A set of possible outcomes for an action, reflecting uncertainty about the result.
*   **Expected Utility (EU(a)):** The utility the agent expects to derive, on average, given the probabilities and utilities of each outcome,.
*   **Decision Network (Influence Diagram):** A graphical model combining chance nodes (ovals), **decision nodes** (rectangles, representing choices), and **utility nodes** (diamonds, representing the utility function) to structure a decision problem,,.
*   **Stochastic Dominance:** A preference relation where one uncertain option is demonstrably better than another, regardless of the specific utility function, based on their cumulative probability distributions,.
*   **Value of Information (VPI):** The maximum amount an agent should be willing to pay for information, calculated as the expected gain in utility resulting from having the information before acting,.
*   **Myopic Information Gathering:** An agent design (often approximate) that selects the observation with the highest utility gain per unit cost, stopping when the expected benefit no longer exceeds the cost.

### Evidence/Examples:
*   **Airline Meals:** Used to illustrate that actions involve uncertainty about outcomes, modelling options like "pasta" or "chicken" as a **lottery**.
*   **Airport Siting Problem:** Used extensively to model decisions with multiple conflicting objectives (e.g., minimizing cost, maximizing safety and quietness),,. This scenario is used to demonstrate Multiattribute Utility and Decision Networks,.
*   **Oil Company Survey:** A specific scenario demonstrating the calculation of the **Expected Value of Information (VPI)**, where an oil company considers paying a seismologist for information on an oil block's contents.
*   **Human Irrationality:** The chapter notes that human behavior often deviates from the **normative theory** of expected utility, citing experimental evidence that humans are "predictably irrational".
*   **The Off-Switch Game (Robbie and Harriet):** A scenario involving a robot (Robbie) and a human (Harriet) where the robot is uncertain about Harriet's preferences. This illustrates the condition under which the robot will choose to **defer** or allow itself to be switched off.

### Conclusion:
Decision theory provides the essential link between an agent's **beliefs (probabilities)** and **desires (utilities)**, establishing a framework for **rational action** that accounts for uncertainty and conflicting goals,. By designing agents to maximize expected utility, the global objective of maximizing performance measure over time can be transformed into a local constraint for guiding action selection step-by-step. This framework enables agents to make informed choices, including deciding the value of acquiring new information.
