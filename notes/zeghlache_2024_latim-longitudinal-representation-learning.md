# LaTiM: Longitudinal Representation Learning in Continuous-Time Models to Predict Disease Progression

## Citation

Zeghlache, R., Conze, P.-H., Daho, M. E. H., Li, Y., Le Boité, H., Tadayoni, R., Massin, P., Cochener, B., Rezaei, A., Brahim, I., Quellec, G., and Lamard, M. LaTiM: Longitudinal Representation Learning in Continuous-Time Models to Predict Disease Progression. MICCAI, 2024.

## Link

- Paper: https://papers.miccai.org/miccai-2024/paper/0263_paper.pdf

## Problem

This paper studies disease progression prediction from irregular longitudinal medical data, focusing on how to learn temporally meaningful representations that can improve continuous-time modeling rather than treating each visit independently.

## Data

- OPHDIAT diabetic retinopathy database

The paper evaluates disease progression prediction in a longitudinal ophthalmology setting.

## Method

LaTiM combines self-supervised representation learning with time-aware neural ordinary differential equations. The framework introduces a time-aware head that injects temporal information into latent-space augmentation and representation learning, aiming to produce more stable and informative continuous-time dynamics for downstream progression prediction.

## Key Results

- Proposes a longitudinal representation-learning framework tailored to continuous-time disease progression modeling.
- Integrates self-supervised learning with time-aware NODE architectures.
- Reports statistically significant gains over non-temporal or less explicitly time-aware baselines on diabetic retinopathy progression prediction, including improvements in AUC and Cohen's kappa according to the arXiv summary.
- Improves training stability for continuous-time temporal models.

## Relevance to Longitudinal AI

This paper is highly relevant. It contributes a representation-learning approach for continuous-time longitudinal disease modeling, which is a core methodological theme for longitudinal AI beyond purely generative forecasting.
