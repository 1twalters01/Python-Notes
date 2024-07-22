* The `json` package is used to work with json data.
* You can convert dict, list, tuple, string, int, float, True, False and None into JSON strings.

Parse JSON strings by using the `json.loads()` method:
```python
import json

json_string = '{ "name":"John", "age":30, "city":"London"}'
data = json.loads(json_string)
print(data["age"])
```

Convert data to a JSON string by using the `json.dumps()` method:
```python
import json

data = {
	"name": "John",
	"age": 30,
	"city": "London"
}
json_string = json.dumps(data)
print(json_string)

formatted_json_string = dumps(data, index=4, separators=(". ", " = "), sort_keys=True)
```

Conversions between python objects and JSON objects are as follows:
| Python | JSON   |
| ------ | ------ |
| dict   | Object |
| list   | Array  |
| tuple  | Array  |
| str    | String |
| int    | Number |
| float  | Number |
| True   | true   |
| False  | false  |
| None   | null   |
