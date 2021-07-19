# Gradient_descent-NN
-  As the loss function is continuous, a small change in x can only result in a small change in y—that’s the intuition behind continuity.
-  f(x + epsilon_x) = y + epsilon_y
-  because the function is smooth (its curve doesn’t have any abrupt angles),when epsilon_x is small enough, around a certain point p, it’s possible to approximate f as a linear function of slope a, so that epsilon_y becomes a * epsilon_x.
- The slope a is called the derivative of f in p. If a is negative, it means a small changeof x around p will result in a decrease of f(x) (as shown in figure 2.10); and if a is positive, a small change in x will result in an increase of f(x). Further, the absolute value of a (the magnitude of the derivative) tells you how quickly this increase or decrease will happen.
- If you’re trying to update x by a factor epsilon_x in order to minimize f(x), andyou know the derivative of f, then your job is done: the derivative completely describes how f(x) evolves as you change x. If you want to reduce the value of f(x),you just need to move x a little in the opposite direction from the derivative.
- Let’s say the current value of W is W0. Then the derivative of f in the point W0 is a tensorgradient(f)(W0) with the same shape as W, where each coefficient gradient(f)(W0)[i, j] indicates the direction and magnitude of the change in loss_value youobserve when modifying W0[i, j]. That tensor gradient(f)(W0) is the gradient of the function f(W) = loss_value in W0.
- W1 = W0 - step * gradient(f)(W0)
- The optimization process would get stuck at the local minimum instead of making its way to the global minimum.
-  You can avoid such issues by using momentum, which draws inspiration from physics. A useful mental image here is to think of the optimization process as a small ball rolling down the loss curve. If it has enough momentum, the ball won’t get stuck in a ravine and will end up at the global minimum
- if there high learning rate we may miss the minimum.

for different Optimizers visit https://medium.datadriveninvestor.com/overview-of-different-optimizers-for-neural-networks-e0ed119440c3
