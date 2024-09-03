# ConfigParser - Python
## items
### class
・ConfigParser
  ### Functions
    ・__init__()<br>
    ・load_config(self, file_path: str, encoding: str = 'utf-8')
    ・add_config(self, key: str, value) -> None
    ・delete_config(self, key: str) -> None
    ・get(self, key: str, default=None)
    ・save_config(self, file_path: str, encoding: str = 'utf-8') -> None
    ・display_config(self)
  ### Variable
    ・self.word -> Don't please edit.
    ・self.config -> Don't please edit.

## How to use ?
### For example
Directory
```
Root Directory
| config.py
| main.py
| temp.config
```
#### temp.config
```config
hello = world!
good-by = world
```
#### main.py
```python main.py
from config import ConfigParser

config = ConfigParser()
config.load_config(file_path="temp.config")
print("Hello {}".format(config.get('hello')))
print("Good-by {}".format(config.get('good-by')))
```
##### ___↓ console___
```text
Hello world!
Good-by world
```
