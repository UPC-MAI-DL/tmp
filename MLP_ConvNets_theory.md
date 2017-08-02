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

Original Figure from McCulloch and Pitts. Source [1].
</div>

In 1958,Frank Rosenblatt developed the "Perceptron" algorithm [2], which was based on McCulloch and Pitts neurons. The algorithm was a binary classifier, mapping a real valued input to a single binary output.

$$
Add the formula here
f(x)=
$$

He implemented the algorithm within the machine "Mark I Perceptron", a visual classifier composed by 400 photosensitive receptors (sensory units), associated with 512 stepping motors (association units), and an output of 8 neurons (response units) [3].

<div style="text-align:center"><img src="/figures/Mark1.png" width="350">

Illustration of the Mark I Perceptron from [3].
</div>


## Bibliography

[1] [McCulloch, Warren S., and Walter Pitts. "A logical calculus of the ideas immanent in nervous activity." The bulletin of mathematical biophysics 5.4 (1943): 115-133.](http://vordenker.de/ggphilosophy/mcculloch_a-logical-calculus.pdf)

[2] [Rosenblatt, Frank. "The perceptron: A probabilistic model for information storage and organization in the brain." Psychological review 65.6 (1958): 386](http://www-public.tem-tsp.eu/~gibson/Teaching/Teaching-ReadingMaterial/Rosenblatt58.pdf)

[3] [Mark I Perceptron Operators' Manual](http://www.dtic.mil/dtic/tr/fulltext/u2/236965.pdf)
