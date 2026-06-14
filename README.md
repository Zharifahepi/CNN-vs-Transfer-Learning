# CNN-vs-Transfer-Learning

**Name:** Zharifah Zahra Salsabila
**NIM:** 452024618106
**Study Program:** Teknik Informatika
**University:** Universitas Darussalam Gontor

This project compares the performance of CNN From Scratch and Transfer Learning (MobileNetV2) for image classification tasks.

The objective of this experiment is to analyze the differences between both approaches in terms of:

- Accuracy
- Loss
- Training Time
- Number of Parameters
- Generalization Ability
- Overfitting Risk

---

## Dataset

### CNN From Scratch

Dataset: CIFAR-10

### Transfer Learning

Dataset: Cats vs Dogs

---

## Model Architecture

### CNN From Scratch

- Conv2D (32)
- MaxPooling2D
- Conv2D (64)
- MaxPooling2D
- Conv2D (128)
- Flatten
- Dense (128)
- Dropout (0.5)
- Output Layer

### Transfer Learning

Backbone:

- MobileNetV2 (ImageNet Pretrained)

Classifier:

- GlobalAveragePooling2D
- Dense (128)
- Dropout (0.5)
- Dense (1)

---

## Experimental Results

| Metric              | CNN     | Transfer Learning |
| ------------------- | ------- | ----------------- |
| Training Accuracy   | 81.70%  | 98.85%            |
| Validation Accuracy | 72.69%  | 98.51%            |
| Testing Accuracy    | 71.88%  | 98.40%            |
| Training Loss       | 0.5097  | 0.0314            |
| Validation Loss     | 0.8626  | 0.0408            |
| Training Time (s)   | 603     | 2552              |
| Parameters          | 356,810 | 2,422,081         |

---

## Repository Structure

```text
project-cnn-vs-transfer-learning/
├── dataset/
├── notebook/
├── report/
├── README.md
└── requirements.txt
```

## How to Run
Install dependencies:

```bash
pip install -r requirements.txt
```

Run notebook:

```bash
jupyter notebook notebook/cnn_vs_transfer_learning.ipynb
```

## Conclusion

Based on the experimental results, Transfer Learning using MobileNetV2 achieved significantly higher performance than CNN From Scratch. Transfer Learning achieved a testing accuracy of 98.40%, while CNN From Scratch achieved 71.88%.
