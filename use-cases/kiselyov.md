# Example of Numpy features using in scientific programming

* **Type**: Use case
* **Author**: Alexander Kiselyov
* **Status**: 
* **Discussion**: [](None)

## Multidimensional arrays

`numpy.ndarray` provides a number of very simple, intuitive and efficient approaches for working with (almost) homogeneous data. Theses are especially useful and scalable when working with multidimensional arrays. First, fancy indexing, `shape` and `dtype` mechanics provide very handy and concise methods for selecting from an array. In many cases these operations can be done transparently without making copies. The memory footprint for `numpy.ndarray` is quite predictable, with low overhead. Structured arrays can be lightweight alternatives for `pandas.DataFrame`, when performance and memory usage are important but index is not (_it was so in most of my tasks_). Masked array is a lightweight alternative for treating missing data.

Vectorization of operations and selection's methods is usefull for solituon of applied task such as working with finite-difference scheme. Using cycle for iteration of conteiners is more verbose and implicit, than point-wise operation and don't request excess representation such as vectors and matrix (For example: `0.5*(a[1:] +a[:-1]`).

Vectorized operations on numpy arrays allow for performing many elementwise array operations with small code footprint and better readability compared to using loops. Of note is that these capabilities does not require to represent the data in form of linear algebra matrices and vectors, which can sometimes be quite cumbersome. An example is working with finite-difference schemes. By the way, in this case `numpy` plays very good with `numexpr` to parallelize these operations.

Vectorized operation example -- calculation of a midpoint for each grid cell:

```
# Prepare initial data
edges = numpy.arange(0, 100, 5)

# For-loop (long!)
midpoints = np.empty(len(edges) - 1)  # need to allocate new array
for idx in range(len(edges) - 1):
    midpoints[idx] = .5*(edges[idx] + edges[idx + 1])

# Vectorized operations (short!)
midpoints = .5*(edges[:-1] + edges[1:])
```

## Specific scientific task

* [numpy.fft](https://docs.scipy.org/doc/numpy-1.15.0/reference/routines.fft.html) --- computation of convolution, [upsampling](https://en.wikipedia.org/wiki/Upsampling) etc. In some cases, `numpy.fft` is very ineffective due to using [Cooley–Tukey FFT algorithm](https://en.wikipedia.org/wiki/Cooley%E2%80%93Tukey_FFT_algorithm), but looks like a patch for Bluestein algorithm is under way.
* [scipy.signal](https://docs.scipy.org/doc/scipy/reference/signal.html) --- [Butterworth filter](https://en.wikipedia.org/wiki/Butterworth_filter), searching of local extrema, estimation of PSD using [Welch’s method](https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.welch.html#r34b375daf612-1)
* [scipy.linalg](https://docs.scipy.org/doc/scipy/reference/tutorial/linalg.html) --- solving linear systems
* [scipy.stats](https://docs.scipy.org/doc/scipy/reference/tutorial/stats.html) --- regression
* [scipy.integrate.ode](https://docs.scipy.org/doc/scipy/reference/generated/scipy.integrate.ode.html) --- quick solving of ODEs.

## I/O operations

Numpy provides a number of methods for (de)serialization of multidimensional arrays. First, it natively supports some widespread formats such as Matlab data files plus others through third-party libraries (e.g. HDF5 via [h5py](https://www.h5py.org/) or [pytables](https://www.pytables.org/)) with good interoperability. Second, it has its own very simple on-disk array format. It has a [short specification](http://www.numpy.org/neps/nep-0001-npy-format.html) and stores all information required to reconstruct an array on any machine. Numpy implementation of this format is quite fast.

## About author experience

The author has been using actively using Numpy/Scipy for 7 years mainly to perform numerical PIC plasma simulations (also with `pyopencl`) and VHF interfermetry data processing.
