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
* [Supervised Algorithms](#supervised-algorithms)
* [Unsupervised Algorithms](#unsupervised-algorithms)
* [Natural Language Processing](#natural-language-processing)

---

## Stanford Materials
The Stanford cheatsheets are collected from [Sherivine Amidi's teaching Material](https://stanford.edu/~shervine/teaching/)
* [CS221 - Artificial Intelligence](https://github.com/Adity-star/Data-Science-Work/tree/main/CheatSheets/Stanford-CS221%20Artifical%20Intelligence)
* [CS229 - Machine Learning](https://github.com/Adity-star/Data-Science-Work/tree/main/CheatSheets/Standford-CS229%20Machine%20Learning)
* [CS230 - Deep Learning](https://github.com/Adity-star/Data-Science-Work/tree/main/CheatSheets/Standford-CS230%20Deep%20Learning)

[Back to Top](#data-science-cheatsheets)
---

## Statistics and Probability
* [Measures of central tendency](#measure-of-central-tendency)
* [Important Terms](#important-terms)
* [Probability Cheatsheet](https://github.com/Adity-star/Data-Science-Work/blob/main/CheatSheets/probability_cheatsheet.pdf)
* [Statistics Cheatsheet](https://github.com/Adity-star/Data-Science-Work/blob/main/CheatSheets/stats_cheatsheet.pdf)
* [Probability Funcations](#probability-funcations)
* [Skewness and Kurtosis](#skewness-and-kurtosis)
* [Probability Distributions](#probability-distributions)
* [Central Limit Theorem](#central-limit-theorem)
* [Hypothesis Test](#hypothesis-test)
* [Complete Statistics Notebook](#complete-statistics-notebook)

[Back to Top](#data-science-cheatsheets)
---

## Measure of central Tendency
### 1. Mean (Arithmetic Mean)

**Definition**: The mean is the sum of all the data points divided by the number of data points. It gives the average value of the data.  
**Formula**:  
\[
\text{Mean} = \frac{\sum_{i=1}^{n} x_i}{n}
\]
where \( x_i \) is each data point and \( n \) is the total number of data points.

---

### 2. Median

**Definition**: The median is the middle value when the data points are sorted in ascending (or descending) order. If the dataset has an even number of observations, the median is the average of the two middle values.

**Formula**:
- If the dataset has an odd number of data points, the median is the value at position \( \frac{n+1}{2} \).
- If the dataset has an even number of data points, the median is the average of the values at positions \( \frac{n}{2} \) and \( \left( \frac{n}{2} + 1 \right) \).

---

### 3. Mode

**Definition**: The mode is the value that appears most frequently in the dataset. A dataset may have no mode, one mode, or more than one mode (bimodal, multimodal).

[Back to Statistics and Probability](#statistics-and-probability)

---
### Important Terms
### 1. Quantile

**Definition**: A quantile is a value that divides a dataset into intervals with a specific number of data points. The most common quantiles are quartiles, quintiles, and percentiles. Quantiles give us insights into the distribution of data. For example, the median is the 2nd quartile (Q2).

**Formula**:  
The \( p \)-th quantile \( Q_p \) is the value below which a fraction \( p \) of the data falls:
\[
Q_p = \text{Value at position} \left( p \times (n + 1) \right)
\]
where \( p \) is the fraction of data points below the quantile, and \( n \) is the total number of data points.

---

### 2. Percentile

**Definition**: A percentile is a specific type of quantile that divides the dataset into 100 equal parts. The \( p \)-th percentile corresponds to the value below which \( p \) percent of the data lies.

**Formula**:  
The \( p \)-th percentile is calculated as:
\[
P_p = \text{Value at position} \left( \frac{p}{100} \times (n + 1) \right)
\]
where \( p \) is the percentile and \( n \) is the total number of data points.

**Example**:  
For the 25th percentile (also known as the 1st quartile), we calculate \( P_{25} \).

---

### 3. Interquartile Range (IQR)

**Definition**: The Interquartile Range (IQR) is a measure of statistical dispersion, or how spread out the data is. It is the difference between the 75th percentile (Q3) and the 25th percentile (Q1). The IQR is used to identify outliers in the dataset.

**Formula**:  
\[
\text{IQR} = Q_3 - Q_1
\]
where:
- \( Q_1 \) is the 25th percentile (1st quartile),
- \( Q_3 \) is the 75th percentile (3rd quartile).

**Usage**:  
The IQR is commonly used to detect outliers. Any data point that lies below \( Q_1 - 1.5 \times \text{IQR} \) or above \( Q_3 + 1.5 \times \text{IQR} \) is often considered an outlier.

---

### Summary of Key Terms:

| **Term**             | **Definition**                                               | **Formula**                                                 |
|----------------------|--------------------------------------------------------------|-------------------------------------------------------------|
| **Quantile**         | Divides data into equal intervals. Quantiles can be any fraction (e.g., quartiles, quintiles). | \( Q_p = \text{Value at position} \left( p \times (n + 1) \right) \) |
| **Percentile**       | A specific quantile dividing data into 100 equal parts.      | \( P_p = \text{Value at position} \left( \frac{p}{100} \times (n + 1) \right) \) |
| **Interquartile Range (IQR)** | The range between the 25th and 75th percentiles, representing the spread of the middle 50% of the data. | \( \text{IQR} = Q_3 - Q_1 \)                                  |

---

### When to Use Each Measure:

- **Quantiles**: Useful to divide the data into equal intervals, such as when examining the distribution or specific sections of a dataset.
- **Percentiles**: Useful when you want to know the relative position of a data point or the distribution of data in 100 intervals.
- **IQR**: Useful to understand the spread of the middle 50% of the data and for identifying potential outliers.

[Back to Statistics and Probability](#statistics-and-probability)

---

### 1. Covariance

**Definition**: Covariance is a measure of how two variables change together. It shows whether an increase in one variable would result in an increase or decrease in another variable. If the covariance is positive, the variables tend to increase or decrease together. If it's negative, one variable tends to increase when the other decreases. If it's close to zero, there is little or no relationship between the variables.

**Formula**:  
For two variables \( X \) and \( Y \), the covariance is given by:
\[
\text{Cov}(X, Y) = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})
\]
where:
- \( x_i \) and \( y_i \) are individual data points of variables \( X \) and \( Y \),
- \( \bar{x} \) and \( \bar{y} \) are the means of \( X \) and \( Y \),
- \( n \) is the number of data points.

**Interpretation**:
- If \(\text{Cov}(X, Y) > 0\), both variables tend to increase or decrease together.
- If \(\text{Cov}(X, Y) < 0\), one variable tends to increase while the other decreases.
- If \(\text{Cov}(X, Y) = 0\), there is no linear relationship between the variables.

---

### 2. Correlation

**Definition**: Correlation is a normalized version of covariance that provides a measure of the strength and direction of the linear relationship between two variables. It ranges from \(-1\) to \(+1\), where:
- \( +1 \) indicates a perfect positive linear relationship,
- \( -1 \) indicates a perfect negative linear relationship,
- \( 0 \) indicates no linear relationship.

**Formula**:  
The Pearson correlation coefficient \( r \) between two variables \( X \) and \( Y \) is given by:
\[
r = \frac{\text{Cov}(X, Y)}{\sigma_X \sigma_Y}
\]
where:
- \(\text{Cov}(X, Y)\) is the covariance between \( X \) and \( Y \),
- \( \sigma_X \) and \( \sigma_Y \) are the standard deviations of \( X \) and \( Y \).

**Interpretation**:
- \( r > 0 \) indicates a positive correlation: as \( X \) increases, \( Y \) tends to increase.
- \( r < 0 \) indicates a negative correlation: as \( X \) increases, \( Y \) tends to decrease.
- \( r = 0 \) indicates no linear relationship between \( X \) and \( Y \).
- The closer \( r \) is to \( +1 \) or \( -1 \), the stronger the linear relationship.

---

### Summary of Key Terms:

| **Term**         | **Definition**                                                                 | **Formula**                                                 |
|------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------|
| **Covariance**   | Measures how two variables change together.                                     | \(\text{Cov}(X, Y) = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})\) |
| **Correlation**   | A normalized version of covariance that measures the strength and direction of a linear relationship. | \(r = \frac{\text{Cov}(X, Y)}{\sigma_X \sigma_Y}\) |

---

### When to Use Each Measure:

- **Covariance**: Use covariance when you want to understand the direction of the relationship between two variables, but be aware that it is affected by the scale of the data (i.e., it doesn't normalize the relationship).
- **Correlation**: Use correlation when you want to understand both the direction and strength of the linear relationship between two variables, and need a scale-independent measure (since correlation is normalized)
  
[Back to Statistics and Probability](#statistics-and-probability)

---
## Probability Funcations
### 1. Probability Mass Function (PMF)

**Definition**: The **Probability Mass Function (PMF)** is used for discrete random variables. It gives the probability that a discrete random variable is exactly equal to some value. The PMF must satisfy two conditions:
- The probability of each possible outcome is between 0 and 1, i.e., \( 0 \leq P(X = x) \leq 1 \),
- The sum of all probabilities over all possible outcomes equals 1, i.e., \( \sum_{x} P(X = x) = 1 \).

**Formula**:  
For a discrete random variable \( X \), the PMF is given by:
\[
P(X = x) = p_x
\]
where \( p_x \) is the probability of the random variable \( X \) taking the value \( x \).

**Usage**:  
PMF is used to describe discrete probability distributions, such as the distribution of the number of heads in a coin toss or the number of successes in a series of Bernoulli trials.

---

### 2. Cumulative Distribution Function (CDF)

**Definition**: The **Cumulative Distribution Function (CDF)** is a function that describes the probability that a random variable \( X \) will take a value less than or equal to \( x \). It is used for both discrete and continuous random variables.

**Formula**:  
The CDF for a random variable \( X \) is given by:
\[
F_X(x) = P(X \leq x)
\]
For a discrete random variable:
\[
F_X(x) = \sum_{t \leq x} P(X = t)
\]
For a continuous random variable:
\[
F_X(x) = \int_{-\infty}^{x} f_X(t) \, dt
\]
where \( P(X \leq x) \) is the probability that \( X \) takes a value less than or equal to \( x \), and \( f_X(t) \) is the probability density function of \( X \).

**Usage**:  
The CDF is helpful for understanding the cumulative probability up to a certain point and for determining percentiles of a distribution.

---

### 3. Probability Density Function (PDF)

**Definition**: The **Probability Density Function (PDF)** is used for continuous random variables. It provides the probability of the random variable falling within a particular range of values, rather than taking any specific value. Unlike PMF, which gives probabilities for specific outcomes, the PDF gives probabilities in the form of a density.

**Formula**:  
The PDF of a continuous random variable \( X \) is denoted by \( f_X(x) \) and satisfies the following properties:
- \( f_X(x) \geq 0 \) for all \( x \),
- The total area under the curve of the PDF is equal to 1:
\[
\int_{-\infty}^{\infty} f_X(x) \, dx = 1
\]
To find the probability that \( X \) lies within a range \( [a, b] \), we compute:
\[
P(a \leq X \leq b) = \int_{a}^{b} f_X(x) \, dx
\]

**Usage**:  
PDF is used to describe continuous probability distributions, such as the normal distribution or the exponential distribution.

---

### Summary of Key Terms:

| **Term**                | **Definition**                                                | **Formula**                                                       |
|-------------------------|---------------------------------------------------------------|-------------------------------------------------------------------|
| **PMF**                 | Probability mass function for discrete random variables.       | \( P(X = x) = p_x \)                                              |
| **CDF**                 | Cumulative distribution function for both discrete and continuous random variables. | \( F_X(x) = P(X \leq x) \)  for discrete, \( F_X(x) = \int_{-\infty}^{x} f_X(t) \, dt \) for continuous |
| **PDF**                 | Probability density function for continuous random variables.  | \( f_X(x) \), such that \( \int_{-\infty}^{\infty} f_X(x) \, dx = 1 \) |

---

### When to Use Each Measure:

- **PMF**: Use PMF when dealing with discrete random variables to calculate the probability of specific outcomes.
- **CDF**: Use CDF when you need to know the cumulative probability up to a certain point or when working with percentiles.
- **PDF**: Use PDF for continuous random variables to find the probability density at a specific point or the probability over a range of values.

[Back to Statistics and Probability](#statistics-and-probability)

---
## Skewness and kurtosis
### 1. Skewness

**Definition**: Skewness measures the asymmetry or lack of symmetry in a probability distribution. A distribution can be:
- **Positively skewed** (right-skewed): The right tail is longer or fatter than the left.
- **Negatively skewed** (left-skewed): The left tail is longer or fatter than the right.
- **Symmetric**: If skewness is zero, the distribution is symmetric.

**Formula**:  
The skewness \( \gamma_1 \) of a random variable \( X \) is given by:
\[
\gamma_1 = \frac{n}{(n-1)(n-2)} \sum_{i=1}^{n} \left( \frac{x_i - \bar{x}}{s} \right)^3
\]
where:
- \( x_i \) is the data point,
- \( \bar{x} \) is the mean of the dataset,
- \( s \) is the standard deviation of the dataset,
- \( n \) is the number of data points.

**Interpretation**:
- If \( \gamma_1 = 0 \), the distribution is symmetric.
- If \( \gamma_1 > 0 \), the distribution is positively skewed (right-skewed).
- If \( \gamma_1 < 0 \), the distribution is negatively skewed (left-skewed).

---

### 2. Kurtosis

**Definition**: Kurtosis measures the "tailedness" or the sharpness of the peak of a probability distribution. It provides an indication of how much of the data is in the tails or the center of the distribution.
- **Leptokurtic**: Distributions with high kurtosis (heavy tails and sharp peaks).
- **Platykurtic**: Distributions with low kurtosis (light tails and flatter peaks).
- **Mesokurtic**: Distributions with kurtosis similar to the normal distribution.

**Formula**:  
The kurtosis \( \gamma_2 \) of a random variable \( X \) is given by:
\[
\gamma_2 = \frac{n(n+1)}{(n-1)(n-2)(n-3)} \sum_{i=1}^{n} \left( \frac{x_i - \bar{x}}{s} \right)^4 - \frac{3(n-1)^2}{(n-2)(n-3)}
\]
where:
- \( x_i \) is the data point,
- \( \bar{x} \) is the mean of the dataset,
- \( s \) is the standard deviation of the dataset,
- \( n \) is the number of data points.

**Interpretation**:
- If \( \gamma_2 = 0 \), the distribution has normal kurtosis (mesokurtic).
- If \( \gamma_2 > 0 \), the distribution is leptokurtic (heavy tails and sharp peak).
- If \( \gamma_2 < 0 \), the distribution is platykurtic (light tails and flatter peak).

---

### Summary of Key Terms:

| **Term**         | **Definition**                                                    | **Formula**                                                       |
|------------------|-------------------------------------------------------------------|-------------------------------------------------------------------|
| **Skewness**     | Measures the asymmetry of the distribution.                       | \( \gamma_1 = \frac{n}{(n-1)(n-2)} \sum_{i=1}^{n} \left( \frac{x_i - \bar{x}}{s} \right)^3 \) |
| **Kurtosis**     | Measures the "tailedness" of the distribution.                     | \( \gamma_2 = \frac{n(n+1)}{(n-1)(n-2)(n-3)} \sum_{i=1}^{n} \left( \frac{x_i - \bar{x}}{s} \right)^4 - \frac{3(n-1)^2}{(n-2)(n-3)} \) |

---

### When to Use Each Measure:

- **Skewness**: Use skewness to understand the asymmetry of a distribution. Positive skewness suggests a longer right tail, while negative skewness indicates a longer left tail.
- **Kurtosis**: Use kurtosis to understand the "tailedness" of a distribution. High kurtosis (leptokurtic) suggests the presence of outliers, while low kurtosis (platykurtic) indicates fewer outliers and a flatter distribution.

[Back to Statistics and Probability](#statistics-and-probability)

---


## Probability Distributions
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

[Back to Statistics and Probability](#statistics-and-probability)

---

### Discrete Probability Distributions
#### [Bernoulli Distribution](#bernoulli-distribution)
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

    ()![image](https://github.com/user-attachments/assets/4ea762b3-981e-4943-85d7-d684c80de287)


[Back to [Discrete Probability Distributions]](#discrete-probability-distributions) | [Back to Probability Distributions](#probability-distributions)

---

#### [Binomial Distribution](#binomial-distribution)
* The **Binomial distribution** is a discrete probability distribution that models the number of successes in a fixed number of independent trials, each with the same probability of success. It generalizes the Bernoulli distribution (which models a single trial) to multiple trials.

* **Key Characteristics** of the Binomial Distribution:
  - **Number of trials**: There are \( n \) independent trials (experiments).
  - **Probability of success**: The probability of success on each trial is \( p \), and the probability of failure is \( 1 - p \).
  - **Number of successes**: The random variable \( X \) represents the number of successes (or the count of successful outcomes) in the \( n \) trials.

* **Formula**:
  - Probability mass function (PMF):
    \[
    P(X=k) = \binom{n}{k} p^k (1 - p)^{n-k}
    \]
    where \( X \) is the number of successes, \( k \in \{0, 1, 2, \dots, n\} \), and \( \binom{n}{k} \) is the binomial coefficient.

* **Example**:
  - In a series of 10 coin tosses, what is the probability of getting exactly 6 heads (successes)? Here, \( n = 10 \) and \( p = 0.5 \).

* **Properties**:
  - **Mean** (Expected Value): \( \mu = n \cdot p \)
  - **Variance**: \( \sigma^2 = n \cdot p \cdot (1 - p) \)
    ![image](https://github.com/user-attachments/assets/b6b4db5c-d84a-4c14-ab75-9e7b8016dda9)


[Back to [Discrete Probability Distributions]](#discrete-probability-distributions) | [Back to Probability Distributions](#probability-distributions)

---

#### [Poisson Distribution](#poisson-distribution)
* The **Poisson distribution** models the number of times an event occurs within a fixed interval of time or space, given that the events occur independently and at a constant average rate.

* **Key Characteristics**:
  - **Parameter** \( \lambda \): The average rate of occurrence of the event within a fixed interval.
  - The number of occurrences is modeled as a random variable \( X \), and it can take values \( k = 0, 1, 2, \dots \).

* **Formula**:
  - Probability mass function (PMF):
    \[
    P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
    \]
    where \( \lambda \) is the expected number of occurrences, and \( k \) is the actual number of occurrences.

* **Example**:
  - The average number of emails received per hour is 5. What is the probability of receiving exactly 3 emails in an hour?

* **Properties**:
  - **Mean**: \( \mu = \lambda \)
  - **Variance**: \( \sigma^2 = \lambda \)

    ![image](https://github.com/user-attachments/assets/2139df1c-b2c9-497a-903a-08f878eb2018)


[Back to [Discrete Probability Distributions]](#discrete-probability-distributions) | [Back to Probability Distributions](#probability-distributions)

---

### Continuous Probability Distributions
#### [Uniform Distribution](#uniform-distribution)
* The **Uniform distribution** is a type of continuous probability distribution in which all outcomes are equally likely within a given range. The distribution is defined by two parameters: the minimum and maximum values.

* **Formula**:
  - Probability density function (PDF):
    \[
    f(x) = \frac{1}{b - a}, \quad \text{for} \, a \leq x \leq b
    \]
    where \( a \) and \( b \) are the minimum and maximum values of the range.

* **Example**:
  - Rolling a fair 6-sided die. Each outcome is equally likely, so the distribution is uniform over the range \( [1, 6] \).
 
    ![image](https://github.com/user-attachments/assets/bb5aad97-c40e-4d44-8faa-2eacdd770c3f)

[Back to [Continuous Probability Distributions]](#continuous-probability-distributions) | [Back to Probability Distributions](#probability-distributions)


---

#### [Normal (Gaussian) Distribution](#normal-gaussian-distribution)
* The **Normal distribution**, also known as the **Gaussian distribution**, is a continuous probability distribution that is symmetric around the mean. It is one of the most commonly used distributions in statistics.

* **Formula**:
  - Probability density function (PDF):
    \[
    f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x - \mu)^2}{2\sigma^2}}
    \]
    where \( \mu \) is the mean and \( \sigma \) is the standard deviation.

* **Properties**:
  - Symmetrical: The distribution is symmetrical around the mean.
  - **Mean** = \( \mu \)
  - **Variance** = \( \sigma^2 \)
 
    ![image](https://github.com/user-attachments/assets/ca8d7261-641b-425e-8976-87c8a7a1d459)


[Back to [Continuous Probability Distributions]](#continuous-probability-distributions) | [Back to Probability Distributions](#probability-distributions)

---

#### [Exponential Distribution](#exponential-distribution)
* The **Exponential distribution** models the time between events in a Poisson process. It is a continuous distribution with a constant hazard rate.

* **Formula**:
  - Probability density function (PDF):
    \[
    f(x) = \lambda e^{-\lambda x}, \quad x \geq 0
    \]
    where \( \lambda \) is the rate parameter.

* **Example**:
  - The time between arrivals of customers at a service desk follows an exponential distribution.
 
    ![image](https://github.com/user-attachments/assets/fb0792a9-4219-4911-8527-ec2562926dfb)


[Back to [Continuous Probability Distributions]](#continuous-probability-distributions) | [Back to Probability Distributions](#probability-distributions)

---

#### [Student’s t-Distribution](#students-t-distribution)
* The **t-distribution** is used in hypothesis testing, particularly in small sample sizes when the population variance is unknown.

* **Formula**:
  - Probability density function (PDF):
    \[
    f(x) = \frac{\Gamma\left(\frac{\nu + 1}{2}\right)}{\sqrt{\nu \pi} \Gamma\left(\frac{\nu}{2}\right)} \left(1 + \frac{x^2}{\nu}\right)^{-\frac{\nu + 1}{2}}
    \]
    where \( \nu \) is the degrees of freedom.

    ![Screenshot 2025-03-20 083543](https://github.com/user-attachments/assets/6a901c9f-caad-4d59-a8b5-5eba0d4d1c7b)


[Back to [Continuous Probability Distributions]](#continuous-probability-distributions) | [Back to Probability Distributions](#probability-distributions)

---

#### [Log-Normal Distribution](#log-normal-distribution)
* The **Log-Normal distribution** is a continuous probability distribution of a random variable whose logarithm is normally distributed. If \( X \) is normally distributed, then \( Y = e^X \) follows a log-normal distribution.

* **Formula**:
  - Probability density function (PDF):
    \[
    f(x) = \frac{1}{x \sigma \sqrt{2\pi}} e^{-\frac{(\ln(x) - \mu)^2}{2\sigma^2}}, \quad x > 0
    \]
    where \( \mu \) and \( \sigma \) are the parameters of the normal distribution of \( \ln(x) \).

* **Example**:
  - The distribution of stock prices is often modeled using a log-normal distribution.
 
    ![image](https://github.com/user-attachments/assets/b2a73c27-2717-46bd-b9fc-96bee2a9595c)


[Back to [Continuous Probability Distributions]](#continuous-probability-distributions) | [Back to Probability Distributions](#probability-distributions)

---

#### [Pareto Distribution](#pareto-distribution)
* The **Pareto distribution** is a power-law probability distribution that is often used to model the distribution of wealth, city populations, or income.

* **Formula**:
  - Probability density function (PDF):
    \[
    f(x) = \frac{\alpha x_m^\alpha}{x^{\alpha+1}}, \quad x \geq x_m
    \]
    where \( \alpha \) is the shape parameter, and \( x_m \) is the scale parameter.

* **Example**:
  - Income distribution, where a small number of people hold most of the wealth.
 
    ![image](https://github.com/user-attachments/assets/d2f14b04-a9af-4f94-be58-7ba49d13362e)

 You can all the visualisations of graphs by setting different parameters [here](https://probstats.org/)

[Back to Continuous Probability Distributions](#continuous-probability-distributions) | [Back to Probability Distributions](#probability-distributions)

[Back to Statistics and Probability](#statistics-and-probability)

---

## Central Limit Theorem
The **Central Limit Theorem (CLT)** is one of the most important theorems in statistics, explaining why the normal distribution appears so often in practice. It describes the distribution of sample means from any population distribution, provided certain conditions are met.

### 1. The Basic Idea of the Central Limit Theorem
The CLT states that if you take a large enough sample from a population with any shape of distribution (it doesn’t have to be normal), the sampling distribution of the sample mean will approach a normal distribution as the sample size increases.

**Formally:**
- Given a population with mean \( \mu \) and variance \( \sigma^2 \).
- Take a random sample of size \( n \) from this population.
- Compute the sample mean for this sample.
- If you repeat this process many times, the distribution of the sample means will approximate a normal distribution with:
  - Mean \( \mu \) (the population mean).
  - Standard deviation \( \frac{\sigma}{\sqrt{n}} \), which is the standard error of the mean.


---

### 2. Key Concepts in CLT
- **Population Distribution**: The distribution of values in the original population. It can be skewed, uniform, binomial, or any other shape.
- **Sample Mean**: The average of the values in each sample.
- **Sampling Distribution**: The distribution of the sample means, which is the key focus of CLT.

---

### 3. What Happens as Sample Size Increases?
As sample size \( n \) increases, the distribution of the sample mean becomes more normal, regardless of the population distribution's shape.
- For a sample size of \( n = 30 \) or greater, the sampling distribution of the sample mean tends to be close to normal, even if the original population distribution is highly skewed.

---

### 4. Mathematical Formulation of the CLT
Suppose the population has a mean \( \mu \) and variance \( \sigma^2 \). 
- Draw a sample of size \( n \) from this population and compute the sample mean \( \bar{X} \).
- The sampling distribution of \( \bar{X} \) will have:
  - Mean: \( E(\bar{X}) = \mu \)
  - Standard deviation (Standard error): \( SE = \frac{\sigma}{\sqrt{n}} \)
  
As the sample size \( n \) increases, the sampling distribution of the sample mean will resemble a normal distribution with:
  \[
  N\left(\mu, \frac{\sigma^2}{n}\right)
  \]
  This means the sample means have the same mean \( \mu \) as the population but a smaller variance, which decreases as \( n \) increases.

---

### 5. Conditions for the Central Limit Theorem to Apply
The Central Limit Theorem holds under the following conditions:
- **Independence**: The samples must be drawn independently of each other.
- **Sample Size**: The sample size \( n \) should be sufficiently large. A sample size of \( n \geq 30 \) is generally considered enough for CLT to apply.
- **Finite Variance**: The population must have finite variance.

---

### 6. Implications of the Central Limit Theorem
- **Sampling Distribution of the Mean**: Even if the population distribution is not normal, the sampling distribution of the sample means will still be normal (or close to normal) as long as the sample size is large.
- **Normal Approximation**: This is why the normal distribution is so commonly used in statistics. The CLT enables statisticians to approximate probabilities using the normal distribution, even if the original data isn’t normally distributed.

---

### 7. Practical Examples of CLT

#### Example 1: Coin Flips
Imagine flipping a fair coin 100 times. The population distribution is binomial, but if you repeatedly take samples of 10 flips and calculate the average number of heads, the sampling distribution of the sample means will approximate a normal distribution as you take more and more samples.

#### Example 2: Height of People
Suppose we are studying the height of adult men in a country. The population distribution might be skewed, but if we repeatedly take random samples of 50 men and calculate the sample means of their heights, the distribution of these means will approach a normal distribution.

---

### 8. Why is the CLT Important?
- **Estimation**: It allows us to use sample data to make inferences about population parameters, such as using the sample mean to estimate the population mean.
- **Hypothesis Testing**: The CLT justifies the use of the normal distribution for conducting hypothesis tests, even when the underlying population is not normal.
- **Confidence Intervals**: It enables the calculation of confidence intervals for population means, assuming the sample size is sufficiently large.

---

### 9. Limitations of the CLT
- **Very Small Sample Sizes**: The CLT does not apply well to very small sample sizes, especially if the population distribution is highly skewed or contains outliers.
- **Non-Independent Samples**: If the samples are not independent, the CLT cannot be applied.
- **Infinite or Very Large Population**: The CLT assumes that the population is large enough or infinite so that sampling does not significantly affect the population distribution.

[Back to Central Limit Theorem](#central-limit-theorem) | [Back to Statistics and Probability](#statistics-and-probability)

[Back to Top](#data-science-cheatsheets)
---

## Hypothesis Test
## 1. What is Hypothesis Testing?
In hypothesis testing, we start with a null hypothesis and an alternative hypothesis. The goal is to use sample data to evaluate whether there is enough evidence to reject the null hypothesis in favor of the alternative hypothesis.

### Null Hypothesis (\(H_0\)):
This is a statement that there is no effect, no difference, or no relationship in the population. It's what we assume to be true unless the evidence suggests otherwise.

**Example**: "The average height of adult men in a country is 175 cm."

### Alternative Hypothesis (\(H_1\) or \(H_a\)):
This is the statement that contradicts the null hypothesis. It suggests that there is an effect, a difference, or a relationship in the population.

**Example**: "The average height of adult men in a country is not 175 cm."

---

## 2. Steps in Hypothesis Testing
Here are the general steps involved in performing a hypothesis test:

### Step 1: State the Hypotheses
- **Null Hypothesis (\(H_0\))**: A statement about the population parameter (e.g., mean, proportion) that you want to test.
- **Alternative Hypothesis (\(H_1\))**: The opposite statement, suggesting what you want to prove.

### Step 2: Choose the Significance Level (\(\alpha\))
The significance level (\(\alpha\)) is the probability of rejecting the null hypothesis when it is actually true (i.e., making a Type I error).  
Common values for \(\alpha\) are 0.05, 0.01, or 0.10.  
For example, if \(\alpha = 0.05\), you are allowing a 5% chance of incorrectly rejecting the null hypothesis.

### Step 3: Select the Appropriate Test
Depending on the nature of the data and the hypothesis, choose the correct statistical test:
- **t-test**: Used when the population standard deviation is unknown and the sample size is small.
- **z-test**: Used when the population standard deviation is known and the sample size is large (typically \(n \geq 30\)).
- **Chi-square test**: Used for categorical data to test the goodness-of-fit or independence.
- **ANOVA (Analysis of Variance)**: Used to compare means across multiple groups.

### Step 4: Collect Data and Compute the Test Statistic
Gather your sample data and calculate the test statistic. The test statistic is a value that measures how far your sample data is from the null hypothesis.

**For example**:  
In a t-test, the test statistic is the t-value, calculated as:  
\[
t = \frac{\overline{X} - \mu_0}{s / \sqrt{n}}
\]
Where:
- \(\overline{X}\) = sample mean  
- \(\mu_0\) = hypothesized population mean  
- \(s\) = sample standard deviation  
- \(n\) = sample size

### Step 5: Determine the Critical Value(s) and Compare
Based on the significance level \(\alpha\), find the critical value (or rejection region) from statistical tables (e.g., z-table or t-table) or statistical software.

- **Critical value**: This is the threshold beyond which you will reject the null hypothesis. If the test statistic exceeds this value, you reject \(H_0\).
- For example, in a two-tailed test with \(\alpha = 0.05\), the critical z-values might be \(\pm 1.96\) for a normal distribution.

### Step 6: Make a Decision
- **Reject \(H_0\)**: If the test statistic falls in the rejection region (i.e., the observed value is far enough from the expected value under \(H_0\)), you reject the null hypothesis and conclude that there is enough evidence to support the alternative hypothesis.
- **Fail to reject \(H_0\)**: If the test statistic does not fall in the rejection region (i.e., the observed value is close enough to the expected value under \(H_0\)), you fail to reject the null hypothesis, meaning there is insufficient evidence to support the alternative hypothesis.

### Step 7: Interpret the Results
Based on the decision made in Step 6, interpret the results in the context of your research question.

**Example**: If you reject the null hypothesis, you might say, "There is enough evidence to suggest that the average height of adult men in the country is not 175 cm."

---

## 3. Types of Errors in Hypothesis Testing

- **Type I Error (False Positive)**: Rejecting the null hypothesis when it is actually true. The probability of making a Type I error is \(\alpha\), the significance level.  
  **Example**: Concluding that the average height of adult men is not 175 cm when it actually is.

- **Type II Error (False Negative)**: Failing to reject the null hypothesis when the alternative hypothesis is actually true. The probability of making a Type II error is denoted by \(\beta\).  
  **Example**: Concluding that the average height of adult men is 175 cm when it is actually different.

---

## 4. One-Tailed vs. Two-Tailed Tests

- **One-Tailed Test**: Tests for an effect in one direction (either greater than or less than). You are testing if the parameter is greater than or less than a certain value.  
  **Example**: Testing if the average height is greater than 175 cm (\(H_1: \mu > 175\)).

- **Two-Tailed Test**: Tests for an effect in both directions (either greater than or less than). You are testing if the parameter is different from a certain value (not equal).  
  **Example**: Testing if the average height is different from 175 cm (\(H_1: \mu \neq 175\)).

---

## Complete Statistics Notebook
* If you want all of these concepts with code and visualisation, check out this [NoteBook](https://github.com/Adity-star/Data-Science-Work/blob/main/CheatSheets/Complete%20Statistics.ipynb).
* Carlos Fernandez-Granda from New York University has great lecture notes [Probability and Statistics for Data Science](https://cims.nyu.edu/~cfgranda/pages/stuff/probability_stats_for_DS.pdf) (available online)

[Back to Hypothesis Testing](#hypothesis-test) | [Back to Statistics and Probability](#statistics-and-probability)

[Back to Top](#data-science-cheatsheets)
---

# Machine Learning Concepts

Machine learning is a subfield of artificial intelligence that deals with algorithms and statistical models that enable computers to perform tasks without explicit instructions. This document provides an overview of core machine learning concepts, algorithms, metrics, and advanced topics.

## Table of Contents
- [Machine Learning Basics](#machine-learning-basics)
- [Machine Learning Workflow](#machine-learning-workflow)
- [Machinr Learning Advanced Concepts](#machine-learning-advanced-concepts)
- [Metrics](#metrics)

[Back to Top](#data-science-cheatsheets)
---
# Machine Learning Basics
## What is Machine Learning?

Machine learning is the process of developing algorithms that can learn from and make predictions on data. Instead of being programmed with specific instructions, the model improves its performance through experience (data). Machine learning can be applied to tasks such as classification, regression, clustering, and recommendation.

---

## Types of Machine Learning

There are three main types of machine learning, based on how the model learns from the data.

### 1. Supervised Learning
In supervised learning, the algorithm is trained on labeled data, meaning the input data is paired with the correct output (label). The goal is to learn a mapping from inputs to outputs, so the model can predict the output for new, unseen data.

**Common algorithms:**
- Linear Regression
- Logistic Regression
- Decision Trees
- Support Vector Machines (SVM)
- K-Nearest Neighbors (KNN)

### 2. Unsupervised Learning
Unsupervised learning involves training on data that has no labels. The goal is to find hidden patterns or structures within the data.

**Common algorithms:**
- K-Means Clustering
- Hierarchical Clustering
- Principal Component Analysis (PCA)

### 3. Reinforcement Learning
In reinforcement learning, the algorithm learns by interacting with an environment and receiving feedback in the form of rewards or penalties. The objective is to learn a policy that maximizes the cumulative reward over time.

**Common algorithms:**
- Q-learning
- Deep Q Networks (DQN)

[Back to Machine Learning Concepts](#machine-learning-concepts) 


---

## Machine Learning Workflow

The typical machine learning workflow involves several key steps that guide the process of building and evaluating models.

### 1. Data Collection
The first step is to gather the data, which is the foundation for training and testing models. The data may come from various sources, such as databases, spreadsheets, or sensors.

### 2. Data Preprocessing
Once the data is collected, it often needs to be cleaned and preprocessed. This can involve tasks such as handling missing values, scaling features, encoding categorical variables, and splitting the data into training and testing sets.

### 3. Model Selection
In this step, you choose the appropriate machine learning algorithm based on the problem you're trying to solve (e.g., classification, regression, etc.) and the type of data you have.

### 4. Model Training
After selecting the model, you train it on the training data. The model adjusts its parameters based on the data to minimize the error.

### 5. Model Evaluation
After training, you evaluate the model using testing data to see how well it generalizes. Various metrics like accuracy, precision, recall, and F1-score are used to assess performance.

### 6. Hyperparameter Tuning
Many machine learning models have hyperparameters (settings that aren't learned during training) that affect performance. Hyperparameter tuning involves experimenting with different values to find the optimal combination.

### 7. Model Deployment
Once the model is trained and evaluated, it can be deployed in real-world applications, such as in a web service or an app.

[Back to Machine Learning Concepts](#machine-learning-concepts) 

[Back to Top](#data-science-cheatsheets)

---
# Machine Learning Advanced Concepts
- [Cross Validation](#cross-validation)
- [Feature Importance](#feature-importance)
- [Mean Squared Error vs. Mean Absolute Error](#mean-squared-error-vs-mean-absolute-error)
- [L1 vs L2 regularization](#l1-vs-l2-regularization)
- [Correlation vs Covariance](#correlation-vs-covariance)
- [Would adding more data address underfitting?](#would-adding-more-data-address-underfitting)
- [Activation Function](#activation-function)
- [Bagging](#bagging)
- [Stacking](#stacking)
- [Parametric vs Nonparametric](#parametric-vs-nonparametric)

[Back to Machine Learning Concepts](#machine-learning-concepts) 

[Back to Top](#data-science-cheatsheets)

---
## Cross Validation
Cross-validation is a technique to evaluate predictive models by partitioning the original sample into a training set to train the model, and a validation set to evaluate it. For example, a k-fold cross validation divides the data into k folds (or partitions), trains on each k-1 fold, and evaluate on the remaining 1 fold. This results to k models/evaluations, which can be averaged to get an overall model performance.

[Back to Machine Learning Concepts](#machine-learning-concepts)

---
## Feature Importance
In linear models, feature importance can be calculated by the scale of the coefficients.
In tree-based methods (such as random forest), important features are likely to appear closer to the root of the tree. We can get a feature's importance for random forest by computing the averaging depth at which it appears across all trees in the forest.
Supervised learning is a type of machine learning where the model is trained using labeled data. The goal is to learn a mapping from inputs to the outputs based on a set of training data.

[Back to Machine Learning Advanced Concepts](#machine-learning-advanced-concepts)

---
## Mean Squared Error vs. Mean Absolute Error
Similarity: both measure the average model prediction error; range from 0 to infinity; the lower the better.
Mean Squared Error (MSE) gives higher weights to large error (e.g., being off by 10 just MORE THAN TWICE as bad as being off by 5), whereas Mean Absolute Error (MAE) assign equal weights (being off by 10 is just twice as bad as being off by 5).
MSE is continuously differentiable, MAE is not (where y_pred == y_true).

[Back to Machine Learning Advanced Concepts](#machine-learning-advanced-concepts)

---

## L1 vs L2 Regularization

### Similarity:
Both L1 and L2 regularization prevent overfitting by shrinking (imposing a penalty) on the coefficients.

### Difference:
- **L2 (Ridge)** shrinks all the coefficients by the same proportions but eliminates none.
- **L1 (Lasso)** can shrink some coefficients to zero, performing variable selection.

### Which to Choose:
- If all the features are correlated with the label, **Ridge (L2)** outperforms **Lasso (L1)**, as the coefficients are never zero in Ridge.
- If only a subset of features are correlated with the label, **Lasso (L1)** outperforms **Ridge (L2)**, as in Lasso some coefficients can be shrunken to zero.

[Back to Machine Learning Advanced Concepts](#machine-learning-advanced-concepts)

---
## Correlation vs Covariance

### Similarities:
Both determine the relationship and measure the dependency between two random variables.

### Difference:
- **Correlation**: Measures the change in one item that may result in the change of another item.
- **Covariance**: Measures when two items vary together (joint variability).

### Key Points:
- Covariance is essentially a measure of correlation.
- **Correlation** refers to the scaled form of covariance.

### Range:
- **Correlation** ranges between **-1 and +1**.
- **Covariance** lies between **negative infinity and infinity**.

[Back to Machine Learning Advanced Concepts](#machine-learning-advanced-concepts)

---
## Would Adding More Data Address Underfitting?

Underfitting happens when a model is not complex enough to learn well from the data. It is a problem with the model rather than the data size. 

### Solution:
A potential way to address underfitting is to increase the model complexity, such as:
- Adding higher-order coefficients for linear models.
- Increasing the depth for tree-based methods.
- Adding more layers or neurons for neural networks, etc.

[Back to Machine Learning Advanced Concepts](#machine-learning-advanced-concepts)

---

# Activation Function

Activation functions in neural networks introduce non-linearity, allowing the model to learn more complex patterns. The choice of activation function depends on the type of problem you are solving (e.g., regression, binary classification, multi-class classification).

## Types of Activation Functions

### 1. Non-linearity: ReLU (Rectified Linear Unit)

- **ReLU** is one of the most commonly used activation functions in neural networks, especially for hidden layers.
- It is simple and computationally efficient.
- The function outputs zero for negative input and returns the input itself for positive input:
  
  \[
  f(x) = \max(0, x)
  \]

  - **Pros**: It helps the model to learn non-linear relationships, making it suitable for most tasks.
  - **Cons**: It can suffer from the "dead ReLU" issue, where some neurons stop updating and output zeros for all inputs.

### 2. Leaky ReLU

- **Leaky ReLU** is a variation of the ReLU function designed to fix the "dead ReLU" issue.
- Instead of outputting zero for negative input, it outputs a small positive gradient:
  
  \[
  f(x) = 
  \begin{cases} 
  x & \text{if } x > 0 \\
  \alpha x & \text{if } x \leq 0 
  \end{cases}
  \]
  
  Where \( \alpha \) is a small constant (e.g., 0.01).

  - **Pros**: It allows for small negative values, preventing neurons from "dying."
  - **Cons**: The choice of \( \alpha \) can affect performance and needs to be tuned.

### 3. Multi-class Classification: Softmax

- **Softmax** is commonly used for multi-class classification problems.
- It converts the output of a neural network into probabilities, with each value between 0 and 1, and the sum of all probabilities is 1. This allows us to treat the output as the likelihood of each class.

  \[
  f(x_i) = \frac{e^{x_i}}{\sum_{j=1}^n e^{x_j}}
  \]
  
  Where \( x_i \) is the output of the \( i \)-th neuron, and \( n \) is the number of classes.

  - **Pros**: Converts the raw output into a probability distribution for multi-class classification tasks.
  - **Cons**: Can be computationally expensive when there are many classes.

### 4. Binary Classification: Sigmoid

- **Sigmoid** is used for binary classification problems. It squashes the output between 0 and 1, interpreting the result as a probability.
  
  \[
  f(x) = \frac{1}{1 + e^{-x}}
  \]

  - **Pros**: It works well for binary classification tasks, producing probabilities that can be interpreted as confidence in the positive class.
  - **Cons**: It suffers from the "vanishing gradient" problem for large values of input, leading to slow learning.

### 5. Regression: Linear

- For regression problems, where the goal is to predict continuous values, the **linear activation function** is used.
- It simply outputs the value of the input without any transformation:

  \[
  f(x) = x
  \]

  - **Pros**: Ideal for regression tasks where the output is a real number.
  - **Cons**: Not suitable for classification tasks, as it does not bound the output between a specific range (e.g., 0 and 1).


[Back to Machine Learning Advanced Concepts](#machine-learning-advanced-concepts)

---
# Bagging 

**Bagging** is an ensemble learning technique that combines multiple models (typically of the same type) to improve the overall performance of a machine learning algorithm. The core idea behind bagging is to generate multiple different subsets of the training data, train a model on each subset, and then combine their predictions.

## How Bagging Works:

1. **Bootstrap Sampling**: Multiple subsets of the original dataset are created by sampling with replacement. This means some data points may appear multiple times in a subset, while others might not appear at all.
2. **Training Multiple Models**: A separate model is trained on each of these subsets.
3. **Aggregation**: The final prediction is made by aggregating the predictions of all the individual models:
   - For **classification**, the final output is determined by majority voting (the class with the most votes).
   - For **regression**, the final prediction is typically the average of all individual model predictions.

## Key Points about Bagging:

- **Reduces Variance**: By combining predictions from multiple models, bagging reduces the variance of the model, making it less sensitive to noise in the training data. This helps to reduce overfitting.
- **Works Well with High-Variance Models**: Bagging is particularly useful for models that have high variance, such as decision trees, as it stabilizes their predictions.
- **Parallelizable**: Since each model is trained independently on different subsets of data, the training process can be parallelized, making it efficient for large datasets.

## Pros of Bagging:

- **Improves Accuracy**: Bagging often leads to higher accuracy by reducing the variance and overfitting.
- **Robust to Outliers**: Since bagging combines predictions from multiple models, outliers that affect one model may not affect the final prediction.
- **Can be Parallelized**: Since each model is trained independently, bagging can be parallelized to speed up training.

## Cons of Bagging:

- **Computationally Expensive**: Training multiple models can be time-consuming and require more computational resources.
- **Difficult to Interpret**: The ensemble nature of bagging can make the model harder to interpret compared to a single model.


[Back to Machine Learning Advanced Concepts](#machine-learning-advanced-concepts)

---
# Stacking 

**Stacking** is an ensemble learning technique that combines multiple models (often of different types) to make predictions. Unlike bagging or boosting, which aggregate the predictions using simple methods like voting or averaging, stacking trains a meta-model to combine the predictions of individual models in a more complex way.

## Key Points about Stacking:

- **Combines Different Models**: Stacking leverages the strengths of different models by combining them in a meta-model. Unlike bagging and boosting, which use the same type of model, stacking can use a variety of models as base learners.
- **Meta-learning**: The second layer (meta-model) learns how to best combine the predictions of the base models, which can improve performance.
- **More Complex**: Stacking tends to be more complex than other ensemble methods like bagging or boosting. It requires careful model selection, data splitting, and training.

## Pros of Stacking:

- **Improved Accuracy**: By combining the strengths of different models, stacking can lead to better performance than using a single model.
- **Flexibility**: You can use any combination of models as base learners, which provides flexibility to experiment with different combinations and improve performance.
- **Handles Overfitting**: The meta-model can help reduce overfitting by learning the optimal way to combine the base model predictions.

## Cons of Stacking:

- **Computationally Expensive**: Training multiple base models and a meta-model requires more computational resources compared to simpler ensemble methods like bagging or boosting.
- **Data Splitting**: Stacking requires careful data splitting, often into multiple subsets, which can reduce the amount of data available for training each model.
- **Complexity**: The process of stacking is more complex to implement and requires more fine-tuning compared to other ensemble methods.

[Back to Machine Learning Advanced Concepts](#machine-learning-advanced-concepts)

---
# Parametric vs Nonparametric

In machine learning, models are typically categorized as **parametric** or **nonparametric**, based on the number of parameters they use and how they scale with respect to the data.

## Parametric Models

A **parametric model** is one that summarizes data using a fixed set of parameters, regardless of the amount of training data. The number of parameters is predetermined before the model is trained, and it remains constant throughout the learning process.

### Key Features of Parametric Models:
- **Fixed number of parameters**: The number of parameters does not depend on the size of the dataset.
- **Model complexity**: The complexity of the model is fixed. Increasing the amount of data doesn't make the model more complex.
- **Training speed**: Parametric models are usually faster to train because the number of parameters is fixed.
- **Assumptions**: Parametric models typically make strong assumptions about the data, such as linearity in linear regression.


### Pros of Parametric Models:
- **Faster to train**: Since the model has a fixed number of parameters, the training process is usually faster.
- **Simpler**: These models are often simpler and easier to interpret due to their limited complexity.
- **Efficient with small data**: Parametric models tend to perform well when you have relatively small amounts of data.

### Cons of Parametric Models:
- **Limited flexibility**: The model's assumptions might not hold for complex data distributions, which can limit its performance.
- **Over-simplification**: If the assumptions are incorrect, the model can underfit the data, resulting in poor predictions.

## Nonparametric Models

A **nonparametric model**, in contrast, does not make a strong assumption about the form or number of parameters in the model. These models can become more complex as the amount of training data increases.


### Pros of Nonparametric Models:
- **Highly flexible**: Nonparametric models can capture complex, non-linear relationships in the data.
- **No strong assumptions**: These models don't require assumptions about the underlying data distribution.
- **Better performance with large datasets**: As the amount of data increases, nonparametric models can become more powerful and accurate.

### Cons of Nonparametric Models:
- **Slower training**: Since the model grows with the data, it can be computationally expensive and take longer to train.
- **Memory-intensive**: Nonparametric models often require storing large amounts of data, which can be inefficient for large datasets.
- **Overfitting**: With increased flexibility, nonparametric models are more prone to overfitting, especially when the training data is noisy.

## Key Differences:

| Feature               | Parametric Models                     | Nonparametric Models                      |
|-----------------------|---------------------------------------|-------------------------------------------|
| **Number of Parameters** | Fixed, independent of data size      | Grows with data size                      |
| **Complexity**         | Fixed complexity                      | Complexity increases with data            |
| **Assumptions**        | Strong assumptions about the data     | Few assumptions, more flexible            |
| **Training Speed**     | Faster                                | Slower, especially with large datasets     |
| **Memory Usage**       | Low memory consumption                | High memory consumption                   |
| **Overfitting Risk**   | Lower risk of overfitting             | Higher risk of overfitting               |

[Back to Machine Learning Advanced Concepts](#machine-learning-advanced-concepts)

---
# Metrics

In machine learning, **metrics** are used to evaluate the performance of models. These metrics provide insights into how well a model is performing for a given task. The metrics you use depend on the type of problem you're working on (e.g., classification, regression, etc.).

In this document, we will cover common evaluation metrics for **classification** and **regression** problems.

---

## Metrics for Classification Problems

### 1. Accuracy
- **Definition**: Accuracy measures the proportion of correct predictions out of all predictions.
- **Formula**:
  \[
  \text{Accuracy} = \frac{\text{Correct Predictions}}{\text{Total Predictions}}
  \]
- **Use case**: Useful when the classes are balanced.
- **Limitation**: Can be misleading if the dataset is imbalanced.

### 2. Precision
- **Definition**: Precision calculates the proportion of true positive predictions among all positive predictions made by the model.
- **Formula**:
  \[
  \text{Precision} = \frac{\text{True Positives}}{\text{True Positives} + \text{False Positives}}
  \]
- **Use case**: Important when false positives have high cost (e.g., in medical diagnoses).
- **Limitation**: Does not consider false negatives.

### 3. Recall (Sensitivity)
- **Definition**: Recall calculates the proportion of true positive predictions out of all actual positive instances.
- **Formula**:
  \[
  \text{Recall} = \frac{\text{True Positives}}{\text{True Positives} + \text{False Negatives}}
  \]
- **Use case**: Useful when false negatives are costly (e.g., fraud detection).
- **Limitation**: Does not consider false positives.

### 4. F1-Score
- **Definition**: The harmonic mean of precision and recall. It balances the trade-off between precision and recall.
- **Formula**:
  \[
  \text{F1-Score} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}
  \]
- **Use case**: Useful when you need a balance between precision and recall, especially for imbalanced datasets.
- **Limitation**: Does not give insights into how much precision or recall is prioritized.

### 5. Confusion Matrix
- **Definition**: A confusion matrix is a table that describes the performance of a classification model. It shows the number of true positives, true negatives, false positives, and false negatives.
- **Components**:
  - **True Positive (TP)**: Correctly predicted positive cases.
  - **True Negative (TN)**: Correctly predicted negative cases.
  - **False Positive (FP)**: Incorrectly predicted as positive.
  - **False Negative (FN)**: Incorrectly predicted as negative.

### 6. Area Under the ROC Curve (AUC-ROC)
- **Definition**: AUC measures the area under the ROC curve, which plots the true positive rate (recall) against the false positive rate. It helps evaluate the model's ability to distinguish between positive and negative classes.
- **Use case**: AUC is a great metric for models with imbalanced classes. A higher AUC indicates better model performance.

### 7. Receiver Operating Characteristic (ROC) Curve
- **Definition**: The ROC curve is a graphical representation of the trade-off between the true positive rate and the false positive rate at various thresholds. 
- **Use case**: Helps visualize and compare the performance of classification models.

---

## Metrics for Regression Problems

### 1. Mean Absolute Error (MAE)
- **Definition**: MAE is the average of the absolute differences between the predicted and actual values. It gives a sense of the average error magnitude.
- **Formula**:
  \[
  \text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|
  \]
- **Use case**: Simple to understand and interpret. Used when you need a measure of how far off predictions are from the actual values.

### 2. Mean Squared Error (MSE)
- **Definition**: MSE is the average of the squared differences between the predicted and actual values. It penalizes larger errors more heavily.
- **Formula**:
  \[
  \text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
  \]
- **Use case**: Commonly used when you want to penalize large errors and emphasize the importance of larger mistakes.

### 3. Root Mean Squared Error (RMSE)
- **Definition**: RMSE is the square root of the mean squared error. It brings the error back to the original unit of the target variable, making it more interpretable.
- **Formula**:
  \[
  \text{RMSE} = \sqrt{\text{MSE}}
  \]
- **Use case**: Useful when you want to understand the error in the same units as the original data.

### 4. R-Squared (R²)
- **Definition**: R² measures how well the regression model fits the data. It is the proportion of the variance in the dependent variable that is predictable from the independent variables.
- **Formula**:
  \[
  R^2 = 1 - \frac{\sum{(y_i - \hat{y}_i)^2}}{\sum{(y_i - \bar{y})^2}}
  \]
- **Use case**: R² provides a measure of goodness-of-fit. An R² value closer to 1 indicates a better fit.

---

## References
- [Scikit-learn: Classification metrics](https://scikit-learn.org/stable/modules/model_evaluation.html#classification-metrics)
- [Scikit-learn: Regression metrics](https://scikit-learn.org/stable/modules/model_evaluation.html#regression-metrics)
- [Kaggle: Evaluation Metrics](https://www.kaggle.com/learn/machine-learning-explainability)

[Back to Machine Learning Advanced Concepts](#machine-learning-advanced-concepts)

[Back to Machine Learning Concepts](#machine-learning-concepts)

[Back to Top](#data-science-cheatsheets)
---

# Supervised Algorithms
## Table of Contents
1. [Linear Regression](#linear-regression)
2. [Logistic Regression](#logistic-regression)
3. [Support Vector Machines (SVM)](#support-vector-machines-svm)
4. [Decision Trees](#decision-trees)
5. [Random Forest](#random-forest)
6. [K-Nearest Neighbors (KNN)](#k-nearest-neighbors-knn)
7. [Naive Bayes](#naive-bayes)
8. [Boosting Trees](#boosting-trees)
9. [Multilayer Perceptron (MLP)](#multilayer-perceptron-mlp)
10. [Convolutional Neural Networks (CNN)](#convolutional-neural-networks-cnn)
11. [Recurrent Neural Networks (RNN) and LSTM](#recurrent-neural-networks-rnn-and-lstm)

[Back to Machine Learning Concepts](#machine-learning-concepts)

[Back to Top](#data-science-cheatsheets)
---

# Linear Regression

Linear Regression is one of the simplest and most widely used techniques in statistics and machine learning. It is a supervised learning algorithm used for regression tasks, where the goal is to predict a continuous output variable based on one or more input features. The objective of linear regression is to model the relationship between the input variables (features) and the output variable (target) by fitting a linear equation to the observed data.

In simple terms, linear regression tries to find the best-fitting straight line (or hyperplane in higher dimensions) that predicts the target variable based on the input features.

## Types of Linear Regression

1. **Simple Linear Regression**: 
   - This involves a single independent variable (X) and a dependent variable (Y).
   - The relationship is modeled as a straight line:  
     \[ Y = \beta_0 + \beta_1 \cdot X + \epsilon \]
   - Where:
     - \( Y \) is the dependent variable (target),
     - \( X \) is the independent variable (feature),
     - \( \beta_0 \) is the intercept, 
     - \( \beta_1 \) is the slope (coefficient),
     - \( \epsilon \) is the error term.

2. **Multiple Linear Regression**:
   - This involves two or more independent variables (features) to predict the dependent variable.
   - The relationship is modeled as:  
     \[ Y = \beta_0 + \beta_1 \cdot X_1 + \beta_2 \cdot X_2 + \cdots + \beta_n \cdot X_n + \epsilon \]
   - Where \( X_1, X_2, \ldots, X_n \) are the independent variables (features).

## Assumptions of Linear Regression

For Linear Regression to give meaningful results, certain assumptions must hold true:

1. **Linearity**: The relationship between the independent and dependent variables should be linear.
2. **Independence**: The residuals (errors) should be independent of each other.
3. **Homoscedasticity**: The variance of errors should be constant across all levels of the independent variable(s).
4. **Normality**: The residuals of the model should be normally distributed.
5. **No multicollinearity**: The independent variables should not be highly correlated with each other.

## Advantages of Linear Regression

- **Simplicity**: Linear regression is easy to understand and interpret.
- **Efficiency**: It is computationally efficient and requires relatively less memory and time to train.
- **Interpretable**: The coefficients provide direct insights into the relationship between variables.

## Disadvantages of Linear Regression

- **Linearity Assumption**: It can only capture linear relationships; complex relationships may not be modeled well.
- **Sensitive to Outliers**: Linear regression is sensitive to outliers, which can skew the results.
- **Multicollinearity**: High correlation between independent variables can cause issues with the model.
[![image](https://github.com/user-attachments/assets/b8ef569c-2b7d-477d-a375-f9c90ebf5e16)
](https://github.com/Adity-star/Data-Science-Work/blob/main/CheatSheets/Visualisations/linear_regression.png)
  - 
[Back to Supervised Algorithms](#supervised-algorithms)

---

# Logistic Regression

Logistic Regression is a supervised machine learning algorithm that is used for classification tasks rather than regression tasks. Despite its name, logistic regression is primarily used for binary classification problems where the output is categorical, typically with two classes or labels. The goal of logistic regression is to predict the probability that a given input belongs to a certain class.

Logistic regression models the probability that a dependent variable \( Y \) belongs to a particular class based on one or more independent variables (features). The output of logistic regression is a probability score between 0 and 1, which is then mapped to a binary label (0 or 1).

## Logistic Function (Sigmoid Function)

The core of logistic regression is the **logistic (sigmoid) function**. The logistic function outputs a probability value between 0 and 1, which is ideal for binary classification. The formula for the logistic function is:

\[
p = \frac{1}{1 + e^{-z}}
\]

Where:
- \( p \) is the probability that the target variable \( Y \) belongs to class 1,
- \( z \) is the linear combination of input features:  
  \[ z = \beta_0 + \beta_1 \cdot X_1 + \beta_2 \cdot X_2 + \cdots + \beta_n \cdot X_n \]
- \( e \) is Euler's number (approximately 2.71828).

The logistic function ensures that the output lies between 0 and 1, making it interpretable as a probability.

## Binary vs. Multinomial Logistic Regression

1. **Binary Logistic Regression**: 
   - This is the most common form of logistic regression, used when the target variable has two possible outcomes (e.g., 0 or 1, Yes or No).
   - The output of the model is a probability score that can be thresholded (e.g., \( p > 0.5 \) for class 1, \( p < 0.5 \) for class 0).

2. **Multinomial Logistic Regression**: 
   - Used when the target variable has more than two classes. The logistic function is extended to handle multiple classes, and each class is compared against a baseline class using a set of coefficients.

## Assumptions of Logistic Regression

For logistic regression to provide meaningful and reliable results, the following assumptions should hold:

1. **Linearity**: There should be a linear relationship between the independent variables and the log-odds of the dependent variable.
2. **Independence of Errors**: The errors (residuals) should be independent.
3. **No Multicollinearity**: The independent variables should not be highly correlated with each other.
4. **Large Sample Size**: Logistic regression typically requires a larger sample size to avoid overfitting and ensure statistical significance.

## Advantages of Logistic Regression

- **Simplicity**: Logistic regression is easy to implement and interpret, especially for binary classification.
- **Probabilistic Output**: It provides a probability estimate for each class, which can be useful for decision-making.
- **Efficient**: It is computationally efficient and works well with linearly separable data.

## Disadvantages of Logistic Regression

- **Linear Decision Boundary**: Logistic regression assumes a linear relationship between the features and the log-odds of the outcome. This may not work well for complex datasets with non-linear relationships.
- **Sensitive to Outliers**: Logistic regression can be sensitive to outliers, which may affect the model's performance.
- **Requires Large Sample Size**: It works better with larger datasets and may not perform well on small datasets with few observations.


[Back to Supervised Algorithms](#supervised-algorithms)

---

# Decision Trees

A **Decision Tree** is a supervised machine learning algorithm used for both classification and regression tasks. It is a tree-like structure where each internal node represents a decision or test on an attribute (feature), each branch represents an outcome of the test, and each leaf node represents a class label or continuous value (in the case of regression).

Decision trees are intuitive and easy to understand, as they resemble a flowchart where decisions are made based on feature values. They are widely used due to their simplicity, interpretability, and ability to handle both numerical and categorical data.

## Key Concepts

1. **Nodes**:
   - **Root Node**: The top-most node in the tree, representing the entire dataset.
   - **Decision Nodes**: Internal nodes that represent tests or decisions based on features.
   - **Leaf Nodes**: Terminal nodes that represent the final decision or outcome (e.g., class label or continuous value in regression).

2. **Splitting**:
   - Splitting refers to dividing the dataset into two or more subsets based on a feature. The goal is to split the data in such a way that the subsets are as pure as possible with respect to the target variable.

3. **Pruning**:
   - Pruning is the process of removing branches from the decision tree that have little importance or are overly specific to the training data, thus preventing overfitting.

4. **Impurity Measures**:
   - Decision trees use different criteria to decide where to split the data. Commonly used impurity measures include:
     - **Gini Impurity**: Measures the "impurity" of a node. The lower the Gini impurity, the purer the node.
     - **Entropy**: A measure of disorder or uncertainty, often used in ID3 (Iterative Dichotomiser 3) algorithm.
     - **Variance (for regression)**: Used to measure the spread of continuous values in the dataset.

5. **Overfitting and Underfitting**:
   - **Overfitting**: Occurs when the tree is too complex, capturing noise and outliers in the training data, leading to poor generalization on new data.
   - **Underfitting**: Occurs when the tree is too simple to capture the underlying patterns in the data.

## Advantages of Decision Trees

- **Interpretability**: Decision trees are easy to visualize and interpret, making them useful for understanding the decision-making process.
- **No Feature Scaling**: Decision trees do not require feature scaling (e.g., normalization or standardization), unlike many other algorithms.
- **Handles Both Numerical and Categorical Data**: Decision trees can handle both types of data without the need for preprocessing.
- **Non-Linear Relationships**: Decision trees are capable of capturing non-linear relationships between features and the target variable.

## Disadvantages of Decision Trees

- **Overfitting**: Decision trees are prone to overfitting, especially if they are deep or have many branches. This can lead to poor generalization to new data.
- **Instability**: Small changes in the data can result in a completely different tree structure, making decision trees sensitive to variations in the training set.
- **Bias**: Decision trees can be biased toward features with more levels (e.g., categorical variables with many distinct values).
- **Computationally Expensive**: For large datasets, building a deep tree can be computationally expensive.

## Pruning a Decision Tree

Pruning is an important step to prevent overfitting. It involves trimming branches that add little value to the model's performance. There are two main types of pruning:
- **Pre-pruning (Early Stopping)**: This involves stopping the tree construction process early before it grows too deep. Stopping criteria like maximum depth or minimum samples per leaf are set.
- **Post-pruning**: After the tree is fully grown, branches are removed if they do not improve model accuracy. Post-pruning can be done using methods like **Cost Complexity Pruning (CCP)** or **Reduced Error Pruning**.

## Hyperparameters of Decision Trees

1. **Max Depth**: The maximum depth of the tree. Limiting depth helps prevent overfitting.
2. **Min Samples Split**: The minimum number of samples required to split an internal node. Increasing this value can make the tree more general.
3. **Min Samples Leaf**: The minimum number of samples required to be at a leaf node. Increasing this value can lead to smoother decision boundaries.
4. **Max Features**: The maximum number of features to consider when looking for the best split.
5. **Criterion**: The function to measure the quality of a split (e.g., **Gini Impurity**, **Entropy**).

[![image](https://github.com/user-attachments/assets/a5806ba8-cfe4-4fc6-8657-a873591c6a48)
](https://github.com/Adity-star/Data-Science-Work/blob/main/CheatSheets/Visualisations/tree.gif)
[Back to Supervised Algorithms](#supervised-algorithms)

---

## Support Vector Machines (SVM)

Support Vector Machines (SVM) is a supervised machine learning algorithm commonly used for classification and regression tasks. However, it is primarily known for its effectiveness in classification problems, particularly for binary classification. SVM is based on the concept of finding a hyperplane (or decision boundary) that best separates data points of different classes in a high-dimensional space.

The key idea behind SVM is to find the optimal hyperplane that maximizes the margin between the closest points of the two classes, known as **support vectors**. This separation allows the model to generalize well to unseen data.

## Key Concepts

1. **Hyperplane**:
   - A hyperplane is a decision boundary that separates data points of different classes. In 2D, it is a line; in 3D, it is a plane; in higher dimensions, it becomes a hyperplane.
   
2. **Support Vectors**:
   - Support vectors are the data points that are closest to the hyperplane. These points are critical as they define the margin and the optimal hyperplane.

3. **Margin**:
   - The margin is the distance between the hyperplane and the support vectors. SVM aims to maximize this margin, as a larger margin implies better generalization.

4. **Kernel Trick**:
   - The kernel trick is a method used in SVM to handle non-linearly separable data by implicitly mapping the input data to a higher-dimensional space where it becomes linearly separable.
   - Common kernel functions include:
     - **Linear Kernel**: No transformation, used when data is linearly separable.
     - **Polynomial Kernel**: Maps data to a higher-dimensional space using a polynomial function.
     - **Radial Basis Function (RBF) Kernel**: Maps data into an infinite-dimensional space using the Gaussian function, commonly used for complex decision boundaries.

## Types of SVM

1. **Linear SVM**:
   - When the data is linearly separable, SVM uses a linear hyperplane to separate the classes.
   - It aims to maximize the margin between the two classes using the support vectors.

2. **Non-Linear SVM**:
   - When data is not linearly separable, SVM uses the kernel trick to transform the data into a higher-dimensional space where a hyperplane can be used to separate the classes.

3. **SVM for Regression (SVR)**:
   - SVM can also be applied to regression tasks, known as **Support Vector Regression (SVR)**. In this case, SVM tries to find a hyperplane that best fits the data while allowing for some margin of error.

## Advantages of SVM

- **Effective in high-dimensional spaces**: SVM performs well in high-dimensional spaces, which makes it suitable for text classification and other problems with many features.
- **Memory efficiency**: Since SVM only relies on the support vectors, it can be more memory efficient compared to other algorithms that use all data points for training.
- **Robust to overfitting**: SVM has good generalization performance, especially in high-dimensional spaces, and can avoid overfitting when the margin is maximized.

## Disadvantages of SVM

- **Computationally expensive**: SVMs can be slow to train, particularly on large datasets, since the algorithm has to compute pairwise distances between data points.
- **Choice of kernel**: The performance of SVM can be highly dependent on the choice of kernel and its parameters. Incorrect kernel choice may lead to poor performance.
- **Difficult to interpret**: SVM models are often seen as "black box" models because the decision boundary is not as easy to interpret as decision trees, for example.

[![image](https://github.com/user-attachments/assets/0efea5d0-c1ed-4fe9-924a-6b5ce3d094f4)
](https://github.com/Adity-star/Data-Science-Work/blob/main/CheatSheets/Visualisations/svm.png)

[Back to Supervised Algorithms](#supervised-algorithms)

---
# Random Forest

A **Random Forest** is an ensemble learning algorithm that combines multiple decision trees to create a stronger, more robust model. It is one of the most powerful machine learning algorithms for both classification and regression tasks. The core idea behind random forests is to build a collection of decision trees, each trained on a random subset of the data, and to combine their predictions to improve accuracy and reduce overfitting.

The key advantage of random forests is their ability to handle large datasets with higher dimensionality and to provide high accuracy without much hyperparameter tuning. Random forests reduce the variance of decision trees by averaging multiple trees, making them less prone to overfitting.

## Key Concepts

1. **Ensemble Learning**:
   - Ensemble learning is a machine learning paradigm where multiple models (often of the same type) are trained and their outputs are combined to improve performance. Random forests are an example of bagging (Bootstrap Aggregating) ensemble methods.
   
2. **Bootstrap Sampling**:
   - Random forests build each decision tree on a different random subset of the training data. This is achieved by bootstrapping, which involves sampling the dataset with replacement, meaning some data points may be repeated while others may be omitted from each sample.

3. **Feature Randomness**:
   - At each node in a decision tree, random forests only consider a random subset of features when making a split. This randomness introduces diversity in the individual trees and helps prevent overfitting.

4. **Aggregation (Voting or Averaging)**:
   - For classification tasks, the final prediction of the random forest is determined by **majority voting** (i.e., the class predicted by most trees). For regression tasks, the final prediction is the **average** of all the tree predictions.

## Advantages of Random Forest

- **High Accuracy**: Random forests generally perform well and provide high accuracy, as they aggregate the results of multiple decision trees.
- **Robustness to Overfitting**: By averaging multiple trees, random forests reduce the risk of overfitting compared to individual decision trees.
- **Handles Missing Values**: Random forests can handle missing values by using surrogate splits (using other features) to make predictions when a value is missing.
- **Feature Importance**: Random forests can provide insights into the importance of different features in making predictions. This can be useful for feature selection and understanding the model.
- **Versatility**: Random forests work well for both classification and regression tasks and can handle high-dimensional data, noisy data, and large datasets.

## Disadvantages of Random Forest

- **Interpretability**: Random forests are often seen as "black box" models because it is difficult to interpret the decisions made by the ensemble of trees. Unlike a single decision tree, it is harder to understand the individual decision-making process.
- **Computationally Expensive**: Building multiple decision trees and storing them can be resource-intensive, both in terms of memory and computation. This makes random forests less suitable for real-time predictions or situations where computation speed is crucial.
- **Slow to Predict**: Because predictions require aggregating the results of multiple trees, random forests can be slower to predict compared to individual decision trees, especially with large datasets and many trees.
- **Risk of Overfitting (with Many Trees)**: While random forests are generally robust to overfitting, an excessively large number of trees may still lead to overfitting, especially if the trees are too deep.

## Hyperparameters of Random Forest

1. **Number of Estimators (n_estimators)**: The number of decision trees in the forest. More trees typically lead to better performance, but they also increase computation time.
2. **Max Depth**: The maximum depth of each decision tree. Limiting the depth helps reduce overfitting and controls model complexity.
3. **Min Samples Split**: The minimum number of samples required to split an internal node. This parameter helps control the growth of the tree and prevents overfitting.
4. **Min Samples Leaf**: The minimum number of samples required to be at a leaf node. Increasing this value can make the model more conservative and reduce overfitting.
5. **Max Features**: The maximum number of features to consider when looking for the best split at each node. Reducing the number of features can increase the randomness of the trees, reducing overfitting.
6. **Bootstrap**: Whether to use bootstrap sampling (sampling with replacement) when creating the trees. This is generally set to `True` in random forests.
7. **Out-of-Bag (OOB) Score**: If set to `True`, the out-of-bag error estimate will be computed for model evaluation.

[Back to Supervised Algorithms](#supervised-algorithms)

---
# K-Nearest Neighbors (KNN)

K-Nearest Neighbors (KNN) is a simple, versatile, and widely used supervised machine learning algorithm for both classification and regression tasks. The main idea behind KNN is to predict the class or value of a data point based on the majority class or average value of its **K** nearest neighbors in the feature space. It is a **lazy learning algorithm**, meaning it does not build an explicit model during training, and predictions are made based on the training data directly during inference.

KNN is non-parametric, meaning it doesn't make any assumptions about the underlying data distribution, making it flexible and useful for various types of problems.

## Key Concepts

1. **Distance Metric**:
   - The core idea of KNN is to measure the distance between data points. The most common distance metric used is **Euclidean distance**, but other distance metrics like **Manhattan**, **Minkowski**, or **Cosine similarity** can also be used depending on the problem.
   
2. **K (Number of Neighbors)**:
   - **K** refers to the number of nearest neighbors that will be used to make a prediction. For classification, the class label that occurs most frequently among the K neighbors is assigned to the data point. For regression, the average of the target values of the K neighbors is used as the prediction.

3. **Majority Voting (for Classification)**:
   - In classification tasks, KNN uses a majority voting approach, where the predicted class label is determined by the most common class label among the K closest points to the query point.

4. **Averaging (for Regression)**:
   - In regression tasks, KNN predicts the target value as the average of the values of the K nearest neighbors.

## Advantages of KNN

- **Simple and Intuitive**: KNN is easy to understand and implement. It is conceptually simple and doesn't require training phase, making it easy to apply.
- **No Assumptions**: KNN does not make any assumptions about the underlying data distribution, making it a non-parametric algorithm.
- **Effective for Small Datasets**: For smaller datasets, KNN can work well and provide a strong baseline model.
- **Versatile**: KNN can be used for both classification and regression tasks.
- **Adaptable**: KNN can be adapted for different distance metrics, depending on the problem at hand.

## Disadvantages of KNN

- **Computationally Expensive**: KNN requires calculating the distance between the query point and all other data points, which can be computationally expensive, especially for large datasets.
- **High Memory Usage**: Since KNN stores the entire training dataset in memory, it can require a lot of memory, particularly when working with large datasets.
- **Sensitive to Irrelevant Features**: KNN is sensitive to the curse of dimensionality. The performance of KNN can degrade as the number of irrelevant or redundant features increases, because the distance between points becomes less meaningful in high-dimensional spaces.
- **Choosing the Right K**: The choice of K can significantly affect the model's performance. A small K can lead to overfitting, while a large K can lead to underfitting.
- **Sensitivity to Noise**: KNN is sensitive to noisy data and outliers, as it directly depends on the proximity of data points.

## Hyperparameters of KNN

1. **K (Number of Neighbors)**: The number of neighbors to consider when making predictions. A smaller K value can make the model more sensitive to noise, while a larger K value can lead to a more generalized model.
2. **Distance Metric**: The function used to calculate the distance between data points. Common choices include **Euclidean**, **Manhattan**, and **Minkowski** distances.
3. **Weights**: Whether all neighbors are weighted equally or whether closer neighbors are given more weight. The parameter can be set to:
   - **Uniform**: All neighbors have equal weight.
   - **Distance**: Closer neighbors have a higher weight.
4. **Algorithm**: The algorithm used to compute the nearest neighbors. Options include:
   - **Ball Tree**: Efficient for high-dimensional data.
   - **KD Tree**: Useful for low-dimensional data.
   - **Brute Force**: A simple but slower approach.
5. **Leaf Size**: A parameter for the tree-based algorithms (Ball Tree or KD Tree), controlling the number of points in a leaf node.

[![image](https://github.com/user-attachments/assets/57458e5e-6c4a-4059-9fd7-1e135ff6c8b7)](https://github.com/Adity-star/Data-Science-Work/blob/main/CheatSheets/Visualisations/knn.png)


[Back to Supervised Algorithms](#supervised-algorithms)

---
# Naive Bayes

**Naive Bayes** is a family of probabilistic algorithms based on **Bayes' Theorem** and is particularly useful for classification tasks. The "naive" aspect of the model comes from the assumption that all features are independent given the class label, which is a simplifying assumption that often works well in practice despite being rarely true in real-world data.

Naive Bayes is popular due to its simplicity, ease of implementation, and efficiency in terms of both computation and memory usage, especially for large datasets. It is particularly well-suited for text classification problems, such as spam filtering, sentiment analysis, and document classification.

## Key Concepts

### Bayes' Theorem
Bayes' Theorem provides a way of calculating the probability of a hypothesis (e.g., a class label) given the observed data (e.g., feature values). The formula is:

\[
P(C | X) = \frac{P(X | C) \cdot P(C)}{P(X)}
\]

Where:
- \( P(C | X) \) is the **posterior probability**, or the probability of class \( C \) given the features \( X \).
- \( P(X | C) \) is the **likelihood**, or the probability of observing the features \( X \) given class \( C \).
- \( P(C) \) is the **prior probability**, or the probability of class \( C \) before seeing the data.
- \( P(X) \) is the **evidence**, or the probability of observing the features \( X \), which serves as a normalizing factor.

### Assumption of Feature Independence
Naive Bayes assumes that the features are conditionally independent, given the class label. This means that the presence or absence of a feature is assumed to be unrelated to the presence or absence of other features, given the class label. While this assumption is often unrealistic in real-world data, it allows Naive Bayes to be computationally efficient.

### Types of Naive Bayes
There are several variations of Naive Bayes, depending on the type of data and how the likelihood is estimated:

1. **Gaussian Naive Bayes**: Assumes that the features are continuous and follow a normal (Gaussian) distribution.
2. **Multinomial Naive Bayes**: Suitable for discrete features, particularly useful for document classification tasks, where the features represent word counts or frequencies.
3. **Bernoulli Naive Bayes**: Suitable for binary/boolean features, where the features are either 0 or 1, indicating the presence or absence of a certain attribute.


## Advantages of Naive Bayes

- **Simple and Efficient**: Naive Bayes is easy to implement and computationally efficient, making it a good choice for large datasets.
- **Works Well with High-Dimensional Data**: Naive Bayes can handle large numbers of features and works well with text classification tasks where the feature space is large (e.g., documents with many words).
- **Fast to Train**: Naive Bayes models are trained quickly as they only require estimating the probabilities (means, variances, or frequencies) from the data.
- **Works Well with Small Datasets**: Since Naive Bayes requires fewer data to make reasonable predictions, it performs well even on smaller datasets.
- **Handles Missing Data**: Naive Bayes can handle missing values by simply ignoring the missing features during the likelihood computation.

## Disadvantages of Naive Bayes

- **Assumption of Feature Independence**: The independence assumption rarely holds true in real-world data, and this can reduce the accuracy of Naive Bayes in some cases.
- **Poor Performance with Highly Correlated Features**: If the features are strongly correlated, Naive Bayes may perform poorly since it treats them as independent.
- **Limited to Classification Tasks**: Naive Bayes is primarily a classification algorithm and is not suitable for regression tasks (though variants exist for some continuous-valued prediction problems).

## Hyperparameters of Naive Bayes

1. **Alpha (Laplace Smoothing)**: This parameter is used in the Multinomial and Bernoulli Naive Bayes models to prevent zero probabilities when a feature is not present in the training data for a given class. The Laplace smoothing parameter \( \alpha \) adds a constant value (usually 1) to the counts of features.
2. **Fit Prior**: A boolean parameter indicating whether to learn class prior probabilities from the data. If set to `False`, equal class priors will be assumed.
3. **Var Smoothing**: In Gaussian Naive Bayes, this parameter adds a small value to the variance of each feature to avoid division by zero errors and improve numerical stability.

[Back to Supervised Algorithms](#supervised-algorithms)

---

# Boosting Trees

**Boosting** is an ensemble learning technique that combines multiple weak learners (typically decision trees) to create a strong learner. The idea behind boosting is to build models sequentially, where each new model corrects the errors made by the previous ones. The most common types of boosting algorithms include **AdaBoost**, **Gradient Boosting**, and **XGBoost**.

Boosting algorithms focus on converting weak models into strong ones by giving more weight to misclassified data points and building new models that emphasize these difficult-to-predict points. Boosting can significantly improve the performance of models by reducing both bias and variance, making it one of the most powerful techniques for classification and regression problems.

## Key Concepts

### Ensemble Learning
Boosting is a type of ensemble learning, where multiple models (weak learners) are combined to create a more robust and accurate model. In boosting, weak learners are trained in sequence, and each learner tries to correct the errors made by the previous one.

### Weak Learners
A weak learner is a model that performs only slightly better than random guessing. Decision trees with a small depth (shallow trees) are commonly used as weak learners in boosting algorithms. While individual weak learners might not be very accurate, combining them effectively can lead to strong predictive performance.

### Sequential Learning Process
Boosting algorithms train models sequentially. After each model is trained, the data points that were misclassified by the previous model are given more weight, so the next model focuses more on correcting those mistakes. This process continues until the maximum number of models is reached or no further improvement is made.

### Overfitting
While boosting algorithms can significantly improve performance, they are also prone to overfitting, especially when too many models are used. Careful tuning of hyperparameters, such as the learning rate and the number of iterations, is essential to prevent overfitting.

## Popular Boosting Algorithms

### AdaBoost (Adaptive Boosting)
AdaBoost was one of the first successful boosting algorithms. It combines weak learners by assigning higher weights to misclassified data points, forcing the next learner to focus on these points.

### Gradient Boosting
Gradient Boosting builds models sequentially by fitting a new model to the residuals (errors) of the previous model. It is widely used for both classification and regression tasks and is more flexible than AdaBoost.


### XGBoost (Extreme Gradient Boosting)
XGBoost is an optimized version of Gradient Boosting that includes additional features to improve performance, such as regularization, parallelization, and better handling of missing data.


### LightGBM (Light Gradient Boosting Machine)
LightGBM is a fast, distributed, high-performance gradient boosting framework based on decision tree algorithms. It is designed for large-scale machine learning tasks and offers faster training times than XGBoost.

## Advantages of Boosting

- **High Accuracy**: Boosting often leads to highly accurate models by combining multiple weak learners to create a strong learner.
- **Robust to Overfitting (with Regularization)**: When properly tuned, boosting models can generalize well to new data and avoid overfitting.
- **Versatile**: Boosting can be used for both classification and regression tasks and works well with various types of data.
- **Effective for Imbalanced Data**: Boosting can handle imbalanced datasets better than other algorithms by focusing on the misclassified data points.

## Disadvantages of Boosting

- **Computationally Expensive**: Boosting algorithms, especially Gradient Boosting and XGBoost, can be computationally intensive and require more time and resources for training compared to simpler models.
- **Prone to Overfitting (Without Regularization)**: Boosting models can overfit if not properly regularized or if the number of iterations is too large.
- **Difficult to Interpret**: Due to the ensemble nature and complexity of boosting models, they can be hard to interpret compared to simpler models like decision trees or logistic regression.

## Hyperparameters of Boosting Algorithms

1. **Learning Rate**: Controls the contribution of each weak learner to the final model. Lower learning rates usually result in better generalization but require more iterations.
2. **Number of Estimators (n_estimators)**: The number of weak learners (e.g., decision trees) to train. More estimators generally lead to better performance but increase computation time.
3. **Maximum Depth**: The maximum depth of individual trees (in Gradient Boosting and XGBoost). Shallow trees are typically used as weak learners in boosting algorithms.
4. **Subsample**: The fraction of the training data used to fit each weak learner. Setting a value less than 1.0 can help prevent overfitting.
5. **Min Samples Split/Leaf**: The minimum number of samples required to split a node or to form a leaf in decision trees. This can help control the complexity of the individual trees.

[Back to Supervised Algorithms](#supervised-algorithms)

---
# Multilayer Perceptron (MLP)

A **Multilayer Perceptron (MLP)** is a type of **Artificial Neural Network (ANN)** that consists of multiple layers of neurons, including an input layer, one or more hidden layers, and an output layer. MLPs are one of the simplest forms of deep learning models and are often used for both classification and regression tasks.

MLPs are powerful because they can learn complex relationships in data through their multiple hidden layers. Each layer in the MLP is made up of units (also known as neurons or nodes) that perform computations. These networks are used for a variety of applications, including image recognition, natural language processing, and time-series forecasting.

## Key Concepts

### Neurons and Layers
- **Neuron (Node)**: A basic unit in an MLP that performs computations. Each neuron receives input, applies weights, passes the result through an activation function, and outputs a value to the next layer.
- **Input Layer**: The layer that receives the input features. Each neuron in this layer represents one feature of the data.
- **Hidden Layers**: One or more layers between the input and output layers. These layers perform computations to learn complex patterns in the data.
- **Output Layer**: The layer that produces the final predictions. The number of neurons in this layer corresponds to the number of output classes (for classification) or a single neuron for regression.

### Activation Functions
Each neuron in an MLP applies an activation function to its input to introduce non-linearity to the model. Without activation functions, the network would simply behave like a linear regression model.

### Feedforward and Backpropagation
- **Feedforward**: The process where input data is passed through the network layer by layer, and the final output is generated.
- **Backpropagation**: The process of adjusting the weights in the network by calculating the gradient of the loss function with respect to each weight and propagating the error back through the network. This is typically done using **gradient descent** or its variants (e.g., stochastic gradient descent).

## Advantages of MLP

- **Ability to Model Non-Linear Relationships**: Due to the non-linear activation functions in the hidden layers, MLPs can model complex relationships in data that are not just linear.
- **Universal Approximation Theorem**: MLPs with a sufficient number of hidden neurons can approximate any continuous function to an arbitrary degree of accuracy, making them extremely powerful for complex tasks.
- **Versatile**: MLPs can be used for both classification and regression tasks, making them a flexible model.
- **Scalability**: MLPs can be scaled to work with large datasets, especially when leveraging modern deep learning frameworks and hardware accelerators (e.g., GPUs).

## Disadvantages of MLP

- **Training Time**: Training an MLP can be computationally expensive, especially with large datasets and many hidden layers. This is because the model has a large number of parameters that need to be updated during backpropagation.
- **Overfitting**: MLPs are prone to overfitting, especially when the model is too complex relative to the amount of data. Regularization techniques like dropout or early stopping can help mitigate this issue.
- **Interpretability**: Like most deep learning models, MLPs are often viewed as "black-box" models, making it difficult to interpret how they make predictions.
- **Require Large Datasets**: MLPs often require a large amount of labeled data to train effectively. For smaller datasets, simpler models might perform better.

## Hyperparameters of MLP

1. **Number of Hidden Layers**: The number of hidden layers in the network. Increasing the number of hidden layers can make the model more powerful, but it also increases the risk of overfitting.
2. **Number of Neurons per Layer**: The number of neurons in each hidden layer. More neurons allow the model to capture more complex patterns, but they also increase the computational cost.
3. **Learning Rate**: The rate at which the model updates its weights during training. A learning rate that is too high can lead to poor convergence, while a learning rate that is too low can slow down the training process.
4. **Batch Size**: The number of samples used in each iteration of gradient descent. Smaller batch sizes lead to more frequent updates, while larger batch sizes lead to more stable estimates of the gradient.
5. **Activation Function**: The activation function used in the hidden layers. Common choices include **ReLU**, **Sigmoid**, and **Tanh**.
6. **Dropout Rate**: The rate at which neurons are randomly dropped during training to prevent overfitting. Dropout helps the model generalize better.
7. **Epochs**: The number of times the entire dataset is passed through the network during training.

[Back to Supervised Algorithms](#supervised-algorithms)

---

# Convolutional Neural Networks (CNN)

**Convolutional Neural Networks (CNNs)** are a class of deep learning algorithms that have proven to be highly effective in analyzing visual data. CNNs are inspired by the human visual processing system and are particularly well-suited for tasks such as image recognition, object detection, and other computer vision problems.

CNNs consist of layers that apply convolutions to input data, followed by pooling layers and fully connected layers. The network automatically learns hierarchical features, starting from low-level features like edges and textures to high-level features like object parts and whole objects.

## Key Concepts

### Convolutional Layer
- **Convolution** is a mathematical operation that applies a filter (or kernel) to an input image or feature map to create a feature map. Each filter detects specific features such as edges, textures, or patterns in the input data.
- **Filter (Kernel)**: A small matrix used to detect specific patterns in the input data. It slides over the input image (or feature map) and performs element-wise multiplication with the input to produce an output.
- **Stride**: The step size with which the filter moves over the input image. A larger stride results in a smaller output feature map.
- **Padding**: The process of adding extra pixels around the border of the input image to preserve the spatial dimensions after applying the convolution.

### Pooling Layer
- **Pooling** is used to reduce the spatial dimensions of the feature map and reduce the number of parameters. This helps prevent overfitting and reduces the computational cost.
- **Max Pooling**: The most common pooling operation, which selects the maximum value from a region of the feature map.
- **Average Pooling**: Selects the average value from a region of the feature map.

### Fully Connected Layer
- After the convolution and pooling layers, the feature maps are flattened into a 1D vector and passed through one or more fully connected layers. These layers are similar to the ones in a regular neural network and are responsible for making the final classification or regression predictions.
- The output layer often uses the **Softmax** activation function in classification tasks to produce probabilities for each class.

### Activation Functions
- **ReLU (Rectified Linear Unit)**: A non-linear activation function that is commonly used in CNNs. It outputs the input if it is positive, otherwise, it outputs zero. ReLU helps introduce non-linearity into the model and allows it to learn complex patterns.
- **Softmax**: Used in the output layer for multi-class classification problems to convert the raw output values into probabilities.

### Dropout and Regularization
- **Dropout**: A technique used to prevent overfitting by randomly dropping a proportion of neurons during training. This forces the network to learn more robust features.
- **Weight Regularization**: Techniques like L2 regularization help prevent overfitting by adding a penalty to the weights, encouraging smaller weights and improving generalization.

## Advantages of CNN

- **Automatic Feature Extraction**: CNNs can automatically learn important features from raw input data, such as edges, textures, and patterns, without the need for manual feature engineering.
- **Spatial Hierarchy**: CNNs are good at capturing the spatial hierarchy in images, meaning they can learn both low-level features (e.g., edges) and high-level features (e.g., objects).
- **Parameter Sharing**: The same filter is applied to different parts of the image, which helps reduce the number of parameters, making CNNs more computationally efficient compared to fully connected networks.
- **Translation Invariance**: By applying convolution and pooling, CNNs become less sensitive to the position of objects in the image, allowing them to recognize objects even if they appear in different locations.
- **Better Performance on Visual Tasks**: CNNs outperform traditional machine learning algorithms like SVM and logistic regression on many computer vision tasks.

## Disadvantages of CNN

- **Computational Cost**: CNNs require significant computational resources, especially for training deep networks with many layers and large datasets. Using GPUs or specialized hardware accelerators like TPUs is often necessary.
- **Need for Large Datasets**: CNNs generally require large labeled datasets to train effectively. They may not perform well on small datasets without data augmentation or transfer learning.
- **Overfitting**: If not properly regularized, CNNs can overfit to the training data, especially when the dataset is small or the model is too complex. Techniques like dropout and weight regularization can help mitigate this issue.

## Hyperparameters of CNN

1. **Number of Filters (Kernels)**: The number of filters used in each convolutional layer. More filters allow the network to capture more features but increase computational cost.
2. **Filter Size**: The dimensions of the filter (e.g., 3x3, 5x5). Smaller filters focus on fine-grained features, while larger filters capture more global patterns.
3. **Stride**: The step size with which the filter moves over the input image. A larger stride reduces the spatial dimensions of the output feature map.
4. **Pooling Size**: The size of the pooling region (e.g., 2x2 or 3x3). Max pooling with a 2x2 region is commonly used.
5. **Dropout Rate**: The fraction of neurons randomly dropped during training to prevent overfitting.
6. **Learning Rate**: The rate at which the model’s weights are updated during training. A learning rate that is too high may result in poor convergence, while a learning rate that is too low may slow down training.

[Back to Supervised Algorithms](#supervised-algorithms)

---
# Recurrent Neural Networks (RNN) and LSTM


**Recurrent Neural Networks (RNNs)** and **Long Short-Term Memory (LSTM)** networks are specialized types of neural networks designed for sequential data, such as time series, speech, or text. Unlike traditional feedforward neural networks, RNNs have connections that form cycles, allowing them to maintain a memory of previous inputs. This makes RNNs particularly well-suited for tasks involving sequential dependencies, such as language modeling, speech recognition, and time-series forecasting.

However, standard RNNs struggle with long-term dependencies due to the **vanishing gradient problem**. To overcome this, **LSTMs**, a type of RNN, were developed. LSTMs are capable of capturing long-term dependencies and are widely used in tasks requiring long-range context.

## Key Concepts

### Recurrent Neural Networks (RNN)
- **Recurrent Connections**: Unlike traditional neural networks, RNNs have loops in their architecture. These loops allow information to persist from one step to another. At each time step, the network takes the current input as well as the previous hidden state as input to generate the next hidden state and output.
  
- **Hidden State**: The hidden state in an RNN stores information about the previous time steps. It serves as the "memory" of the network, allowing it to process sequential data.

- **Backpropagation Through Time (BPTT)**: RNNs are trained using a variant of backpropagation known as BPTT. During BPTT, the error is propagated backward through time to adjust the weights, but this process can lead to issues with long sequences.

- **Vanishing Gradient Problem**: During training, gradients can become extremely small as they are propagated backward through many time steps. This causes the network to "forget" earlier parts of the sequence, especially in long sequences.

### Long Short-Term Memory (LSTM)
- **LSTM Architecture**: LSTM is a type of RNN designed to combat the vanishing gradient problem. It does so by introducing special units called **memory cells**, which can store information over long periods. LSTM cells are controlled by three gates: 
  - **Forget Gate**: Decides what information from the memory cell should be discarded.
  - **Input Gate**: Controls how much new information should be added to the memory cell.
  - **Output Gate**: Determines how much of the information from the memory cell should be passed to the next time step.
  
- **Memory Cells**: The memory cells in LSTMs are capable of retaining information for much longer than the hidden states in traditional RNNs. This allows LSTMs to capture long-term dependencies and handle sequential data more effectively.

- **Gating Mechanism**: The key innovation of LSTM over standard RNNs is the gating mechanism, which regulates the flow of information into and out of the memory cells. This ensures that relevant information is retained while irrelevant information is discarded.

### Key Differences Between RNN and LSTM
- **Vanishing Gradient**: While traditional RNNs struggle with long-term dependencies due to the vanishing gradient problem, LSTMs are designed to avoid this issue by using memory cells and gating mechanisms.
- **Complexity**: LSTMs are more complex than standard RNNs because they have more parameters (i.e., the weights for the gates) and are computationally more expensive.
- **Handling Long-Term Dependencies**: LSTMs are more capable of capturing long-range dependencies compared to RNNs, making them the go-to architecture for many tasks involving sequential data.

## How RNNs and LSTMs Work

1. **Input Sequence**:
   - Both RNNs and LSTMs process sequential data one element at a time. For each input at time step `t`, the model updates its hidden state based on both the current input and the previous hidden state.
   
2. **Hidden State**:
   - In RNNs, the hidden state at each time step is calculated as a function of the previous hidden state and the current input.
   - In LSTMs, the hidden state is updated using the memory cell, which is influenced by the forget, input, and output gates.

3. **Forward Pass**:
   - For each time step, the network takes the input and the previous hidden state (or memory cell state in the case of LSTM) to generate the current output and updated hidden state.
   - In LSTMs, the gates decide how much information should be passed on or forgotten.

4. **Backpropagation**:
   - The error is backpropagated through the sequence using **Backpropagation Through Time (BPTT)** to update the model's parameters. In the case of LSTM, the error is also backpropagated through the memory cells and gates.

## Advantages of RNNs and LSTMs

### RNNs:
- **Modeling Sequential Data**: RNNs are capable of handling sequential data, which makes them suitable for tasks such as language modeling, machine translation, and time series prediction.
- **Parameter Sharing**: RNNs share weights across all time steps, making them parameter-efficient when working with sequential data.

### LSTMs:
- **Capturing Long-Term Dependencies**: LSTMs excel in capturing long-range dependencies in sequences, which is something traditional RNNs struggle with.
- **Handling Complex Sequential Data**: LSTMs are highly effective for tasks that require understanding of long-term patterns, such as sentiment analysis, speech recognition, and language translation.
- **Mitigating Vanishing Gradient**: LSTMs address the vanishing gradient problem through their gating mechanisms, ensuring the network can learn from longer sequences without losing important information.

## Disadvantages of RNNs and LSTMs

- **Computational Complexity**: LSTMs are more computationally expensive than RNNs due to the additional complexity introduced by the memory cells and gates.
- **Training Time**: Both RNNs and LSTMs can be slow to train, especially on long sequences or large datasets, because of the need for backpropagation through time.
- **Overfitting**: Like other deep learning models, RNNs and LSTMs are prone to overfitting, particularly when training on small datasets. Regularization techniques such as dropout can help mitigate this issue.

## Hyperparameters of RNNs and LSTMs

1. **Number of Layers**: The number of recurrent layers in the model. Deeper networks can model more complex patterns, but may be harder to train and prone to overfitting.
2. **Hidden Units**: The number of hidden units (neurons) in each layer. More units can increase the capacity of the model but also increase computational cost.
3. **Learning Rate**: The rate at which the model’s parameters are updated during training. A good learning rate ensures fast convergence without overshooting.
4. **Sequence Length**: The number of time steps used in the input sequence. In practice, sequences are often truncated or padded to a fixed length.
5. **Batch Size**: The number of samples processed in each training step. Larger batch sizes result in faster training but may require more memory.
6. **Dropout Rate**: The fraction of neurons randomly dropped during training to prevent overfitting.
7. **Optimizer**: The optimization algorithm used to minimize the loss function. Common choices for RNNs and LSTMs include **Adam**, **RMSprop**, and **SGD**.

[Back to Supervised Algorithms](#supervised-algorithms)

[Back to Machine Learning Concepts](#machine-learning-concepts)

[Back to Top](#data-science-cheatsheets)
---











