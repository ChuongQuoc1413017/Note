## Computational Vision

### Table of contents
* [1. Vision as a Computational Problem](#1-Vision-as-a-Computational-Problem) 
* [2. Edge Detection Depth Perception Object Recognition](#2-Edge-Detection-Depth-Perception-Object-Recognition)
* [3. The Turn Towards Neuroscience](#3-The-Turn-Towards-Neuroscience)
* [4. Perceptrons](#4-Perceptrons)

### 1. Vision as a Computational Problem
+ The eye is like a pinhole camera
+ "Solving" the vision problem is mathematically impossible
+ Illusions can tell us something about the computational side of human vision
+ Let's try to make a first (approximate) statement of the "vision problem"

### 2. Edge Detection Depth Perception Object Recognition
+ ***Edge detection***
	+ As a first step, we'd like to find the edges in an image (the boundaries of the three-dimensional objects that we hope to identify)
	+ It's hard to identify an object if you can't determine its edges
	+ ***Convolution*** is a signal-processing technique that can be used to identify edges in an image
	+ In machine vision, we convolve the image with a "sombrero function"
	+ Every single pixel in the image is convolved with a sombrero function; "zero crossings" of the resulting image correspond to edges
	+ Convolution can be "tuned" to coarser or finer scales
	+ ***Human vision includes an approximate convolution step as well***
+ ***Depth Perception***
	+ Using two eyes to determine distance
	+ Let's begin with a question: how do you know using just your eyes, how far (from you) an object is?
		+ Size of objects
		+ Movement of objects
	+ Using geometry to determine distance
+ ***Object Recognition***
	+ Identifying objects as collections of "Geons"
	+ What object-recognizing phenomena do geons not explain?

### 3. The Turn Towards Neuroscience
+ ***Mental Imagery***: a watershed debate in the cognitive sciences
	+ "The nature of memory and its process has now been explained as the persistent possession of an image, in the sense of a copy of the thing to which the image refers..." - Aristotle, On Memory and Recollection
	+ "... after the object is removed or the eye shut, we still retain an image of the thing seen, though more obscure than when we see it." - Thomas Hobbes, Leviathan
	+ "... The ideas of the nurse and mother are well framed in their [children's] minds; and, like pictures of them, represent only those individuals." - John Locke, Essay Concerning Human Understanding
	+ Albert Einstein, in a letter to J. Hadamard (in Hadamard, The Psychology of Invention in the Mathematical Field [1949])
	+ E. Ferguson, Engineering and the Mind's Eye (1992)
+ Some immediate questions about imagery
	+ Indistinctness: the tiger example
	+ Difficulty of reinterpretation: the "ambiguous figure" example
	+ Difficulty of re-examination: the "Star of David" example
	+ The homunculus objection
+ Summing up the experiments...
	+ Certain types of operations may be performed on mental images:
		+ Rotation (Shepard/Metzler)
		+ Scanning (Kosslyn, Ball, and Reiser)
	+ Mental imagery seems to recreate some effects...
		+ Ponzo illusion
		+ McCollough effect
		+ Resolution (Finke experiment)
	+ But not others
		+ Ambiguous figures
		+ Finding "part" of figures
+ Some problems with the ***Pictorial*** Model of Mental Imagery
	+ Introspection is an insufficient guide 
	+ "Hidden" knowledge (e.g., direction to scan)
	+ Background knowledge (Pylyshyn's "cognitive impenetrability")
	+ The "parsimony" argument
	+ Mental imagery seems to do too much
	+ Mental imagery doesn't do enough (Hinton's example)
+ Things that Kosslyn's model accounts for...
	+ Imagery is effortful (because "top-down" connections to visual cortex are weaker and fade quickly)
	+ Imagery is accompanied by semantics and perceptual organization
	+ Differential effects of imagery in (e.g.) color, shape, motion
	+ Clinical evidence (e.g., hemispheric inattention)
+ ***Methods in Cognitive Meuroscience*** (a Sampler):
	+ 1. Clinical Evidence
	+ 2. Animal Experiments
	+ 3. Measuring, or Affecting, Brain Activity
	+ 4. Cognitive Psychology Experiments in the Lab
	+ 5. Computer Simulations (Neural Networks)

### 4. Perceptrons
+ ***Neural Networks***: Some First Concepts
	+ Each neural element is loosely based on the structure of neurons
	+ A neural net is a collection of neural elements connected by weighted links
	+ We think of some set of neurons as "input elements"; these are linked to "output elements" which can be interpreted as a classification of the input pattern
	+ Standard formats: perceptrons and multilayer feedforward networks
+ Structure of an (artificial) neuron
	+ Think of each neuron as a very simple computational element: it receives numeric input values, sums those values, and compares them to a threshold
	+ If the sum of the inputs is greater than the threshold, the neuron outputs a 1; otherwise it outputs a 0
	+ The output of this neuron is connected (as usual, via weighted links) to subsequent neurons in the net
+ Training a Perceptron by Adjusting its Weights
	+ Overall error is the value of the difference between what we wanted and what we got from our perceptron. (In some situations we use the "squared" error to avoid issues of sign.)
	+ Once we see that our perceptron is in error, we can adjust each of the weights leading to the output node. We'll adjust each weight in such a way as to make the error value smaller
+ Adjusting an Edge Weight in a Perceptron
	+ To update the weight from a node j leading to an output node, we adjust the weight according to the following formula:
		+ W_j <--- W_j + (alpha Err out'(in) x_j)
	+ Here:
		+ Err is the difference between what we wanted and what we got from the output. (i.e., the "un-squared" error)
		+ out'(in) is the derivative or our output function
		+ x_j is the output from node j leading to us
		+ alpha is a "rate parameter"
+ Side Issue: The Derivative of the Output Function of a Neuron
	+ A handy choice for output function of a neuron is a sigmoidal function. Let's call "x" in this case the sum of all the inputs. Then for a sigmoidal function:
		+ out(x) = 1/(1+e^(-x))
	+ If we use the sigmoidal function out(x), then
		+ out'(x) = out(x)(1-out(x))
+ ***Multi-Layer Networks***:
+ Now, we expand our network architecture so that it has several (or more) layers of neural elements. We think of the layers as numbered in columns left to right, with the leftmost layer as "layer 1" (input) and the rightmost layer as "layer n" (output)
+ Adjusting Weight for Multilayer Networks
	+ Here's thhe perceptron rule, again:
		+ W_j <--- W_j + (alpha Err out'(in) x_j)
	+ Note that this is the update rule to adjust a weight from neuron j to an output neuron. Let's rewrite this for our new multilayer network as:
		+ W_(j->k) <--- W_(j->k) + (alpha delta_k a_j)
	+ That is, we call the output neuron k and we combine the error term and the derivative-at-k term into one symbol, delta. We also relabel the output coming from neuron j as a_j. Think of the delta term as "how much node k wants its output to change". For an output node, this is just the product of the error at k and the rate at which error changes for a small change in input at k
+ How much does a hidden node want to change its output?
	+ What should its value of delta be?
+ Backpropagation, Final Step: Adjusting Weights
	+ We now have, for each node, a measure of how much that node wishes to change its own output value. We now adjust the weights on each edge as follows:
	+ W_(j->i) <--- W_(j->i) + (alpha delta_i a_j)
+ A Samlper of Additional Issues
	+ How do we choose an appropriate network size to train? Too small a network, and we may not be able to represent our concept; too big, and we run the risk of overfitting
	+ How do we choose a training rate parameter? (The notion of "simulated annealing")
	+ Training partial nets
+ An Example of Deep Learning: Object Recognition
	+ Neural networks beyond the "Hidden Layer": an example in image processing
	+ What is a "Convolution" step?
		+ Let's think about a "2D convolution". The idea is that we take a single pixel location; look at the pixel in a neighborhood around (and including) that location; and replace the original pixel value with a weighted sum of the pixel values in the neighborhood
			+ Now, think about what this "convolution" step is doing here. It's actually very like a perceptron, isn't it?
			+ We take nine inputs (the pixels in the yellow area)...
			+ Multiply their values by "weight edges" (the filter values written in small numbers in the yellow area)...
			+ And output the sum (we don't even bother with a "threshold" step)
		+ What about the weights in the filter? How do we get those?...
			+ The weight in the yellow area could come from a perceptron trained to look for particular features (like, say, the upper area of a face, or the bottom left portion of a handwritten capital "G"
			+ In other words, we could first train a 3x3 perceptron on a set of images corresponding to a particular type of "feature" that we want to notice; then use the weights from that trained perceptron as the filter weights for a convoltuion step. The result will correspond to the "amount" of that feature we notice at each pixel
			+ The easiest sort of pooling is just to take the maximum value in asmall region. In this example, we're using pooling to cut the size of the data set by a factor of four
		+ After we do this a couple of times, we have multiple condensed pictures, each corresponding to an examination of the original picture for particular features. We now feed this data to a complete feed-forward net that takes, as input, sets of feature maps and outputs responses corresponding to (say) objects of interest
	+ One particular type of visual convolution filter looks for edges...
		+ Input Image -> Convolution Kernel -> Feature Map
+ ***Is Deep Learning the "Sercret" to AI?***

***

<br><br>
<br><br>
_This note was created by [**ChuongQuoc1413017**](https://github.com/ChuongQuoc1413017/Note/tree/main/Mind%20and%20Machine%20Specialization)@2022_
