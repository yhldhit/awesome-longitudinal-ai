# HERGen: Elevating Radiology Report Generation with Longitudinal Data

## Citation

Wang, F., Du, S., and Yu, L. HERGen: Elevating Radiology Report Generation with Longitudinal Data. In Computer Vision - ECCV 2024, Lecture Notes in Computer Science, vol. 15113, pp. 183-200. Springer, 2024.

## Link

- Publisher: https://link.springer.com/chapter/10.1007/978-3-031-73001-6_11
- Paper: https://arxiv.org/abs/2407.15158
- Code: https://github.com/HKU-MedAI/HERGen

## Problem

Most radiology report generation systems process each examination independently or use only one prior image, limiting their ability to represent disease progression across a patient's full imaging history. HERGen aims to generate temporally coherent chest X-ray reports from variable-length longitudinal image sequences while learning representations that support disease-progression assessment.

## Data

The study evaluates report generation on MIMIC-CXR and a Longitudinal MIMIC-CXR subset restricted to patients with at least two consecutive visits. After removing lateral and duplicate images, the curated MIMIC-CXR split contains 145,471 image-report pairs for training, 1,151 for validation, and 2,210 for testing. Temporal image classification is evaluated on MS-CXR-T, which contains 1,326 longitudinal frontal chest X-ray samples annotated for five findings and three progression states: improving, stable, and worsening.

## Method

HERGen encodes each chest X-ray with a CvT-based visual encoder and treats all visual tokens from one study as a group. A group causal transformer permits within-study token interaction and causal interaction with earlier visits, allowing variable-length patient histories to be aggregated without using future information. GPT-2 decodes the temporally aggregated representation into a report. An auxiliary contrastive objective aligns longitudinal image sequences with CXR-BERT report embeddings. Training follows a three-stage curriculum: single-study report generation, cross-modal alignment refinement, and temporal information learning with the group causal transformer.

## Key Results

- On curated MIMIC-CXR, HERGen achieves BLEU-4 of 0.122 and clinical F1 of 0.317, with a reported 5.9% average improvement across NLG metrics and 3.6% improvement in F1 over the strongest directly comparable rerun baseline.
- On Longitudinal MIMIC-CXR, HERGen obtains BLEU-4 of 0.117 and clinical F1 of 0.295, outperforming both single-image baselines and the longitudinal Prefilling method across the reported NLG metrics.
- Relative to CvT-212DistilGPT2 on the longitudinal subset, the paper reports gains of 14.7% in precision, 12.0% in recall, and 13.0% in clinical F1.
- On MS-CXR-T, HERGen achieves the best macro-accuracy for four of five findings and improves over the second-best method by 11.1, 4.9, 14.7, and 3.7 percentage points for consolidation, pleural effusion, pneumonia, and pneumothorax, respectively.
- Ablation analyses support the contributions of auxiliary contrastive alignment, temporal aggregation, and the staged curriculum.

## Relevance to Longitudinal AI

HERGen is directly relevant to longitudinal AI because it models variable-length patient histories, enforces causal temporal information flow, aligns imaging trajectories with clinical language, and evaluates whether the learned representation captures improving, stable, and worsening disease states. It provides a concrete multimodal framework for moving from isolated-visit interpretation toward history-aware clinical generation and progression modeling.
