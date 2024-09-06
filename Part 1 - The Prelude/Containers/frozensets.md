* A frozenset is an immutable, unordered collection with no duplicate elements.
* They are created using the `frozenset()` function.
* A frozenset‘s items can be of any data type and the items can be different types.
* They support mathematical operations like union, intersection, difference, and symmetric difference.

Set overview:
```python
frozenset_1 = frozenset(("apple", "banana", "cherry"))

print(len(frozenset_1)) # 3
print(type(frozenset_1)) # <class 'frozenset'>
print("apple" in frozenset_1) # True
print("grape" in frozenset_1) # False
print("grape" not in frozenset_1) # True

for fruit in frozenset_1:
	print(fruit)
```

1 and True are considered to be the same value, as are False and 0:
```python
frozenset_1 = frozenset(("apple", "banana", "chery", True, 1, 2, 0, False))
print(frozenset_1) # {0, True, 2, 'banana', 'apple', 'cherry'}
```

# Joins
Use the `union()` method to return a new set with all items from both sets.
```python
frozenset_1 = frozenset(("a", "b", "c"))
frozenset_2 = frozenset((1, 2, 3))
frozenset_3 = frozenset(("x", "y", "z"))

frozenset_3 = frozenset_1.union(frozenset_2, frozenset_3)
print(frozenset_3)
```

Use the `intersection()` method to return a new set that only contains items present in both frozensets. 1 and True are seen as the same, as is 0 and False.
```python
frozenset_1 = {"apple", "banana", "cherry"}
frozenset_2 = {"apple", "google", "microsoft"}

frozenset_3 = frozenset_1.intersection(frozenset_2)
print(frozenset_3)
```

Use the `difference()` method to return a new set that contains items from the first set that are not present in the second set. 1 and True are seen as the same, as is 0 and False.
```python
frozenset_1 = {"apple", "banana", "cherry"}
frozenset_2 = {"apple", "google", "microsoft"}

frozenset_3 = frozenset_1.difference(frozenset_2)
print(frozenset_3)
```

Use the `symmetric_difference()` method to keep only the elements that are not present in both sets. 1 and True are seen as the same, as is 0 and False.
```python
frozenset_1 = {"apple", "banana", "cherry"}
frozenset_2 = {"apple", "google", "microsoft"}

frozenset_3 = frozenset_1.symmetric_difference(frozenset_2)
print(frozenset_3)
```
