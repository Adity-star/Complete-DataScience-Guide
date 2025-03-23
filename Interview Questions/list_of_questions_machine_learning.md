# Machine Learning - List of questions

## [Learning Theory](#learning-theory)

1.Describe bias and variance with examples.
2.What is Empirical Risk Minimization?
3.What is Union bound and Hoeffding's inequality?
4.Write the formulae for training error and generalization error. Point out the differences.
5.State the uniform convergence theorem and derive it.
6.What is sample complexity bound of uniform convergence theorem?
7.What is error bound of uniform convergence theorem?
8.What is the bias-variance trade-off theorem?
9.From the bias-variance trade-off, can you derive the bound on training set size?
10.What is the VC dimension?
11.What does the training set size depend on for a finite and infinite hypothesis set? Compare and contrast.
12.What is the VC dimension for an n-dimensional linear classifier?
13.How is the VC dimension of a SVM bounded although it is projected to an infinite dimension?
14.Considering that Empirical Risk Minimization is a NP-hard problem, how does logistic regression and SVM loss work?


---

## Model Selection and Feature Selection

#### 1. [Why are model selection methods needed?](#answer-15)
#### 2. [How do you do a trade-off between bias and variance?](#answer-16)
#### 3. [What are the different attributes that can be selected by model selection methods?](#answer-17)
#### 4. [Why is cross-validation required?](#answer-18)
#### 5. [Describe different cross-validation techniques.](#answer-19)
#### 6. [What is hold-out cross validation? What are its advantages and disadvantages?](#answer-20)
#### 7. [What is k-fold cross validation? What are its advantages and disadvantages?](#answer-21)
#### 8. [What is leave-one-out cross validation? What are its advantages and disadvantages?](#answer-22)
#### 9. [Why is feature selection required?](#answer-23)
#### 10. [Describe some feature selection methods.](#answer-24)
#### 11. [What is forward feature selection method? What are its advantages and disadvantages?](#answer-25)
#### 12. [What is backward feature selection method? What are its advantages and disadvantages?](#answer-26)
#### 13. [What is filter feature selection method and describe two of them?](#answer-27)
#### 14. [What is mutual information and KL divergence?](#answer-28)
#### 15. [Describe KL divergence intuitively.](#answer-29)

## Curse of Dimensionality and Universal Approximation of Neural Networks

#### 1. [Describe the curse of dimensionality with examples.](#answer-30)
#### 2. [What is local constancy or smoothness prior or regularization?](#answer-31)
#### 3. [State the universal approximation theorem? What is the technique used to prove that?](#answer-32)
#### 4. [What is a Borel measurable function?](#answer-33)
#### 5. [Given the universal approximation theorem, why can't an MLP still reach an arbitrarily small positive error?](#answer-34)

---

## Deep Learning Motivation

#### 1. [What is the mathematical motivation of Deep Learning as opposed to standard Machine Learning techniques?](#answer-35)
#### 2. [In standard Machine Learning vs. Deep Learning, how is the order of number of samples related to the order of regions that can be recognized in the function space?](#answer-36)
#### 3. [What are the reasons for choosing a deep model as opposed to shallow model? (1. Number of regions O(2^k) vs O(k) where k is the number of training examples 2. # linear regions carved out in the function space depends exponentially on the depth.)](#answer-37)
#### 4. [How Deep Learning tackles the curse of dimensionality?](#answer-38)

## Support Vector Machine

