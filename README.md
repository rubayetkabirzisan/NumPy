# NumPy Comprehensive README

## Table of Contents

1. Introduction
2. Creating Arrays
3. Inspecting Array Properties
4. Special Array Creation Methods
5. Random Number Generation
6. Data Types and Type Casting
7. Arithmetic Operations
8. Mathematical Functions
9. Reshaping and Dimensions
10. Broadcasting
11. Indexing and Slicing
12. Iteration Techniques
13. Copy vs View
14. Concatenation & Splitting
15. Searching, Sorting, Filtering
16. Shuffling, Unique, Resize, Flatten, Ravel
17. Insert, Append, Delete
18. Matrix Operations & Linear Algebra

---

## 1. Introduction

NumPy is a powerful numerical computing library used for efficient array operations, mathematical computations, and scientific computing.

**Example:**

```python
import numpy as np
x = np.array([1,2,3])
print(x)
```

---

## 2. Creating Arrays

### Using `np.array()`

```python
import numpy as np
x = np.array([1,2,3,4])
```

### Converting list to array

```python
lst = [1,2,3]
arr = np.array(lst)
```

### Multidimensional arrays

```python
ar2 = np.array([[1,2,3],[4,5,6]])
```

---

## 3. Inspecting Array Properties

### Dimension count

```python
arr.ndim
```

### Shape

```python
arr.shape
```

### Creating minimum dimension arrays

```python
arr = np.array([1,2,3], ndmin=4)
```

---

## 4. Special Array Creation Methods

```python
np.zeros((3,4))
np.ones(4)
np.empty(4)
np.arange(1,10)
np.eye(3)
np.linspace(1,20,5)
```

---

## 5. Random Number Generation

```python
np.random.rand(4)
np.random.randn(4)
np.random.randint(1,100,5)
np.random.ranf(4)
```

---

## 6. Data Types and Casting

### Checking dtype

```python
arr.dtype
```

### Casting types

```python
new = arr.astype(float)
```

### Using specific dtypes

```python
x = np.array([1,2], dtype=np.int8)
```

---

## 7. Arithmetic Operations

```python
var + 3
np.reciprocal(var)
var1 + var2
np.mod(var1, var2)
var1 * var2
```

---

## 8. Mathematical Functions

```python
np.min(arr)
np.max(arr)
np.sqrt(arr)
np.argmin(arr)
np.argmax(arr)
np.sin(arr)
np.cos(arr)
np.cumsum(arr)
```

---

## 9. Reshaping and Dimensions

```python
x = arr.reshape(3,2)
y = arr.reshape(2,3,2)
z = y.reshape(-1)
```

---

## 10. Broadcasting

```python
var1 + var2
x + y
```

---

## 11. Indexing and Slicing

```python
arr[1]
arr[1:6]
arr[::2]
arr2[1,1]
arr3[1,1,1]
```

---

## 12. Iteration Techniques

### Normal iteration

```python
for i in arr: print(i)
```

### Nested loops for multi-dimensional arrays

```python
for row in arr:
    for val in row:
        print(val)
```

### `nditer`

```python
for i in np.nditer(arr): print(i)
```

### `ndenumerate`

```python
for idx, val in np.ndenumerate(arr): print(idx,val)
```

---

## 13. Copy vs View

```python
copy_arr = arr.copy()
view_arr = arr.view()
```

---

## 14. Concatenation & Splitting

### Concatenation

```python
np.concatenate((arr1, arr2))
np.vstack((arr1, arr2))
np.hstack((arr1, arr2))
np.dstack((arr1, arr2))
```

### Splitting

```python
np.array_split(arr, 2)
```

---

## 15. Searching, Sorting, Filtering

```python
np.where(arr % 2 == 0)
np.searchsorted(arr, [5,6], side="right")
np.sort(arr)
filtered = arr[boolean_mask]
```

---

## 16. Shuffle, Unique, Resize, Flatten

```python
np.random.shuffle(arr)
np.unique(arr, return_index=True, return_counts=True)
np.resize(arr, (2,3))
arr.flatten(order='F')
arr.ravel(order='C')
```

---

## 17. Insert, Append, Delete

```python
np.append(arr, 6)
np.insert(arr, 2, 10)
np.delete(arr, 3)
```

---

## 18. Matrix Operations & Linear Algebra

### Matrix multiplication

```python
A * B
A.dot(B)
```

### Transpose

```python
A.T
```

### Inverse

```python
np.linalg.inv(A)
```

### Determinant

```python
np.linalg.det(A)
```

### Matrix power

```python
np.linalg.matrix_power(A, 2)
```

---

