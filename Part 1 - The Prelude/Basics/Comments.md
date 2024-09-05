* Use the octothorpe (`#`) to write a comment.
* Python does not have multi-line comments. Instead you have to either:
	* Use a multi-line string that isn’t assigned to a variable.
	* Have octothorpes on each line.
* A Docstring is a multiline string that is directly underneath a class, module, function, or method definition.
	* They are accessible from the doc attribute `(__doc__)` or the `help()` function.
	* Use ReST style for Docstrings

Octothorpe example:
```python
# A comment
# Another comment
print("Some Text") # A third comment
```

Multi-line string:
```python
"""
An example of a
multiline string
"""
```

Docstring:
```python
class Vehicle(object):
   """
   The Vehicle object contains ...
   :param arg: The arg is used for ...
   :type arg: str
   :param `*args`: The variable arguments are used for ...
   :param `**kwargs`: The keyword arguments are used for ...
   :ivar arg: This is where we store arg
   :vartype arg: str
   """
   
   def __init__(self, arg, *args, **kwargs):
       self.arg = arg def cars(self, distance, destination):
       """We can't travel a certain distance in vehicles
       without fuels, so here's the fuels
       
       :param distance: The amount of distance traveled
       :type amount: int
       :param bool destinationReached: Should the fuels be refilled?
       
       :raises: :class:`RuntimeError`: Out of fuel
       
       :returns: A Car mileage
       :rtype: Cars
       """
       pass
```
