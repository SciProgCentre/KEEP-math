# List of numpy/scipy features for porting

* **Type**: Use case
* **Author**: Mikhail Zelenyi
* **Status**: 
* **Discussion**: [](None)

Numpy and Scipy is foundation of Python science toolkit. This is really powerfull library, which attract researcher. In this document enumerate main features, which potential usefull for implementation in Kotlin math library. 

## Basic and unspecified features
 
 * Special class for working with [polynomials](https://docs.scipy.org/doc/numpy/reference/generated/numpy.poly1d.html#numpy.poly1d).
 * Generation of number sequence in [linear](https://docs.scipy.org/doc/numpy/reference/generated/numpy.linspace.html?highlight=linspace#numpy.linspace) and [logarithmic](https://docs.scipy.org/doc/numpy/reference/generated/numpy.logspace.html?highlight=logspace#numpy.logspace) scale.
 * Tools for [selection](https://docs.scipy.org/doc/scipy/reference/tutorial/basic.html#other-useful-functions), shuffle, [slicing](https://docs.scipy.org/doc/scipy/reference/tutorial/basic.html#index-tricks), comparison element in arrays.
 * Tools for creating prefilled [arrays](https://docs.scipy.org/doc/numpy/reference/routines.array-creation.html).
 * Native type for [complex number](https://docs.python.org/3/library/cmath.html) ([Python features](https://docs.python.org/3.7/c-api/complex.html))
 
## Common and special math function

Common and special function for advanced math, financial(?) and theoretical physics (?).

* Simple math function: Heaviside, triangle, factorial, binominal coefficient etc.
* Fast implementation of elementary function (?).
* Logic function
* Functions, integrals and zeros: Airy, Elliptic, Bessel, Riccati-Bessel, Legendre, Struve, Gamma, Beta, Fresnel, erf and [another](https://docs.scipy.org/doc/scipy/reference/special.html#module-scipy.special)
* [Information theory functions](https://docs.scipy.org/doc/scipy/reference/special.html#information-theory-functions)

## Integration

Calculation of univariate and multivariate [integral](https://docs.scipy.org/doc/scipy/reference/tutorial/integrate.html) on grid (include infinite limits)

## Optimization 

* [Sets of different minimizator](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.minimize.html#scipy.optimize.minimize)
* Tools for [fitting](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.curve_fit.html#scipy.optimize.curve_fit) and [least squres](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.least_squares.html#scipy.optimize.least_squares)
* [Univariate equation solver](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.root_scalar.html#scipy.optimize.root_scalar)
* [Multivariate equation system solvers](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.root.html#scipy.optimize.root)

## Interpolation

* [Spline](https://docs.scipy.org/doc/scipy/reference/tutorial/interpolate.html#spline-interpolation-in-1-d-procedural-interpolate-splxxx) (1d and 2d) and [B-splines](https://docs.scipy.org/doc/scipy/reference/tutorial/signal.html#b-splines)
* [1d interpolation](https://docs.scipy.org/doc/scipy/reference/generated/scipy.interpolate.interp1d.html#scipy.interpolate.interp1d) and [extrapolition](https://docs.scipy.org/doc/scipy/reference/generated/scipy.interpolate.interp1d.html#scipy.interpolate.interp1d) tools
* [Tools for smoothness interpolation](https://docs.scipy.org/doc/scipy/reference/tutorial/interpolate.html#using-radial-basis-functions-for-smoothing-interpolation)
* [Multivariate data interpolation](https://docs.scipy.org/doc/scipy/reference/generated/scipy.interpolate.griddata.html#scipy.interpolate.griddata)

## Fourier Transforms

* [Fast Fourier transforms](https://docs.scipy.org/doc/scipy/reference/tutorial/fftpack.html)

## Signal Processing 

Many tools for signal processing: window, waveforms, wavelets, spectal analysis and [another](https://docs.scipy.org/doc/scipy/reference/signal.html#module-scipy.signal)

* [Convolution](https://docs.scipy.org/doc/scipy/reference/signal.html#convolution)
* [Filtering](https://docs.scipy.org/doc/scipy/reference/signal.html#filtering)
* [Deconvolution](https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.deconvolve.html?highlight=deconvolve#scipy.signal.deconvolve)
* [Autocorrelation](https://docs.scipy.org/doc/scipy/reference/generated/scipy.ndimage.correlate.html?highlight=corre#scipy.ndimage.correlate)
* [Image processing](https://www.scipy-lectures.org/packages/scikit-image/index.html#scikit-image-and-the-scipy-ecosystem)

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

[Implementation of sparse matrix and arrays](https://docs.scipy.org/doc/scipy/reference/sparse.html)

## Spatial data structures and algorithms
[scipy.spatial](https://docs.scipy.org/doc/scipy/reference/tutorial/spatial.html) can compute triangulations, Voronoi diagrams, and convex hulls of a set of points, by leveraging the Qhull library.

## Statistics

* Generation random sequence from different [continuous](https://docs.scipy.org/doc/scipy/reference/stats.html#continuous-distributions), [multivariate](https://docs.scipy.org/doc/scipy/reference/stats.html#multivariate-distributions) and [discrete](https://docs.scipy.org/doc/scipy/reference/stats.html#discrete-distributions) distribution and [user](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.rvs_ratio_uniforms.html#scipy.stats.rvs_ratio_uniforms) distribution
* [PDF and CDF for different distribution](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.rvs_ratio_uniforms.html#scipy.stats.rvs_ratio_uniforms), inverse function
* [Calculation of momentum, median and moda for data](https://docs.scipy.org/doc/scipy/reference/stats.html#summary-statistics)
* Calculation of [percenticle, quantile](https://docs.scipy.org/doc/scipy/reference/stats.html#frequency-statistics), [correlation coeficient, covariance](https://docs.scipy.org/doc/scipy/reference/stats.html#correlation-functions)
* [Statistical tests](https://docs.scipy.org/doc/scipy/reference/stats.html#statistical-tests)
* [Kernel density estimation](https://docs.scipy.org/doc/scipy/reference/stats.html#univariate-and-multivariate-kernel-density-estimation-scipy-stats-kde) (include multivariate)
* [Histogramms](https://docs.scipy.org/doc/numpy-1.13.0/reference/routines.statistics.html#histograms):  multidimensional, with uniform and user binning

## Multidimensional image processing

[Tools for image processing](https://docs.scipy.org/doc/scipy/reference/ndimage.html) (can be used for machine and deep learning)
