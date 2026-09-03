# PySR-0003, "Method Chaining"

Prefer using method chaining where appropriate on member functions that would otherwise return nothing.

Example:
```python
from typing import Self

class Number:
    def __init__(self, value: int = 0) -> None:
        self.value = value

    def add(self, value: int) -> Self:
        self.value += value
        return self

    def __repr__(self) -> str:
        return f"Number({self.value})"

n = Number(2)
n.add(1).add(3)

print(n)    # Number(6)
```

This result to cleaner codebases overall. Another common real-world example of method chaining is found in **numpy ndarray's**:
```python
import numpy as np

data = np.zeros((20, 30))
data = data.transpose(0, 1).flatten().mean()
```
