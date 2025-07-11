# ✍️ Predicting Handwritten Digits to Identify Motor Skill Deficiencies

## 🧠 Overview

This project explores the application of machine learning models—**K-Nearest Neighbors (KNN), Artificial Neural Networks (ANN), Convolutional Neural Networks (CNN), and Recurrent Neural Networks (RNN)**—to classify handwritten digits and investigate whether digit misclassifications can serve as indicators of **motor skill deficiencies** in students.

Trained on the `letters.csv` dataset, the models were evaluated using **accuracy, confusion matrices, classification reports, and cross-validation scores**. The findings demonstrate that **CNN** and **RNN** models offer superior performance, with potential for early diagnostic use in educational and clinical settings.

---

## 🎯 Objectives

- Classify handwritten digits using multiple ML models.
- Compare the effectiveness of KNN, ANN, CNN, and RNN on image data.
- Explore misclassifications to identify potential motor skill deficiencies.
- Provide insight into fine motor challenges faced by students.

---

## 📦 Dataset: `letters.csv`

- Each row: 1 handwritten digit sample
- Features: Pixel values (flattened)
- Target: Digit label (0–9)

### 🔍 Sample Preprocessing

- ✅ Loaded via `pandas`
- ✅ Normalized pixel values to [0,1]
- ✅ One-hot encoded target variable for ANN, CNN, and RNN
- ✅ Train-test split: 80/20

---

## 🧪 Models & Methodology

### 🔸 K-Nearest Neighbors (KNN)
- **K = 3**
- Simple baseline for classification
- **Accuracy**: 62%
- Common misclassifications: 3 vs 5, 7 vs 9
- Insight: Misclassified digits suggest potential motor pattern inconsistencies.

### 🔸 Artificial Neural Network (ANN)
- 3 Layers: Input → Hidden (128 units + Dropout) → Output
- **Activation**: ReLU (hidden), Softmax (output)
- **Optimizer**: Adam | **Loss**: Categorical Cross-Entropy
- **Accuracy**: 68%
- Visualized training/validation accuracy and loss
- Improved performance over KNN

### 🔸 Convolutional Neural Network (CNN)
- 2 Convolutional layers (32 and 64 filters)
- MaxPooling + Flatten + Dense layers
- Best at capturing spatial hierarchies
- **Accuracy**: 71%
- **Best overall performance**

### 🔸 Recurrent Neural Network (RNN) — LSTM
- 2 LSTM layers + Dense
- Captures sequential dependencies in pixel data
- **Accuracy**: 70%
- Slightly below CNN, but better than KNN/ANN

---

## 📊 Results Summary

| Model | Test Accuracy | Notable Feature |
|-------|---------------|-----------------|
| KNN   | 62%           | Simple baseline |
| ANN   | 68%           | Learns abstract patterns |
| CNN   | **71%**       | Best for image data |
| RNN   | 70%           | Good for sequential features |

---

## 📈 Visualizations

- 🔹 **Confusion Matrices**: Revealed which digits were commonly confused
- 🔹 **Accuracy & Loss Curves**: Tracked training progress and overfitting
- 🔹 **Sample Images**: Visual inspection of correctly vs incorrectly classified digits

---

## 💡 Key Insights

- CNN's spatial feature extraction enables superior recognition of digit patterns.
- RNN's sequential understanding allows robust interpretation of pixel streams.
- Misclassified digits may indicate **motor skill delays**, such as:
  - Poor stroke control (e.g., 3 vs 5)
  - Inconsistent pressure or angles (e.g., 4 vs 9)
- Early intervention can benefit from automated handwriting assessment tools like this.

---

## ⚠️ Limitations

- Dataset may not represent all variations in handwriting (e.g., left-handed writers, students with dysgraphia).
- Class imbalance and real-world noise not considered.
- Models assume pixel arrays fully represent motor intent.

---

## 🔍 Future Work

- Include time-sequence handwriting data (e.g., stroke order or pen pressure).
- Integrate CNN-RNN hybrid architectures for better spatial-temporal learning.
- Collaborate with occupational therapists for clinical validation.
- Expand dataset with children’s actual classroom handwriting samples.

---

## 📚 References

- LeCun, Y., Bengio, Y., & Hinton, G. (2015). Deep learning. *Nature*, 521(7553), 436–444.
- Graves, A. (2013). *Supervised Sequence Labelling with Recurrent Neural Networks*. Springer.
- Piek, J. P., et al. (2007). Motor coordination and social-emotional problems in preschool-aged children. *Developmental Medicine & Child Neurology*, 49(10), 755–760.
- King, R. D., & Zeng, H. (2020). Evaluation metrics for machine learning algorithms. *Journal of Machine Learning Research*, 21(1), 1–19.

---

## 🧠 Author
**Mohammed Saif Wasay**  
*Data Analytics Graduate — Northeastern University*  
*Machine Learning Enthusiast | Passionate about turning data into insights*

🔗 [Connect with me on LinkedIn](https://www.linkedin.com/in/mohammed-saif-wasay-4b3b64199/)

---
