
## Solutions Section

### Chapter 13: Probabilistic Reasoning

**Question 1**
What structural property allows a Bayesian network to represent a full joint probability distribution in a concise manner?
**A) It exploits the underlying statistical relationships, specifically conditional independence.**
*Supporting Quote: "Bayesian networks can represent [conditional independence relationships] explicitly in the form of Bayesian networks."; "Bayesian networks provide a concise graphical structure that exploits the underlying statistical relationships, specifically conditional independence, resulting in a representation that is often exponentially smaller than an explicitly enumerated joint distribution."*

**Question 2**
If a node in a Bayesian network represents a Boolean variable and has $k$ Boolean parents, how many independently specifiable probabilities are contained in its Conditional Probability Table (CPT)?
**C) $2^k$**
*Supporting Quote: "In general, a table for a Boolean variable with k Boolean parents contains $2^k$ independently specifiable probabilities."*

**Question 3**
Which statement accurately describes the relationship between the conditional probability table (CPT) entries and the conditional probabilities they represent in a Bayesian network?
**B) The parameters $\theta(x_i | \text{parents}(X_i))$ are exactly the conditional probabilities $P(x_i | \text{parents}(X_i))$ implied by the joint distribution.**
*Supporting Quote: "It turns out that from Equation (13.1) we can prove that the parameters $\theta(x_i | \text{parents}(X_i))$ are exactly the conditional probabilities $P(x_i | \text{parents}(X_i))$ implied by the joint distribution."*

**Question 4**
In general, exact probabilistic inference in Bayesian networks is classified as being harder than NP-complete problems. What is the specific complexity classification cited in the sources?
**C) \#P-hard**
*Supporting Quote: "Because computing the number of satisfying assignments for a 3-SAT problem is \#P-complete ('number-P complete'), this means that Bayes net inference is \#P-hard—that is, strictly harder than NP-complete problems."*

**Question 5**
When constructing the links of a Bayesian network, the resulting network will generally be more compact if the variables are ordered such that:
**C) Causes precede effects.**
*Supporting Quote: "Any order will work, but the resulting network will be more compact if the variables are ordered such that causes precede effects."*

**Question 6**
What is the primary computational task for any probabilistic inference system in a Bayes net, given query variable $X$ and evidence $e$?
**D) Computing the posterior probability distribution for $X$, given observed evidence $e$, denoted $P(X | e)$.**
*Supporting Quote: "The basic task for any probabilistic inference system is to compute the posterior probability distribution for a set of query variables, given some observed event—usually, some assignment of values to a set of evidence variables... A typical query asks for the posterior probability distribution $P(X | e)$."*

**Question 7**
The Variable Elimination algorithm optimizes exact inference in Bayesian networks by leveraging which mathematical principle to rearrange the summation over the full joint distribution?
**A) Distributing the summations inwards over factors that do not depend on the variable being summed out.**
*Supporting Quote: "The Variable Elimination algorithm exploits the fact that summation distributes over multiplication: $\sum_{x} f_{1}(X, Y) \times f_{2}(Y, Z) = f_{2}(Y, Z) \times \sum_{x} f_{1}(X, Y)$."*

**Question 8**
In the context of approximate inference using sampling, how does **rejection sampling** estimate the posterior probability $P(X|e)$?
**C) By generating samples from the prior distribution and discarding those that do not match the observed evidence.**
*Supporting Quote: "First, it generates samples from the prior distribution specified by the network. Then, it rejects all those that do not match the evidence."

**Question 9**
What is the core difference between the way **Likelihood Weighting** handles evidence variables compared to **Rejection Sampling**?
**B) Likelihood Weighting fixes the values of the evidence variables and weights the sample by their likelihood, whereas Rejection Sampling discards samples inconsistent with the evidence.**
*Supporting Quote (Likelihood Weighting): "The most common approach is called likelihood weighting... the algorithm fixes the values for the evidence variables E and samples all the nonevidence variables in topological order, each conditioned on its parents."*
*Supporting Quote (Rejection Sampling): "Then, it rejects all those that do not match the evidence."*

