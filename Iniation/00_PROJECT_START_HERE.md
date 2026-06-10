# 🚀 START HERE — Group 4 Collaborative Sciences Project

**Project:** EcoMetaPanel — Sustainable Acoustic Metamaterial Wall Panel  
**Topic:** Acoustic Metamaterials (Topic 1)  
**Date:** 10 June 2026 | **Phase:** Initiation → Planning  

---

## ⏱️ READ THIS FIRST (2 minutes)

You have **13 days** to go from idea → presentation. Here's the big picture:

| Milestone | Date | What Happens |
|-----------|------|--------------|
| 🧠 Planning | June 10–11 | Define the plan, assign roles, do research |
| 🔬 Build & Test | June 16 | Construct prototypes, run experiments |
| 📊 Analysis | June 17–22 | Analyze data, make graphs, build presentation |
| 🎤 **PRESENT** | **June 23** | Final presentation + poster + physical model |

**You need to deliver 3 things:**
1. Digital Presentation (10–12 min slides)
2. Poster (with graphs, photos, diagrams)
3. Physical Model (cross-section showing internal structure)

---

## 👥 YOUR TEAM

| Student | Role | Subject Strength | Key Jobs |
|---------|------|------------------|----------|
| **Student A** | Group Leader | Physics | Acoustic calculations, resonator design, testing lead |
| **Student B** | Deputy Leader | Physics | CAD sketches, prototype construction, assembly |
| **Student C** | Chemistry Lead | Chemistry | Material characterization, density/porosity testing |
| **Student D** | Chemistry Support | Chemistry | Sustainability research, LCA, material sourcing |
| **Student E** | CS Lead | Computer Science | Data collection, FFT analysis, graphs, presentation |
| **Student F** | Documentation & Media | General | Photography, process documentation, poster layout, visual polish |
| **Student G** | Testing & Data Support | General | Experimental assistance, data verification, equipment management |

---

## 🎯 YOUR GOAL IN ONE SENTENCE

**Build a sound-absorbing panel from recycled materials that beats a flat panel at blocking low-frequency noise (200–1000 Hz), and prove it with data.**

---

## 📂 HOW TO USE THIS FOLDER

```
Iniation/
├── 00_PROJECT_START_HERE.md     ← YOU ARE HERE
├── 01_ROLE_ASSIGNMENTS.md        ← Who does exactly what, day by day
├── 02_PHYSICS_WORKBOOK.md        ← Student A & Student B: calculations & design
├── 03_CHEMISTRY_WORKBOOK.md      ← Student C & Student D: materials & sustainability
├── 04_CS_WORKBOOK.md             ← Student E: software, data, graphs
├── 05_EXPERIMENT_PROTOCOL.md     ← The testing procedure everyone follows
├── 06_BUILD_INSTRUCTIONS.md      ← Step-by-step prototype construction
└── 07_CHECKLIST_AND_DEADLINES.md ← Track everything, don't miss anything
```

**Read this file first, then jump to your role's workbook.**

---

## 🔬 THE SCIENCE (Simplified)

### What are acoustic metamaterials?

Normal materials absorb sound through their mass and porosity (like foam). Acoustic metamaterials absorb sound through their **shape and structure** — even when they're thin and light.

### How they work:

1. **Helmholtz Resonance** — Like blowing across a bottle top. Air in the neck vibrates against the air spring in the cavity. At the right frequency, sound energy converts to heat.

2. **Longer Sound Path** — Folded channels make sound travel further than the panel is thick. A 5 cm panel can act like a 34 cm path.

3. **Thermoviscous Losses** — In narrow channels, air friction turns sound energy into tiny amounts of heat.

### The Key Formula (Helmholtz Resonator):

```
f₀ = (c / 2π) × √(A / (V × L_eff))

f₀    = resonance frequency (Hz) — the pitch it absorbs best
c     = speed of sound (≈343 m/s at 20°C)
A     = area of the neck opening (m²)
V     = cavity volume (m³)
L_eff = effective neck length (actual length + correction)
```

---

## 🏗️ THE THREE PROTOTYPES

### Prototype A — Flat Control Panel
- **What:** Plain flat cardboard, 30×30 cm, ~2 cm thick
- **Purpose:** Baseline — the minimum performance
- **Expected:** Lowest sound absorption
- **Build time:** 15 minutes

