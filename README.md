# Practical Lab 3 – Vanilla CNN and Fine-Tuned VGG16 for Dogs vs Cats Classification

This lab demonstrates how to build and evaluate two deep learning models to classify dog and cat images:

- A **Vanilla CNN** (custom convolutional neural network from scratch)
- A **Fine-Tuned VGG16** model (transfer learning with ImageNet weights)

---

## Dataset

- **Dataset** used: [Dogs vs Cats Dataset (Kaggle)](https://www.kaggle.com/datasets/biaiscience/dogs-vs-cats)
- A subset of **5000 images** (2000 train, 1000 validation, 2000 test) was used for training and evaluation.
- Images were pre-split using a custom Python script.

---

##  Models

### 1. Vanilla CNN
- 3 Convolutional Layers
- Trained from scratch
- Overfitting observed after Epoch 5

### 2. Fine-Tuned VGG16
- Transfer learning with frozen convolutional base
- Custom dense head
- Achieved ~**89%** accuracy on test data
- Better generalization and performance than Vanilla CNN

---

##  Evaluation Metrics

Both models were compared using:

- Accuracy
- Confusion Matrix
- Precision, Recall, F1-Score
- Precision-Recall Curves
- Visualization of misclassifications
- Side-by-side predictions on random test images

---

##  Model Download Links

Trained models are saved as `.keras` files. Download from the links below:

### Vanilla CNN Model
[ Download vanilla_cnn_best.keras](https://stuconestogacon-my.sharepoint.com/:u:/g/personal/akondeti7046_conestogac_on_ca/ETRrNrRqVINOqdQqN6Y9Hx8BOG0NSK7fhNTZ6Dg2nJO_CQ?e=DFe3rn)

### VGG16 Fine-Tuned Model
[ Download vgg16_finetuned_best.keras](https://stuconestogacon-my.sharepoint.com/:u:/g/personal/akondeti7046_conestogac_on_ca/ERFNfdBA_VdImxlWE4RTAgkBATfFy5NBEnGIQre2QQUkBQ?e=RGbhqy)

*These files are tracked using [DVC](https://dvc.org/) for version control.*

---


### **Results Summary:**

Vanilla CNN showed early overfitting after epoch 5

VGG16 achieved significantly better generalization

Transfer learning proved effective for limited datasets

Precision–Recall curves showed reduced false positives for VGG16


### ** Key Learnings:**

Designing CNN architectures from scratch

Applying transfer learning using pre-trained ImageNet weights

Managing overfitting with callbacks and fine-tuning

Evaluating classification models beyond accuracy

Version-controlling large models using DVC

### **Why This Project Matters**

This project demonstrates:

End-to-end deep learning workflow

Practical application of transfer learning

Strong evaluation and comparison methodology

Clean experimentation and reproducibility





 Dataset: https://www.kaggle.com/datasets/biaiscience/dogs-vs-cats







##  Setup Instructions

### 1. Create and activate a virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate     # Windows
