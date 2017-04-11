---
layout: post
title: Introduction
---
Probabilistic graphical modeling is a branch of machine learning that studies how to use probability distributions to describe the world and to make useful predictions about it.

### Representation

How do we express a probability distribution that models some real-world phenomenon? This is not a trivial problem: we have seen that a naive model for classifying spam messages with $$n$$ possible words requires us in general to specify $$O(2^n)$$ parameters. We will address this difficulty via general techniques for constructing tractable models. These recipes will make heavy use of graph theory; probabilities will be described by graphs whose properties (e.g. connectivity, tree-width) will reveal probabilistic and algorithmic features of the model (e.g., independence, learning complexity).

### Inference

Given a probabilistic model, how do we obtain answers to relevant questions about the world? Such questions often reduce to querying the marginal or conditional probabilities of certain events of interest. More concretely, we will be typically interested in asking the system two types of questions:

- *Marginal inference*: what is the probability of a given variable in our model after we sum everything else out?
{% math %}
p(x_1) = \sum_{x_2} \sum_{x_3}  \cdots \sum_{x_n} p(x_1, x_2, ..., x_n).
{% endmath %}
An example query would be to determine the probability that a random house has more than three bedrooms.

- *Maximum a posteriori (MAP) inference* asks for the most likely assignment of variables. For example, we may try to determine the most likely spam message, solving the problem
{% math %}
\max_{x_1, \dots, x_n} p(x_1,...,x_n, y=1)
{% endmath %}

Often our queries will involve evidence (like in the MAP example above), in which case we will fix the assignment of a subset of the variables.

It turns out that inference is a very challenging task. For many probabilities of interest, it will be NP-hard to answer any of these questions. Crucially, whether inference is tractable will depend on the structure of the graph that describes that probability! If a problem is intractable, we will still be able to obtain useful answers via approximate inference methods. Interestingly, algorithms described in this part of the course will be heavily based on work done in the statistical physics community in the mid-20th century.

### Learning

Our last key task refers to fitting a model to a dataset, which could be for example a large number of labeled examples of spam. By looking at the data, we can infer useful patterns (e.g. which words are found more frequently in spam emails), which we can then use to make predictions about the future. However, we will see that learning and inference are also inherently linked in a more subtle way, since inference will turn out to be a key subroutine that we will repeatedly call within learning algorithms. Also, the topic of learning will feature important connections to the field of computational learning theory --- which deals with questions such as generalization from limited data and overfitting --- as well as to Bayesian statistics --- which tells us (among other things) about how to combine prior knowledge and observed evidence in a principled way.