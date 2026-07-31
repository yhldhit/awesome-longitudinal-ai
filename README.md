# Awesome Longitudinal AI

A curated repository for papers, tools, datasets, benchmarks, and notes related to longitudinal AI.

<!-- ## Scope -->

<!-- This repository is intended to organize and share resources around:

- Longitudinal modeling in healthcare and biomedicine
- Time-aware foundation models and representation learning
- Sequential decision making and patient trajectory modeling
- Multimodal longitudinal data
- Datasets, benchmarks, and surveys -->
## Contents
- [Survey Papers](#survey-papers)
- [Research Papers](#research-papers)
  - [Foundation models](#foundation-models)
  - [Diffusion-based](#diffusion-based)
  - [Flow matching-based](#flow-matching-based)
  - [Latent Diffusion-based](#latent-diffusion-based)
  - [Multimodal-based](#multimodal-based)
- [Resources](#resouces)
  - [Datasets](#datasets)
  - [Benchmarks](#benchmarks)

## Survey Papers

**A Survey on Generative Diffusion Model** \
*Hanqun Cao, Cheng Tan, Zhangyang Gao, Guangyong Chen, Pheng-Ann Heng, Stan Z. Li* \
[TKDE, 2024] [CUHK, Weslake University]\
[[Paper](https://arxiv.org/pdf/2209.02646.pdf)] [[Github](https://github.com/chq1155/A-Survey-on-Generative-Diffusion-Model)] [[Note](notes/cao_2024_a-survey-on-generative-diffusion-model.md)]

**A Survey on Diffusion Models for Time Series and Spatio-Temporal Data** \
*Yiyuan Yang, Ming Jin, Haomin Wen, Chaoli Zhang, Yuxuan Liang, Lintao Ma, Yi Wang, Chenghao Liu, Bin Yang, Zenglin Xu, Shirui Pan, Qingsong Wen* \
[ACM Computing Surveys, 2026] [University of Oxford, Griffith University, Carnegie Mellon University] \
[[Paper](https://dl.acm.org/doi/epdf/10.1145/3783986)] [[Note](notes/yang_2026_survey-on-diffusion-models-for-time-series-and-spatio-temporal-data.md)]

**A Review of Longitudinal Radiology Report Generation: Dataset Composition, Methods, and Performance Evaluation** \
*Shaoyang Zhou, Yingshu Li, Yunyi Liu, Lingqiao Liu, Lei Wang, Luping Zhou* \
[arXiv, 2025] [The University of Sydney, The University of Adelaide, University of Wollongong] \
[[Paper](https://arxiv.org/abs/2510.12444)] [[Note](notes/zhou_2025_review-of-longitudinal-radiology-report-generation.md)]

**Foundation Models in Radiology: What, How, Why, and Why Not** \
*Magdalini Paschali, Zhihong Chen, Louis Blankemeier, Maya Varma, Alaa Youssef, Christian Bluethgen, Curtis Langlotz, Sergios Gatidis, Akshay Chaudhari* \
[Radiology, 2025] [Stanford Center for AI in Medicine and Imaging, Stanford University, University Hospital Zurich] \
[[Paper](https://pubs.rsna.org/doi/epdf/10.1148/radiol.240597)] [[Note](notes/paschali_2025_foundation-models-in-radiology.md)]

## Research Papers

### Foundation models

**LaTiM: Longitudinal Representation Learning in Continuous-Time Models to Predict Disease Progression** \
*Rachid Zeghlache, Pierre-Henri Conze, Mostafa El Habib Daho, Yihao Li, Hugo Le Boité, Ramin Tadayoni, Pascal Massin, Béatrice Cochener, Alireza Rezaei, Ikram Brahim, Gwenolé Quellec, Mathieu Lamard* \
[MICCAI, 2024] [LaTIM Inserm UMR 1101, University of Western Brittany, Lariboisiere Hospital AP-HP] \
[[Paper](https://papers.miccai.org/miccai-2024/paper/0263_paper.pdf)] [[Note](notes/zeghlache_2024_latim-longitudinal-representation-learning.md)]

**Vision Foundation Models for Computed Tomography** \
*Suraj Pai, Ibrahim Hadzic, Dennis Bontempi, Keno Bressem, Benjamin H. Kann, Andriy Fedorov, Raymond H. Mak, Hugo J. W. L. Aerts* \
[arXiv, 2025] [Mass General Brigham, Harvard Medical School, Maastricht University] \
[[Paper](https://arxiv.org/abs/2501.09001)] [[Note](notes/pai_2025_vision-foundation-models-for-computed-tomography.md)]

**Do Pathology Foundation Models Encode Disease Progression? A Pseudotime Analysis of Visual Representations** \
*Pritika Vig, Ren-Chin Wu, William Lotter* \
[arXiv, 2026] [MIT, Dana-Farber Cancer Institute, Harvard Medical School] \
[[Paper](https://arxiv.org/abs/2601.21334)] [[Github](https://github.com/pritika-vig/embeddings_disease_progression_analysis)] [[Note](notes/vig_2026_do-pathology-foundation-models-encode-disease-progression.md)]

### Diffusion-based

### Latent Diffusion-based

**Conditional Latent Diffusion Models for Irregularly Spaced Longitudinal Radiological Data** \
*Nabil Mouadden, Othmane Laousy, Rafael Marini, Valentin Ong, Marie-Pierre Revel, Guillaume Chassagnon, Stergios Christodoulidis, Maria Vakalopoulou* \
[MICCAI, 2025] [CentraleSupelec, Hôpital Cochin AP-HP, Archimedes/Athena RC] \
[[Paper](https://papers.miccai.org/miccai-2025/paper/2656_paper.pdf)] [[Note](notes/mouadden_2025_conditional-latent-diffusion-models-for-irregularly-spaced-longitudinal-radiological-data.md)]



### Flow Matching-based

**ImageFlowNet: Forecasting Multiscale Image-Level Trajectories of Disease Progression with Irregularly-Sampled Longitudinal Medical Images** \
*Chen Liu, Ke Xu, Liangbo L. Shen, Guillaume Huguet, Zilong Wang, Alexander Tong, Danilo Bzdok, Jay Stewart, Jay C. Wang, Lucian V. Del Priore, Smita Krishnaswamy* \
[arXiv, 2024] [Yale University, New York Eye and Ear Infirmary of Mount Sinai] \
[[Paper](https://arxiv.org/pdf/2406.14794)] [[Github](https://github.com/KrishnaswamyLab/ImageFlowNet)] [[Note](notes/liu_2024_imageflownet-forecasting-multiscale-trajectories.md)]

**Learning Patient-specific Disease Dynamics with Latent Flow Matching for Longitudinal Imaging Generation** \
*Hao Chen, Rui Yin, Yifan Chen, Qi Chen, Chao Li* \
[ICLR, 2026] [University of Cambridge, Nanjing Medical University, University of Dundee] \
[[Paper](https://openreview.net/pdf?id=cuGnuOfQ4U)] [[Github](https://github.com/chqwer2/Delta-LDM-Longitudinal)] [[Note](notes/chen_2026_learning-patient-specific-disease-dynamics-with-latent-flow-matching-for-longitudinal-imaging-generation.md)]

### Multimodal-based

**HERGen: Elevating Radiology Report Generation with Longitudinal Data** \
*Fuying Wang, Shenghui Du, Lequan Yu* \
[ECCV, 2024] [The University of Hong Kong] \
[[Paper](https://link.springer.com/chapter/10.1007/978-3-031-73001-6_11)] [[Github](https://github.com/HKU-MedAI/HERGen)] [[Note](notes/wang_2024_hergen-elevating-radiology-report-generation.md)]

**Enhanced Contrastive Learning with Multi-view Longitudinal Data for Chest X-ray Report Generation** \
*Kang Liu, Zhuoqi Ma, Xiaolu Kang, Yunan Li, Kun Xie, Zhicheng Jiao, Qiguang Miao* \
[CVPR, 2025] [Xidian University, Brown University] \
[[Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Liu_Enhanced_Contrastive_Learning_with_Multi-view_Longitudinal_Data_for_Chest_X-ray_CVPR_2025_paper.html)] [[Github](https://github.com/mk-runner/MLRG)] [[Note](notes/liu_2025_enhanced-contrastive-learning-multiview-longitudinal.md)]

**CT2Rep: Automated Radiology Report Generation for 3D Medical Imaging** \
*Ibrahim Ethem Hamamci, Sezgin Er, Bjoern Menze* \
[MICCAI, 2024] [University of Zurich, Istanbul Medipol University] \
[[Paper](https://papers.miccai.org/miccai-2024/paper/2185_paper.pdf)] [[Github](https://github.com/ibrahimethemhamamci/CT2Rep)] [[Note](notes/hamamci_2024_ct2rep-automated-radiology-report-generation.md)]

**Advancing cancer detection and treatment using longitudinal routine clinical data** \
*Fei Liu, Kai Wang, Hui Xu, et al.* \
[Cell, 2026] [Wenzhou Medical University, Macau University of Science and Technology, Guangzhou National Laboratory] \
[[Paper](https://www.cell.com/cell/fulltext/S0092-8674(26)00807-X)] [[Github](https://github.com/kaiwang13/Oncoformer)] [[Note](notes/liu_2026_advancing-cancer-detection-treatment-longitudinal-data.md)]

## Resources

### Datasets

### Benchmarks

