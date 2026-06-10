# 🔬 PHYSICS WORKBOOK — Student A (Lead) & Student B (Support)

**This is your complete guide to the acoustic physics of the project.**

---

## PART 1: UNDERSTANDING THE PROBLEM

### Why Low Frequencies Are Hard to Block

| Frequency | Wavelength (λ) | λ/4 (conventional absorber needed) | Our panel (5 cm) |
|-----------|----------------|-------------------------------------|-------------------|
| 250 Hz | 1.37 m | 34 cm | Only 5 cm! |
| 500 Hz | 0.69 m | 17 cm | Only 5 cm! |
| 1000 Hz | 0.34 m | 8.6 cm | Only 5 cm! |
| 2000 Hz | 0.17 m | 4.3 cm | 5 cm is enough |

**The key insight:** At 250 Hz, a conventional foam absorber would need to be 34 cm thick. Our metamaterial panel does it in 5 cm by folding the sound path or using resonance. This is the ENTIRE point of the project.

### Speed of Sound

```
c = 331.3 × √(1 + T/273.15)

At 20°C (room temperature): c ≈ 343 m/s
At 25°C: c ≈ 346 m/s
At 15°C: c ≈ 340 m/s

Use 343 m/s for all calculations unless your room is very hot/cold.
```

---

## PART 2: HELMHOLTZ RESONATOR DESIGN

### The Master Formula

```
        c         A
f₀ = ───── × √(────────)
      2π        V × L_eff

Where:
  f₀    = resonance frequency (Hz)
  c     = speed of sound = 343 m/s
  A     = cross-sectional area of the neck (m²)
  V     = cavity volume (m³)
  L_eff = effective neck length (m)
```

### Effective Neck Length (IMPORTANT — don't forget this!)

```
L_eff = L_physical + END CORRECTION

For a neck flush with the surface (flanged):
  End correction = 0.85 × d  (add once for outer end)

For an unflanged neck (protruding):
  End correction = 0.70 × d  (add once for outer end)

For both ends open (if neck goes through a thin wall):
  Add end correction for BOTH ends

Where d = diameter of the neck (circular) or equivalent diameter
  For rectangular neck: d_equiv = √(4A/π)
```

### Design Strategy: Pick Materials First, Then Calculate

You can't freely choose dimensions — you're limited by available materials. Strategy:

1. Choose available container (bottle, PVC tube, cardboard box) → this fixes V
2. Choose available neck material (straw, small tube, bottle neck) → this fixes A
3. Adjust L_eff to hit target frequency
4. If you can't adjust L_eff enough, change the cavity volume or neck area

---

## PART 3: STEP-BY-STEP CALCULATIONS

### Example: Target 250 Hz with a 500mL Plastic Bottle

**Given:**
- Bottle volume: 500 mL = 5 × 10⁻⁴ m³
- Neck: bottle opening, diameter ~2.2 cm = 0.022 m
- Neck area: A = π(0.011)² = 3.80 × 10⁻⁴ m²
- Neck physical length: ~1.5 cm = 0.015 m

**Step 1: Calculate end correction**
```
d = 0.022 m
End correction (flanged) = 0.85 × 0.022 = 0.0187 m
L_eff = 0.015 + 0.0187 = 0.0337 m
```

**Step 2: Calculate resonance frequency**
```
f₀ = (343/2π) × √(3.80×10⁻⁴ / (5×10⁻⁴ × 0.0337))
f₀ = 54.60 × √(3.80×10⁻⁴ / 1.685×10⁻⁵)
f₀ = 54.60 × √(22.55)
f₀ = 54.60 × 4.749
f₀ = 259 Hz  ← Close to 250 Hz!
```

**Step 3: Tune it**
- To lower f₀: make the neck longer (add a straw), or make the cavity bigger
- To raise f₀: make the neck shorter/wider, or make the cavity smaller

### Your Turn: Calculate for Each Target Frequency

Use the worksheet below. All values in SI units (meters, m², m³, kg).

#### RESONATOR 1: Target 250 Hz

| Parameter | Symbol | Value | Unit |
|-----------|--------|-------|------|
| Container/material | — | ________ | — |
| Cavity volume | V | ________ | m³ |
| Neck diameter (or width) | — | ________ | m |
| Neck area | A | ________ | m² |
| Neck physical length | L_phys | ________ | m |
| End correction type | — | flanged/unflanged | — |
| End correction | — | ________ | m |
| Effective neck length | L_eff | ________ | m |
| **Calculated f₀** | **f₀** | **________** | **Hz** |
| Error from target | — | ________ | % |

