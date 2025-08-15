# Data_Structures_Practice

## Notes from Python Review
Strings are immutable, once created they cannot be transformed, can be copied or altered into new variables.
Strings are objects. String methods alwauys return new obejcts.
### The `in` operator
Using in with two strings gives a boolean result based on whether (or not) the first operand is a substring of the second
### List methods
```python 
append() #add element to the end of list
t.append("d")
extend() #append list to end of other list
t1.extend(t2)
sort() 3 arrange from high to low
t.sort()
pop() # deleted item at index, then returns it
del() #remove item from list via idex
remove() #remove item from list, without index
sum() sums values in provided list
map
filter
reduce
```
### var args
variable-length arguments, meaning that a function can accept varying nuber of arguments. Use the sytax *arg for 
the arguments are collected into a tuple within the func
#### *arg

```python
    def sum_all(*numbers):
        total = 0
        for num in numbers:
            total += num
        return total

    print(sum_all(1, 2, 3))       # Output: 6
    print(sum_all(10, 20, 30, 40)) # Output: 100
```
#### *kwarg
allows function to accept multple keyword args. Arges are collected into dictionary.
```python
    def display_info(**details):
        for key, value in details.items():
            print(f"{key}: {value}")

    display_info(name="Alice", age=30, city="New York")
    # Output:
    # name: Alice
    # age: 30
    # city: New York
```
### zip()
combine multiple iterables into tuples
```python
names = ["Alice", "Bob", "Charlie"]
scores = [85, 90, 95]

zipped = zip(names, scores)
print(list(zipped))  
# → [('Alice', 85), ('Bob', 90), ('Charlie', 95)]
```
### enumerate()
add an index to  iterable
```python
fruits = ["apple", "banana", "cherry"]

for i, fruit in enumerate(fruits, start=1):
    print(i, fruit)
# 1 apple
# 2 banana
# 3 cherry
```
### items (method)
view object of key and value from dictionary
```py
person = {"name": "Alice", "age": 30}

for key, value in person.items():
    print(key, value)
# name Alice
# age 30
```
