# 📐 EXPERIMENT PROTOCOL — Standard Operating Procedure

**Every team member must follow this EXACTLY during testing.**

---

## PRINCIPLE: ONE VARIABLE AT A TIME

If you change anything between tests (volume, position, distance), you don't know WHY the result changed. Keep everything identical EXCEPT the panel being tested.

---

## EQUIPMENT CHECKLIST

| # | Item | Check |
|---|------|-------|
| 1 | Smartphone with Phyphox installed | ☐ |
| 2 | Smartphone with Spectroid (backup) | ☐ |
| 3 | Bluetooth speaker or laptop speaker | ☐ |
| 4 | Tripod or phone stand (or tape + books) | ☐ |
| 5 | Measuring tape (at least 30 cm) | ☐ |
| 6 | Masking tape (mark positions) | ☐ |
| 7 | Tone source (YouTube playlist or generated .wav files) | ☐ |
| 8 | Prototypes A, B, C | ☐ |
| 9 | Data recording sheet (printed or digital) | ☐ |
| 10 | Pen and paper (backup recording) | ☐ |

---

## BEFORE YOU START (ONE-TIME SETUP)

### Step 1: Find a Quiet Room
- Close windows and doors
- Turn off fans, AC, and other noise sources
- Ask people nearby to be quiet during testing
- Record ambient noise level: _______ dB (baseline check)

### Step 2: Mark Positions with Tape

```
TOP-DOWN VIEW (looking from above):

    [Speaker]              [Panel Position]        [Phone Mic]
        |                        |                      |
        |←──── 20 cm ──────→|←── 5 cm ──→|
        |                        |                      |
        |←────────── 25 cm total ──────────────────→|
        
    All at same height above table surface
    Mark these positions with tape on the table
```

### Step 3: Fix Speaker Settings
- Connect speaker to phone/laptop
- Set volume to **50–60%** (not max — you want clean sound, not distorted)
- **MARK THE VOLUME POSITION** or take a photo of the volume slider
- **NEVER CHANGE THE VOLUME** between tests

### Step 4: Prepare Tone Playlist

Create a playlist or queue with this order:
1. 250 Hz — 15 seconds
2. Silence — 5 seconds (gap)
3. 500 Hz — 15 seconds
4. Silence — 5 seconds
5. 1000 Hz — 15 seconds
6. Silence — 5 seconds
7. 2000 Hz — 15 seconds

Or test one frequency at a time (recommended for beginners).

---

## TESTING PROCEDURE (DO THIS FOR EACH PROTOTYPE)

### Phase 1: BASELINE (No Panel)

1. Remove any panel from the setup
2. Open Phyphox → "Audio Amplitude" (or "Audio Spectrum")
3. Start Phyphox recording
4. Play 250 Hz tone for 10–15 seconds
5. Stop Phyphox recording
6. Record the average/peak SPL: **Trial 1** = _______ dB
7. Export data as CSV → save as `Baseline_250Hz_Trial1.csv`
8. Wait 10 seconds for the room to settle
9. **REPEAT steps 3–8 two more times** (Trials 2 and 3)
10. Repeat Steps 1–9 for 500 Hz, 1000 Hz, 2000 Hz

### Phase 2: WITH PROTOTYPE

1. Place prototype in the marked panel position
2. **Ensure the panel is centered and perpendicular to the speaker-phone line**
3. Open Phyphox → "Audio Amplitude"
4. Start Phyphox recording
5. Play 250 Hz tone (SAME volume as baseline!)
6. Stop Phyphox recording
7. Record the SPL: **Trial 1** = _______ dB
8. Export data as CSV → save as `PrototypeX_250Hz_Trial1.csv`
9. Wait 10 seconds
10. **REPEAT steps 4–9 two more times** (Trials 2 and 3)
11. Repeat Steps 1–10 for 500 Hz, 1000 Hz, 2000 Hz
12. **REPEAT ENTIRE Phase 2 for each prototype**

---

## TESTING ORDER (Recommended)

| Order | What | Why |
|-------|------|-----|
| 1 | Baseline (all frequencies) | Reference for everything |
| 2 | Prototype A (all frequencies) | Control — worst performer |
| 3 | Prototype B (all frequencies) | Intermediate |
| 4 | Prototype C (all frequencies) | Star performer |
| 5 | Re-test Prototype C (250 Hz, 500 Hz only) | Verify C's low-frequency advantage |

**Total testing time estimate:** ~1.5–2 hours

---

## DATA RECORDING SHEET

### BASELINE (No Panel)

