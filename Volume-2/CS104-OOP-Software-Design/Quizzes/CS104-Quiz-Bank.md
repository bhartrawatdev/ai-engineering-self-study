# CS104 — Self-Check Quiz Bank

Informal, ungraded. Use these to spot-check yourself at the end of each week — if you can answer confidently without looking anything up, you're on track.

## Week 1 — OOP Pillars, Properly

1. Is Python's `_protected`/`__private` naming convention actually enforced by the language? What does it actually do?
2. What's the difference between `__repr__` and `__str__`?
3. Why does defining `__eq__` on a class affect whether instances can be used in a set or as a dict key?
4. When would you use `@property` instead of a plain attribute?

## Week 2 — Inheritance & Polymorphism

5. What makes inheritance the "right" tool for a given relationship, versus the wrong one?
6. What does an abstract base class actually enforce that a plain class doesn't?
7. What is duck typing, and how does it let you skip formal inheritance in some cases?
8. Why is a deep inheritance chain (5+ levels) usually considered a design smell?

## Week 3 — Composition & Design Principles

9. What does "composition over inheritance" mean, in a sentence?
10. What's a "God object," and what design principle does it violate?
11. Explain the Open/Closed principle in your own words, with a small example.
12. Why aren't SOLID principles meant to be applied rigidly to every piece of code?

## Week 4 — Common Design Patterns

13. What problem does the Strategy pattern solve?
14. When would a Factory pattern be worth the added complexity over direct instantiation?
15. What does the Observer pattern decouple from what?
16. Why is the Singleton pattern often considered risky or overused?

## Week 5 — Type Hints, Dataclasses & Modern Python

17. Do type hints change Python's behavior at runtime by default? What actually enforces them?
18. What does `@dataclass` generate for you automatically?
19. Why do type hints pay off more on a multi-file project than a small standalone script?
20. What's the point of running `mypy` if you already have type hints in your code?

## Week 6 — Testing & Testable Design

21. What does "arrange/act/assert" mean as a test structure?
22. Why is untested code considered a design liability, not just a quality concern?
23. What's a concrete sign that a piece of code is hard to test, and how would you fix it?
24. What's wrong with a single test that checks many unrelated behaviors at once?

## Week 7 — Packaging & Project Structure

25. Why does a proper package structure (with `__init__.py` and absolute imports) matter more as a project grows?
26. What does `pip install -e .` actually let you do that you couldn't before?
27. What should a good project README always include?

## Full-Course Gut Check

28. Given a plain, untested, tightly-coupled 100-line script, walk through — out loud, without notes — how you'd refactor it: which responsibilities you'd split out, which pattern (if any) fits, how you'd add type hints, and how you'd start testing it. If you can do this comfortably, CS104 is done.
