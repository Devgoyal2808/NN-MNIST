# Neural-Network-Implementation-for-XOR

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
