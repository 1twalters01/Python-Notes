* Use `break` to exit a loop
* Use `continue` to go to the next iteration
* Use `else` to run code if the loop ran normally (didn’t encounter a `break` statement)
* Use the `pass` statement if you need to have a list with no content

A simple example:
```python
i: int = 0
while i < 5:
    print(i)
```
An example showcasing `else`:
```python
def break_if(value):
    i: int = 0
    while i < 10:
        if i == value: break
        i += 2
    else:
        print(f"Loop complete")
    print()

break_if(5)
break_if(6)
```

A `continue` example:
```python
# print odd numbers
i: int = 0
while i < 10:
    i += 1
    if (i % 2) == 0:
        continue
    print(i)
```

An example using `pass`:
```python
while True:
    pass
```
