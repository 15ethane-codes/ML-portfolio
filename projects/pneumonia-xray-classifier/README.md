# Pneumonia X-ray Classifier

A transfer learning-based image classifier for detecting pneumonia from chest X-ray scans. Built using PyTorch and ResNet18, this project demonstrates how medical imaging and AI can intersect to support diagnosis.

## Dataset
- **Source**: [`paultimothymooney/chest-xray-pneumonia`](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)
- **Structure**: 
  ```
  chest_xray/
  ├── train/
  ├── val/
  └── test/
  ```
- **Classes**:
  - `NORMAL`
  - `PNEUMONIA`

## Model Architecture
- **Backbone**: `ResNet18` pretrained on ImageNet
- **Modifications**: Final `fc` layer adjusted to output 2 classes
- **Loss**: `CrossEntropyLoss`
- **Optimizer**: `Adam (lr=1e-4)`

## Training
- Resizes all X-ray images to `224x224`
- Applies normalization: `mean=0.5`, `std=0.5`
- Batch size: `8`
- Trained for `5 epochs`
- Tracks accuracy per epoch
- Trains on GPU if available

## Evaluation
Evaluates performance on test images:
- Uses `torch.max()` for class prediction
- Final accuracy printed
- Overall precision/recall not shown but can be added with `classification_report`

## Upload & Predict (Prediction in colab file is a different test)



## Visualization
- Uses `matplotlib` to render the uploaded X-ray image.
- Displays prediction results directly below the image.

## Notes
- Classifier sometimes mispredicts real-world X-rays due to:
  - Lighting/contrast differences
  - Different X-ray angles
  - Dataset limitations (overfitting to training distribution)
- Try Grad-CAM or attention overlays for interpretability.

## Future Ideas
- Swap ResNet18 with DenseNet or EfficientNet
- Add Grad-CAM heatmaps
- Convert to Streamlit or Gradio demo
- Incorporate binary classification with confidence thresholding

## Summary
| Component       | Details                    |
|----------------|----------------------------|
| Model          | ResNet18 (pretrained)      |
| Classes        | NORMAL, PNEUMONIA          |
| Input Size     | 224x224                    |
| Accuracy       | ~XX% (depends on run)   |
| Dataset Size   | ~5k+ X-ray images          |

...In progress