### Prototype B — Honeycomb Panel
- **What:** Cardboard honeycomb structure, 30×30 cm, ~3–5 cm thick
- **Purpose:** Show that geometry alone improves absorption
- **Expected:** Moderate absorption, better than A
- **Build time:** 45–60 minutes

### Prototype C — EcoMetaPanel (THE STAR)
- **What:** Multiple tuned Helmholtz resonators + folded channels + fabric backing
- **Purpose:** Best low-frequency absorption using recycled materials
- **Expected:** Highest attenuation at 250–1000 Hz
- **Build time:** 2–3 hours

---

## 📐 KEY DIMENSIONS & TARGETS

| Parameter | Value |
|-----------|-------|
| Panel size | 30 cm × 30 cm (max) |
| Panel thickness | ≤ 5 cm |
| Target frequencies | 250 Hz, 500 Hz, 1000 Hz, 2000 Hz |
| Primary materials | Recycled cardboard, plastic bottles, PVC tubing, fabric |
| Measurement tool | Smartphone + Phyphox or Spectroid app (free) |
| Sound source | Bluetooth speaker + tone generator app |

---

## ⚡ IMMEDIATE ACTIONS (June 10–11)

### TODAY (June 10):
- [ ] Everyone reads this guide
- [ ] Everyone reads their role workbook
- [ ] Student A: Start resonator calculations for 250 Hz and 500 Hz
- [ ] Student C & Student D: Gather available recycled materials, start weighing/measuring
- [ ] Student B: Sketch initial panel designs
- [ ] Student E: Install Python + libraries (numpy, scipy, matplotlib), test Phyphox app
- [ ] Student F: Review all guides, prepare photo documentation plan, set up shared photo album
- [ ] Student G: Install and test Phyphox + Spectroid apps, review experiment protocol

### TOMORROW (June 11):
- [ ] Full team meeting: review calculations, finalize design
- [ ] Confirm material availability
- [ ] Complete detailed task assignments
- [ ] Begin prototype construction planning

---

## 🛠️ MATERIALS SHOPPING LIST

| Item | Quantity | For | Est. Cost |
|------|----------|-----|-----------|
| Corrugated cardboard sheets | 5–6 large pieces | All prototypes | Free (recycled) |
| Plastic bottles (500mL) | 6–8 | Prototype C resonators | Free (recycled) |
| PVC pipe scraps (various diameters) | 4–6 pieces | Prototype C necks | ~$5 |
| Old fabric/felt/cloth | 1 piece (30×30 cm) | Porous backing layer | Free (recycled) |
| Hot glue sticks | 10–15 | Assembly | ~$3 |
| Duct tape / masking tape | 1 roll | Assembly, marking positions | ~$2 |
| Craft knife / scissors | 1 each | Cutting | Already have |
| Ruler (30 cm) | 1 | Measuring | Already have |
| **TOTAL** | | | **~$10** |

**Principle: Use recycled/free materials wherever possible. This IS the sustainability story.**

---

## 📱 APPS TO INSTALL NOW

1. **Phyphox** (iOS/Android, free) — Use "Audio Amplitude" or "Audio Spectrum" mode
2. **Spectroid** (Android, free) — Real-time frequency spectrum display
3. **Tone Generator** or use YouTube — Search "250 Hz test tone", "500 Hz test tone", etc.

---

## 🚨 COMMON MISTAKES TO AVOID

1. ❌ **No control group** — Always measure baseline (no panel) before testing
2. ❌ **Moving the phone/speaker between tests** — Mark positions with tape
3. ❌ **Testing in noisy environments** — Find the quietest room possible
4. ❌ **Only testing once** — Minimum 3 measurements per test, take the average
5. ❌ **Changing two variables at once** — Change only one thing per experiment
6. ❌ **Forgetting to document** — Take photos of EVERYTHING, write down EVERY measurement

---

## 📞 COMMUNICATION PLAN

- **Group chat:** Share photos of progress, measurements, questions
- **Shared document:** Google Docs or similar for collaborative writing
- **File naming:** Use clear names like `PrototypeA_test_500Hz_trial1.csv`
- **Backup:** Save everything in at least two places

---

*Now go to your role workbook and start working!*
