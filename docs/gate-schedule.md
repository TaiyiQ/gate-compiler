# Gate Schedule


- Routing-Aware Placement for Zoned NA-based QC
	- Reuse-Aware COmpilation for Zoned Quantum Architecutres Based on NA

The compiler is independent of any vendor SDK. It will define its own intermediate representation (IR), and has to perforce the following steps:

1. [[Zoned Architecture]]
2. [[Gate Decomposition]]
3. [[Stage Scheduling]]
4. [[Physical Zone Placement]]
5. [[Collision-Free Atom Routing]]
6. Fidelity Estimation
7. Iterative Refinement

## Hardware Contraints

- [ ] At what level does timing sit. Gate compiler or Pulse compiler?
	- [ ] Can we control the speed of which AOD moves?
	- [ ] Can we select if the AOD picks up a row or a col?

| Constant                    | Default | Unit  | Physical meaning                  |
| --------------------------- | ------- | ----- | --------------------------------- |
| `T_SHUTTLE_SPEED_UM_PER_US` | 0.05    | µm/µs | Optical tweezer translation speed |
| `T_SETTLE_US`               | 0.5     | µs    | Atom thermalisation after a move  |
| `T_GATE_1Q_US`              | 0.2     | µs    | Single-qubit rotation pulse       |
| `T_GATE_CZ_US`              | 0.4     | µs    | CZ - 3-pulse Rydberg sequence     |
| `T_MEASURE_US`              | 200.0   | µs    | Fluorescence readout              |
| `GRID_COLS`                 | 24      | cells | Discrete routing grid width       |
| `GRID_ROWS`                 | 12      | cells | Discrete routing grid height      |
| `CELL_UM`                   | 5.0     | µm    | Physical size of one grid cell    |