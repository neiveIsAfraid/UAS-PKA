### Quiz Section (1-30)

**Chapter 7: Logical Agents**

**Question 1**\
What is the primary function of the **Knowledge Base (KB)** within a knowledge-based agent?\
A. It executes the physical actions determined by the agent function.\
B. It is a set of sentences representing the agent’s knowledge about the world.\
C. It generates percepts from the environment using sensors.\
D. It performs random walks in the state space to find solutions.\

**Question 2**\
In the architecture of a generic knowledge-based agent, which function is responsible for determining the appropriate action to take at the current time?\
A. TELL(KB, MAKE-PERCEPT-SENTENCE(percept, t))\
B. ASK(KB, MAKE-ACTION-QUERY(t))\
C. MAKE-ACTION-SENTENCE(action, t)\
D. KB-AGENT(percept)\

**Question 3**\
The **semantics** of a logical language define the rules for determining:\
A. The formal structure of sentences (syntax).\
B. The efficiency of the inference algorithm.\
C. The truth of a sentence with respect to a particular model.\
D. Whether an inference procedure is sound or complete.\

**Question 4**\
What does the central semantic relationship $\text{KB} \models \alpha$ (entailment) mean?\
A. The inference algorithm found a proof for $\alpha$ from KB.\
B. KB and $\alpha$ are syntactically sound.\
C. $\alpha$ is true in the real world.\
D. $\alpha$ is true in all possible worlds (models) in which KB is true.\

**Question 5**\
In propositional logic, under what condition is an implication $P \Rightarrow Q$ false?\
A. When both $P$ and $Q$ are false.\
B. When $P$ is false and $Q$ is true.\
C. When $P$ is true and $Q$ is false.\
D. When $P$ and $Q$ have the same truth value.\

**Question 6**\
For propositional resolution to be applied, all sentences in the knowledge base must first be converted into which standardized form?\
A. Disjunctive Normal Form (DNF)\
B. Horn Form\
C. Conjunctive Normal Form (CNF)\
D. Successor-State Axioms\

**Question 7**\
The algorithms of **forward chaining** and **backward chaining** are especially efficient and complete for knowledge bases composed of which type of logical structure?\
A. Arbitrary CNF clauses.\
B. Clauses that are disjunctions of literals.\
C. Horn clauses (or definite clauses).\
D. Sentences containing only biconditionals ($\Leftrightarrow$).\

**Question 8**\
In the DPLL algorithm for propositional satisfiability, the **pure symbol heuristic** suggests a symbol should be assigned a value that:\
A. Maximizes the number of clauses made true immediately.\
B. Makes the symbol appear with only one sign (e.g., only positive) in the remaining clauses.\
C. Minimizes the number of symbols in the remaining model.\
D. Ensures the clause containing it becomes a unit clause.\

**Question 9**\
What is the worst-case time complexity of the truth-table enumeration algorithm (TT-ENTAILS?) for deciding propositional entailment, where $n$ is the total number of proposition symbols?\
A. $O(n^2)$\
B. $O(\log n)$\
C. $O(2^n)$\
D. $O(n \cdot 2^n)$\

**Question 10**\
What is cited as the key limitation of propositional logic, making it unsuitable for environments of unbounded size?\
A. Its inability to support sound inference rules.\
B. Its lack of expressive power to deal concisely with time, space, and universal patterns of relationships among objects.\
C. The requirement that all symbols must be Boolean (true/false).\
D. The difficulty of converting complex sentences into Conjunctive Normal Form.\

**Chapter 8: First-Order Logic**\

**Question 11**\
First-Order Logic (FOL) differs from propositional logic in its **ontological commitment** by committing to the existence of:\
A. Only facts.\
B. Facts, objects, and relations.\
C. Only facts and time.\
D. Only time and utility.\

**Question 12**\
In the syntax of FOL, an expression that refers to an object in the world (e.g., a constant, a variable, or the application of a function symbol) is known as a:\
A. Predicate\
B. Term\
C. Atomic Sentence\
D. Quantifier\

**Question 13**\
What is the function of the **interpretation** in an FOL model?\
A. It determines the truth values of propositional symbols (True or False).\
B. It specifies which objects, relations, and functions are referred to by the logical vocabulary.\
C. It defines the logical relationship between syntax and semantics.\
D. It dictates the efficiency of the unification process.\

**Question 14**\
When universal quantification ($\forall$) is used with implication ($P \Rightarrow Q$) in FOL, what happens when the premise ($P$) is false for a specific object?\
A. The entire universally quantified sentence is immediately false.\
B. The conclusion ($Q$) must also be false.\
C. The implication is true, regardless of the truth of the conclusion $Q$.\
D. The system must use the closed-world assumption to determine $Q$.\

**Question 15**\
The sentence $\neg \exists x P$ (It is not the case that there exists an $x$ such that $P$) is logically equivalent to which universal quantification sentence?\
A. $\forall x P$\
B. $\exists x \neg P$\
C. $\forall x \neg P$\
D. $\neg \forall x P$\

