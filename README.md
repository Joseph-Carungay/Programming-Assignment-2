# Programming Assignment 2
Advanced Computer Programming

Joseph Bryn P. Carungay - 2ECE-C

# Advanced Computer Programming Assignment 2
## 1. Normalization Problem
### A program that generates a random 5x5 array and used for basic preprocessing techniques in data analytics
---
#### Code:
#### Generating and Displaying a Random 5x5 Array
    import numpy as np          #Import the NumPy library as np
    X = np.random.rand(5, 5)    #Create a 5x5 array of random numbers between 0 and 1 and store it in X 
    print("Original Array X: ") #Print the label "Original Array X:"
    print(X)                    #Print the array X
<img width="966" height="365" alt="image" src="https://github.com/user-attachments/assets/a6395abd-aed3-48af-a5b8-5c1017470a45" />

#### Calculating Mean and Standard Deviation of an Array
    mean = X.mean()                      #Calculate the mean of all elements in X and store it in mean
    std = X.std()                        #Calculate the standard deviation of all elements in X and store it in std
    print("Mean of X: ")                 #Print the "Mean of X:"
    print(mean)                          #Print the mean value
    print("Standard Deviation of X: ")   #Print the "Standard Deviation of X:"
    print(std)                           #Print the standard deviation value
<img width="893" height="300" alt="image" src="https://github.com/user-attachments/assets/febc5f58-8c1a-4af8-865e-aa5d34a69d89" />

#### Normalizing a 5x5 Array Using Mean and Standard Deviation
    X_normalized = (X - mean) / std   #Normalize the array X using (X - mean) / std and store it in X_normalized
    print("Normalized Array: ")       #Print the label "Normalized Array:"
    print(X_normalized)               #Print the normalized array X_normalized
<img width="1032" height="272" alt="image" src="https://github.com/user-attachments/assets/a4cf8970-471b-4d9a-8384-8e2257d04a0f" />

#### Saving the Normalized Array to a .npy File
    np.save('X_normalized.npy', X_normalized)             #Save the normalized array X_normalized to a file named X_normalized.npy
    print("Normalized array saved as X_normalized.npy")   #Print a message confirming the array has been saved
<img width="1111" height="147" alt="image" src="https://github.com/user-attachments/assets/46ddfc80-28dd-49a8-8f4e-c058b7292136" />

#### Key parts of the code:
    - import numpy as np is used to load NumPy library
    - np.random.rand(5,5) is used to generate a random 5x5 ndarray
    - .mean() is used to compute the mean of the ndarray
    - .std() is used to compute the standard deviation of the ndarray
    - (X - mean) / std is the normalization formula
    - np.save("X_normalized.npy", X_normalized) is used to save the normalized array
---
### Conclusion:
####  In summary, this program creates a random 5x5 array and applies normalization using the formula (X - mean) / std. The mean was computed with .mean() and the standard deviation with .std(). The resulting normalized array was then stored as a .npy file using np.save(). This process demonstrates how normalization prepares data by centering and scaling values to make them more consistent for analysis.
---
## 2. Squares of Integers Divisible by 3 Problem
### A program that creates a 10x10 array of squares of the first 100 integers and extract integers divisible by 3.
---
#### Code:
#### Creating a 10x10 Array of Squares of the First 100 Integers
    numbers = np.arange(1, 101)                                 #Create an array of numbers from 1 to 100 and store it in numbers
    squares = numbers**2                                        #Calculate the square of each number and store it in squares
    X = squares.reshape(10, 10)                                 #Reshape squares into a 10x10 array and store it in X
    print("Array of the squares of the first 100 integers: ")   #Print the label "Array of the squares of the first 100 integers:"
    print(X)                                                    #Print the 10x10 array X
<img width="1216" height="470" alt="image" src="https://github.com/user-attachments/assets/b677a1ff-c1f9-4e68-b001-7abf639cb1aa" />

#### Extracting Elements Divisible by 3 from the Array
    div_by_3 = X[X % 3 == 0]             #Filter elements in X that are divisible by 3 and store them in div_by_3
    print("Integers divisible by 3: ")   #Print the label "Integers divisible by 3:"
    print(div_by_3)                      #Print the filtered array div_by_3
<img width="955" height="225" alt="image" src="https://github.com/user-attachments/assets/07368a68-a004-4bf2-972d-b3565bb3b739" />

#### Saving Filtered Elements Divisible by 3 to a .npy File
    np.save('div_by_3.npy', div_by_3)      #Save the array div_by_3 to a file named div_by_3.npy
    print("Saved result as div_by_3.npy")  #Print a message confirming the array has been saved
<img width="910" height="155" alt="image" src="https://github.com/user-attachments/assets/e4d74e97-86cc-49c2-9879-ecaadadfeb69" />

#### Key parts of the code:
    - import numpy as np is used to load NumPy library
    - np.arange(1,101) is used to generate integers from 1 to 100
    - numbers**2 is used to compute the squares of numbers
    - .reshape(10,10) is used to form a 10x10 ndarray
    - X % 3 == 0 is used to filter elements divisible by 3
    - np.save("div_by_3.npy", div_by_3) is used to save the divisible elements
--- 
### Conclusion:
#### In summary, this program constructs a 10x10 array containing the squares of the first 100 positive integers and identifies the elements that are divisible by 3. The array  was generated using np.arange(), squared, and reshaped with .reshape(). A condition (X % 3 == 0) was applied to filter the results, which were then saved as a .npy file through np.save(). This showcases NumPy’s efficiency in generating, manipulating, and storing structured numerical data.
