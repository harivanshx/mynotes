

we use deepp learning for the problems related to , 
- 
- There is no deterministic algorithm in deep learniing for 3d recognition , 
- handwriting recognition 
- speech recognition 
Problems that dont have a fix sol and goal keep changes
ex - It security framework , finance fraud, Spam Filter

wehre solution are specific or timedependent 
- recomentation and targated advertisement
- Where solution are indevidual specific or time dependennt 
- to get the large pot to buy
Prediction based on past and exostomg pattersm
not defined or defined by huge patterns


### deep learning will not replace human 
it will leave room for humans 


Deep Learning has not and will not be able to explicitly replace humans.

Its role will be more of an implicit partnership.

It will leave room for humans to think smarter (hopefully) and innovate more.

As many programmers fear, Deep Learning or Artificial Intelligence will not replace their jobs
but will instead help them to write better software.

Availability of Data
has increased due
to explosion in
Smart Mobiles and
devices

Release/development
of new algorithms,
APIs and Platforms
for Deep Learning
Applications

More Computing
Power is
available due to
coming of
NVIDIA GPUs


Essential Tools

• Git and Github
• Python
• Jupyter Notebooks
• Numpy for Matrix and Vector calculations
• Pandas for Data handling, curation and manipulation
• Matplotlib for plotting of graphs for different analysis on data
• So many other Python APIs to make your life easy to develop DL models


![[Pasted image 20251217200625.png]]



![[Pasted image 20251217200644.png]]

![[Pasted image 20251217200947.png]]

Weights

Weights correspond to each feature.
Weights denote how much the feature matters in the model.
Higher weight of a particular feature means that it is more important in
deciding the outcome of the model.

Weights of a feature represent that how much evidence it gives in favor or
against the current hypothesis in context of the existence or non-existence
of the pattern you are trying to identify in the current input.

Generally weights are initialized randomly.
we try to bring them to near optimal values so that they are able to fit the
model well and can help in prediction of unseen values

# [[Linear Regression]] and [[Logistic Regression]]



Linear Regression: For applications where output will be a real
value e.g. Predicting housing price, or predicting price of a
share in stock market. In most cases we have multiple
dependent variables, and we call it multiple linear regression

[[Logistic Regression]]: For applications where the output will be a binary value (0/1). E.g. whether this Medical Image depicts
Tumor or not


![[Pasted image 20251217201919.png]]


[[Linearity]] Vs. [[Non-Linearity]]

Simple multiplication of weights with inputs and giving the outputs will be linear
function.

A linear function is just a polynomial of one degree and will not be able to learn
complex functions.

Linear functions don’t have much expressive power and will loose out when
solving complex problems.

Without activation functions (which will help us to achieve non-linearity) Neural
Network will not be able to learn unstructured data like images, audio data,
videos and text.


- Without activation functions (which will help us to achieve non-linearity) Neural Network will not be able to learn unstructured data like images, audio data, videos and text.

[[Neural Network]] with one hidden Neuron
and one hidden layer


![[Pasted image 20251217202514.png]]

Activation Functions

Output from every neuron is generated after applying activation Function to the
values being calculated with set of inputs and their weights.

Most Popular Activation Functions are ReLU ( Rectified Linear Units) and
Sigmoid, Softmax and tanh

Activation functions should be differentiable. Non-linear Activation functions
help you to bring non-linearity in the system

To transform/squash your input to a different space/domain and do some kind of
thresholding

![[Pasted image 20251217204422.png]]


![[Pasted image 20251217210406.png]]


for hidden layer for just one layer 


![[Pasted image 20251217210447.png]]


Cost function is for whole input 




![[Pasted image 20251217210627.png]]

![[Pasted image 20251217210639.png]]

the angles are telling us the slope 




B is bias and also we can say intercept , it is the default value of the program 
It allows the model to say **YES or NO even when all inputs are zero**.

z=w1​x1​+w2​x2​+⋯+w5​x5​+b

![[Pasted image 20251217212427.png]]





Activation Functions: tanh
Tanh activation function is more preferred than the sigmoid function.
It is the shifted version of sigmoid function with a mean value of zero.
It has better centering effect for the activation function to be used on the hidden layer.
For binary classification problem at the output layer we use the Sigmoid function.

e
z − e
−z

e
z + e
−z

tanh =

Problem in both Sigmoid and tanh is that the slope of the
curve except the middle region is too small and goes
close to zero. This create a serious issue with gradient
descent and learning becomes very slow.



![[Pasted image 20251217213623.png]]


Zero mean value ![[Pasted image 20251217213637.png]]


