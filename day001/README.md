Task was to recreate https://appbrewery.github.io/python-day1-demo/. I tried to keep the code as 
compact as possible.

```python
print(
    "Your band name could be:", 
    *[input(q) for q in [
        print("Welcome to the Band Name Generator.") or "What's the name of the city you grew up in?\n", 
        "What's your pet's name?\n"
    ]]
)
```

Note that Python automatically inserts a space between the arguments separated by commas. By 
unpacking a list comprehension, we pass the inputs directly into `print()`. We use `or` to print 
the welcome message immediately since `print()` returns `None` and thus is always evaluated as 
`False`.
