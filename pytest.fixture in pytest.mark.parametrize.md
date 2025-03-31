#pytest #python #unittest

```python
import pytest


@pytest.fixture
def input_a() -> int:
	return 1

@pytest.fixture
def input_b() -> int:
	return 2
```

## Problem
This will **NOT** work:

```python
@pytest.mark.parametrize(("input", "value"), [(input_a, 1), (input_a, 2)])
def test_inputs1(input: int, value: int) -> None:

    assert input == value
```

It will throw `assert <function input_a at 0x7fb5a3c52680> == 1`
The variable `input` is here a `function` not the expected `int`.

## Solution
This **WILL** work:

```python
@pytest.mark.parametrize(("input", "value"), [("input_a", 1), ("input_b", 2)])
def test_inputs(
    request: pytest.FixtureRequest,
    input: str,
    value: int,
) -> None:

    input = request.getfixturevalue(input)
    assert input == value
```
