# Data Science Cheatsheets

## Purpose of This Repository
This repository serves two main purposes:
1. Help Data Science Practitioners Prepare for Interviews.
2. Introduce Data Science Concepts to Beginners.

Categories:
* [Stanford Materials](#stanford-materials)
* [Statistics and Probability](#statistics-and-probability)
* [Machine Learning Concepts](#machine-learning-concepts)
* [Deep Learning Concepts](#deep-learning-concepts)
* [Natural Language Processing](#natural-language-processing)

## Stanford Materials
The Stanford cheatsheets are collected from [Sherivine Amidi's teaching Material](https://stanford.edu/~shervine/teaching/)
* [CS221 - Artificial Intelligence](https://github.com/Adity-star/Data-Science-Work/tree/main/CheatSheets/Stanford-CS221%20Artifical%20Intelligence)
* [CS229 - Machine Learning](https://github.com/Adity-star/Data-Science-Work/tree/main/CheatSheets/Standford-CS229%20Machine%20Learning)
* [CS230 - Deep Learning](https://github.com/Adity-star/Data-Science-Work/tree/main/CheatSheets/Standford-CS230%20Deep%20Learning)

## Statistics and Probability
* [Probability Cheatsheet](https://github.com/Adity-star/Data-Science-Work/blob/main/CheatSheets/probability_cheatsheet.pdf)
* [Statistics Cheatsheet](https://github.com/Adity-star/Data-Science-Work/blob/main/CheatSheets/stats_cheatsheet.pdf)
* [Probability Distributions](#probability-distributions)
* [Central Limit Theorem](#central-limit-theorem)
* [Hypothesis Test](#hypothesis-test)

### Probability Distributions
Types of Probability Distributions:
1. [Discrete Probability Distributions](#discrete-probability-distributions)
   * [Bernoulli Distribution](#bernoulli-distribution)
   * [Binomial Distribution](#binomial-distribution)
   * [Poisson Distribution](#poisson-distribution)
2. [Continuous Probability Distributions](#continuous-probability-distributions)
   * [Uniform Distribution](#uniform-distribution)
   * [Normal (Gaussian) Distribution](#normal-gaussian-distribution)
   * [Exponential Distribution](#exponential-distribution)
   * [Student’s t-Distribution](#students-t-distribution)
   * [Log-Normal Distribution](#log-normal-distribution)
   * [Pareto Distribution](#pareto-distribution)

### Discrete Probability Distributions
#### Bernoulli Distribution
* The **Bernoulli distribution** is a discrete probability distribution of a random variable that has exactly two possible outcomes, usually labeled as success and failure. It is a special case of the binomial distribution where the number of trials is one.
  
* **Key Characteristics** of the Bernoulli Distribution:
  - Two outcomes: Typically represented as 1 (success) and 0 (failure).
  - **Parameter** \( p \): The probability of success (i.e., \( P(X=1) = p \)).
  - The probability of failure is \( 1 - p \) (i.e., \( P(X=0) = 1 - p \)).

* **Formula**:
  - Probability mass function (PMF):
    \[
    P(X = x) = p^x (1 - p)^{1-x}
    \]
    where \( x \in \{0, 1\} \).
  
* **Example**:
  - A coin toss: Heads = 1 (success), Tails = 0 (failure), with \( p = 0.5 \) for a fair coin.

* **Properties**:
  - **Mean** (Expected Value): \( \mu = p \)
  - **Variance**: \( \sigma^2 = p(1 - p) \)
