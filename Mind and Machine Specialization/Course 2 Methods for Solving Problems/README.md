## Methods for Solving Problems

### Table of contents
* [1. Recognizing Problems and Problem Solving Methods](#1-Recognizing-Problems-and-Problem-Solving-Methods) 
* [2. Understanding the Difficulty of Problems](#2-Understanding-the-Difficulty-of-Problems)
* [3. Judgment and Decision Making](#3-Judgment-and-Decision-Making)
* [4. Heuristics and Biases](#4-Heuristics-and-Biases)


### 1. Recognizing Problems and Problem Solving Methods
+ Modeling People's Thinking with Machines: Solving Problems
+ What can we say about puzzles like rubik or sudoku?
	+ Characterized by conscious (and effortful!) thought
	+ Evolutionarily recent
	+ Not especially "messy" in the sense that they don't have strong cultural or affective elements
	+ Self-contained (not a whole lot of background knowledge is needed)
+ => All of this makes them good candiadates for first attempts at modeling by machine
+ Let's represent the problem by a ***problem space***
	+ We will make a graph with vertices (nodes) and edges (links)
	+ Each vertex represents a distinct ***state*** of the problem
	+ Each edge represents a natural ***move*** from one state of the problem to another
	+ Think of how this would apply to (say) the Rush Hour puzzle, or Rubik's Cube, or the 15-16 puzzle
+ So, a first question that we could ask is:
	+ "How hard is this puzzle?" (Recall our discussion of "what makes a problem hard?")
	+ One (very partial) answer to that question is to reframe it:
		+ "How ***big*** is the problem space?" (How many vertices and edges are in it?)
	+ Intuitively, it makes sense that the bigger the problem space, the harder the problem will be to solve
+ Once we think about the problem as a space or graph, that suggests a lot of other ideas:
	+ Think of our puzzle as a "starting state" in the graph: the vertex that we start out with
	+ Think of our goal of the puzzle as "getting to a goal state" (say, one in which the 15 tiles are in the right spots)
	+ Think of our job as finding a ***path*** in the graph from our starting state to the (or a) goal state, traversing edges (moves) at each step
	+ This is what we mean by a ***search problem***: we're searching a (possibly very large) graph for a path to a solution
	+ That's the kind of task that we can write a computer program to do!
+ When computers search problem spaces, they often do it in ways that don't seem like the "human" approach
	+ "Weak" methods
	+ Depth-first search
	+ Breadth-first search
+ Some computer search strategies feel at least a little more true to "human style" problem solving
	+ "Heuristic" methods
	+ Hill climbing
	+ Best-first search
	+ Means-ends analysis: an early example of a problem-solving strategy inspired by human beings
		+ Look for the most important difference between where we are now and the "goal state"
		+ If you can fix this most important difference right away, do so
		+ Otherwise, see if you can do something that will enable you to fix the most important difference
		+ Finding this "something" may involve yet another round of means-ends analysis 
+ When computer scientists look at search algorithms, they're generally concerned about a number of key issues:
	+ ***Completeness***: will we always find a solution if there is one?
	+ ***Running time***: how long will it take to find the solution?
	+ ***Space***: how much memory space will the strategy need?
	+ ***Optimality***: once we find a solution, is it the best solution?

### 2. Understanding the Difficulty of Problems
+ Problems that challenge minds and machines
		+ For some (many? most?) problems, it's hard to come up with a straightforward "problem space" representation
	+ From Michalewicz and Fogel, How to solve It: Morden Heuristics
		+ Mr. Smith and his wife invited four other couples for a party. When everyone arrvied, some of the people in the room shook hands with some of the others. Of course, nobody shook hands with their spouse, and nobody shook hands with the same person twice
		+ After that, Mr. Smith asked everyone how many times they shook someone's hand. He received different answers from everybody
		+ How many times did Mrs. Smith shake someone's hand?
	+ Polya's Heuristics: a Sampler
		+ Do you know a related problem? (If you cannot solve the proposed problem, try to solve first some related problem)
		+ Did you use all the data?
		+ Can you use the result for a related problem?
		+ Draw a figure
		+ Reductio ad absurdum, induction, decomposing and recomposing, dimensional analysis, etc.
	+ How would you solve a problem like this?
		+ Imagine two quarters side by side, as in the picture. Now roll the )heads) quarter at right, without slipping, counterclockwise around the edge of the quarter at left. Eventually, the (heads) quarter will be at the left of the stationary quarter. Which way wil George Washington be gacing at that point?
		+ Imagine a ping pong ball rolling to the left at 1 cm/sec on a frictionless track. On the same track, rolling to the right at 1 cm/sec, is a bowling ball. The mass of the ping pong is 1 gram; the mass of the bowling ball is 10,000 grams. After the two collide (elastically), what will their final velocities be?
	+ Poundstone, Labyrinths of Reason
		+ A man gets an unsigned letter telling him to go to the local graveyard at midnight. He does not generally pay attention to such things, but complies out of curiosity. It is a deathly still night, lighted by a thin crescent moon. The man stations himself in front of his family's ancestral crypt. The man is about to leave when he hears scraping footsteps. He yells out, but no one answers. The next morning, the caretaker finds the man dead in front of the crypt, a hideous grin on his face
		+ Did the man vote for Teddy Roosevelt in the 1904 US Presidential election?
+ Machines and Logic
	+ Propositional Logic
	+ Modus Ponens
		+ Premises: 
			+ If there is fire, there is smoke.
			+ There is fire
		+ Conclusion:
			+ There is smoke
	+ Modus Tollens
		+ Premises: 
			+ If there is fire, there is smoke.
			+ There is not smoke
		+ Conclusion:
			+ There is not fire
+ Logical Fallacies
	+ Denial of the Antecedent
		+ Premises: 
			+ If there is fire, there is smoke.
			+ There is not fire
		+ Conclusion:
			+ There is not smoke
	+ Affirmation of the Consequent
		+ Premises: 
			+ If there is fire, there is smoke.
			+ There is smoke
		+ Conclusion:
			+ There is fire
+ A logical selection task (Wason)
	+ If a card has a vowel on one side, then it has an even number on the other side
+ A logical selection task (Tooby/Cosmides)
	+ if a person is drinking beer, then the person must be over 19 years of age

### 3. Judgment and Decision Making
+ Judgment and Decision Making: the Computational View
+ First of all, what do mean by "judgment" or "decision-making"?
	+ Not quite the same as problem-solving (though there are gray areas)
	+ The normative (as opposed to descriptive) stance
	+ Judgment and decision-making is usually thought to have deeper evolutionary roots
+ An example of a decision-making situation (problem-framing)
	+ First, we are offered a bonus of $300. Then, we are asked to choose between the two following possibilities:
		+ A. To receive $100 for sure; or
		+ B. To toss a coin. If we win the toss, we will get $200; if we lose, we receive nothing at all
+ An example of a decision-making situation (problem-framing)
	+ First, we are offered a bonus of $300. Then, we are asked to choose between the two following possibilities:
		+ C. We are guaranteed to lose $100
		+ D. We toss a coin, and if we lose, we have to pay $200, but if we win, we don't have to pay anything
+ Another example of "problem-framing" from Dan Ariely, Predictable Irrational
	+ Economist.com subscription: $59
	+ Print subscription to The Economist: $125
	+ Print plus web subscription: $125
+ Some issues for discussion
	+ Are these examples of "mistakes" in judgement?
	+ If they are mistakes, why do we make them?
	+ The issue of other agents manipulating our judgement, and the "environment of evolutionary adaptedness"

### 4. Heuristics and Biases
+ The conjunction effect
	+ Bill is 34 years old. He is intelligent, but unimaginative, compulsive, and generally lifeless. In school, he was strong in mathematics but weak in social studies and humannities
		+ Bill is a doctor, and his hobby is playing poker
		+ Bill is an architect
		+ Bill is an accountant
		+ Bill plays jazz for a hobby
		+ Bill surfs for a hobby
		+ Bill is a reporter
		+ Bill is an accountant who plays jazz for a hobby
		+ Bill climbs mountains for a hobby
	+ Steve is very shy and withdrawn, invariably helpful, but with little interest in people or in the world of reality. A meek and tidy soul, he has a need for order and structure, and a passion for detail
		+ Architect
		+ Farmer
		+ Librarian
		+ Biologist
		+ Tax Driver
+ Anchoring
	+ Was Ronald Reagan 120 years old when he died?
	+ Was Ronald Reagan 50 years old when he died?
+ Memory Effects
	+ Estimate the proposition of English words that begin with the letter "K" versus words that have a "K" in the third position
+ Some issues for discussion
	+ Are there mistakes - and if so, why do we make them?
	+ What computational constraints do we bring to bear on answering questions like this?

***

<br><br>
<br><br>
_This note was created by [**ChuongQuoc1413017**](https://github.com/ChuongQuoc1413017/Note/tree/main/Mind%20and%20Machine%20Specialization)@2022_
