# Machine Learning - List of questions

## Learning Theory

#### 1. [Describe bias and variance with examples](#answer-1)
#### 2. [What is Empirical Risk Minimization?](#answer-2)
#### 3. [What is Union bound and Hoeffding's inequality?](#answer-3)
#### 4. [Write the formulae for training error and generalization error. Point out the differences.](#answer-4)
#### 5. [State the uniform convergence theorem and derive it.](#answer-5)
#### 6. [What is sample complexity bound of uniform convergence theorem?](#answer-6)
#### 7. [What is error bound of uniform convergence theorem?](#answer-7)
#### 8. [What is the bias-variance trade-off theorem?](#answer-8)
#### 9. [From the bias-variance trade-off, can you derive the bound on training set size?](#answer-9)
#### 10. [What is the VC dimension?](#answer-10)
#### 11. [What does the training set size depend on for a finite and infinite hypothesis set? Compare and contrast.](#answer-11)
#### 12. [What is the VC dimension for an n-dimensional linear classifier?](#answer-12)
#### 13. [How is the VC dimension of a SVM bounded although it is projected to an infinite dimension?](#answer-13)
#### 14. [Considering that Empirical Risk Minimization is a NP-hard problem, how does logistic regression and SVM loss work?](#answer-14)


---


## Model Selection and Feature Selection

#### 1. [Why are model selection methods needed?](#answer-1)
#### 2. [How do you do a trade-off between bias and variance?](#answer-2)
#### 3. [What are the different attributes that can be selected by model selection methods?](#answer-3)
#### 4. [Why is cross-validation required?](#answer-4)
#### 5. [Describe different cross-validation techniques.](#answer-5)
#### 6. [What is hold-out cross validation? What are its advantages and disadvantages?](#answer-6)
#### 7. [What is k-fold cross validation? What are its advantages and disadvantages?](#answer-7)
#### 8. [What is leave-one-out cross validation? What are its advantages and disadvantages?](#answer-8)
#### 9. [Why is feature selection required?](#answer-9)
#### 10. [Describe some feature selection methods.](#answer-10)
#### 11. [What is forward feature selection method? What are its advantages and disadvantages?](#answer-11)
#### 12. [What is backward feature selection method? What are its advantages and disadvantages?](#answer-12)
#### 13. [What is filter feature selection method and describe two of them?](#answer-13)
#### 14. [What is mutual information and KL divergence?](#answer-14)
#### 15. [Describe KL divergence intuitively.](#answer-15)

## Curse of Dimensionality and Universal Approximation of Neural Networks

#### 1. [Describe the curse of dimensionality with examples.](#answer-1)
#### 2. [What is local constancy or smoothness prior or regularization?](#answer-2)
#### 3. [State the universal approximation theorem? What is the technique used to prove that?](#answer-3)
#### 4. [What is a Borel measurable function?](#answer-4)
#### 5. [Given the universal approximation theorem, why can't an MLP still reach an arbitrarily small positive error?](#answer-5)

---

## Deep Learning Motivation

#### 1. [What is the mathematical motivation of Deep Learning as opposed to standard Machine Learning techniques?](#answer-1)
#### 2. [In standard Machine Learning vs. Deep Learning, how is the order of number of samples related to the order of regions that can be recognized in the function space?](#answer-2)
#### 3. [What are the reasons for choosing a deep model as opposed to shallow model? (1. Number of regions O(2^k) vs O(k) where k is the number of training examples 2. # linear regions carved out in the function space depends exponentially on the depth.)](#answer-3)
#### 4. [How Deep Learning tackles the curse of dimensionality?](#answer-4)

## Support Vector Machine

