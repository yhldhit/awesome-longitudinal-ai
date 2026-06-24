# Foundation Models in Radiology: What, How, Why, and Why Not

## Citation

Paschali, M., Chen, Z., Blankemeier, L., Varma, M., Youssef, A., Bluethgen, C., Langlotz, C., Gatidis, S., and Chaudhari, A. Foundation Models in Radiology: What, How, Why, and Why Not. Radiology, 2025.

## Link

- Paper: https://pubs.rsna.org/doi/epdf/10.1148/radiol.240597

## Problem

This review explains what foundation models mean in radiology, how they are trained and adapted, what capabilities they can support in clinical imaging workflows, and what risks and limitations must be addressed before responsible deployment.

## Data

The paper is a review rather than a benchmark study. It discusses large-scale radiology datasets and multimodal data sources used for foundation model training, including imaging archives, image-text pairs, reports, electronic health records, and other clinical modalities.

## Method

As a review paper, it organizes the field around the defining properties of radiology foundation models, core architectural blocks such as encoders, fusion modules, and decoders, major self-supervised pretraining paradigms including generative and contrastive learning, adaptation strategies such as zero-shot inference and fine-tuning, dataset requirements, evaluation methods, and deployment risks.

## Key Results

- Provides a structured overview of foundation models in radiology.
- Reviews generative and contrastive pretraining strategies relevant to radiologic imaging and image-text learning.
- Summarizes available radiology datasets and multimodal training resources.
- Discusses clinical use cases, evaluation strategies, and major risks such as hallucination and automation bias.
- Emphasizes the need for standardized benchmarks and responsible deployment practices.

## Strengths

- Strong overview paper for the radiology-specific foundation model landscape.
- Bridges technical model design with clinical workflow and safety considerations.
- Useful reference for understanding how multimodal, self-supervised, and large-scale pretraining ideas translate into radiology.

## Limitations

- This is a review paper, so it does not introduce a new longitudinal modeling method directly.
- Its scope is broader than longitudinal AI and focuses on radiology foundation models overall.
- The current note is based on the published Radiology review page and abstract-level content; a deeper extraction of the paper's tables and taxonomy could still add value.

## Relevance to Longitudinal AI

This paper is indirectly but importantly relevant. It provides background on multimodal and self-supervised foundation model design in radiology, which is useful for longitudinal imaging, longitudinal report generation, and future patient-trajectory modeling systems.

## Follow-up Ideas

- Extract the review's discussion of multimodal radiology datasets into the repository `Resources` section later.
- Add longitudinally oriented foundation model papers that build on the pretraining and adaptation patterns summarized here.
- Compare this review with longitudinal radiology report-generation surveys to identify shared benchmark and evaluation gaps.
