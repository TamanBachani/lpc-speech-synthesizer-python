# 🗣️ Linear Predictive Speech Synthesizer (LPC-Based)

This repository contains the implementation and report for a **Linear Predictive Coding (LPC)–based Speech Synthesizer**, developed for the **Speech & Audio Processing module** as part of the MSc Artificial Intelligence program at the University of Surrey.

---

## 🎯 Objective

To synthesize vowel sounds (“ea” and “oo”) by simulating the Source-Filter model of speech production.  
- **Source:** Impulse train simulating glottal excitation  
- **Filter:** LPC model approximating vocal tract characteristics

---

## 🧠 Highlights

- Implemented in **Python**, replacing MATLAB routines
- Used `librosa`, `scipy`, and `matplotlib` for signal processing
- Tested various LPC orders to tune clarity and reduce robotic artifacts
- Subjective and spectral assessment of naturalness

---

## 🎧 Synthesized Output

> 🧑‍🦱 Male Vowel (F0 ≈ 90 Hz)  
> 👩‍🦰 Female Vowel (F0 ≈ 220 Hz)

Both were synthesized from 100ms speech segments using LPC with order 20.

---

## 📈 Results

| LPC Order | Quality      | Notes                                  |
|-----------|--------------|----------------------------------------|
| 6         | Robotic/Buzz | Low formant resolution                 |
| 10        | Improved     | Slightly better vowel approximation    |
| 20        | ✅ Best      | Clear vowel identity, minimal artifacts|

| Formant | Male (Hz)     | Female (Hz)    |
|---------|---------------|----------------|
| F1      | 328.13        | 679.69         |
| F2      | 1875.00       | 2320.31        |
| F3      | 3492.19       | 3562.50        |

---

## 🧪 Methodology Overview

### 1. 🎙️ Load and Trim Audio
- Used `.wav` recordings (`head_f.wav`, `hood_m.wav`)
- Trimmed 100ms vowel segments for consistency

### 2. 🔍 Estimate Pitch (F0)
- Mean F0 for male ≈ 90 Hz; female ≈ 220 Hz
- Used for impulse train periodicity

### 3. 🧮 Compute LPC Coefficients
- Orders: 6, 10, 14, 16, 20
- Extracted using `librosa.lpc`

### 4. 🧬 Simulate Impulse Train
- Periodic, with slight **jitter** to avoid robotic tone

### 5. 🧹 Post-processing
- Normalized signal
- Low-pass filtered for clarity

### 6. 🎧 Subjective Testing
- Informal listening + waveform and spectrum comparison

---

## 📁 Folder Contents

| File                     | Description                             |
|--------------------------|-----------------------------------------|
| `notebook.ipynb`         | Full code and plots                     |
| `report.docx`            | Detailed report with methodology        |
| `assets/`                | 📸 Screenshots and waveform visualizations |
| `.gitignore`             | Ignores `.DS_Store` and temp files      |

---

## 📸 Sample Visuals

_(Add these inside the `/assets` folder)_

- LPC Frequency Response  
- Original vs Synthesized Waveforms  
- Amplitude Spectrum  

---

## 🚀 How to Run

```bash
pip install librosa scipy matplotlib numpy