#### RESONATOR 2: Target 500 Hz

| Parameter | Symbol | Value | Unit |
|-----------|--------|-------|------|
| Container/material | — | ________ | — |
| Cavity volume | V | ________ | m³ |
| Neck diameter (or width) | — | ________ | m |
| Neck area | A | ________ | m² |
| Neck physical length | L_phys | ________ | m |
| End correction type | — | flanged/unflanged | — |
| End correction | — | ________ | m |
| Effective neck length | L_eff | ________ | m |
| **Calculated f₀** | **f₀** | **________** | **Hz** |
| Error from target | — | ________ | % |

#### RESONATOR 3: Target 750 Hz

| Parameter | Symbol | Value | Unit |
|-----------|--------|-------|------|
| Container/material | — | ________ | — |
| Cavity volume | V | ________ | m³ |
| Neck diameter (or width) | — | ________ | m |
| Neck area | A | ________ | m² |
| Neck physical length | L_phys | ________ | m |
| End correction type | — | flanged/unflanged | — |
| End correction | — | ________ | m |
| Effective neck length | L_eff | ________ | m |
| **Calculated f₀** | **f₀** | **________** | **Hz** |
| Error from target | — | ________ | % |

#### RESONATOR 4: Target 1000 Hz

| Parameter | Symbol | Value | Unit |
|-----------|--------|-------|------|
| Container/material | — | ________ | — |
| Cavity volume | V | ________ | m³ |
| Neck diameter (or width) | — | ________ | m |
| Neck area | A | ________ | m² |
| Neck physical length | L_phys | ________ | m |
| End correction type | — | flanged/unflanged | — |
| End correction | — | ________ | m |
| Effective neck length | L_eff | ________ | m |
| **Calculated f₀** | **f₀** | **________** | **Hz** |
| Error from target | — | ________ | % |

---

## PART 4: RESONATOR ARRAY LAYOUT

### Why Multiple Resonators?

One resonator = one narrow absorption peak. Four detuned resonators = four peaks that overlap = broader absorption.

### Layout Principles:

