<div align="center">

# Awesome Affordance Learning

**A curated collection of papers on affordance learning for embodied AI.**

[![Awesome](https://img.shields.io/badge/Awesome-0066CC?style=for-the-badge&logo=awesome-lists&logoColor=white)](https://github.com/hq-King/Awesome-Affordance-Learning) [![License](https://img.shields.io/badge/License-MIT-2E7D32?style=for-the-badge)](https://opensource.org/licenses/MIT) [![Last Commit](https://img.shields.io/github/last-commit/hq-King/Awesome-Affordance-Learning?style=for-the-badge&color=1F4E79)](https://github.com/hq-King/Awesome-Affordance-Learning/commits) [![GitHub Stars](https://img.shields.io/github/stars/hq-King/Awesome-Affordance-Learning?style=for-the-badge&logo=github&color=000000)](https://github.com/hq-King/Awesome-Affordance-Learning/stargazers)

</div>


<!-- <div align="center">

## From Passive Perception to Active Interaction: A Survey of Affordance Learning for Embodied AI

**Gen Li**<sup>1,#,‡</sup>, **Hanqing Wang**<sup>2,#</sup>, **Jingliang Li**<sup>1,#</sup>, **Yifan Han**<sup>3,#</sup>, **Jindou Jia**<sup>1</sup>, **Tao Lin**<sup>3</sup>, **Yutong Wang**<sup>4</sup>, **Bo Zhao**<sup>3</sup>, **Fangqiang Ding**<sup>2</sup>, **Anh Nguyen**<sup>5</sup>, **Laura Sevilla-Lara**<sup>6</sup>, **Gregory S. Chirikjian**<sup>7</sup>, **Huazhe Xu**<sup>8</sup>, **Marc Pollefeys**<sup>9</sup>, **Oier Mees**<sup>9</sup>, **Hui Xiong**<sup>2,†</sup>, **Jianfei Yang**<sup>1,†</sup>

<sup>1</sup>Nanyang Technological University &nbsp;&nbsp; <sup>2</sup>HKUST(GZ) &nbsp;&nbsp; <sup>3</sup>Shanghai Jiao Tong University
<sup>4</sup>The University of Sydney &nbsp;&nbsp; <sup>5</sup>University of Liverpool &nbsp;&nbsp; <sup>6</sup>The University of Edinburgh
<sup>7</sup>MBZUAI &nbsp;&nbsp; <sup>8</sup>Tsinghua University &nbsp;&nbsp; <sup>9</sup>ETH Zurich

<sup>#</sup>Equal Contribution &nbsp;&nbsp; <sup>‡</sup>Project Lead &nbsp;&nbsp; <sup>†</sup>Corresponding Author

</div> -->


> 🧭 Exploring Embodied AI and Embodied perception? We hope this collection proves useful in your journey. If you'd like to support the project, feel free to ⭐️ the repo and share it with your peers. Contributions are warmly welcome!



## 📖 Contents

- [Awesome Affordance Learning](#awesome-affordance-learning)
- [🔥 News](#-news)
- [🌟 Introduction](#-introduction)
- [🧭 Taxonomy](#-taxonomy)
- [📄 Paper List](#-paper-list)
  - [👁️ Affordance Perception](#perception)
  - [🧠 Affordance Reasoning](#reasoning)
  - [🤖 Affordance-Guided Action](#action)
  - [📊 Affordance Datasets / Benchmarks](#affordance-datasets-benchmarks)
  - [📚 Related Surveys](#related-surveys)
- [🎉 Contributing](#-contributing)
- [🌟 Acknowledgment](#-acknowledgment)
- [📄 License](#-license)
- [👥 Contributors](#-contributors)



## 🔥 News

> 📢 This list is **actively maintained**, and community contributions are always appreciated!  
> Feel free to [open a pull request](https://github.com/hq-King/Awesome-Affordance-Learning/pulls) if you find any relevant papers.

- **[2025-05]** 🎉 This repository was launched to curate a comprehensive list of affordance-learning research.


## 🌟 Introduction

This repository accompanies the survey **From Passive Perception to Active Interaction: A Survey of Affordance Learning for Embodied AI** and maintains a curated collection of papers, datasets, and benchmarks.

As robots and embodied agents move into real-world applications, they must understand not only what objects are, but also where, why, and how they can interact with them. Following the survey, the list is organized around three complementary questions:

- **Affordance Perception:** Where or which region affords an interaction?
- **Affordance Reasoning:** Which affordance is relevant under the current task, environment, and constraints?
- **Affordance-Guided Action:** How can an affordance be converted into an executable action?

A paper may be cross-referenced when the survey discusses it in more than one role (for example, both perception and reasoning). A separate section collects datasets and benchmarks. Venue labels use the formally published version whenever one is available; otherwise the first public preprint is marked `arXiv`.


## 🧭 Taxonomy

The taxonomy follows the survey's functional pipeline rather than only model architecture. It expands each primary category into second- and third-level categories. Cross-listing is intentional when a method contributes to multiple stages or perspectives.

| Primary Category | Secondary Category | Third-Level Categories | Main Distinction |
|---|---|---|---|
| Affordance Perception | Visual affordance perception | Object-centric grounding; scene-level grounding; weakly supervised perception | Grounds masks, heatmaps, or keypoints on the 2D image plane. |
| Affordance Perception | Spatial affordance perception | 3D object grounding; 3D scene grounding | Grounds functional regions or geometric structures directly in metric 3D space. |
| Affordance Perception | Interaction-driven affordance perception | Demonstration/HOI video; HOI image; interaction-conditioned 3D; interaction-grounded scene perception | Derives supervision or context from observed human-object interactions. |
| Affordance Perception | Generalizable affordance perception | Example-based transfer; open-set grounding | Transfers to novel objects, labels, queries, or interaction contexts. |
| Affordance Reasoning | Relation-based reasoning | Probabilistic/semantic relations; object-pair and scene context; manipulation graphs | Infers affordances through explicit relations among objects, actions, agents, and scene context. |
| Affordance Reasoning | Language-centric reasoning | Grounded skill selection; integrated LLM/MLLM prediction; modular semantic-to-spatial grounding; sequential reasoning | Uses language to interpret intent and select or ground task-relevant affordances. |
| Affordance Reasoning | Agentic reasoning | Predefined workflows; adaptive workflows | Uses planning, memory, verification, or iterative tool/model calls over multiple steps. |
| Affordance-Guided Action | Hierarchical affordance-to-action | Primitive-based execution; retrieval-based transfer; planner-based execution | Predicts affordances first and then converts them into actions through a separate execution module. |
| Affordance-Guided Action | Affordance-integrated policy learning | Affordance as explicit input; implicit representation; optimization signal | Integrates affordance information directly into policy representation, input, or optimization. |


## 📄 Paper List

The **Venue/Date** column prioritizes the formal venue and publication year. Papers without a confirmed venue are labeled `arXiv`. The **Name** column records the method or system name explicitly introduced by the authors, including names stated only in the abstract or main text rather than in the title; `-` means that no explicit method name has been verified and no acronym is inferred from the title.

<a id="perception"></a>
### 👁️ Affordance Perception

| Venue/Date | Name | Title | Paper | Scope | Perception Subcategory |
| :-: | :-: | :- | :-: | :-: | :-: |
| IJRR 2013 | - | Learning Human Activities and Object Affordances from RGB-D Videos | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://dl.acm.org/doi/abs/10.1177/0278364913478446) | Scene | Interaction-driven |
| ICRA 2015 | `UMD` | Affordance Detection of Tool Parts from Geometric Features | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](http://users.umiacs.umd.edu/~fermulcm/affordance/ICRA15_affordance_parts_final.pdf) | Object | Visual · Spatial |
| ECCV 2016 | - | A Multi-scale CNN for Affordance Segmentation in RGB Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://web.engr.oregonstate.edu/~sinisa/research/publications/eccv16_affordance.pdf) | Scene | Visual |
| IROS 2016 | - | Detecting Object Affordances with Convolutional Neural Networks | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://www.csc.liv.ac.uk/~anguyen/assets/pdfs/2016_IROS_Affordance.pdf) | Object | Visual |
| CVPR 2017 | - | Weakly Supervised Affordance Detection | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content_cvpr_2017/papers/Sawatzky_Weakly_Supervised_Affordance_CVPR_2017_paper.pdf) | Object | Visual |
| IROS 2017 | - | Object-Based Affordances Detection with Convolutional Neural Networks and Dense Conditional Random Fields | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://ieeexplore.ieee.org/document/8206484/) | Object | Visual |
| ICCVW 2017 | - | Adaptive Binarization for Weakly Supervised Affordance Segmentation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/1707.02850) | Object | Visual |
| ICCVW 2017 | - | Learning to Segment Affordances | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content_ICCV_2017_workshops/papers/w14/Luddecke_Learning_to_Segment_ICCV_2017_paper.pdf) | Object/Scene | Visual |
| Humanoids 2017 | - | Affordance Detection for Task-Specific Grasping Using Deep Learning | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://ieeexplore.ieee.org/abstract/document/8239542) | Object | Visual |
| ICRA 2018 | `AffordanceNet` | AffordanceNet: An End-to-End Deep Learning Approach for Object Affordance Detection | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/1709.07326) | Object | Visual |
| CVPR 2018 | `Demo2Vec` | Demo2Vec: Reasoning Object Affordances from Online Videos | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content_cvpr_2018/papers/Fang_Demo2Vec_Reasoning_Object_CVPR_2018_paper.pdf) | Object | Visual · Interaction-driven |
| ECCV 2018 | `Gaze + Action` | In the Eye of Beholder: Joint Learning of Gaze and Actions in First Person Video | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content_ECCV_2018/html/Yin_Li_In_the_Eye_ECCV_2018_paper.html) | Scene | Interaction-driven |
| Autonomous Robots 2019 | - | Towards Affordance Detection for Robot Manipulation Using Affordance for Parts and Parts for Affordance | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://link.springer.com/article/10.1007/s10514-018-9787-5) | Object | Visual |
| RAS 2019 | - | Context-Based Affordance Segmentation from 2D Images for Robot Actions | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://www.sciencedirect.com/science/article/abs/pii/S0921889018309990) | Object | Visual |
| RA-L with ICRA 2019 | `AffordanceLearn` | Learning Affordance Segmentation for Real-world Robotic Manipulation via Synthetic Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://sites.google.com/view/affordance-learn) | Object | Visual |
| arXiv 2019 | `AffContext` | Recognizing Object Affordances to Support Scene Reasoning for Manipulation Tasks | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/1909.05770) | Object | Visual |
| ICCV 2019 | `Interaction Hotspots` | Grounded Human-Object Interaction Hotspots From Video | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content_ICCV_2019/html/Nagarajan_Grounded_Human-Object_Interaction_Hotspots_From_Video_ICCV_2019_paper.html) | Object | Visual · Interaction-driven |
| CVPR 2020 | `Ego-Topo` | Ego-Topo: Environment Affordances from Egocentric Video | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2001.04583) | Scene | Interaction-driven |
| NeurIPS 2020 | `IntExp` | Learning Affordance Landscapes for Interaction Exploration in 3D Environments | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://proceedings.neurips.cc/paper_files/paper/2020/hash/15825aee15eb335cc13f9b559f166ee8-Abstract.html) | Scene | Spatial |
| Neural Comput. Appl. 2020.09 | - | Object Affordance Detection with Relationship-Aware Network | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1007/s00521-019-04336-0) | Object | Visual |
| RA-L with ICRA2021 | `AffKp` | An Affordance Keypoint Detection Network for Robot Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://sites.google.com/view/affordancekp/home) | Object | Visual |
| ACM ICDAR 2021 | `ST-HOI` | ST-HOI: A Spatial-Temporal Baseline for Human-Object Interaction Detection in Videos | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://dl.acm.org/doi/10.1145/3463944.3469097) | Scene | Interaction-driven |
| CVPR 2021 | `3D AffordanceNet` | 3D AffordanceNet: A Benchmark for Visual Object Affordance Understanding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2103.16397) | Object | Spatial |
| CoRL 2021 | `O2O-Afford` | O2O-Afford: Annotation-Free Large-Scale Object-Object Affordance Learning | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2106.15087) | Object-pair | Spatial |
| Neurocomputing 2021 | - | Visual Affordance Detection Using an Efficient Attention Convolutional Neural Network | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1016/j.neucom.2021.01.018) | Object | Visual |
| IJCAI 2021 | `OS-AD` | One-Shot Affordance Detection | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2106.14747) | Object | Visual · Generalizable |
| Humanoids 2022 | `ACF` | Manipulation-Oriented Object Perception in Clutter through Affordance Coordinate Frames | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2010.08202) | Object | Spatial |
| ECCVW 2022 | `PartAfford` | PartAfford: Part-level Affordance Discovery from 3D Objects | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2202.13519) | Object | Spatial |
| CVPR 2022 | `OCT` | Joint Hand Motion and Interaction Hotspots Prediction from Egocentric Videos | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2204.01696) | Object | Visual · Interaction-driven |
| CVPR 2022 | `Cross-view-AG` | Learning Affordance Grounding from Exocentric Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2203.09905) | Object | Visual · Interaction-driven |
| CoRL 2022 | `AffCorrs` | One-Shot Transfer of Affordance Regions? AffCorrs! | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2209.07147) | Object | Visual · Generalizable |
| Neural Comput. Appl. 2022 | `BPN` | Object Affordance Detection with Boundary-Preserving Network for Robotic Manipulation Tasks | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1007/s00521-022-07446-4) | Object | Visual |
| IJCV 2022 | `OSAD-Net` | One-Shot Object Affordance Detection in the Wild | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2108.03658) | Object | Visual · Generalizable |
| WACV 2023 | - | Fine-Grained Affordance Annotation for Egocentric Hand-Object Interaction Videos | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/WACV2023/html/Yu_Fine-Grained_Affordance_Annotation_for_Egocentric_Hand-Object_Interaction_Videos_WACV_2023_paper.html) | Object | Interaction-driven |
| arXiv 2023 | `STRAP` | STRAP: Structured Object Affordance Segmentation with Point Supervision | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2304.08492) | Object | Visual |
| CVPR 2023 | `Afformer` | Affordance Grounding From Demonstration Video To Target Image | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2303.14644) | Object | Interaction-driven |
| CVPR 2023 |  | Leverage Interactive Affinity for Affordance Learning | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/CVPR2023/html/Luo_Leverage_Interactive_Affinity_for_Affordance_Learning_CVPR_2023_paper.html) | Object | Visual · Interaction-driven |
| CVPR 2023 | `LOCATE` | LOCATE: Localize and Transfer Object Parts for Weakly Supervised Affordance Grounding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2303.09665) | Object | Visual · Interaction-driven |
| NeurIPS 2023 | `Where2Explore` | Where2Explore: Few-shot Affordance Learning for Unseen Novel Categories of Articulated Objects | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2309.07473) | Object | Spatial · Generalizable |
| ICIP 2023 | - | A Large Scale Multi-View RGBD Visual Affordance Learning Dataset | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2203.14092) | Object | Visual |
| IROS 2023 | `VAT` | Hierarchical Transformer for Visual Affordance Understanding using a Large-scale Dataset | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/IROS55552.2023.10341976) | Object | Visual |
| ICCV 2023 | `AffordPose` | AffordPose: A Large-Scale Dataset of Hand-Object Interactions with Affordance-Driven Hand Pose | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/ICCV2023/html/Jian_AffordPose_A_Large-Scale_Dataset_of_Hand-Object_Interactions_with_Affordance-Driven_Hand_ICCV_2023_paper.html) | Object | Spatial · Interaction-driven |
| IROS 2023 | `HANDAL` | HANDAL: A Dataset of Real-World Manipulable Object Categories with Pose Annotations, Affordances, and Reconstructions | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2308.01477) | Object | Visual · Spatial |
| ICCV 2023 | `IAGNet` | Grounding 3D Object Affordance from 2D Interactions in Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2303.10437) | Object | Spatial · Interaction-driven |
| ICCV 2023 | - | Understanding 3D Object Interaction from a Single Image | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/ICCV51070.2023.01988) | Scene | Spatial |
| ICCV 2023 | `EPIC-Aff` | Multi-label Affordance Mapping from Egocentric Vision | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/ICCV2023/html/Mur-Labadia_Multi-label_Affordance_Mapping_from_Egocentric_Vision_ICCV_2023_paper.html) | Scene | Spatial · Interaction-driven |
| IROS 2023 | `OpenAD` | Open-vocabulary Affordance Detection in 3D Point Clouds | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2303.02401) | Object | Spatial · Generalizable |
| ICRA 2024 | - | Open-Vocabulary Affordance Detection using Knowledge Distillation and Text-Point Correlation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2309.10932) | Object | Spatial · Generalizable |
| CVPR 2024 | `LEMON` | LEMON: Learning 3D Human-Object Interaction Relation from 2D Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2312.08963) | Object | Spatial · Interaction-driven |
| AAAI 2024 | `WSMA` | Weakly Supervised Multimodal Affordance Grounding for Egocentric Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://ojs.aaai.org/index.php/AAAI/article/view/28451) | Object | Visual · Interaction-driven |
| arXiv 2024 | - | Text-driven Affordance Learning from Egocentric Vision | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2404.02523) | Object | Interaction-driven |
| ICRA 2024 | `3DAPNet` | Language-Conditioned Affordance-Pose Detection in 3D Point Clouds | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/ICRA57147.2024.10610008) | Object | Spatial · Generalizable |
| CVPR 2024 | `OOAL` | One-Shot Open Affordance Learning with Foundation Models | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2311.17776) | Object | Visual · Generalizable |
| CVPR 2024 | `LASO` | LASO: Language-guided Affordance Segmentation on 3D Object | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/CVPR2024/papers/Li_LASO_Language-guided_Affordance_Segmentation_on_3D_Object_CVPR_2024_paper.pdf) | Object | Spatial · Generalizable |
| CVPRW 2024 | `LGAfford-Net` | LGAfford-Net: A Local Geometry Aware Affordance Detection Network for 3D Point Clouds | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/CVPRW63382.2024.00535) | Object | Spatial |
| CVPR 2024 | `SceneFun3D` | SceneFun3D: Fine-Grained Functionality and Affordance Understanding in 3D Scenes | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/CVPR2024/papers/Delitzas_SceneFun3D_Fine-Grained_Functionality_and_Affordance_Understanding_in_3D_Scenes_CVPR_2024_paper.pdf) | Scene | Spatial |
| arXiv 2024 | `Ego-SAG` | Grounding 3D Scene Affordance From Egocentric Interactions | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2409.19650) | Scene | Interaction-driven · Spatial |
| ECCV 2024 | `INTRA` | INTRA: Interaction Relationship-aware Weakly Supervised Affordance Grounding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2409.06210) | Object | Visual · Interaction-driven |
| ECCV 2024 | `ComA` | Beyond the Contact: Discovering Comprehensive Affordance for 3D Objects from Pre-trained 2D Diffusion Models | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1007/978-3-031-72983-6_23) | Object | Spatial |
| IROS 2024 | `FAKP-Net` | 3D Affordance Keypoint Detection for Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/IROS58592.2024.10801792) | Object | Spatial |
| ICCV 2025 | `GLANCE` | GLANCE: Intermediate Connectors and Geometric Priors for Language-Guided Affordance Segmentation on Unseen Object Categories | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://ieeexplore.ieee.org/abstract/document/11445074) | Object | Spatial · Generalizable |
| AAAI 2025 | `MIFAG` | Learning 2D Invariant Affordance Knowledge for 3D Affordance Grounding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2408.13024) | Object | Spatial · Interaction-driven |
| CVPR 2025 | `GEAL` | GEAL: Generalizable 3D Affordance Learning with Cross-Modal Consistency | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2412.09511) | Object | Spatial · Generalizable |
| AAAI 2025 | `MaskPrompt` | MaskPrompt: Open-Vocabulary Affordance Segmentation with Object Shape Mask Prompts | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://ojs.aaai.org/index.php/AAAI/article/view/32200) | Object | Visual · Generalizable |
| arXiv 2025 | `AffordanceSAM` | AffordanceSAM: Segment Anything Once More in Affordance Grounding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2504.15650) | Object | Visual · Generalizable |
| CVPR 2025 | `IAAO` | IAAO: Interactive Affordance Learning for Articulated Objects in 3D Environments | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2504.06827) | Object | Spatial |
| arXiv 2025 | - | Interpretable Affordance Detection on 3D Point Clouds with Probabilistic Prototypes | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2504.18355) | Object | Spatial |
| arXiv 2025 | - | Weakly-Supervised Affordance Grounding Guided by Part-Level Semantic Priors | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2505.24103) | Object | Visual |
| ICRA 2025 | `UAD` | UAD: Unsupervised Affordance Distillation for Generalization in Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2506.09284) | Object | Visual · Generalizable |
| CVPR 2025 | `Reasoning Mamba` | Reasoning Mamba: Hypergraph-Guided Region Relation Calculating for Weakly Supervised Affordance Grounding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/CVPR2025/papers/Wang_Reasoning_Mamba_Hypergraph-Guided_Region_Relation_Calculating_for_Weakly_Supervised_Affordance_CVPR_2025_paper.pdf) | Object | Visual |
| IROS 2025 | `OS-AGDO` | One-Shot Affordance Grounding of Deformable Objects in Egocentric Organizing Scenes | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2503.01092) | Object | Visual · Generalizable |
| IROS 2025 | `BiT-Align` | Resource-Efficient Affordance Grounding with Complementary Depth and Semantic Prompts | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2503.02600) | Object | Visual |
| ICCV 2025 | `LoopTrans` | Closed-Loop Transfer for Weakly-supervised Affordance Grounding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2510.17384) | Object | Visual |
| ICCV 2025 | - | Selective Contrastive Learning for Weakly Supervised Affordance Grounding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/ICCV2025/html/Moon_Selective_Contrastive_Learning_for_Weakly_Supervised_Affordance_Grounding_ICCV_2025_paper.html) | Object | Visual |
| ICCV 2025 | `OVA-Fields` | OVA-Fields: Weakly Supervised Open-Vocabulary Affordance Fields for Robot Operational Part Detection | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/ICCV2025/papers/Su_OVA-Fields_Weakly_Supervised_Open-Vocabulary_Affordance_Fields_for_Robot_Operational_Part_ICCV_2025_paper.pdf) | Object | Spatial · Generalizable |
| CVPR 2025 | `FunGraph3D` | Open-Vocabulary Functional 3D Scene Graphs for Real-World Indoor Spaces | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2503.19199) | Scene | Spatial |
| ACM MM 2025 | `RoboAfford` | RoboAfford: A Dataset and Benchmark for Enhancing Object and Spatial Affordance Learning in Robot Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1145/3746027.3755653) | Object/Scene | Visual · Spatial |
| ECCV 2026 | `Affogato` | Affogato: Learning Open-Vocabulary Affordance Grounding with Automated Data Generation at Scale | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2506.12009) | Object | Visual · Spatial · Generalizable |
| CVPR 2026 | `Affostruction` | Affostruction: 3D Affordance Grounding with Generative Reconstruction | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2601.09211) | Object | Spatial |
| arXiv 2026 | `PanoAffordanceNet` | PanoAffordanceNet: Towards Holistic Affordance Grounding in 360° Indoor Environments | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2603.09760) | Scene | Visual |
| ECCV 2026 | `PAP` | Panoramic Affordance Prediction | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2603.15558) | Scene | Visual |
| CVPR 2026 | `AffordMatcher` | AffordMatcher: Affordance Learning in 3D Scenes from Visual Signifiers | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2603.27970) | Scene | Spatial |
| ECCV 2026 | `DAG` | Diffusion Models are Open-World Affordance Learners: Leveraging Generative Priors for 3D Affordance Learning | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2508.01651) | Object | Spatial · Generalizable |
| CVPR 2026 | `FunREC` | FunREC: Reconstructing Functional 3D Scenes from Egocentric Interaction Videos | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2604.05621) | Scene | Interaction-driven · Spatial |
| arXiv 2026 | `AFUN` | AFUN: Towards an Affordance Foundation Model for Functionality Understanding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2606.02551) | Object | Visual · Spatial · Generalizable |

