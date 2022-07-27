# Neural Networks Learning 

Based on the mechanism of artificial neurons, neural networks use multiple layers of artificial neurons to process complicated inputs and learn. 

An example of this could a dog. The dog could be trained in its feeding habits through alarming its neurons. 

A Training dataset has: 

- An input 
- Expected result 

Using this training dataset, the error can be calculated for each output and hidden node. 

The error can then be used to adjust the corresponding weights of the node: 

- wi,j = wi,j + p * E * ii
  - Who knows what this means. 

  A number of ways have been developed for error propagation.

Refer to the first diagram on this page.

## Implementation varients 

Based on the idea of using a number of layers with different numbers of neurons as well as the propagation function calculation, there are many implementations and variants. 

They have different number of layers where each layer has different number of nodes. 

The layers are connected differently and the neurons are implemented differently. 

input layer ==> Multiple Hidden Layers ===> Output layer.