#### 1. [How can the SVM optimization function be derived from the logistic regression optimization function?](#answer-1)
#### 2. [What is a large margin classifier?](#answer-2)
#### 3. [Why SVM is an example of a large margin classifier?](#answer-3)
#### 4. [SVM being a large margin classifier, is it influenced by outliers? (Yes, if C is large, otherwise not)](#answer-4)
#### 5. [What is the role of C in SVM?](#answer-5)
#### 6. [In SVM, what is the angle between the decision boundary and theta?](#answer-6)
#### 7. [What is the mathematical intuition of a large margin classifier?](#answer-7)
#### 8. [What is a kernel in SVM? Why do we use kernels in SVM?](#answer-8)
#### 9. [What is a similarity function in SVM? Why is it named so?](#answer-9)
#### 10. [How are the landmarks initially chosen in an SVM? How many and where?](#answer-10)
#### 11. [Can we apply the kernel trick to logistic regression? Why is it not used in practice then?](#answer-11)
#### 12. [What is the difference between logistic regression and SVM without a kernel? (Only in implementation – one is much more efficient and has good optimization packages)](#answer-12)
#### 13. [How does the SVM parameter C affect the bias/variance trade off? (Remember C = 1/lambda; lambda increases means variance decreases)](#answer-13)
#### 14. [How does the SVM kernel parameter sigma^2 affect the bias/variance trade off?](#answer-14)
#### 15. [Can any similarity function be used for SVM? (No, have to satisfy Mercer’s theorem)](#answer-15)
#### 16. [Logistic regression vs. SVMs: When to use which one?](#answer-16)

## Bayesian Machine Learning

#### 1. [What are the differences between “Bayesian” and “Frequentist” approach for Machine Learning?](#answer-1)
#### 2. [Compare and contrast maximum likelihood and maximum a posteriori estimation.](#answer-2)
#### 3. [How does Bayesian methods do automatic feature selection?](#answer-3)
#### 4. [What do you mean by Bayesian regularization?](#answer-4)
#### 5. [When will you use Bayesian methods instead of Frequentist methods? (Small dataset, large feature set)](#answer-5)


