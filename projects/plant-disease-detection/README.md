# 🌿 Plant Disease Classification (CNN + Augmentation)

This project uses a Convolutional Neural Network (CNN) to classify plant leaf images into 38 different disease categories. The dataset includes thousands of augmented images to boost performance, and the model is trained with strong regularization and visualized with accuracy/loss curves and a confusion matrix.

## 📦 Dataset

- **Source:** [Kaggle - New Plant Diseases Dataset (Augmented)](https://www.kaggle.com/datasets/vipoooool/new-plant-diseases-dataset)
- **Structure:**
  ```
  /train/
  /valid/
  /test/
  ```
- **Classes:** 38 disease labels  
- **Image Size:** 128x128 (resized)  
- **Augmentation:** Includes artificially rotated, zoomed, and flipped leaf images.

## Model
A custom CNN architecture built with TensorFlow/Keras.
```python
for filters in [32, 64, 128]:
    Conv2D -> BatchNorm -> MaxPool -> Dropout
```

- Final layers:
  - `Flatten → Dense(512, relu) → Dropout → Dense(38, softmax)`
- **Activation:** ReLU (hidden), Softmax (output)
- **Loss:** Categorical Crossentropy  
- **Optimizer:** Adam (lr = 1e-4)  
- **Callbacks:** ReduceLROnPlateau, EarlyStopping

## Training
- **Epochs:** 15  
- **Batch size:** 64  
- **Input Shape:** (128, 128, 3)  
- **Augmentation:**
  - Rotation: ±20°
  - Shifts: ±10%
  - Zoom: ±20%
  - Horizontal flip

## Results
> Final validation accuracy: **XX.XX%** (fill in your actual result)  
> Includes visual performance breakdown with confusion matrix + metrics.

### Accuracy / Loss Curves
- Visualized using `matplotlib`
- Side-by-side plots for training vs validation accuracy and loss

### Confusion Matrix
- Confirms performance across all 38 classes
- Rendered using `seaborn` and `sklearn`

## Evaluation
- Classification Report: Precision, Recall, F1 for each label
- Example Output:
  ```
  Class: Apple___Black_rot
  Precision: 0.96
  Recall:    0.98
  F1-score:  0.97
  ```

## Future Improvements
- Add real-time prediction on custom leaf images  
- Add EfficientNet or MobileNet-based transfer learning baseline  
- Deploy to web using Flask or Streamlit  
- Reduce GPU memory usage for inference

Notebook includes preprocessing steps and evaluation metrics.
