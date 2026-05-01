EEG-Based Automated Depression Detection
An end-to-end machine learning pipeline for automated depression detection using EEG signals — combining non-linear feature extraction, class balancing, and deep learning classification.

📌 Overview
Depression is one of the most underdiagnosed neurological conditions worldwide. This project builds an automated detection system by extracting meaningful features from raw EEG signals and classifying them using a Multi-Level Perceptron (MLP) deep learning model.
The pipeline covers everything from raw signal processing to final classification — including non-linear feature extraction, epoch-level analysis, SMOTE-based data balancing, and MLP training.

🏗️ Pipeline Architecture
Raw EEG Signal
      │
      ▼
┌──────────────────────────────────┐
│  Epoch Level Extractor           │  ← Segment EEG into 15 epochs
└──────────────┬───────────────────┘
               │
               ▼
┌──────────────────────────────────┐
│  Non-linear Feature Extraction   │  ← M-DFA & Entropy metrics
│  Feature Extractor (40 features) │  ← Full feature vector per epoch
└──────────────┬───────────────────┘
               │
               ▼
┌──────────────────────────────────┐
│  SMOTE Analysis                  │  ← Handle class imbalance
└──────────────┬───────────────────┘
               │
               ▼
┌──────────────────────────────────┐
│  MLP Deep Learning Model         │  ← Multi-level perceptron classifier
└──────────────────────────────────┘

📁 File Descriptions
FileDescriptionEpoch Level Extractor (with 15 Epochs)Segments raw EEG signals into 15 time epochs for time-windowed analysisNon-linear feature extraction (M-DFA & Entropy)Extracts Multiscale DFA and entropy-based features to capture signal complexityFeature Extractor (40 features)Builds a complete 40-dimensional feature vector per epoch combining all extracted metricsSMOTE AnalysisApplies Synthetic Minority Over-sampling Technique to handle class imbalanceDeep learning Model - MLP (Multi-level perceptron)Trains and evaluates the MLP classifier on extracted feature vectors

🔬 Key Techniques
Multiscale DFA (M-DFA):
Analyzes long-range temporal correlations in EEG signals
Computes scaling exponent across multiple time scales
Captures subtle signal patterns linked to depression

Entropy Metrics:
Measures complexity and irregularity of EEG signals
Differentiates between normal and depressed brain activity patterns

SMOTE (Synthetic Minority Oversampling):
Generates synthetic samples for the minority class
Prevents model bias toward the majority class
Improves classification performance on imbalanced EEG datasets

MLP Classifier:
Multi-layer perceptron trained on 40 extracted features
Deep learning approach for robust binary classification
Trained over 15 epochs with epoch-level feature inputs


🛠️ Tools & Technologies
CategoryToolLanguagePython 3Signal ProcessingNumPy, SciPyMachine LearningScikit-learn, imbalanced-learn (SMOTE)Deep LearningTensorFlow / KerasVisualizationMatplotlib

📊 Results
Extracted 40 non-linear features per EEG epoch using M-DFA and entropy analysis
Applied SMOTE to balance the dataset for unbiased training
Trained MLP model over 15 epochs for automated depression classification


🎓 Academic Context
Developed as part of B.E. Electronics & Communication Engineering at BV Raju Institute of Technology (BVRIT), Narsapur.
Author: Vemula Shashank
LinkedIn: vemula-shashank
Email: vemulashashank361@gmail.com
