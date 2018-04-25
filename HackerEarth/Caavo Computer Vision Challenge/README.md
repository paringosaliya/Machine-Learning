
- [Link](https://www.hackerearth.com/challenge/hiring/caavo-software-engineer-hiring-challenge/problems/)

# End date

- `22nd Apr 2018`

# Read up
- Optimization and annealing in neural networks
  - Optimization using RMSprop
- How to come up with structure of a neural network for our specific problem
- Dropout
- Keras - official documentation
- Categorical crossentropy : Used to measure loss/ error in observed and predicted for multi - class

# Reference

1. [Tutorial: Optimizing Neural Networks using Keras (with Image recognition case study)](https://www.analyticsvidhya.com/blog/2016/10/tutorial-optimizing-neural-networks-using-keras-with-image-recognition-case-study/) 
2. [Dropout in NNs](https://medium.com/@amarbudhiraja/https-medium-com-amarbudhiraja-learning-less-to-learn-better-dropout-in-deep-machine-learning-74334da4bfc5)
3. [An Introduction to Implementing Neural Networks using TensorFlow](https://www.analyticsvidhya.com/blog/2016/10/an-introduction-to-implementing-neural-networks-using-tensorflow/)
4. Categorical cross entropy - 
    - [Machine Learning: Should I use a categorical cross entropy or binary cross entropy loss for binary predictions?](https://stats.stackexchange.com/questions/260505/machine-learning-should-i-use-a-categorical-cross-entropy-or-binary-cross-entro)
    - [A Friendly Introduction to Cross-Entropy Loss](http://rdipietro.github.io/friendly-intro-to-cross-entropy-loss/)
5. Kaggle kernels
    - [Kaggle - Plant Seedlings Classification](https://www.kaggle.com/raoulma/plants-xception-90-06-test-accuracy)
    - [Kaggle - Digit recognizer](https://www.kaggle.com/yassineghouzam/introduction-to-cnn-keras-0-997-top-6)
6. [An overview opf gradient descent optimization algorithms](http://ruder.io/optimizing-gradient-descent/)
7. Categorical crossentropy
    - [Stackexchange]((https://stats.stackexchange.com/questions/260505/machine-learning-should-i-use-a-categorical-cross-entropy-or-binary-cross-entro))

## 1. [Tutorial: Optimizing Neural Networks using Keras (with Image recognition case study)](https://www.analyticsvidhya.com/blog/2016/10/tutorial-optimizing-neural-networks-using-keras-with-image-recognition-case-study/) 

#### Keras : Overview

The key features of Keras are:
- **Modularity** : Modules necessary for building a neural network are included in a simple interface so that Keras is easier to use for the end user
- **Minimalistic** : Implementation is short and concise
- **Extensibility** : It’s very easy to write a new module for Keras and makes it suitable for advance research

#### General way to solve problems with Neural Networks

- Check if it is a problem where Neural Network gives you uplift over traditional algorithms (refer to the checklist in the section above)
- Do a survey of which Neural Network architecture is most suitable for the required problem
- Define Neural Network architecture through whichever language / library you choose.
- Convert data to right format and divide it in batches
- Pre-process the data according to your needs
- Augment Data to increase size and make better trained models
- Feed batches to Neural Network
- Train and monitor changes in training and validation data sets
- Test your model, and save it for future use

# 7. Cross-entropy

## [Machine Learning: Should I use a categorical cross entropy or binary cross entropy loss for binary predictions?](https://stats.stackexchange.com/questions/260505/machine-learning-should-i-use-a-categorical-cross-entropy-or-binary-cross-entro)

Binomial cross-entropy loss is a special case of multinomial cross-entropy loss for m=2.

- <math xmlns="http://www.w3.org/1998/Math/MathML" display="block">
  <mrow class="MJX-TeXAtom-ORD">
    <mi class="MJX-tex-caligraphic" mathvariant="script">L</mi>
  </mrow>
  <mo stretchy="false">(</mo>
  <mi>&#x03B8;<!-- θ --></mi>
  <mo stretchy="false">)</mo>
  <mo>=</mo>
  <mo>&#x2212;<!-- − --></mo>
  <mfrac>
    <mn>1</mn>
    <mi>n</mi>
  </mfrac>
  <munderover>
    <mo>&#x2211;<!-- ∑ --></mo>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>i</mi>
      <mo>=</mo>
      <mn>1</mn>
    </mrow>
    <mi>n</mi>
  </munderover>
  <mrow>
    <mo>[</mo>
    <msub>
      <mi>y</mi>
      <mi>i</mi>
    </msub>
    <mi>log</mi>
    <mo>&#x2061;<!-- ⁡ --></mo>
    <mo stretchy="false">(</mo>
    <msub>
      <mi>p</mi>
      <mi>i</mi>
    </msub>
    <mo stretchy="false">)</mo>
    <mo>+</mo>
    <mo stretchy="false">(</mo>
    <mn>1</mn>
    <mo>&#x2212;<!-- − --></mo>
    <msub>
      <mi>y</mi>
      <mi>i</mi>
    </msub>
    <mo stretchy="false">)</mo>
    <mi>log</mi>
    <mo>&#x2061;<!-- ⁡ --></mo>
    <mo stretchy="false">(</mo>
    <mn>1</mn>
    <mo>&#x2212;<!-- − --></mo>
    <msub>
      <mi>p</mi>
      <mi>i</mi>
    </msub>
    <mo stretchy="false">)</mo>
    <mo>]</mo>
  </mrow>
  <mo>=</mo>
  <mo>&#x2212;<!-- − --></mo>
  <mfrac>
    <mn>1</mn>
    <mi>n</mi>
  </mfrac>
  <munderover>
    <mo>&#x2211;<!-- ∑ --></mo>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>i</mi>
      <mo>=</mo>
      <mn>1</mn>
    </mrow>
    <mi>n</mi>
  </munderover>
  <munderover>
    <mo>&#x2211;<!-- ∑ --></mo>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>j</mi>
      <mo>=</mo>
      <mn>1</mn>
    </mrow>
    <mi>m</mi>
  </munderover>
  <msub>
    <mi>y</mi>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>i</mi>
      <mi>j</mi>
    </mrow>
  </msub>
  <mi>log</mi>
  <mo>&#x2061;<!-- ⁡ --></mo>
  <mo stretchy="false">(</mo>
  <msub>
    <mi>p</mi>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>i</mi>
      <mi>j</mi>
    </mrow>
  </msub>
  <mo stretchy="false">)</mo>
</math>

Where <math xmlns="http://www.w3.org/1998/Math/MathML">
  <mi>i</mi>
</math> indexes samples/observations and jj indexes classes, and yy is the sample label (binary for LSH, one-hot vector on the RHS) and <math xmlns="http://www.w3.org/1998/Math/MathML">
  <msub>
    <mi>p</mi>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>i</mi>
      <mi>j</mi>
    </mrow>
  </msub>
  <mo>&#x2208;<!-- ∈ --></mo>
  <mo stretchy="false">(</mo>
  <mn>0</mn>
  <mo>,</mo>
  <mn>1</mn>
  <mo stretchy="false">)</mo>
  <mo>:</mo>
  <munder>
    <mo>&#x2211;<!-- ∑ --></mo>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>j</mi>
    </mrow>
  </munder>
  <msub>
    <mi>p</mi>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>i</mi>
      <mi>j</mi>
    </mrow>
  </msub>
  <mo>=</mo>
  <mn>1</mn>
  <mi mathvariant="normal">&#x2200;<!-- ∀ --></mi>
  <mi>i</mi>
  <mo>,</mo>
  <mi>j</mi>
</math> is the prediction for a sample

## [A Friendly Introduction to Cross-Entropy Loss](http://rdipietro.github.io/friendly-intro-to-cross-entropy-loss/)

- #### [Difference between probabilty and likelihood](https://stats.stackexchange.com/questions/2641/what-is-the-difference-between-likelihood-and-probability)
- #### [StatQuest: Probability vs Likelihood](https://www.youtube.com/watch?v=pYxNSUDSFH4)


# 6. [An overview opf gradient descent optimization algorithms](http://ruder.io/optimizing-gradient-descent/)

Gradient descent is a way to minimize an objective function J(θ) parameterized by a model's parameters θ∈Rd by updating the parameters in the opposite direction of the gradient of the objective function ∇θJ(θ) w.r.t. to the parameters. The learning rate η determines the size of the steps we take to reach a (local) minimum. In other words, we follow the direction of the slope of the surface created by the objective function downhill until we reach a valley

### Gradient descent variants

There are three variants of gradient descent, which differ in how much data we use to compute the gradient of the objective function :
- Batch
- Stochaistic
- 

#### Batch gradient descent :

- Vanilla gradient descent, aka batch gradient descent, computes the gradient of the cost function w.r.t. to the parameters θθ for the entire training dataset:
- θ = θ − η ⋅ ∇θJ(θ)
- Batch gradient  code 
```python 
for i in range(nb_epochs):
params_grad = evaluate_gradient(loss_function, data, params)
params = params - learning_rate * params_grad
```
- As we need to calculate the gradients for the whole dataset to perform just one update, batch gradient descent can be very slow and is intractable for datasets that don't fit in memory. Batch gradient descent also doesn't allow us to update our model online, i.e. with new examples on-the-fly

#### Stochastic gradient descent :

- Stochastic gradient descent (SGD) in contrast performs a parameter update for each training example x(i) and label y(i):
- θ = θ − η ⋅ ∇θJ(θ; x(i); y(i))
- Batch gradient descent performs redundant computations for large datasets, as it recomputes gradients for similar examples before each parameter update. SGD does away with this redundancy by performing one update at a time. It is therefore usually much faster and can also be used to learn online
- SGD performs frequent updates with a high variance that cause the objective function to fluctuate heavily
- While batch gradient descent converges to the minimum of the basin the parameters are placed in, SGD's fluctuation, on the one hand, enables it to jump to new and potentially better local minima
```python
for i in range(nb_epochs):
  np.random.shuffle(data)
  for example in data:
    params_grad = evaluate_gradient(loss_function, example, params)
    params = params - learning_rate * params_grad
```

#### Mini-batch gradient descent : 

- Mini-batch gradient descent finally takes the best of both worlds and performs an update for every mini-batch of n training examples:
- θ=θ−η⋅∇θJ(θ;x(i:i+n);y(i:i+n))
- This way, it
    a. reduces the variance of the parameter updates and 
    b. can make use of highly optimized matrix optimizations
```python
for i in range(nb_epochs):
  np.random.shuffle(data)
  for batch in get_batches(data, batch_size=50):
    params_grad = evaluate_gradient(loss_function, batch, params)
    params = params - learning_rate * params_grad
```

### Challenges

Vanilla mini - batch gradient descent challenges - 

- Choosing a proper learning rate can be difficult
- Learning rate schedules try to adjust the learning rate during training by e.g. **annealing**, i.e. reducing the learning rate according to a **pre-defined schedule** or when the **change in objective between epochs falls below a threshold**. These schedules and thresholds, however, have to be defined in advance and are thus unable to adapt to a dataset's characteristics
- Additionally, the same learning rate applies to all parameter updates. If our data is sparse and our features have very different frequencies, we might not want to update all of them to the same extent, but perform a larger update for rarely occurring features
- Another key challenge of minimizing highly non-convex error functions common for neural networks is avoiding getting trapped in their numerous suboptimal local minima

### Gradient descent optimization algorithms

- Momentum
