#### 1. [How can the SVM optimization function be derived from the logistic regression optimization function?](#answer-39)
#### 2. [What is a large margin classifier?](#answer-40)
#### 3. [Why SVM is an example of a large margin classifier?](#answer-41)
#### 4. [SVM being a large margin classifier, is it influenced by outliers? (Yes, if C is large, otherwise not)](#answer-42)
#### 5. [What is the role of C in SVM?](#answer-43)
#### 6. [In SVM, what is the angle between the decision boundary and theta?](#answer-44)
#### 7. [What is the mathematical intuition of a large margin classifier?](#answer-45)
#### 8. [What is a kernel in SVM? Why do we use kernels in SVM?](#answer-46)
#### 9. [What is a similarity function in SVM? Why is it named so?](#answer-47)
#### 10. [How are the landmarks initially chosen in an SVM? How many and where?](#answer-48)
#### 11. [Can we apply the kernel trick to logistic regression? Why is it not used in practice then?](#answer-49)
#### 12. [What is the difference between logistic regression and SVM without a kernel? (Only in implementation – one is much more efficient and has good optimization packages)](#answer-50)
#### 13. [How does the SVM parameter C affect the bias/variance trade off? (Remember C = 1/lambda; lambda increases means variance decreases)](#answer-51)
#### 14. [How does the SVM kernel parameter sigma^2 affect the bias/variance trade off?](#answer-52)
#### 15. [Can any similarity function be used for SVM? (No, have to satisfy Mercer’s theorem)](#answer-53)
#### 16. [Logistic regression vs. SVMs: When to use which one?](#answer-54)

## Bayesian Machine Learning

#### 1. [What are the differences between “Bayesian” and “Frequentist” approach for Machine Learning?](#answer-55)
#### 2. [Compare and contrast maximum likelihood and maximum a posteriori estimation.](#answer-56)
#### 3. [How does Bayesian methods do automatic feature selection?](#answer-57)
#### 4. [What do you mean by Bayesian regularization?](#answer-58)
#### 5. [When will you use Bayesian methods instead of Frequentist methods? (Small dataset, large feature set)](#answer-59)


## Regularization

#### 1. [What is L1 regularization?](#answer-60)
#### 2. [What is L2 regularization?](#answer-61)
#### 3. [Compare L1 and L2 regularization.](#answer-62)
#### 4. [Why does L1 regularization result in sparse models?](#answer-63)

## Evaluation of Machine Learning systems

#### 1. [What are accuracy, sensitivity, specificity, ROC?](#answer-64)
#### 2. [What are precision and recall?](#answer-65)
#### 3. [Describe t-test in the context of Machine Learning.](#answer-66)

## Clustering

#### 1. [Describe the k-means algorithm.](#answer-67)
#### 2. [What is distortion function? Is it convex or non-convex?](#answer-68)
#### 3. [Tell me about the convergence of the distortion function.](#answer-69)
#### 4. [Topic: EM algorithm](#answer-70)
#### 5. [What is the Gaussian Mixture Model?](#answer-71)
#### 6. [Describe the EM algorithm intuitively.](#answer-72)
#### 7. [What are the two steps of the EM algorithm?](#answer-73)
#### 8. [Compare GMM vs GDA.](#answer-74)

## Dimensionality Reduction

#### 1. [Why do we need dimensionality reduction techniques? (data compression, speeds up learning algorithm and visualizing data)](#answer-75)
#### 2. [What do we need PCA and what does it do? (PCA tries to find a lower dimensional surface such that the sum of the squared projection error is minimized)](#answer-76)
#### 3. [What is the difference between logistic regression and PCA?](#answer-77)
#### 4. [What are the two pre-processing steps that should be applied before doing PCA? (mean normalization and feature scaling)](#answer-78)

## Basics of Natural Language Processing

#### 1. [What is WORD2VEC?](#answer-79)
#### 2. [What is t-SNE? Why do we use PCA instead of t-SNE?](#answer-80)
#### 3. [What is sampled softmax?](#answer-81)
#### 4. [Why is it difficult to train a RNN with SGD?](#answer-82)
#### 5. [How do you tackle the problem of exploding gradients? (By gradient clipping)](#answer-83)
#### 6. [What is the problem of vanishing gradients? (RNN doesn't tend to remember much things from the past)](#answer-84)
#### 7. [How do you tackle the problem of vanishing gradients? (By using


## Miscellaneous
1. What is the difference between loss function, cost function and objective function?


---
# Machine Learning - List of questions and answers

## Learning Theory

