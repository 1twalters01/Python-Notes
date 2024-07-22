* There can be zero or more `elif` parts
* The `else` part is optional.
* If you are comparing the same value to several constants, or checking for specific types or attributes, consider using [`match`](The%20`match`%20statement.md).

The `if` statement is as follows:
```python
x: int = int(input("Please enter an integer: "))
if x < 0:
    print("Negative")
elif x == 0:
    print("Zero")
else:
    print("Positive")

# More code
```

Do a ternary operator as follows:
```python
profit: int = 53
bonus: str = "Bonus" if profit > 50 else "No bonus"
print(bonus)
```
