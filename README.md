# Movie Review Sentiment Analysis
A lightweight NLP system for sentiment classification of movie reviews, trained on IMDb data.

# Project Goal
Build a resource-efficient transformer-based model to classify movie reviews as positive/negative, optimized for limited compute.

# Key Features
✅ Custom-trained on IMDb dataset tokenizer

✅ Small MLM (Masked Language Model) pretrained on IMDb dataset

✅ Hybrid classification head for fine-tuning

✅ Evaluated on 4 datasets (IMDb, SST-2, Amazon, MB)

# Performance

Matches traditional ML models

Accuracy: 86% on test IMDb (vs. 90%+ for SOTA)

Domain Shift Challenge: Performance drops on older data (see Report)

# Repository Structure

movie-reviews/
│

├── data/               # Datasets (raw/processed)

│   ├── IMDb/           # Training and IMDb test data

│   ├── MB/             # MB test data

│   ├── SST-2/          # SST-2 test data

│   └── Amazon/         # Amazon test data

│

├── notebooks/          # Jupyter notebooks

│   ├── 01_data_preprocessing.ipynb    # Cleaning & tokenization

│   ├── 02_MLM_training.ipynb          # Pretraining MLM

│   ├── 03_classifier_training.ipynb   # Fine-tuning classifier

│   └── 04_evaluation.ipynb            # Cross-dataset tests

│

├── models/             # Models weights

├── README.md           

├── requirements.txt    # Python dependencies

└── report.pdf          # Detailed methodology/results