**Question 16**\
In FOL, what is the role of the **equality symbol** (=)?\
A. It establishes a necessary connection between the logical vocabulary and the real world.\
B. It is used to signify that two terms refer to the same object.\
C. It defines the truth of any atomic sentence using predicates.\
D. It converts the logic into database semantics.\

**Question 17**\
What is the **unique-names assumption** in database semantics (like that used in Prolog)?\
A. It assumes that every object exists and is unique.\
B. It assumes that every constant symbol refers to a distinct object.\
C. It assumes that every sentence not known to be true is false.\
D. It assumes that the number of objects is finite (domain closure).\

**Question 18**\
If an agent uses $\text{ASKVARS}(\text{KB}, \text{Person}(x))$ to query a First-Order Knowledge Base, the answer returned (e.g., $\{x/\text{John}\}$ or $\{x/\text{Richard}\}$) is referred to as a:\
A. Term\
B. Literal\
C. Substitution or binding list\
D. Predicate\

**Question 19**\
Which phase of the **knowledge engineering process** involves choosing predicates, functions, and constants to represent the domain concepts, effectively defining the vocabulary?\
A. Identify the questions.\
B. Assemble the relevant knowledge.\
C. Decide on an ontology.\
D. Encode a description of the problem instance.\

**Question 20**\
In FOL, **successor-state axioms** for dynamic fluents (like $\text{HaveArrow}(t)$) are more concise than in propositional logic because:\
A. They require no logical connectives.\
B. They use the equality symbol to bypass negation.\
C. They only apply to definite clauses.\
D. They quantify over time $t$, requiring only one axiom per predicate regardless of the number of time steps.\

**Chapter 9: Inference in First-Order Logic**\

**Question 21**\
What is the term used to describe the status of FOL entailment, meaning that algorithms exist that can confirm every entailed sentence, but no algorithm exists that can definitively confirm all nonentailed sentences?\
A. Completeness\
B. Soundness\
C. Decidable\
D. Semidecidable\

**Question 22**\
The process of **propositionalization** (reducing FOL inference to propositional inference by substituting ground terms for quantified variables) is generally infeasible if the KB includes which type of symbol?\
A. Constant symbols\
B. Predicate symbols\
C. Function symbols\
D. Universal quantifiers\

**Question 23**\
What is the name of the core process in lifted inference that finds the substitution ($\theta$) required to make two logical expressions identical?\
A. Skolemization\
B. Resolution\
C. Unification\
D. Indexing\

**Question 24**\
When applying **Generalized Modus Ponens**, the inference rule is triggered if the premise of the implication (e.g., $p_1 \land \dots \land p_n$) can be made identical to a set of facts in the KB using a single operation called:\
A. Subsumption\
B. Indexing\
C. Substitution ($\theta$)\
D. Demodulation\

**Question 25**\
The **FOL-FC-ASK** algorithm (First-Order Logic Forward Chaining) is guaranteed to be complete for which type of First-Order knowledge bases?\
A. Those containing non-Horn clauses.\
B. Those containing definite clauses.\
C. Those requiring Skolemization.\
D. Those using only unique names assumption.\

**Question 26**\
The **Prolog** logic programming language is based on which goal-directed inference procedure?\
A. Forward Chaining\
B. Refutation Completeness\
C. Model Checking\
D. Backward Chaining\

**Question 27**\
In the generalized resolution procedure for FOL, what technique is used to eliminate existential quantifiers before conversion to Conjunctive Normal Form (CNF)?\
A. Universal Instantiation\
B. Demodulation\
C. Skolemization\
D. Standardization apart\

**Question 28**\
**Resolution** is a single, complete proof procedure for all of FOL. Its completeness is specifically described as **refutation completeness**, meaning that:\
A. If a sentence is entailed, the resolution algorithm will find a proof.\
B. If the KB contains the empty clause, the KB is sound.\
C. If a set of sentences is unsatisfiable, a contradiction (the empty clause) will always eventually be derived.\
D. If a sentence is not entailed, the algorithm will eventually stop and confirm nonentailment.\

**Question 29**\
Which inference rule is typically used in equality reasoning to simplify expressions by taking a unit clause $x=y$ and substituting $y$ for $x$ within another clause $\alpha$ that contains the term $x$?\
A. Resolution\
B. Generalized Modus Ponens\
C. Demodulation\
D. Unification\

**Question 30**\
What characteristic defines a **definite clause** in first-order logic (assuming universal quantifiers are implicit)?\
A. It is a disjunction of literals with zero positive literals.\
B. It is any sentence that uses Skolem constants.\
C. It is an atomic sentence or an implication whose antecedent is a conjunction of positive literals and whose consequent is a single positive literal.\
D. It must include function symbols but no constant symbols.\
