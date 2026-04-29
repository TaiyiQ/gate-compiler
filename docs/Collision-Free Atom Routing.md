## Collision-Free Atom Routing

### Conflict-Based Search (CBS)

Implements CBS (Sharon et al. 2015, AIJ 219) for multi-agent pathfinding on the discrete grid.

**Why CBS?** Multiple atoms can shuttle simultaneously. Naive independent A\* paths may collide — two atoms at the same grid cell at the same timestep (*vertex conflict*), or two atoms swapping positions in one step (*edge/swap conflict*). CBS finds provably optimal collision-free paths.

**Algorithm**

```
TODO
```

**Space-time A\*** (inner search):

Each node in the A\* search space is `(timestep, col, row)`. The agent can wait in place (cost 1) or move to any of 4 adjacent cells. Vertex and edge constraints are checked before expanding each node. Heuristic: Manhattan distance to goal.

**Grid parameters:**
- Grid size: 24 × 12 cells
- Cell size: 5 µm/cell
