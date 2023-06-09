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
   ## What are Tuples? 
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
   
   - Tuples use round brackets
   - There can be empty tuples
   - A comma is used for singleton tuples (only one item)
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
   ## Tuple Operators
   ---
   - **Concatenation**: Joining two tuples
   - **Repetition**: Repeating a list 
   - **Membership**: Check if a value is in a tuple
   
   ---
   ## [Tuple Comprehension](https://mrparkonline.github.io/courses/datastruct/tuples/)
   ---
   ```python3
   # Tuple of even values from a range of 1 to 100 
   even_tup - tuple(i for i in range(1, 101) if i % 2 == 0)
   
   print(even_tup)
   #Output: (2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30, 32, 34, 36, 38, 40, 42, 44, 46, 48, 50, 52, 54, 56, 58, 60, 62, 64, 66, 68, 70, 72, 74, 76, 78, 80, 82, 84, 86, 88, 90, 92, 94, 96, 98, 100)
   ```
   - General format of tuple comprehension is the **same as list comprehension**
   
   ---
   ## [Tuple & Python: Packing and Unpacking](https://mrparkonline.github.io/courses/datastruct/tuples/)
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
   ```
   - **Packing** grabs multiple variable values and assigns them all to one variable
   - **Unpacking** allows certain values from a tuple to be assigned to different variables
   - This is useful for Function definitions and calls
   ---
   # Sets in Python 3
   ## Using Sets in Python 3
   ---
   - A set is a collection of values with **no duplicates** and in **no particular order**
   - A **mathematical** way to describe a **unique set of objects**
   [*Defining a Set*](https://mrparkonline.github.io/courses/datastruct/sets/)
   ```python3
   #Examples of set defintiions
   example_set1 = {1, 2, 3}
   example_set2 = {'h', 'e', 'l', 'l', 'o'}
   
   print('example_set1:', example_set1)
   print('example_set2:', example_set2)
    
   singleton_set = {7}
   empty_set = set()
   
   print('Singleton:', singleton_set)
   print('Empty Set:', empty_set)
   
   #Output: example_set1: {1, 2, 3}
   #Output 2: example_set2: {'o', 'e', 'h', 'l'}
   #Output 3: Singleton: {7}
   #Output 4: Empty Set: set()
   ```
   
   - Note: The order of example_set2 output and the fact that there is **only one** 'l'
   
   ## Basic Membership Operations
   ---
   - Membership is a vital operation with sets because:
      - A set has **no duplicates**
      - A set's membership operation is extremely **fast compared to strings, lists, or tuples**
      - Membership operator can **guarantee if a targer does or does not exist in our data**

   [*Membership Example*](https://mrparkonline.github.io/courses/datastruct/sets/)
   ```python3
   example_set = set('hello')

   print("Membership of: \'h\'", 'h' in example_set)
   print("Non-Membership of: \'z\'", 'z' not in example_set)
   
   #Output: Membership of: 'h' True
   #Output2: Non-Membership of: 'z' True
   ```
   ---
   ## Accessing Values in a Set
   ---
   - Sets are **unordered** so we **cannot index or slice** them however they **are iterable**
   [*Iterating of a Set Example*](https://mrparkonline.github.io/courses/datastruct/sets/)
   ```python3
   example_set = {2,3,5,7,11,13}

   for v in example_set:
   print('Values of example_set:', v)
   
   #Output: Values of example_set: 2
   #Output2: Values of example_set: 3
   #Output3: Values of example_set: 5
   #Output4: Values of example_set: 7
   #Output5: Values of example_set: 11
   #Output6: Values of example_set: 13
   ```
   ---
   ## Adding and Removing Values from a Set
   ---
   - Sets **are mutable** so we can **add or remove** values
   [*Adding and Removing Example*](https://mrparkonline.github.io/courses/datastruct/sets/)
   ```python 3
   languages = set()
   programming_languages = ['C', 'C#', 'Java', 'Python', 'HTML', 'CSS', 'JavaScript', 'Haskell']
   
   #.add() used to add item to a set
   for item in programming_languages:
    languages.add(item) 
    
   print('Languages set:', languages)
   
   #Removes target if found
   languages.discard('HTML')
   print('HTML deleted:', langauges)
   
   #Similar to discard but will raise an error if target not found
   langauges.remove('CSS')
   print('CSS deleted:', languages)
   
   #.pop() deletes and returns a random value
   random_remove = languages.pop()
   print('Randomly Removed value:', random_remove)
   
   #.clear() empties an entire set thus making the output set()
   languages.clear()
   print('Empty languages:', languages)
   
   #Output: Languages set: {'HTML', 'CSS', 'JavaScript', 'Python', 'Haskell', 'Java', 'C', 'C#'}
   #Output2: HTML deleted: {'CSS', 'JavaScript', 'Python', 'Haskell', 'Java', 'C', 'C#'}
   #Output3: CSS deleted: {'JavaScript', 'Python', 'Haskell', 'Java', 'C', 'C#'}
   #Output4: Randomly Removed value: JavaScript
   #Output5: Empty languages: set()
   ```
   ---
   ## Powering Up Sets: Set Operators
   ---
   - Union: Joining two sets
   - Intersection: Items that only exist in two sets
   - Difference: Items that only exist in the first set but not the second
   - Symmetric Difference: Items that exist in one set or the other but never in both
   - Proper Subset: One set is a proper subset of another if all members of the first subset can be found in the second without the first and the second being identical
   - Subset: A < B but A can also = B unlike a proper subset
   - Proper Superset: A and B aren't equal but all the values of B exist in A
   - Superset: A is a superset of B given A > B or A == B
   ## Disjoint: A Set Behavior Property
   ---
   - Two sets are disjointed when they have no value in common
      - A and B are both a set
      - A and B are both empty so they are disjointed
      - There is a method to check this in python called **isdisjoint()**
   ## Set Comprehension
   - Sets support comprehension
   ---
   # Dictionary in Python 3
   ## Defining a Dictionary in Python 3
   ---
   - Dictionaries are a data type that stores **key, value pairs** so that **each key is unique in the collection**
   - Common operations:
      - **Adding** a pair
      - **Removing** a pair
      - **Modify** an existing pair
      - **Lookup** of a value associated with a particular key
   - Dictionaries use **curly brackets** {} just like sets but their **item format is different**
   
   [*Dictionary Example*](https://mrparkonline.github.io/courses/datastruct/dictionary/)
   ```python3
   #Three items with a unique address and value
   sammy = {
    'username': 'sammy',
    'online': True,
    'followers': 42
   }

   #Accessing items
   print('Sammy dict:', sammy)
   print('Username:', sammy['username'])
   print('Online Status:', sammy['online'])
   print('Follower Count:', sammy['followers'])
   
   #output: Sammy dict: {'username': 'sammy', 'online': True, 'followers': 42} 
   #output2: Username: sammy 
   #output3: Online Status: True
   #output4: Follower Count: 42
   ```
   ---
   ## Dictionary Properties
   ---
   - Key value pair
   #### Keys
   - Keys are the unique address of a dictionary value's location
   #### Key properties
   - Have to be immutable (strings, numbers, tuples, etc.)
   - Cannot be duplicated, if there is a duplicate the newest item will superceed the old one
   ## Updating a Dictionary
   - Modify existing values using the key
   - Add new values by creating a key
   - Overwrite a value by modifying and recreating the value for it
   ## Deletion with Dictionary
   - Deleting a key deletes the value connected to it
   - Can empty an entire dictionary
   - Can delete an entire dictionary
   ## Membership
   - Can use **in** and **not in** operators to check a dictionary for specific keys
   ## Dictionary Methods
   - A.keys() is used to return a sequence of keys/addresses in A
   - A.values() is used to return a sequence of item values in A
   - A.items() is used to return a sequence of item and key pairs in A
   - A.get(address) is used to return an item value at a specified address
   - A.update(B) is used to extend dictionary A with the key value pairs of B
   ## Iterationg a Dictionary
   - Three iteration methods
     - Iterating keys
     - Iterating values
     - Iterating the pairs of the keys and values by unpacking
   ## dict() Constructor Dictionary Comprehension
   - Can turn other data types to dictionaries 
   - Dictionaries also support comprehension
   
   
  
    
   
   
   


   


 
   
    
  

