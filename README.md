### Mark Filter


Most pytest marks accept additional keywords arguments. This plugin will check for the __match__ and __not_match__ keywords. Any test that has the string in its name will be filtered accordingly. You can use both at the same time too.

#### Match

```python
import pytest

pytestmark = [
    pytest.mark.skipif(match="skip")
]

def test_normal():
    pass

def test_skip():
    pass

def test_other():
    pass
```

Any test that has "skip" in the name will get the mark. In this case, test_skip.

#### Not Match

```python
import pytest

pytestmark = [
    pytest.mark.skipif(not_match="skip")
]

def test_normal():
    pass

def test_skip():
    pass

def test_other():
    pass
```

Any test that doesn't have "skip" in the name will get the mark. In this case, test_normal and test_other.

### Installing

```
pip install pytest-mark-filter
```