#### 1. [Describe bias and variance with examples](#describe-bias-and-variance-with-examples)
**Answer**: 
Bias refers to the error introduced by approximating a real-world problem with a simplified model. High bias leads to underfitting. Variance refers to the model's sensitivity to small fluctuations in the training set. High variance leads to overfitting. For example, a linear regression model with few features (high bias) vs. a decision tree with many splits (high variance).

#### 2. [What is Empirical Risk Minimization?](#answer-2)
**Answer**: 
Empirical Risk Minimization (ERM) is a principle that aims to minimize the average loss (or error) on a given training set. It finds the model parameters that minimize the training error, assuming that the training data is a good representation of the true distribution.

#### 3. [What is Union bound and Hoeffding's inequality?](#answer-3)
**Answer**: 
Union bound is a probability inequality that provides an upper bound on the probability of the union of events. Hoeffding’s inequality gives a bound on the probability that the sum of random variables deviates from its expected value, providing confidence in how closely the empirical mean approximates the true mean.

#### 4. [Write the formulae for training error and generalization error. Point out the differences.](#answer-4)
**Answer**: 
Training error is the average error over the training set, while generalization error is the expected error over the true distribution. Mathematically:
- Training error: \( \hat{R}(h) = \frac{1}{m} \sum_{i=1}^{m} L(h(x_i), y_i) \)
- Generalization error: \( R(h) = \mathbb{E}_{(X,Y)} [L(h(X), Y)] \)
Where \( h \) is the hypothesis, \( L \) is the loss function, and \( (x_i, y_i) \) are the training examples.

#### 5. [State the uniform convergence theorem and derive it.](#answer-5)
**Answer**: 
The uniform convergence theorem states that, with high probability, the empirical risk converges to the true risk uniformly across all hypotheses in a hypothesis class as the number of training samples increases. It implies that a hypothesis class with a low bound on uniform convergence will generalize well to unseen data.

#### 6. [What is sample complexity bound of uniform convergence theorem?](#answer-6)
**Answer**: 
The sample complexity bound indicates the number of training samples required for a hypothesis class to have a uniform convergence property. Typically, it scales as \( O\left(\frac{1}{\epsilon^2} \log\frac{1}{\delta}\right) \), where \( \epsilon \) is the error tolerance and \( \delta \) is the confidence level.

#### 7. [What is error bound of uniform convergence theorem?](#answer-7)
**Answer**: 
The error bound indicates how much the empirical risk can deviate from the true risk. It gives a probability that the error of a hypothesis will exceed a certain value based on the size of the sample set and the complexity of the hypothesis class.

#### 8. [What is the bias-variance trade-off theorem?](#answer-8)
**Answer**: 
The bias-variance trade-off theorem states that as a model becomes more complex (lower bias), it tends to overfit (higher variance), while simpler models (higher bias) generalize better but may underfit. The optimal model complexity minimizes both bias and variance.

#### 9. [From the bias-variance trade-off, can you derive the bound on training set size?](#answer-9)
**Answer**: 
From the trade-off, we derive that the training set size should increase with model complexity to prevent overfitting and underfitting. Typically, to reduce variance, the sample size must be large enough to ensure that the model can generalize well while controlling bias.

#### 10. [What is the VC dimension?](#answer-10)
**Answer**: 
The VC (Vapnik-Chervonenkis) dimension is a measure of the capacity of a hypothesis class. It is the largest number of points that can be shattered (classified in all possible ways) by the hypothesis class.

#### 11. [What does the training set size depend on for a finite and infinite hypothesis set? Compare and contrast.](#answer-11)
**Answer**: 
For a finite hypothesis set, the training set size is generally small and depends on the complexity of the model. For an infinite hypothesis set, the training set size must be large enough to ensure that the model generalizes well. The sample size required grows with the VC dimension.

#### 12. [What is the VC dimension for an n-dimensional linear classifier?](#answer-12)
**Answer**: 
The VC dimension of an n-dimensional linear classifier is \( n+1 \). This is because an n-dimensional hyperplane can separate data points in a way that it can shatter \( n+1 \) points, but not more.

