* Use `range()` if you need to iterate over a sequence of numbers.
* Use `reversed()` to loop through the sequence in the opposite direction.
* Use `enumerate` to get both the index and the item.
* Use `else` to run code if the loop ran normally (didn’t encounter a `break` statement).
* Use `break` to exit a loop.
* Use `continue` to go to the next iteration.
* Use the `pass` statement if you need to have a list with no content.

A simple example:
```python
languages: list[str] = ["Rust", "Python", "Swift"]
for language in languages:
    print(f"language: {language}")
```

Using `range()`:
```python
for x in range(6):  
  print(x)
```

The syntax of range is `range(start, end, step)`:
```python
print(list(range(5)))               # [0, 1, 2, 3, 4]
print(list(range(5, 10)))           # [5, 6, 7, 8, 9]
print(list(range(0, 10, 3)))        # [0, 3, 6, 9]
print(list(range(-10, -100, -30)))  # [-10, -40, -70]
```

Using `reversed()`:
```python
for x in reversed(range(6)):
    print(x)
```

Using `enumerate()`:
```python
languages: list[str] = ["French", "English", "Spanish"]
for i, language in enumerate(languages):
    print(f"index: {i}, language: {language}")
```

Using `else`:
```python
def has_dog(pets: list[str]):
    for pet in pets:
        if pet == "cat": continue
        if pet == "dog": break
        print(pet)
    else:
        print("You don’t have a dog")
    print("")


has_dog(["cat", "parrot", "dog", "goldfish"])
has_dog(["cat", "parrot", "pig", "goldfish"])
```

Using `pass`:
```python
for pet in pets:
    pass
```
