# Personality Behavior Classifier: Introvert vs Extrovert

This project classifies personality types (Introvert vs Extrovert) based on behavioral and survey data. It applies multiple ML models and visualizations to explore what traits contribute most to personality prediction.

## What It Does
- Loads a labeled dataset of personality traits and behaviors
- Cleans and scales numerical features
- Trains and compares classifiers: `Random Forest` and `Logistic Regression`
- Visualizes feature importance and dimensionality with `t-SNE`
- Performs error analysis using a confusion matrix

## Dataset
- **Source**: [Extrovert vs Introvert Behavior Data](https://www.kaggle.com/datasets/rakeshkapilavai/extrovert-vs-introvert-behavior-data)
- Attributes include behavioral metrics and responses to personality-related questions
- Target: `Personality` (Introvert or Extrovert)

## Techniques Used
- `LabelEncoder` for class labels
- `StandardScaler` for normalization
- `RandomForestClassifier` for feature importance & prediction
- `LogisticRegression` for comparison
- `t-SNE` for 2D visualization of clusters

## Tech Stack
- Python, pandas, scikit-learn, seaborn, matplotlib
- Notebook-compatible (Jupyter or Colab)

## Results
| Model              | Accuracy | F1 Score |
|--------------------|----------|----------|
| Random Forest       | ~92.24%      | ~91.98%      |
| Logistic Regression | ~92.93%      | ~92.72%      |

## Key Features
- **Feature Importance Plot**: Highlights which traits matter most for classification
- **t-SNE Projection**: 2D visualization of introverts vs extroverts
- **Error Analysis**: Counts false positives/negatives for misclassifications

## Insights
- Which behaviors separate introverts from extroverts?
- Which model performs best, and why?
- What patterns does t-SNE reveal?

## Future Improvements
- Try more advanced models (e.g., Gradient Boosting, XGBoost)
- Tune hyperparameters for better F1 score
- Add non-numeric feature handling via encoding
- Create a live survey input → personality predictor app

Includes notebook with full ML workflow, feature analysis, and model comparison.
