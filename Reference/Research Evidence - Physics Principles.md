# Research Evidence: Physics Principles of Acoustic Metamaterials

> Source: Web research conducted June 2026. See sources at end.

## 1. Fundamental Mechanisms

Acoustic metamaterials (AMs) are artificially architected structures composed of subwavelength unit cells that manipulate sound wave propagation in ways impossible with conventional materials.

### Core Physical Principles (Comandini et al., Applied Physics Reviews, March 2025 — 53pp, 732 refs)

| Mechanism | Description |
|-----------|-------------|
| **Acoustic Impedance** | Mismatch between material and air controls reflection/transmission |
| **Bragg Scattering** | Periodic structures create band gaps via constructive/destructive interference |
| **Local Resonance (LRSM)** | Mass-spring-type resonators produce band gaps well below Bragg frequencies |
| **Helmholtz Resonance** | Cavity-and-neck structures providing tuned narrowband absorption |
| **Thermoviscous Losses** | Viscous dissipation in narrow channels, critical for broadband absorption |
| **Fano-like Interference** | Asymmetric resonance profiles from coupled resonant/non-resonant paths |
| **Generalized Snell's Law** | Phase-gradient metasurfaces for anomalous reflection/refraction |

## 2. Key Formulas

### Helmholtz Resonator
```
f₀ = (c / 2π) × √(A / (V × L_eff))

Where:
  f₀    = resonance frequency (Hz)
  c     = speed of sound in air (≈343 m/s at 20°C)
  A     = cross-sectional area of neck (m²)
  V     = cavity volume (m³)
  L_eff = effective neck length = L_neck + 1.7×r (end correction)
```

### Membrane-Type Acoustic Metamaterial (MAM)
```
f₀ = (1 / 2π) × √(k_eff / m_eff)

Where:
  k_eff = effective stiffness of membrane + air cavity
  m_eff = effective mass including attached mass plate + air loading
```

### Sound Transmission Loss (STL)
```
STL = 10 × log₁₀(1/τ)  [dB]

Where τ = transmitted power / incident power
```

### Quarter-Wavelength Resonance
```
f = c / (4 × L_eff)

Where L_eff = effective path length of folded/labyrinthine channel
```

## 3. Key Geometric Architectures

- **Helmholtz-type** — cavity-neck resonators (classic bottle resonance)
- **Membrane-type** — tensioned membranes with attached masses
- **Labyrinthine/Coiled** — tortuous paths maximizing phase delay in compact volume
- **Plate-type (PAMs)** — thin plates with periodic mass attachments
- **Sonic Black Hole** — tapered waveguide profiles that funnel and dissipate energy
- **Origami/Folded** — fold-induced acoustic-mass effect shifts absorption to lower frequencies

## 4. Performance Benchmarks (2024-2026)

| Innovation | Mechanism | Performance |
|------------|-----------|-------------|
| Viscoelastic-shell HR | Material damping | >97% absorption, 227–329 Hz, λ/15 thick |
| Blockfold origami (BOSAM) | Fold-induced mass effect | α>0.85, 440–1958 Hz, 19 mm (λ/44) |
| Acoustic Black Hole (ρ-ABH) | Density gradient | 25–1200 Hz absorption, threshold 24.5 Hz |
| Mirror-symmetric labyrinth | Reciprocal resonance | >22 dB attenuation, 659–1495 Hz, λ/18 |
| Nonlocal coupling gradient | Phase cancellation | Avg STL 32.8 dB, 400–2500 Hz |

## 5. Design Equations Summary

### For labyrinthine/space-coiling metamaterial:
- Target frequency: f_target = c / (4 × L_path)
- For 100 Hz: L_path ≈ 343/(4×100) = 0.858 m path in a thin panel
- For 500 Hz: L_path ≈ 0.172 m

### For coupled resonator array:
- Bandwidth ∝ number of detuned resonators
- Optimal spacing: stagger resonance frequencies by ~20-30% for smooth coverage
- Coherent weak-resonance coupling produces flatter absorption curves

## Sources
- Comandini et al. (2025), *Applied Physics Reviews* — comprehensive 53-page review
- *Nature Communications* (2025) Vol. 16, 11276 — ρ-ABH acoustic black hole
- *Materials & Design* (2025) — nonlocal coupling gradient metamaterial
- *Physics Letters A* (April 2025) — plate-type AM + Helmholtz STL overlay
- *Building and Environment* (2026) — blockfold origami BOSAM
- *J. Brazilian Soc. Mech. Sci. Eng.* (2025) — mirror-symmetric labyrinth
