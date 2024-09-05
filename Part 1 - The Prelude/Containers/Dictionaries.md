* Dictionaries are ordered, changeable, and do not allow duplicates.
* They are written with curly brackets `{}` or the `dict()` function, and have keys and values.

Dictionary overview:
```python
dict_1 = {
	"brand": "Ford",
	"electric": False,
	"year": 1964,
	"colours": ["red", "white", "blue"]
}

dict_2 = dict(
	brand = "Ford",
	electric = False,
	year = 1964,
	colours = ["red", "white", "blue"]
)

print(dict_1 == dict_2) # True
print(len(dict_1)) # 3
print(type(dict_1)) # <class 'dict'>
print("brand" in set_1) # True
```

Use either square bracket notation or the `get()` method to access the items of a dictionary:
```python
dict_1 = {
	"brand": "Ford",
	"electric": False,
	"year": 1964,
	"colours": ["red", "white", "blue"]
}
brand_1 = dict_1["brand"]
brand_2 = dict_1.get("brand")
```

The `keys()` method will return a list of all the keys in the dictionary.
The `values()` method will return a list of all the values in the dictionary.
The `items()` method will return each item in a dictionary as tuples in a list.
You can then loop through these as normal:
```python
dict_1 = {
	"brand": "Ford",
	"electric": False,
	"year": 1964,
	"colours": ["red", "white", "blue"]
}
brand_keys = dict_1.keys()
brand_values = dict_1.values()
brand_items = dict_1.items()

for key, value in dict_1.items():
	print(f"Key: {key}, Value: {value}")
```

You can change the value of a specific item by referring to its key name or by using the `update` function:
```python
dict_1 = {
	"brand": "Ford",
	"electric": False,
	"year": 1964,
	"colours": ["red", "white", "blue"]
}
dict_1["year"] = 2008
print(dict_1["year"])
dict_1.update({"year": 1964})
print(dict_1["year"])
```

Use the `pop()` method to remove an item with the specified key name:
```python
dict_1 = {
	"brand": "Ford",
	"electric": False,
	"year": 1964,
	"colours": ["red", "white", "blue"]
}
dict_1.pop("year")
print(dict_1)
```

Use the `popitem()` method to remove the last inserted item:
```python
dict_1 = {
	"brand": "Ford",
	"electric": False,
	"year": 1964,
	"colours": ["red", "white", "blue"]
}
dict_1.popitem()
print(dict_1)
```

The `clear()` method empties the dictionary:
```python
dict_1 = {
	"brand": "Ford",
	"electric": False,
	"year": 1964,
	"colours": ["red", "white", "blue"]
}
dict_1.clear()
print(dict_1)
```

You cannot copy a dictionary by typing `dict1 = dict2`, because `dict2` will only be a reference to `dict1`. Use the `copy()` method instead:
```python
dict_1 = {
	"brand": "Ford",
	"electric": False,
	"year": 1964,
	"colours": ["red", "white", "blue"]
}
dict_2 = dict_1.copy()
