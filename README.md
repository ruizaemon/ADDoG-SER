# Adversarial Discriminative Domain Generalization for Speech Emotion Recognition

## Introduction

- Emotion recognition models built on one domain degrades significantly when tested against another with a different domain
- In the study of speech emotion recognition (SER), obtaining labelled speech data across various domains is very costly
- Machine learning techniques such as domain generalisation and domain adaptation is employed to bridge this gap between different domains

- This repository builds a cross-domain SER model using adversarial discriminative domain generalization (ADDoG), obtaining a ~10% increase in test accuracy

## Requirements

- **Python**

### Python packages

- 

### Dataset

This repository uses 2 datasets:

- [RAVDESS](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio)
- [TESS](https://tspace.library.utoronto.ca/handle/1807/24487)

## Preprocessing

[Preprocessing](Processing_TESS%2BRAVDESS(30%25)_TVT_5features.ipynb) the raw data comprises several steps:

- Extracting emotion label corresponding to each audio file and storing the data into comprehensible dataframes
- Loading the audio signals into NumPy arrays and trimming noise
- Splitting the signals into training, validation, and test sets
  - **In this repository, the training and validation sets consists of TESS combined with 30% of RAVDESS, while the test set comprises the remaining 70% of the RAVDESS dataset**
- Augmenting the training set with Gaussian noise
- **Feature extraction**

### Feature extraction

In this repository, a combination of five feature types of sound are used:

- Mel-frequency cepstral coefficients (MFCCs)
- Mel-spectrogram
- Chromagram
- Spectral contrast feature
- Tonnetz feature

## Model architecture

In this repository, a comparison of test accuracy is made between two models:

- [CNN](https://en.wikipedia.org/wiki/Convolutional_neural_network)
- [ADDoG](https://doi.org/10.48550/arXiv.1903.12094)

### CNN


