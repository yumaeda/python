# Python Coding Standard

## Import Module

### 1. Import module under the specific namespace.

```python
import datetime

class Test:
    def __init__(self):
        self.__now = datetime.datetime.now()
```

### 2. Divide import statements.
- Divide the import statements and arrange them as below.

```python
# Standard Library
import time
import datetime

# 3rd Party Library
import requests

# Custom Library
import jf_mailgun
import jf_slack
```

&nbsp;

## Class Variable Name

### 1. Protected Variable
- Prefix the variable name with '_'.

```python
class Test:
    def __init__(self):
        self._var1 = 'var1'
        self._var2 = 'var2'
    ...
```

### 2. Private Variable
- Prefix the variable name with '__'.

```python
class Test:
    def __init__(self):
        self.__var1 = 'var1'
        self.__var2 = 'var2'
    ...
```

&nbsp;

## Class Constant Name

- Use snake case with upper case letters.

```python
class Test:
    CONSTANT1 = 'constant1'
    CONSTANT2 = 'constant2'

    def __init__(self):
    ...
```

&nbsp;

## Type Hint

- Use type hints, so that IDEs or linters can take advantage of it.

```python
def prepend_hello(text: str) -> str:
    """
    Prepend 'Hello' to the specified text.
    """
    return 'Hello {}'.format(text)
```

&nbsp;

# References
- [PEP8](https://www.python.org/dev/peps/pep-0008/)
- [PEP20](https://www.python.org/dev/peps/pep-0020/)
- [PEP257](https://www.python.org/dev/peps/pep-0257/)
