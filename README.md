# Marine-Species-Classifier-using-Transfer-Learning-MobileNetV2-
This project implements an image classification model to identify different Marine species using transfer learning with MobileNetV2.The project is built and run in Google Colab, making it easy to replicate and test with minimal setup. Ideal for beginners in deep learning and computer vision.

The model leverages the efficiency of MobileNetV2 and is suitable for lightweight, accurate image classification tasks.


# 🐟 Marine Species Classifier using MobileNetV2

This project is a deep learning-based image classification system that identifies various Marine species from images. It uses **Transfer Learning** with **MobileNetV2**, a lightweight yet powerful convolutional neural network pre-trained on ImageNet.

Built in **TensorFlow** and designed to run in **Google Colab**, this model can be used to classify aquatic animals with high accuracy and efficiency.

---

## 📁 Dataset Structure

The dataset (`aquatic_dataset.zip`) should follow this structure once extracted:( DataSet Link : "https://www.kaggle.com/api/v1/datasets/download/mikoajfish99/marine-animal-images").

    aquatic_dataset/ └── images/ ├── train/ │ ├── class_1/ │ ├── class_2/ │ └── ... └── test/ ├── class_1/ ├── class_2/ └── ...


Each subfolder contains images of a specific aquatic category.

---

## 🚀 Features

- 📦 Dataset upload and auto-extraction
- 🧼 Image preprocessing (resizing + normalization)
- 🤖 Transfer Learning with MobileNetV2 (frozen base)
- 🧠 Dense layers with Dropout to reduce overfitting
- 📊 Training with validation and accuracy metrics
- 💾 Model saving and export as `.keras`
- 🖼️ Image upload for real-time predictions

---

## 🧠 Model Details

| Component           | Description                        |
|---------------------|------------------------------------|
| Base Model          | MobileNetV2 (imagenet weights)     |
| Input Size          | 128 × 128 × 3                      |
| Loss Function       | Sparse Categorical Crossentropy    |
| Optimizer           | Adam                               |
| Epochs              | 50                                 |
| Output Layer        | Softmax (for multi-class)          |

---

## 📥 Usage in Google Colab

1. Upload `aquatic_dataset.zip` when prompted.
2. Model will train and validate automatically.
3. Upload a test image (e.g., `test_fish.jpg`) to get predictions.

---

## 💾 Output

- Trained model file: `aquatic_model_transfer_learning.keras`
- Printed prediction of uploaded image's category

---

## 📜 License

This project is for educational purposes. Feel free to modify and use with attribution.

---

## 🔍 Example

```python
predicted_category = predict_image("test_fish.jpg")
print("Predicted Category:", predicted_category)


