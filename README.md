Rock paper scissors game that runs in terminal. I tried to keep the code as compact as possible.

```python
(
    L := lambda: 
        (u := input("rock/paper/scissors: ").lower()[0]) and 
        (c := ("r", "p", "s")[id(object()) % 3]) and 
        print(f"Computer chose {c}") or 
        (
            (print("Draw! Retrying...") or L()) if u == c else 
            print(
                "You win!" if (u, c) in [
                    ("r", "s"), 
                    ("p", "r"), 
                    ("s", "p")
                ] else "You lose!"
            )
        )
)()
```

Importing `random` cost us a line, so we use the trick `id(object())` to simulate a random number 
generator. `object()` creates an empty object and `id()` returns the object's unique memory ID. 
Note that `id(object())` does not really change during runtime.