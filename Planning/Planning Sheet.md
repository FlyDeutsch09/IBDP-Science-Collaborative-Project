# Acoustic Metamaterials — Planning Sheet

**IB Group 4 Collaborative Sciences Project**
**Date:** 10 June 2026 | **Phase:** Planning | **Version:** 1.0

---

## 1. Project Framing

### Central Question
> How can acoustic metamaterials — engineered structures that manipulate sound waves — provide sustainable, futuristic alternatives to conventional architectural sound design?

### Why This Topic Matters
- **Noise pollution** costs Europe ~€100 billion/year in health and productivity losses
- **Conventional soundproofing** (foam, mineral wool) is bulky, petroleum-derived, and performs poorly at low frequencies (traffic hum, HVAC drone)
- **Acoustic metamaterials** break the rules: they can absorb bass frequencies with structures 50× thinner than the wavelength, and can be made from waste plastic, agricultural byproducts, or biodegradable materials
- **Dual sustainability win**: tackles noise pollution AND material waste simultaneously

### IB Criteria Alignment
- **Environmental impact**: life-cycle of materials, carbon footprint, circular economy
- **Energy input/output**: passive operation (no power needed), embodied energy of fabrication
- **Human benefit**: quieter living/working spaces, health improvements, sustainable cities (UN SDG 11)

---

## 2. Scientific Foundations

### Physics Domain (Lead: A, Deputy: B)

**Wave Mechanics:**
- Sound as pressure waves: wavelength λ = c/f (c ≈ 343 m/s in air)
- Low frequency = long wavelength. 100 Hz → λ = 3.43 m. Traditional absorbers need λ/4 thickness (85 cm!). Metamaterials achieve this in 3 cm via path folding.
- Reflection, transmission, absorption: energy conservation R + T + A = 1

**Resonance Physics:**
- Helmholtz resonance: f₀ = (c/2π) × √(A / V·L_eff) — air plug in neck oscillates against cavity spring
- Membrane resonance: f₀ = (1/2π) × √(k_eff / m_eff) — tensioned membrane + added mass
- Quarter-wave resonance: f = c/(4L_eff) — folded channels extend L_eff without increasing thickness

**Metamaterial Mechanisms:**
- **Local resonance** → band gaps at subwavelength scales
- **Impedance matching** → sound enters rather than reflects, then dissipates
- **Thermoviscous losses** → energy converted to heat in narrow channels
- **Bragg scattering** → periodic structure interference creates stop bands

### Chemistry Domain (Lead: C, D)

**Material Chemistry:**
- **Polymers**: PET (polyethylene terephthalate), PVC (polyvinyl chloride) — upcycling waste into acoustic structures; polymer chain structure affects viscoelastic damping
- **Natural fibers**: cellulose/lignin matrix in bamboo, hemp, cork — porosity and fiber morphology control absorption
- **Bio-polymers**: alginate (from seaweed), chitosan — freeze-cast into porous foams; crosslinking density tunes mechanical properties

**Chemical Analysis Methods:**
- FTIR spectroscopy — verify polymer composition of recycled feedstock
- TGA/DSC — thermal stability, glass transition (critical for fire safety)
- Porosimetry — pore size distribution vs. acoustic performance
- Contact angle — hydrophobicity for durability in humid environments

**Chemical Sustainability Metrics:**
- Embodied carbon (kg CO₂-eq per kg material)
- Biodegradability / recyclability at end-of-life
- Toxicological profile (VOC emissions, health during fabrication)

### Interdisciplinary Bridge
- **Materials selection** sits at the physics-chemistry boundary: physical properties (ρ, E, ν, η) determine acoustic behavior; chemical composition determines those physical properties
- **Fabrication processes** (3D printing, freeze-casting, compression molding) are governed by chemistry (rheology, curing, phase transitions) but produce geometries that determine acoustic physics

---

## 3. Project Direction: Chosen Approach

### Primary Focus: Sustainable Metamaterial Panel for Low-Frequency Building Sound Absorption

**Rationale:**
1. Low-frequency noise (traffic, HVAC, industrial) is the hardest problem — and where metamaterials show the biggest advantage over conventional materials
2. Sustainability angle is strong: we can use recycled or bio-based materials
3. Buildable as a physical model: a panel with visible internal structure demonstrates the principle
4. Measurable: smartphone-based acoustic testing can quantify performance

### Target Specification
| Parameter | Target |
|-----------|--------|
| Frequency range | 200–1000 Hz (low-mid, where conventional foam fails) |
| Thickness | ≤ 5 cm (demonstrate subwavelength advantage) |
| Absorption coefficient α | ≥ 0.6 at target frequencies |
| Primary material | Recycled or bio-based (rPET, bamboo, cork, or cardboard) |
| Passive operation | No electronics, purely structural absorption |

### Design Concept: Hybrid Resonator Array + Porous Backing

Combine two mechanisms:
1. **Multiple tuned Helmholtz/membrane resonators** for targeted low-frequency peaks
2. **Porous absorption layer** (natural fiber felt) for broadband mid-frequency absorption

