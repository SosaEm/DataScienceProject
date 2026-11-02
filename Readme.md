# RSV Respiratory Infections: Hospital Admission Prediction (Prototype)

End-to-end data science prototype that ingests live clinical data from
REDCap, cleans it, and compares machine learning models to predict ICU
admission in children under 5 hospitalized with respiratory illness
(tested for Respiratory Syncytial Virus, RSV).

> Status: functional prototype / feasibility study. Not a validated clinical tool.

## Context
Data come from an ongoing multi-center study covering 4 hospitals in
Buenos Aires (CABA and Greater Buenos Aires). Because the study was still
running, data were pulled dynamically through the REDCap API so the sample
stayed up to date.

## What it does
1. **Ingestion:** connects to the REDCap API (`requests`) and downloads the
   current records.
2. **EDA & cleaning:** exploratory analysis and cleaning of clinical data
   (pandas, ydata-profiling).
3. **Modeling:** trains and compares [list the models, e.g. logistic
   regression, random forest, XGBoost] using [validation strategy,
   e.g. stratified train/test split or cross-validation].
4. **Evaluation:** [recall, precision, ROC-AUC].

## Tech stack
Python · pandas · NumPy · requests · scikit-learn · XGBoost ·
statsmodels · matplotlib · seaborn · ydata-profiling

## Repository structure
- `Tercer Entrega/` : 
- `EntregaFinal_Sosa.ipynb` : final notebook 
- `requirements.txt`

## How to run
```bash
pip install -r requirements.txt
```
[REDCap API token and raw data are not included]

## Data privacy
Patient records are identified only by non-identifiable IDs. No raw data
or API credentials are included in this repository.

## Limitations & lessons learned
- Clinician review identified **target leakage** in one feature (mechanical
  ventilation is only applied to patients already in the ICU), which made
  early results look better than they were.
- The analysis focused on technical feasibility and model comparison; further
  work would require redefining features available at admission time and
  clinical validation.

## Author
Emiliano Martín Sosa · [www.linkedin.com/in/emiliano-m-sosa] · [emsosa50@gmail.com]
<img width="854" height="385" alt="imagen" src="https://github.com/user-attachments/assets/afe0a68e-1248-42f6-ac49-2321aae821a6" />
<img width="1014" height="388" alt="imagen" src="https://github.com/user-attachments/assets/5c16b01d-8e24-4003-89ab-eeeaa0209a09" />
<img width="510" height="421" alt="imagen" src="https://github.com/user-attachments/assets/6a98f2a4-241b-47ef-8a1a-843397d871ba" />

