# 🔨 BUILD INSTRUCTIONS — All Three Prototypes

**Lead Builder: Student B | Support: All Team Members**

---

## GENERAL BUILDING RULES

1. **Measure twice, cut once.**
2. **Hot glue dries fast** — position parts BEFORE gluing.
3. **Seal air gaps** — air leaks kill resonance. Use hot glue or tape on all joints.
4. **Take photos** of every step — you'll use these in the presentation.
5. **Label everything** — write on the back which prototype is which.
6. **Wear safety glasses** when cutting — cardboard dust in eyes is not fun.

---

# PROTOTYPE A — Flat Control Panel

**Purpose:** Baseline — the bare minimum  
**Build Time:** ~15 minutes  
**Difficulty:** ★☆☆☆☆ (Easiest)

### Materials:
- 2 sheets of flat cardboard, 30×30 cm each
- 4 cardboard strips, 30×2 cm (for the frame edge)
- Hot glue or strong tape
- Ruler, craft knife, cutting mat

### Dimensions Summary:
- Width: 30 cm
- Height: 30 cm
- Thickness: 2 cm
- Mass: ~100–200 g

### Build Steps:

1. Cut two 30×30 cm squares from flat cardboard (not corrugated if possible).
2. Cut four 30×2 cm strips for the sides.
3. Glue the strips along the edges of one square, forming a shallow box.
4. Glue the second square on top, sealing the box.
5. Done! This is your control panel.

### Expected Acoustic Behavior:
- Acts as a simple mass barrier
- Slightly better at high frequencies than low
- Provides the baseline against which B and C are compared

---

# PROTOTYPE B — Honeycomb Sustainable Panel

**Purpose:** Show that geometric structure matters  
**Build Time:** ~45–60 minutes  
**Difficulty:** ★★★☆☆ (Moderate)

### Materials:
- Corrugated cardboard (the wavy kind), enough for ~30 strips
- 1 sheet flat cardboard, 30×30 cm (front face with holes)
- 1 sheet flat cardboard, 30×30 cm (solid back)
- 4 cardboard strips, 30×4 cm (side walls)
- Hot glue, ruler, craft knife

### Dimensions Summary:
- Width: 30 cm
- Height: 30 cm
- Thickness: 3–5 cm (the deeper, the better the effect)
- Honeycomb cell size: ~3–4 cm per cell
- Mass: ~300–500 g

### Build Steps:

#### Step 1: Prepare the Frame
1. Cut the 4 side strips (30×4 cm)
2. Glue them onto the back panel edges, forming an open box

#### Step 2: Make the Honeycomb Grid
**Option A: Square grid (easier)**
1. Cut corrugated cardboard into strips, 4 cm wide × 30 cm long
2. Cut slots halfway through each strip at 4 cm intervals
3. Interlock the strips to form a grid:

```
┌──┬──┬──┬──┬──┬──┬──┐
│  │  │  │  │  │  │  │
├──┼──┼──┼──┼──┼──┼──┤
│  │  │  │  │  │  │  │
├──┼──┼──┼──┼──┼──┼──┤  ← Interlocking cardboard strips
│  │  │  │  │  │  │  │
├──┼──┼──┼──┼──┼──┼──┤
│  │  │  │  │  │  │  │
└──┴──┴──┴──┴──┴──┴──┘
```

**Option B: Hexagonal honeycomb (harder, looks cooler)**

1. Cut corrugated cardboard into strips, 4 cm wide
2. Accordion-fold each strip into a hexagon pattern
3. Glue hexagons together side-by-side

#### Step 3: Add the Perforated Front Face
1. Cut a 30×30 cm piece of thin cardboard
2. Poke or cut small holes (~5 mm diameter) across the entire surface
3. Spacing: ~2 cm between holes
4. Glue this onto the front of the honeycomb frame

#### Step 4: Seal and Finish
1. Check all glue joints — reapply if loose
2. The panel should feel sturdy but not heavy
3. You should be able to see through the holes into the honeycomb

### Expected Acoustic Behavior:
- Honeycomb creates multiple small air cavities
- Each cavity acts as a mini absorber
- Corrugation increases surface area for viscous losses
- Should outperform Prototype A by 1–4 dB

---

# PROTOTYPE C — EcoMetaPanel (THE MAIN EVENT)

**Purpose:** Demonstrate acoustic metamaterial principles with tuned resonators  
**Build Time:** ~2–3 hours  
**Difficulty:** ★★★★★ (Most Complex — but doable!)

### Materials:
- 1 rigid cardboard box frame, 30×30 cm outside, ~5 cm deep
- 4 resonator containers (plastic bottles or cardboard boxes of different sizes)
- Neck materials: Plastic straws, small PVC tubes, or rolled paper tubes
- 1 sheet recycled fabric/felt, 30×30 cm (porous backing)
- 1 sheet thin cardboard, 30×30 cm (front face)
- Hot glue (lots), duct tape, ruler, craft knife

### Dimensions Summary:
- Width: 30 cm
- Height: 30 cm
- Thickness: 5 cm (maximum)
- 4 Helmholtz resonators tuned to 250, 500, 750, 1000 Hz
- Mass: ~400–800 g

### Design Concept:

