***

### Solutions Section

**1. Correct Answer: B**
"The central component of a knowledge-based agent is its knowledge base, or KB. A knowledge base is a set of sentences."

**2. Correct Answer: B**
"MAKE-ACTION-QUERY constructs a sentence that asks what action should be done at the current time. The details of the inference mechanisms are hidden inside TELL and ASK." and "action←ASK(KB, MAKE-ACTION-QUERY(t))"

**3. Correct Answer: C**
"The semantics defines the rules for determining the truth of a sentence with respect to a particular model."

**4. Correct Answer: D**
"a sentence $\alpha$ is entailed by a KB if $\alpha$ is true in all possible worlds where the KB is true."

**5. Correct Answer: C**
"$P \Rightarrow Q$ is true unless P is true and Q is false in $m$."

**6. Correct Answer: C**
"The resolution rule applies only to clauses... Every sentence of propositional logic is logically equivalent to a conjunction of clauses."

**7. Correct Answer: C**
"For simpler knowledge bases in Horn form (definite clauses), forward chaining (data-driven) and backward chaining (goal-directed) provide natural and efficient reasoning algorithms."

**8. Correct Answer: B**
"A pure symbol is a symbol that always appears with the same 'sign' in all clauses... It is easy to see that if a sentence has a model, then it has a model with the pure symbols assigned so as to make their literals true, because doing so can never make a clause false."

**9. Correct Answer: C**
"If KB and $\alpha$ contain $n$ symbols in all, then there are $2^n$ models. Thus, the time complexity of the algorithm is $O(2^n)$."

**10. Correct Answer: B**
"Propositional logic does not scale to environments of unbounded size because it lacks the expressive power to deal concisely with time, space, and universal patterns of relationships among objects."

**11. Correct Answer: B**
"Propositional logic commits only to facts, but FOL commits to facts, objects, and relations."

**12. Correct Answer: B**
"An expression that refers to an object is called a term. The different kinds of terms are constant symbols, variable symbols, and function symbols."

**13. Correct Answer: B**
"each model includes an interpretation that specifies exactly which objects, relations and functions are referred to by the logical vocabulary."

**14. Correct Answer: C**
"the implication is true whenever its premise is false—regardless of the truth of the conclusion."

**15. Correct Answer: C**
"$\neg \exists x P \equiv \forall x \neg P$"

**16. Correct Answer: B**
"We can use the equality symbol to signify that two terms refer to the same object."

**17. Correct Answer: B**
"First, we insist that every constant symbol refer to a distinct object—the unique-names assumption."

**18. Correct Answer: C**
"Such an answer is called a substitution or binding list."

**19. Correct Answer: C**
"Decide on a vocabulary of predicates, functions, and constants. That is, translate the important domain-level concepts into logic-level names... The result is a vocabulary that is known as the ontology of the domain."

**20. Correct Answer: D**
"in first-order logic we can quantify over time, so we need just one successor-state axiom for each predicate, rather than a different copy for each time step."

**21. Correct Answer: D**
"entailment for first-order logic is semidecidable—that is, algorithms exist that say yes to every entailed sentence, but no algorithm exists that also says no to every nonentailed sentence."

**22. Correct Answer: C**
"if the KB includes function symbols, this set of ground terms can be infinite, meaning that general propositionalization is not feasible"

**23. Correct Answer: C**
"This process is called unification and is a key component of all first-order inference algorithms."

**24. Correct Answer: C**
"if there is some substitution $\theta$ that makes each of the conjuncts of the premise of the implication identical to sentences already in the knowledge base, then we can assert the conclusion of the implication, after applying $\theta$."

**25. Correct Answer: B**
"it is complete for definite clause knowledge bases; that is, it answers every query whose answers are entailed by any knowledge base of definite clauses."

**26. Correct Answer: D**
"The backward-chaining algorithm... is essentially identical to the AND-OR-GRAPH-SEARCH algorithm... This approach is the foundation of the Prolog logic programming language." and "Prolog uses database semantics".

**27. Correct Answer: C**
"Skolemization is the process of removing existential quantifiers"

**28. Correct Answer: C**
"Resolution proves that KB $\models \alpha$ by proving that $\text{KB} \land \neg \alpha$ unsatisfiable... if a set of sentences is unsatisfiable, then resolution will always be able to derive a contradiction. Resolution cannot be used to generate all logical consequences of a set of sentences, but it can be used to establish that a given sentence is entailed by the set of sentences."

**29. Correct Answer: C**
"The simplest rule, demodulation, takes a unit clause $x=y$ and some clause $\alpha$ that contains the term $x$, and yields a new clause formed by substituting $y$ for $x$ within $\alpha$."

**30. Correct Answer: C**
"a definite clause is either atomic, or is an implication whose antecedent is a conjunction of positive literals and whose consequent is a single positive literal."
