# MA101 — Self-Check Quiz Bank

Informal, ungraded. Use these to spot-check yourself at the end of each week — if you can answer confidently without looking anything up, you're on track.

## Week 1 — Vectors & Vector Operations

1. What are the three ways of thinking about a vector, and why are they all the same object?
2. If two vectors' dot product is zero, what does that tell you geometrically?
3. What's the practical difference between the L1 norm and the L2 norm of a vector?
4. Given two vectors pointing in nearly opposite directions, would you expect their dot product to be positive or negative?

## Week 2 — Matrices & Matrix Operations

5. Why is matrix multiplication defined the specific way it is, instead of just being element-wise?
6. If `A` is shape `(3, 4)` and `B` is shape `(4, 2)`, what shape is `A @ B`? What about `B @ A`?
7. Is matrix multiplication commutative? Why or why not, in terms of what matrices represent?
8. What does multiplying a vector by a matrix actually *do* to that vector?

## Week 3 — Linear Transformations & Systems of Equations

9. How does `Ax = b` relate to the idea of a matrix as a transformation?
10. Without solving it, how could you tell a 2x2 system of equations has no unique solution just by looking at the coefficients?
11. What does a shear transformation do to a square, geometrically?
12. Why does `numpy.linalg.solve(A, b)` get preferred over manually inverting `A`?

## Week 4 — Determinants, Inverses & Rank

13. What does it mean, geometrically, for a matrix's determinant to be zero?
14. Why does a matrix with a zero determinant have no inverse?
15. What does "rank" measure about a matrix, in plain language?
16. Can a large matrix (say, 10x10) have a low rank? What would that imply?

## Week 5 — Eigenvalues, Eigenvectors & Diagonalization

17. In your own words (no jargon), what is an eigenvector?
18. What's the relationship between an eigenvector and its corresponding eigenvalue?
19. For a diagonal matrix, what are its eigenvalues and eigenvectors, without computing anything?
20. Why is diagonalization useful for computing something like `A^10`?

## Week 6 — Norms, Orthogonality & Dimensionality Reduction

21. What does SVD decompose a matrix into, and why does it work for non-square matrices when eigendecomposition doesn't?
22. In one sentence, what is PCA actually doing, in terms of eigenvectors?
23. Why does keeping only the top few singular values of an image still produce a recognizable reconstruction?
24. What's the practical reason SVD is more commonly used than plain eigendecomposition in real ML systems?

## Full-Course Gut Check

25. Without looking anything up, implement 2-component PCA from scratch on a small synthetic dataset (covariance matrix → eigendecomposition → projection) and get a result that visually matches scikit-learn's PCA on the same data. If you can do this comfortably, MA101 is done.
