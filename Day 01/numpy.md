
# Numpy

### Attributes
- ndim
- shape
- size: number of elements in the array
- dtype
- flat: the array flattened in 1 dimension for iterating

### Functions
- np.function()
    - array([], dtype=np.int16)
    - zeros(dim, dim, ...)
    - ones(dim, dim, ...)
    - empty(dim, dim, ...): fills the array with random values
    - arange(start in, end ex, skip): as python
    - linspace(start in, end in, n.elements)
- array.function()
    In these you can also specify the axis on which you want to perform the operations with axis=1
    - arr.sum()
    - arr.min()
    - arr.max()
    - arr.mean()
    - arr.std()
    - arr.sort()
    - arr.unique()
    - arr.concatenate()
    - arr.random.rand(size=(1 or more)): random number from 0 to 1
    - arr.random.randn(size=(1 or more)): random number also negative
    - arr.random.randint(top, size=(...))
- Universal functions:
    - np.sum(arr)
    - np.sin(arr)
    - np.exp(arr)
    - np.sqrt(arr)
    - np.all(arr)
    - np.any(arr)
    - np.max(arr)
    - np.floor()
    - ..... 

### Operations
+ - * /      ...  : create a new array.

+= -= *= /=  ...  : modify existing array.

### Indexing and slicing
With 1 axis is the same as lists in Python.

With 2 or more axis (take the second element of each row of the matrix):
```
arr[0:5, 1]  
# or
arr[:, 1] 
```
When fewer indices are provided than the number of axes, the missing indices are considered complete slices

### Iterating 
Same as lists in Python.

### Reshaping
- a.ravel(): the array in 1 dimension, copy=False
- arr.reshape(dim, dim, ...): creates a copy
- arr.resize((dim, dim,...)): no copy
- a.T: makes a transposition, inverting the axis

By putting -1 in **ONLY ONE** of the axis' dimension, it understand on his own what's the value needed

### Stacking
- np.hstack((arr1, arr2))
- np.vstack((arr1, arr2))
- np.column_stack((arr1, arr2))

```
a = np.floor(10 * rg.random((2, 2)))   --->
array([[9., 7.],
       [5., 2.]])

b = np.floor(10 * rg.random((2, 2)))   --->
array([[1., 9.],
       [5., 1.]])

np.vstack((a, b))   --->
array([[9., 7.],
       [5., 2.],
       [1., 9.],
       [5., 1.]])

np.hstack((a, b))   --->
array([[9., 7., 1., 9.],
       [5., 2., 5., 1.]])

a = np.array([4., 2.])
b = np.array([3., 8.])

np.column_stack((a, b))   --->
array([[4., 3.],
       [2., 8.]])

np.hstack((a, b))   --->
array([4., 2., 3., 8.])
```