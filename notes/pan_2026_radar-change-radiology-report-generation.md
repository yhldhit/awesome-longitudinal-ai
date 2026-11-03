# RADAR: A Difference-Aware Retrieval With Organ-Level Alignment for Change Radiology Report Generation

## Citation

Pan, Y., Sun, G., Zhu, Y., Jiang, H., Shu, H., and Nguyen, L. M. RADAR: A Difference-Aware Retrieval With Organ-Level Alignment for Change Radiology Report Generation. IEEE Transactions on Medical Imaging, 45(10), 2026. DOI: 10.1109/TMI.2026.3712240.

Primary affiliations: Hangzhou Medical College; Japan Advanced Institute of Science and Technology; Guangzhou Institutes of Biomedicine and Health, Chinese Academy of Sciences. Pan and Sun contributed equally.

## Link

- Paper: https://doi.org/10.1109/TMI.2026.3712240
- Code address listed in the paper: https://github.com/yizhipan/RADAR
- Source: user-provided published PDF, pp. 4954-4969. The paper states that code will be publicly available; release status has not been verified.

## Problem

Generate a comparative report from current and prior chest radiographs, describing clinically relevant interval changes. The task requires separating pathological evolution from differences in positioning, inspiration, and acquisition, then expressing change direction and anatomical location accurately (pp. 4954-4957).

## Data

The authors construct a task-specific Change Radiology Report Generation benchmark from existing chest radiograph resources, including MIMIC-CXR. Evaluation spans report-level, anatomy-level, and pathology-level comparison. Chest ImaGenome supplies anatomical supervision discussed in the alignment design. These are derived resources rather than a newly acquired prospective cohort.

## Method

RADAR follows an align-first-then-compare pipeline. A visual encoder extracts paired image features, and an organ-level cross-attention module aligns prior features to current features with dual alignment supervision. The model then builds explicit difference-aware representations (Fig. 4, p. 4957).

Knowledge-Infused Generation retrieves clinical entities from a training-derived case memory using visual difference features as keys. The frozen language decoder receives aligned visual features, difference tokens, retrieved entities, learnable soft prompts, and a structured instruction. Three soft tokens encode no-change, improved, and worsened tendencies. The instruction guides observation, clinical vocabulary selection, change judgment, and report writing (Appendix, p. 4968).

## Key Results

- The authors report improvements over comparison methods on most benchmark evaluation metrics.
- In the pilot radiologist evaluation, consensus error rates were 22% for incorrect change direction, 16% for hallucination, and 39% for critical omission. These results show that automatic metric gains coexist with substantial clinical errors (p. 4967).
- In an analysis of 1,000 ground-truth no-change cases using a DeepSeek-based text check, 74.3% were described correctly as stable; 25.7% contained errors. This is an automated analysis, not a radiologist-validated clinical accuracy estimate (p. 4967).

## Relevance to Longitudinal AI

RADAR directly addresses longitudinal image-to-text modeling through paired-exam comparison, anatomical correspondence, explicit difference representations, and retrieval conditioned on disease evolution. It provides a useful comparison with HERGen and other longitudinal report-generation methods, especially for studying temporal factuality and distinguishing genuine progression from acquisition variation.