<a id="reasoning"></a>
### 🧠 Affordance Reasoning

| Venue/Date | Name | Title | Paper | Reasoning Subcategory |
| :-: | :-: | :- | :-: | :-: |
| ECCV 2014 | - | Reasoning about Object Affordances in a Knowledge Base Representation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://link.springer.com/chapter/10.1007/978-3-319-10605-2_27) | Relation-Based Affordance Reasoning |
| TCDS 2016 | - | Bootstrapping Relational Affordances of Object Pairs Using Transfer | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/TCDS.2016.2616496) | Relation-Based Affordance Reasoning |
| CVPR 2018 | - | Learning to Act Properly: Predicting and Explaining Affordances From Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content_cvpr_2018/html/Chuang_Learning_to_Act_CVPR_2018_paper.html) | Relation-Based Affordance Reasoning |
| RA-L/IROS 2019 | - | Learning Grasp Affordance Reasoning through Semantic Relations | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/1906.09836) | Relation-Based Affordance Reasoning |
| ICRA 2020 | - | Learning Object Placements For Relational Instructions by Hallucinating Scene Representations | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2001.08481) | Relation-Based Affordance Reasoning |
| arXiv 2021 | `AR-Net` | Relationship Oriented Affordance Learning through Manipulation Graph Construction | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2110.14137) | Relation-Based Affordance Reasoning |
| ICDH 2022 | `VAR-Net` | A Visual Affordance Reasoning Network Based on Graph Attention | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://ieeexplore.ieee.org/document/9978423) | Relation-Based Affordance Reasoning |
| CoRL 2023 | `SayCan` | Do As I Can, Not As I Say: Grounding Language in Robotic Affordances | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2204.01691) | Agentic Affordance Reasoning |
| NeurIPS 2023 | `Grounded Decoding` | Grounded Decoding: Guiding Text Generation with Grounded Models for Embodied Agents | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2303.00855) | Agentic Affordance Reasoning |
| CVPRW 2024 | `AffordanceLLM` | AffordanceLLM: Grounding Affordance from Vision Language Models | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2401.06341) | Language-Centric Affordance Reasoning |
| RA-L 2024 | `NaturalVLM` | NaturalVLM: Leveraging Fine-grained Natural Language for Affordance-Guided Visual Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2403.08355) | Language-Centric Affordance Reasoning |
| ICRAW 2024 | `OVAL-Prompt` | OVAL-Prompt: Open-Vocabulary Affordance Localization for Robot Manipulation through LLM Affordance-Grounding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2404.11000) | Language-Centric Affordance Reasoning |
| ICTAI 2024 | `WorldAfford` | WorldAfford: Affordance Grounding based on Natural Language Instructions | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2405.12461) | Language-Centric Affordance Reasoning |
| CoRL 2024 | `RoboPoint` | RoboPoint: A Vision-Language Model for Spatial Affordance Prediction for Robotics | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2406.10721) | Language-Centric Affordance Reasoning |
| IROS 2024 | `ManipVQA` | ManipVQA: Injecting Robotic Affordance and Physically Grounded Information into Multi-Modal Large Language Models | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2403.11289) | Language-Centric Affordance Reasoning |
| IROS 2025 | `PAVLM` | PAVLM: Advancing Point Cloud based Affordance Understanding Via Vision-Language Model | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2410.11564) | Language-Centric Affordance Reasoning |
| CVPR 2025 | `GREAT` | GREAT: Geometry-Intention Collaborative Inference for Open-Vocabulary 3D Object Affordance Grounding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2411.19626) | Language-Centric Affordance Reasoning |
| CVPR 2025 | `SeqAfford` | SeqAfford: Sequential 3D Affordance Reasoning via Multimodal Large Language Model | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2412.01550) | Language-Centric Affordance Reasoning |
| ICLR 2025 | `3D-AffordanceLLM` | 3D-AffordanceLLM: Harnessing Large Language Models for Open-Vocabulary Affordance Detection in 3D Worlds | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2502.20041) | Language-Centric Affordance Reasoning |
| arXiv 2025 | `Afford-X` | Afford-X: Generalizable and Slim Affordance Reasoning for Task-oriented Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2503.03556) | Language-Centric Affordance Reasoning |
| CVPR 2025 | `LMAffordance3D` | Grounding 3D Object Affordance with Language Instructions, Visual Observations and Interactions | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2504.04744) | Language-Centric Affordance Reasoning |
| ACM MM 2025 | `3DAffordSplat` | 3DAffordSplat: Efficient Affordance Reasoning with 3D Gaussians | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2504.11218) | Language-Centric Affordance Reasoning |
| ICRA 2025 | `UniAff` | UniAff: A Unified Representation of Affordances for Tool Usage and Articulation with Vision-Language Models | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2409.20551) | Language-Centric Affordance Reasoning |
| ACL 2025 | `InstructPart` | InstructPart: Task-Oriented Part Segmentation with Instruction Reasoning | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2505.18291) | Language-Centric Affordance Reasoning |
| CVPR 2025 | `Fun3DU` | Functionality Understanding and Segmentation in 3D Scenes | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2411.16310) | Language-Centric Affordance Reasoning |
| ICCV 2025 | `RAGNet` | RAGNet: Large-scale Reasoning-based Affordance Segmentation Benchmark towards General Grasping | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2507.23734) | Language-Centric Affordance Reasoning |
| arXiv 2025 | `SeqAffordSplat` | SeqAffordSplat: Scene-level Sequential Affordance Reasoning on 3D Gaussian Splatting | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2507.23772) | Language-Centric Affordance Reasoning |
| arXiv 2025 | `ASP` | Agentic Scene Policies: Unifying Space, Semantics, and Affordances for Robot Action | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2509.19571) | Agentic Affordance Reasoning |
| ACM MM 2025 | `Aff3DFunc` | Open-Vocabulary 3D Affordance Understanding via Functional Text Enhancement and Multilevel Representation Alignment | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://eprints.gla.ac.uk/360521/) | Language-Centric Affordance Reasoning |
| IROS 2025 | `AffordGrasp` | AffordGrasp: In-Context Affordance Reasoning for Open-Vocabulary Task-Oriented Grasping in Clutter | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/IROS60139.2025.11245995) | Language-Centric Affordance Reasoning |
| NeurIPS 2025 | `AffordBot` | AffordBot: 3D Fine-grained Embodied Reasoning via Multimodal Large Language Models | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2511.10017) | Language-Centric Affordance Reasoning |
| IROSW 2025 | `RoboAfford++` | RoboAfford++: A Generative AI-Enhanced Dataset for Multimodal Affordance Learning in Robotic Manipulation and Navigation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2511.12436) | Language-Centric Affordance Reasoning |
| NeurIPS 2025 | `ViSPLA` | ViSPLA: Visual Iterative Self-Prompting for Language-Guided 3D Affordance Learning | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://neurips.cc/virtual/2025/poster/119081) | Language-Centric Affordance Reasoning |
| ICASSP 2026 | `A4Bench` | Affordance Benchmark for MLLMs | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2506.00893) | Language-Centric Affordance Reasoning |
| AAAI 2026 | `Affordance-R1` | Affordance-R1: Reinforcement Learning for Generalizable Affordance Reasoning in Multimodal Large Language Model | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2508.06206) | Language-Centric Affordance Reasoning |
| AAAI 2026 | `TASA` | Task-Aware 3D Affordance Segmentation via 2D Guidance and Geometric Refinement | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2511.11702) | Language-Centric Affordance Reasoning |
| ECCV 2026 | `A4-Agent` | A4-Agent: An Agentic Framework for Zero-Shot Affordance Reasoning | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2512.14442) | Agentic Affordance Reasoning |
| arXiv 2026 | `TRACER` | TRACER: Texture-Robust Affordance Chain-of-Thought for Deformable-Object Refinement | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2601.20208) | Language-Centric Affordance Reasoning |
| arXiv 2026 | `AffordanceGrasp-R1` | AffordanceGrasp-R1: Leveraging Reasoning-Based Affordance Segmentation with Reinforcement Learning for Robotic Grasping | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2602.03547) | Language-Centric Affordance Reasoning |
| arXiv 2026 | `VideoAfford` | VideoAfford: Grounding 3D Affordance from Human-Object-Interaction Videos via Multimodal Large Language Model | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2602.09638) | Language-Centric Affordance Reasoning |
| arXiv 2026 | `SceneTeract` | SceneTeract: Agentic Functional Affordances and VLM Grounding in 3D Scenes | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2603.29798) | Agentic Affordance Reasoning |
| arXiv 2026 | - | Part-Aware Open-Vocabulary 3D Affordance Grounding via Prototypical Semantic and Geometric Alignment | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2603.17647) | Language-Centric Affordance Reasoning |
| arXiv 2026 | `A3R` | A3R: Agentic Affordance Reasoning via Cross-Dimensional Evidence in 3D Gaussian Scenes | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2604.01882) | Agentic Affordance Reasoning |
| ECCV 2026 | `TokAG` | Token-Based Affordance Grounding with Large Vision-Language Models | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2607.03595) | Language-Centric Affordance Reasoning |
| arXiv 2026 | `CompassAD` | CompassAD: Intent-Driven 3D Affordance Grounding in Functionally Competing Objects | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2604.02060) | Language-Centric Affordance Reasoning |
| arXiv 2026 | `A-Harness` | Affordance Agent Harness: Verification-Gated Skill Orchestration | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2605.00663) | Agentic Affordance Reasoning |
| arXiv 2026 | `AffordMEM` | Grounding by Remembering: Cross-Scene and In-Scene Memory for 3D Functional Affordances | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2605.11616) | Agentic Affordance Reasoning |
<a id="action"></a>
### 🤖 Affordance-Guided Action

