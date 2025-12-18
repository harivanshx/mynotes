

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
