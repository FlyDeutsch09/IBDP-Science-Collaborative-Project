# 🧪 CHEMISTRY WORKBOOK — Student C (Lead) & Student D (Sustainability)

**This is your complete guide to the materials science of the project.**

---

## PART 1: YOUR SCIENTIFIC CONTRIBUTION

In this project, Chemistry explains:

1. **WHY materials behave differently** — density, porosity, fiber structure → acoustic properties
2. **WHICH materials to choose** — data-driven material selection
3. **WHY sustainability matters** — environmental impact comparison
4. **HOW materials can be improved** — treatments, composites, end-of-life

**Your data appears in:** Presentation slides, poster graphs, physical model labels.

---

## PART 2: MATERIAL CHARACTERIZATION

### Required Measurements for EVERY Material

| Property | How to Measure | Equipment Needed | Unit |
|----------|---------------|------------------|------|
| Mass | Weigh on balance/scale | Kitchen scale or lab balance | grams (g) |
| Volume | Length×Width×Height (regular) or water displacement (irregular) | Ruler or measuring cylinder | cm³ |
| Density | ρ = mass/volume | Calculator | g/cm³ |
| Porosity | Water absorption test (see below) | Water, dropper, timer | Qualitative or % |
| Surface texture | Visual + touch inspection | Your senses | Descriptive |

### Simple Porosity Test:

1. Cut a small sample of each material (~5×5 cm)
2. Place one drop of water on the surface
3. Time how long it takes to absorb
4. Rate: **Fast (<5 sec)** = High porosity | **Medium (5–30 sec)** = Moderate | **Slow (>30 sec)** = Low porosity | **Never** = Non-porous

### Material Data Sheet Template:

| Material | Mass (g) | Dimensions (cm) | Volume (cm³) | Density (g/cm³) | Porosity | Texture |
|----------|----------|------------------|--------------|-----------------|----------|---------|
| Corrugated cardboard | | | | | | |
| Flat cardboard | | | | | | |
| Cotton fabric | | | | | | |
| Felt | | | | | | |
| Plastic bottle (PET) | | | | | | |
| Cork (if available) | | | | | | |
| Newspaper (compressed) | | | | | | |
| Bubble wrap | | | | | | |
| Egg carton | | | | | | |
| Other: ________ | | | | | | |

---

## PART 3: HOW MATERIAL PROPERTIES AFFECT SOUND

### The Science:

```
Sound Absorption Mechanism:

High porosity → Sound enters material easily
                  ↓
Tortuous path → Air molecules rub against fibers
                  ↓
Friction → Kinetic energy → Thermal energy (heat)
                  ↓
              SOUND ABSORBED
```

### Material Property → Acoustic Effect:

| Material Property | Effect on Sound | Why |
|-------------------|-----------------|-----|
| **High porosity** | Better high-frequency absorption | More air channels for viscous dissipation |
| **High density** | Better low-frequency blocking | More mass = harder to vibrate (mass law) |
| **Fibrous structure** | Good broadband absorption | Tortuous paths at multiple scales |
| **Closed cells** (e.g., styrofoam) | Poor absorption, good reflection | Sound can't enter the material |
| **Open cells** (e.g., sponge, felt) | Good absorption | Sound enters and dissipates |
| **Viscoelastic** (e.g., rubbery) | Good damping | Converts vibration to heat efficiently |
| **Rigid and smooth** | Good reflection | Sound bounces off without entering |

### Material Ranking for Our Project:

| Material | Best For | Limitation |
|----------|----------|------------|
| **Corrugated cardboard** | Structural body + honeycomb | Not durable when wet |
| **Felt/fabric** | Porous absorption backing | Needs support structure |
| **Plastic bottles (PET)** | Helmholtz cavity (rigid walls) | Hard to cut precisely |
| **PVC pipe/tubing** | Resonator neck (precise diameter) | Sourcing specific sizes |
| **Cork** | Vibration damping layer | May not be available recycled |
| **Newspaper (compressed)** | Filler, extra mass | Compresses over time, fire risk |
| **Egg carton** | Diffusive surface (scatters sound) | Limited structural strength |

---

## PART 4: PROTOTYPE-SPECIFIC MATERIAL RECOMMENDATIONS

### Prototype A (Flat Control):
- **Layer 1 (front face):** Flat cardboard, 30×30 cm
- **Layer 2 (backing):** Flat cardboard, 30×30 cm
- **Spacer:** Cardboard strips around edges, 2 cm thick
- **Total thickness:** ~2 cm
- **Chemistry note:** This is essentially a limp mass barrier. Performance follows Mass Law: STL increases ~6 dB per doubling of mass.

### Prototype B (Honeycomb):
- **Frame:** Cardboard box frame, 30×30 cm, 3–5 cm deep
- **Honeycomb cells:** Strips of corrugated cardboard, ~3–5 cm wide, arranged in hexagonal or square grid
- **Front face:** Thin cardboard with small holes (perforated)
- **Back face:** Solid cardboard
- **Chemistry note:** The air pockets in honeycomb cells create multiple small cavities. Each acts as a mini absorber. Corrugation provides additional surface area.

