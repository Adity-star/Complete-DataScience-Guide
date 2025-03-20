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
* [Probability Distributions](#probability-distributions)
* [Central Limit Theorem](#central-limit-theorem)
* [Hypothesis Test](#hypothesis-test)

[Back to Top](#data-science-cheatsheets)

### Measure of central Tendency
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

[Back to Top](#statistics-and-probability)
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

  [Back to Top](#statistics-and-probability)
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
  
[Back to Top](#statistics-and-probability)
---


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

[Back to Top](#statistics-and-probability)

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

[Back to Continuous Probability Distributions](#continuous-probability-distributions) | [Back to Probability Distributions](#probability-distributions)

---

#### [Back to Top](#data-science-cheatsheets)

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

#### [Back to Top](#data-science-cheatsheets)
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

[Back to Hypothesis Testing](#hypothesis-test) | [Back to Statistics and Probability](#statistics-and-probability)

#### [Back to Top](#data-science-cheatsheets)

