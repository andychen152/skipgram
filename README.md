# skipgram

In the first part of the assignment, you will need to implement the Skipgram model from Word2Vec.
Recall that the Skipgram model that we covered in class: the main idea is to use the target word to
predict the context word. More specifically, we use a one-hot input vector and a input embedding
matrix to find the target hidden word embedding. Then, we use a softmax function to predict a
probabilistic distribution over the context output words.
Given the input text such as: “the quick brown fox jumped over the lazy dog”. You will need to
generate the training instances in the form of (quick, the), (quick, brown), (brown, quick), (brown,
fox), .... Note that in addition to the positive training examples, you will also need to sample
words to form negative examples, for example (he, the).
You will need to implement a Stochastic Gradient Descent algorithm (https://en.wikipedia.
org/wiki/Stochastic_gradient_descent) to optimize the word embeddings for this problem.
Remember that we have already derived the gradient updates for you in class: all you need to do,
is to randomly initialize the target word embeddings, perform multiple passes over the dataset,
set up a convergence criteria (e.g., the delta in negative log-likelihood), and select appropriate
adaptive learning rates.
For the full description of the Skipgram model, please refer to Mikolov et al., 20131 and our
lecture slides on the Piazza resource page.
