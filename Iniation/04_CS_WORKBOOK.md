# 💻 COMPUTER SCIENCE WORKBOOK — Student E

**This is your complete guide to the data analysis and presentation technology.**

---

## PART 1: YOUR ROLE

You are the bridge between raw experimental data and the final presentation. Your job is to:

1. **Collect** — Ensure data is properly recorded and saved
2. **Analyze** — Process audio, perform FFT, calculate metrics
3. **Visualize** — Create publication-quality graphs
4. **Present** — Design slides and poster layout
5. **Archive** — Keep everything organized and reproducible

---

## PART 2: SOFTWARE SETUP (Do This TODAY)

### Required Software:

```
Python 3.x (any version 3.8+)
  ↓
Install these libraries (run in terminal/command prompt):
  pip install numpy scipy matplotlib
  ↓
Optional but helpful:
  pip install pandas soundfile jupyter
```

### Phone Apps (test today):

| App | Platform | What It Does | Export Format |
|-----|----------|--------------|---------------|
| **Phyphox** | iOS + Android | Audio Spectrum, Audio Amplitude | CSV, Excel |
| **Spectroid** | Android | Real-time spectrogram | Screenshot only |
| **Audacity** (laptop) | Win/Mac/Linux | Record, generate tones, analyze | .wav, .mp3 |

### Tone Generation:

**Option A:** YouTube — Search "250 Hz pure tone", "500 Hz sine wave", etc.  
**Option B:** Generate with Python (see Part 3)  
**Option C:** Audacity → Generate → Tone → [frequency] Hz → Export as .wav

---

## PART 3: PYTHON CODE TEMPLATES

### Template 1: Generate Test Tones

```python
import numpy as np
from scipy.io import wavfile

def generate_tone(frequency, duration=5.0, sample_rate=44100, amplitude=0.5):
    """Generate a pure sine wave tone."""
    t = np.linspace(0, duration, int(sample_rate * duration), endpoint=False)
    signal = amplitude * np.sin(2 * np.pi * frequency * t)
    # Fade in/out to avoid clicks
    fade_samples = int(sample_rate * 0.01)  # 10ms fade
    fade_in = np.linspace(0, 1, fade_samples)
    fade_out = np.linspace(1, 0, fade_samples)
    signal[:fade_samples] *= fade_in
    signal[-fade_samples:] *= fade_out
    return signal, sample_rate

# Generate all test frequencies
for freq in [250, 500, 1000, 2000]:
    signal, sr = generate_tone(freq, duration=10.0)
    wavfile.write(f'tone_{freq}Hz.wav', sr, (signal * 32767).astype(np.int16))
    print(f'Created tone_{freq}Hz.wav')
```

### Template 2: Perform FFT Analysis

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.io import wavfile
from scipy.signal import welch

def analyze_audio(filepath, title="Audio Spectrum"):
    """Load audio file and compute frequency spectrum."""
    # Load audio
    sample_rate, data = wavfile.read(filepath)
    
    # Convert to mono if stereo
    if len(data.shape) > 1:
        data = data.mean(axis=1)
    
    # Normalize
    data = data / np.max(np.abs(data))
    
    # Compute power spectral density using Welch's method
    frequencies, psd = welch(data, sample_rate, nperseg=4096)
    
    # Convert to dB scale
    psd_db = 10 * np.log10(psd + 1e-12)
    
    # Plot
    fig, ax = plt.subplots(figsize=(10, 5))
    ax.semilogx(frequencies, psd_db)
    ax.set_xlabel('Frequency (Hz)')
    ax.set_ylabel('Power/Frequency (dB/Hz)')
    ax.set_title(title)
    ax.set_xlim([20, 5000])  # Focus on our range
    ax.grid(True, alpha=0.3)
    
    # Mark target frequencies
    for f_target in [250, 500, 1000, 2000]:
        ax.axvline(x=f_target, color='red', linestyle='--', alpha=0.5, 
                   label=f'{f_target} Hz' if f_target == 250 else None)
    
    ax.legend()
    plt.tight_layout()
    plt.savefig(f'{title.replace(" ", "_")}.png', dpi=150)
    plt.show()
    
    return frequencies, psd_db

