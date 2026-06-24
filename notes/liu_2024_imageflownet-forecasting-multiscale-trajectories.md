# ImageFlowNet: Forecasting Multiscale Image-Level Trajectories of Disease Progression with Irregularly-Sampled Longitudinal Medical Images

## Citation

Liu, C., Xu, K., Shen, L. L., Huguet, G., Wang, Z., Tong, A., Bzdok, D., Stewart, J., Wang, J. C., Del Priore, L. V., and Krishnaswamy, S. ImageFlowNet: Forecasting Multiscale Image-Level Trajectories of Disease Progression with Irregularly-Sampled Longitudinal Medical Images. arXiv, 2024.

## Link

- Paper: https://arxiv.org/pdf/2406.14794
- Project: https://github.com/KrishnaswamyLab/ImageFlowNet

## Problem

This paper tackles longitudinal medical image forecasting under irregular sampling, where patients have repeated scans collected at uneven time intervals. The goal is to predict disease progression trajectories directly at the image level while preserving spatial structure.

## Data

- Longitudinal geographic atrophy imaging
- Longitudinal multiple sclerosis imaging
- Longitudinal glioblastoma imaging

The paper validates the method on three real-world longitudinal medical image datasets covering different disease progression settings.

## Method

ImageFlowNet learns multiscale representation spaces across patients and time points, then models temporal evolution with deterministic or stochastic flow fields using a position-parameterized neural ODE/SDE framework. A UNet backbone is used to build multiscale features, and the model includes regularization terms for high-level visual consistency, latent-space structure, and trajectory smoothness.

## Key Results

- Proposes a multiscale image-level trajectory forecasting framework for irregularly sampled longitudinal medical images.
- Combines shared representation learning across patients with flow-based temporal evolution modeling.
- Outperforms prior longitudinal forecasting baselines on three medical imaging datasets, according to the arXiv abstract.

## Relevance to Longitudinal AI

This paper is highly relevant. It focuses squarely on irregularly sampled longitudinal imaging trajectories and provides a generative temporal modeling framework for disease progression forecasting.
