# 🐶🐱 Cat vs Dog Image Classifier using CNN

## 📌 Project Overview
This deep learning project classifies images of cats and dogs using a custom-built Convolutional Neural Network (CNN). The model is trained on the **Dogs vs. Cats - filtered 25K** dataset from Kaggle and includes an **interactive Gradio web interface** for real-time predictions via uploaded images.

---

## ⚙️ Technologies Used

- **Python 3**
- **TensorFlow / Keras**
- **OpenCV**
- **Matplotlib**
- **Gradio**
- **Kaggle API**
- **Google Colab**

---

## 📁 Dataset

- **Source**: [Dogs vs. Cats - filtered 25K (Kaggle)](https://www.kaggle.com/datasets/salader/dogs-vs-cats)
- **Size**: ~25,000 images
- **Labels**: Balanced classes (`cats`, `dogs`)
- **Structure**:
  ```
  /train
      /cats
      /dogs
  /test
      /cats
      /dogs
  ```

---

## 🚀 Workflow Summary

### 🔽 1. Dataset Handling
- Downloaded using the Kaggle API.
- Extracted and organized into training and testing folders.

### 🧹 2. Data Preprocessing
- Images resized to **256×256**.
- Normalized pixel values to `[0, 1]`.
- Augmentation applied (flip, rotation, zoom).
- Shuffled and batched using `image_dataset_from_directory()`.

### 🧠 3. CNN Model Architecture

```
Conv2D (32) → BatchNormalization → MaxPooling
Conv2D (64) → BatchNormalization → MaxPooling
Conv2D (128) → BatchNormalization → MaxPooling
Flatten → Dense(128) → Dropout
Dense(64) → Dropout → Dense(1, sigmoid)
```

### ⚙ 4. Training

- **Optimizer**: Adam
- **Loss**: Binary Crossentropy
- **Metric**: Accuracy
- **Class Weights**: Used for balance
- **Early Stopping**: Enabled (patience = 3)

### 📊 5. Evaluation

- Plotted **training vs validation** loss and accuracy curves.
- Visualized confusion matrix.
- Tested on **custom uploaded images**.

---

## 🖼 Example Predictions

| Image | Prediction | Score |
|-------|------------|-------|
| 🐱 cat-1.jpeg | CAT | 0.1362 |
| 🐶 download.jpeg | DOG | 0.8059 |

---

## 🌐 Gradio Interface

- Web-based UI for real-time prediction
- Upload any cat/dog image or use webcam
- See prediction and confidence level instantly



---

## ✅ Requirements

```bash
pip install tensorflow opencv-python matplotlib gradio numpy
```

---

## 📂 How to Use

1. Upload your `kaggle.json` to authenticate with Kaggle.
2. Run the notebook step-by-step in **Google Colab**.
3. Test predictions using:
   - Custom `.jpeg` or `.png` images.
   - Live Gradio interface.

---

## 👨‍💻 Developed By

**Uplakshya Tiwari**  
Student at United College of Engineering and Research, Naini, Prayagraj.  

