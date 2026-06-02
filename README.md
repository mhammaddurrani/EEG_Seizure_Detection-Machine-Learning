# EEG-Based Seizure Detection Using Machine Learning

Automatic epileptic seizure detection from scalp EEG recordings using ensemble ML models. Trained on 24–72 hour recordings from 6 drug-resistant epilepsy patients.

**Best result:** Stacking Classifier — **99.85% F1-score | 1.00 Precision** (balanced data)

---

## Dataset
- **Source:** American University of Beirut Medical Center
- **Patients:** 6 drug-resistant epilepsy patients (2014–2015)
- **Channels:** 19 electrodes (10-20 system) · downsampled to 50 Hz
- **Challenge:** Severe class imbalance — seizures < 5% of recordings

---

## Models & Results

| Model | F1 (Unbalanced) | F1 (Balanced) | Improvement |
|---|---|---|---|
| Random Forest | 0.4257 | 0.9977 | +134% |
| Decision Tree | 0.3765 | 0.9361 | +149% |
| Hard Voting | 0.2782 | 0.9800 | +252% |
| **Stacking Classifier** | **0.4842** | **0.9985** | **+106%** |

> Class imbalance — not model complexity — was the primary bottleneck. RandomOverSampler outperformed SMOTE and ADASYN in both F1 gain and speed.

---

## Tech Stack
`Python` `scikit-learn` `MNE-Python` `imbalanced-learn` `XGBoost` `NumPy` `Pandas` `Matplotlib` `Seaborn`

---

## How to Run
```bash
git clone https://github.com/mhammaddurrani/eeg-seizure-detection.git
cd eeg-seizure-detection
pip install -r requirements.txt
jupyter notebook eeg_seizure_detection.ipynb
```

---

## Author
**Muhammad Hammad Durrani** · [GitHub](https://github.com/mhammaddurrani)