## Regularization
1. What is L1 regularization?
1. What is L2 regularization?
1. Compare L1 and L2 regularization.
1. Why does L1 regularization result in sparse models? [here](https://stats.stackexchange.com/questions/45643/why-l1-norm-for-sparse-models)

## Evaluation of Machine Learning systems
1. What are accuracy, sensitivity, specificity, ROC?
1. What are precision and recall?
1. Describe t-test in the context of Machine Learning.

## Clustering
1. Describe the k-means algorithm.
1. What is distortion function? Is it convex or non-convex?
1. Tell me about the convergence of the distortion function.
1. Topic: EM algorithm
1. What is the Gaussian Mixture Model?
1. Describe the EM algorithm intuitively. 
1. What are the two steps of the EM algorithm
1. Compare GMM vs GDA.

## Dimensionality Reduction
1. Why do we need dimensionality reduction techniques? (data compression, speeds up learning algorithm and visualizing data)
1. What do we need PCA and what does it do? (PCA tries to find a lower dimensional surface such the sum of the squared projection error is minimized)
1. What is the difference between logistic regression and PCA?
1. What are the two pre-processing steps that should be applied before doing PCA? (mean normalization and feature scaling)

## Basics of Natural Language Processing
1. What is WORD2VEC?
1. What is t-SNE? Why do we use PCA instead of t-SNE?
1. What is sampled softmax?
1. Why is it difficult to train a RNN with SGD?
1. How do you tackle the problem of exploding gradients? (By gradient clipping)
1. What is the problem of vanishing gradients? (RNN doesn't tend to remember much things from the past)
1. How do you tackle the problem of vanishing gradients? (By using LSTM)
1. Explain the memory cell of a LSTM. (LSTM allows forgetting of data and using long memory when appropriate.)
1. What type of regularization do one use in LSTM?
1. What is Beam Search?
1. How to automatically caption an image? (CNN + LSTM)

## Miscellaneous
1. What is the difference between loss function, cost function and objective function?


---

### Answer 1: [Describe bias and variance with examples](#answer-1)
- **Bias**: The error introduced by approximating a real-world problem with a simplified model. Example: Using a linear model for non-linear data causes high bias because the model is too simple.
- **Variance**: The error due to the model's sensitivity to small fluctuations in the training data. Example: A very complex model that overfits to the training data may have high variance and perform poorly on unseen data.

---

### Answer 2: [What is Empirical Risk Minimization?](#answer-2)
Empirical Risk Minimization (ERM) is a principle in machine learning where the model aims to minimize the average error on the training set. Essentially, it seeks to minimize the empirical risk (i.e., the average loss) over the given dataset.

---

### Answer 3: [What is Union bound and Hoeffding's inequality?](#answer-3)
- **Union Bound**: A probability bound that provides an upper limit for the probability of the union of multiple events. For events \( A \) and \( B \), \( P(A \cup B) \leq P(A) + P(B) \).
- **Hoeffding's Inequality**: A statistical tool that provides a bound on the probability that the sum of random variables deviates from its expected value. It is often used for large sample sizes to analyze how much the observed mean deviates from the expected mean.

---

### Answer 4: [Write the formulae for training error and generalization error. Point out the differences.](#answer-4)
- **Training error**: \( \hat{L}_{\text{train}} = \frac{1}{N} \sum_{i=1}^{N} \ell(f(x_i), y_i) \)
- **Generalization error**: \( \hat{L}_{\text{gen}} = \mathbb{E}[\ell(f(x), y)] \)
  
The **training error** is calculated on the training data, while the **generalization error** measures how well the model performs on unseen data. Generalization error is typically more important for assessing model performance.

---

### Answer 5: [State the uniform convergence theorem and derive it.](#answer-5)
The uniform convergence theorem states that as the number of samples increases, the empirical risk (error on the training set) converges uniformly to the true risk (error on the entire distribution) for all hypotheses in the hypothesis class. The derivation involves bounding the deviation of the empirical risk from the true risk using concentration inequalities.

---

### Answer 6: [What is sample complexity bound of uniform convergence theorem?](#answer-6)
The sample complexity bound of the uniform convergence theorem provides the number of samples required to ensure that the empirical risk approximates the true risk with high probability. This is typically bounded as \( O\left(\frac{1}{\epsilon^2} \log \frac{1}{\delta}\right) \), where \( \epsilon \) is the error tolerance and \( \delta \) is the confidence level.

---

### Answer 7: [What is error bound of uniform convergence theorem?](#answer-7)
The error bound of the uniform convergence theorem provides a limit on how far the empirical risk can be from the true risk. The probability that this deviation exceeds some threshold \( \epsilon \) is bounded by \( \delta \), i.e., \( P(\hat{L} - L > \epsilon) \leq \delta \), ensuring that the model generalizes well.

---

### Answer 8: [What is the bias-variance trade-off theorem?](#answer-8)
The bias-variance trade-off theorem suggests that there is a trade-off between the complexity of the model and its ability to generalize. Increasing model complexity reduces bias (leading to a better fit to training data) but increases variance (making it more sensitive to noise and overfitting). The optimal model balances both to minimize total error.

---

### Answer 9: [From the bias-variance trade-off, can you derive the bound on training set size?](#answer-9)
The training set size is critical in managing the bias-variance trade-off. A larger training set reduces variance by providing more representative data, thus preventing overfitting. From the trade-off, a bound on the training set size can be derived based on the desired error and confidence levels, often related to the complexity of the hypothesis class.

---

### Answer 10: [What is the VC dimension?](#answer-10)
The VC (Vapnik-Chervonenkis) dimension is a measure of the capacity of a hypothesis class. It represents the largest set of points that can be shattered by a hypothesis class, meaning that the hypothesis class can correctly classify all possible labelings of those points.

---

### Answer 11: [What does the training set size depend on for a finite and infinite hypothesis set? Compare and contrast.](#answer-11)
- **Finite hypothesis set**: The training set size typically depends on the number of hypotheses and their complexity. It grows logarithmically with the number of hypotheses.
- **Infinite hypothesis set**: The training set size grows significantly larger, typically requiring \( O(1/\epsilon^2) \) samples to avoid overfitting and ensure good generalization.

---

### Answer 12: [What is the VC dimension for an n-dimensional linear classifier?](#answer-12)
The VC dimension of an \( n \)-dimensional linear classifier is \( n + 1 \). This means that an \( n \)-dimensional linear classifier can shatter any set of \( n + 1 \) points in general position.

---

### Answer 13: [How is the VC dimension of a SVM bounded although it is projected to an infinite dimension?](#answer-13)
The VC dimension of an SVM is bounded despite the kernel potentially mapping data to an infinite-dimensional space due to the regularization term and the specific form of the kernel. The capacity of the SVM is controlled by the regularization parameter, preventing it from overfitting the data.

---

### Answer 14: [Considering that Empirical Risk Minimization is a NP-hard problem, how does logistic regression and SVM loss work?](#answer-14)
Despite ERM being NP-hard, **logistic regression** and **SVM** use convex loss functions (like log-loss and hinge loss), which allows for efficient optimization. These convex functions ensure that the optimization problem can be solved efficiently and guarantees finding the global minimum without the need for exhaustive search.

### Answer 1: [Why are model selection methods needed?](#answer-1)
Model selection methods are needed to choose the best-performing model from a set of candidate models. They help optimize the model's performance and ensure that it generalizes well to unseen data. The goal is to avoid overfitting or underfitting by selecting a model that balances complexity and performance.

---

### Answer 2: [How do you do a trade-off between bias and variance?](#answer-2)
The trade-off between bias and variance is done by selecting a model that balances the two:
- **High bias**: Occurs with underfitting, where the model is too simple and fails to capture the underlying pattern.
- **High variance**: Occurs with overfitting, where the model is too complex and fits the training data very well but performs poorly on unseen data.
You can manage the trade-off by tuning model complexity or using techniques like regularization, cross-validation, or increasing the training data.

---

### Answer 3: [What are the different attributes that can be selected by model selection methods?](#answer-3)
Model selection methods can select attributes like:
- **Hyperparameters**: Parameters of the model that are not learned during training, like the learning rate or the number of layers in a neural network.
- **Model type**: The algorithm to use, such as linear regression, decision trees, or support vector machines.
- **Feature selection**: Which features or input variables to use for training the model.
  
---

### Answer 4: [Why is cross-validation required?](#answer-4)
Cross-validation is required to estimate the generalization ability of a model. It helps to ensure that the model performs well not just on the training data but also on unseen data. Cross-validation mitigates the risk of overfitting by using different subsets of the data for training and validation.

---

### Answer 5: [Describe different cross-validation techniques.](#answer-5)
Some common cross-validation techniques are:
- **Hold-out**: Split the dataset into training and test sets.
- **k-fold**: Divide the data into k equal parts, using one part for testing and the rest for training, rotating through all k parts.
- **Leave-one-out**: Use one data point for testing and the rest for training, repeated for all data points.

---

### Answer 6: [What is hold-out cross validation? What are its advantages and disadvantages?](#answer-6)
**Hold-out cross-validation** splits the data into two sets: a training set and a test set. The model is trained on the training set and tested on the test set.

- **Advantages**: Simple and fast to implement.
- **Disadvantages**: The performance estimate depends heavily on how the data is split. It may not be as reliable as other methods with smaller datasets.

---

### Answer 7: [What is k-fold cross validation? What are its advantages and disadvantages?](#answer-7)
**k-fold cross-validation** divides the data into k equal parts, trains the model on k-1 parts, and tests it on the remaining part. This process is repeated k times, with each part used for testing once.

- **Advantages**: Provides a better estimate of model performance by averaging over k test sets.
- **Disadvantages**: Computationally expensive, especially for large datasets.

---

### Answer 8: [What is leave-one-out cross validation? What are its advantages and disadvantages?](#answer-8)
**Leave-one-out cross-validation** (LOOCV) uses each data point as a test set while training the model on the remaining data points. This is repeated for each data point in the dataset.

- **Advantages**: Uses all data points for both training and testing, leading to a very reliable estimate.
- **Disadvantages**: Computationally expensive, as it requires training and testing the model n times, where n is the number of data points.

---

### Answer 9: [Why is feature selection required?](#answer-9)
Feature selection is required to improve model performance by removing irrelevant or redundant features, reducing the model complexity, and preventing overfitting. It also helps in making the model more interpretable and reduces computation time.

---

### Answer 10: [Describe some feature selection methods.](#answer-10)
Some feature selection methods include:
- **Filter methods**: Evaluate features independently of the model, using statistical tests like correlation or mutual information.
- **Wrapper methods**: Evaluate features by training a model with different subsets of features and selecting the best-performing subset.
- **Embedded methods**: Perform feature selection during the model training process, such as Lasso regression.

---

### Answer 11: [What is forward feature selection method? What are its advantages and disadvantages?](#answer-11)
**Forward feature selection** starts with no features and adds features one by one, selecting the feature that improves the model's performance the most.

- **Advantages**: Simple and easy to implement. It can be very effective for models with many features.
- **Disadvantages**: Can be computationally expensive, especially for large datasets. It may also miss interactions between features.

---

### Answer 12: [What is backward feature selection method? What are its advantages and disadvantages?](#answer-12)
**Backward feature selection** starts with all features and removes the least useful features one by one.

- **Advantages**: Often more accurate than forward selection because it considers all features initially.
- **Disadvantages**: Computationally expensive, as it requires training a model for each feature subset.

---

### Answer 13: [What is filter feature selection method and describe two of them?](#answer-13)
**Filter methods** evaluate features independently of the model. Two examples include:
- **Chi-square test**: Tests the independence between each feature and the target variable.
- **Correlation coefficient**: Measures the linear relationship between a feature and the target, selecting features with the highest correlation.

---

### Answer 14: [What is mutual information and KL divergence?](#answer-14)
- **Mutual Information**: A measure of the amount of information that one variable provides about another. It quantifies the reduction in uncertainty of one variable given the knowledge of another.
- **KL Divergence**: A measure of how one probability distribution diverges from a second, expected probability distribution. It quantifies the difference between two distributions.

---

### Answer 15: [Describe KL divergence intuitively.](#answer-15)
KL Divergence measures how much information is lost when approximating one probability distribution by another. If the distributions are the same, the KL divergence is zero. If the distributions are very different, the KL divergence will be large, indicating a significant difference in the information content of the two distributions.
---
## PCA 

### Answer 1: [Describe the curse of dimensionality with examples.](#answer-1)
The **curse of dimensionality** refers to the exponential growth of computational complexity and the need for exponentially more data as the number of dimensions (features) in a dataset increases. For example:
- **In machine learning**, when you have more features, the volume of the feature space grows exponentially, which means that data points become sparse and harder to generalize over.
- **In clustering**, when the data has many features, the distance between any two data points becomes similar, making it difficult to distinguish between clusters.

---

### Answer 2: [What is local constancy or smoothness prior or regularization?](#answer-2)
The **local constancy** or **smoothness prior** is a regularization technique used in machine learning models where the model is encouraged to have small variations in output when the input changes slightly. This assumption helps in preventing overfitting by assuming that the underlying function is smooth and continuous. For instance, in image processing, regularization can be used to avoid sharp transitions between neighboring pixels.

---

### Answer 3: [State the universal approximation theorem? What is the technique used to prove that?](#answer-3)
The **universal approximation theorem** states that a feedforward neural network with a single hidden layer containing a finite number of neurons can approximate any continuous function, given appropriate activation functions and enough neurons. The technique used to prove this theorem involves **constructing a series of simple functions** that converge to any given continuous function by adjusting the weights and biases in the network.

---

### Answer 4: [What is a Borel measurable function?](#answer-4)
A **Borel measurable function** is a function that maps elements from a topological space (often real numbers) to a set of values such that the pre-image of any Borel set is also a Borel set. This property ensures that the function is compatible with the structure of the space and is important in measure theory, making it useful for defining integrals, probabilities, and expectations in many areas of mathematics.

---

### Answer 5: [Given the universal approximation theorem, why can't an MLP still reach an arbitrarily small positive error?](#answer-5)
While the **universal approximation theorem** guarantees that a multi-layer perceptron (MLP) can approximate any continuous function, it does not imply that the network can always achieve **arbitrarily small positive error**. This is because:
- **Optimization issues**: Finding the optimal parameters is a complex non-convex problem, and the network may get stuck in local minima during training.
- **Insufficient training data**: The network may not have enough data or iterations to reach an arbitrarily small error.
- **Computational constraints**: There may be limitations in terms of the number of neurons, layers, or training time that prevent reaching the theoretically minimal error.

---
## Deep learning


### Answer 1: [What is the mathematical motivation of Deep Learning as opposed to standard Machine Learning techniques?](#answer-1)
Deep Learning's mathematical motivation stems from the ability to model highly complex, non-linear relationships in data through hierarchical feature extraction. Unlike standard machine learning techniques, which rely on manually crafted features or shallow models, deep learning models learn to automatically extract relevant features at multiple levels of abstraction. The key advantage is that deep models can learn from raw data (e.g., images, audio) without requiring explicit feature engineering.

---

### Answer 2: [In standard Machine Learning vs. Deep Learning, how is the order of number of samples related to the order of regions that can be recognized in the function space?](#answer-2)
In **standard machine learning**, the number of regions that can be recognized in the function space grows linearly with the number of samples, meaning that with each additional sample, the number of regions is limited by the model's simplicity. However, in **deep learning**, the number of regions that can be recognized grows exponentially with the number of layers and neurons in the model. This allows deep models to capture a much richer, more complex set of patterns and representations as the number of samples increases.

---

### Answer 3: [What are the reasons for choosing a deep model as opposed to shallow model? (1. Number of regions O(2^k) vs O(k) where k is the number of training examples 2. # linear regions carved out in the function space depends exponentially on the depth.)](#answer-3)
Deep models are chosen over shallow models due to several reasons:
1. **Number of regions**: With a shallow model, the number of distinct regions the model can recognize is \( O(k) \), where \( k \) is the number of training examples, meaning it has limited capacity to capture complex decision boundaries. In contrast, deep models allow for exponentially more regions \( O(2^k) \), providing much greater flexibility in capturing intricate patterns.
2. **Exponential increase in linear regions**: The number of linear regions in the function space grows exponentially with the depth of the model. Deep models, therefore, have a significantly higher capacity to model complex, non-linear relationships compared to shallow models, which are limited in the number of regions they can define.

---

### Answer 4: [How Deep Learning tackles the curse of dimensionality?](#answer-4)
Deep Learning tackles the **curse of dimensionality** by learning hierarchical feature representations at different levels of abstraction. Rather than trying to directly model high-dimensional input data, deep networks break the data down into lower-dimensional representations at each layer, progressively capturing relevant patterns while ignoring irrelevant variations. This allows deep models to work effectively in high-dimensional spaces, where traditional machine learning methods struggle due to the exponential growth in the amount of data needed for generalization.
---

## SVM
---

### Answer 1: [How can the SVM optimization function be derived from the logistic regression optimization function?](#answer-1)
SVM optimization can be derived from logistic regression by viewing logistic regression as a probabilistic method that minimizes a loss function (cross-entropy), while SVM aims to maximize the margin between classes. The logistic regression loss function, when combined with a regularization term, can resemble the optimization objective of SVM, which tries to find a hyperplane that maximizes the margin between classes.

---

### Answer 2: [What is a large margin classifier?](#answer-2)
A **large margin classifier** is a machine learning model that seeks to find a decision boundary (hyperplane) that maximizes the margin (distance) between the closest points of different classes (support vectors). Maximizing the margin helps in improving generalization and reducing overfitting.

---

### Answer 3: [Why is SVM an example of a large margin classifier?](#answer-3)
SVM is considered a large margin classifier because it explicitly aims to maximize the margin between the two classes in the feature space. By doing so, it tries to find the hyperplane that provides the largest possible distance between the closest points (support vectors) of each class.

---

### Answer 4: [SVM being a large margin classifier, is it influenced by outliers? (Yes, if C is large, otherwise not)](#answer-4)
Yes, SVM is influenced by outliers, but the extent depends on the parameter \( C \). When \( C \) is large, the model becomes more sensitive to outliers, as it tries to minimize the classification error on the training data. If \( C \) is small, the model becomes more tolerant of outliers, allowing for a larger margin and focusing more on generalization.

---

### Answer 5: [What is the role of C in SVM?](#answer-5)
The **parameter \( C \)** controls the trade-off between maximizing the margin and minimizing the classification error. A larger \( C \) makes the SVM focus more on minimizing misclassifications, which can lead to overfitting, while a smaller \( C \) allows for a larger margin, potentially leading to underfitting.

---

### Answer 6: [In SVM, what is the angle between the decision boundary and theta?](#answer-6)
The angle between the decision boundary and the vector \( \theta \) (the weight vector in SVM) is perpendicular, as the decision boundary is defined by the equation \( \theta \cdot x + b = 0 \). The vector \( \theta \) defines the orientation of the hyperplane, and the decision boundary is orthogonal to this vector.

---

### Answer 7: [What is the mathematical intuition of a large margin classifier?](#answer-7)
Mathematically, a large margin classifier maximizes the distance between the decision boundary (hyperplane) and the closest points (support vectors) of the classes. The margin is defined as \( \frac{1}{||\theta||} \), and the classifier maximizes this margin while minimizing the misclassification error, which is the core idea behind SVM.

---

### Answer 8: [What is a kernel in SVM? Why do we use kernels in SVM?](#answer-8)
A **kernel** in SVM is a function that computes the inner product of two vectors in a high-dimensional feature space, without explicitly transforming the data into that space (the "kernel trick"). Kernels are used to efficiently compute decision boundaries in complex, non-linear spaces without the need to explicitly map data to higher dimensions.

---

### Answer 9: [What is a similarity function in SVM? Why is it named so?](#answer-9)
A **similarity function** in SVM measures the similarity between two data points in the feature space. It is called a similarity function because it quantifies how similar two data points are to each other. Common similarity functions include the linear kernel, polynomial kernel, and Gaussian (RBF) kernel.

---

### Answer 10: [How are the landmarks initially chosen in an SVM? How many and where?](#answer-10)
Landmarks in SVM are initially chosen as the **support vectors**, which are the data points closest to the decision boundary. These support vectors determine the optimal hyperplane. The number of support vectors depends on the data and the parameter \( C \), and they are located along the margin, where the decision boundary separates the two classes.

---

### Answer 11: [Can we apply the kernel trick to logistic regression? Why is it not used in practice then?](#answer-11)
While the kernel trick can theoretically be applied to logistic regression, it is not commonly used because:
1. **Computational Complexity**: The kernel trick requires computing a similarity matrix between all data points, which can be computationally expensive for large datasets.
2. **Optimization**: Logistic regression is designed for probabilistic classification, and applying kernels in this context complicates the optimization process.

---

### Answer 12: [What is the difference between logistic regression and SVM without a kernel? (Only in implementation – one is much more efficient and has good optimization packages)](#answer-12)
Logistic regression and SVM without a kernel are both linear classifiers, but SVM typically has better optimization algorithms for finding the optimal hyperplane with large margin, especially for small datasets. Logistic regression is generally faster and easier to implement, especially when the dataset is large.

---

### Answer 13: [How does the SVM parameter C affect the bias/variance trade off? (Remember C = 1/lambda; lambda increases means variance decreases)](#answer-13)
The parameter \( C \) controls the bias-variance trade-off in SVM:
- **Large \( C \)**: The model becomes more sensitive to misclassification errors, reducing bias but increasing variance.
- **Small \( C \)**: The model allows some misclassification to achieve a larger margin, reducing variance but increasing bias.

---

### Answer 14: [How does the SVM kernel parameter \( \sigma^2 \) affect the bias/variance trade off?](#answer-14)
The kernel parameter \( \sigma^2 \) controls the spread of the kernel function (e.g., Gaussian kernel). A smaller \( \sigma^2 \) leads to a more localized kernel, making the model more sensitive to small variations in the data, increasing variance and reducing bias. A larger \( \sigma^2 \) makes the kernel broader, reducing variance but increasing bias.

---

### Answer 15: [Can any similarity function be used for SVM? (No, have to satisfy Mercer’s theorem)](#answer-15)
No, not all similarity functions can be used in SVM. The similarity function (kernel) must satisfy **Mercer's theorem**, which ensures that the kernel function corresponds to a valid inner product in some feature space.

---

### Answer 16: [Logistic regression vs. SVMs: When to use which one?](#answer-16)
- If \( n \) (number of features) is large relative to \( m \) (number of samples), use **logistic regression** or **SVM with a linear kernel**.
- If \( n \) is small and \( m \) is intermediate, use **SVM with a Gaussian kernel**.
- If \( n \) is small and \( m \) is massive, **create or add more features** and then use **logistic regression** or **SVM without a kernel**.

  ---
  