# Example usage:
# freqs, psd = analyze_audio('recording_baseline.wav', 'Baseline - No Panel')
```

### Template 3: Compare Before/After Spectra

```python
def compare_spectra(baseline_file, with_panel_file, panel_name, frequency):
    """Overlay two spectra and calculate dB reduction."""
    sr1, data1 = wavfile.read(baseline_file)
    sr2, data2 = wavfile.read(with_panel_file)
    
    if len(data1.shape) > 1:
        data1 = data1.mean(axis=1)
    if len(data2.shape) > 1:
        data2 = data2.mean(axis=1)
    
    # Compute PSD for both
    f1, psd1 = welch(data1/np.max(np.abs(data1)), sr1, nperseg=4096)
    f2, psd2 = welch(data2/np.max(np.abs(data2)), sr2, nperseg=4096)
    
    psd1_db = 10 * np.log10(psd1 + 1e-12)
    psd2_db = 10 * np.log10(psd2 + 1e-12)
    
    # Find the reduction at the target frequency
    idx_target = np.argmin(np.abs(f1 - frequency))
    reduction = psd1_db[idx_target] - psd2_db[idx_target]
    
    # Plot overlay
    fig, ax = plt.subplots(figsize=(10, 5))
    ax.semilogx(f1, psd1_db, 'b-', alpha=0.7, label='Baseline (no panel)')
    ax.semilogx(f2, psd2_db, 'r-', alpha=0.7, label=f'With {panel_name}')
    ax.axvline(x=frequency, color='green', linestyle='--', 
               label=f'{frequency} Hz: Δ = {reduction:.1f} dB')
    ax.set_xlabel('Frequency (Hz)')
    ax.set_ylabel('Power/Frequency (dB/Hz)')
    ax.set_title(f'{panel_name} at {frequency} Hz\nSound Reduction: {reduction:.1f} dB')
    ax.set_xlim([20, 5000])
    ax.legend()
    ax.grid(True, alpha=0.3)
    plt.tight_layout()
    plt.savefig(f'compare_{panel_name}_{frequency}Hz.png', dpi=150)
    plt.show()
    
    return reduction

# Example usage:
# reduction = compare_spectra('baseline_500Hz.wav', 'prototypeC_500Hz.wav', 
#                              'Prototype C', 500)
# print(f'Sound reduction: {reduction:.1f} dB')
```

### Template 4: Bar Chart — All Prototypes Compared

```python
def plot_comparison_barchart(results_dict):
    """
    results_dict = {
        '250 Hz': {'Prototype A': 1.2, 'Prototype B': 2.8, 'Prototype C': 5.3},
        '500 Hz': {'Prototype A': 2.1, 'Prototype B': 3.5, 'Prototype C': 7.1},
        ...
    }
    """
    frequencies = list(results_dict.keys())
    prototypes = list(results_dict[frequencies[0]].keys())
    
    x = np.arange(len(frequencies))
    width = 0.25
    multiplier = 0
    
    fig, ax = plt.subplots(figsize=(10, 6))
    
    colors = ['#95a5a6', '#3498db', '#27ae60']
    
    for i, proto in enumerate(prototypes):
        values = [results_dict[f][proto] for f in frequencies]
        offset = width * (i - 1)
        bars = ax.bar(x + offset, values, width, label=proto, color=colors[i])
        
        # Add value labels on bars
        for bar in bars:
            height = bar.get_height()
            ax.text(bar.get_x() + bar.get_width()/2., height + 0.2,
                    f'{height:.1f}', ha='center', va='bottom', fontsize=9)
    
    ax.set_xlabel('Frequency')
    ax.set_ylabel('Sound Reduction (ΔdB)')
    ax.set_title('Sound Attenuation by Prototype and Frequency')
    ax.set_xticks(x)
    ax.set_xticklabels(frequencies)
    ax.legend(loc='upper left')
    ax.grid(True, axis='y', alpha=0.3)
    
    plt.tight_layout()
    plt.savefig('attenuation_comparison.png', dpi=150)
    plt.show()
```

### Template 5: Theory vs. Experiment Plot

```python
def plot_theory_vs_experiment(theory, experiment):
    """
    theory = {'250': 8.5, '500': 7.2, '750': 6.8, '1000': 5.9}
    experiment = {'250': 5.3, '500': 7.1, '750': 4.2, '1000': 3.8}
    """
    freqs = list(theory.keys())
    freqs_num = [int(f) for f in freqs]
    
    fig, ax = plt.subplots(figsize=(8, 5))
    ax.plot(freqs_num, list(theory.values()), 'b-o', label='Theory (predicted)', 
            linewidth=2, markersize=8)
    ax.plot(freqs_num, list(experiment.values()), 'r-s', label='Experiment (measured)', 
            linewidth=2, markersize=8)
    
    # Fill the gap
    ax.fill_between(freqs_num, list(theory.values()), list(experiment.values()), 
                     alpha=0.2, color='gray', label='Error')
    
    ax.set_xlabel('Frequency (Hz)')
    ax.set_ylabel('Sound Reduction (ΔdB)')
    ax.set_title('Theory vs. Experiment: Prototype C Performance')
    ax.legend()
    ax.grid(True, alpha=0.3)
    
    plt.tight_layout()
    plt.savefig('theory_vs_experiment.png', dpi=150)
    plt.show()
```

---

## PART 4: DATA COLLECTION PLAN

### On Testing Day (June 16):

1. **Before testing starts:**
   - [ ] Create folder structure: `Data/Raw/`, `Data/Processed/`, `Graphs/`
   - [ ] Test the tone generation/speaker setup
   - [ ] Test Phyphox export to CSV
   - [ ] Bring laptop charger!

2. **During testing:**
   - [ ] Record Phyphox data for EVERY test (export as CSV immediately)
   - [ ] Name files clearly: `ProtoA_250Hz_Trial1.csv`, `ProtoA_250Hz_Trial2.csv`, etc.
   - [ ] Also record audio files (.wav) as backup
   - [ ] Take screenshots of Spectroid display for visual comparison
   - [ ] Record ambient/background noise level before starting

3. **After testing:**
   - [ ] Backup ALL data to two locations
   - [ ] Run quick analysis to check for obvious errors
   - [ ] Share raw data with Student A for verification

### File Naming Convention:

```
Prototype_Frequency_TrialNumber.ext

