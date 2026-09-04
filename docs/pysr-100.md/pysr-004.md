# PySR 0004: Deprecated functions

## Abstract

If you are working on a library, you should mark a function as deprecated before removing it.

Do so using the `warnings.deprecated` decorator.

## Examples

```python
from warnings import deprecated

@deprecated("Use new_foo instead")
def foo() -> None:
    ...

def new_foo() -> int:
    ...

@deprecated()
def do_foo_and_print() -> None:
    print(new_foo())
```

## Related

Also see:

* [PEP 0702](https://peps.python.org/pep-0702/)
* [Deprecated library](https://pypi.org/project/Deprecated/)
