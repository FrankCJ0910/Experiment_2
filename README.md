Problem 1 :
The first problem tasks us to create a random array 5 by array and normalize it.
  Formula:(X-𝑥̅)/𝜎
  where: X is the element of the array,
         𝑥̅ is the mean of the array,
         𝜎 is the standard deviation

I use the numerical python library to solve the following problems which lets us create and manipulate different arrays
Using this line, I import the libary as np to be used in the code

``` python
  import numpy as np
```

To solve problem 1, the program first creates two 5x5 arrays, one with random values and another that is empty

``` python
  X = np.random.random((5,5))
  norm = np.zeros([5,5])
```

The program then gets the mean and standard deviation of array X

``` python
  m = X.mean()
  std = X.std()
```

The program then uses a nested for loop to normalize array X

``` python
  #Nested loop for every row and column of X
  for i in range(5):
      for j in range(5):
          #Perform normalization on each element
          norm[i,j] = (X[i,j] - m)/std
```

The program then saves the normalized value into a file named 'X_normalized.npy'

``` python
  np.save('X_normalized.npy',norm)
```

Problem 2
  This problem tasks us to create a 10x10 array with the squared values of 1 to 100, then find all of the values that are divisible by 3 and store it in an array
