# 📰 Fake News Classification with the LIAR Dataset

## Project Summary

This project tackles the task of political fact classification using the LIAR dataset, which consists of short statements labeled by their truthfulness. Using both traditional machine learning (Random Forest) and a fine-tuned BERT model, the goal is to classify statements into categories such as *true*, *false*, *mostly-true*, etc.

## Dataset Overview
- **Source**: LIAR dataset (`liar_dataset.zip`)
- **Files**: `train.tsv`, `test.tsv`, `valid.tsv`
- **Total Samples**: ~12,800
- **Features Used**:
  - `statement`: the actual political claim
  - `label`: one of 6 truth labels: `true`, `mostly-true`, `half-true`, `barely-true`, `false`, `pants-fire`
- **Other Features (available but not used in modeling)**:
  - Subject, speaker, state, speaker job, party affiliation
  - Truth counts from previous statements

## Models
### 1. Random Forest (TF-IDF Based)
- **Preprocessing**: TF-IDF vectorization on `statement` column
- **Classifier**: `RandomForestClassifier` with hyperparameter tuning via `GridSearchCV`
- **Evaluation**:
  - Accuracy score
  - F1 score
  - Classification report (per label)

### 2. BERT Fine-Tuned Model
- **Tokenizer**: `bert-base-uncased` from HuggingFace Transformers
- **Architecture**:
  - Pretrained BERT with classification head
  - Max length: 128 tokens
  - Batch size: 16
- **Training**:
  - Optimizer: `AdamW`
  - Scheduler: Linear warm-up
  - Epochs: 4
- **Evaluation**:
  - Accuracy on training, validation, and test sets
  - Loss tracking per epoch

## Sample Results
| Model             | Accuracy (Val) | Accuracy (Test) |
|------------------|----------------|-----------------|
| Random Forest     | ~0.XX          | ~0.XX           |
| BERT (4 epochs)   | ~0.XX     | 0.XX|

## Next Steps
- Improve class balance via weighted loss or oversampling
- Incorporate metadata (e.g., party, speaker) as additional features
- Try deeper models (RoBERTa, DeBERTa)
- Add visualization: confusion matrix, attention heatmaps
- Implement per-class F1 optimization

## Files
- `liar_dataset.zip`: Dataset source (University made by William)
- `train.tsv`, `test.tsv`, `valid.tsv`: Raw data files
- `bert_classifier.py`: Code for model definition + training
- `random_forest_baseline.py`: Classic ML baseline

## My Notes
This project helped explore the differences between traditional ML and modern NLP with transformers. Although performance can be improved, it’s a solid baseline showing how deep learning models handle nuanced text classification tasks.
