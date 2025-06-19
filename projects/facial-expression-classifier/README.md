# Facial Expression Classifier

This project classifies human facial expressions using the FER-2013 dataset. It compares two deep learning models: a custom CNN and a fine-tuned MobileNetV2.

## What It Does
- Loads and visualizes facial images from FER-2013 dataset
- Preprocesses grayscale images and augments training data
- Trains two models:
  - A custom Convolutional Neural Network (CNN)
  - A transfer learning model using MobileNetV2
- Evaluates both on test accuracy and class-wise performance

## Dataset
- **Source**: [FER-2013 (Kaggle)](https://www.kaggle.com/datasets/msambare/fer2013)
- Contains ~35,000 labeled grayscale images (48x48 pixels)
- Emotion labels: Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral

## Techniques Used
### CNN Model
- Multiple convolutional and pooling layers
- Dropout and L2 regularization
- Final dense layers for classification

### MobileNetV2 (Transfer Learning)
- Uses pretrained ImageNet weights
- Converts grayscale to RGB input
- Adds custom classification head

## Tech Stack
- Python, TensorFlow/Keras
- matplotlib, sklearn, kagglehub
- Jupyter Notebook

## Results
- **Custom CNN**: Trained for 60 epochs with regularization
- **MobileNetV2**: Fine-tuned for 50 epochs with frozen base
- Both models achieved strong performance on emotion recognition tasks
- Evaluation includes classification report and confusion matrix

| Model         | Train Accuracy | Test Accuracy |
|---------------|----------------|---------------|
| CNN           | ~TBD%           | ~TBD%          |
| MobileNetV2   | ~TBD%           | ~TBD%          |

*(Replace with actual accuracy values)*

## Future Improvements

- Fine-tune MobileNetV2 after unfreezing some layers
- Add emotion-aware data augmentation (e.g. brightness, tilt)
- Deploy as a live webcam emotion detector

Notebook includes training visualizations, evaluation reports, and confusion matrices for both models.
