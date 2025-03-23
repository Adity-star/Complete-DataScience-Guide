# Machine Learning - List of questions

## Learning Theory

#### 1. [Describe bias and variance with examples](#answer-1)
#### 2. [What is Empirical Risk Minimization?](#answer-2)
#### 3. [What is Union bound and Hoeffding's inequality?](#answer-3)
#### 4. [Write the formulae for training error and generalization error. Point out the differences.](#answer-4)
#### 5. [State the uniform convergence theorem and derive it.](#answer-5)
## 6. [What is sample complexity bound of uniform convergence theorem?](#answer-6)
#### 7. [What is error bound of uniform convergence theorem?](#answer-7)
#### 8. [What is the bias-variance trade-off theorem?](#answer-8)
#### 9. [From the bias-variance trade-off, can you derive the bound on training set size?](#answer-9)
#### 10. [What is the VC dimension?](#answer-10)
#### 11. [What does the training set size depend on for a finite and infinite hypothesis set? Compare and contrast.](#answer-11)
#### 12. [What is the VC dimension for an n-dimensional linear classifier?](#answer-12)
#### 13. [How is the VC dimension of a SVM bounded although it is projected to an infinite dimension?](#answer-13)
#### 14. [Considering that Empirical Risk Minimization is a NP-hard problem, how does logistic regression and SVM loss work?](#answer-14)


## Model and feature selection
1. Why are model selection methods needed?
1. How do you do a trade-off between bias and variance?
1. What are the different attributes that can be selected by model selection methods?
1. Why is cross-validation required?
1. Describe different cross-validation techniques.
1. What is hold-out cross validation? What are its advantages and disadvantages?
1. What is k-fold cross validation? What are its advantages and disadvantages?
1. What is leave-one-out cross validation? What are its advantages and disadvantages?
1. Why is feature selection required?
1. Describe some feature selection methods.
1. What is forward feature selection method? What are its advantages and disadvantages?
1. What is backward feature selection method? What are its advantages and disadvantages?
1. What is filter feature selection method and describe two of them?
1. What is mutual information and KL divergence?
1. Describe KL divergence intuitively.

## Curse of dimensionality 
1. Describe the curse of dimensionality with examples.
1. What is local constancy or smoothness prior or regularization?

## Universal approximation of neural networks
1. State the universal approximation theorem? What is the technique used to prove that?
1. What is a Borel measurable function?
1. Given the universal approximation theorem, why can't a MLP still reach a arbitrarily small positive error?

## Deep Learning motivation
1. What is the mathematical motivation of Deep Learning as opposed to standard Machine Learning techniques?
1. In standard Machine Learning vs. Deep Learning, how is the order of number of samples related to the order of regions that can be recognized in the function space?
1. What are the reasons for choosing a deep model as opposed to shallow model? (1. Number of regions O(2^k) vs O(k) where k is the number of training examples 2. # linear regions carved out in the function space depends exponentially on the depth. )
1. How Deep Learning tackles the curse of dimensionality? 

## Support Vector Machine
1. How can the SVM optimization function be derived from the logistic regression optimization function?
1. What is a large margin classifier?
1. Why SVM is an example of a large margin classifier?
1. SVM being a large margin classifier, is it influenced by outliers? (Yes, if C is large, otherwise not)
1. What is the role of C in SVM?
1. In SVM, what is the angle between the decision boundary and theta?
1. What is the mathematical intuition of a large margin classifier?
1. What is a kernel in SVM? Why do we use kernels in SVM?
1. What is a similarity function in SVM? Why it is named so?
1. How are the landmarks initially chosen in an SVM? How many and where?
1. Can we apply the kernel trick to logistic regression? Why is it not used in practice then?
1. What is the difference between logistic regression and SVM without a kernel? (Only in implementation – one is much more efficient and has good optimization packages)
1. How does the SVM parameter C affect the bias/variance trade off? (Remember C = 1/lambda; lambda increases means variance decreases)
1. How does the SVM kernel parameter sigma^2 affect the bias/variance trade off?
1. Can any similarity function be used for SVM? (No, have to satisfy Mercer’s theorem)
1. Logistic regression vs. SVMs: When to use which one? 
( Let's say n and m are the number of features and training samples respectively. If n is large relative to m use log. Reg. or SVM with linear kernel, If n is small and m is intermediate, SVM with Gaussian kernel, If n is small and m is massive, Create or add more fetaures then use log. Reg. or SVM without a kernel)

## Bayesian Machine Learning
1. What are the differences between “Bayesian” and “Freqentist” approach for Machine Learning?
1. Compare and contrast maximum likelihood and maximum a posteriori estimation.
1. How does Bayesian methods do automatic feature selection?
1. What do you mean by Bayesian regularization?
1. When will you use Bayesian methods instead of Frequentist methods? (Small dataset, large feature set)

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

