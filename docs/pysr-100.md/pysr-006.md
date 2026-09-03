# PySR-0006, "Type Annotations"

## Abstract

Always write type annotations for your functions, even if not variables. This not only allows static type checkers (ex. `mypy`) and runtime type checkers (ex. `typegaurd`) to verify the types passed to your functions, but it also provides future you, and other readers with insight as to what the function expects.

## Deprecated typing types

Certain types from within `typing` are deprecated and have been moved into `collections` or other libraries. Some examples include:

* `typing.Iterable` -> `collections.abc.Iterable`
* `typing.Iterator` -> `collections.abc.Iterator`
* `typing.Callable` -> `collections.abc.Callable`
* `typing.Generator` -> `collections.abc.Generator`
* `typing.Hashable` -> `collections.abc.Hashable`
* `typing.Deque` -> `collections.Deque`
* `typing.OrderedDict` -> `collections.OrderedDict`
* `typing.Type` -> `builtins.type`
* `typing.Tuple` -> `builtins.tuple`

Prefer using the new versions over the deprecated `typing.*` aliases for these specific deprecated types.

## Related
Also see:

* [`typing` documentation](https://docs.python.org/3/library/typing.html#typing.Iterable)
