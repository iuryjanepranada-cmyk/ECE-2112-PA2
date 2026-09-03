# ECE-2112-PA2
This repository contains the implementation for ECE 2112 - Experiment 2: Numerical Python (NumPy). It demonstrates vectorized array operations, array reshaping, statistical calculations, and Boolean filtering in Python without the use of standard loops or list comprehensions. Key tasks include normalizing a reproducible 5x5 random matrix, applying Boolean conditions to filter cubed integers divisible by 4, and selecting elements above the mean from a matrix of squared values, with all outputs verified and saved as binary .npy files.
# A. Reproducible Normalization Problem

Create a 5x5 matrix of reproducible random integers between 10 and 100, normalize its values using its mean and standard deviation, and save the output array.

Code: `X_normalized = (X - X.mean()) / X.std()`

The first section of code sets the random seed to 2112 and generates a 5x5 array named `X` with random integers ranging from 10 to 100. Meanwhile, the second statement normalizes the array by subtracting the overall mean (`X.mean()`) from each element and dividing by the population standard deviation (`X.std()`) to store the normalized result in `X_normalized`.

Example: `X_normalized.mean()` and `X_normalized.std()`

For example, checking `X_normalized.mean()` returns `0.0` and `X_normalized.std()` returns `1.0`, confirming the matrix has been centered around zero with unit variance before saving it as `"X_normalized.npy"`.
