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

## Relevance to Longitudinal AI

This paper is highly relevant. It is a clear example of latent diffusion being adapted to longitudinal AI, especially for irregularly spaced patient trajectories in imaging-based clinical prediction.
