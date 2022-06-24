# Linear-Regression-by-Hand
Implementation of Linear Regression and Gradient Descent by hand

## The Model
The purpose of the linear regression model is to fit a line to a set of points. The function for the model can be represented as
$$f_{w, b}(x) = wx + b$$
where $w$ is the slope and $b$ is the y-intercept.

## The Cost Function
For this model, we use the **Squared Error** cost function. This can be represented as a function of $w$ and $b$:
$$J(w, b) = \frac{1}{2m} \sum_{i = 1}^{m} (\hat{y}^{(i)} - y^{(i)})^2$$
or
$$J(w, b) = \frac{1}{2m} \sum_{i = 1}^{m} (f_{w, b}(x^{(i)}) - y^{(i)})^2$$

## Gradient Descent
The goal of gradient descent is to minimize the cost function. We do this by taking the partial derivative of the cost function with respect to each of its parameters. After doing this, we adjust each parameter by the negative of the partial derivative times a learning rate $\alpha$. For the squared error cost function with parameters $w$ and $b$ we adjust each in the following way:
$$w_{i + 1} = w_i - \alpha \frac{\partial}{\partial w} J(w, b)$$
$$b_{i + 1} = b_i - \alpha \frac{\partial}{\partial b} J(w, b)$$

and each partial derivative is as follows:
$$\frac{\partial}{\partial w} J(w, b) = \frac{1}{m} \sum_{i = 1}^{m} (f_{w, b}(x^{(i)}) - y^{(i)})x^{(i)}$$
$$\frac{\partial}{\partial b} J(w, b) = \frac{1}{m} \sum_{i = 1}^{m} (f_{w,b}(x^{(i)}) - y^{(i)})$$

We repeat these incremental steps until convergence, which represents the minimum of the cost function.
