# Programming Assignment 2
Advanced Computer Programming

Joseph Bryn P. Carungay - 2ECE-C

# Advanced Computer Programming Assignment 2
## 1. Normalization Problem
### A program that generates a random 5x5 array and used for basic preprocessing techniques in data analytics

    - Key parts of the code
      - import numpy as np is used to load NumPy library
      - np.random.rand(5,5) is used to generate a random 5x5 ndarray
      - .mean() is used to compute the mean of the ndarray
      - .std() is used to compute the standard deviation of the ndarray
      - (X - mean) / std is the normalization formula
      - np.save("X_normalized.npy", X_normalized) is used to save the normalized array

### Conclusion
### In summary, this program creates a random 5x5 array and applies normalization using the formula (X - mean) / std. The mean was computed with .mean() and the standard deviation with .std(). The resulting normalized array was then stored as a .npy file using np.save(). This process demonstrates how normalization prepares data by centering and scaling values to make them more consistent for analysis.

## 2. Squares of Integers Divisible by 3 Problem
### A program that creates a 10x10 array of squares of the first 100 integers and extract integers divisible by 3.

    - Key parts of the code
      - import numpy as np is used to load NumPy library
      - np.arange(1,101) is used to generate integers from 1 to 100
      - numbers**2 is used to compute the squares of numbers
      - .reshape(10,10) is used to form a 10x10 ndarray
      - X % 3 == 0 is used to filter elements divisible by 3
      - np.save("div_by_3.npy", div_by_3) is used to save the divisible elements

### Conclusion
### In summary, this program constructs a 10x10 array containing the squares of the first 100 positive integers and identifies the elements that are divisible by 3. The array  was generated using np.arange(), squared, and reshaped with .reshape(). A condition (X % 3 == 0) was applied to filter the results, which were then saved as a .npy file through np.save(). This showcases NumPy’s efficiency in generating, manipulating, and storing structured numerical data.