**Question 10**
**Gibbs sampling** is categorized as an instance of what family of statistical algorithms used for approximate inference?
**C) Markov Chain Monte Carlo (MCMC) algorithms**
*Supporting Quote: "We begin by describing a particular form of MCMC called Gibbs sampling..."*

**Question 11**
In Gibbs sampling, when a non-evidence variable $X_i$ is chosen for updating, the new value for $X_i$ is sampled based on the values of the variables in its:
**D) Markov blanket**
*Supporting Quote: "set the value of $Z_i$ in $x$ by sampling from $P(Z_i | \text{mb}(Z_i))$"; "The one remaining detail concerns the method of calculating the Markov blanket distribution $P(X_i | \text{mb}(X_i))$, where $\text{mb}(X_i)$ denotes the values of the variables in $X_i$’s **Markov blanket**, $MB(X_i)$."*

**Question 12**
In the theory of **Causal Networks**, what is the purpose of the **do-operator** (e.g., $do(\text{Sprinkler}=\text{true})$)?
**C) To model external intervention by replacing the intervened variable's conditional distribution with a deterministic assignment, effectively deleting incoming links.**
*Supporting Quote: "In the notation of the do-calculus... this is written as $do(\text{Sprinkler}=\text{true})$. Once done, this means that the sprinkler variable is no longer dependent on whether it’s a cloudy day. We therefore delete the equation S= $f_S(C, U_S)$ from the system of structural equations and replace it with S= true..."*

**Question 13**
Noisy logical relationships, such as **noisy-OR**, help simplify the representation of Conditional Probability Tables (CPTs) by reducing the number of parameters required for a variable with $k$ parents from $O(2^k)$ to approximately what complexity?
**B) $O(k)$**
*Supporting Quote: "In general, noisy logical relationships in which a variable depends on $k$ parents can be described using $O(k)$ parameters instead of $O(2^k)$ for the full conditional probability table."*

**Question 14**
In the context of probabilistic inference (e.g., computing $P(X | e)$), the set of all random variables in the domain is divided into three components. These components are:
**C) Query variables, evidence variables, and hidden (nonevidence, nonquery) variables.**
*Supporting Quote: "X denotes the query variable; E denotes the set of evidence variables $E_1, \ldots, E_m$, and $e$ is a particular observed event; Y denotes the hidden (nonevidence, nonquery) variables $Y_1, \ldots, Y_{\ell}$."*

**Question 15**
The enumeration-ask algorithm (ENUMERATION-ASK) suffers from a severe efficiency problem because the calculation of the posterior probability involves:
**B) Repeatedly calculating the same subexpressions within the summation.**
*Supporting Quote: "If you look carefully at the tree in Figure 13.10, however, you will see that it contains repeated subexpressions... The key to efficient inference in Bayes nets is avoiding such wasted computations."*

### Chapter 14: Probabilistic Reasoning over Time

**Question 16**
In probabilistic reasoning over time, what is the world state generally modeled using?
**A) A sequence of time slices, each containing state ($X_t$) and evidence ($E_t$) variables.**
*Supporting Quote: "A changing world is modeled using a series of time slices, where the state variables ($X_t$) and evidence variables ($E_t$) are replicated over time."*

**Question 17**
What is the specific inference task defined as calculating the probability distribution over the current state given all evidence observed so far, $P(X_t|e_{1:t})$?
**C) Filtering (or State Estimation)**
*Supporting Quote: "Filtering, or state estimation, is the computation of $P(X_t | e_{1:t})$. It is the core task for an agent that needs to make decisions based on its current belief state."*

**Question 18**
Which recursive algorithm is used to compute the single **most likely sequence** of states $x_{1:t}$ given the entire evidence sequence $e_{1:t}$?
**B) The Viterbi algorithm**
*Supporting Quote: "The Viterbi Algorithm can be used to compute the single most likely sequence of states $x_{1:t}$ given the entire evidence sequence $e_{1:t}$."*

**Question 19**
A key characteristic defining a **Hidden Markov Model (HMM)** is that the state variable must be:
**D) A single, discrete entity.**
*Supporting Quote: "A Hidden Markov Model (HMM) is a temporal probabilistic model in which the state variable $X_t$ is a single, discrete random variable."*

