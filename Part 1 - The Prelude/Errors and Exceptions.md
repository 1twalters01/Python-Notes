
	* They are always fatal.
* Errors detected during execution are called exceptions.
	* They are not unconditionally fatal.
	* They come in different types, such as NameError and TypeError.

The `try` statement works as follows:
* First execute the try the clause
* If no exception occurs, the except clause is skipped and execution of the try statement is finished.
* If an exception occurs during execution of the try clause then the rest of it is skipped.
* If its type matches the exception named after the except keyword, the except clause is executed, and then execution continues after the try/except block.
* If an exception occurs which does not match the exception named in any of the except clauses, it is passed on to outer try statements.
* If no handler is found it is an unhandled exception and execution stops with an error message.
* There is an optional else clause which must come after all except clauses. It is executed if the try clause does not raise an exception.

An example:
```python
import sys

try:
	f = open("myfile.txt")
	s = f.readline()
	i = = int(s.strip())
except OSError as err:
	print("OS error:", err)
except ValueError:
	print("Could not convert data to an integer.")
except Exception as err:
	print(f"Unexpected {err=}, {type(err)=}")
else:
	f.close()
```

Use the `raise` statement to force a specified exception to occur:
```python
raise NameError("Test name error")
```

If an unhandled exception occurs inside an `except` section, it will have the exception being handled attached to it and included in the error message. To indicate that an execption is a direct consequence of another, the `raise` statement allows an optional `from` clause:
```python
def func():
	raise ConnectionError
try:
	func()
except ConnectionError as c_err
	raise RuntimeError("Failed to open database") from c_err
```

You can disable the automatic exception chaining by using `from None`:
```python
def func():
	raise ConnectionError
try:
	func()
except ConnectionError as c_err
	raise RuntimeError("Failed to open database") from 
```

Use the finally clause to execute code whether or not there was an exception:
```python
try:
	raise KeyboardInterrupt
finally:
	print("Goodbye")
```

Create your own errors by creating a class by deriving from the Exception class either directly or indirectly:
```python
class MyError(Exception):
	pass

class MyKeyboardInterrupt(KeyboardInterrupt):
	pass
```

Some objects, such as the `open()` method have standard clean-up actions to be done whether the operation succeeded or failed. Use the `with` statement to clean up correctly:
```python
with open("myfile.txt") as f:
	for line in f:
		print(line, end="")
```

Use `ExeptionGroup` to raise a group of exceptions together:
```python
def f():
	excs = [OSError("error 1"), SystemError("Error 2")]
	raise ExceptionGroup("There were problems", execs)

try:
	f()
except Eception as e:
	print(f"Caught {type(e)}: e")
```

You can add additional information to an exception with the `add_note` method:
```python
try:
	raise TypeError("bad type")
except Exception as e:
	e.add_note("Add some information")
	e.add_note("Add some more information")
	raise
```
