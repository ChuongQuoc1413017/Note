## Interpersonal, Developmental, and Evolutionary Perspectives of the Mind

### Table of contents
* [1. Multiple Deciding Agents](#1-Multiple-Deciding-Agents) 
* [2. Game Theory](#2-Game-Theory)
* [3. Game Theory and Evolution](#3-Game-Theory-and-Evolution)
* [4. Game Theory and Cognitive Science](#4-Game-Theory-and-Cognitive-Science)
* [5. Embodied Cognition](#5-Embodied-Cognition)

### 1. Multiple Deciding Agents
+ ***Schelling's Model of Neighborhoods***
	+ Each cell in the grid can have a "red" occupant, a "blue" occupant, or else it is empty
	+ Begin by setting 50 percent of the cells to "red" and 50 percent to "blue"; then remove about 10 percent of the occupants to produce a randomly chosen, set of about 10 percent empty cells
	+ Here, each type of occupant wants at least four of their own type in their neighborhood
	+ Now repeat the folloing procedure:
		+ Find a "dissatisfied" cell (one which is currently unhappy with its surroundings). If there isn't any dissatisfied cell, we're done
		+ Move the "dissatisfied" cell contents to a randomly-chosen empty cell. For example, a red dot with only 2 red neighbors may move to a randomly-chosen empty cell
		+ That's it! Repeat till done (there are many variations on this basic idea)
+ ***What are the major themes to take from this example?***
	+ The idea of modeling cognition "beyod the individual": looking at phenomena that occur when multiple deciding agents interact
	+ The idea of "emergent" collective behaviors: here, the formation of coherent neighborhoods even when no one individual had that intention (perhaps it happened despite their intentions)
	+ A prelude to discussions of game theory in cognitive science

### 2. Game Theory
+ Prisoner's Dilemma
+ A few important, basic ideas from game theory
	+ Zero-sum vs. non-zero-sum games
	+ Two-person vs. n-person games
	+ Finite vs. infinite number of strategy choices
	+ Iterated vs. non-iterated games
+ Axelrod's Tournament
	+ Book: Robert Axelrod, The evolution of cooperation
	+ Axelrod's idea: hold a computer tournament in which each "contestant" is a program that will play a series of rounds of the Prisoner's Dilemma game
	+ Researchers can send in a program to enter in the tournament: each program will play all the others in a series of about 100 successive rounds of the "PD game"
	+ Some simple Axelrod's Tournament-like strategies:
		+ ***All-Defect*** simply defects on every round
		+ ***Poor-Trusting-Fool*** simply cooperates on every round
		+ ***Random*** is a "test" strategy that simply cooperates or defects randomly
		+ ***Unforgiving*** cooperates initially until the first time that the other player defects; after that, ***Unforgiving*** defects forever
	+ ***The Tit-for-Tat strategy***
		+ ***Tit-for-Tat*** cooperates on the first round. Thereafter, on every subsequent round, it simply imitates what the other player did on the previous round. (That is, Tit-for-Tat does at round N what the other player did at round N-1)
+ Simulating evolation in a PD "World"
	+ Consider a world of "animals", each one playing in a PD tournament against representative rules from the original tournament
	+ Each animal is completely determined by its actions in the PD game. Each animal has a memory of the past three rounds only
	+ Since each round has four possibilities, there are sixty-four responses that each animal must remember. Thus, each animal is essentially determined by a 64-entry table (one entry for each of the possible preceding three-round sets)
	+ It seems, then, that we need sixty-four bits to specify an "animal. To be a bit more precise, since each animal must begin on the first round by making some choice, we include an additional six bits to specify which of the sixty-four table choices we will begin with. Thus, each animal requires seventy bits total
	+ In each generation, a population of our animal plays against the representative rules. The best-scoring of these animal are preferentially allowed to survive to the next genetation
	+ We also include new animals created by "mating" between the successful animals. New animals are derived via crossover (between two animals) and occasional mutations
	+ Rules that evolve in the PD world
		+ ***Dont' rock the boat***: continue to cooperate after three mutual cooperations
		+ ***Be provocable***: defect when the other player defects out of the blue
		+ ***Accept an apology***: continue to cooperate after cooperation has been restored
		+ ***Forget***: cooperate when mutual cooperation has been restored after an exploitation
		+ ***Accept a rut***: defect after three mutual defections

### 3. Game Theory and Evolution
+ Book: Richard Dawkins, The Selfish Gene: a Game Theory-Influenced View of Evolution
	+ Altruism
	+ Kin preference (and other familial relationships)
	+ Sex
	+ Death
+ Two Strategies ("Hawk" and "Dove") for Animals Fighting over a Resource
	+ The resource is woth 50
	+ Injury costs 100
	+ Dove display costs 10
+ Looking for an "Evolutionarily Stable Strategy"
	+ Here, neither "pure hawk" nor "pure dove" is an evolutionaruly stable strategy (or ESS), since each can be successfully invaded by the other
	+ Suppose our population isn't all one or the other, bu instead has (in percentage) P hawks and (1-P) doves. The payoff to a newborn hawk is -25P + 50(1-P). The payoff to a new dove is 0P + (1-P)15. When these are equal, neither strategy is favored. So conceivably our population could stabilize at a percentage P = 35/60 of hawks
+ "Bourgeois Strategy"
	+ means "Play Hawk if you were at the resource ***first***, and dove otherwise"
		|                | Hawk  | Dove | Bourgeois |
		|----------------|-------|------|-----------|
		| ***Hawk***     | -25   | 50   | 12.5      |
		| ***Dove***     | 0     | 15   | 7.5       |
		| ***Bourgeois***| -12.5 | 32.5 | 25        |

### 4. Game Theory and Cognitive Science
+ Book: 
	+ Steven Pinker, How The Mind Works
	+ David J. Buller, Adapting Minds
	+ Jerome H. Barkow et al., The Adapted Mind: Evolution Psychology and the Generation of Culture
	+ Geoffrey Miller, The Mating Mind
	+ Douglas T. Kenrick, Sex, Murder, And The Meaning Of Life
+ Some fundatmental themes in evolutionary cognitive science
	+ Empiricism vs. Rationalism (or "nurture vs. nature"): against the blank slate
	+ Evolutionary reasoning as (sometimes, but not always) teleological
	+ Evolutionary reasoning and its relationship to a broader biological challenge to "classical" cognitive science
+ Complications to "Pure" Teleological Reasoning
	+ Genetic drift
	+ The "environment of evolutionary adaption" (EEA)
	+ Natural selection vs. sexual selection
	+ Cultural vs. genetic effects
+ Evolutionary Psychology: Potential Pitfalls
	+ The problem of "just-so stories"
	+ How to find evidence? And how good is the evidence, anyhow?
	+ Genes and "memes" as alternative (sometimes interwoven) self-reproducing agents
+ Child Cognition and Human Biology
	+ Humans are altricial (as opposed to precocial) animals
	+ Prolonged preiod of juvenility
	+ These factors constrain both child and adult behavior and cognition
+ Why the Blossoming Interest in Infant and Child Cognition?
	+ Laboratory techniques for studying babies
	+ Philosophical reasons
	+ The ambivalent legacy of the computationl metaphor
+ ***Piaget's Account: Major Themes***
	+ A ***zoological*** approach
	+ Viewing development as taking place in thematically coherent stages:
		+ Sensori-motor Stage (< 18 months)
		+ Concrete Operational Stage (< 11 yrs)
		+ Formal Operational Stage
	+ Themes along which development takes place
		+ Object permanence
		+ Egocentrism and "decentering"
		+ Mathematical operations (especially group theory): composition, reversibility/inverses, associativity, identity
		+ Set theoretic notions: inclusion, one-to-one mappings
	+ Movement between stages taking place via an interplay between "accommodation" and "assimilation"
	+ Archetypal experiments (conservation, class inclusion, object permanence)
+ Infants and Objects
	+ Object permanence (reaching studies)
	+ Object conservation (subitizing)
	+ Object undergo unified movement
	+ Continuity of movement
	+ Objects as physical causes of movement of other objects
	+ Linking between tactile and visual perception

### 5. Embodied Cognition
+ Book: 
	+ Richard Menary, The Extended Mind
	+ Shaun Gallagher, How The Body Shapes The Mind
	+ George Lakoff, Mark Johnson, Metaphors We Live By
	+ Andy Clark, Being There
+ Major Themes of Embodied Cognition
	+ Cognition as interwoven with action
	+ Cognition as linked to (and constrained by) the parameters of the physical body
	+ Cognition as a systemic process that may include external tools and artifacts ("extended cognition")
+ From children's cognition to embodied cognition: gesture as an indicator of cognitive development (Goldin-Meadow, Hearning Gesture)
+ The perception of one's own body is surpisingly plastic
+ Cognitive tasks aren't all in the brain
+ Artificial Animals
	+ Book: Valentino Braitenberg, Vehicles: Experiments in Synthetic Psychology
	+ "intelligence Without Representation" (Brooks, 1991)
		+ "We must incrementally build up the capabilities of intelligent systems, having complete systems at each step of the way and thus automatically ensure that the pieces and their interfacesare valid."
		+ "At each step we should build complete intelligent systems that we let loose in the real world with real sensing and real action. Anything less provides a candidate with which we can delude ourselves."
+ An "Unexpected Conclusion" and "Radical Hypothesis"
	+ When we examine very simple level intelligence we find that explicit representations and models of the world simply get in the way. It turns out to be better to use the world as its own model
	+ Representation is the wrong unit of abstraction in building the bulkiest parts of intelligent systems
+ Slogans of the "Brooks Style" of AI Design
	+ "Intelligence without representation"
	+ "The world is its own best representation"
	+ Working on "horizontal" microworlds (a complete creature) as opposed to "vertical" microworlds (a complete task)
	+ A "layered" architecture, often consisting of weakly communicating simple processors
	+ Avoidance of a "central processor", and emergent behaviors
	+ A focus on physical (as opposed to "virtual", or simulated) test cases

***

<br><br>
<br><br>
_This note was created by [**ChuongQuoc1413017**](https://github.com/ChuongQuoc1413017/Note/tree/main/Mind%20and%20Machine%20Specialization)@2022_
