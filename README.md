# CodeAlpha_HandwrittenRecognition

# CodeAlpha_HandwrittenRecognition

# Handwritten Character Recognition - MNIST
### CodeAlpha Machine Learning Internship - Task 3

## Overview
Built a Convolutional Neural Network (CNN) to predict handwritten digits (0-9)
from images using the MNIST dataset.

Dataset used: [MNIST](http://yann.lecun.com/exdb/mnist/) (built into TensorFlow/Keras)  
Language: Python  
Notebook: Jupyter Notebook

---

## Model Architecture

| Layer | Details |
|-------|---------|
| Conv2D | 32 filters, 3x3, ReLU |
| MaxPooling2D | 2x2 |
| Conv2D | 64 filters, 3x3, ReLU |
| MaxPooling2D | 2x2 |
| Flatten | - |
| Dense | 128 units, ReLU |
| Dropout | 0.5 |
| Dense | 10 units, Softmax |

---

## Results

| Metric | Value |
|--------|-------|
| Test Accuracy | **99.26%** |
| Test Loss | 0.0238 |
| Training Accuracy | 99.05% |
| Validation Accuracy | 99.08% |
| Misclassified | 74 / 10,000 |

### Accuracy per digit

| Digit | Accuracy |
|-------|----------|
| 0 | 99.69% |
| 1 | 99.82% |
| 2 | 99.32% |
| 3 | 99.01% |
| 4 | 99.80% |
| 5 | 98.21% |
| 6 | 99.06% |
| 7 | 99.22% |
| 8 | 99.38% |
| 9 | 98.81% |

---

## Project Structure
```
CodeAlpha_HandwrittenRecognition/
├── reports/
│   └── figures/          # saved plots
├── models/               # saved model (not pushed to GitHub)
├── handwritten_recognition.ipynb
└── README.md
```

---

## How to Run

1. Open `handwritten_recognition.ipynb` in Jupyter Notebook
2. Run all cells from top to bottom
3. MNIST dataset downloads automatically via Keras

---

## Libraries Required

```bash
pip install numpy matplotlib seaborn tensorflow scikit-learn
```

---

## Key Takeaways

- CNN works extremely well on image tasks — 99%+ accuracy with a simple architecture
- Dropout (0.5) kept train and val accuracy close throughout, no overfitting
- Digit 5 was the hardest to classify — mostly confused with 3 and 6
- Most of the 74 misclassified images are genuinely ambiguous handwriting