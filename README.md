Problem 1 :
/tThe first problem tasks us to create a random array 5 by array and normalize it.
  /tformula:(X-𝑥̅)/𝜎
  w/there: X is the element of the array
         𝑥̅ is the mean of the array
         𝜎 is the standard deviation

I use the numerical python library to solve this problem which lets us create and manipulate different arrays

``` python
  import numpy as np
```

Using this line, I immport the libary as np to be used in the code

``` python
  X = np.random.random((5,5))
```

To create the 5x5 array, I use the np.random.random() function and store it into X

``` python
  m = X.mean()
  std = X.std()
```

I used .mean() and .std() functions to get the mean and standard deviation of the entire array and store it into m for mean and std for standard deviation

``` python
  norm = np.zeros([5,5])
```

I create an empty 5x5 array using np.zeros() for storage of the normalized X values

``` python
  for i in range(5):
    for j in range(5):
```

To go through every element of the array X, I use a nested for loop with values of range(5) since this function gives the value of 0-4 which lets the program check every element of X

``` python
      norm[i,j] = (X[i,j] - m)/std
```

Inside the nested for loop is this line of code, which takes an element from array X with the index value of i and j, then subtracts it with the mean and divides it with the std and lastly stores it into norm

``` python
  np.save('X_normalized.npy',norm)
```

Lasltly for problem 1, it asks us to save the normalized array into X_normalized.npy which the .save() function does for the program
