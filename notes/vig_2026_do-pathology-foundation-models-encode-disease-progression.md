# Do Pathology Foundation Models Encode Disease Progression? A Pseudotime Analysis of Visual Representations

## Citation

Vig, P., Wu, R.-C., and Lotter, W. Do Pathology Foundation Models Encode Disease Progression? A Pseudotime Analysis of Visual Representations. arXiv, 2026.

## Link

- Paper: https://arxiv.org/abs/2601.21334
- Code: https://github.com/pritika-vig/embeddings_disease_progression_analysis

## Problem

Pathology foundation models are usually evaluated with discrete classification benchmarks, which do not reveal whether their representations preserve the continuous biological processes connecting disease states. This paper asks whether foundation-model embedding spaces implicitly encode coherent cancer progression trajectories and whether this geometric property predicts downstream generalization.

## Data

The study uses expert-annotated 224 x 224 H&E patches at 20x magnification from the SPIDER dataset. It evaluates four cancer progressions: skin squamous cell carcinoma, the colorectal conventional pathway, the colorectal serrated pathway, and breast ductal carcinoma. Each disease class is standardized to 1,000 patches with slide-aware sampling where possible; the breast cohort contains 2,714 patches because high-grade DCIS samples are limited. SPIDER was not used to train any of the evaluated foundation models.

## Method

The authors evaluate six frozen vision encoders: the natural-image model DINOv2 and five computational pathology foundation models (UNI-2, Virchow-2, Prov-GigaPath, CONCH, and MUSK). For each disease cohort, they construct a k-nearest-neighbor graph over patch embeddings, apply diffusion pseudotime from a root patch in the earliest disease class, and quantify agreement between inferred pseudotime and ordinal disease-stage labels using Kendall's tau-b. Label-order permutations test whether the embeddings encode the biological progression direction rather than merely separating disease classes. Intermediate-layer analysis, intrinsic-dimension estimation, few-shot classification, and cell-composition analysis further probe when the trajectory structure emerges and whether it is biologically meaningful.

## Key Results

- All pathology-specific models recover progression orderings significantly above label-shuffled null baselines.
- Vision-only pathology models show the strongest and most consistent trajectory fidelity, with Kendall's tau above 0.78 on the colorectal serrated progression.
- Trajectory fidelity generally increases with network depth, while the inferred diffusion manifold remains low-dimensional at approximately four to five dimensions.
- Model rankings by trajectory fidelity on reference diseases strongly predict 5-shot classification performance on held-out diseases, with a mean Spearman correlation of 0.92.
- Along the inferred colorectal trajectory, fibroblast and neutrophil abundance changes smoothly in patterns consistent with known stromal remodeling, supporting biological relevance beyond discrete stage labels.

## Relevance to Longitudinal AI

This paper directly addresses a central longitudinal AI problem: recovering continuous disease progression from cross-sectional static observations. It adapts diffusion pseudotime from single-cell biology to pathology foundation-model representations and introduces trajectory fidelity as a geometry-based evaluation criterion. The framework is useful for assessing whether pretrained medical-image encoders preserve progression structure before they are used for longitudinal prediction, retrieval, or generative modeling, although the inferred pseudotime provides relative ordering rather than absolute temporal rates.
