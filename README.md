BCI Motor Imagery Classifier

This project explores Brain-Computer Interface (BCI) signal classification using real EEG data from the BCI Competition III, Dataset IVa. The goal is to distinguish between right-hand and right-foot motor imagery based on EEG band power features.

Dataset Overview
	•	Source: BCI Competition III, Dataset IVa
	•	Subjects: 5 healthy individuals
	•	Channels: 118 EEG channels
	•	Classes: Right hand (1), Right foot (2)
	•	Data Format: .mat (MATLAB), includes EEG signal (cnt) and event markers (mrk)

Methodology
	1.	Data Loading: MATLAB .mat files parsed using scipy.io.
	2.	Preprocessing: Extracted relevant channels (C3, Cz), scaled signals.
	3.	Feature Extraction: Computed band power (alpha, beta) for C3 and Cz.
	4.	Classification: Trained a Random Forest Classifier.
	5.	Evaluation: Accuracy, precision, recall, F1-score, and feature importance analyzed.

Key Findings
	•	Accuracy: ~56%
	•	Most Important Features: C3 Alpha and Cz Alpha band powers
	•	Insight: C3 and Cz are useful but not sufficient alone; further features or channels may improve performance.

Future Work
	•	Include additional motor-related channels (e.g., C1, C4, FCz)
	•	Apply spatial filtering (e.g., CSP)
	•	Explore deep learning models (e.g., CNN, LSTM)
	•	Evaluate across multiple subjects

Repository Structure
├── data/               # Contains downloaded .mat EEG datasets
├── BCI_EEG_Motor_Imagery_Classification.ipynb      # Full preprocessing, feature extraction, training pipeline
├── README.md           # Project documentation (this file)
└── requirements.txt    # Python dependencies

Credits
	•	Dataset: BCI Competition III IVa (TU Berlin, Fraunhofer FIRST)
	•	Author: Judy Hsu
	•	Tools: Python, Scikit-learn, MNE, SciPy, Matplotlib

Why This Matters

This project demonstrates the foundational steps in building a non-invasive BCI pipeline, paving the way toward brain-controlled interfaces, assistive technology, and future human-AI interaction.
