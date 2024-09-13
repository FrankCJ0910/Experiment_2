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

Problem 2 :
  This problem tasks us to create a 10x10 array with the squared values of 1 to 100, then find all of the values that are divisible by 3 and store it in an array

First created an empty array to store values

``` python
  A = np.zeros([10,10])
```

A nested loop is used to populate the array with squared values of the first 100 integers

``` python
  #Starting value of array
  n = 1
  #Nested loop for each element of A
  for i in range(10):
      for j in range(10):
          #Store the value of n squared
          A[i,j] = n**2
          #increment value of n by 1
          n += 1
```

The array is then spliced to get the values of A that are divisible by 3 and stored in B

``` python
  B = A[A%3==0]
```

B is then saved into a file named 'div_by_3.npy'

``` python
  np.save('div_by_3.npy',B)
```
