# Conditional Latent Diffusion Models for Irregularly Spaced Longitudinal Radiological Data

## Citation

Mouadden, N., Laousy, O., Marini, R., Ong, V., Revel, M.-P., Chassagnon, G., Christodoulidis, S., and Vakalopoulou, M. Conditional Latent Diffusion Models for Irregularly Spaced Longitudinal Radiological Data. MICCAI, 2025.

## Link

- Paper: https://papers.miccai.org/miccai-2025/paper/2656_paper.pdf

## Problem

This paper studies longitudinal medical imaging under irregular follow-up intervals, where patients may have different numbers of scans collected at uneven time gaps. The goal is to predict future patient states from prior imaging history in a way that works across heterogeneous longitudinal scenarios.

## Data

- 3D chest CT scans for Interstitial Lung Disease progression in Systemic Sclerosis patients
- Longitudinal chest X-rays and reports from MIMIC-CXR

## Method

The proposed framework combines three components: a universal 2D/3D vision encoder, a temporal transformer that fuses multiple prior exams with learned date embeddings, and a conditional latent diffusion model that predicts future latent representations at predefined time points. Task-specific decoders then map the generated latent state to either segmentation masks or radiology reports.

## Key Results

- Uses one unified pipeline for both 2D and 3D radiological longitudinal data.
- Handles variable numbers of historical scans and irregularly spaced follow-up intervals.
- Outperforms baseline approaches on both future pathology forecasting and longitudinal report generation, according to the paper abstract.

## Strengths

- Directly targets a realistic longitudinal imaging setting with irregular sampling.
- Uses latent diffusion in a clinically meaningful forecasting setup rather than only static generation.
- Unifies segmentation-style prediction and report generation within one temporal framework.

## Limitations

- The current note is based on the paper PDF rather than a full experimental extraction table.
- No public code link was identified from the paper URL alone.
- Generalization to other modalities or non-radiology longitudinal settings remains to be validated.

## Relevance to Longitudinal AI

This paper is highly relevant. It is a clear example of latent diffusion being adapted to longitudinal AI, especially for irregularly spaced patient trajectories in imaging-based clinical prediction.

## Follow-up Ideas

- Extract the exact baselines, metrics, and quantitative gains from the experiments section.
- Compare this paper with latent flow matching and other temporal generative methods in the repo.
- Track whether a public implementation appears later and add it to the entry if available.
