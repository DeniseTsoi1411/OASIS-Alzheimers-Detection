# OASIS-Alzheimers-Detection
Machine learning project modelling OASIS brain MRI images to train for dementia detection

## Project Overview
This project applies Deep Learning (Convolutional Neural Networks) to classify MRI scans into four stages of Alzheimer's Disease. By analyzing structural changes in brain tissue, the model aims to assist in the early identification of dementia severity.

## Dataset
The model uses the OASIS Alzheimer's Dataset (extracted from Kaggle), containing MRI images categorized into:
- Non Demented
- Very Mild Dementia
- Mild Dementia
- Moderate Dementia

## Model Architecture
The primary model is a **Sequential CNN** built with TensorFlow:
1. **Normalization Layer:** Scales pixel values (0-255) to a range of (0-1).
2. **Convolutional Layers:** Three stages of feature extraction using 16, 32, and 64 filters.
3. **Pooling Layers:** Dimensionality reduction to focus on key pathological markers.
4. **Classification Head:** A dense network with a Softmax output for 4-class probability.

## Bio-Technical Interpretation
In clinical terms, the CNN layers learn to identify **brain atrophy** and **ventricular expansion**. The model's "Feature Maps" correspond to the biological shrinkage of the hippocampus and cortex, which are primary indicators of neurodegeneration in Alzheimer's patients.

## Requirements
- Python 3.11+
- TensorFlow
- NumPy
- Matplotlib
- Seaborn
## Relevance

This project demonstrates core machine learning skills applicable to healthcare AI and aligns with research in neurodegenerative disease prediction.
