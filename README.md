# EEG Motor Imagery Classification – BCI Competition III, Dataset IVa

This project explores motor imagery classification using EEG data from the [BCI Competition III Dataset IVa](https://www.bbci.de/competition/iii/desc_IVa.html). The goal is to distinguish between imagined right hand and right foot movements using brainwave signals.

## 🧠 Overview

Using EEG signals recorded from five subjects, we:
- Visualized and explored data from motor cortex channels (C3 and Cz)
- Extracted alpha band power features
- Built a simple Random Forest classifier
- Achieved baseline accuracy and identified next steps for improving performance

## 📊 Key Findings

- **Accuracy**: 56% on test data using only C3 and Cz band power
- **Top Features**: Alpha band power from C3 and Cz channels
- **Insight**: Using only two channels is limited. Future work should explore more features and channels.

## 🗂️ Dataset

- Source: [BCI Competition III - Dataset IVa](https://www.bbci.de/competition/iii/)
- Subjects: 5
- Channels: 118 EEG channels (downsampled to 100Hz)
- Classes: 
  - 1 = Right Hand
  - 2 = Right Foot

## 🛠️ Dependencies

```txt
numpy
scipy
matplotlib
scikit-learn
mne
