# Capability‑Space Coordinate Definition  
*(core 4‑D dynamics basis with optional extensions)*  

| Symbol | Description | Unit | Notes |
|:------:|-------------|:----:|-------|
| **a<sub>x</sub>** | Longitudinal acceleration (body‑frame) | m/s² | Positive = forward |
| **a<sub>y</sub>** | Lateral acceleration (body‑frame)      | m/s² | Positive = left |
| **ψ̇** (yaw rate) | Yaw‑rate about Z‑axis                  | rad/s | Directly sensed or estimated |
| **β** (beta)      | Sideslip angle                         | rad   | β ≈ arctan(v<sub>y</sub>/v<sub>x</sub>) |

### Optional (used in ablations / appendix)

| Symbol | Description | Unit | Notes |
|:------:|-------------|:----:|-------|
| **κ** (kappa) | Path curvature = ψ̇ / V | 1/m | One‑to‑one mapping with ψ̇ (see App.A) |
| **λ<sub>z</sub>** | Vertical load ratio = min(F<sub>z</sub>)/m g | – | 0 ≤ λ<sub>z</sub> ≤ 1; λ→0 ⇒ wheel lift‑off |

---

## Core State Vector  

\[
\mathbf{z} \;=\; \bigl(a_x,\; a_y,\; \dot\psi,\; \beta\bigr) \;\in\; \mathbb R^{4}.
\]

All theoretical results (existence, uniqueness, ε‑upper‑bound) are proved on  
the 4‑D state space **ℝ⁴** formed by **z**.

---

## Remark — Deriving the 2 s Position‑Reachable Set  

The 2‑second position‑level reachable footprint is **not** part of the core  
coordinate, but can be *derived* by forward integrating **z** via a 3‑DoF  
bicycle model:

\[
\mathcal R_{2\text{s}} \;=\; \Phi_{2\text{s}}\!\bigl(\mathcal C(x_\text{veh},x_\text{env})\bigr)
\;\subset\; \mathbb R^{2},
\]

where **Φ<sub>2 s</sub>** propagates **z** over *t ∈ [0, 2 s]* to obtain (x, y) points.  
Completeness of the core capability envelope **𝒞** guarantees that any real  
trajectory within 2 s lies inside **ℛ<sub>2 s</sub>**. This footprint is only used for  
visualization (Fig. 14) and case‑study analysis; it does **not** enter the  
existence‑uniqueness theorem nor the complexity table.

---

*Last updated : 2025‑08‑06*  
