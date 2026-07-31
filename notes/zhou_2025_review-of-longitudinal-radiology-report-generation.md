# A Review of Longitudinal Radiology Report Generation: Dataset Composition, Methods, and Performance Evaluation

## Citation

Zhou, S., Li, Y., Liu, Y., Liu, L., Wang, L., and Zhou, L. A Review of Longitudinal Radiology Report Generation: Dataset Composition, Methods, and Performance Evaluation. arXiv, 2025.

## Link

- Paper: https://arxiv.org/abs/2510.12444
- HTML: https://arxiv.org/html/2510.12444v1

## Problem

Conventional chest X-ray report generation usually treats each examination independently, limiting its ability to produce clinically faithful comparisons with prior studies and sometimes causing hallucinated references to historical findings. This survey reviews longitudinal radiology report generation (LRRG), where current images and reports are interpreted together with one or more prior examinations.

## Data

The review focuses on longitudinal subsets derived from MIMIC-CXR, which contains 473,057 images and 227,835 reports from 63,478 patients. It describes a commonly used longitudinal subset containing 95,168 studies from 26,625 patients and organizes dataset construction along three axes: the modalities available from prior studies (images, reports, or both), the number of prior time points, and the use of frontal and lateral views. Most methods use only the most recent prior study, while a smaller group models multiple historical examinations.

## Method

The paper develops a taxonomy covering dataset composition, visual encoders and text decoders, and longitudinal-specific mechanisms. It groups temporal modeling approaches into handling missing historical data, cross-time and cross-modal feature alignment, longitudinal feature fusion, and auxiliary modules such as temporal-change classification, retrieval augmentation, and time-gap encoding. It also compares lexical, clinical, LLM-based, and longitudinal-specific evaluation metrics and compiles reported benchmark and ablation results.

## Key Results

- Presents what the paper describes as the first comprehensive review of longitudinal radiology report generation.
- Shows that prior studies can be represented as image-only, report-only, or combined image-report context, with substantial variation in the number of time points and imaging views used.
- Identifies contrastive alignment and temporal feature fusion as central architectural components; the compiled ablations consistently show performance degradation when these modules are removed.
- Distinguishes standard lexical and clinical metrics from longitudinal measures such as Temporal F1, TEM, and LUNGUAGE SCORE, while noting that current temporal metrics remain limited in spatial alignment and radiologist validation.
- Summarizes five major limitations: scarce longitudinal data, underuse of time intervals, redundant historical context, inadequate cross-time image registration, and the lack of robust longitudinal-specific datasets and evaluation metrics.
- Highlights future directions including synthetic longitudinal data, time-aware and redundancy-aware modeling, spatial alignment, expert-validated evaluation, prospective disease-progression prediction, and extension beyond chest X-rays to CT, MRI, and PET.

## Relevance to Longitudinal AI

This survey maps a core longitudinal AI task in which models must integrate multimodal observations across irregular clinical time points, distinguish true change from redundant history, and communicate progression in clinically faithful language. Its dataset taxonomy, temporal-modeling design space, and evaluation critique provide a practical reference for longitudinal report generation and for broader work on disease-trajectory representation and forecasting.
