# A Review of Longitudinal Radiology Report Generation: Dataset Composition, Methods, and Performance Evaluation

## Citation

Zhou, S., Li, Y., Liu, Y., Liu, L., Wang, L., and Zhou, L. A Review of Longitudinal Radiology Report Generation: Dataset Composition, Methods, and Performance Evaluation. arXiv, 2025.

## Link

- Paper: https://arxiv.org/pdf/2510.12444

## Problem

This survey reviews longitudinal radiology report generation, with a focus on how to generate clinically meaningful follow-up reports that incorporate prior studies and comparison statements instead of relying only on single-image report generation.

## Data

The survey focuses primarily on longitudinal chest X-ray report generation settings and discusses how datasets are constructed for longitudinal report generation, including historical exam context and paired reporting information.

## Method

As a review paper, it organizes the field around three main aspects: dataset construction, model architectures with longitudinal-specific design choices, and evaluation protocols. It also summarizes reported performance and ablation findings across existing longitudinal radiology report generation methods.

## Key Results

- Presents what the paper describes as the first comprehensive review of longitudinal radiology report generation.
- Summarizes dataset composition strategies for longitudinal report generation tasks.
- Reviews model design patterns tailored to historical context and temporal comparison.
- Covers evaluation methods, including longitudinal-specific measures and common report-generation benchmarks.
- Highlights major current limitations and future research directions for the field.

## Strengths

- Highly aligned with longitudinal AI in a clinically important multimodal setting.
- Helps structure an emerging literature that is otherwise scattered across report-generation and medical vision-language communities.
- Useful as an entry point for understanding datasets, architectures, and evaluation gaps in longitudinal report generation.

## Limitations

- As a survey, it does not propose a new modeling method directly.
- The current note is based mainly on the arXiv abstract and metadata; detailed method taxonomy and benchmark tables still need fuller extraction.
- The scope appears centered on radiology report generation, especially chest X-ray contexts, rather than all longitudinal medical modalities.

## Relevance to Longitudinal AI

This paper is highly relevant. It covers a core longitudinal AI problem where historical context, temporal comparison, and multimodal clinical understanding all matter for generating faithful follow-up reports.

## Follow-up Ideas

- Extract the survey's taxonomy of longitudinal report-generation architectures into a reusable table for the repository.
- Add the key datasets and evaluation metrics mentioned in the paper to the `Resources` section later.
- Use this survey to identify seminal longitudinal radiology report-generation papers that should also be added individually.
