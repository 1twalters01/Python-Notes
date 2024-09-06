* A list is a collection that is ordered, changeable, and allows duplicate values.
* They are written with square brackets `[]` or the `list()` constructor.
* A list can contain different data types and its elements can be of any type.

List overview:
```python
list_1 = ["apple", 7, "cherry"]
list_2 = list(("apple", 7, "cherry"))

print(list_1 == list_2) # True
print(len(list_1))
print(type(list_1)) # <class 'list'>

if "apple" in list_1:
    print(true)
```

Access list items by referring to the index number inside square brackets:
```python
fruit_list = ["apple", "banana", "cherry", "orange", "melon", "mango"]
print(fruit_list[1])
print(fruit_list[-1])
print(fruit_list[2:5])

fruit_list[1] = "grapefruit"
fruit_list[2:4] = ["watermelon", "blackcurrant"]
```

They are reference types by default - typing `list2 = list1` makes `list2` a reference to `list1`. Changes made in `list1` will also be made in `list2`. Use the `copy()` method to copy:
```Python
list1 = ["apple", "banana", "cherry"]
list2 = list_1.copy()

# Alternatively, you can use the list function:
list3 = list(list1)

# You can also make a copy of a list by using the `:` (slice) operator:
list4 = list1[:]
```

Update lists as so:
```python
fruit_list = ["apple", "banana", "cherry"]
print(fruit_list)
fruit_list.append("orange") # Append to the end of the list
fruit_list.insert(1, "grapefruit") # Insert at position chosen
print(fruit_list)
fruit_list.remove("banana")
print(fruit_list)
fruit_list.pop(0) # Remove an item at a specific index
print(fruit_list)
fruit_list.pop() # Remove the last item
print(fruit_list)

tropical_list = ["mango", "pineapple", "papaya"]
vegetable_tuple = ("spinach", "kale")
fruit_list = fruit_list + tropical_list
fruit_list.extend(tropical_list)
fruit_list.extend(vegetable_tuple)
print(fruit_list)

fruit_list.clear() # empty the list
print(fruit_list)
del fruit_list # delete the list completely
```

Loop lists as so:
```python
fruit_list = ["apple", "banana", "cherry"]

# list comprehension
# newlist = [expression for item in iterable if condition else expression]
[print(fruit) for fruit in fruit_list]

for fruit in fruit_list:
	print(fruit)
	
for index in range(len(fruit_list)):
    print(fruit_list[index])

for index, fruit in enumerate(fruit_list):
    print(index, fruit)
```