It has better centering effect for the activation function to be used on the hidden layer.
For binary classification problem at the output layer we use the Sigmoid function.

Problem in both Sigmoid and tanh is that the slope of the
curve except the middle region is too small and goes
close to zero. This create a serious issue with gradient
descent and learning becomes very slow.










Softmax Function

When we have to classify in multiple categories then softmax function is useful. For
example if you want to categorize pictures into

A) scene b) Animals c) Humans d) Vehicles then in that case we will have four outputs
from the softmax function which will give us the probabilities of each of these categories.

Sum of the probabilities will be one and that with the highest probability will be shown as
the answer.



|Feature|**Sigmoid**|**tanh**|
|---|---|---|
|Range|(0, 1)|(−1, 1)|
|Zero-centered?|❌ No|✅ Yes|
|Vanishing gradient|❌ Yes|❌ Yes|
|Output meaning|Probability|Scaled signal|
|Convergence speed|Slower|Faster than sigmoid|
|Typical use|Binary output layer|Hidden layer (older nets)|


|Feature|**Sigmoid**|**ReLU**|
|---|---|---|
|Formula|( \frac{1}{1+e^{-x}} )|( \max(0,x) )|
|Range|(0,1)|[0, ∞)|
|Vanishing gradient|❌ Yes|✅ No (positive side)|
|Speed|Slow|Fast|
|Zero-centered?|❌ No|❌ No|
|Sparsity|❌ No|✅ Yes|
|Deep networks|❌ Bad|✅ Excellent|




|Feature|**Sigmoid**|**Softmax**|
|---|---|---|
|Output|Independent probability|Probability distribution|
|Output sum|≠ 1|= 1|
|Use case|Binary classification|Multi-class classification|
|Multiple classes|❌|✅|
|Activation style|Per neuron|Across all neurons|


The input is fed to the input layer, the neurons perform a linear transformation on this input using the weights and biases.

```ini
x = (weight * input) + bias
```

Post that, an activation function is applied on the above result.

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2017/10/17123344/act.png)

Finally, the output from the activation function moves to the next hidden layer and the same process is repeated. This forward movement of information is known as the **_forward propagation_**.

What if the output generated is far away from the actual value? Using the output from the forward propagation, error is calculated. Based on this error value, the weights and biases of the neurons are updated. This process is known as **_back-propagation_**.




