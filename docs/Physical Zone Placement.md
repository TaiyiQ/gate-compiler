## Physical Zone Placement

| Zone             | Purpose                        | Atom spacing                         | Notes                                                     |
| ---------------- | ------------------------------ | ------------------------------------ | --------------------------------------------------------- |
| **Storage**      | Idle qubits live here          | `storage_spacing_um` (default 10 µm) | Keep > R_b so idle atoms don't accidentally interact      |
| **Entanglement** | 2-qubit CZ gates executed here | `ent_spacing_um` (default 5 µm)      | Must be < R_b; all pairs guaranteed within blockade range |
| **Readout**      | Fluorescence measurement       | ≥ 8 µm                               | Single column, one atom per slot                          |