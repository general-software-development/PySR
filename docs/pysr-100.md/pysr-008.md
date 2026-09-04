# PySR 0008: Line Length

## Abstract

You should avoid overly-long lines, as they make the code harder to read and understand, especially on small screens.

## Line Lengths

All lines should be limited to a maximum of 100 characters.

Docstrings and comments should be limited to 70 characters, where appropriate.

Code snippets in public documentation should preferably be kept to 70-90 characters at most.

## Splitting Lines

### Function call splitting

When splitting a function, place the function name and opening parantheses on the first line, the arguments on the following lines &mdash; one per line &mdash; indented by another level, with the closing parantheses placed on the last line, after all arguments, indented as much as the line from which the function call started.

While not recommended, one or more arguments can be placed on the same line as the opening parantheses, after the opening parantheses, with no extra space between.

<div good markdown>

```python
# Do:
order = order(
    "John Doe",
    age = 21,
    email = "john-doe@example.com",
    location = "New York City, New York, US"
)
```
</div>

<div maybe markdown>

```python
# Prefer not to:
order = order("John Doe", age = 21,
    email = "john-doe@example.com",
    location = "New York City, ew York, US"
)
```
</div>

<div bad markdown>

```python
# Don't:
order = order("John Doe", age = 21, email = "john-doe@example.com", location = "New York City, New York, US")
```
</div>

<div bad markdown>

```python
# Don't:
order = order(
    "John Doe",
    age = 21,
    email = "john-doe@example.com",
    location = "New York City, ew York, US")
```
</div>

### Arithmetic splitting

When splitting arithmetic, either:

1. Split the line, placing a backslash (`\`) at the end of the first line, and start the second line with the arithmetic operator
2. Wrap the entire arithmetic expression in parantheses (`()`), with new lines after the opening parantheses and before the closing parantheses, and with all inner lines indented by another level, and start the second line with the arithmetic operator

The arithmetic operator at the start of the next line should be indented as much as the first item of the arithmetic expression.

<div good markdown>

```python
# Do:
result = 3 + 4 \
         + 2 \
         + 4 \
         - 6 \
         // 2
```
</div>

<div good markdown>

```python
# Do:
result = (
    3 + 4
    + 2
    + 4
    - 6
    // 2
)
```
</div>

<div bad markdown>

```python
# Don't:
result = 3 + 4 \
    + 2 \
         + 4 \
         - 6 \
         // 2
```
</div>

<div bad markdown>

```python
# Don't:
result = 3 + 4 + 2 + 4 - 6 // 2 * 24 + int(input("> "))
```
</div>

### Comment splitting

If a comment needs to be split across multiple lines, move the comment onto its own line (if not already on its own line), and create a new comment on the following line for the rest of the text. Repeat this as needed. Make sure that, before all the comments, there is a new line, if there is any code before them.

Split multi-line comments like these up into blocks/paragraphs, separated by empty comments in between, when they get too long.

<div good markdown>

```python
# For an example, you could split comments like this.
#
# This way, you avoid making comments too long, and ensure
# that they remain readable on small screens.
```
</div>

<div bad markdown>

```python
# Meanwhile, you shouldn't have comments like these. They are hard to read on small or narrow monitors, and are also generally harder to read at a glance while scrolling through code.
```
</div>

<div bad markdown>

```python
# Additionally, you shouldn't
# split your comments into
# such short lines,
# since they can make it more
# difficult to traverse your code.
#
# Additionally, comments spanning
# too many lines are also more
# difficult to read due to the excessive
# amount of line breaks
```
</div>
