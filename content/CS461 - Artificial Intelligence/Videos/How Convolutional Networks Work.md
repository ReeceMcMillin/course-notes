---
title: "How Convolutional Networks Work"
date: 2022-12-01
link: 
tags:
- cs461
- video
- cs461-final
---

[YouTube Link](https://www.youtube.com/watch?v=FmpDIaiMIeA)

* Convolutional networks are multilayer networks
	* first layer catches edges
	* second layer catches things with more structure, e.g. facial features
	* progressively more from there
* well-suited for grid-like structures
1. filtering
	* filters are small matrices of numbers used to represent features
2. layering
	* one image becomes a stack of *filtered* images
3. pooling
	* idea: similar to filtering, take a little window and move by some *stride* across your image
	* max pooling steps:
		1. pick a window size (usually 2 or 3)
		2. pick a stride (usually 2)
		3. walk your window across your filtered images
		4. from each window, take the *maximum* value
	* pooling makes it *much* easier to 
	* pooling doesn't care *where* in the window the maximum value occurs, which increases its resilience to specific pixel positions
	* So we do max pooling with our *entire stack* of filtered images (layer)
4. Normalization
	* ReLU is common - clip negative values to 0, retain positive values

Once we've got these component pieces, we *stack* layers such that the output of one becomes the input to the next.

Fully connected layer
* every value gets a vote on what the final value is going to be
* vote depends on how strongly a value predicts X or O

> [!NOTE] Idea
> 
> In a fully connected layer, a list of ==feature values== becomes a list of ==votes==.

> [!QUESTION] Question
> 
> Where do the *features* come from?
> 
> 


# Backpropagation

Convolutional neural networks use backpropagation

# Hyperparameters

* Convolution
	* Number of features
	* Size of features
* Pooling
	* Window size
	* Window stride
* Fully Connected
	* Number of neurons

# Limitations

CNNs only capture local "spatial" patterns in data.
* rule of thumb: if you can swap columns 