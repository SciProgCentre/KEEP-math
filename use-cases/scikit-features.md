# List of numpy/scipy features for porting

* **Type**: Use case
* **Author**: Mikhail Zelenyi
* **Status**: 
* **Discussion**: [](None)

Numpy and Scipy is foundation of Python science toolkit. This is really powerfull library, which attract researcher. In this document enumerate main features, which potential usefull for implementation in Kotlin math library. 

## Basic and unspecified features
 
 * Special class for working with polynomials.
 * Generation of number sequence in linear and logarithmic scale.
 * Tools for selection, shuffle, slicing, comparison element in arrays.
 * Tools for creating prefilled arrays
 * Native type for complex number (Python features)
 
## Common and special math function

Common and special function for advanced math, financial(?) and theoretical physics (?).

* Simple math function: Heaviside, triangle, factorial, binominal coefficient etc.
* Fast implementation of elementary function (?).
* Logic function
* Functions, integrals and zeros: Airy, Elliptic, Bessel, Riccati-Bessel, Legendre, Struve, Gamma, Beta, Fresnel, erf and [another](https://docs.scipy.org/doc/scipy/reference/special.html#module-scipy.special)
* Information theory functions

## Integration

Calculation of univariate and multivariate integral on grid (include infinite limits)

## Optimization 

* Sets of different minimizator
* Tools for fitting
* Univariate equation solver
* Multivariate equation system solvers

## Interpolation

* Spline (1d and 2d) and B-splines
* 1d interpolation and extrapolition tools
* Tools for smoothness interpolation
* Multivariate data interpolation

## Fourier Transforms

* Fast Fourier transforms

## Signal Processing 

* Convolution
* Filtering
* Deconvolution
* Autocorrelation
* Image processing

## Linear Algebra 

* Special class for matrix
* Matrix operation: transpose, production, determinant, trace, norm, inverse, pseudodeterminant  etc
* Solution of linear equation and least squares methods  
* Decomposition: eigenvalues, eigenvectors
* Singular value decomposition
* Decomposition: LU, QR, Cholesky, Schur, ID. SVD
* Special matrix functions (`exp` etc)
* Named matrix: Hilbert and [another](https://docs.scipy.org/doc/scipy/reference/tutorial/linalg.html#special-matrices)
* Tensor operation

## Sparse matrix and arrays

Implementation of sparse matrix and arrays

## Statistics

* Generation random sequence from different distribution and user distribution
* PDF and CDF for different distribution, inverse function
* Calculation of momentum, median and moda for data
* Calculation of percenticle, quantile, correlation coeficient, covariance
* Statistical test
* Kernel density estimation (include multivariate)
* Histogramms:  multidimensional, with uniform and user binning

## Multidimensional image processing

Tools for image processing (can be used for machine and deep learning)
