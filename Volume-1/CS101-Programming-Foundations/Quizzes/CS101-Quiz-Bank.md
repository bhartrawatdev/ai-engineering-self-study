# CS101 — Self-Check Quiz Bank

Informal, ungraded. Use these to spot-check yourself at the end of each week — if you can answer confidently without looking anything up, you're on track. No scoring, no passing threshold, just an honesty check.

## Week 1–2 — Basics & Control Flow

1. What does `"5" * 3` evaluate to, and why doesn't `"5" + 3` work the same way?
2. Why is `range(5)` producing `0, 1, 2, 3, 4` and not `1, 2, 3, 4, 5` a common source of bugs?
3. Rewrite this loop as a list comprehension: `result = []` then `for x in items: if x > 0: result.append(x * 2)`.
4. When would you reach for a `while` loop instead of a `for` loop?

## Week 3 — Data Structures

5. What's the difference between `list_b = list_a` and `list_b = list_a.copy()`? Why does it matter?
6. Given a problem where you need to count how many times each item appears in a list, which data structure do you reach for first, and why?
7. Name one operation that's meaningfully faster on a `set` than on a `list`, and explain why.
8. When would you choose a tuple over a list for the same data?

## Week 4 — Functions & Scope

9. What's the difference between `*args` and `**kwargs`, in your own words?
10. Why is `def f(x, items=[]):` considered a bug trap in Python?
11. Describe a closure without using the word "closure."
12. What's the base case of a recursive function, and what happens if you forget one?

## Week 5 — Strings, Files & Errors

13. Why does using a `with` statement to open a file matter, beyond shorter syntax?
14. What's wrong with a bare `except:` (no exception type specified)?
15. When is regex the right tool, and when is it the wrong tool (e.g. for parsing JSON)?

## Week 6 — Modules & Standard Library

16. Why use a virtual environment instead of installing packages globally?
17. What does `collections.defaultdict` save you from writing by hand?
18. What does the `if __name__ == "__main__":` guard actually do, and why does it matter?

## Week 7 — Light OOP

19. What's the difference between a class and an instance, in plain terms?
20. Why does `self` need to be the first parameter of an instance method?
21. Give one concrete reason you'd use a class instead of a dictionary for the same data.

## Week 8 — NumPy & Integration

22. What does "vectorized" mean, and why is it usually faster than a Python-level loop?
23. If you're writing a `for` loop to process every element of a NumPy array one at a time, what should that make you suspicious of?
24. Without writing code, describe how you'd structure the Main Project (Log Analyzer) into files and classes.

## Full-Course Gut Check

25. Pick any ~50-line Python script you didn't write (a tutorial example, a snippet from docs) and explain what it does, line by line, out loud, without running it. If you can do this comfortably, CS101 is done.
