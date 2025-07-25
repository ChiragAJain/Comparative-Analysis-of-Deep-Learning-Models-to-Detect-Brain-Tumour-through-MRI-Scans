# A Comparative Analysis of Brain Tumour Detection Models using Deep Learning

This repository contains the code and resources for the paper titled "A Comparative Analysis of Brain Tumour Detection Models using Deep learning Model", which will be presented at the 2nd International Conference on Artificial Intelligence and Machine Vision (AIMV-2025).

***

## 📖 Introduction

A brain tumor is an abnormal growth of cells within the brain. Early and accurate detection is crucial, but manual interpretation of Magnetic Resonance Imaging (MRI) scans can be time-consuming and prone to error. This study explores the use of deep learning models to automate the detection and classification of brain tumors from MRI scans, aiming to improve accuracy and efficiency. We compare several deep learning architectures to identify the most reliable approach for potential clinical use.

***

## ⚙️ Methodology

The process involves the following key stages:

1.  **Data Acquisition**: The study utilizes both an internal and an external MRI dataset. The datasets contain three types of tumors (Glioma, Meningioma, Pituitary) and non-tumorous scans.
2.  **Data Transformation**: MRI scans are resized to a uniform $224 \times 224$ pixels and normalized. The data is then converted into tensors for processing by the deep learning models.
3.  **Model Selection**: Five deep learning models were selected for comparison:
    * A custom-built Convolutional Neural Network (CNN)
    * VGG16
    * VGG19
    * Xception
    * EfficientNet with Self-Attention
4.  **Training and Validation**: The models were trained using a 10-fold cross-validation approach for 25 epochs. The Adam optimizer and a `ReduceLROnPlateau` learning rate scheduler were employed. Early stopping with a patience of 5 was used to prevent overfitting.
5.  **Performance Evaluation**: Models were evaluated based on accuracy, precision, recall, and F1-score on both internal and external test datasets.
6.  **Hypothesis Testing**: Statistical tests, including the Friedman, Nemenyi, and Cohen's d tests, were conducted to validate the significance of the performance differences between the models.

***

## 📊 Results

The performance of the five models was rigorously evaluated. The EfficientNet with Self-Attention model consistently achieved the highest scores across all metrics on both internal and external datasets.

### Performance Metrics

| Model | Internal Test Accuracy (%) | External Test Accuracy (%) | Internal Test F1-Score (%) | External Test F1-Score (%) |
| :--- | :--- | :--- | :--- | :--- |
| CNN | 95.96 | 98.79 | 96.07 | 98.73 |
| VGG16 | 95.94 | 99.32 | 96.02 | 99.28 |
| VGG19 | 96.36 | 99.52 | 96.52 | 99.49 |
| Xception | 95.81 | 99.25 | 95.99 | 99.22 |
| **EfficientNet-Attn** | **97.45** | **99.82** | **97.54** | **99.82** |

### Statistical Analysis

The hypothesis testing confirmed the superior performance of the EfficientNet with Self-Attention model. The Friedman test yielded a significant p-value of 0.004. Subsequent Nemenyi post-hoc tests revealed that EfficientNet with Self-Attention significantly outperformed Xception and the baseline CNN. Furthermore, Cohen's d test showed a large quantifiable performance difference between EfficientNet and the other models.

***

## 🏆 Conclusion

This study provides a comprehensive comparison of five deep learning models for brain tumor classification. The results demonstrate that the **EfficientNet with Self-Attention** architecture is the most robust and effective model among those evaluated, showcasing excellent performance and generalization capabilities. This highlights the potential of advanced deep learning models in medical imaging to enhance diagnostic accuracy and consistency.

Future work could explore hybrid models that combine the strengths of different architectures to further improve diagnostic capabilities.

***
