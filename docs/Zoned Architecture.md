## Zoned Architecture

| Zone             | Purpose                        | Atom Spacing                       | Notes                                                     |
| ---------------- | ------------------------------ | ---------------------------------- | --------------------------------------------------------- |
| **Storage**      | Idle qubits live here          | $d_s = 3\;\mu m$         | Keep > R_b so idle atoms don't accidentally interact      |
| **Entanglement** | 2-qubit CZ gates executed here | $d_{\omega} = 10\;\mu m$, $d_{ryd} = 2\;\mu m$ | Must be < R_b; all pairs guaranteed within blockade range |
| **Readout**      | Fluorescence measurement       | ≥ 8 µm                             | Single column, one atom per slot                          |

Parameters are pulled from [[Reuse-Aware Compilation for Zoned Quantum Architectures Based on Neutra Atoms]]. The layout schematic [[layout.excalidraw]] displays the parameters visually.

A typical zoned architecture only contains a single instance of each zone type:
1. Storage Zone
2. Entangle Zone
3. Readout Zone

- JSON for machine generated IR
- TOML for configs that are created by engineers, see [[arch]]