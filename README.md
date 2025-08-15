# Python Review

## Table of Contents
- [Strings](#strings)
- [The `in` Operator](#the-in-operator)
- [List Methods](#list-methods)
  - [append()](#append)
  - [extend()](#extend)
  - [sort()](#sort)
  - [pop()](#pop)
  - [del](#del)
  - [remove()](#remove)
  - [sum()](#sum)
- [Arguments](#arguments)
  - [Default Arguments](#default-arguments)
  - [Variable-Length Arguments](#variable-length-arguments)
    - [*args](#args)
    - [**kwargs](#kwargs)
- [Built-in Functions](#built-in-functions)
  - [zip()](#zip)
  - [enumerate()](#enumerate)
  - [items() Method](#items-method)

---

## Strings
Strings are immutable — once created, they cannot be changed in place.  
They can be copied or altered into **new variables**.  
Strings are objects, and **string methods always return new objects**.  
[](#```python-review)

---

## The `in` Operator
Using `in` with two strings gives a boolean result based on whether the first operand is a substring of the second.  
[](#```python-review)

---

## List Methods

### append()
**Example:**
```python
t = ["a", "b", "c"]
t.append("d")
print(t)  # ['a', 'b', 'c', 'd']
```
Explanation:
Adds an element to the end of the list.


extend()
Example:
```python


t1 = [1, 2]
t2 = [3, 4]
t1.extend(t2)
print(t1)  # [1, 2, 3, 4]
```
Explanation:
Appends all elements of another iterable to the list.


sort()
Example:

```python


t = [3, 1, 2]
t.sort()
print(t)  # [1, 2, 3]
```
Explanation:
Sorts the list in place. By default, ascending order.


pop()
Example:

```python


t = [1, 2, 3]
x = t.pop(1)
print(x)  # 2
print(t)  # [1, 3]
```
Explanation:
Removes and returns the element at the given index.
If no index is given, removes and returns the last item.


del
Example:

```python


t = [1, 2, 3]
del t[1]
print(t)  # [1, 3]
```
Explanation:
Deletes an element at a specific index without returning it.


remove()
Example:

```python


t = [1, 2, 3]
t.remove(2)
print(t)  # [1, 3]
```
Explanation:
Removes the first occurrence of a value from the list.


sum()
Example:

```python
nums = [1, 2, 3]
print(sum(nums))  # 6
```
Explanation:
Returns the sum of all elements in the iterable.


## Arguments
#### Default Arguments
Default arguments are defined in the function signature and used if the caller does not provide a value.

Example:

```python


def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()            # Hello, Guest!
greet("Archie")    # Hello, Archie!
```
Important:
Default arguments are created once, when the function is defined — not each time it’s called.
Using mutable objects (list, dict, set) as defaults will reuse the same object.

Bad Example:

```python


def some_func(my_list=[]):
    my_list.append(1)
    return my_list

print(some_func())  # [1]
print(some_func())  # [1, 1]
```
Good Example:

```python


def some_func(my_list=None):
    if my_list is None:
        my_list = []
    my_list.append(1)
    return my_list
```
✅ Rule:

Mutable: list, dict, set → Don’t use as defaults.

Immutable: int, float, bool, str, tuple → Safe to use.


### Variable-Length Arguments
*args
Collects extra positional arguments into a tuple.

```python
def sum_all(*numbers):
    total = 0
    for num in numbers:
        total += num
    return total

print(sum_all(1, 2, 3))       # 6
print(sum_all(10, 20, 30, 40)) # 100
```


**kwargs
Collects extra keyword arguments into a dictionary.

```python


def display_info(**details):
    for key, value in details.items():
        print(f"{key}: {value}")

display_info(name="Alice", age=30, city="New York")
# name: Alice
# age: 30
# city: New York
```


Built-in Functions
zip()
Example:

```python


names = ["Alice", "Bob", "Charlie"]
scores = [85, 90, 95]

zipped = zip(names, scores)
print(list(zipped))
# [('Alice', 85), ('Bob', 90), ('Charlie', 95)]
```
Explanation:
Combines multiple iterables into tuples, stopping at the shortest iterable.


enumerate()
Example:

```python


fruits = ["apple", "banana", "cherry"]

for i, fruit in enumerate(fruits, start=1):
    print(i, fruit)
# 1 apple
# 2 banana
# 3 cherry
```
Explanation:
Adds an index to each element in an iterable.


items() Method
Example:

```python


person = {"name": "Alice", "age": 30}

for key, value in person.items():
    print(key, value)
# name Alice
# age 30
```
Explanation:
Returns a view object of dictionary key-value pairs.