### Prototype C (EcoMetaPanel — The Star):
- **Frame:** Rigid cardboard frame, 30×30 cm, 5 cm deep
- **Resonator bodies:** Plastic bottles (PET) or cardboard boxes
- **Resonator necks:** Plastic straws, small PVC tubes, or rolled paper tubes
- **Porous backing:** Recycled fabric/felt, ~5 mm thick, covering entire back
- **Sealant:** Hot glue or tape — must be AIRTIGHT around resonator necks
- **Chemistry note:** This is a HYBRID system. The resonators provide tuned narrowband absorption (Helmholtz). The fabric backing provides broadband absorption. Together they cover more frequencies than either alone.

---

## PART 5: SUSTAINABILITY ASSESSMENT (Student D Lead)

### Life Cycle Assessment Framework:

Compare your EcoMetaPanel materials against conventional acoustic foam (polyurethane or melamine foam).

| Criterion | Conventional Acoustic Foam | Our EcoMetaPanel | Winner |
|-----------|---------------------------|------------------|--------|
| **Raw material** | Petroleum-based (fossil fuel) | Recycled waste (cardboard, PET) | EcoMetaPanel |
| **Manufacturing energy** | High (polymerization, foaming) | Low (cutting, gluing, hand assembly) | EcoMetaPanel |
| **Toxicity (VOCs)** | Can off-gas formaldehyde | None (unless glue has VOCs) | EcoMetaPanel |
| **Recyclability** | Difficult (thermoset foam) | Easy (cardboard recyclable, PET recyclable) | EcoMetaPanel |
| **Biodegradability** | Centuries (non-biodegradable) | Cardboard: months; PET: decades | Mixed |
| **Performance at low freq** | Poor (needs 30+ cm for 250 Hz) | Good (5 cm via resonance) | EcoMetaPanel |
| **Cost** | $20–50/m² | ~$5/m² (mostly free materials) | EcoMetaPanel |
| **Fire safety** | Melamine: good; PU: poor (toxic smoke) | Cardboard: poor without treatment | Conventional |
| **Durability/humidity** | Good | Poor (cardboard absorbs moisture) | Conventional |

### Key Sustainability Talking Points:

1. **Dual waste solution:** Our panel addresses TWO environmental problems at once — noise pollution AND material waste.

2. **Circular economy:** Materials are sourced from waste streams, used in a long-life building product, and can be recycled again at end-of-life.

3. **Low embodied energy:** Hand assembly with simple tools. No high-temperature processing. Minimal energy input compared to manufacturing acoustic foam.

4. **Local materials:** Using locally available waste eliminates transportation emissions.

5. **bio-inspiration:** Our honeycomb design is inspired by natural bee structures — efficient geometry with minimal material.

### The Numbers (if you can find/estimate):

- Mass of recycled material per panel: ~_____ g
- Estimated CO₂ saved vs. new acoustic foam: ~_____ kg CO₂-eq
- Recycled content percentage: _____%
- Distance materials traveled (ideally <10 km for local waste): _____ km

---

## PART 6: YOUR DELIVERABLES

### For the Presentation:

**Slide: "Materials Science"**
- Show the material comparison table
- Explain porosity → absorption relationship
- Highlight WHY felt + cardboard + PET work together
- Include a photo of materials in raw form vs. finished panel

**Slide: "Environmental Impact"**
- LCA comparison table (conventional vs. EcoMetaPanel)
- Visual: bar chart comparing carbon footprint
- Specific numbers with sources
- Statement about circular economy

### For the Poster:

- Material ranking matrix (density, porosity, sustainability score)
- Photo showing material samples with labels
- Mini LCA comparison graphic

### For the Physical Model:

- Labels on the model indicating materials used
- Cross-section showing different material layers
- Note: "100% recycled content" if true (or state the actual %)

---

## PART 7: TREATMENT CONSIDERATIONS (Optional Enhancement)

If you want to address the cardboard/water vulnerability:

| Treatment | What It Does | How To Apply |
|-----------|-------------|--------------|
| Wax coating (beeswax or candle wax) | Water resistance | Rub wax on surface, heat gently to absorb |
| PVA glue seal (white glue + water, 1:1) | Stiffens + slight moisture resistance | Paint on, let dry |
| Salt solution soak | Natural fire retardant | Dissolve salt in water, soak, dry completely |
| Borax solution | Fire + pest resistance | Dissolve, spray on, dry |

**Note:** Any treatment changes the acoustic properties! Test before and after.

---

## KEY TERMS FOR YOUR PRESENTATION

- **Porosity:** Percentage of void space in a material
- **Tortuosity:** How twisted/indirect the path through pores is
- **Viscoelasticity:** Material deforms AND flows under stress → damping
- **Mass Law:** Heavier materials block more sound (especially low frequencies)
- **Embodied carbon:** CO₂ emitted during material production
- **Circular economy:** Materials stay in use, not in landfill
- **VOCs:** Volatile Organic Compounds — bad for indoor air quality

---

*Share your completed material data sheet with the team before June 11 session.*
