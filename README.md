# 🗣️ Linear Predictive Speech Synthesizer (LPC-Based)

This repository contains the implementation and report for a **Linear Predictive Coding (LPC)-based Speech Synthesizer**, developed for the **Speech & Audio Processing module** during the MSc in Artificial Intelligence at the University of Surrey.

---

## 🎯 Objective

To synthesize vowel sounds (“ea” and “oo”) by simulating the Source–Filter model of speech production:

- **Source:** Impulse train simulating vocal cord excitation
- **Filter:** Linear Predictive model simulating vocal tract response

---

## 📄 Files in This Repo

| File                           | Description                                     |
|--------------------------------|-------------------------------------------------|
| `EEEM030_Assignment1.ipynb`    | Complete Python implementation                 |
| `EEEM030_Assignment1_Report.docx` | Full academic report with results & visuals |
| `assets/`                      | 📸 Screenshots from waveform and spectrum plots |

---

## 📈 Results

| LPC Order | Quality       | Notes                                      |
|-----------|---------------|---------------------------------------------|
| 6         | Robotic       | Limited formant detail                      |
| 10        | Clearer       | Better vowel shape, less noise              |
| 20        | ✅ Best       | Most natural result; preserved formants     |

### 📊 Formant Frequencies (LPC Order = 20)

| Formant | Male (Hz) | Female (Hz) |
|---------|-----------|-------------|
| F1      | 328.13    | 679.69      |
| F2      | 1875.00   | 2320.31     |
| F3      | 3492.19   | 3562.50     |

---

## 🎧 Synthesized Audio Samples

- [🔊 Synthesized Male Vowel](assets/audio/synthesized_vowel_male.wav)
- [🔊 Synthesized Female Vowel](assets/audio/synthesized_vowel_female.wav)

---

## 📈 Key Visuals

### 🧠 Source-Filter Model Overview
![Source-Filter](assets/source_filter_diagram.png)

---

### 🔊 Frequency Analysis of Vowels

**Male Segment:**
![Male Spectrum](assets/amplitude_spectrum_male.png)

**Female Segment:**
![Female Spectrum](assets/amplitude_spectrum_female.png)

---

### 🧪 Synthesized vs Original Amplitude Comparison
![Amplitude Comparison](assets/amplitude_comparison_librosa.png)

---

## 🚀 How to Run

```bash
pip install librosa numpy matplotlib scipy
