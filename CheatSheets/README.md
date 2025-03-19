# Data Science Cheatsheets

## Purpose of This Repository
This repository serves two main purposes:
1. Help Data Science Practitioners Prepare for Interviews.
2. Introduce Data Science Concepts to Beginners.

Categories:
* [Stanford Materials](#standford-materials)
* [Statistics and Probability](#stastics-and-probability)
* [Machine Learning Concepts]
* [Deep Learning Concepts]
* [Natural Language Processing]

## Stanford Materials
The Stanford cheatsheets are collected from [Sherivine Amidi's teaching Material](https://stanford.edu/~shervine/teaching/)
* [CS221 - Artificial Intelligence](https://github.com/Adity-star/Data-Science-Work/tree/main/CheatSheets/Stanford-CS221%20Artifical%20Intelligence)
* [CS229 - Machine Learning](https://github.com/Adity-star/Data-Science-Work/tree/main/CheatSheets/Standford-CS229%20Machine%20Learning)
* [CS230 - Deep Learning](https://github.com/Adity-star/Data-Science-Work/tree/main/CheatSheets/Standford-CS230%20Deep%20Learning)

## Statistics and Probability
* [Probability Cheatsheet](https://github.com/Adity-star/Data-Science-Work/blob/main/CheatSheets/probability_cheatsheet.pdf)
* [Statistics Cheatsheet](https://github.com/Adity-star/Data-Science-Work/blob/main/CheatSheets/stats_cheatsheet.pdf)
* [Probability Distributions](#probability-distributions)
* [Central Limit Theorem]
* [ hypothesis test]

## Probability Distributions
Types of  Probability Distributions
1. Discrete Probability Distributions(#discrete-probability-dictributions)
  * Bernoulli Distribution
  * Binomial Distribution
  * Poisson Distribution
2. Continuous Probability Distributions
  * Uniform Distribution
  * Normal (Gaussian) Distribution
  * Exponential Distribution
  * Student’s t-Distribution
  * Log-Normal Distribution
  * Pareto Distribution

Lets Start one by one
1. Discrete Probability Distributions
a. bernouli Distributions
* The Bernoulli distribution is a discrete probability distribution of a random variable that has exactly two possible outcomes, usually labeled as success and failure. It is a special case of the binomial distribution where the number of trials is one.
* Key Characteristics of the Bernoulli Distribution:
Two outcomes: Typically represented as 1 (success) and 0 (failure).
Parameter 
𝑝
p: The probability of success (i.e., 
𝑃
(
𝑋
=
1
)
=
𝑝
P(X=1)=p).
The probability of failure is 
1
−
𝑝
1−p (i.e., 
𝑃
(
𝑋
=
0
)
=
1
−
𝑝
P(X=0)=1−p).
* Formula:

  * Probability mass function (PMF):
𝑃
(
𝑋
=
𝑥
)
=
𝑝
𝑥
(
1
−
𝑝
)
1
−
𝑥
P(X=x)=p 
x
 (1−p) 
1−x
 
where 
𝑥
∈
{
0
,
1
}
x∈{0,1}.
* Example:

   * A coin toss: Heads = 1 (success), Tails = 0 (failure), with 
𝑝
=
0.5
p=0.5 for a fair coin.
* Properties:

  * Mean (Expected Value): 
𝜇
=
𝑝
μ=p
  * Variance: 
𝜎
2
=
𝑝
(
1
−
𝑝
)
σ 
2
 =p(1−p)


  
