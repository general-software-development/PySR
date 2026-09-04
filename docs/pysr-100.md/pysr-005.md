# PySR 0005: Use built-in functions

## Abstract

Use built-in functions unless there is a good reason to reimplement them.

The python built-in functions, such as `map()`, `filter()`, etc. are implemented in C, and as such are faster than Python-based implementations.

There is also no point in wasting time reimplementing a built-in function just to not change anything, unless you explicitly do it just to learn and understand how built-in functions work.

## Examples

<div bad markdown>

```python
# Bad:
def my_map(fn, data: list) -> list:
    new_data = []
    
    for item in data:
        new_data.append(fn(item))

    return new_data

old = [1, 2, 3]
out = my_map(lambda x: x + 1, old)
```
</div>

<div good markdown>

```python
# Good:
old = [1, 2, 3]
out = list(
    map(lambda x: x + 1, old)
)
```
</div>
