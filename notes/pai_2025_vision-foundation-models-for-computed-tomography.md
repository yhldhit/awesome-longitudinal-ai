# Vision Foundation Models for Computed Tomography

## Citation

Pai, S., Hadzic, I., Bontempi, D., Bressem, K., Kann, B. H., Fedorov, A., Mak, R. H., and Aerts, H. J. W. L. Vision Foundation Models for Computed Tomography. arXiv, 2025.

## Link

- Paper: https://arxiv.org/abs/2501.09001
- Project: https://aim.hms.harvard.edu/ct-fm

## Problem

This paper aims to build a large-scale native 3D vision foundation model for computed tomography that can transfer across a broad range of radiology tasks without relying on joint image-text pretraining.

## Data

- Pretraining: 148,000 CT scans from the Imaging Data Commons.
- Evaluation tasks include whole-body segmentation, heterogeneous tumor segmentation, head CT triage classification, medical image retrieval, and semantic understanding.
- Benchmark datasets mentioned in the paper include TotalSegmentator, Medical Segmentation Decathlon subsets, SinoCT, CQ500, OrganMNIST3D, and 3D-MIR.

## Method

The paper proposes CT-FM, a vision-centric 3D CT foundation model trained with label-agnostic contrastive learning on large-scale CT data. The pretraining objective is a modified SimCLR-style framework tailored to 3D medical imaging, with within-sample patch-based negatives used to better preserve fine-grained structural information. The resulting encoder is evaluated through fine-tuning on segmentation and classification tasks and through zero-shot retrieval and semantic concept search analyses.

## Key Results

- CT-FM is pretrained on 148,000 CT scans from the Imaging Data Commons.
- The model outperforms or matches strong baselines across whole-body segmentation, tumor segmentation, head CT triage, image retrieval, and semantic understanding tasks.
- It demonstrates strong zero-shot retrieval and semantic search behavior, including improved organ centroid distance and more anatomically coherent embeddings than comparison baselines.
- The paper emphasizes robustness across test-retest settings and interpretable localized representations.
- Weights, code, and data-access pipeline are reported as open-sourced through the project website.

## Relevance to Longitudinal AI

This paper is not itself a longitudinal modeling paper, but it is highly relevant as a backbone paper for longitudinal CT research. It provides a strong native 3D vision encoder trained on large-scale CT data, which can serve as the visit-level representation module for multi-visit sequence modeling, time-to-event continued pretraining, progression retrieval, and change-aware longitudinal CT forecasting.