| Frequency | Trial 1 (dB) | Trial 2 (dB) | Trial 3 (dB) | Average (dB) |
|-----------|--------------|--------------|--------------|---------------|
| 250 Hz | | | | |
| 500 Hz | | | | |
| 1000 Hz | | | | |
| 2000 Hz | | | | |

### PROTOTYPE A — Flat Control

| Frequency | Trial 1 (dB) | Trial 2 (dB) | Trial 3 (dB) | Average (dB) | ΔdB (Baseline − Average) |
|-----------|--------------|--------------|--------------|---------------|---------------------------|
| 250 Hz | | | | | |
| 500 Hz | | | | | |
| 1000 Hz | | | | | |
| 2000 Hz | | | | | |

### PROTOTYPE B — Honeycomb

| Frequency | Trial 1 (dB) | Trial 2 (dB) | Trial 3 (dB) | Average (dB) | ΔdB (Baseline − Average) |
|-----------|--------------|--------------|--------------|---------------|---------------------------|
| 250 Hz | | | | | |
| 500 Hz | | | | | |
| 1000 Hz | | | | | |
| 2000 Hz | | | | | |

### PROTOTYPE C — EcoMetaPanel

| Frequency | Trial 1 (dB) | Trial 2 (dB) | Trial 3 (dB) | Average (dB) | ΔdB (Baseline − Average) |
|-----------|--------------|--------------|--------------|---------------|---------------------------|
| 250 Hz | | | | | |
| 500 Hz | | | | | |
| 1000 Hz | | | | | |
| 2000 Hz | | | | | |

---

## QUALITY CHECKS (After Each Test)

- [ ] Are the 3 trials within ±2 dB of each other? (If not, re-test — something changed)
- [ ] Is the ΔdB positive? (If negative, the panel is AMPLIFYING sound — check setup)
- [ ] Did Prototype C block MORE than Prototype A at 250 and 500 Hz? (If not, our hypothesis is wrong — investigate)
- [ ] Are the CSV files saved with the correct names?

---

## TROUBLESHOOTING DURING TESTING

| Problem | Possible Cause | Fix |
|---------|---------------|-----|
| Inconsistent readings | Someone walked by / door opened | Wait for quiet, retest |
| Negative ΔdB (panel makes sound louder) | Panel reflecting sound toward phone | Adjust panel angle, check position |
| All prototypes give same result | The setup isn't sensitive enough | Move phone closer to panel, check speaker position |
| Phyphox crashing | Memory full | Restart phone, close other apps |
| Can't hear 250 Hz clearly | Speaker can't reproduce low frequencies | Use better speaker, or test at 300 Hz instead |
| ΔdB values very small (<1 dB) | Panel too thin or sound leaking around edges | Seal edges with tape, try thicker panel |

---

## ALTERNATIVE METHOD: SPECTROID VISUAL CAPTURE

If Phyphox export isn't working, use Spectroid as backup:

1. Open Spectroid
2. Play the test tone
3. Wait for the display to stabilize (~5 seconds)
4. Take a screenshot
5. Note the peak dB value at the target frequency
6. Use the same dB value for comparison

**Spectroid shows a LIVE frequency spectrum** — very visual, great for screenshots in the presentation!

---

## AMBIENT CONDITIONS (Record These)

| Condition | Value |
|-----------|-------|
| Room temperature | _______ °C |
| Time of day | _______ |
| Ambient noise level | _______ dB |
| Room description | _______ (classroom, hallway, etc.) |
| Phone model | _______ |
| Speaker model | _______ |

---

## AFTER TESTING — IMMEDIATE TASKS

1. [ ] **Backup all CSV files** to two locations
2. [ ] Send data to Student E for analysis
3. [ ] Fill in the Summary Results Table:

### SUMMARY RESULTS

| Prototype | 250 Hz ΔdB | 500 Hz ΔdB | 1000 Hz ΔdB | 2000 Hz ΔdB |
|-----------|------------|------------|-------------|-------------|
| A (Flat) | | | | |
| B (Honeycomb) | | | | |
| C (EcoMetaPanel) | | | | |

### THE KEY TEST (Circle One):
**Did Prototype C outperform Prototype A at 250 Hz and 500 Hz?**

YES / NO

If NO → This is NOT a failure! It's a finding. Explain why. Maybe the resonators were tuned wrong, or the seal wasn't airtight. This makes for a GREAT discussion in the presentation.

---

*This protocol is adapted from ISO 10534-2 (impedance tube method), simplified for smartphone measurement.*
