# ECE-2112-PA2
This repository contains the implementation for ECE 2112 - Experiment 2: Numerical Python (NumPy). It demonstrates vectorized array operations, array reshaping, statistical calculations, and Boolean filtering in Python without using standard loops or list comprehensions. Key tasks include normalizing a reproducible 5x5 random matrix, applying Boolean conditions to filter cubed integers divisible by 4, and selecting elements above the mean from a matrix of squared values, with all outputs verified and saved as binary .npy files.

First, import the NumPy Library into the Python environment using the standard alias to enable vectorized array operations and numerical processing.  

Code: `import numpy as np`

The import numpy statement loads the NumPy library and its numerical functions into the notebook's runtime environment. Meanwhile, the as np part creates a standard shortcut alias, allowing all NumPy functions and data structures to be called using np. Instead of typing out numpy. repeatedly.

# A. Reproducible Normalization Problem

Create a 5x5 matrix of reproducible random integers between 10 and 100, normalize its values using its mean and standard deviation, and save the output array.

Code: `X_normalized = (X - X.mean()) / X.std()`

The first section of code sets the random seed to 2112 and generates a 5x5 array named `X` with random integers ranging from 10 to 100. Meanwhile, the second statement normalizes the array by subtracting the overall mean (`X.mean()`) from each element and dividing by the population standard deviation (`X.std()`) to store the normalized result in `X_normalized`.

Example: `X_normalized.mean()` and `X_normalized.std()`

For example, checking `X_normalized.mean()` returns `0.0` and `X_normalized.std()` returns `1.0`, confirming the matrix has been centered around zero with unit variance before saving it as `"X_normalized.npy"`.

B. Cubes Divisible by 4 Problem

Create an array of the first 100 positive integers, cube each value, reshape it into a 10x10 matrix, extract all elements divisible by 4 using Boolean indexing, and save the filtered array.  

Code: `div_by_4 = C[C % 4 == 0]`

The first section generates integers from 1 to 100 using `np.arange(1, 101)`, computes their cubes with `C = x**3`, and reshapes the array into a 10x10 matrix. Meanwhile, the Boolean condition `C % 4 == 0` checks each cubed value for divisibility by 4, filtering out only the matching elements and storing them in `div_by_4`.  

Example: `div_by_4 `and `np.save("div_by_4.npy", div_by_4)`. 

C. Above-Mean Squares Problem

Create a 6x6 matrix containing the squares of the first 36 positive integers, calculate its overall mean, filter for elements strictly greater than the mean, and save the filtered array.  

Code: `above_mean = S[S > S_mean]`

The first section generates the squares of integers from 1 to 36 using `np.arange(1, 37) ** 2` and formats them into a 6x6 matrix `S`. Meanwhile, `S.mean()` calculates the average value of all elements (450.17), and the Boolean condition `S > S_mean` filters out only the values strictly greater than this average, storing the result in `above_mean`.  

Example: `above_mean.size` and `np.save("above_mean.npy", above_mean)`
