# Matrices & List Comprehension:
## Matrices in Python 3:
---
  #### What is a Matrix?:
  - **Mathetmatically:** A matrix is a representation of numbers, symbols, and/or expressions in a 2D array.
  - **Computer Science:** A representation of data strcutures with values in rows and columns like the example shown below. This can be done by creating a list within a list or with imported modules and libraries.

[*Matrix array example*](https://mrparkonline.github.io/courses/datastruct/matrices/)

![matrix_fig01](https://user-images.githubusercontent.com/129294925/233080490-9c74143b-371f-483d-85d7-08d20c95c0f6.png)

[*Matrix in Python 3 example*](https://mrparkonline.github.io/courses/datastruct/matrices/):

```python3
matrix = [
    [1, 2, 3, 4,],
    [5, 6, 7, 8,]
]

#Accessing 'matrix'
print('Row 1: %s' % matrix[0]) #Indexing
print('Value at Row 2 Column 2: %s' % matrix[1][1])

#Outputs:
#The output of the first print statement will be an index of the first row (Row 1: [1, 2, 3, 4])
#The output of the second print statement will be an index of row 2 column 2 (Value at Row 2 Column 2: 6)
```
  - Since the data structure of a "Matrix" **does not exist** in Python 3, we use a list within a list
---
## List Comprehension in Python 3
---
  #### What is list comprehension?
  - List comprehension is a **consice** way to create lists in Python
  
  - **Common uses**:
    - A list is created as a result of an operation being applied to all its items
    - A list is made from another set of sequences/iterable data
    - A list is a member of another list, sequence, and/or iterable data
  
  [*List Comprehension Example 1*](https://mrparkonline.github.io/courses/datastruct/matrices/):
  
  ```python3
  
  #Creating a list to square all the numbers from 0 - 10
  #List Comp method
  
  squares = [i**2 for i in range(10)]
  
  print('Our new result: %s' % squeres)
  
  #Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
  ```
  ---
  # Map & Filter in Python 3
  ## The Map Function
  ---
  #### What is the map function?
  - Map function *applies* a function to a set of **iterable** data

  [*Map Function Example*](https://mrparkonline.github.io/courses/datastruct/map/):                              
  ```python3
    #Formatted as: 
    map(function_name, sequence)
    
    #Example of map function
    def square(num):
      return num ** 2
    #end square function (function squares the number argument given)
    
    array = list(range(1, 11))
    square_array = list(map(square, array))
    
    print('Original Array', array)
    print('Array Squared:', square_array)
    
    #Output: Original Array: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    #Output 2: Array Squared: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
   ```
   - Map function doesn't return any specific data type so it is common practice to execute a list function after using map
   ---
   ## Filter Function
   ---
   #### What is the filter function?
   - Filter function filters out the items of the set **depending on a set of criteria** which must be met
   
   [*Filter Function Example*](https://mrparkonline.github.io/courses/datastruct/map/)
   ```python3
   #Formatted as:
   filter(bool_returning_function, sequence)
   
   #Example of filter function
   def isOdd(x):
   
    return x % 2 != 0 
   #end of isOdd function (function returns True if x is odd)
   
   array = list(range(1,101))
   odds = list(filter(isOdd, array))
   
   print('Odd Numbers from 1 to 100:', odds)
   
   #Output: Odd Numbers from 1 to 100: [1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51, 53, 55, 57, 59, 61, 63, 65, 67, 69, 71, 73, 75, 77, 79, 81, 83, 85, 87, 89, 91, 93, 95, 97, 99]
   ```
   #### Composition of functions:
   - The concept of using a function while **calling upon another function** or **applying a function to the result of another function**
   ---
   # Tuples in Python 3
   #### What are Tuples? 
   ---
   - Strings and Lists are iterable data types with a **few differences**:
      - Strings can only allow alphanumeric and special characters for text
      - Lists allow all data types to be within it
      - Strings are immutable but lists are mutable
      
   - These differences **cause problems** when data must:
      - Be immutable
      - Allow different datatypes within them
      - Be iterable
      - Be nestable
      
   - **Tuples fix these issues**
   
   - Tuples can be **iterable**, **indexable**, and/or **sliceable** 

   [*Tuple Example*](https://mrparkonline.github.io/courses/datastruct/tuples/)
   ```python3
   tup = ('C', 'Java', 'Python')
   empty_tup = ()
   single_tup = ('Park',)
   
   print(tup)
   print(empty_tup)
   print(single_tup)
   
   #Output: ('C', ' Java', 'Python')
   #Output 2: ()
   #Output 3: ('Park',)
   ```
   ---
   #### Tuple Operators
   ---
   - **Concatenation**: Joining two tuples
   - **Repetition**: Repeating a list 
   - **Membership**: Check if a value is in a tuple
   
   ---
   #### [Tuple Comprehension](https://mrparkonline.github.io/courses/datastruct/tuples/)
   ---
   ```python3
   # Tuple of even values from a range of 1 to 100 
   even_tup - tuple(i for i in range(1, 101) if i % 2 == 0)
   
   print(even_tup)
   #Output: (2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30, 32, 34, 36, 38, 40, 42, 44, 46, 48, 50, 52, 54, 56, 58, 60, 62, 64, 66, 68, 70, 72, 74, 76, 78, 80, 82, 84, 86, 88, 90, 92, 94, 96, 98, 100)
   ```
   - General format of tuple comprehension is the same as list comprehension
   
   ---
   #### [Tuple & Python: Packing and Unpacking](https://mrparkonline.github.io/courses/datastruct/tuples/)
   ---
   ```python3
   #Packing
   var_1 = 2
   var_2 = 3
   var_3 = 5
   
   prime = var_1, var_2, var_3 
   
   print('Packed prime values:', prime)
   
   #Unpacking and Repacking
   fib = (0, 1, 2, 3, 5, 8)
   
   fib_0, fib_1, fib_n = fib[0], fib[1], fib[2:]
   print('fib_0:', fib_0)
   print('fib_1:', fib_1)
   print('fib_n:', fib_n)
   
   #Output: Packed prime values: (2, 3, 5)
   #Output 2: fib_0: 0
   #Output 3: fib_1: 1
   #Output 4: fib_n: (1, 2, 3, 5, 8)


   
   


 
   
    
  

