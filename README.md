# Lung and Colon Cancer Classification with DenseNet121

This project focuses on developing a deep learning model using the DenseNet121 architecture to classify histopathological images of lung and colon cancer. The dataset used is sourced from Kaggle:  
[Lung and Colon Cancer Histopathological Images](https://www.kaggle.com/datasets/andrewmvd/lung-and-colon-cancer-histopathological-images).

## Dataset
The dataset contains histopathological images of lung and colon cancer, organized as:
- **Training Data**: Lung and colon images used for training the model.
- **Testing Data**: Separate lung and colon images for evaluating model performance.

---

## Project Overview
### Key Features
- **Data Augmentation**:  
  - Rescales pixel values to [0, 1] (normalization).  
  - Applies random transformations: rotation, width and height shift, zoom, shearing, and horizontal flips to improve model generalization.  
- **DenseNet121 Pretrained Model**:  
  - Leveraged as a feature extractor with weights pretrained on ImageNet.  
- **Custom Classification Layers**:  
  - Fully connected layers added to perform classification into three categories.  
- **Validation Split**:  
  - 80% of the training data is used for training, while 20% is allocated for validation.

---

## Project Structure
- **`train_dir`** – Directory containing training images.  
- **`test_dir`** – Directory containing test images.  
- **Data Augmentation** – Performed using `ImageDataGenerator` from Keras.  
- **DenseNet121 Model** – Enhanced with custom classification layers.

---

## Results
| Metric                  | Value      |
|------------------------|------------|
| **Training Accuracy**   | 0.9613     |
| **Training Loss**       | 0.0972     |
| **Validation Accuracy** | 0.9620     |
| **Validation Loss**     | 0.0927     |

The model achieved high accuracy and low loss on both training and validation datasets, indicating effective learning and minimal overfitting.

### 1. Clone the Repository  
```bash  
git clone https://github.com/ahmetbekir22/LungAndColonCancerClassification.git
