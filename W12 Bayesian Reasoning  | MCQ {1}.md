## Quiz Section

### Chapter 13: Probabilistic Reasoning

**Question 1**\
What structural property allows a Bayesian network to represent a full joint probability distribution in a concise manner?\
A) It must be a complete graph, ensuring all dependencies are explicit.\
B) It exploits the underlying statistical relationships, specifically conditional independence.\
C) It requires nodes to be ordered alphabetically, simplifying lookup.\
D) It converts all conditional probabilities into standard deviation values.

**Question 2**\
If a node in a Bayesian network represents a Boolean variable and has $k$ Boolean parents, how many independently specifiable probabilities are contained in its Conditional Probability Table (CPT)?\
A) $k$\
B) $k^2$\
C) $2^k$\
D) $2 \times k$

**Question 3**\
Which statement accurately describes the relationship between the conditional probability table (CPT) entries and the conditional probabilities they represent in a Bayesian network?\
A) The CPT entries $\theta(x_i | \text{parents}(X_i))$ are defined only as upper bounds on $P(x_i | \text{parents}(X_i))$.\
B) The parameters $\theta(x_i | \text{parents}(X_i))$ are exactly the conditional probabilities $P(x_i | \text{parents}(X_i))$ implied by the joint distribution.\
C) The CPT entries must sum to $2^k$ where $k$ is the number of parents.\
D) The CPT entries define probabilities only in diagnostic, non-causal models.

**Question 4**\
In general, exact probabilistic inference in Bayesian networks is classified as being harder than NP-complete problems. What is the specific complexity classification cited in the sources?\
A) P-complete\
B) NP-hard\
C) \#P-hard\
D) Logspace-complete

**Question 5**\
When constructing the links of a Bayesian network, the resulting network will generally be more compact if the variables are ordered such that:\
A) Effects precede causes.\
B) Causally independent variables are listed first.\
C) Causes precede effects.\
D) Variables with the largest CPTs are placed last.

**Question 6**\
What is the primary computational task for any probabilistic inference system in a Bayes net, given query variable $X$ and evidence $e$?\
A) Computing the prior probability $P(X)$.\
B) Computing the full joint probability distribution $P(X, E, Y)$.\
C) Computing the maximum likelihood estimate of the hidden variables $Y$.\
D) Computing the posterior probability distribution for $X$, given observed evidence $e$, denoted $P(X | e)$.

**Question 7**\
The Variable Elimination algorithm optimizes exact inference in Bayesian networks by leveraging which mathematical principle to rearrange the summation over the full joint distribution?\
A) Distributing the summations inwards over factors that do not depend on the variable being summed out.\
B) Requiring the network to be a polytree, which simplifies all subsequent matrix multiplications.\
C) Using the product rule to replace all conditional distributions with prior probabilities.\
D) Performing a fixed, top-down enumeration order independent of the network structure.

**Question 8**\
In the context of approximate inference using sampling, how does **rejection sampling** estimate the posterior probability $P(X|e)$?\
A) By generating weighted samples where the weights correspond to the likelihood of the evidence.\
B) By repeatedly sampling new values for variables based on their Markov blanket.\
C) By generating samples from the prior distribution and discarding those that do not match the observed evidence.\
D) By computing the full joint distribution for all variables and selecting samples randomly from it.

**Question 9**\
What is the core difference between the way **Likelihood Weighting** handles evidence variables compared to **Rejection Sampling**?\
A) Likelihood Weighting samples the evidence variables first, whereas Rejection Sampling samples non-evidence variables first.\
B) Likelihood Weighting fixes the values of the evidence variables and weights the sample by their likelihood, whereas Rejection Sampling discards samples inconsistent with the evidence.\
C) Likelihood Weighting only works for discrete variables, whereas Rejection Sampling works for continuous variables.\
D) Likelihood Weighting uses a single best hypothesis, whereas Rejection Sampling uses a distribution over all hypotheses.

**Question 10**\
**Gibbs sampling** is categorized as an instance of what family of statistical algorithms used for approximate inference?\
A) Direct Sampling Methods\
B) Sequential Importance Sampling\
C) Markov Chain Monte Carlo (MCMC) algorithms\
D) Expectation-Maximization (EM) algorithms

**Question 11**\
In Gibbs sampling, when a non-evidence variable $X_i$ is chosen for updating, the new value for $X_i$ is sampled based on the values of the variables in its:\
A) Parent set\
B) Children set\
C) Ancestors set\
D) Markov blanket

**Question 12**\
In the theory of **Causal Networks**, what is the purpose of the **do-operator** (e.g., $do(\text{Sprinkler}=\text{true})$)?\
A) To model passive observation of variables without altering the network structure.\
B) To compute the total probability of an outcome by summing over hidden causes.\
C) To model external intervention by replacing the intervened variable's conditional distribution with a deterministic assignment, effectively deleting incoming links.\
D) To ensure the network remains acyclic during structural learning.

**Question 13**\
Noisy logical relationships, such as **noisy-OR**, help simplify the representation of Conditional Probability Tables (CPTs) by reducing the number of parameters required for a variable with $k$ parents from $O(2^k)$ to approximately what complexity?\
A) $O(k!)$\
B) $O(k)$\
C) $O(2k)$\
D) $O(k \log k)$

**Question 14**\
In the context of probabilistic inference (e.g., computing $P(X | e)$), the set of all random variables in the domain is divided into three components. These components are:\
A) Causal variables, diagnostic variables, and intermediate variables.\
B) Prior variables, posterior variables, and likelihood variables.\
C) Query variables, evidence variables, and hidden (nonevidence, nonquery) variables.\
D) Boolean variables, discrete variables, and continuous variables.

