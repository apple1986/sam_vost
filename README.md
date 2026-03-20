# Segment Anything for Video: A Comprehensive Review of Video Object Segmentation and Tracking from Past to Future

Guoping Xu1, Jayaram K. Udupa2, Yajun Yu1, Hua-Chieh Shao1, Songlin Zhao3, Wei Liu3, You Zhang1*

1 The Medical Artificial Intelligence and Automation (MAIA) Laboratory, Department of Radiation Oncology, University of Texas Southwestern Medical Center, Dallas, TX, USA  
2 Medical Image Processing Group, University of Pennsylvania, USA  
3 Department of Radiation Oncology, Mayo Clinic, USA  


## 1. Basic Architecture for VOST
The standard pipeline for Video Object Segmentation and Tracking consists of three primary components:

(1) Encoder: Extracts features from the current frame.


(2) Memory/Feature Update: Incorporates features from preceding frames to provide temporal-spatial cues, facilitating target recognition and differentiation.


(3) Decoder: Generates the final predicted mask for the current frame.


## 2. Representative Published Works

This document provides a comprehensive overview of Video Object Segmentation and Tracking (VOST) methods, including core mechanisms, advantages, limitations, and benchmark datasets for both natural and medical scenes.

---

# Segment Anything for Video: VOST Review

## 1. Basic Architecture for VOST
The standard pipeline for Video Object Segmentation and Tracking consists of three primary components:
1.  [cite_start]**Encoder**: Extracts features from the current frame[cite: 8].
2.  [cite_start]**Memory/Feature Update**: Incorporates features from preceding frames to provide temporal-spatial cues, facilitating target recognition and differentiation[cite: 8, 9].
3.  [cite_start]**Decoder**: Generates the final predicted mask for the current frame[cite: 10].


---

## 2. Representative Published Works

| Method | Publication | Core Mechanisms | Advantages & Limitations |
| :--- | :--- | :--- | :--- |
| **[MaskTrack ConvNet](https://ieeexplore.ieee.org/document/8100115)** | CVPR 2017 | [cite_start]Concatenates previous mask with current frame[cite: 12]. | [cite_start]Simple short-term propagation; fails with large appearance changes or drift[cite: 12]. |
| **[STM](https://arxiv.org/abs/1904.00607)** | ICCV 2019 | [cite_start]Space-Time Memory Network with key-value memory[cite: 12]. | [cite_start]Pioneer in memory mechanisms; high memory and computation requirements[cite: 12]. |
| **[AOT](https://arxiv.org/abs/2103.14158)** | NeurIPS 2021 | [cite_start]Transformer-based instance-level embeddings[cite: 12]. | [cite_start]Strong multi-object association; suffers from memory degradation[cite: 12]. |
| **[XMem](https://arxiv.org/abs/2207.07115)** | ECCV 2022 | [cite_start]Multi-store memory (sensory, short, and long-term)[cite: 12]. | [cite_start]Long-term retention; sensitive to extreme pose changes and shadows[cite: 12]. |
| **[DEVA](https://arxiv.org/abs/2309.03915)** | ICCV 2023 | [cite_start]Decouples image segmentation and temporal propagation[cite: 12]. | [cite_start]Flexible framework; complicated temporal propagation[cite: 12]. |
| **[SAM-Track](https://arxiv.org/abs/2305.04910)** | arXiv 2023 | [cite_start]Combines SAM, AOT tracking, and Grounding-DINO[cite: 12]. | [cite_start]Supports text-prompts; computationally expensive[cite: 12]. |
| **[SAM 2](https://arxiv.org/abs/2408.00714)** | arXiv 2024 | [cite_start]Streaming memory architecture with memory attention[cite: 21]. | [cite_start]Real-time performance; robustness depends on memory selection strategy[cite: 22]. |
| **[MedSAM2](https://arxiv.org/abs/2408.03357)** | arXiv 2024 | [cite_start]SAM2 adapted for medical video with temporal memory[cite: 25]. | [cite_start]Improves consistency in medical video; generalization is challenging[cite: 26]. |

---

## 3. Benchmarking Datasets

### Natural Scene Datasets
| Dataset | Website | Description |
| :--- | :--- | :--- |
| **SegTrack-v2** | [Link](https://web.engr.oregonstate.edu/~lif/SegTrack2/dataset.html) | [cite_start]Expanded benchmark with more objects and challenging sequences[cite: 125]. |
| **DAVIS17** | [Link](https://davischallenge.org/davis2017/code.html) | [cite_start]Multi-object extension with complex scenes and interactions[cite: 125]. |
| **YouTube-VOS** | [Link](https://youtube-vos.org/dataset/vos/) | [cite_start]Large-scale dataset with diverse real-world scenarios[cite: 125]. |
| **SA-V** | [Link](https://ai.meta.com/datasets/segment-anything-video/) | [cite_start]Massive dataset for fine-grained segmentation at scale[cite: 125]. |

### Medical Scenario Datasets
| Dataset | Website | Description |
| :--- | :--- | :--- |
| **Endovis18** | [Link](https://zenodo.org/records/10527017) | [cite_start]Robotic scene segmentation including anatomical objects[cite: 129]. |
| **EchoNet-Dynamic**| [Link](https://echonet.github.io/dynamic/index.html)| [cite_start]2D apical two-chamber heart videos[cite: 129]. |
| **SUN-SEG** | [Link](https://github.com/openmedlab/Awesome-Medical-Dataset/blob/main/resources/SUN-SEG.md)| [cite_start]Specialized for Polyp segmentation[cite: 129]. |
| **Cell Tracking** | [Link](https://celltrackingchallenge.net/datasets/) | [cite_start]Biological videos for cell segmentation and tracking[cite: 129]. |


```

## BibTeX
Please consider to cite it if it helps your research.

```latex
@article{xu2025segment,
  title={Segment anything for video: a comprehensive review of video object segmentation and tracking from past to future},
  author={Xu, Guoping and Udupa, Jayaram K and Yu, Yajun and Shao, Hua-Chieh and Zhao, Songlin and Liu, Wei and Zhang, You},
  journal={arXiv preprint arXiv:2507.22792},
  year={2025}
}

```
