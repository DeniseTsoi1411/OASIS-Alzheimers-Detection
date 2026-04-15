# OASIS-Alzheimers-Detection
Machine learning project modelling OASIS brain MRI images to train for dementia detection

## Project Overview
This project utilises deep learning to classify severity of Alzheimer's disease as seen in MRI brain scans. By analyzing structural changes in brain tissue, the model aims to assist in the early identification of dementia severity. This model can successfuly predict dementia severity with over 80% accuracy. 

## Dataset
The model uses the OASIS Alzheimer's Dataset (extracted from Kaggle), containing MRI images categorized into:
- Non Demented
- Very Mild Dementia
- Mild Dementia
- Moderate Dementia

## Model Architecture
The primary model is a Sequential CNN built with TensorFlow:
1. Normalisation Layer = Pixels of value 0 to 255 scaled to range 0 to 1
2. Convolutional Layers = Feature extraction done in 3 stages using 16, 32, and 64 filters
3. Pooling Layers = Max pooling to focus only on strong pathological markers
4. Classification Head: A dense network with a softmax output for 4-class probability

## Model explanation
This project requires analysis of images to predict dementia severity. Thus, a Convolution Neural Network (CNN) was chosen based on its specific design to scan images in small, moving windows. It is capable of handling slight positional differences to account for changes in brain structure from one person to the next. 

After the normalisation of the layers, each layer undergoes analysis through filters of increasing size. This is the Pyramid strategy, where the low level filter (16) emphasises on simple edges and the contrast between the brain and the skull. Incrementally increasing the filter size allows for analysis of brain structure with increasing judgement and sensitivity. This reduces data loss that may arise from using just the highest filter straight away. 

As every brain and scan looks different, Max Pooling was used to filter out small variations and noise that would otherwise be too complex for the computer to handle. Focusing only on the most significant pattern provides a more definitive analysis. 

## Bio-Technical Interpretation
The CNN layers strived to identify brain atrophy and ventricular expansion which corresponds with the shrinkage of the hippocampus and the cortex, all of which are primary neurodegenerative symptoms of Alzheimer's. 

## Requirements
- Python 3.11+
- TensorFlow
- NumPy
- Matplotlib
- Seaborn
## Relevance

This project demonstrates core machine learning skills applicable to healthcare AI and aligns with research in neurodegenerative disease prediction.
