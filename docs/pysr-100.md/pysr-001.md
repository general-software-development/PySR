# PySR-0001, "Code of Conduct"

## 1. Submitting or suggesting AI-generated code

Any AI-generated code is to be clearly marked as such via in-code comments, and externally if submitted as a PR, within the body of a GitHub Issue, or via a bug tracker.

Example:

<div good markdown>

```python
# AI-generated
def func():
    ...
```
</div>
<div bad markdown>

```python
def func():
    """
    This function is AI-generated.
    """

    ...
```
</div>
<div bad markdown>

```python
def func():
    ...
```
</div>


## 2. Constructive Criticism

Point out flaws in other people's code and PR's, even if minor. One can't improve their code past a certain point without feedback.

This applies both ways. You should also accept constructive criticism without getting argumentative/defensive. The point is to improve, not to attack your ability to write code/
