---
title: "How Recurrent & LSTM Networks Work"
date: 2022-12-01
tags:
- cs461
- video
- cs461-final
---

[YouTube Link](https://www.youtube.com/watch?v=WCUNPb-5EYI)

# Overview

* good for sequential data

# LSTM

A Long Short-Term Memory (LSTM) network is similar to a recurrent neural network (RNN) but with a memory function.

1. New information vectors are passed into main RNN, we make predictions on them
2. Predictions are passed through a gate, some are forgot
3. An *entirely separate neural network* sits in the middle ==learning what to forget and when!==
4. Yet another NN keeps track of *selection*
5. *Attention mechanism* lets things that aren't immediately relevant be set aside so they don't cloud predictions in memory going forward
	* has its own neural network, logistic function, and squashing function


* LSTMs can make negative predictions as well
	* "I just saw the word 'Doug', I probably won't see it again right away, -1 point"

# Summary
* LSTMs can represent *sequential* patterns well.
	* text, speech, audio, video, physical processes
	* basically, ==anything embedded in time==
* 