| Venue/Date | Name | Title | Paper | Architecture | Affordance Usage | Action Subcategory |
| :-: | :-: | :- | :-: | :-: | :-: | :-: |
| IEEE TCDS 2016 | - | Training Agents With Interactive Reinforcement Learning and Contextual Affordances | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/TCDS.2016.2543839) | E2E | reward | Integrated policy · Optimization signal |
| ICRA 2020 | `ASPN` | Learning Affordance Space in Physical World for Vision-based Robotic Object Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://ieeexplore.ieee.org/abstract/document/9196783) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICRA 2021 | `GRAFF` | Learning Dexterous Grasping with Object-Centric Visual Affordances | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2009.01439) | E2E | reward | Integrated policy · Optimization signal |
| ICRA 2021 | `VAL` | What Can I Do Here? Learning New Skills by Imagining Visual Affordances | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2106.00671) | E2E | reward | Integrated policy · Optimization signal |
| ICRA 2021 | `Contact-GraspNet` | Contact-GraspNet: Efficient 6-DoF Grasp Generation in Cluttered Scenes | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2103.14127) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICCV 2021 | `Where2Act` | Where2Act: From Pixels to Actions for Articulated 3D Objects | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2101.02692) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ECCV 2022 | `AdaAfford` | AdaAfford: Learning to Adapt Manipulation Affordance for 3D Articulated Objects via Few-shot Interactions | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2112.00246) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICRA 2022 | `VAPO` | Affordance Learning from Play for Sample-Efficient Policy Learning | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2203.00352) | E2E | reward | Integrated policy · Optimization signal |
| IROS 2022 | - | Learning 6-DoF Task-oriented Grasp Detection via Implicit Estimation and Visual Affordance | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2210.08537) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICLR 2022 | `VAT-Mart` | VAT-Mart: Learning Visual Action Trajectory Proposals for Manipulating 3D Articulated Objects | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2106.14440) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICRA 2023 | `HULC++` | Grounding Language with Visual Affordances over Unstructured Data | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2210.01911) | E2E | implicit | Integrated policy · Implicit representation |
| ICLR 2023 | `DualAfford` | DualAfford: Learning Collaborative Visual Affordance for Dual-gripper Object Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2207.01971) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICRA 2023 | `RLAfford` | RLAfford: End-to-End Affordance Learning for Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2209.12941) | E2E | implicit | Integrated policy · Implicit representation |
| ICRA 2023 | - | Visual Affordance Prediction for Guiding Robot Exploration | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2305.17783) | E2E | reward | Integrated policy · Optimization signal |
| CoRL 2023 | `ACE-NBV` | Affordance-Driven Next-Best-View Planning for Robotic Grasping | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2309.09556) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| NeurIPS 2023 | - | Learning Environment-aware Affordance for 3D Articulated Object Manipulation under Occlusions | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2309.07510) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| CoRL 2023 | `LERF-TOGO` | Language Embedded Radiance Fields for Zero-Shot Task-Oriented Grasping | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2309.07970) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| CoRL 2023 | `VoxPoser` | VoxPoser: Composable 3D Value Maps for Robotic Manipulation with Language Models | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2307.05973) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| CVPR 2023 | `VRB` | Affordances from Human Videos as a Versatile Representation for Robotics | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2304.08488) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICCV 2023 | `DefoAfford` | Learning Foresightful Dense Visual Affordance for Deformable Object Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2303.11057) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| IEEE T-RO 2024 | `PRIMP` | PRIMP: Probabilistically-Informed Motion Primitives for Efficient Affordance Learning from Demonstration | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/TRO.2024.3390052) | Motion primitives | explicit | Hierarchical affordance-to-action · Primitive-based |
| arXiv 2024 | `AnyPart` | Open-Vocabulary Part-Based Grasping | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2406.05951) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICRA 2024 | `IDA` | Information-driven Affordance Discovery for Efficient Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/ICRA57147.2024.10611170) | Hierarchical model | reward | Hierarchical affordance-to-action · Planner-based |
| arXiv 2024 | - | Affordance-based Robot Manipulation with Flow Matching | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2409.01083) | E2E | explicit | Integrated policy · Explicit input |
| CoRL 2024 | `ReKep` | ReKep: Spatio-Temporal Reasoning of Relational Keypoint Constraints for Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2409.01652) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ECCV 2024 | `Robo-ABC` | Robo-ABC: Affordance Generalization Beyond Categories via Semantic Correspondence for Robot Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2401.07487) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| IROS 2024 | `PreAfford` | PreAfford: Universal Affordance-Based Pre-Grasping for Diverse Objects and Environments | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2404.03634) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| CoRL 2024 | `RAM` | RAM: Retrieval-Based Affordance Transfer for Generalizable Zero-Shot Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://proceedings.mlr.press/v270/kuang25a.html) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICCV 2025 | `GAT` | Learning Precise Affordances from Egocentric Videos for Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/ICCV2025/html/Li_Learning_Precise_Affordances_from_Egocentric_Videos_for_Robotic_Manipulation_ICCV_2025_paper.html) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICRA 2025 | `RT-Affordance` | RT-Affordance: Affordances are Versatile Intermediate Representations for Robot Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2411.02704) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| IROS 2025 | `ManipGPT` | ManipGPT: Is Affordance Segmentation by Large Vision Models Enough for Articulated Object Manipulation? | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2412.10050) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICCV 2025 | `AffordDexGrasp` | AffordDexGrasp: Open-set Language-guided Dexterous Grasp with Generalizable-Instructive Affordance | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2503.07360) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| CVPR 2025 | `GarmentPile` | GarmentPile: Point-Level Visual Affordance Guided Retrieval and Adaptation for Cluttered Garments Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2503.09243) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| ICCV 2025 | `A0` | A0: An Affordance-Aware Hierarchical Model for General Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://a-embodied.github.io/A0/) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| IEEE CBS 2025 | `DORA` | DORA: Object Affordance-Guided Reinforcement Learning for Dexterous Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2505.14819) | E2E | reward | Integrated policy · Optimization signal |
| CoRL 2025 | `GLOVER++` | GLOVER++: Unleashing the Potential of Affordance Learning from Human Behaviors for Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2505.11865) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| CVPR 2025 | `AffordDP` | AffordDP: Generalizable Diffusion Policy with Transferable Affordance | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2412.03142) | E2E | explicit | Integrated policy · Explicit input |
| ICML 2025 | `BiAssemble` | BiAssemble: Learning Collaborative Affordance for Bimanual Geometric Assembly | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2506.06221) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| CoRL 2025 | `O3Afford` | O3Afford: One-Shot 3D Object-to-Object Affordance Grounding for Generalizable Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2509.06233) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| IEEE/ASME Transactions on Mechatronics 2025 | `DART` | DART: A Novel Task-Driven Diffusion-Based Policy with Affordance Learning for Generalizable Manipulation of Articulated Objects | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2509.14939) | E2E | explicit | Integrated policy · Explicit input |
| ICCV 2025 | `CoA-VLA` | CoA-VLA: Improving Vision-Language-Action Models via Visual-Textual Chain-of-Affordance | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2412.20451) | E2E | explicit | Integrated policy · Explicit input |
| ICCV 2025 | `2HandedAfforder` | 2HandedAfforder: Learning Precise Actionable Bimanual Affordances from Human Videos | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/ICCV51701.2025.01368) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| arXiv 2025 | `OVAL-Grasp` | OVAL-Grasp: Open-Vocabulary Affordance Localization for Task Oriented Grasping | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2511.20841) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| RA-L 2025 | `ScaleADFG` | ScaleADFG: Affordance-based Dexterous Functional Grasping via Scalable Dataset | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2511.09602) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| AAAI 2026 | `AffordDex` | Towards Affordance-Aware Robotic Dexterous Grasping with Human-like Priors | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2508.08896) | E2E | reward | Integrated policy · Optimization signal |
| CVPR 2026 | `AFI` | Affordance Field Intervention: Enabling VLAs to Escape Memory Traps in Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2512.07472) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| AAAI 2026 | `A3D` | A3D: Adaptive Affordance Assembly with Dual-Arm Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2601.11076) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| IROS 2026 | `FSAG` | FSAG: Enhancing Human-to-Dexterous-Hand Finger-Specific Affordance Grounding via Diffusion Models | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2601.08246) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| arXiv 2026 | `CorDex` | Generate, Transfer, Adapt: Learning Functional Dexterous Grasping from a Single Human Demonstration | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2601.05243) | Hierarchical model | implicit | Hierarchical affordance-to-action · Retrieval-based |
| IEEE Access 2026 | `AffoRo-GS` | One-Shot 3-D Affordance Learning for Multi-Stage Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://ieeexplore.ieee.org/document/11475721) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| CVPR 2026 | `BiPreManip` | BiPreManip: Learning Affordance-Based Bimanual Preparatory Manipulation through Anticipatory Collaboration | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2603.21679) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| arXiv 2026 | `RAAP` | RAAP: Retrieval-Augmented Affordance Prediction with Cross-Image Action Alignment | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2603.29419) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| arXiv 2026 | `BridgeACT` | BridgeACT: Bridging Human Demonstrations to Robot Actions via Unified Tool-Target Affordances | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2604.23249) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| arXiv 2026 | `Afford-VLA` | Afford-VLA: Action-Aligned Visual Planning via Internalized Affordance | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2605.24203) | E2E | implicit | Integrated policy · Implicit representation |
| arXiv 2026 | `AffordVLA` | AffordVLA: Injecting Affordance Representations into Vision-Language-Action Models via Implicit Feature Alignment | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2605.17517) | E2E | implicit | Integrated policy · Implicit representation |
| CVPR 2026 | `PALM` | PALM: Progress-Aware Policy Learning via Affordance Reasoning for Long-Horizon Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2601.07060) | E2E | implicit | Integrated policy · Implicit representation |
| CVPR 2026 | `AffordGen` | AffordGen: Generating Diverse Demonstrations for Generalizable Object Manipulation with Affordance Correspondence | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2604.10579) | E2E | implicit | Integrated policy · Implicit representation |
| arXiv 2026 | `AffordanceVLA` | AffordanceVLA: A Vision-Language-Action Model Empowering Action Generation through Affordance-Aware Understanding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2606.06155) | E2E | implicit | Integrated policy · Implicit representation |
| arXiv 2026 | `Affordance2Action` | Affordance2Action: Task-Conditioned Scene-level Affordance Grounding for Real-Time Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2606.04172) | E2E | explicit/implicit | Integrated policy · Explicit/implicit representation |
| arXiv 2026 | `GROW2` | GROW2: Grounding Which and Where for Robot Tool Use | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2606.30632) | Hierarchical model | explicit | Hierarchical affordance-to-action |
| arXiv 2026 | `AffordSim` | AffordSim: A Scalable Data Generator and Benchmark for Affordance-Aware Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2604.11674) | Hierarchical model | explicit | Hierarchical affordance-to-action · Simulation benchmark |


