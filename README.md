# Titanic competition
This repository contains a solution for the Kaggle dataset Titanic using logistic regression. The project aims to predict the survival of passengers on the Titanic based on various features such as age, gender, and class. 

## Brief overview 
### The Challenge

The sinking of the Titanic is one of the most infamous shipwrecks in history.

On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew.

While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

In this challenge, I am asked to build a predictive model that answers the question: “what sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).

### What Data Will I Use in This Competition?

In this competition, I’ll gain access to two similar datasets that include passenger information like name, age, gender, socio-economic class, etc. One dataset is titled train.csv and the other is titled test.csv.

**Train.csv** will contain the details of a subset of the passengers on board (891 to be exact) and importantly, will reveal whether they survived or not, also known as the “ground truth”.

The **test.csv** dataset contains similar information but does not disclose the “ground truth” for each passenger. 

#### Formalized Task

When choosing an algorithm for the problem of predicting a survivor on the Titanic, we will be guided by the principle of model interpretability. This means that we will choose algorithms that make it easy to understand which factors influence survival prediction and how much.

For example, linear regression is one of the most interpretable algorithms, as it allows you to evaluate the impact of each of the factors on survival. If we see that simplifying the model to linear regression does not lead to a significant deterioration in the results, then we will use this algorithm.

However, if we see that simplifying the model to linear regression leads to a significant deterioration in the results, then we will use more complex algorithms, such as gradient boosting or neural networks. At the same time, we will take into account that the results of these algorithms may be less interpretable and require additional analysis and verification before making decisions based on these results.

Thus, when choosing an algorithm for a problem, we will pay special attention to the interpretability of the model and use more complex algorithms only if simplifying the model leads to worse results.

Thus, the formalized task at the first stage of the primary model selection is as follows:

**Model** with k features:
$$a(x) = w_0 + w_1x^1 + \dots w_kx^k = \langle w, x \rangle,\\x = (1, x^1, \dots, x^k)$$

At the same time, we understand that life/death assessment is a binary category. Thus, to solve the problem, we will use **logistic regression**, which is a special case of generalized linear regression

We will teach a linear model to correctly predict some object associated with a probability, but with a range of values $$(\infty; -\infty),$$ 

and convert the model's responses to a probability. Such an object is **logit** or **log odds** — the logarithm of the ratio of the probability of a positive event to a negative one $$\log(\frac{p}{1-p}).$$

For further analysis, we will use the sigmoid $$p = \sigma(\langle w, x \rangle)$$

The assumptions of logistic regression are almost identical to those for linear regression:

1. the dependent variable must be binary, usually encoded as zero and one;
2. independence of observations from each other;
3. lack of multicollinearity;
4. sufficient sample size (at least thirty observations);
5. no outliers.

## Results
My score is - 0.77272
