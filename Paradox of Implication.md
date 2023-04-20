# Paradox of Implication: Irrelevant Reasoning and Counter-Intuitive

Material implication generates valid conclusions from irrelevant premises, which mismatches classical logic and human intuition. For instance, consider the valid sequent ¬𝑝 ⊢ 𝑝 → ¬q, if p is the statement "it is a sunny day," q is the statement "the earth does not explode"; then, the sequent becomes "it is not a sunny day, therefore, if it is a sunny day, then the earth explodes". This paradox shows classical logic allows people to do irrelevant reasoning and it does not capture the essence of natural language (counter-intuitive).

## Proposal: Relevant Logic with 4-Valued Logic
To prevent irrelevant reasoning, it is obvious that something else should be added to the classical logic system for restricting the reasoning and showing relevancy between premises and conclusions. Meanwhile, the current truth values are not rich enough to capture some meanings in natural language. So, my proposal for solving this paradox will be applying some features from relevant logic which introduces ";" as a new symbol and stops allowing the weakening rule for adding irrelevant assumptions. Meanwhile, instead of three-valued semantics for relevant logic, the proposal chooses to use 4-valued logic (truth values are {“True”, “False”, “Both”, “Neither”}) from Belnap (1977) for better catching and interpreting the natural language’s ambiguity, then trying best to solve the counter-intuitive problem.

## Merits and Demerits:
The merit of this proposal is it solved some problems from the irrelevant reasoning, still using the sequent in the first paragraph:

```
¬𝑝 ⊢ 𝑝 → ¬𝑞
α1            (1) ¬𝑝 𝐴
α2            (2) 𝑝 𝐴
α3            (3) 𝑞 𝐴
α1,α2         (4) ¬𝑞 (1)(2)[α3] 𝑅𝐴𝐴
α1            (5) 𝑝 → ¬𝑞 (4)[α2] → I
```

The (4) will not be allowed because we cannot add the irrelevant assumption α3 to use the RAA without the weakening rule. However, relevant logic allows the contraction, but one of the important reasons for making this proposal is to capture more accurate meanings in natural language for avoiding counterintuitive, and natural languages care about the quantity or resource in most situations.

From my understanding, the relevant logic is like classic logic, assumptions are mostly used to build the relations or connections for single or compound statements, but classical logic can utilize the weakening rule and "," to build non-existent relationships to make irrelevant reasoning. So, it does not matter whether we have multiple same assumptions or just one. In the above table, (6) and (7) are logically equivalent from the relevancy or relationship perspective, they all show that we need α1 and α2 for deducing 𝑟. For example, “I eat breakfast and drink a cup of coffee” (α1; α2) and “I eat breakfast and I drink two cups of coffee” (α1; α2;α2), are the same in terms of the meaning of “I drink coffee” (r). It is a convenient way but may inevitably result in some problems when we need to deal with the sequent with arithmetic properties for both premises and conclusions such as “one 1000ml glass; 500ml water; 500ml water ⊢ a glass of water”, which has totally different truth values for the sequent when we decide to contract one repeat antecedent. The dilemma is throwing the contraction feature away makes the system redundant for capturing the relevance when there is some arithmetic property in the antecedent but not in the conclusion such as “one 1000ml glass; 500ml water; 500ml water ⊢ there are some waters in glass”, which is also counter-intuitive in natural language as normal people do not need the second “500ml water” to know “there are some waters in glass”. So far, I cannot think of a better idea to solve the problem and make the logic work without considering the content in logic, following the relevant logic is the best method even scarifying some accuracy in natural language. The three-valued semantics in relevant logic improves from classical logic and captures more reasoning and meaning of natural languages by adding the undefined truth value. However, it is still not rich enough as in real life we use the sentence “I don’t know.” very often, which represents the status of neither true nor false because we have no information so we cannot simply say something is true, false, or both. The merit of extending logical connectives to A4 is helping the system to capture more meaning in natural language because we can express the new status “Neither” rather than simply “Both”. Sadly, the choice of suitable entailment relationship has not been settled done for this 4-valued logic, so I made mine for this proposal (row implies column), which may result in some problems and demerits:

```
| → | N | F | T | B |
|---|---|---|---|---|
| N | T | F | F | F |
| F | F | T | F | B |
| T | F | F | T | B |
| B | F | B | B | T |
```
The ideology of the above table is anything infers from nothing (e.g., 𝑁 → 𝐹), or nothing infers from anything is false unless it is from nothing to nothing; without the “Neither” status, anything infers from both true and false and vice versa is both true and false (e.g., 𝐵 → 𝐹) except it infers from itself; with only “True” and “False”, the true conditional is when both antecedent and conclusions are true or are false. This ideology may share some common ground with statistics, which has a basic idea of you cannot deduce anything with no information or data, and you cannot simply erase the effective information (unless it is trimming outliers) to a less or even empty information state in the system (ignoring some specific forecasting techniques such as mean-square forecasting one-step or three-step, which makes prediction when pretending not to know the data in each next period of data series). The counter-intuitive conditional “ 𝑝 → 𝑞 is true unless p is true, and q is false” is addressed to some extent by following the implication rules in the above table. The “if…then…” in natural language is mostly used for expressing causation such as “if tomorrow rains then we don’t go to the school”. Another usage of “if…then…” in natural language is when people try to say someone cannot do something in an ironic way such as “if you can get full mark from exam, then I’m the Batman.”. Both of two situations are covered and there will not counter-intuitive true conditional when true antecedent and false conclusions (vice-versa).