**Question 15**\
The enumeration-ask algorithm (ENUMERATION-ASK) suffers from a severe efficiency problem because the calculation of the posterior probability involves:\
A) Extensive matrix inversion which is computationally expensive.\
B) Repeatedly calculating the same subexpressions within the summation.\
C) Recursively calling the same network structure for every possible permutation of the variables.\
D) Requiring a full set of $0$ and $1$ probabilities in the CPTs, leading to many error checks.

***

### Chapter 14: Probabilistic Reasoning over Time

**Question 16**\
In probabilistic reasoning over time, what is the world state generally modeled using?\
A) A sequence of time slices, each containing state ($X_t$) and evidence ($E_t$) variables.\
B) A continuous function $S(t)$ that tracks all variable changes.\
C) A logical theory consisting of successor-state axioms.\
D) A single, large, static Bayesian network structure.

**Question 17**\
What is the specific inference task defined as calculating the probability distribution over the current state given all evidence observed so far, $P(X_t|e_{1:t})$?\
A) Prediction\
B) Smoothing\
C) Filtering (or State Estimation)\
D) Most Likely Sequence

**Question 18**\
Which recursive algorithm is used to compute the single **most likely sequence** of states $x_{1:t}$ given the entire evidence sequence $e_{1:t}$?\
A) The Forward-Backward algorithm\
B) The Viterbi algorithm\
C) Variable Elimination\
D) The Expectation-Maximization (EM) algorithm

**Question 19**\
A key characteristic defining a **Hidden Markov Model (HMM)** is that the state variable must be:\
A) Continuous and linearly related to the previous state.\
B) Deterministic and fully observable.\
C) A factored representation composed of multiple variables.\
D) A single, discrete entity.

**Question 20**\
For what kind of state spaces are **Kalman Filters** primarily designed?\
A) Discrete state spaces with large state variables.\
B) Continuous state spaces.\
C) Factored, Boolean state spaces.\
D) Partially observable, logical state spaces.

**Question 21**\
A Linear Dynamical System assumes two mathematical properties for its processes. It assumes **linear transitions** and which type of conditional probability distribution?\
A) Bernoulli distributions.\
B) Gaussian (or normal) conditional distributions.\
C) Exponential distributions.\
D) Categorical distributions.

**Question 22**\
What major advantage do **Dynamic Bayesian Networks (DBNs)** offer over HMMs for modeling complex systems?\
A) DBNs remove the Markov property, allowing for non-local dependencies.\
B) DBNs can use a factored representation for the state, allowing linear scaling with the number of variables, rather than exponential.\
C) DBNs can only model deterministic state transitions, making calculations faster.\
D) DBNs require less sensor data because they rely on fixed prior beliefs.

**Question 23**\
Temporal probabilistic models rely on the **Markov property**, which simplifies the model by stipulating that:\
A) The probability of all future states is 0.\
B) The future depends only on the present, not on the path by which the present state was reached.\
C) All state variables are independent of all evidence variables.\
D) The state transitions are irreversible.

**Question 24**\
What property is assumed in temporal probabilistic models when the agent assumes that the transition model $P(X_t|X_{t-1})$ and the sensor model $P(E_t|X_t)$ are fixed throughout time?\
A) Time-heterogeneity\
B) Time-homogeneity\
C) Atomic Representation\
D) Stochastic Dominance

**Question 25**\
When applying likelihood weighting to Dynamic Bayesian Networks (DBNs), why does its accuracy often suffer?\
A) Because likelihood weighting requires solving the prediction problem exactly before sampling.\
B) Because early state variables are sampled without the benefit of later evidence variables, leading to low weights.\
C) Because the algorithm can only handle discrete variables, violating the model's structure.\
D) Because the maximum number of samples $N$ is fixed, limiting accuracy regardless of the evidence.

**Question 26**\
The **Particle Filtering** algorithm maintains a set of weighted samples (particles) to track the belief state. What is the crucial step in the recursive update cycle that prevents the sample population from diverging from the true distribution?\
A) Rejection of samples that violate the time-homogeneity assumption.\
B) Exact calculation of the mean and covariance (similar to Kalman filters).\
C) Resampling the population based on sample weights, replicating high-weight samples.\
D) Logarithmic transformation of all particle coordinates.

**Question 27**\
Which inference task in temporal models involves calculating $P(X_k|e_{1:t})$ for some time $k < t$, effectively refining the estimate of a past state using all observations up to the current time $t$?\
A) Filtering\
B) Prediction\
C) Forecasting\
D) Smoothing

**Question 28**\
Dynamic Bayesian Networks (DBNs) are presented as a factored model for Markov processes that include which two classic temporal models as special cases?\
A) The Viterbi algorithm and Forward-Backward algorithm.\
B) Markov Decision Processes (MDPs) and Partially Observable MDPs (POMDPs).\
C) Hidden Markov Models (HMMs) and Kalman Filters.\
D) First-Order Logic and Propositional Logic.

**Question 29**\
In DBNs, what type of model is typically used to handle sensor noise for both continuous and discrete state variables, often approximated using a distribution in which the probability of error drops off appropriately?\
A) Bernoulli error model.\
B) Gaussian error model.\
C) Maximum Likelihood model.\
D) Laplace error model.

**Question 30**\
What are the three core steps in the recursive update cycle of Particle Filtering, in order?\
A) Sampling, Normalizing, Prediction.\
B) Propagation, Weighting, Resampling.\
C) Initialization, Prediction, Evaluation.\
D) Filtering, Smoothing, Prediction.

***
[This is the answers](https://github.com/neiveIsAfraid/UAS-PKA/blob/main/W12%20Bayesian%20Reasoning%20%7C%20MCQ%20Answers%20%7B1%7D.md)
