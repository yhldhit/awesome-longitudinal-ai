# Advancing cancer detection and treatment using longitudinal routine clinical data

## Citation

Liu, F., Wang, K., Xu, H., et al. Advancing cancer detection and treatment using longitudinal routine clinical data. *Cell*, 2026. https://doi.org/10.1016/j.cell.2026.07.009.

## Link

- Paper: https://www.cell.com/cell/fulltext/S0092-8674(26)00807-X
- PDF: https://www.cell.com/cell/pdf/S0092-8674(26)00807-X.pdf
- Code: https://github.com/kaiwang13/Oncoformer
- Alternative code repository: https://must.digitwinmed.com/must/Oncoformer

## Problem

Cancer care is commonly divided into separate models for diagnosis, future risk, staging, treatment response, and prognosis. Many approaches also rely on specialized assays or single-time-point measurements. This study asks whether routinely collected longitudinal data can support the entire cancer continuum in one model, from pre-diagnostic risk prediction to treatment-response forecasting and recurrence surveillance.

## Data

- The China Oncology Multimodal Prediction and Surveillance Study (COMPASS) contains 17,748,334 clinical visits from 3,672,989 individuals, including 347,940 patients with cancer and 3,325,049 non-cancer controls.
- COMPASS-Main contains 2,810,742 individuals for model development; COMPASS-Replication provides an independent external hold-out cohort of 862,247 individuals.
- The study evaluates ten cancer types: lung, prostate, breast, liver, colorectal, esophageal, gastric, ovarian, cervical, and pancreatic cancer.
- External transfer is assessed in the UK Biobank cohort (n = 502,665), which is geographically and ethnically distinct from the predominantly Asian COMPASS cohorts.
- A prospective colorectal cancer screening pilot recruited 38,059 consenting participants and evaluated 3,025 high-risk individuals against colonoscopy.

## Method

- Oncoformer is a unified multimodal time-series Transformer that models longitudinal routine-care records.
- Dedicated encoders process time-series EHR variables, including laboratory tests and vital signs, and chest X-ray images; their representations are projected into a shared latent space.
- Self-supervised reconstruction and adversarial learning against missingness patterns and cohort identity aim to reduce bias from incomplete records and domain shifts.
- Task-specific heads support current cancer diagnosis, future cancer prediction, stage inference, treatment-response trajectory forecasting, and recurrence-free survival stratification.
- Causal masking allows predictions and risk scores to be updated at each visit using only information available up to that time.

## Key Results

- Pan-cancer diagnosis achieved an AUROC of 0.956, while future cancer onset up to one year before diagnosis achieved an AUROC of 0.869.
- Overall stage prediction reached a mean AUROC above 0.90, and predicted stage scores correlated with postoperative pathological endpoints and canonical cancer pathways.
- In the colorectal screening pilot, Oncoformer achieved an AUROC of 0.927, detecting 54 of 60 cancers with 90.0% sensitivity and 86.8% specificity.
- Treatment-response trajectories were forecast across six cancer-therapy settings, with R-squared values from 0.573 to 0.721.
- Oncoformer significantly stratified recurrence-free survival across all ten cancer types and outperformed Cox regression, random survival forests, and DeepHit in concordance index.
- On UK Biobank, transferred Oncoformer representations improved future lung cancer AUROC from 0.708 to 0.787 and pancreatic cancer AUROC from 0.603 to 0.690 over a locally trained routine-data baseline.

## Relevance to Longitudinal AI

This work is strongly aligned with longitudinal AI because it treats repeated clinical encounters as evolving patient trajectories rather than independent records. Its main contributions are:

- population-scale temporal modeling across 17.7 million visits;
- multimodal fusion of longitudinal EHR, laboratory, vital-sign, and imaging data;
- a shared representation spanning early detection, disease staging, therapeutic response, and prognosis;
- dynamically updated predictions that can support continuous surveillance.

The study is primarily retrospective, and most COMPASS participants are Asian. Although external and prospective-pilot results are encouraging, broader prospective randomized validation is required before clinical deployment. Performance also varies across cancer types and may be affected by different testing practices, severe missingness, and unmeasured confounding.