<a id="affordance-datasets-benchmarks"></a>
### 📊 Affordance Datasets / Benchmarks

**Survey groups:** object-centric · scene-level · interaction-driven · language- and reasoning-oriented · action-oriented.

| Venue/Date | Name | Title | Paper | Data Modality |
| :-: | :-: | :- | :-: | :-: |
| ICRA 2015 | `UMD RGB-D Part Affordance Dataset` | Affordance Detection of Tool Parts from Geometric Features | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://www.umiacs.umd.edu/user.php?path=cteo%2Fpublic-shared%2FICRA15_affordance_parts_final.pdf) | image |
| ECCV 2016 | `NYUv2 affordance annotations` | A Multi-scale CNN for Affordance Segmentation in RGB Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://web.engr.oregonstate.edu/~sinisa/research/publications/eccv16_affordance.pdf) | image |
| IROS 2017 | `IIT-AFF` | Object-Based Affordances Detection with Convolutional Neural Networks and Dense Conditional Random Fields | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://sites.google.com/site/ocnncrf/) | image |
| CVPR 2018 | `ADE-Affordance` | Learning to Act Properly: Predicting and Explaining Affordances From Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content_cvpr_2018/html/Chuang_Learning_to_Act_CVPR_2018_paper.html) | image |
| CVPR 2018 | `OPRA` | Demo2Vec: Reasoning Object Affordances from Online Videos | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content_cvpr_2018/papers/Fang_Demo2Vec_Reasoning_Object_CVPR_2018_paper.pdf) | video-image |
| ECCV 2018 | `EPIC-KITCHENS` | Scaling egocentric vision: The epic-kitchens dataset | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/1804.02748) | video |
| CVPR 2020 | `GraspNet-1Billion` | Graspnet-1billion: A large-scale benchmark for general object grasping | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/1912.13470) | RGB-D/3D grasp |
| CVPR 2021 | `3D AffordanceNet` | 3D AffordanceNet: A Benchmark for Visual Object Affordance Understanding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2103.16397) | 3D |
| CVPR 2022 | `AGD20K` | Learning Affordance Grounding from Exocentric Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2203.09905) | image-image |
| CVPR 2022 | `Ego4D` | Ego4d: Around the world in 3,000 hours of egocentric video | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2110.07058) | video |
| ECCVW 2022 | `PartAfford` | PartAfford: Part-level Affordance Discovery from 3D Objects | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2202.13519) | 3D |
| ICCV 2023 | `3DOI` | Understanding 3D Object Interaction from a Single Image | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/ICCV51070.2023.01988) | image/3D interaction |
| ICCV 2023 | `AffordPose` | AffordPose: A Large-Scale Dataset of Hand-Object Interactions with Affordance-Driven Hand Pose | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/ICCV2023/html/Jian_AffordPose_A_Large-Scale_Dataset_of_Hand-Object_Interactions_with_Affordance-Driven_Hand_ICCV_2023_paper.html) | 3D |
| ICCV 2023 | `EPIC-Aff` | Multi-label Affordance Mapping from Egocentric Vision | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/ICCV2023/html/Mur-Labadia_Multi-label_Affordance_Mapping_from_Egocentric_Vision_ICCV_2023_paper.html) | video-3D |
| ICCV 2023 | `PIAD` | Grounding 3D Object Affordance from 2D Interactions in Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2303.10437) | image-3D |
| IROS 2023 | `HANDAL` | HANDAL: A Dataset of Real-World Manipulable Object Categories with Pose Annotations, Affordances, and Reconstructions | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2308.01477) | RGB-D/6-DoF pose/3D mesh |
| WACV 2023 | `EPIC-KITCHENS Affordance` | Fine-Grained Affordance Annotation for Egocentric Hand-Object Interaction Videos | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/WACV2023/html/Yu_Fine-Grained_Affordance_Annotation_for_Egocentric_Hand-Object_Interaction_Videos_WACV_2023_paper.html) | video/image |
| CVPR 2024 | `3DIR` | LEMON: Learning 3D Human-Object Interaction Relation from 2D Images | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2312.08963) | image-3D |
| CVPR 2024 | `AffordQ` | LASO: Language-guided Affordance Segmentation on 3D Object | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/CVPR2024/papers/Li_LASO_Language-guided_Affordance_Segmentation_on_3D_Object_CVPR_2024_paper.pdf) | 3D |
| CVPR 2024 | `SceneFun3D` | SceneFun3D: Fine-Grained Functionality and Affordance Understanding in 3D Scenes | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://openaccess.thecvf.com/content/CVPR2024/papers/Delitzas_SceneFun3D_Fine-Grained_Functionality_and_Affordance_Understanding_in_3D_Scenes_CVPR_2024_paper.pdf) | 3D |
| ACL 2025 | `InstructPart` | InstructPart: Task-Oriented Part Segmentation with Instruction Reasoning | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2505.18291) | image-language |
| ACM MM 2025 | `3DAffordSplat` | 3DAffordSplat: Efficient Affordance Reasoning with 3D Gaussians | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2504.11218) | 3D |
| ACM MM 2025 | `RoboAfford` | RoboAfford: A Dataset and Benchmark for Enhancing Object and Spatial Affordance Learning in Robot Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1145/3746027.3755653) | image/language |
| arXiv 2025 | `A4Bench` | Affordance Benchmark for MLLMs | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2506.00893) | image |
| arXiv 2025 | `Affogato-750K` | Affogato: Learning Open-Vocabulary Affordance Grounding with Automated Data Generation at Scale | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2506.12009) | language-3D |
| arXiv 2025 | `HOVA-500K` | GLOVER++: Unleashing the Potential of Affordance Learning from Human Behaviors for Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2505.11865) | image |
| arXiv 2025 | `SeqAffordSplat` | SeqAffordSplat: Scene-level Sequential Affordance Reasoning on 3D Gaussian Splatting | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2507.23772) | language/3D Gaussian |
| CVPR 2025 | `AGPIL` | Grounding 3D Object Affordance with Language Instructions, Visual Observations and Interactions | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2504.04744) | image-3D |
| CVPR 2025 | `FunGraph3D` | Open-Vocabulary Functional 3D Scene Graphs for Real-World Indoor Spaces | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2503.19199) | RGB-D/3D scene graph |
| CVPR 2025 | `PIADv2` | GREAT: Geometry-Intention Collaborative Inference for Open-Vocabulary 3D Object Affordance Grounding | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2411.19626) | image-language-3D |
| CVPR 2025 | `SeqAfford` | SeqAfford: Sequential 3D Affordance Reasoning via Multimodal Large Language Model | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2412.01550) | language-3D |
| ICCV 2025 | `2HandedAffordance` | 2HandedAfforder: Learning Precise Actionable Bimanual Affordances from Human Videos | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/ICCV51701.2025.01368) | video/text/3D |
| ICCV 2025 | `RAGNet` | RAGNet: Large-scale Reasoning-based Affordance Segmentation Benchmark towards General Grasping | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2507.23734) | image |
| IROS 2025 | `AGDDO15` | One-Shot Affordance Grounding of Deformable Objects in Egocentric Organizing Scenes | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2503.01092) | image |
| IROS Workshop 2025 | `RoboAfford++` | RoboAfford++: A Generative AI-Enhanced Dataset for Multimodal Affordance Learning in Robotic Manipulation and Navigation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2511.12436) | image/language |
| RA-L 2025 | `ScaleADFG` | ScaleADFG: Affordance-based Dexterous Functional Grasping via Scalable Dataset | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2511.09602) | 3D/grasp |
| AAAI 2026 | `ReasonAff` | Affordance-R1: Reinforcement Learning for Generalizable Affordance Reasoning in Multimodal Large Language Model | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2508.06206) | image/language |
| arXiv 2026 | `360-AGD` | PanoAffordanceNet: Towards Holistic Affordance Grounding in 360° Indoor Environments | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2603.09760) | panoramic image/text |
| arXiv 2026 | `A2A-Bench` | Affordance2Action: Task-Conditioned Scene-level Affordance Grounding for Real-Time Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2606.04172) | image |
| arXiv 2026 | `AffordSim` | AffordSim: A Scalable Data Generator and Benchmark for Affordance-Aware Robotic Manipulation | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2604.11674) | simulation/3D/robot action |
| arXiv 2026 | `CompassAD` | CompassAD: Intent-Driven 3D Affordance Grounding in Functionally Competing Objects | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2604.02060) | language-3D |
| arXiv 2026 | `VIDA` | VideoAfford: Grounding 3D Affordance from Human-Object-Interaction Videos via Multimodal Large Language Model | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2602.09638) | video-3D |
| CVPR 2026 | `AffordBridge` | AffordMatcher: Affordance Learning in 3D Scenes from Visual Signifiers | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2603.27970) | image-3D |
| ECCV 2026 | `PAP-12K` | Panoramic Affordance Prediction | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2603.15558) | panoramic image/text |

