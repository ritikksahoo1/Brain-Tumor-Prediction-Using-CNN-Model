# Brain Tumor Detection Using Deep Learning and VGG-16 Model

This project demonstrates the use of deep learning for brain tumor detection using MRI images. We employed the VGG-16 architecture for feature extraction and fine-tuning to achieve high accuracy in classifying brain tumor images.

## Dataset

The dataset used in this project consists of MRI images of both healthy and tumor-affected brains. The dataset includes images from multiple sources, including:
- Brain Tumor Data Set
- Brain Tumor Classification MRI
- Brain Tumor MRI Dataset

## Data Summary

- Classes:
  - Brain Tumor
  - Healthy (No Tumor)
- Image Dimensions: 224x224 pixels

## Model Architecture

We used the pre-trained VGG-16 model for feature extraction. The model architecture includes the following layers:
- Convolutional Layers: Pre-trained VGG-16 layers (frozen)
- Global Average Pooling
- Dense layers (1024, 1024, 512, 256 units)
- Dropout layers
- Final Dense layer with softmax activation

## Model Summary

- Total parameters: 16,946,242
- Trainable parameters: 2,231,554
- Non-trainable parameters: 14,714,688

## Training

The model was trained on the following data split:
- Training Data: 75% of the dataset
- Testing Data: 25% of the dataset

## Results

The model achieves high accuracy on the test set:

- Test Accuracy: 99.65%
- Precision: 99.9% (Healthy), 99.1% (Brain Tumor)
- Recall: 99.4% (Healthy), 99.8% (Brain Tumor)
- F1-Score: 99.7% (Healthy), 99.4% (Brain Tumor)

Training metrics:
- Maximum Training Accuracy: 99.79%
- Maximum Validation Accuracy: 99.71%
- Minimum Training Loss: 0.0086
- Minimum Validation Loss: 0.0253

## Inference

The trained model can be used to predict whether a given MRI image contains a brain tumor. Here's an example of a prediction:

Prediction: BRAIN TUMOR DETECTED

![image](https://github.com/user-attachments/assets/2ab393a9-dfc3-48a6-94ca-b2acc78e0657)

## Requirements

To run this project, you need the following dependencies:
- tensorflow
- keras
- numpy
- opencv-python
- scikit-learn
- matplotlib
- seaborn
- pandas

## Usage

1. Install required libraries: tensorflow, opencv-python, scikit-learn, matplotlib, seaborn
2. Prepare your dataset in the specified directory structure
3. Run the Jupyter notebook to train and evaluate the model
4. Use the trained model to predict on new brain MRI images

## Future Work

- Expand dataset with more diverse samples
- Experiment with other pre-trained models and architectures
- Implement model interpretability techniques
- Deploy model as a web application or API

## Conclusion

This project demonstrates the effectiveness of deep learning, particularly transfer learning using the VGG-16 model, in detecting brain tumors from MRI images. With a high accuracy rate and robust performance, this model can be a valuable tool for medical professionals.
