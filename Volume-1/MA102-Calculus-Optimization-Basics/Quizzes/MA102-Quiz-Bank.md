# MA102 — Self-Check Quiz Bank

Informal, ungraded. Use these to spot-check yourself at the end of each week — if you can answer confidently without looking anything up, you're on track.

## Week 1 — Derivatives & Rates of Change

1. In plain language, what question does a derivative answer?
2. If a function's derivative is negative at a point, what does that tell you about the function there?
3. Can a function have a derivative of zero at a point that isn't a maximum or minimum? Give an example.
4. What does the power rule actually compute, in words, not just symbols?

## Week 2 — Chain Rule & Differentiation Rules

5. For `f(x) = sin(3x + 1)`, identify the outer and inner functions before differentiating.
6. What's the most common mistake people make when applying the chain rule?
7. What is numerical differentiation, and why is it useful as a sanity check rather than a primary method?
8. Why does the chain rule matter so much more for this program than the product or quotient rule?

## Week 3 — Partial Derivatives & Gradients

9. What does it mean to take a "partial" derivative — what are you holding constant?
10. What does the gradient vector represent, geometrically?
11. If you're standing on a hill and want to go downhill fastest, which direction relative to the gradient would you walk?
12. On a contour plot, what's the relationship between the gradient direction and the contour lines?

## Week 4 — Gradient Descent

13. In one or two sentences, describe the entire gradient descent algorithm.
14. What happens to gradient descent's behavior if the learning rate is set way too high? Too low?
15. Why would you use stochastic or mini-batch gradient descent instead of computing the gradient over the full dataset every step?
16. Looking at a loss-over-iterations plot that's oscillating wildly and increasing, what would you suspect is wrong?

## Week 5 — Jacobians, Hessians & Convexity

17. How does the Jacobian relate to the gradient — what's the generalization?
18. If a Hessian's eigenvalues at a critical point are all positive, what kind of point is it?
19. What does convexity guarantee about a function's local minima?
20. Why is it expected, not a bug, that gradient descent on a neural network's loss doesn't necessarily find the global minimum?

## Week 6 — Toward Backpropagation

21. Is backpropagation a separate algorithm from the chain rule, or an application of it? Explain briefly.
22. What's the difference between the forward pass and backward pass in a computational graph?
23. What distinguishes automatic differentiation from both numerical and symbolic differentiation?
24. Why does the backward pass depend on values computed during the forward pass?

## Full-Course Gut Check

25. Without looking anything up, implement gradient descent from scratch on a simple 1D function, and correctly diagnose — from the loss curve alone — whether a given learning rate is too high, too low, or good. If you can do this comfortably, MA102 is done.
