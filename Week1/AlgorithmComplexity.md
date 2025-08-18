# Complexity Analysis
# Table of Contents
- [Order of Growth](#order-of-growth)
- [Sort Examples](#sort-examples)
- [Big O Notation](#big-o-notation)
- [Reasoning for Use of n](#reasoning-for-use-of-n)
## Order of Growth
|Notation| Growth Order | Form taken in Code | Example |
| :----- |--------------| :----------------- |:--------|
| O(n)  |linear| `for` loops| linear search|
|O(n²)| quadratic| nested loops| selection sort|
|O(log n)|logarithmic||binary search|
## Sort Examples
### Linear Sort
linear, looking at every element, one at a time, as one does in a `for` loop
### Selection Sort
quadratic, items are sleected and plaved in appropraite place one at a time, ascending as default
n2 comparisons, n exchanges
### Binary Search
logarithmic, requires sorted data, Gives O(log n) performance by eliminatng half the remaining items on each unsuccessful find attempt by adjusng the range of indices
- Uses the order of the array to extrapolate each comparison

To determine the speed of the binary search algorithm, we ask:
>"How many times can you divide a collection of n elements in half?"

| | |
| :- | :- |
| exponential | The function you get by repeated multiplication. Typically powers of two: 1, 2, 4, 8, 16, 32, 64, 128, 256, 512, etc. |



## Big O Notation
used to characteize a fxn `f(x)` in terms of its growth rate `g(x)`. Specifically, used to indicated an upper bound on `f(x)`.
![Big O](https://github.com/user-attachments/assets/571695e0-271a-4d9a-875d-69827067c9da)
## Reasoning for Use of `n`
>"What is important is that the total amount of work
you will perform is proportional to n. That is to say, if you were to search a list of 2000
words it would take twice as long as it would to search a list of 1000 words. Now
suppose the search is successful; that is, the word is found on the list. We have no idea
where it might be found, so on average we would expect to search half the list. So the
expectation is still that you will have to perform about n/2 comparisons. Again, this value
is proportional to the length of the list – if you double the length of the list, you would
expect to do twice as much work. "