<a id="related-surveys"></a>
### 📚 Related Surveys

| Venue/Date | Name | Title | Paper | Focus |
| :-: | :-: | :- | :-: | :-: |
| IEEE TCDS 2016 | - | Affordance Research in Developmental Robotics: A Survey | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/TCDS.2016.2614992) | Developmental robotics and robot acquisition of affordance knowledge |
| IEEE TCDS 2018 | - | Affordances in Psychology, Neuroscience, and Robotics: A Survey | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/TCDS.2016.2594134) | Cross-disciplinary foundations spanning psychology, neuroscience, and robotics |
| IJCAI 2021 | - | Building Affordance Relations for Robotic Agents - A Review | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.24963/ijcai.2021/590) | Relational affordance representations for robotic agents |
| ACM Computing Surveys 2021 | - | Visual Affordance and Function Understanding: A Survey | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1145/3446370) | Visual affordance recognition, segmentation, and function understanding |
| IEEE TBD 2023 | - | A Survey of Visual Affordance Recognition Based on Deep Learning | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/TBDATA.2023.3291558) | Deep-learning methods for visual affordance recognition |
| IEEE TCDS 2023 | - | Recent Advances of Deep Robotic Affordance Learning: A Reinforcement Learning Perspective | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://doi.org/10.1109/TCDS.2023.3277288) | Robotic affordance learning from a reinforcement-learning perspective |
| arXiv 2025 | - | Visual Affordance Prediction: Survey and Reproducibility | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge)](https://arxiv.org/abs/2505.05074) | Visual affordance prediction with an emphasis on reproducibility |





## 🎉 Contributing

⭐ Help us grow this repository! If you know any valuable works we’ve missed, don’t hesitate to contribute — every suggestion makes a difference!

We welcome and appreciate all contributions! Here’s how you can help:

- 📄 **Add or Update a Paper**  
  Contribute by adding a new paper or improving details of an existing one. Please consider the most appropriate category for the work.

- ✍️ **Use Consistent Formatting**  
  Follow the format of the existing entries to maintain clarity and consistency across the list.

- 🔗 **Include Abstract Link**  
  If the paper is from arXiv, use the `/abs/` link format for the abstract (e.g., `https://arxiv.org/abs/xxxx.xxxxx`).

- 💡 **Explain Your Edit (Optional but Helpful)**  
  A short note on why you think the paper deserves to be added or updated is appreciated and helps maintainers process your PR faster.

> **✅ Don't worry about getting everything perfect!**  
> Minor mistakes are totally fine — we’ll help fix them. What matters most is your contribution. Let's highlight your awesome work together!


## 🌟 Acknowledgment

Thanks for the wonderful project: [Awesome-LLM-Empathy](https://github.com/JhCircle/Awesome-LLM-Empathy). This project is built upon it.

## 📄 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

<!-- ## 👥 Contributors -->

<!-- <a href="https://github.com/hq-King/Awesome-Affordance-Learning/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=hq-King/Awesome-Affordance-Learning" /> -->
</a>
