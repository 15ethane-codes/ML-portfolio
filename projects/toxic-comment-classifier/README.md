# Toxic Comment Classifier

This project detects toxic comments using both classical machine learning and deep learning approaches. It performs **multi-label classification** across six types of online toxicity.

## What It Does

Given a comment, the models identify whether it is:
- toxic
- severe_toxic
- obscene
- threat
- insult
- identity_hate

The project implements three approaches:
1. **Binary Classification** (Logistic Regression for `toxic` only)
2. **Multi-Label Classification** (One-vs-Rest Logistic Regression across all 6 labels)
3. **Deep Learning Model** (Bidirectional LSTM for multi-label prediction)

## Dataset
- **Source**: [Jigsaw Toxic Comment Classification Challenge](https://www.kaggle.com/competitions/jigsaw-toxic-comment-classification-challenge)
- **Size**: 150,000+ comments
- Each comment is annotated with six binary labels (can have multiple per comment)

## Techniques Used
### Classical ML
- **Vectorizer**: TF-IDF (top 10,000 features)
- **Model**: 
  - Logistic Regression (binary)
  - OneVsRestClassifier for multi-label
- **Evaluation**: Accuracy, classification report (per label)

### Deep Learning
- **Architecture**:
  - Embedding layer
  - Bidirectional LSTM → Dropout
  - Dense + Sigmoid output (for 6 classes)
- **Loss**: Binary cross-entropy
- **Metrics**:
  - Per-label accuracy
  - Subset accuracy (exact match across all labels)
- **Tokenizer**: Keras Tokenizer, padded to 150 tokens
- **Training**: 5 epochs with 128 batch size

## Results
- **Binary Logistic Regression Accuracy**: ~90%-Good baseline for detecting general toxicity
- **Multi-label (LogReg)**: ~90%-Solid per-label performance across all 6 categories
- **Deep Learning**:
  - **Subset Accuracy**: ~91%
  - **Mean Per-label Accuracy**: ~98%
  - Captured more nuanced toxicity patterns

## Libraries Used
- `pandas`, `numpy`
- `sklearn` (TF-IDF, Logistic Regression, metrics)
- `tensorflow.keras` (Embedding, BiLSTM, Dropout, Dense)
- No visualization libraries (e.g., matplotlib or seaborn) were used in this project

## Future Work
- Add BERT-based transformer models (e.g., DistilBERT)
- Experiment with attention layers
- Create real-time toxicity filtering app
- Add visualizations and live examples via Gradio or Streamlit

Notebook includes preprocessing steps, model architecture, and evaluation metrics.
