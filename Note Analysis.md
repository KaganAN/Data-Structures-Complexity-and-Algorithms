# Matrices & List Comprehension:
## Matrices in Python 3:
---
  #### What is a Matrix?:
  - **Mathetmatically:** A matrix is a representation of numbers, symbols, and/or expressions in a 2D array.
  - **Computer Science:** A representation of data strcutures with values in rows and columns like the example shown below. This can be done by creating a list within a list or with imported modules and libraries.

Matrix array example:

![matrix_fig01](https://user-images.githubusercontent.com/129294925/233080490-9c74143b-371f-483d-85d7-08d20c95c0f6.png)

[*Source*](https://mrparkonline.github.io/courses/datastruct/matrices/)

[Matrix in Python 3 example](https://mrparkonline.github.io/courses/datastruct/matrices/):

```python3
matrix = [
    [1, 2, 3, 4,],
    [5, 6, 7, 8,]
]

# Accessing 'matrix'
print('Row 1: %s' % matrix[0]) #Indexing
print('Value at Row 2 Column 2: %s' % matrix[1][1])

#Outputs:
#The output of the first print statement will be an index of the first row (Row 1: [1, 2, 3, 4])
#The output of the second print statement will be an index of row 2 column 2 (Value at Row 2 Column 2: 6)
```
  - Since the data structure of a "Matrix" does not exist in Python 3, we use a list within a list
---
## List Comprehension in Python 3
---
  - List comprehension is a succient way to create lists in Python
  
  - Common uses:
    - A list is created as a result of an operation being applied to all its items
    - A list is made from another set of sequences/iterable data
    - A list is a member of another list, sequence, and/or iterable data
  
  [List Comprehension Example 1](https://mrparkonline.github.io/courses/datastruct/matrices/):
  
  ```python3
  
  #Creating a list to square all the numbers from 0 - 10
  #List Comp method
  
  squares = [i**2 for i in range(10)]
  
  print('Our new result: %s' % squeres)
  
  #Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
  ```
  - 
  
  [List Comprehension Example 2](https://mrparkonline.github.io/courses/datastruct/matrices/)
  
  ```python3
  
  

