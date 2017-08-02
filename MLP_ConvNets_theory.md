---
layout: default
mathjax: true
permalink: /mlp-convnets-theory/
---

## Multilayer Perceptron and Convolutional Neural Networks - Theory

This document contains the first theoretical part (1/4) of the Deep Learning subject at the Master in Artificial Inteligence of the Universitat Politècnica de Catalunya. It briefly reviews the basic concepts regarding Multilayer Perceptron (MLP) and Convolutional Neural Networks (CNNs).

### A bit of history

Neural networks have recently (i.e., 2010s) become a hot topic for both academia and industry. However, neural networks have been around for a while.

Artificial Neural Networks (ANN) were born in 1943, through a work by Warren McCulloch and Walter Pitts [1]. In their paper, McCulloch and Pitts tried to understand how could the brain compute highly complex behaviors, using processing units as simple as neurons. Their design of single neurons was the first contribution to the field, and included the idea of weighted inputs to produce an output.

<div style="text-align:center"><img src="/figures/mcculloch_fig1.jpg" width="350">
</div>

<div><p style="text-align: center;">Original Figure from McCulloch and Pitts. Source [1].</p></div>

### Rosenblatt's Perceptron

In 1958,Frank Rosenblatt developed the "Perceptron" algorithm [2], which was based on McCulloch and Pitts neurons. The algorithm was a binary classifier, mapping a real valued input to a single binary output.

$$
f(x)= \begin{cases}1\ \ if\ w \cdot x+b>0\\ 0\ otherwise \end{cases}
$$
Where w is is a vector of real-valued weights, · is the dot product, and b is a real scalar constant.

Rosenblatt implemented the algorithm within the machine "Mark I Perceptron", a visual classifier composed by 400 photosensitive receptors (sensory units), associated with 512 stepping motors (association units), and an output of 8 neurons (response units) [3]. It contained only one layer of trainable parameters (association units). For more details see [4,9].

<div style="text-align:center"><img src="/figures/Mark1.png" width="350">
</div>
<p style="text-align: center;">Illustration of the Mark I Perceptron from [3].</p>

Rosenblatt acknolwedged a set of limitations of his Perceptron machine in a series of publications. Minsky and Papert published the book "Perceptrons: an introduction to computational geometry", also detailing some of those limitations. See [6] for more details. The work of Minsky and Papert had a huge impact on the public, although few people actually understood the nature of their contribution. Simply put, Minsky and Papert argue that a multilayer network (or MLP) is needed for learning certain basic functions such as XOR, and that no appropriate training algorithm existed for that kind of network.
Regardless of the technical aspects of Misnky and Papert's work, the reaction from the public was a drastic cut in funding on ANN during the 70s, until the mid 80s, in what is knows as the "AI Winter". After ANNs were almost abandoned, AI research focused on "expert systems" instead, which would also suffer their own "AI Winter" in the 90s.

### Backpropagation and Stochastic Gradient Descent

The backpropagation algorithm reignited the interest on ANN. Originally intended for ANN by Webos in 1974 [7], it gained attention when rediscovered by Rumelhart, Hinton and Williams in 1985 [8], and effectively finished the "AI Winter" on ANN.
Simply put, the backpropagation algorithm is based on the chain rule, which allows to compute the derivative of previous layers, and thus addapt the weights of those layers as well. By doing this process iteratively, we can eventually optimize the weights of all layers in a MLP. Originally, the change in the weights was computed using an optimization algorithm called Stochastic Gradient Descent (SGD). See [10] for a full mathematical explanation of the backprop algorithm.

With a new training methodology, research on ANN became active again. LeCun et. al. [11] developed a digit recognition system using data from the US Postal Service, and showed how ANN could be used to solve complex practical problems. LeCun system included a layer of convolutional neurons, which had been previously proposed by Fukushima in 1980 [12].

### Convolutional Neural Networks

Convolutional Neural Networks (CNN) are based on a special type of neuron: convolutional neurons. Typically, convolutional neurons have a limited input, e.g., are only connected with a few neurons from the previous layer. Conv neurons assume the existence of a two-dimensional structure in the data, 

Convolutional neurons implement the concept of "weight sharing", as several neurons of the same layer are defined by a common set of weights.


## Bibliography

[1] McCulloch, Warren S., and Walter Pitts. "A logical calculus of the ideas immanent in nervous activity." The bulletin of mathematical biophysics 5.4 (1943): 115-133.](http://vordenker.de/ggphilosophy/mcculloch_a-logical-calculus.pdf)

[2] [Rosenblatt, Frank. "The perceptron: A probabilistic model for information storage and organization in the brain." Psychological review 65.6 (1958): 386](http://www-public.tem-tsp.eu/~gibson/Teaching/Teaching-ReadingMaterial/Rosenblatt58.pdf)

[3] [Mark I Perceptron Operators' Manual](http://www.dtic.mil/dtic/tr/fulltext/u2/236965.pdf)

[4] [Kurzweil, Ray. How to create a mind: The secret of human thought revealed. Penguin, 2013.]

[5] [Misky, M., and S. Papert. "Perceptrons: an introduction to computational geometry." (1969).]

[6] [https://en.wikipedia.org/wiki/Perceptrons_(book)](https://en.wikipedia.org/wiki/Perceptrons_(book))

[7] [Werbos, Paul John. "Beyond regression: New tools for prediction and analysis in the behavioral sciences." Doctoral Dissertation, Applied Mathematics, Harvard University (1974)]()

[8] [Rumelhart, David E., Geoffrey E. Hinton, and Ronald J. Williams. Learning internal representations by error propagation. No. ICS-8506. California Univ San Diego La Jolla Inst for Cognitive Science, 1985.](http://www.dtic.mil/get-tr-doc/pdf?AD=ADA164453)

[9] [http://www.andreykurenkov.com/writing/a-brief-history-of-neural-nets-and-deep-learning/](http://www.andreykurenkov.com/writing/a-brief-history-of-neural-nets-and-deep-learning/)

[10] [http://neuralnetworksanddeeplearning.com/chap2.html](http://neuralnetworksanddeeplearning.com/chap2.html)

[11] [LeCun, Yann, et al. "Backpropagation applied to handwritten zip code recognition." Neural computation 1.4 (1989): 541-551.](http://www.ics.uci.edu/~welling/teaching/273ASpring09/lecun-89e.pdf)

[12] [Fukushima, Kunihiko. "Neocognitron: A hierarchical neural network capable of visual pattern recognition." Neural networks 1.2 (1988): 119-130.](https://pdfs.semanticscholar.org/c85e/6878f2048d0ec9d7186e3f20592c543635dd.pdf)