**Question 20**
For what kind of state spaces are **Kalman Filters** primarily designed?
**B) Continuous state spaces.**
*Supporting Quote: "Hidden Markov Models are primarily designed for discrete state spaces... For continuous state spaces, the **Kalman filter** algorithm is the most common method for filtering."*

**Question 21**
A Linear Dynamical System assumes two mathematical properties for its processes. It assumes **linear transitions** and which type of conditional probability distribution?
**B) Gaussian (or normal) conditional distributions.**
*Supporting Quote: "A Linear Dynamical System is defined by the assumption of linear transitions and Gaussian conditional distributions."*

**Question 22**
What major advantage do **Dynamic Bayesian Networks (DBNs)** offer over HMMs for modeling complex systems?
**B) DBNs can use a factored representation for the state, allowing linear scaling with the number of variables, rather than exponential.**
*Supporting Quote: "DBNs solve the problem of exponential size of the state space by factoring the state into individual state variables, enabling the system to scale linearly rather than exponentially with the number of state variables."*

**Question 23**
Temporal probabilistic models rely on the **Markov property**, which simplifies the model by stipulating that:
**B) The future depends only on the present, not on the path by which the present state was reached.**
*Supporting Quote: "The Markov property is the assumption that the current state is sufficient to predict the next state, given the action... the future is conditionally independent of the past, given the present."*

**Question 24**
What property is assumed in temporal probabilistic models when the agent assumes that the transition model $P(X_t|X_{t-1})$ and the sensor model $P(E_t|X_t)$ are fixed throughout time?
**B) Time-homogeneity**
*Supporting Quote: "We assume that the transition model $P(X_t|X_{t-1})$ and the sensor model $P(E_t|X_t)$ are time-homogeneous; that is, they do not change over time."*

**Question 25**
When applying likelihood weighting to Dynamic Bayesian Networks (DBNs), why does its accuracy often suffer?
**B) Because early state variables are sampled without the benefit of later evidence variables, leading to low weights.**
*Supporting Quote: "In our discussion of likelihood weighting in Chapter 13, we pointed out that the algorithm’s accuracy suffers if the evidence variables are 'downstream' from the variables being sampled, because in that case the samples are generated without any influence from the evidence and will nearly all have very low weights."*

**Question 26**
The **Particle Filtering** algorithm maintains a set of weighted samples (particles) to track the belief state. What is the crucial step in the recursive update cycle that prevents the sample population from diverging from the true distribution?
**C) Resampling the population based on sample weights, replicating high-weight samples.**
*Supporting Quote: "The second key innovation is to focus the set of samples on the high-probability regions of the state space. This can be done by throwing away samples that have very low weight, according to the observations, while replicating those that have high weight."*

**Question 27**
Which inference task in temporal models involves calculating $P(X_k|e_{1:t})$ for some time $k < t$, effectively refining the estimate of a past state using all observations up to the current time $t$?
**D) Smoothing**
*Supporting Quote: "Smoothing, or hindsight, is the computation of $P(X_k | e_{1:t})$ for $1 \le k < t$. The result is a refined estimate of the state at some past time $k$..."*

**Question 28**
Dynamic Bayesian Networks (DBNs) are presented as a factored model for Markov processes that include which two classic temporal models as special cases?
**C) Hidden Markov Models (HMMs) and Kalman Filters.**
*Supporting Quote: "DBNs subsume both HMMs and Kalman filters, allowing for more complex factored representations."*

**Question 29**
In DBNs, what type of model is typically used to handle sensor noise for both continuous and discrete state variables, often approximated using a distribution in which the probability of error drops off appropriately?
**B) Gaussian error model.**
*Supporting Quote: "For continuous measurements, a Gaussian distribution with a small variance might be used... We use the term **Gaussian error model** to cover both the continuous and discrete versions."*

**Question 30**
What are the three core steps in the recursive update cycle of Particle Filtering, in order?
**B) Propagation, Weighting, Resampling.**
*Supporting Quote: "1. The samples are propagated forward... 2. Each sample is weighted by the likelihood it assigns to the new evidence... 3. The population is resampled to generate a new population of N samples."; *See also pseudocode step numbers in.*
