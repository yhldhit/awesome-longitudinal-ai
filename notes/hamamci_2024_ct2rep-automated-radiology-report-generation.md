# CT2Rep: Automated Radiology Report Generation for 3D Medical Imaging

## Citation

Hamamci, I. E., Er, S., and Menze, B. CT2Rep: Automated Radiology Report Generation for 3D Medical Imaging. In *Medical Image Computing and Computer Assisted Intervention - MICCAI 2024*, LNCS 15012, pp. 476-486, 2024.

## Link

- Paper: https://papers.miccai.org/miccai-2024/paper/2185_paper.pdf
- arXiv: https://arxiv.org/abs/2403.06801
- Code: https://github.com/ibrahimethemhamamci/CT2Rep
- Dataset: https://huggingface.co/datasets/ibrahimhamamci/CT-RATE

## Problem

Most radiology report generation systems operate on 2D images, while volumetric CT report generation remains underexplored because 3D scans are computationally demanding and paired CT-report datasets are scarce. The paper introduces an end-to-end system for generating findings from 3D chest CT and extends it to the longitudinal setting, where a patient's previous CT volume and report can provide clinically relevant temporal context for the current examination.

## Data

- The study introduces CT-RATE, a chest CT dataset with 25,701 non-contrast volumes from 21,314 patients and corresponding radiology reports.
- Multiple reconstructions expand the dataset to 49,138 CT volumes. The split contains 20,000 training patients and 1,314 validation patients.
- Report generation uses the Findings section of each report as the target text.
- The longitudinal subset includes patients with more than one visit. After reconstruction expansion, it contains 13,354 training volumes and 849 validation volumes from 2,638 and 169 patients, respectively.
- Pairing all chronologically valid examinations yields 28,441 training pairs and 1,689 validation pairs for CT2RepLong.

## Method

- CT2Rep divides a CT volume into 3D patches and applies a spatial transformer followed by a causal transformer to learn volumetric visual features autoregressively.
- A transformer encoder-decoder generates the report from the extracted 3D representation.
- Relational memory and memory-driven conditional layer normalization preserve report-level context and guide token generation.
- CT2RepLong extends the base model with hierarchical longitudinal memory and cross-attention-based multimodal fusion.
- For a current CT examination, CT2RepLong combines the current volume with the patient's previous CT volume and previous report, allowing prior image and text evidence to inform the new report.

## Key Results

- On CT-RATE, CT2Rep improves over the CT-Net-based baseline in both language and clinical metrics: BLEU-4 increases from 0.354 to 0.369, ROUGE-L from 0.442 to 0.459, and clinical F1 from 0.456 to 0.534.
- On the longitudinal subset, CT2RepLong reaches a clinical F1 of 0.536, compared with 0.525 without prior-examination context and 0.533 for a simpler previous-report-plus-volume fusion strategy.
- Ablation experiments indicate that combining prior report and prior volume is more effective than using either modality alone, while the cross-attention fusion further improves clinical content.
- The longitudinal extension is trained on data from only about 13% of the full patient cohort, highlighting the value of prior-examination context despite limited longitudinal supervision.

## Relevance

This paper is directly relevant to longitudinal AI because CT2RepLong models same-patient temporal context rather than treating each scan independently. It is particularly notable for:

- extending longitudinal report generation from 2D radiographs to full 3D CT volumes;
- integrating prior imaging and prior text in a unified multimodal model;
- releasing the large-scale CT-RATE dataset, code, and pretrained models for reproducible research.

The method focuses on pairs of current and previous examinations rather than longer patient trajectories, leaving multi-visit temporal modeling as an important direction for future work.
