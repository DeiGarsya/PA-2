# Programming Assignment 2
NAME : Deirojel Martin M. Garcia

SECTION : 2ECE-A

SUBMITTED : September 9, 2024

## Problem 1: Normalization Problem

In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized
ndarray as X_normalized.npy .

We start with the code

``` python
**x = np.random.random((5,5))**
```
to create a random value 5x5 array then in the next line, we perform an operation of normalization on the values inside the array.

``` python
**z = (x - np.mean(x)) / np.std(x)**
```
The formula for normalization is the value minus the mean of values divided by the standard deviation of the values.

Finally we save the values in variable z into a file with the function np.save and name the file 

``` python
**np.save("X_normalized.npy", z)**
```

## Problem 2: Divisible by 3 Problem
Create a 10 x 10 ndarray which are the squares of the first 100 positive integers. From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy

In this problem, we start of by creating the 10 x 10 array of squares with this code 

``` python
A = np.arange(1,101)**2
```
Here we create an array of 1 to 100 and at each interval, the values is squared with the use of the operator **2. 

``` python
A = A.reshape(10,10)
```
With this code we rearrange the created array above into a 10 x 10 array 

``` python
X = A[A % 3 == 0]
```
With this line, we test each number in the array that are divisible by 3 using the modulo operator and if the result bares a remainder of 0 (==0) the number will be saved in to a new array.

Lasly we need to save the filtered values into a file using this function where the data in variable x is saved into a file named  "div_by_3.npy".

``` python
np.save("div_by_3.npy", X)
```
