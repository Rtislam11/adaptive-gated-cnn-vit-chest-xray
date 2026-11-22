# Adaptive Gated Bidirectional Cross-Attention Fusion of CNN and Vision Transformer Features for Multi-Setting Chest X-Ray Classification

## Overview

This repository contains the experimental implementations and resources for the research paper:

**Adaptive Gated Bidirectional Cross-Attention Fusion of CNN and Vision Transformer Features for Multi-Setting Chest X-Ray Classification**

The proposed framework combines Convolutional Neural Networks (CNNs) and Vision Transformers (ViTs) for four-class chest X-ray (CXR) classification.

The architecture integrates local and global image representations through bidirectional cross-attention and adaptive gated feature fusion.

## Repository Contents

This repository contains three Jupyter notebooks:

| Notebook | Description |
|---|---|
| `baseline-1-model-resnet50.ipynb` | ResNet50 baseline implementation |
| `baseline-2-model-vit-16 (3).ipynb` | ViT-Small/16 baseline implementation |
| `proposed-model-cnn-vit (2).ipynb` | Proposed hybrid CNN–ViT model |

## Proposed Architecture

The proposed model consists of the following components:

- **EfficientNet-B2:** Extracts local and fine-grained radiographic features.
- **ViT-Small/16:** Captures global contextual information.
- **Bidirectional Cross-Attention:** Enables interaction between CNN and Transformer feature representations.
- **Adaptive Gated Fusion:** Learns the relative contribution of the two feature branches.
- **Grad-CAM:** Provides visual explanations of model predictions.

## Dataset

The experiments use the Curated COVID-19 Posterior-Anterior Chest Radiography Images dataset.

- **Total images:** 9,208
- **Classification classes:**
  1. COVID-19
  2. Bacterial Pneumonia
  3. Viral Pneumonia
  4. Normal

**Dataset source:**

https://data.mendeley.com/datasets/9xkhgts2s6/4

The dataset is divided into the following subsets:

| Dataset | Percentage |
|---|---:|
| Training | 70% |
| Validation | 15% |
| Testing | 15% |

Please download the dataset from its original source and follow its applicable terms of use.

## Baseline Models

The proposed architecture is evaluated against two pretrained baseline models:

1. ResNet50
2. ViT-Small/16

The same dataset partitions and training procedures are used to support a controlled architectural comparison.

## Experimental Results

The proposed model achieved the following results in the four-class classification experiment:

| Evaluation Metric | Result |
|---|---:|
| Accuracy | 90.8% |
| Macro-F1 Score | 90.1% |
| Macro-AUROC | 97.8% |

These results are reported from the research experiments.

## Experimental Environment

The experiments were conducted using the following environment:

- **Platform:** Kaggle Notebooks
- **Programming Language:** Python
- **Deep Learning Framework:** PyTorch
- **Hardware Accelerator:** NVIDIA Tesla T4 GPU

## Requirements

The notebooks use Python and deep learning libraries, including PyTorch and the other dependencies imported in the respective notebooks.

Install any required packages that are not already available in the Kaggle environment before running the experiments.

## How to Run Using Kaggle

1. Clone or download this GitHub repository.
2. Open [Kaggle Notebooks](https://www.kaggle.com/code).
3. Create a new Kaggle Notebook.
4. Upload the required `.ipynb` notebook.
5. Add the chest X-ray dataset using Kaggle's **Add Input** option, or obtain it from the original Mendeley Data source.
6. Update the dataset directory paths if necessary.
7. Select an NVIDIA T4 GPU accelerator.
8. Execute the notebook cells sequentially.

### Running the Proposed Model

Open:

`proposed-model-cnn-vit (2).ipynb`

Execute the notebook cells sequentially to run the proposed hybrid CNN–ViT experiment.

### Running the Baseline Models

**ResNet50 baseline:**

`baseline-1-model-resnet50.ipynb`

**ViT-Small/16 baseline:**

`baseline-2-model-vit-16 (3).ipynb`

Execute the corresponding notebook cells to run each baseline experiment.

## Evaluation Metrics

The experiments use the following evaluation metrics:

- Accuracy
- Macro-Precision
- Macro-Recall
- Macro-F1 Score
- Macro-AUROC
- Confusion Matrix

## Model Interpretability

Grad-CAM visualizations and adaptive gate values are used to examine model predictions, spatial evidence, and the contribution of different feature branches.

## Reproducibility

The repository provides the Jupyter notebook implementations of the proposed hybrid CNN–ViT model and the two baseline models.

For reproducing the reported results, use the same dataset, data partitions, preprocessing procedures, and experimental settings described in the research paper.

## Citation

If you use this work in your research, please cite the corresponding paper:

**Adaptive Gated Bidirectional Cross-Attention Fusion of CNN and Vision Transformer Features for Multi-Setting Chest X-Ray Classification.**

## Repository Link

https://github.com/RtIslam11/adaptive-gated-cnn-vit-chest-xray

## Contact

For questions or further information, please contact the corresponding author.

**GitHub:** https://github.com/RtIslam11/adaptive-gated-cnn-vit-chest-xray
