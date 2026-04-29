# Gate Decomposition

Decomposes all logical gates into the **native gate set**: `{RX, RY, RZ, CZ, MEASURE}`.

```
  Decompositions:

  H    →  RY(π/2) · RZ(π)
  X    →  RX(π)
  Y    →  RY(π)
  Z    →  RZ(π)
  S    →  RZ(π/2)
  T    →  RZ(π/4)
  SDG  →  RZ(-π/2)
  TDG  →  RZ(-π/4)

  CNOT(ctrl, tgt) →  RY(π/2) · RZ(π) [on tgt]
                      CZ(ctrl, tgt)
                      RY(π/2) · RZ(π) [on tgt]
```

Phase conventions follow Jaksch et al. (2000) PRL 85, 2208.