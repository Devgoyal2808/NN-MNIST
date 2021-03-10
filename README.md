# Neural-Network MNIST
Implementation-for-XOR
Neural Network helps to move from linear function to non linear function as output making results for our model more effective.

We basically combine different linear models in layers to make a resultant model b/w input and predictions non linear.
we than apply Gradient Descent on this model to find best possible solution with minimized cost and error.

Considered Cost: Error + (lamba)*(regularization)                                                                                                                                  

Error: (sigma(Y_actual - Y_pred)^2)/2

Function used: sigmoid(z)= 1 / (1+e^-z)


End result minimized by calculating and forming equations based on : dell(Error)/dell(weight(i)(j))  and  dell(Error)/dell(biasing_factor(i)(j))

### BackPropogation
after applying calculus on stated above for every layer we can drive that  dell(Error)/dell(weight(i)(j)) depends on weights(i,j), inputs(j), output(j) , output(i) etc and we end up reaching a recursive function from nth layer to n-1 layer. Hence this entire function is called back propogation. 

### FrontPropogation
In this we calculate all the values at every layer using new weights and biasing factor from from nth to n+1 layer so called FrontPropogation. We use this data in back Propogation for next step.


# NN MNIST
MNIST is data set which contains 70k images of numbers in range [0,9]. 55k in train,10k in test,5k in validation.

After knowing how NN is implemented , we use Tensorflow to build Stochastic Non Linear Regression model with 2 hiden layer of 256,256 nodes.Input with 784 nodes and output with 10 nodes.Hence having 256,256,10 biasing factors.

TensorFlow is a free and open-source software, symbolic math library for machine learning. It can be used across a range of tasks but has a particular focus on training and inference of deep neural networks based on dataflow and differentiable programming

Considered Error :: Cross Entropy: sigma(-y*log(h)-(1-y)log(1-h)).             where h is derivative of net error w.r.t respective node.

Optimizer : AdamOptimizer used with learning rate 0.01 . It basically perform backward Propogation with values that are trainable.

Front Propagation: We need to write our own function every time as per the model we use.

Stochastic:Dividing into 100 Batches increased our accuracy from 86% to 98% in particular cases.
