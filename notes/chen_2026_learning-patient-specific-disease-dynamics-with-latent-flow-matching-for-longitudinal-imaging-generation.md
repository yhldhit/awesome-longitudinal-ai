# Learning Patient-specific Disease Dynamics with Latent Flow Matching for Longitudinal Imaging Generation

## Citation

Chen, H., Yin, R., Chen, Y., Chen, Q., and Li, C. Learning Patient-specific Disease Dynamics with Latent Flow Matching for Longitudinal Imaging Generation. ICLR, 2026.

## Link

- Paper: https://openreview.net/pdf?id=cuGnuOfQ4U
- Project: https://github.com/chqwer2/Delta-LDM-Longitudinal

## Problem

This paper studies longitudinal medical image generation with a focus on modeling patient-specific disease progression over time, rather than producing only generic population-level trajectories.

## Data

The paper targets longitudinal imaging data. The README entry does not list the dataset details, so the exact cohorts and modalities should be filled in after reading the paper more closely.

## Method

The method uses latent flow matching for longitudinal imaging generation, aiming to capture temporal disease dynamics in a patient-specific latent space and support trajectory-aware synthesis.

## Key Results

- Proposes a longitudinal image generation framework centered on patient-specific disease dynamics.
- Uses latent flow matching instead of a standard static generation setup.
- Positions the model for personalized trajectory modeling in longitudinal imaging settings.

## Strengths

- Directly relevant to longitudinal AI and disease progression modeling.
- Focuses on personalization, which is important for clinical forecasting and simulation.
- Connects modern generative modeling with temporal medical imaging.

## Limitations

- The current note is based on repository metadata and title-level context; quantitative details still need to be extracted from the full paper.
- Applicability beyond the studied imaging setting may depend on modality and cohort scale.

## Relevance to Longitudinal AI

This paper is highly relevant. It sits close to the core of longitudinal AI by modeling subject-level temporal evolution in medical imaging with a generative framework.

## Follow-up Ideas

- Extract the exact latent flow matching formulation and temporal conditioning strategy.
- Record the datasets, time intervals, and evaluation metrics used in the experiments.
- Compare it against diffusion-based, autoregressive, and trajectory-forecasting baselines in longitudinal imaging.