A neural network without an activation function in [deep learning](https://www.analyticsvidhya.com/blog/2021/12/a-guide-on-deep-learning-from-basics-to-advanced-concepts/) is essentially just a linear regression model


**Sparse activation** in deep learning means that **only a small number of neurons are active (non-zero) at a time**, while most neurons output zero (or near zero).

---

### Simple intuition 🧠

Think of a classroom:

- Teacher asks a question
    
- Only **2–3 students raise their hands**
    
- Others stay silent
    

That’s **sparse activation**.






**Dying ReLU problem** occurs when a ReLU neuron outputs zero for all inputs due to negative weights, stopping learning.  
**Solution:** use Leaky ReLU, proper weight initialization, smaller learning rates, or batch normalization.

![[Pasted image 20251217231605.png]]





5. Conclusion
Activation functions are crucial for deep learning models. The choice depends on the problem type, layer position, and model behavior during
training.



Keras Optimizer 

**Keras optimizers** control **how model weights are updated** to minimize loss during training.

## 1. SGD - Stochastic Gradient Descent
**Concept**: Standard optimizer using gradient descent.
**Update Rule**:

w = w - learning_rate * gradient
**Highlights**:
- Simple and widely used baseline
- No adaptive learning
- Can be slow and oscillate
**Use When**:
- Fine-tuning models
- Want complete control with manual learning rate tuning

## 2. Momentum / Nesterov Momentum

**Concept**: Adds a velocity term to dampen oscillations.


![[Pasted image 20251217232333.png]]

**Momentum Update**:

v = gamma * v_prev + learning_rate * gradient w = w - v

**Nesterov Update**:

v = gamma * v_prev + learning_rate * gradient(w - gamma * v_prev) w = w - v

**Why It’s Better**:
- Faster convergence than vanilla Stochastic Gradient Descent
- Nesterov anticipates (to expect something to happen) direction = better performance
---


## 3. Adagrad

### **Adagrad Optimizer (simple & clear)**

**Adagrad (Adaptive Gradient)** is an optimizer that **automatically adjusts the learning rate for each parameter** based on how often it has been updated.

### **Core idea**

- Parameters with **frequent updates** → get **smaller learning rates**
    
- Parameters with **rare updates** → get **larger learning rates**

**Concept**: Adapts learning rate per parameter.
for each parameter

**Update Rule**:

accumulated_grad += gradient ** 2 w = w - (learning_rate / sqrt(accumulated_grad + epsilon)) * gradient

**Key Feature**:
- Higher learning rate for infrequent parameters
- Great for sparse features (NLP, recommendation)
**Limit**:
- Learning rate shrinks too much over time
---

### **Why use Adagrad**

✅ Great for **sparse data** (NLP, recommender systems)  
✅ No need to manually tune learning rate much






---
## 4. RMSprop
**Concept**: Fixes Adagrad’s shrinking learning rate using moving average.
**Update Rule**:

E[g2] = rho * E[g2] + (1 - rho) * gradient ** 2 w = w - (learning_rate / sqrt(E[g^2] + epsilon)) * gradient

**Best For**:
- RNNs and non-stationary objectives
**Innovation**:
- Introduced by Geoffrey Hinton for deep networks
---
### **RMSprop Optimizer in Keras (simple explanation)**

**RMSprop (Root Mean Square Propagation)** is an optimizer that **adapts the learning rate for each weight** so training becomes faster and more stable.

---

### **Why RMSprop is used**

It fixes a big problem of Adagrad:

- Adagrad’s learning rate keeps shrinking ❌
    
- RMSprop **prevents learning from stopping**
    

---

### **How it works (intuition)**

- Keeps an **exponential moving average of squared gradients**
    
- Divides the gradient by this average
    

So:

- Large, noisy gradients → smaller step

Non-stationary objectives are loss functions that change over time; RMSprop handles them by adapting learning rates using recent gradients.



## 5. Adadelta
**Concept**: Builds on RMSprop, eliminates need to set learning rate manually.
**Update Rule**:

E[g2] = rho * E[g2] + (1 - rho) * gradient ** 2 E[delta2] = rho * E[delta2] + (1 - rho) * delta ** 2 w = w - (sqrt(E[delta2] + epsilon) / sqrt(E[g2] +

epsilon)) * gradient

**Why Use It**:
- No manual learning rate
- Safer convergence than Adagrad


do we need to set learning rate manually for rms prop

Yes — **you still need to set a learning rate for RMSprop**, but **it’s much less sensitive** than in SGD.

#### Clear answer

- **RMSprop has a learning rate (`η`)**
    
- It **automatically adapts** step sizes per parameter
    
- So the exact value is **not very critical**


---
## 6. Adam - Adaptive Moment Estimation
**Concept**: Combines Momentum + RMSprop

**Why It’s Popular**:
- Excellent performance across tasks
- Fast convergence, less sensitive to learning rate
- Good default for most models
---
## 7. Adamax
**Concept**: Variant of Adam using infinity norm (L∞)
**Difference**:
- Uses `max` of past gradients instead of `mean` for better stability
**Use When**:
- Adam shows instability or high variance
---
## 8. Nadam
**Concept**: Adam + Nesterov Momentum
**Why Use It**:
- Combines adaptive gradient and lookahead
- Better convergence on noisy gradients
---
## 9. FTRL - Follow The Regularized Leader
**Concept**: Designed for sparse, high-dimensional problems with L1/L2 regularization
**Use Case**:
- Linear models, ad click prediction, search ranking
**Why It’s Famous**:
- Used at Google for large-scale problems
---






| Optimizer | Key Idea                    | Adaptive LR | Notes                            |
| --------- | --------------------------- | ----------- | -------------------------------- |
| SGD       | Basic gradient descent      | No          | Good for simple problems         |
| Momentum  | Adds velocity to SGD        | No          | Faster convergence               |
| Adagrad   | Per-parameter learning rate | Yes         | Sparse data, NLP                 |
| RMSprop   | Moving average of gradients | Yes         | RNNs, non-stationary-loss        |
| Adadelta  | Auto-learning rate          | Yes         | No need to tune    learning      |
| Adam      | Momentum + RMSprop          | Yes         | Most Commonly    Used  Optimizer |
| Adamax    | Adam with infinity norm     | Yes         | Stable Adam variant              |
| Nadam     | Adam + Nesterov             | Yes         | Better for RNNs                  |
| FTRL      | Regularized optimizer       | Yes         | Sparse linear models             |
## Optimizer Recommendations
- Default choice: **Adam**
- Sparse data: **Adagrad** or **FTRL**
- Fine-tuning / control: **SGD + Momentum**
- RNNs or sequential: **RMSprop** or **Nadam**
- If Adam is unstable: **Adamax**
---
## References
- Keras Official Documentation: https://keras.io/api/optimizers/
- Deep Learning Book - Ian Goodfellow, Yoshua Bengio, Aaron Courville
- Geoffrey Hinton's Coursera Lectures





### **MSE (Mean Squared Error)**

- Squares errors
    
- Penalizes large errors **heavily**
    
- Sensitive to outliers
    
- Use for clean data
    

---

### **MAE (Mean Absolute Error)**

- Uses absolute error
    
- Penalizes all errors **equally**
    
- Robust to outliers
    
- Slower learning
    

---

### **Huber Loss**

- Combimation of mse and Mae
 
- MSE for small errors
    
- MAE for large errors
    
- Balanced and stable
    
- Good default choice
    

---

### **Log-Cosh Loss**

- Smooth version of MSE
    
- Less sensitive to outliers
    
- Fully differentiable
    
- Used in deep learning





|Feature|Huber Loss|Log-Cosh Loss|
|---|---|---|
|Switching point|**Uses delta (manual cutoff)**|**Automatic (no cutoff)**|
|Shape|Piecewise (MSE → MAE)|Smooth curve|
|Differentiability|Smooth except at delta|Smooth everywhere|
|Control|You control robustness via delta|No tuning needed|




# 🟦 E. Choosing the Right Loss (MEMORIZE THIS)

| Problem                | Loss                            |
| ---------------------- | ------------------------------- |
| Regression             | MSE, MAE, Huber, Log-Cosh       |
| Binary classification  | Binary Crossentropy             |
| Multiclass (one-hot)   | Categorical Crossentropy        |
| Multiclass (integer)   | Sparse Categorical Crossentropy |
| Probability comparison | KL Divergence                   |
| NLP / similarity       | Cosine Similarity               |
|                        |                                 |




## 1️⃣ Accuracy

- % of correct predictions
    

Types:

- `accuracy`
    
- `binary_accuracy`
    
- `categorical_accuracy`
    
- `sparse_categorical_accuracy`
- 


![[Pasted image 20251218010118.png]]


## 4️⃣ F1 Score

- Balance of Precision & Recall
- Harmonic mean of precision and recall 
- 
    
- Not built-in but custom implementation can be implemented 


## AUC

- Area under ROC curve
    
- Best for **imbalanced datasets**



[Complete Deep Learning.pdf](attachment:59dd48e7-c9e2-4925-9d1f-aa4abb1717ea:Complete_Deep_Learning.pdf)

![image.png](attachment:df1f25e4-856f-43aa-8efc-6eb2c1ab26f9:image.png)

![image.png](attachment:f5985227-ef92-4235-8cdf-27b3f1245272:image.png)

![image.png](attachment:4413a2bc-0948-4e52-bdf6-b6779c25c6a4:image.png)

# CNN

Convolution is an operation where a **small matrix (kernel / filter)** slides over the image and **extracts features**.

### **Problem with Classical CV**

> “Classical CV feature definition is domain-specific and time-consuming”

Meaning:

- Features had to be **manually designed**
- Different features for different problems
- Took a lot of **expert knowledge + time**
- Did not scale well

---

### **One-line summary**

Classical Computer Vision =

**Manually design features → apply ML → get results**

But it’s **slow, hard, and problem-specific**, which is why **Deep Learning replaced it**.

**“A Logical Calculus of the Ideas Immanent in Nervous Activity” (1943)**

What this means:

- First paper that said:
    
    > Brain activity can be explained using mathematics and logic
    
- Published in **1943**
    
- This paper started:
    
    - Neural Networks
    - AI
    - Computational neuroscience

---

## **Key idea of the slide**

- Brain neurons → **logical units**
- Logical units → **artificial neurons**
- Artificial neurons → **neural networks**

![image.png](attachment:bcc7c50c-ec96-4a6f-92fb-2516d29ad247:image.png)

## **What this diagram shows**

This is **one artificial neuron** (basic building block of a neural network).

---

## **x₁ and x₂ (inputs)**

- These are **features** (numbers from your data)
- Example: height, weight, pixel value, marks, etc.
- **Normalized** means values are scaled between **0 and 1**

👉 Here:

- x₁ = 0.3
- x₂ = 0.8

---

## **w₁ and w₂ (weights)**

- Weights tell **how important** each input is
- Bigger weight = more importance

👉 Given:

- w₁ = 0.5
- w₂ = 0.5

---

## **Multiplication (importance applied)**

Each input is multiplied by its weight:

- x₁ × w₁ → contribution of x₁
- x₂ × w₂ → contribution of x₂

---

## **Σ (summation block)**

This symbol **adds everything**:

sum=(w1×x1)+(w2×x2)\text{sum} = (w₁ × x₁) + (w₂ × x₂)

sum=(w1×x1)+(w2×x2)

Substitute values:

=(0.5×0.3)+(0.5×0.8)= (0.5 × 0.3) + (0.5 × 0.8)

=(0.5×0.3)+(0.5×0.8)

=0.15+0.40=0.55= 0.15 + 0.40 = 0.55

=0.15+0.40=0.55

👉 This is called **weighted sum**

---

## **Activation function (step / curve symbol)**

- Takes the weighted sum (0.55)
- Decides **should neuron fire or not**
- Converts number into output **y**

Examples:

- Step → 0 or 1
- Sigmoid → probability
- ReLU → max(0, x)

---

## **y (output)**

- Final output of neuron
- Can be:
    - Class label (0 / 1)
    - Probability
    - Score

---

## **One-line summary**

A neuron:

> multiplies inputs by importance (weights), adds them, applies a function, and produces output

![image.png](attachment:ea7f0b4c-49a2-4b95-a5d2-7440aefb47bd:image.png)

![image.png](attachment:21ef709f-b66c-44cf-951d-13ae7aa5c122:image.png)

## **The Bayes Classifier**

A **Bayes classifier** predicts the class that has the **highest probability given the data**.

---

## **Main idea on the slide**

arg⁡max⁡Y  P(Y∣X1,…,Xn)\arg\max_Y \; P(Y \mid X_1, \dots, X_n)

argYmaxP(Y∣X1,…,Xn)

### Break it down:

- **Y** → class label
    
    (e.g., digit = 0,1,2,…,9)
    
- **X₁ … Xₙ** → features
    
    (e.g., pixel values of an image)
    
- **P(Y | X₁,…,Xₙ)** →
    
    “Probability that the class is **Y**, given the features”
    
- **arg max** →
    
    “Pick the class with the **largest probability**”
    

## Drive into CNN

In a convolutional network (ConvNet), there are basically three types of layers: 1.Convolution layer 2.Pooling layer 3.Fully connected layer

### **“A CNN is a neural network with some convolutional layers”**

- CNN = Convolutional Neural Network
- It is a neural network **specialized for images**
- It has:
    - Convolution layers
    - Plus other layers (ReLU, pooling, fully connected)

---

### **“A convolutional layer has a number of filters”**

- A **filter (kernel)** is a small matrix (e.g., 3×3, 5×5)
- Filters are **learned during training**
- Each filter looks for **one pattern**

## Important

**In a convolutional network (ConvNet), there are basically three types of layers: 1.Convolution layer 2.Pooling layer 3.Fully connected layer**

![image.png](attachment:34d0416d-e78c-4145-9045-719778cb3c9d:image.png)

# for visualization

[https://www.pinecone.io/learn/series/image-search/cnn/](https://www.pinecone.io/learn/series/image-search/cnn/)

![image.png](attachment:f277ea4a-e6b6-4728-9aac-338529587b20:image.png)

![image.png](attachment:9fa9ce75-9209-4241-897d-e663ba9578c2:image.png)

![image.png](attachment:c44b1096-ffd9-4266-a241-3c6be89629f1:image.png)

![image.png](attachment:53fdc860-eab4-482d-a049-832392268448:image.png)

A CNN compresses a fully connected network in two ways:

- Reducing number of connections • Shared weights on the edges • Max pooling further reduces the complexity

# Rendom Search

## 1️⃣ Random Search

### What is it?

Random Search **randomly picks hyperparameters** from the search space.

No memory.

No intelligence.

Each trial is independent.

No memory so no learn from past experience

it can take much more time as ve rendomly choose hyperparameters

We randomly try different settings and see which works best.

### Why do this?

- Simple
- Faster than trying all combinations
- Good starting point

## 2️⃣ Hyperband

### New term: Resource

A **resource** is how much training we give:

- Number of epochs
- Time
- Computation

### What is Hyperband?

Hyperband is **Random Search + Early Stopping**.

### What is Early Stopping?

Stop training models **early** if they perform badly.

What we will do …..

- Start **many models**
- Train each for **few epochs**
- Kill bad ones early
- Give more epochs to good ones

## 3️⃣ Bayesian Optimization

### New term: Probabilistic Model

A model that **predicts performance and uncertainty**.

Usually uses a **Gaussian Process** (fancy probability model).

---

### What is Bayesian Optimization?

It **learns from previous results** and makes **smart guesses**.

---

### What are we doing?

1. Train model with some hyperparameters
2. Observe result
3. Build a probability model
4. Predict which hyperparameters will work best next

---

### Why do this?

Training models can be **very expensive**.

Bayesian optimization reduces **number of trials needed**.