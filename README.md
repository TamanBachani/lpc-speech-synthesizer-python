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

## 📈 Visualizations

### Formant Plot

![Formant Plot](assets/images/formant_plot_amplitude_spectrum.png)

### Waveform Comparisons

**Female Vowel:**

![Original Female Waveform](assets/images/waveform_female_original.png)
![Synthesized Female Waveform](assets/images/waveform_female_synth.png)

**Male Vowel:**

![Original Male Waveform](assets/images/waveform_male_original.png)
![Synthesized Male Waveform](assets/images/waveform_male_synth.png)

---

## 🚀 How to Run

```bash
pip install librosa numpy matplotlib scipy
