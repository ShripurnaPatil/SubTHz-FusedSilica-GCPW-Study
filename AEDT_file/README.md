# Parameterized Ansys HFSS 3D EM Model

Full-wave 3D finite-element electromagnetic project file (**Ansys HFSS 2025 R2**, *Driven Terminal* solver) for the **60–120 GHz Grounded Coplanar Waveguide (GCPW)** on a `100 µm` fused-silica substrate.

## Model & Solver Specifications
* **Project File:** `GCPW_90GHz_Study.aedt` *(mesh/results cleared for lightweight sharing; ready to run)*
* **Substrate Stack-Up:** `100 µm` Fused Silica (`εr = 3.8`, `tanδ = 0.002`) with `1.5 µm` gold conductors (`5 nm` RMS roughness)
* **TGV Ground Fence:** 8 gold-filled Through-Glass Vias (`D_via = 50 µm`, longitudinal pitch `P_via = 120 µm`, `70 µm` inter-via glass web)
* **Adaptive Mesh & Sweep:** Solved at `90 GHz` (`Max Passes = 6`, `Max ΔS = 0.02`) with an interpolating sweep across `45–135 GHz`
* **Included Parametric Setup (`Optimetrics`):** `ParametricSetup1` sweeps center signal width `$S` from `50 µm` to `1100 µm` while automatically scaling slot gaps and sliding the TGV fence outward.

## How to Re-Run in Ansys HFSS
1. Open `GCPW_90GHz_Study.aedt` in Ansys Electronics Desktop (2025 R2 or newer).
2. Right-click **`Analysis → SP1` → Analyze** (`~25 seconds`) to regenerate the `50.0 Ω` baseline (`W = 119 µm`, `L = 540.9 µm`).
3. Right-click **`Optimetrics → ParametricSetup1` → Analyze** (`~3–4 minutes`) to reproduce the full 11-width dispersion sweep.