This hybrid approach is backed by 2025–2026 research showing that coherent weak-resonance coupling produces flatter, broader absorption curves than single mechanisms alone.

---

## 4. Workstreams & Task Allocation

### Workstream A: Physics Design & Simulation
**Lead:** A | **Support:** B

| Task | Description | Output |
|------|-------------|--------|
| A1 | Calculate target frequencies and required resonator dimensions using Helmholtz and quarter-wave formulas | Design parameters spreadsheet |
| A2 | Design 3–5 resonator geometries tuned to staggered frequencies across 200–1000 Hz | CAD sketches / drawings |
| A3 | Model acoustic performance using transfer matrix method (analytical, spreadsheet-based) | Predicted absorption curve |
| A4 | Optimize resonator layout for mutual coupling (avoiding anti-resonance dips) | Final resonator array layout |
| A5 | Design testing protocol: impedance tube dimensions, speaker/mic setup | Testing procedure document |

### Workstream B: Materials Chemistry
**Lead:** C | **Support:** D

| Task | Description | Output |
|------|-------------|--------|
| B1 | Characterize available recycled/bio-based materials (composition, density, porosity) | Materials datasheet |
| B2 | Evaluate material suitability: damping properties, workability, sustainability metrics | Material recommendation report |
| B3 | Prepare/test material samples for porous absorption layer | Tested samples with absorption data |
| B4 | Investigate chemical treatments for durability (moisture resistance, fire retardancy) | Treatment protocol |
| B5 | Life-cycle comparison: chosen material vs. conventional acoustic foam | LCA summary table |

### Workstream C: Physical Model Construction
**Lead:** B | **Support:** All

| Task | Description | Output |
|------|-------------|--------|
| C1 | Source materials and tools (cardboard/PVC pipes/3D printing/wood) | Materials list with costs |
| C2 | Build resonator units (3–5 units with different tuning) | Individual resonator prototypes |
| C3 | Assemble full panel with integrated resonators + porous backing | Completed physical model |
| C4 | Aesthetic finishing for presentation (cross-section visible, labeled) | Presentation-ready model |

### Workstream D: Testing & Measurement
**Lead:** A | **Support:** E

| Task | Description | Output |
|------|-------------|--------|
| D1 | Set up measurement rig (impedance tube or speaker-box method with phone app) | Working measurement setup |
| D2 | Measure absorption of individual resonators | Per-resonator frequency response |
| D3 | Measure absorption of full panel | Overall absorption curve |
| D4 | Compare experimental results with theoretical predictions | Validation report |
| D5 | Iterate: identify gaps and propose design improvements | Improvement recommendations |

### Workstream E: Presentation & Documentation
**Lead:** E | **Support:** All

| Task | Description | Output |
|------|-------------|--------|
| E1 | Research and write scientific background section | Background slides/content |
| E2 | Document design process and decisions | Methods section |
| E3 | Create graphs: predicted vs. measured absorption, LCA comparison | Data visualizations |
| E4 | Design poster layout (graphs, photos, diagrams) | Poster draft |
| E5 | Prepare digital presentation slides | Slide deck |

---

## 5. Detailed Timeline

### Phase 1: Planning & Research (June 10–11)
| Date | Activity | Workstream |
|------|----------|------------|
| **June 10 (Tue)** 13:00–13:40 | Introduction, science lecture, initial planning | All |
| **June 10 (Tue)** post-session | Distribute research: Physics principles (A,B), Chemistry/materials (C,D), Applications (E) | All |
| **June 11 (Thu)** 13:00–15:50 | Consolidate research, finalize design concept, assign detailed tasks, begin calculations | All |

### Phase 2: Detailed Design & Preparation (June 12–15, independent work)
| Deadline | Activity | Workstream |
|----------|----------|------------|
| **June 12 (Fri)** | Complete resonator calculations (A1), complete materials characterization (B1) | A, C |
| **June 13 (Sat)** | Finalize CAD/sketches (A2), source materials (C1) | A, B, C |
| **June 14 (Sun)** | Complete simulations (A3, A4), prepare material samples (B3) | A, C |
| **June 15 (Mon)** | Design review: verify all calculations, confirm materials ready | All |

### Phase 3: Build & Test (June 16)
| Date | Activity | Workstream |
|------|----------|------------|
| **June 16 (Tue)** 13:00–15:50 | Build resonator units (C2), set up testing rig (D1), begin assembly | All |
| **June 16 (Tue)** 13:00–15:50 | Initial testing, iterate design if needed (D2, D3, D5) | A, E |

### Phase 4: Analysis & Refinement (June 17–22, independent work)
| Deadline | Activity | Workstream |
|----------|----------|------------|
| **June 17–18** | Complete all measurements, data analysis (D2–D4) | A, E |
| **June 19 (Fri)** | Draft presentation structure, begin poster design (E1–E4) | E |
| **June 20–21** | Refine model, re-test if needed, finalize data visualizations | All |
| **June 22 (Mon)** | Full rehearsal: presentation walkthrough, poster review, model check | All |

