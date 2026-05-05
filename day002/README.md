Task was to recreate https://appbrewery.github.io/python-day2-demo/. Tried to make it compact.

```python
print(
    (lambda b, t, p: 
        f"Each person should pay: €{float(b) * (1 + float(t) / 100) / float(p):.2f}" 
        if all(x.replace('.', '', 1).isdigit() for x in [b, t, p]) 
        else "Invalid input!"
    )(
        input("Welcome to the tip calculator!\nWhat was the total bill? €"), 
        input("How much would you like to give? 10, 12 or 15? "), 
        input("How many people to split the bill? ")
    )
)
```

Use `:.2f` in fstrings to round float into the nearest two decimal point.