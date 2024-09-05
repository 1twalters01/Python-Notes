* A tuple is a collection which is ordered an unchangeable.
* They are written with round brackets `()` or the `tuple()` constructor.
* They can have duplicates.
* A tuple can contain different data types and its elements can be of any type.

Tuple overview:
```python
tuple_1 = ("apple", "banana", "cherry")
tuple_2 = tuple(("apple", "banana", "cherry"))

print(tuple_1 == tuple_2) # True
print(len(tuple_1))
print(type(tuple_1)) # <class 'tuple'>
```

Access tuple items by referring to the index number inside square brackets:
```python
tuple_1 = ("apple", "banana", "cherry", "orange", "melon", "mango")
print(tuple_1[1])
print(tuple_1[-1])
print(tuple_1[2:5])

for fruit in tuple_1:
	print(fruit)
```

Convert tuples to a list using the `list()` function. This will then let you update them:
```python
fruit_tuple = ("apple", "banana", "cherry")
fruit_list = list(fruit_tuple)
fruit_list.append("orange")
fruit_tuple = tuple(fruit_list)
```

You can assign tuples values to variables. This is known as unpacking:
```python
fruit_tuple = ("apple", "banana", "cherry")
(green, yellow, red) = fruits
print(green)
```

If the number of variables is less than the number of values, you can add an `*` to the variable name and the values will be assigned to the variable as a list:
```python
fruits = ("apple", "banana", "cherry", "raspberry", "strawberry")
(green, yellow, *red) = fruits
print(red)
```

If the asterisk is added to a variable that isn’t the last one, Python will assign values to the variable until the umber of values left matches the number of variables left:
```python
fruit_tuple = ("apple", "banana", "pineapple", "mango", "cherry")
(green, *yellow, red) = fruits
print(green)
```

Join two or more tuples using the `+` operator
```python
tuple1 = ("a", "b", "c")
tuple2 = (1, 2, 3)

tuple3 = tuple1 + tuple2
print(tuple3) # ('a', 'b', 'c', 1, 2, 3)
```
