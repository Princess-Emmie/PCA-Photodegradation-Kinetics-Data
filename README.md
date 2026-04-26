# Diphenhydramine Photodegradation & Kinetics Study

This repository contains spectral, photodegradation profiles, and kinetics datasets from a study on the photodegradation of **Diphenhydramine** under various UV and chemical treatment conditions.

---

## 📁 Repository Structure

```
├── README.md
├── data/
│   ├── Diphenhydaramine_data.xlsx         # UV-Vis spectral data for PCA (post-expiry, standard, within-expiry samples)
│   ├── Photodegradation_profiles_data.xlsx    # Time-resolved spectral degradation profiles (UV and UV/H₂O₂ treatments)
│   └── Kinetics_data.xlsx                     # Zero, first, and second order kinetic data
```

---

## 📊 Dataset Descriptions

### 1. `Diphenhydaramine_data.xlsx` — PCA Spectral Data

- **Sheets:** Sheet1 (data), Sheet2 (empty), Sheet3 (empty)
- **Description:** UV-Vis absorbance spectra (wavelength 200–800 nm) of Diphenhydramine samples across three categories — **Post-expiry**, **Standard**, and **Within-expiry** — used for Principal Component Analysis (PCA) to examine spectral variability and classify sample groups.
- **Format:** Row 1 = sample category headers (Post-expiry / Standard / Within-expiry); Column A = wavelength (nm); remaining columns = absorbance values for individual sample replicates.
- **Sample groups:**
  - Post-expiry: ~98 replicates
  - Standard: ~100 replicates
  - Within-expiry: ~100 replicates

---

### 2. `Photodegradation_profiles_data.xlsx` — Photodegradation Spectral Profiles

- **Sheets:** ICE, LCE, EUVHO, HUVHO, FUVHO, GUVHO, AUV, DUV, CUV
- **Description:** Time-resolved UV-Vis absorbance spectra (1100–200 nm) of DPH formulations under different photodegradation treatment conditions. Each sheet contains spectra recorded at successive time intervals throughout the degradation experiment.
- **Format:** Row 1 = time point headers; Column A = wavelength (nm, descending from 1100); remaining columns = absorbance values at each time point.
- **Treatment conditions:**

| Sheet | Treatment | Time Points | Interval |
|-------|-----------|-------------|----------|
| ICE | Imacoff — BCG ion pair complex + UV  | 0–120 min | 10 min |
| LCE | Tricoff —  BCG ion pair complex + UV | 0–120 min | 10 min |
| EUVHO | Tricoff — UV + H₂O₂ | 0–180 min | 20 min |
| HUVHO | Imacoff — UV + H₂O₂ | 0–160 min | 20 min |
| FUVHO | Lacoff — UV + H₂O₂ | 0–180 min | 20 min |
| GUVHO | Lunahist — UV + H₂O₂ | 0–180 min | 20 min |
| AUV | Tricoff — UV only | 0–60 min | 10 min |
| DUV | Imacoff — UV only | 0–100 min | 10 min |
| CUV | Lunahist — UV only | 0–80 min | 10 min |

> Note: H₂O₂-only control conditions have been excluded from this dataset.

---

### 3. `Kinetics_data.xlsx` — Kinetic Order Analysis

- **Sheets:** Zero Order, First Order, Second Order
- **Description:** Kinetic data for DPH degradation under 10 treatment conditions, organised by kinetic model. Each sheet lists all conditions sequentially, with a title row, a header row, and data rows per condition.
- **Format:** Column A = Time (minutes); Column B = measured or derived absorbance parameter; conditions separated by a blank row.
- **Kinetic parameters:**

| Sheet | Y-axis Parameter | Kinetic Model |
|-------|-----------------|---------------|
| Zero Order | Absorbance (A.U.) | Linear decay in concentration |
| First Order | ln(Absorbance) | Exponential decay |
| Second Order | 1/Absorbance | Inverse concentration relationship |

- **Conditions included (all three sheets):**
  1. Simple Diluted Tricoff
  2. Simple Diluted Imacoff
  3. Simple Diluted Lunahist
  4. UV + H₂O₂ on Tricoff (peak 434 nm)
  5. UV + H₂O₂ on Tricoff (peak 632 nm)
  6. UV + H₂O₂ on Imacoff
  7. UV + H₂O₂ on Lunahist
  8. UV + H₂O₂ on Lacoff
  9. Complexed and Extracted Tricoff
  10. Complexed and Extracted Imacoff

---

## 🧪 Study Context

This dataset supports the investigation of photodegradation kinetics of **Diphenhydramine hydrochloride** (an antihistamine present in post-expiry pharmaceutical formulations) under UV and oxidative treatment conditions. Analyses performed include:

- **PCA** on multi-sample UV-Vis spectral data to discriminate post-expiry, within-expiry, and standard samples
- **Photodegradation profiling** across UV-only and UV/H₂O₂ advanced oxidation treatment matrices
- **Kinetic modelling** — zero, first, and second order rate law fitting to determine degradation mechanisms per formulation

---

## 📌 Usage Notes

- All measurements are in absorbance units (A.U.)
- Wavelength range: 200–800 nm (PCA data); 1100–200 nm (photodegradation profiles)
- Some cells in the photodegradation profiles are marked `--` indicating instrument out-of-range readings at those time points
- Software recommended: Python (pandas, scikit-learn, matplotlib) or Origin

---

## 📬 Contact

For questions about this dataset, please open an issue in this repository.

