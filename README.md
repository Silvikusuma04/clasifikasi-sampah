# Garbage Image Classification with Deep Learning

## Project Overview

This project demonstrates the implementation of a deep learning model for **garbage image classification** using **EfficientNetV2L**. It is developed as part of the **Submission 2** requirement for the Dicoding course: *Belajar Pengembangan Machine Learning*.

The model is trained on the **Garbage Dataset**, which contains 19,762 images across 10 categories of common waste items. This project covers the complete pipeline: data preprocessing, model training, performance evaluation, and model conversion for deployment on web and mobile platforms.

## Dataset

- **Name**: Garbage Dataset
- **Total Images**: 19,762
- **Classes**: Metal, Glass, Biological, Paper, Battery, Trash, Cardboard, Shoes, Clothes, Plastic.
- **Source**: [Kaggle - Garbage Dataset](https://www.kaggle.com/datasets/sumn2u/garbage-classification-v2)


## Data Splitting

- **Training Set**: 70%
- **Validation Set**: 15%
- **Test Set**: 15%

## Model Architecture

- Base model: **EfficientNetV2L** (`include_top=False`)
- Fine-tuning applied to 30 last layers 
- Additional layers:
  - Conv2D + ReLU
  - BatchNormalization
  - MaxPooling2D, GlobalAveragePooling2D
  - Dense layers + Dropout
  - Softmax output (10 classes)

## Preprocessing Steps

- Resize to 384x384 pixels
- Normalize with `preprocess_input`
- Load using `image_dataset_from_directory`

## Model Saving and Inference

- Model saved in four formats: SavedModel, Keras (.keras), TensorFlow Lite (.tflite), and TensorFlow.js (.json).
- Performed inference using the TensorFlow Lite (.tflite) model.

## Credits

This project was created by Silvi Kusuma Wardhani Gunawan as part of the requirements for:
**Dicoding - Belajar Pengembangan Machine Learning (Submission 2)**

## License

This project is licensed under the MIT License.
