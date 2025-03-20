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

[Back to Hypothesis Testing](#hypothesis-test) | [Back to Statistics and Probability](#statistics-and-probability)

[Back to Top](#data-science-cheatsheets)
---

# Machine Learning Concepts

Machine learning is a subfield of artificial intelligence that deals with algorithms and statistical models that enable computers to perform tasks without explicit instructions. This document provides an overview of core machine learning concepts, algorithms, metrics, and advanced topics.

## Table of Contents
- [Machine Learning Basics](#machine-learning-basics)
- [Supervised Algorithms](#supervised-algorithms)
- [Unsupervised Algorithms](#unsupervised-algorithms)
- [Metrics](#metrics)
- [Advanced Concepts](#advanced-concepts)

---
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

---

# Supervised Learning Algorithms

Supervised learning is a type of machine learning where the model is trained using labeled data. The goal is to learn a mapping from inputs to the outputs based on a set of training data.

## Table of Contents
1. [Linear Regression](#linear-regression)
2. [Logistic Regression](#logistic-regression)
3. [Support Vector Machines (SVM)](#support-vector-machines-svm)
4. [Decision Trees](#decision-trees)
5. [Random Forest](#random-forest)
6. [k-Nearest Neighbors (k-NN)](#k-nearest-neighbors-knn)
7. [Naive Bayes](#naive-bayes)
8. [References](#references)

---

## Linear Regression

Linear Regression is a statistical method that models the relationship between a dependent variable and one or more independent variables by fitting a linear equation to observed data.

- **Equation:**  
  The model assumes the relationship is linear:  
  \[
  y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + ... + \beta_n x_n + \epsilon
  \]
  Where:
  - \( y \) is the dependent variable.
  - \( x_1, x_2, ... x_n \) are the features.
  - \( \beta_0, \beta_1, ... \beta_n \) are the coefficients.
  - \( \epsilon \) is the error term.

- **References:**
  - [Linear Regression - Wikipedia](https://en.wikipedia.org/wiki/Linear_regression)
  - [Introduction to Linear Regression - Towards Data Science](https://towardsdatascience.com/introduction-to-linear-regression-9c2cc73c7229)

---

## Logistic Regression

Logistic Regression is used for binary classification problems. Unlike linear regression, it uses a logistic function to model a probability distribution and make decisions based on thresholds.

- **Equation:**
  The logistic function is given by:
  \[
  p(y = 1 | X) = \frac{1}{1 + e^{-(\beta_0 + \beta_1 x_1 + \beta_2 x_2 + ... + \beta_n x_n)}}
  \]
  Where \( p(y=1) \) is the probability of the output being class 1, and the terms are similar to linear regression.

- **References:**
  - [Logistic Regression - Wikipedia](https://en.wikipedia.org/wiki/Logistic_regression)
  - [Logistic Regression Explained - Analytics Vidhya](https://www.analyticsvidhya.com/blog/2015/10/basics-logistic-regression/)

---

## Support Vector Machines (SVM)

Support Vector Machines are powerful classifiers that work by finding a hyperplane that best separates the data points of different classes.

- **Key Idea:**
  - SVM tries to maximize the margin between two classes. The "support vectors" are the points that define the margin.
  - SVM can also be extended to nonlinear problems using the kernel trick.

- **References:**
  - [Support Vector Machine - Wikipedia](https://en.wikipedia.org/wiki/Support_vector_machine)
  - [A Guide to Support Vector Machines - Machine Learning Mastery](https://machinelearningmastery.com/support-vector-machines-for-machine-learning/)

---

## Decision Trees

Decision Trees are a non-linear model used for classification and regression tasks. They recursively split the data based on feature values that lead to the best prediction.

- **Key Idea:**
  - Decision trees use a greedy approach to make decisions at each node by choosing the feature that best splits the data.
  - Common algorithms: ID3, CART, C4.5

- **References:**
  - [Decision Tree - Wikipedia](https://en.wikipedia.org/wiki/Decision_tree_learning)
  - [Understanding Decision Trees - Towards Data Science](https://towardsdatascience.com/understanding-decision-trees-54e0f5f282bc)

---

## Random Forest

Random Forest is an ensemble learning method that combines multiple decision trees to improve the accuracy of predictions. Each tree is built using a random subset of features and data.

- **Key Idea:**
  - Random Forest works by averaging multiple decision trees' predictions to reduce variance.
  - It is less prone to overfitting compared to a single decision tree.

- **References:**
  - [Random Forest - Wikipedia](https://en.wikipedia.org/wiki/Random_forest)
  - [Random Forests - Machine Learning Mastery](https://machinelearningmastery.com/random-forest-ensemble-in-python/)

---

## k-Nearest Neighbors (k-NN)

k-Nearest Neighbors is a simple, non-parametric algorithm used for classification and regression. It makes predictions based on the k-nearest data points in the feature space.

- **Key Idea:**
  - For classification, the majority class among the nearest k neighbors is chosen as the predicted class.
  - For regression, the average of the k nearest neighbors' values is used as the prediction.

- **References:**
  - [k-Nearest Neighbors - Wikipedia](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm)
  - [k-NN Algorithm - Towards Data Science](https://towardsdatascience.com/the-k-nearest-neighbors-algorithm-9c7b013c1e1b)

---

## Naive Bayes

Naive Bayes is a family of probabilistic classifiers based on Bayes' Theorem. It assumes that the features are conditionally independent given the class.

- **Key Idea:**
  - The Naive Bayes classifier calculates the probability of a class given the features, using Bayes' theorem:
  \[
  P(C|X) = \frac{P(X|C)P(C)}{P(X)}
  \]
  Where:
  - \( P(C|X) \) is the posterior probability of class \( C \) given features \( X \).
  - \( P(X|C) \) is the likelihood of features given class \( C \).
  - \( P(C) \) is the prior probability of class \( C \).
  - \( P(X) \) is the evidence (the probability of the features).

- **References:**
  - [Naive Bayes - Wikipedia](https://en.wikipedia.org/wiki/Naive_Bayes_classifier)
  - [Naive Bayes Classifier - Towards Data Science](https://towardsdatascience.com/naive-bayes-classifier-344a7da3d85e)

---

## References

1. [Introduction to Supervised Learning - GeeksforGeeks](https://www.geeksforgeeks.org/supervised-learning/)
2. [Supervised Learning Algorithms - Towards Data Science](https://towardsdatascience.com/supervised-learning-algorithms-3e5f5b6b88b2)

---

End of Document.