```
┌──────────────────────────────────────────┐
│  FRONT FACE (thin cardboard with holes)    │
│     ○          ○          ○          ○     │  ← Neck openings
├──────────────────────────────────────────┤
│  ┌────────┐ ┌────────┐ ┌────────┐ ┌────┐ │
│  │ 250 Hz │ │ 500 Hz │ │ 750 Hz │ │1000│ │  ← Resonator cavities
│  │bottle  │ │bottle  │ │bottle  │ │ Hz │ │
│  │        │ │        │ │        │ │box │ │
│  └────────┘ └────────┘ └────────┘ └────┘ │
├──────────────────────────────────────────┤
│  POROUS BACKING (recycled fabric/felt)     │  ← Broadband absorber
└──────────────────────────────────────────┘
```

### Build Steps:

#### Step 1: Build the Frame
1. Construct a sturdy cardboard box, 30×30 cm, 5 cm deep
2. Leave the front open (will add face later)
3. Leave the back open (will add fabric backing)
4. Reinforce corners with extra tape

#### Step 2: Create Resonator 1 (Target: 250 Hz)
1. Use Student A's calculations from `02_PHYSICS_WORKBOOK.md`
2. Choose the largest container (~500 mL bottle)
3. Cut the bottle to the calculated cavity volume if needed
4. Attach the neck (straw/tube) to the bottle opening
5. Adjust neck length to hit calculated L_eff
6. Seal the neck-bottle joint with hot glue — MUST BE AIRTIGHT
7. Test: blow across the top and listen for the resonant "whoosh"

#### Step 3: Create Resonators 2, 3, and 4
1. Repeat Step 2 for 500 Hz, 750 Hz, and 1000 Hz
2. Each resonator should be smaller than the previous one
3. Higher frequency = smaller cavity OR shorter/wider neck

**Rule of thumb:**
| Target f₀ | Approximate Cavity | Approximate Neck |
|-----------|-------------------|------------------|
| 250 Hz | ~500 mL bottle | ~2 cm long, ~2 cm diameter |
| 500 Hz | ~250 mL (half bottle) | ~1.5 cm long, ~2 cm diameter |
| 750 Hz | ~150 mL (cut bottle) | ~1 cm long, ~2 cm diameter |
| 1000 Hz | ~100 mL (small box) | ~1 cm long, ~2 cm diameter |

*These are APPROXIMATE — USE Student A'S CALCULATED VALUES!*

#### Step 4: Mount Resonators in the Frame
1. Arrange the 4 resonators evenly in the frame (see layout diagram)
2. Glue each resonator to the back of the frame
3. Ensure all necks face FORWARD (toward the sound source)
4. Neck openings should be flush with the front face

#### Step 5: Add the Porous Backing
1. Cut fabric/felt to 30×30 cm
2. Stretch it across the back of the frame
3. Glue or tape the edges securely
4. The fabric should be taut but not overstretched

#### Step 6: Add the Front Face
1. Cut thin cardboard to 30×30 cm
2. Mark the positions of the 4 resonator necks
3. Cut holes at those positions — holes should match neck diameter EXACTLY
4. Glue the front face onto the frame
5. Ensure neck openings are flush with the front surface

#### Step 7: Quality Check
- [ ] All resonators are securely mounted and won't rattle
- [ ] All neck joints are airtight (no gaps)
- [ ] Fabric backing is attached on all sides
- [ ] Front face holes align with necks
- [ ] The panel stands on its own
- [ ] Blowing across each neck produces a resonant tone

### Quick Resonator Test (Before Full Assembly):

1. Hold a resonator to your ear
2. Tap the side gently with a finger
3. You should hear a "boing" at the resonant frequency
4. Compare with a tone generator app — does it match?

---

## ASSEMBLY DAY WORKFLOW (June 16)

| Time | Activity | Who |
|------|----------|-----|
| 0:00–0:15 | Set up workspace, gather all materials | All |
| 0:15–0:30 | Build Prototype A | Student B + Student C |
| 0:30–1:15 | Build Prototype B | Student B + Student D |
| 1:15–3:30 | Build Prototype C | Student B (lead) + All |
| 3:30–3:50 | Quality check all prototypes | Student A |
| 3:50–4:30 | Touch-up, labels, photos | Student F + All |

**Concurrent work:** While Student B builds, Student C and Student D prepare material samples for testing. Student E sets up the testing equipment with Student G. Student A reviews and prepares the data sheets. Student F photographs every stage.

---

## PRESENTATION-READY FINISHING

### For Each Prototype:
- [ ] Clean edges (trim excess glue, straighten cuts)
- [ ] Add a small label: "Prototype A/B/C" on the back
- [ ] Note materials used on a card attached to the back
- [ ] Take a beauty photo against a clean background

### For Prototype C (Physical Model):
- [ ] **Create a cross-section view** — if you can, cut one side to show internal structure
- [ ] Alternatively, build a SECOND copy with one side left open for display
- [ ] Label: Resonator cavities, neck openings, porous backing, front face
- [ ] Add arrows showing sound path: IN → through neck → into cavity → absorbed by fabric

### Display Option:
```
         ┌─────────────────────┐
         │   PROTOTYPE PANEL   │
         │                     │
  Sound  │  [Visible internal  │  Attenuated
  ──────→│   structure with   │──────→
  IN     │   labeled parts]   │  Sound OUT
         │                     │
         └─────────────────────┘
```

---

## SAFETY NOTES

- Use a cutting mat or thick cardboard underneath when cutting
- Hot glue gun tips reach ~190°C — don't touch!
- Cardboard edges can be sharp — sand or tape edges if needed
- Work in a well-ventilated area (hot glue fumes)
- Clean up immediately — cardboard scraps are trip hazards

---

*When all prototypes are built, hand them to Student A for testing!*
