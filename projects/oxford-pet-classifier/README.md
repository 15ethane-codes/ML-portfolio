# Oxford Pet Classification

# Oxford-IIIT Pet Classification

This project uses a transfer learning approach to classify cat and dog breeds from the Oxford-IIIT Pet Dataset. It applies MobileNetV2 as a feature extractor and achieves high performance using TensorFlow and `tf.data`.

## What It Does
- Loads and processes the Oxford-IIIT Pet Dataset from `tensorflow_datasets`
- Applies image normalization and augmentation
- Builds a classifier on top of a frozen MobileNetV2 model
- Trains and evaluates model performance over multiple epochs

## Dataset

- **Source**: [Oxford-IIIT Pet Dataset](https://www.robots.ox.ac.uk/~vgg/data/pets/)
- Downloaded via: `tensorflow_datasets`
- Includes 37 different pet breeds (cats and dogs)
- ~7,300 images, labeled by breed and segmentation mask (only breed used here)

## Techniques Used
- `tf.data` pipeline for efficient batching, shuffling, caching, and prefetching
- Pretrained MobileNetV2 base (frozen)
- Global average pooling and dropout for generalization
- Final softmax dense layer for multi-class classification

## Tech Stack
- Python, TensorFlow, TensorFlow Datasets
- Jupyter Notebook or Colab for experimentation
- GPU acceleration if available

## Results
- Trained for 10 epochs
- Reached a validation accuracy of approximately **XX%** *(replace with your result)*
- Accuracy and loss visualized over training time

| Metric              | Value    |
|---------------------|----------|
| Validation Accuracy | 0.8886%      |
| Validation Loss     | 0.3384   |

## 📈 Training Curve

Includes plotted graphs for both:
- Accuracy (train vs validation)
- Loss (train vs validation)

## Future Improvements
- Fine-tune the MobileNetV2 layers after initial training
- Add data augmentation (flip, rotate, crop) for improved robustness
- Implement real-time classification from webcam input
- Compare with other architectures (e.g., EfficientNet, ResNet)

Notebook contains full code with GPU support, preprocessing, model building, and training.
