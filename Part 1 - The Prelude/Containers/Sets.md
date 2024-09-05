* A set is an unordered collection with no duplicate elements.
* They are created using curly braces `{}` or the `set()` function.
* A set‘s items can be of any data type and the items can be different types.
* You cannot change a set’s items, but you can add and remove them.
* They support mathematical operations like union, intersection, difference, and symmetric difference.

Set overview:
```python
set_1 = {"apple", "banana", "cherry"}
set_2 = set(("apple", "banana", "cherry"))

print(set_1 == set_2) # True
print(len(set_1)) # 3
print(type(set_1)) # <class 'set'>
print("apple" in set_1) # True
print("grape" in set_1) # False
print("grape" not in set_1) # True

for fruit in set_1:
	print(fruit)
```

1 and True are considered to be the same value, as are False and 0:
```python
example_set = {"apple", "banana", "chery", True, 1, 2, 0, False}
print(example_set) # {0, True, 2, 'banana', 'apple', 'cherry'}
```

Use the `update()` method to add items from another set into the current set:
```python
example_set = {"apple", "banana"}
vegetable_set = {"broccoli", "carrot"}
fruit = ["cherry"]

example_set.update(vegetable_set)
print(example_set) # {'carrot', 'broccoli', 'apple', 'banana'}
example_set.update(fruit)
print(example_set) # {'broccoli', 'banana', 'apple', 'carrot', 'cherry'}
```

Use the `pop()` function to remove a random item from the set.
Use the `remove()` or the `discard()` function to remove an item in a set.
* `remove()` will raise an error if the item to remove does not exist.
* `discard()` will not raise an error if the item does not exist set.
Use the `clear()` function to empty the set.
Use the `del` keyword to delete the set completely.
```python
example_set = {"apple", "banana", "cherry", "grape", "strawberry"}
example_set.remove("apple")
print(example_set)
example_set.discard("cherry")
print(example_set)
fruit = example_set.pop()
print(example_set)
print(fruit)
example_set.clear()
del example_set
print(example_set)
```

# Joins
Use the `union()` method to return a new set with all items from both sets.
The `update()` method updates the set instead of creating a new one.
```python
set1 = {"a", "b", "c"}
set2 = {1, 2, 3}
set3 = ["x", "y", "z"]

set3 = set1.union(set2, set3)
print(set3)
```

Use the `intersection()` method to return a new set that only contains items present in both sets. 1 and True are seen as the same, as is 0 and False.
The `intersection_update()` method updates the set instead of creating a new one.
```python
set_1 = {"apple", "banana", "cherry"}
set_2 = {"apple", "google", "microsoft"}

set_3 = set_1.intersection(set_2)
print(set3)
```

Use the `difference()` method to return a new set that contains items from the first set that are not present in the second set. 1 and True are seen as the same, as is 0 and False.
The `difference_update()` method updates the set instead of creating a new one.
```python
set_1 = {"apple", "banana", "cherry"}
set_2 = {"apple", "google", "microsoft"}

set_3 = set_1.difference(set_2)
print(set3)
```

Use the `symmetric_difference()` method to keep only the elements that are not present in both sets. 1 and True are seen as the same, as is 0 and False.
The `symmetric_difference_update()` method updates the set instead of creating a new one.
```python
set_1 = {"apple", "banana", "cherry"}
set_2 = {"apple", "google", "microsoft"}

set_3 = set_1.symmetric_difference(set_2)
print(set3)
```