### Phase 5: Final Presentation (June 23)
| Time | Activity |
|------|----------|
| 8:00–11:40 | Final preparations, printing, model touch-ups |
| 13:00–14:20 | Continued preparation |
| 14:30–15:50 | **Final Presentation** (Venue A105) |
| 16:00–16:40 | Reflection on ManageBac |

---

## 6. Deliverables Checklist

### Digital Presentation
- [ ] Title slide: project name, topic, team
- [ ] Scientific background: wave physics, metamaterial principles
- [ ] Sustainability framing: environmental problem + solution
- [ ] Design methodology: calculations, material selection rationale
- [ ] Results: predicted vs. measured absorption curves
- [ ] LCA comparison: our material vs. conventional alternatives
- [ ] Conclusion: what we achieved, what we'd improve
- [ ] References

### Poster
- [ ] Eye-catching title and visual layout
- [ ] Key diagram: how acoustic metamaterials work (wave paths, resonance)
- [ ] Photo of physical model with labeled components
- [ ] Main graph: absorption coefficient vs. frequency (predicted + measured)
- [ ] Secondary graph: environmental impact comparison
- [ ] Brief bullet-point conclusions

### Physical Model
- [ ] Visible internal structure (cross-section or transparent side)
- [ ] Labeled components (resonator cavities, necks, porous layer)
- [ ] Sturdy and portable
- [ ] Aesthetic presentation quality

---

## 7. Risk Assessment

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Resonator fabrication inaccurate → wrong tuning | Medium | High | Build extras, allow tuning adjustment (variable cavity volume) |
| Recycled material properties inconsistent | Medium | Medium | Characterize multiple samples, have backup commercial material |
| Measurement setup unreliable | Medium | High | Calibrate with known material, use multiple phone apps cross-checking |
| Model breaks during transport | Low | Medium | Reinforce structure, bring repair kit on presentation day |
| Not enough time for full testing | Medium | Medium | Prioritize 2–3 key frequencies if needed; simulation results are valid backup |
| Team member illness/absence | Low | High | All key knowledge documented; cross-train tasks across members |

---

## 8. Resources Needed

### Materials (estimate)
| Item | Purpose | Est. Cost |
|------|---------|-----------|
| Cardboard/foam board sheets | Main panel structure | ~$5 |
| PVC pipes (various diameters) or 3D-printed parts | Helmholtz resonator bodies | ~$10 |
| Natural fiber felt / recycled fabric | Porous absorption layer | ~$5 |
| Wooden/base frame | Panel housing | ~$5 |
| Hot glue, tape, fasteners | Assembly | ~$3 |
| **Total material cost estimate** | | **~$28** |

### Equipment
- Smartphone with Phyphox or Spectroid app (free) — acoustic measurement
- Laptop with Audacity (free) — tone generation
- Speaker (Bluetooth or wired) — test signal source
- Ruler, utility knife, hot glue gun — construction
- Optional: 3D printer (school FabLab?) — precise resonator fabrication
- Optional: COMSOL Multiphysics (school license?) — advanced simulation

---

## 9. Key References

1. Comandini et al. (2025). "Architected acoustic metamaterials: An integrated design perspective." *Applied Physics Reviews*. — Comprehensive 53-page review of all physical mechanisms.
2. Ciaburro & Puyana-Romero (2025). "Sustainable Membrane-Based Acoustic Metamaterials Using Cork and Honeycomb Structures." *Buildings*, 14(9). — Fully sustainable, recyclable metamaterial.
3. Ciaburro & Puyana-Romero (2026). "Upcycled PVC-Based Metamaterials for Low-Frequency Sound Absorption." *Sustainability*, 18(5). — Waste PVC → acoustic panels.
4. *Building and Environment* (2026). "Blockfold origami ultrathin metamaterials." — 19 mm panel, α>0.85 from 440–1958 Hz.
5. *Nature Communications* (2025). "Deep-subwavelength acoustic-black-hole metamaterials." — 25–1200 Hz absorption, λ/11 thickness.
6. Liu et al. (2000). "Locally Resonant Sonic Materials." *Science*, 289. — The founding paper of acoustic metamaterials.
7. IB Collaborative Sciences Project Guide — Official assessment criteria and requirements.

---

## 10. Appendix: Quick Reference Formulas

```
Speed of sound:       c = 331.3 × √(1 + T/273.15)  [m/s, T in °C]
                      c ≈ 343 m/s at 20°C

Wavelength:           λ = c / f

Helmholtz f₀:         f₀ = (c/2π) × √(A / V·L_eff)
                      L_eff = L_neck + 0.85×d (flanged) or 0.7×d (unflanged)

Quarter-wave tube:    f₀ = c / (4L)

Sound absorption:     α = 1 - |R|²  (where R = reflection coefficient)
                      Measured via impedance tube (ISO 10534-2)

Transmission loss:    STL = 10 × log₁₀(1/τ)  [dB]
                      τ = transmitted / incident power
```
