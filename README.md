# Equitable AI for Dermatology - Spring 2025

## Overview
This repository contains our team's submission to the Break Through Tech and Algorithmic Justice League (AJL) Kaggle competition. The goal was to develop a dermatology-focused AI model capable of accurately classifying 21 skin conditions across diverse skin tones, addressing existing biases and ensuring equitable healthcare outcomes.

## Challenge Background
AI tools in dermatology frequently demonstrate biases against darker skin tones due to limited diversity in training datasets. This project aims to counteract these disparities by incorporating fairness and explainability into our model development process.

## Our Approach

### Model Architecture
We utilized a **Vision Transformer (ViT)** architecture (*ViT Base Patch 16*), leveraging transfer learning for enhanced performance and reduced computational costs.

### Data Preparation
- **Data Augmentation**: IWe enriched our dataset through random rotation, flips, shifts, color jitter, CLAHE, and noise addition to diversify our dataset.
- **Label Encoding**: Encoded skin condition labels for efficient model processing.
- **Data Splitting**: Stratified splitting ensured representative validation sets.

### Fairness and Explainability
- We utilized the **Focal Loss** function to handle class imbalance.
- **Mixup Augmentation** was applied during training to promote robust generalization.
- Model decision-making processes were visualized through explainability techniques (e.g Confusion Matrix), highlighting the regions and patterns influencing predictions.

## Training Details
- **Optimizer**: AdamW optimizer with cosine scheduler and warm-up for stable convergence.
- **Training Strategy**: Early stopping based on validation accuracy to prevent overfitting.
- **Best Model**: Saved and reloaded the best-performing model based on validation accuracy.

## Performance Evaluation
Our model achieved competitive results measured by the weighted average F1-score on the Kaggle leaderboard.

## Files Included
- `vit_predictions.csv`: Final predictions submitted to Kaggle.
- `ViT - skin condition classification.ipynb`: Notebook detailing the full pipeline.

## Future Work
We aim to further refine our model by incorporating additional diverse datasets and leveraging advanced fairness algorithms.

---

**Team Members:**
- Hanh Minh Pham (hanhminhpham01@gmail.com)
- Malik Salim (maliksalim@bennington.edu)
- Krishna Kanodia (krishna.kanodia77@gmail.com)
- Chioma Opara (copara@smith.edu)
- Keta Patel (k.patel010@umb.edu)

**Acknowledgments:**
Special thanks to Break Through Tech and our mentors for guidance and support throughout this impactful project.
