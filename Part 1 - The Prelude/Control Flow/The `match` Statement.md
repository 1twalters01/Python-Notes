* This is non-exhaustive matching.
	* If no case matches then none of the branches are executed.
	* Use a wildcard (`_`) to have a failsafe.
* It is similar to pattern matching in languages like Rust or Haskell:
	* Only the first pattern that matches gets executed.
	* Sequence elements or object attributes can be extracted from the value into variables.
	* You can use `if` on a case to add more specificity.

A simple example:
```python
def http_client_errors(status: int) -> str:
    match status:
        case 400:
            return "Bad request"
        case 404:
            return "Not found"
        case 401 | 402| 403:
            return "Not allowed"
        case _:
            return "Other error"

print(http_client_errors(400))
print(http_client_errors(402))
```

Unpacking assignments:
```python
def where_is(point: tuple[int, int]):
    match point:
        case(0, 0):
            print("Origin")
        case(x, 0):
            print(f"X={x}")
        case(0, y):
            print(f"Y={y}")
        case(x, y) if x > 0 and y > 0:
            print("First quadrant: X={x}, Y={y}")
        case(x, y):
            print("Other")
        case _:
            raise ValueError("Not a point")


point_1, point_2, point_3 = (5, 4), (5, -4), (5)
where_is(point_1)
where_is(point_2)
where_is(point_3)
```

Capturing object attributes:
```python
class Point:
  def __init__(self, x: int, y: int):
      self.x = x
      self.y = y

def where_is(point: Point):
    match point:
      case Point(x=0, y=0):
          print("Origin")
      case Point(x=x, y=y) if x > 0 and y > 0:
          print(f"First quadrant: ({x}, {y})")
      case Point():
          print("Other")
      case _:
          print("Not a point")

point_1, point_2, point_3 = Point(1, 1), Point(0, 0), Point(1, 0)
where_is(point_1)
where_is(point_2)
where_is(point_3)
```

Using an enum:
```python
from enum import Enum
class Colour(Enum):
    RED = "red"
    YELLOW = "yellow"
    BLUE = "blue"

colour: Colour = Colour(input("red, blue or yellow: "))

match colour:
    case Colour.RED:
        print(f"Colour is: {Colour.RED.name}")
    case Colour.YELLOW:
        print(f"Colour is: {Colour.YELLOW.name}")
    case Colour.BLUE:
        print(f"Colour is: {Colour.BLUE.name}")
```
