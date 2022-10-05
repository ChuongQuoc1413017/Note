## How to Reason Deductively

### Table of contents
* [1. Definition of deductive argument](#1-Definition-of-deductive-argument) 
* [2. Deductive Logic](#2-Deductive-Logic)
* [3. Conjunctions and Disjunctions](#3-Conjunctions-and-Disjunctions)
* [4. Conditionals](#4-Conditionals)


### 1. Definition of deductive argument:
+ A ***deductive argument*** is an argument that is persented as valid:
+ An argument is ***valid*** just in case there is no possible way for its premises to be true when its conclusion is false

### 2. Deductive Logic
+ A ***proposition*** is something that can be either true or false, and that can be the premise or the conclusion of an argument
+ A ***propositional connective*** is something that takes propositions , and makes new propositions out of them
+ A ***truth-functional connective*** is a propositional connective that makes a new proposition whose truth or falsity depends solely on the truth or falsity of its propositional ingredients
+ A ***truth-table*** is a device that can be used to explain how a truth-functional connective or a truth-functional operator works
+ Notation for truth-functions
	+ Conjunction: &
	+ Disjunction: V
	+ Negation: ~
+ Rules are general 
	+ Rule are designed to apply to mainy different possible cases
	+ Ex: "you should never under any circumstances hit another person" is a rule
+ Summary:
	+ Some propositional connectives are truth-functional connectives
	+ A truth-functional connective is a propositional connective that makes a new proposition whose truth or falsity depends solely on the truth or falsity of its propositional ingredients 
	+ Some arguments are avlid because of the truth-functional connectives  that they are (in below)

### 3. Conjunctions, Disjunctions and Negation
+ ***and*** can have different uses, 
	+ but we only consider ***and*** as a connective
	+ When "and" is used to express a truth-functional connective, we call that truth-functional connective ***conjunction***
	+ The truth-table of "conjunction"
		| P     | Q     | P & Q |
		|-------|-------|-------|
		| True  | True  | True  |
		| True  | False | False |
		| False | True  | False |
		| False | False | False |
	+ Conjunction elimination: valid by using truth-table
+ ***or*** as ***disjunction***
	+ Either Mancheester won it or Barcelona won it => exclusive
	+ This breakfast or lunch => inclusive
	+ The truth-table of "disjunction"
		| P     | Q     | P V Q |
		|-------|-------|-------|
		| True  | True  | True  |
		| True  | False | True  |
		| False | True  | True  |
		| False | False | False |
	+ Disjunction introduction: valid by using truth-table
+ ***Negation*** 
	+ The truth-table
		| P     | ~ P  |
		|-------|------|
		| True  | False|
		| False | True |
	+ Does "not" express negation?
		+ Sometimes, but not always. It depends on the context
+ Conjunctions and disjunctions can be combined together
	| S     | P     | Q     | P V Q | S & (P V Q) |
	|-------|-------|-------|-------|-------------|
	| True  | True  | True  | True  |True         |
	| True  | True  | False | True  |True         | 
	| True  | False | True  | True  |True         |
	| True  | False | False | False |False        |
	| False | True  | True  | True  |False        |
	| False | True  | False | True  |False        |
	| False | False | True  | True  |False        |
	| False | False | False | False |False        |
+ Truth-function connectives are not associative
	+ (P & Q) V R has a different truth-table than does P & (Q V R)
	+ The truth-table for propositions (combined or basic) depends on the order in which we apply the connectives
+ Operators
	+ A ***propositional operator*** converts one proposition into another proposition, e.g. "I believe that"
	+ A ***truth-functional operator*** is a propositional operator that creats proposition whose truth depends solely on the trurh of the proposition to which the operator is applied

+ ***Commutativity***
	+ A function of two things is commutative when it delivers the same result no matter what order it operates on those things
	+ Conjunction is commutative: p & q = q & p
	+ Disjunction is commutative: p V q = q V p
+ ***Associativity***
	+ A function of three or more things is associative when it delivers the same result no matter what order it operates on those things.
	+ Conjunction is associative: p & (q & r) = (p & q) & r
	+ Disjunction is associative: p V (q V r) = (p V q) V r

### 4. Conditionals
+ "If ..., then ..." is a propositional connective
+ Is "if ..., then ..." turth-functional?
	+ ~(P & ~Q) is true
	+ P & ~Q is false
	+ If P is true, then ~Q is false
	+ If P is true, then Q is true
	+ That is just to say: If P, then Q
	+ So: "If P, then Q" follows from "~(P & ~Q)"
+ On the ther hand,
	+ If P, then Q
	+ If P is true, then Q is true
	+ If P is true, then ~Q is false
	+ P & ~Q is not true
	+ ~(P & ~Q) is true
	+ So "~(P & ~Q)" follows from "If P, then Q"
+ ***Modus Ponens***
	+ From the premises
		+ P
		+ If P, then Q
	+ Infer
		+ Q
	+ Using the truth-table to prove that modus ponens is a good rule
		| P     | Q     | if P, then Q |
		|-------|-------|--------------|
		| True  | True  | True         |
		| True  | False | False        |
		| False | True  | True         |
		| False | False | True         |
+ ***Modus Tollens***
	+ From the premises
		+ ~Q
		+ If P, then Q
	+ Infer
		+ ~P
	+ Using the truth-table to prove that modus tollens is a good rule
		| P     | Q     | if P, then Q |
		|-------|-------|--------------|
		| True  | True  | True         |
		| True  | False | False        |
		| False | True  | True         |
		| False | False | True         |
+ "if ..., then ..." does not always express a conditional
+ ***BiconditionalS***
	+ "If ... and only if ..."
	+ P = Q means (P -> Q) & (Q -> P)
	+ Truth-table for the biconditional
		| P     | Q     | P = Q |
		|-------|-------|-------|
		| True  | True  | True  |
		| True  | False | False |
		| False | True  | False |
		| False | False | True  |

***

<br><br>
<br><br>
_This note was created by [**ChuongQuoc1413017**](https://github.com/ChuongQuoc1413017/Note/tree/main/Introduction%20to%20Logic%20and%20Critical%20Thinking%20Specialization)@2022_
