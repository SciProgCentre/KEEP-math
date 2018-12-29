Turchin's method of statistical regularization

* **Type**: Use case
* **Author**: Mikhail Zelenyi
* **Status**: 
* **Discussion**: [](None)

During analysis of experimental data, one usually needs to restore a signal after it has been convoluted with some kind of apparatus function. According to Hadamard's definition this problem is ill-posed and requires regularization to provide sensible results. The Turchin's method of statistical regularization based on the Bayesian approach to the regularization strategy.

Description of Turchin's method of statistical regularization, we could show [here](Description of Turchin's method of statistical regularization, we could show here.).

Python implementation, we could find on [github](https://github.com/mipt-npm/statreg-py)

## Simple implementation
For simple implementation of statistical regularization, we needed in :
* Matrix tools: transpose, inverse, determinant (logarithim), pseudodetermiant, rank, eigvalues, SVD and Cholesky decomposition.
* Minimizator: in current version we used simplex (Nelder-Mead).
* Integrators.
* Cubic spline and B-Spline.
* Special function, which we can use as basis in functional space.

## Advanced implementation (in develop)

For simple implementation of statistical regularization, we needed in Markov chain Monte-Carlo (MCMC)

