# Movie Review Sentiment Analysis
A lightweight NLP system for sentiment classification of movie reviews, trained on IMDb data.

Project Goal: build a resource-efficient transformer-based model to classify movie reviews as positive/negative.

# Key Features
✅ Custom-trained on IMDb dataset tokenizer

✅ Small MLM (Masked Language Model) pretrained on IMDb dataset

✅ Hybrid classification head for fine-tuning

✅ Evaluated on 4 datasets (IMDb, SST-2, Amazon, MB)

# Performance

Matches traditional ML models

Accuracy: 86% on test IMDb (vs. 90%+ for SOTA)

Lowered performance on other datasets (see Report)

# Repository Structure

movie-reviews/
│

├── data/              [Google Drive](https://drive.google.com/drive/folders/1btauwCy79V9HXDOJIXMhpNxeUAUOLWyQ?usp=sharing)

│   ├── IMDb/           # Training and IMDb test data

│   ├── MB/             # MB test data

│   ├── SST-2/          # SST-2 test data

│   └── Amazon/         # Amazon test data

│

├── notebooks/          # Jupyter notebooks

│   ├── 01_tokenizer.ipynb             # Training tokenizer

│   ├── 02_data_preprocessing.ipynb    # Cleaning & tokenization

│   ├── 03_MLM_training.ipynb          # Pretraining MLM

│   ├── 04_classifier_training.ipynb   # Fine-tuning classifier

│   └── 05_evaluation.ipynb            # Cross-dataset tests

│

├── models/             # Models weights and tokenizer [Google Drive](https://drive.google.com/drive/folders/1-oC42w-uOL5_a9d-mrrXHHJ1Pr8fka8j?usp=sharing)

|

├── README.md           

├── requirements.txt    # Python dependencies

└── report.pdf          # Detailed methodology/results

# Pipeline

01_tokenizer.ipynb -> Train tokenizer  -> CPU

02_data_preprocessing.ipynb -> Clean data and prepare for training / testing -> CPU

03_MLM_training.ipynb -> Train MLM	-> GPU

04_classifier_training.ipynb	-> Fine-tune classifier	-> GPU

05_evaluation.ipynb	-> Evaluate on all test datasets	-> CPU/GPU

# Accuracy Table:

IMDb (Test)	-> 86.1%

SST-2	      -> 44.5%

Amazon	    -> 50.8%

MB          -> 77.2%
