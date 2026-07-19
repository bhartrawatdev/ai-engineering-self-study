# CS103 — Main Project: Grid Pathfinding Visualizer

This is the standalone spec for CS103's Main Project (also summarized in `CS103.md`). Use this file as your working checklist while building.

## Description

A tool that visualizes and compares BFS, DFS, and Dijkstra's algorithm finding a path across a 2D grid with obstacles and varying terrain costs. This project exists to make the difference between these algorithms visible and concrete — not just three implementations that happen to all "find a path," but a real comparison of how and why they behave differently.

## Requirements

- [ ] Represent a 2D grid as a graph — each open cell connects to its valid neighbors — with configurable obstacles (impassable cells).
- [ ] Implement BFS, DFS, and Dijkstra's algorithm (using a heap) to find a path from a start cell to an end cell.
- [ ] Support at least two different terrain costs for Dijkstra specifically (e.g. normal cells cost 1, difficult terrain costs 3), so weighted-graph behavior is genuinely exercised.
- [ ] Visualize each algorithm's result: the final path found, and ideally the order cells were explored in (a simple Matplotlib grid coloring by visit order is enough).
- [ ] Report path length/cost and number of cells explored for each algorithm on the same grid.
- [ ] Write a short comparison in this project's README explaining the differences you observed.

## Suggested File Layout

```
grid-pathfinder/
├── grid.py               ← Grid representation, neighbor logic, obstacles/terrain costs
├── search.py               ← BFS, DFS, Dijkstra implementations
├── visualize.py             ← Matplotlib visualization of paths/exploration order
├── main.py                   ← ties it together, runs all three algorithms on a grid
├── outputs/                   ← saved comparison visualizations
├── requirements.txt
└── README.md                   ← how to run it + your written comparison
```

## Stretch Goals

- [ ] Implement A* search (Dijkstra + a heuristic) and compare its explored-cell count against plain Dijkstra on the same grid.
- [ ] Generate random grids with random obstacles/terrain costs and run all algorithms across several grids for a broader comparison, not just one example.
- [ ] Add a simple step-by-step animation of the search frontier expanding.

## What "Done" Looks Like

- All three algorithms run correctly on at least one non-trivial grid with obstacles, producing valid paths (or correctly reporting no path exists when the end is unreachable).
- At least one clear visualization compares the algorithms' explored-cell counts or paths on the same grid.
- You can explain, without notes, why BFS finds the shortest path on an unweighted grid but can produce a suboptimal path once terrain costs are introduced, while Dijkstra handles both correctly.
- Code is organized into functions/classes across multiple files, pushed to this repo's `Projects/` folder with a README including the comparison and visualizations.

## Notes on Building the Grid

Start small (a 10x10 or 15x15 grid) while developing — it's easier to hand-verify correctness on a small grid before scaling up to something larger for the final visualizations. Hardcode a couple of interesting obstacle layouts (e.g. a wall with a single gap, a maze-like pattern) rather than only testing on random noise, since deliberate layouts make the algorithms' different behaviors much easier to see and explain.