Examples:
  A_250Hz_Trial1.csv       ← Prototype A, 250 Hz, first trial
  C_1000Hz_Trial3.wav      ← Prototype C, 1000 Hz, third trial
  Baseline_500Hz.wav        ← No panel measurement
  Ambient_noise.wav          ← Background noise reference
```

---

## PART 5: GRAPHS YOU MUST PRODUCE

### Graph 1: Frequency Spectra (FFT)
- **Type:** Line plot, log x-axis
- **Shows:** Power vs. frequency for baseline vs. with-panel
- **One per prototype per frequency** = 12 graphs (or combine into multi-panel)
- **Highlight:** The target frequency line + dB reduction value

### Graph 2: Attenuation Bar Chart (MAIN GRAPH)
- **Type:** Grouped bar chart
- **Shows:** ΔdB for all 3 prototypes at all 4 frequencies
- **This is the HERO graph** — goes on the poster and in the presentation
- **Expected pattern:** C > B > A, especially at low frequencies

### Graph 3: Theory vs. Experiment
- **Type:** Line plot with error shading
- **Shows:** Predicted ΔdB vs. measured ΔdB for Prototype C
- **Purpose:** Scientific rigor — did our design work as expected?

### Graph 4: Environmental Impact Comparison (from Student D)
- **Type:** Horizontal bar chart or radar/spider chart
- **Shows:** EcoMetaPanel vs. conventional foam across sustainability metrics

---

## PART 6: PRESENTATION DESIGN SPECS

### Slide Dimensions:
- Standard 16:9 (1920×1080 pixels or 33.87×19.05 cm)

### Color Palette (suggestion):
```
Primary (dark):    #2C3E50  (dark blue-gray)
Secondary:         #27AE60  (green — sustainability)
Accent:            #3498DB  (blue — science/tech)
Light bg:          #ECF0F1  (light gray)
Text:              #2C3E50  (same as primary)
Highlight:         #E74C3C  (red — for emphasis)
```

### Font:
- Titles: Bold, sans-serif (Arial, Calibri, or similar)
- Body: Regular, sans-serif, minimum 24pt for readability
- Graph labels: Minimum 14pt

### Slide Template Structure:
1. **Title** — Project name, team members, date
2. **The Problem** — Noise pollution statistics, why it matters
3. **What Are Acoustic Metamaterials?** — Simple explanation with diagrams
4. **Physics Principles** — Helmholtz resonance, quarter-wave, key formulas
5. **Materials Science** — Material properties, comparison table
6. **Our Design** — 3 prototypes with diagrams/photos
7. **Experimental Setup** — Photo of testing rig, procedure
8. **Results** — THE MAIN GRAPH (attenuation bar chart)
9. **Computer Analysis** — FFT spectra, how we processed data
10. **Environmental Impact** — LCA comparison, sustainability argument
11. **Limitations & Improvements** — What went wrong, what we'd do better
12. **Conclusion** — Did Prototype C beat Prototype A? (Yes, hopefully!)

---

## PART 7: WEEK-BY-WEEK CS PLAN

### This Week (June 10–11):
- [ ] Install all software, test Python environment
- [ ] Test Phyphox app, understand CSV export format
- [ ] Write and test tone generation script
- [ ] Test FFT analysis on a sample recording
- [ ] Create slide template

### June 12–15 (independent):
- [ ] Complete all Python analysis scripts
- [ ] Test full pipeline: generate tone → record → analyze → plot
- [ ] Draft presentation slides (leave content holes)
- [ ] Create graph templates ready for real data

### June 16 (testing day):
- [ ] Collect ALL data (your most important day)
- [ ] Quick-look analysis to catch problems
- [ ] Backup everything

### June 17–22 (analysis & production):
- [ ] Run full analysis, generate all graphs
- [ ] Fill in presentation content from team
- [ ] Design and produce the poster
- [ ] Export graphs at high resolution (300 DPI for poster)

### June 23 (presentation day):
- [ ] Set up laptop and presentation
- [ ] Control slides during presentation
- [ ] Ensure poster is printed

---

## 🚨 TROUBLESHOOTING

| Problem | Solution |
|---------|----------|
| Phyphox won't export | Take screenshot + manually record the dB reading |
| FFT looks noisy | Increase recording duration (10+ seconds), use Welch method |
| Python import error | `pip install [package]` — make sure you're in the right environment |
| Graphs don't show difference | Check if speaker volume changed between tests |
| File won't open | Check file path, use absolute paths in scripts |

---

*Send your test graph to the group chat by June 11 evening to confirm the pipeline works!*
