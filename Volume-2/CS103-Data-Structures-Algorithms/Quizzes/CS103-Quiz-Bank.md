# CS103 — Self-Check Quiz Bank

Informal, ungraded. Use these to spot-check yourself at the end of each week — if you can answer confidently without looking anything up, you're on track.

## Week 1 — Complexity Analysis

1. What does Big O notation actually describe — speed, or something else?
2. If you have two nested loops both running n times, what's the combined time complexity? What if the loops were sequential instead of nested?
3. Why can an O(n) algorithm sometimes run slower in practice than an O(n²) algorithm?
4. Name the common complexity classes from fastest to slowest growth.

## Week 2 — Linear Data Structures

5. Why is inserting at the front of a Python list O(n) instead of O(1)?
6. What's the core tradeoff between arrays and linked lists?
7. Why is `collections.deque` a better choice than a plain list for a queue?
8. What real-world data structure is the recursive call stack an example of?

## Week 3 — Recursion & Backtracking

9. What are the three steps in the backtracking pattern?
10. What's a common bug that happens when backtracking uses a shared mutable structure?
11. Why can backtracking algorithms have exponential time complexity?
12. What does a "recursion tree" help you visualize?

## Week 4 — Trees & Binary Search Trees

13. What ordering property makes a binary search tree different from a general binary tree?
14. Why does in-order traversal of a BST produce sorted output?
15. What happens to a BST's performance if you insert already-sorted data one element at a time?
16. What's the trickiest case when deleting a node from a BST, and how is it typically handled?

## Week 5 — Hash Tables & Heaps

17. In plain terms, what does a hash function do, and why does collision handling matter?
18. Why is average-case O(1) lookup possible for a hash table, and when can it degrade?
19. What does a min-heap guarantee about its structure, and what does it NOT guarantee?
20. Why is a heap a natural fit for "always process the next-cheapest item"?

## Week 6 — Sorting & Searching

21. Why is O(n log n) considered the best possible complexity for comparison-based sorting?
22. What's the difference between quicksort's average-case and worst-case complexity, and what causes the worst case?
23. What precondition does binary search require, and what happens if you ignore it?
24. Why might a hand-written sort still lose to Python's built-in `sorted()` even if both are O(n log n)?

## Week 7 — Graphs

25. What's the key difference in exploration order between BFS and DFS?
26. Why does BFS find the shortest path in an unweighted graph, but not necessarily in a weighted one?
27. Why is a min-heap the natural underlying structure for Dijkstra's algorithm?
28. Why is tracking visited nodes essential for BFS/DFS on a graph but often unnecessary on a tree?

## Week 8 — Dynamic Programming

29. What two properties make a problem "DP-shaped"?
30. What's the relationship between memoization and plain recursion — how much do you actually have to change?
31. What's the difference between top-down (memoization) and bottom-up (tabulation) approaches?
32. Why does adding memoization to naive recursive Fibonacci change its complexity so dramatically?

## Full-Course Gut Check

33. Given an unfamiliar real-world problem description (e.g., "find the fastest way to route a delivery truck through a city with traffic delays on some roads"), identify which data structure(s) and algorithm(s) from this course you'd reach for, and explain why — without being told it's a "graph problem" first. If you can do this comfortably, CS103 is done.