1. **Spread frequencies** — stagger by ~20–30% (we're doing: 250, 500, 750, 1000)
2. **Avoid mutual interference** — space resonators at least 2× neck diameter apart
3. **Distribute evenly** — don't cluster all resonators on one side
4. **Front-facing necks** — all neck openings face the sound source

### Suggested 30×30 cm Layout:

```
┌──────────────────────────────────┐
│                                  │
│   ┌─────┐          ┌─────┐      │
│   │250Hz│          │500Hz│      │
│   │  ○  │          │  ○  │      │
│   └─────┘          └─────┘      │
│                                  │
│          ┌─────┐    ┌─────┐     │
│          │750Hz│    │1000 │     │
│          │  ○  │    │ Hz ○│     │
│          └─────┘    └─────┘     │
│                                  │
│     (Porous fabric backing)      │
│     behind all resonators        │
└──────────────────────────────────┘
        30 cm × 30 cm panel
```

### Quarter-Wave Folded Channels (Optional Enhancement)

If you have time and skill, add folded channels for continuous broadband absorption:

```
Target 500 Hz quarter-wave:
  L = c/(4f) = 343/(4×500) = 0.172 m = 17.2 cm path length

In a 5 cm thick panel, fold the path:
  ┌──┐
  │  │  ← 5 cm total thickness
  │  │
  │  ↓  Path goes: down → across → up → across → down
  └──┘  Total path = 5+12+5+12+5 ≈ 39 cm ← can target lower freq!
```

---

## PART 5: PREDICTED PERFORMANCE MODELING

### Simple Absorption Prediction (Spreadsheet Method)

For each frequency, estimate the absorption coefficient:

```
α_expected = α_porous_layer + Σ(α_resonator_i × coupling_factor_i)

Where:
  α_porous_layer ≈ 0.2–0.4 (for fabric/felt backing)
  α_resonator_i ≈ 0.7–0.95 at f₀_i, drops to ~0.1 at other frequencies
  coupling_factor_i ≈ 0.7–0.9 (accounts for mutual interference)
```

Create a table like this:

| Frequency (Hz) | Porous α | Res1 α | Res2 α | Res3 α | Res4 α | Total α (predicted) |
|----------------|----------|--------|--------|--------|--------|---------------------|
| 125 | | | | | | |
| 250 | | | | | | |
| 500 | | | | | | |
| 750 | | | | | | |
| 1000 | | | | | | |
| 2000 | | | | | | |

---

## PART 6: TESTING PROTOCOL (Physics Lead Responsibility)

### Equipment Setup:

```
                    30 cm
    [Speaker] ────────── [Panel] ── [Phone Mic]
       ↑                    ↑            ↑
       |←──── 15 cm ────→|←─ 5 cm ─→|
       
    All at same height
    Mark positions with tape on the table
    Speaker at consistent volume (mark the volume setting!)
```

### Measurement Procedure (Do EXACTLY this each time):

1. **Baseline measurement (no panel):**
   - Play tone at test frequency for 10 seconds
   - Record SPL (sound pressure level) in dB
   - Repeat 3 times → average

2. **With panel:**
   - Insert panel between speaker and phone
   - Play SAME tone at SAME volume
   - Record SPL
   - Repeat 3 times → average

3. **Calculate attenuation:**
   ```
   ΔdB = SPL_baseline(dB) - SPL_with_panel(dB)
   ```
   Positive ΔdB = panel is blocking sound ✓

### Data Recording Sheet:

| Prototype | Frequency | Trial 1 (dB) | Trial 2 (dB) | Trial 3 (dB) | Average (dB) | Baseline (dB) | ΔdB |
|-----------|-----------|--------------|--------------|--------------|--------------|---------------|-----|
| A | 250 | | | | | | |
| A | 500 | | | | | | |
| A | 1000 | | | | | | |
| A | 2000 | | | | | | |
| B | 250 | | | | | | |
| B | 500 | | | | | | |
| B | 1000 | | | | | | |
| B | 2000 | | | | | | |
| C | 250 | | | | | | |
| C | 500 | | | | | | |
| C | 1000 | | | | | | |
| C | 2000 | | | | | | |

### Expected Results:

| Prototype | 250 Hz | 500 Hz | 1000 Hz | 2000 Hz |
|-----------|--------|--------|---------|---------|
| A (flat) | 0–2 dB | 1–3 dB | 2–4 dB | 3–5 dB |
| B (honeycomb) | 1–3 dB | 2–5 dB | 3–6 dB | 4–7 dB |
| C (EcoMetaPanel) | **3–8 dB** | **4–10 dB** | **3–7 dB** | **2–5 dB** |

**Prototype C should show the biggest advantage at 250 and 500 Hz — that's the whole point!**

---

## PART 7: THEORY vs. EXPERIMENT ANALYSIS

After testing, fill this out:

| Frequency | Predicted f₀ (Hz) | Measured peak (Hz) | Difference (%) | Explanation |
|-----------|-------------------|---------------------|----------------|-------------|
| 250 Hz target | | | | |
| 500 Hz target | | | | | |
| 750 Hz target | | | | | |
| 1000 Hz target | | | | | |

### Sources of Error to Discuss:

1. **End correction uncertainty** — the formula is approximate
2. **Leakage** — air gaps around necks reduce resonance
3. **Material damping** — cardboard absorbs some energy, shifts resonance
4. **Temperature variation** — c changes with temperature (±0.6 m/s per °C)
5. **Ambient noise** — background sounds contaminate measurements
6. **Phone mic limitations** — not calibrated, frequency response not flat
7. **Speaker nonlinearity** — may not produce pure tones at all frequencies

---

## KEY NUMBERS TO MEMORIZE FOR THE PRESENTATION

- Speed of sound: **343 m/s at 20°C**
- 250 Hz wavelength: **1.37 m** → conventional absorber needs **34 cm**, we use **5 cm**
- Our thickness-to-wavelength ratio at 250 Hz: **λ/27** (5 cm / 137 cm)
- Helmholtz formula: **f₀ = (c/2π) × √(A/V·L_eff)**
- Number of resonators in Prototype C: **4** (one per target frequency)
- Primary mechanism: **Helmholtz resonance + thermoviscous dissipation**

---

*Give your completed calculations to Student B for CAD, and to Student E for data format planning.*