#### 13. [How is the VC dimension of a SVM bounded although it is projected to an infinite dimension?](#answer-13)
**Answer**: 
The VC dimension of a Support Vector Machine (SVM) is bounded due to the regularization constraints imposed by the SVM’s optimization process. The kernel trick allows for high-dimensional projections, but the hypothesis class's complexity is controlled by the regularization parameter \( C \).

#### 14. [Considering that Empirical Risk Minimization is a NP-hard problem, how does logistic regression and SVM loss work?](#answer-14)
**Answer**: 
Although Empirical Risk Minimization (ERM) is NP-hard, logistic regression and SVMs simplify the problem by using convex loss functions. For logistic regression, the loss is convex in terms of model parameters, and SVM uses a quadratic loss, both of which ensure efficient optimization.

---

**[Back to top](#machine-learning---list-of-questions)**

---

## Model Selection and Feature Selection

#### 1. [Why are model selection methods needed?](#answer-15)
**Answer**: 
Model selection methods are needed to choose the best model based on performance metrics. These methods help to avoid overfitting, underfitting, and ensure that the chosen model generalizes well to unseen data.

#### 2. [How do you do a trade-off between bias and variance?](#answer-16)
**Answer**: 
The trade-off between bias and variance is balanced by choosing an appropriate model complexity. Simple models have high bias and low variance, while complex models have low bias and high variance. Cross-validation and regularization are methods to control this trade-off.

#### 3. [What are the different attributes that can be selected by model selection methods?](#answer-17)
**Answer**: 
Model selection methods focus on selecting attributes such as feature importance, model complexity, hyperparameters, and regularization strength to improve model performance.

#### 4. [Why is cross-validation required?](#answer-18)
**Answer**: 
Cross-validation is required to estimate the performance of a model on unseen data. It helps to reduce overfitting by using different training and validation subsets, ensuring the model’s generalizability.

#### 5. [Describe different cross-validation techniques.](#answer-19)
**Answer**: 
Common cross-validation techniques include:
- **K-fold cross-validation**: Splits data into k subsets and trains on k-1 subsets while validating on the remaining subset.
- **Leave-one-out cross-validation (LOO-CV)**: Uses a single data point as validation and the rest as training data.
- **Holdout cross-validation**: Randomly splits the dataset into training and validation sets.

#### 6. [What is hold-out cross validation? What are its advantages and disadvantages?](#answer-20)
**Answer**: 
Hold-out cross-validation splits the dataset into training and validation sets once. It is computationally efficient but may lead to higher variance in performance estimates compared to k-fold cross-validation.

#### 7. [What is k-fold cross validation? What are its advantages and disadvantages?](#answer-21)
**Answer**: 
K-fold cross-validation splits the data into k subsets, training the model k times, each time using a different subset for validation. It provides more reliable performance estimates than hold-out but is computationally more expensive.

#### 8. [What is leave-one-out cross validation? What are its advantages and disadvantages?](#answer-22)
**Answer**: 
Leave-one-out cross-validation (LOO-CV) uses one data point for validation and the rest for training. It has low bias and works well for small datasets but is computationally expensive for large datasets.

#### 9. [Why is feature selection required?](#answer-23)
**Answer**: 
Feature selection is required to reduce dimensionality, improve model performance, reduce overfitting, and enhance interpretability by selecting only the most relevant features.

#### 10. [Describe some feature selection methods.](#answer-24)
**Answer**: 
Feature selection methods include:
- **Filter methods**: Evaluate each feature independently using statistical tests (e.g., correlation).
- **Wrapper methods**: Use a learning algorithm to assess feature subsets.
- **Embedded methods**: Perform feature selection during model training (e.g., L1 regularization).

#### 11. [What is forward feature selection method? What are its advantages and disadvantages?](#answer-25)
**Answer**: 
Forward feature selection starts with no features and adds features iteratively based on performance improvement. It is simple and efficient but may miss feature interactions and lead to overfitting.

#### 12. [What is backward feature selection method? What are its advantages and disadvantages?](#answer-26)
**Answer**: 
Backward feature selection starts with all features and removes the least important ones iteratively. It is computationally expensive but can lead to better feature sets by eliminating irrelevant features.

#### 13. [What is filter feature selection method and describe two of them?](#answer-27)
**Answer**: 
Filter methods select features based on statistical tests, independent of any learning algorithm. Two common methods are:
- **Chi-square test**: Evaluates the independence of each feature with the target.
- **Mutual information**: Measures the dependency between features and the target.

#### 14. [What is mutual information and KL divergence?](#answer-28)
**Answer**: 
Mutual information measures the amount of information shared between two variables. KL divergence is a measure of how one probability distribution diverges from a second, expected probability distribution.

#### 15. [Describe KL divergence intuitively.](#answer-29)
**Answer**: 
KL divergence quantifies the difference between two probability distributions, indicating how much information is lost when approximating one distribution with another.

---

**[Back to top](#machine-learning---list-of-questions)**

---

## Curse of Dimensionality and Universal Approximation of Neural Networks

#### 1. [Describe the curse of dimensionality with examples.](#answer-30)
**Answer**: 
The curse of dimensionality refers to the exponential growth of volume in a space as dimensions increase. For example, in high-dimensional spaces, data points become sparse, leading to increased computational costs and difficulty in finding meaningful patterns.

#### 2. [What is local constancy or smoothness prior or regularization?](#answer-31)
**Answer**: 
Local constancy or smoothness prior assumes that functions should not change drastically over small regions. This regularization technique ensures that the model behaves smoothly, preventing overfitting and improving generalization.

#### 3. [State the universal approximation theorem? What is the technique used to prove that?](#answer-32)
**Answer**: 
The universal approximation theorem states that a feedforward neural network with one hidden layer can approximate any continuous function on compact subsets of \( \mathbb{R}^n \). The proof uses tools from functional analysis and the Stone-Weierstrass theorem.

#### 4. [What is a Borel measurable function?](#answer-33)
**Answer**: 
A Borel measurable function is a function whose domain and codomain are equipped with the Borel σ-algebra, making it measurable with respect to the standard Borel measures.

#### 5. [Given the universal approximation theorem, why can't an MLP still reach an arbitrarily small positive error?](#answer-34)
**Answer**: 
While an MLP can approximate any function arbitrarily well, achieving arbitrarily small error in practice requires an infinite number of neurons. In practice, a finite number of neurons limits the ability to reach an arbitrarily small error.

---

**[Back to top](#machine-learning---list-of-questions)**

---

## Deep Learning Motivation

#### 1. [What is the mathematical motivation of Deep Learning as opposed to standard Machine Learning techniques?](#answer-35)
**Answer**: 
Deep Learning leverages layered structures (neural networks) that can model complex, high-dimensional patterns. Unlike traditional methods like linear regression, deep learning can capture non-linear relationships and hierarchies of features, leading to better performance in tasks like image recognition and natural language processing.

#### 2. [In standard Machine Learning vs. Deep Learning, how is the order of number of samples related to the order of regions that can be recognized in the function space?](#answer-36)
**Answer**: 
In standard machine learning, the number of regions that can be recognized grows linearly with the number of samples. In deep learning, the number of regions grows exponentially with depth, enabling deep models to capture more complex patterns.

#### 3. [What are the reasons for choosing a deep model as opposed to shallow model?](#answer-37)
**Answer**: 
Deep models are chosen over shallow models due to their ability to capture hierarchical structures in data. Deep learning models can learn complex patterns from raw data, whereas shallow models often require manual feature engineering.

#### 4. [How Deep Learning tackles the curse of dimensionality?](#answer-38)
**Answer**: 
Deep learning addresses the curse of dimensionality by using hierarchical layers that learn to represent data at multiple levels of abstraction. This allows deep networks to focus on the most relevant features while reducing the impact of irrelevant ones.

---

**[Back to top](#machine-learning---list-of-questions)**

---

  


