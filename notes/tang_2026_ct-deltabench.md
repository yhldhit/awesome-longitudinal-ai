# CT-∆Bench: A Benchmark for Longitudinal 3D Medical Imaging Difference Reporting with Vision-Language Models

## Citation

Tang, K., Wang, J., Ren, S., and Wang, Z. CT-∆Bench: A Benchmark for Longitudinal 3D Medical Imaging Difference Reporting with Vision-Language Models. COLM, 2026 (as stated in the supplied PDF).

Primary affiliation: University of Tennessee at Chattanooga. Corresponding author: Zihao Wang.

## Link

- Data and code entry listed in the paper: https://huggingface.co/datasets/tangkg/CT-DeltaBench
- Source: user-provided PDF, 17 pages. A separate canonical publication URL was not identified in the PDF.

## Problem

Generate a clinically meaningful interval-change report from two temporally separated CT studies of the same patient. The benchmark targets explicit change reasoning rather than single-study description, including new, resolved, increased, decreased, and stable findings (pp. 1-3).

## Data

CT-DeltaBench is constructed from CT-RATE with 2,638 training pairs and 169 validation pairs, split at patient level. Gemini-2.5-Flash synthesizes reference difference Findings and Impression from the corresponding sections of the two original reports. Reference reports therefore derive from report text rather than independent paired-volume annotation (pp. 3-4).

Two physicians independently assess 50 validation cases for reference acceptability, correctness, completeness, and extracted-event quality. This validation evaluates the synthesized reports and event extraction, rather than model-generated reports (pp. 4-6).

## Method

The benchmark compares direct paired-CT prompting with an indirect pipeline that generates two single-study reports before textual differencing. Five medical vision-language models are evaluated zero-shot, with supervised experiments at 1%, 10%, and 100% of training data (p. 8).

DeltaMed uses shared MedSigLIP encoders for prior and follow-up scans. It concatenates prior features, follow-up features, and their directional difference, then applies linear fusion and normalization before the multimodal projector and Gemma 3 4B decoder. Only temporal fusion and language-model LoRA adapters are trained; the encoder, original projector, and base language weights are frozen (pp. 7-8).

Alongside ROUGE-L, BERTScore, and BLEURT, Qwen2.5-14B-Instruct extracts atomic change events for Change-F1, Missing Rate, Hallucination Rate, and Change Type Accuracy. Fuzzy matching uses normalized event text with anatomy and laterality constraints. Type accuracy is conditional on matched events; extracted events omit measurements and uncertain changes (pp. 5-7, 15-17).

## Key Results

- Direct zero-shot Change-F1 ranges from 0 to 0.0175 across the five models. Two-stage reporting is inconsistent, reaching 0.0614 for Med3DVLM-Qwen2.5-7B (Tables 2-3).
- With full training data, DeltaMed reaches Change-F1 0.1980 versus 0.1577 for paired-CT MedGemma, with Missing Rate 0.8301 versus 0.8856. DeltaMed has a higher Hallucination Rate: 0.8057 versus 0.7462 (Table 4).
- With 1% training data, DeltaMed achieves Change-F1 0.0909 versus 0.0010 for MedGemma, supporting the value of an explicit difference branch in this setting (Table 4).
- Reference-report clinical validation averages 4.82/5 for acceptability, with 99/100 physician judgments clinically acceptable. These are 100 ratings of 50 cases, not 100 independent cases (Table 1).
- Event errors are measured relative to synthesized reference reports and an automated extraction/matching pipeline; the rates should not be read as direct clinical error rates established by radiologist review of model outputs.

## Relevance to Longitudinal AI

This benchmark directly targets paired-volume longitudinal reasoning and separates textual similarity from temporal event correctness. It complements chest-X-ray methods such as RADAR by extending difference reporting to CT, and offers a concrete baseline for testing explicit change representations, paired-study fusion, and temporal factuality.
