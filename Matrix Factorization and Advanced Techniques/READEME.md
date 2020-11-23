## On Folding-In with Gradient Descent

The gradient descent approach - particularly with regularization, or with additional modifications such as sigmoid functions restricting predicted values to be within the valid range of ratings - results in a matrix factorization that is not a proper SVD in the linear algebra sense. In particular, the left and right matrices are no longer guaranteed to be orthogonal. Since folding-in formally requires orthogonality to be correct, it is no longer safe to assume that it will work.

However, in practice - especially with a sufficiently small learning rate - they may be orthogonal enough that folding-in works with acceptable accuracy. Whether it works depends on data set, application, and choice of hyperparameters (such as learning rate and regularization strength). If you need folding-in, test with your data and see if it is effective or if it introduces unacceptable accuracy loss.

For more information on this, [see:](https://math.stackexchange.com/a/653158).