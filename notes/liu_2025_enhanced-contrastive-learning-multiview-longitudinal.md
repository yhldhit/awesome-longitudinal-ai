# Enhanced Contrastive Learning with Multi-view Longitudinal Data for Chest X-ray Report Generation

## Citation

Liu, K., Ma, Z., Kang, X., Li, Y., Xie, K., Jiao, Z., and Miao, Q. Enhanced Contrastive Learning with Multi-view Longitudinal Data for Chest X-ray Report Generation. Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), pp. 10348-10359, 2025.

## Link

- Paper: https://openaccess.thecvf.com/content/CVPR2025/html/Liu_Enhanced_Contrastive_Learning_with_Multi-view_Longitudinal_Data_for_Chest_X-ray_CVPR_2025_paper.html
- arXiv: https://arxiv.org/abs/2502.20056
- Code: https://github.com/mk-runner/MLRG

## Problem

Existing chest X-ray report generation systems often use a single image, fixed dual views, or longitudinal context without fully modeling multiple views at the current visit. They also struggle when patient-specific context such as the indication, previous image, or previous report is missing. MLRG aims to combine spatial evidence across current views with temporal evidence from the most recent prior visit while remaining robust to incomplete clinical context.

## Data

The study evaluates MLRG on MIMIC-CXR, MIMIC-ABN, and Two-view CXR. The MIMIC-CXR training split contains 239,998 images and 150,957 reports, while its test split contains 3,852 images and 2,343 reports. MIMIC-ABN focuses on abnormal cases. Two-view CXR combines paired-view studies from MIMIC-CXR and IU X-ray; its training split contains 181,312 images and 90,656 reports. The authors release processed annotations, checkpoints, and generated reports, with PhysioNet authorization required for MIMIC data.

## Method

MLRG uses RAD-DINO as the vision encoder, CXR-BERT as the text encoder, and DistilGPT2 as the report generator. Stage 1 performs multi-view longitudinal contrastive learning: learnable view embeddings distinguish radiographic views, multi-positive contrastive learning aligns images from the same visit, and a fusion network combines current multi-view features with the most recent previous image before bidirectional image-report alignment. Stage 2 fuses this representation with patient-specific prior knowledge. Tokenized absence encoding uses `[NHI]` and `[NHPR]` when the indication or previous report is unavailable, allowing the generator to use whichever inputs are present.

## Key Results

- On MIMIC-CXR, MLRG reports BLEU-4 of 0.158, ROUGE-L of 0.320, RadGraph F1 of 0.291, and CheXpert F1 of 0.505; BLEU-4 improves by 2.3% over the strongest compared method.
- On MIMIC-ABN, it achieves BLEU-4 of 0.094, RadGraph F1 of 0.219, and CheXpert F1 of 0.515, including a reported 5.5% F1 improvement.
- On Two-view CXR, it achieves BLEU-4 of 0.154, RadGraph F1 of 0.328, and CheXpert F1 of 0.501, with a reported 2.7% RadGraph F1 improvement.
- Ablations show benefits from multi-view longitudinal contrastive learning, current multi-view images, previous images and reports, and indication information.
- The official repository provides training code, checkpoints for all three datasets, processed annotations, and generated reports for reproducible evaluation.

## Relevance to Longitudinal AI

MLRG is directly relevant to longitudinal AI because it jointly models within-visit spatial diversity and across-visit temporal change, rather than reducing a patient trajectory to one image per time point. Its explicit handling of missing historical and clinical inputs is also important for real-world longitudinal records, where prior examinations and indications are frequently incomplete.
