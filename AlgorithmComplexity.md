# Complexity Analysis
# Table of Contents
- [Order of Growth](#order-of-growth)
- [Sort Examples](#sort-examples)
## Order of Growth
|Notation| Growth Order | Form taken in Code | Example |
| :----- |--------------| :----------------- |:--------|
| O(n)  |linear| `for` loops| linear search|
|O(n²)| quadratic| nested loops| selection sort|
|O(log n)|logarithmic||binary search|
# Sort Examples
### Linear Sort
linear, looking at every element, one at a time, as one does in a `for` loop
### Selection Sort
quadratic, items are sleected and plaved in appropraite place one at a time, ascending as default
n2 comparisons, n exchanges
### Binary Search
logarithmic, requires sorted data, Gives O(log n) performance by eliminatng half the remaining items on each unsuccessful find attempt by adjusng the range of indices
- Uses the order of the array to extrapolate each comparison
- 
