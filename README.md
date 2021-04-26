# Sequence to sequence learning for performing number addition
* **Author:** Smerity and others
* **Date created:** 2015/08/17
* **Last modified:** 2020/04/17
* **Description:** A model that learns to add strings of numbers, e.g. "535+61" -> "596".
* **Source:** https://keras.io/examples/nlp/addition_rnn/


In this example, we train a model to learn to add two numbers, provided as strings.

## Example

    Input: "535+61"
    Output: "596"

Input may optionally be reversed, which was shown to increase performance in many tasks in: Learning to Execute and [Sequence to Sequence Learning with Neural Networks](

http://papers.nips.cc/paper/5346-sequence-to-sequence-learning-with-neural-networks.pdf)

Theoretically, sequence order inversion introduces shorter term dependencies between source and target for this problem.

## Results:

For two digits (reversed):

* One layer LSTM (128 HN), 5k training examples = 99% train/test accuracy in 55 epochs

Three digits (reversed):

* One layer LSTM (128 HN), 50k training examples = 99% train/test accuracy in 100 epochs

Four digits (reversed):

* One layer LSTM (128 HN), 400k training examples = 99% train/test accuracy in 20 epochs

Five digits (reversed):

* One layer LSTM (128 HN), 550k training examples = 99% train/test accuracy in 30 epochs
