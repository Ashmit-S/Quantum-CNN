# Quantum Convolutional Neural Networks for Image Classification

## Overview
This project explores the performance of Quantum Convolutional Neural Networks (QCNNs) for image classification under varying levels of image resolution and class complexity.

The work was conducted as part of undergraduate research in collaboration with Dr. Shitala Prasad from IIT Goa and resulted in a paper accepted at ICTCon 2024 (Springer Proceedings).

---

## Motivation
Classical CNNs require large datasets and significant computational resources. This project investigates whether QCNNs can achieve comparable performance in low-data settings and how they scale with increasing task complexity.

---

## Datasets Used
- scikit-learn Digits dataset (8×8 grayscale)
- MNIST (downscaled from 28×28 to 8×8)
- CIFAR-10 (downscaled to 8×8 and converted to grayscale)

All datasets were standardized to enable fair comparison across different complexity levels.

---

## Approach
- Implemented QCNN using **PennyLane** 
- Used amplitude embedding to encode image data into quantum states
- Designed quantum convolutional layers using:
  - U3 gates
  - Ising interaction gates
- Applied quantum pooling and dense layers for classification

Experiments were conducted across:
- Binary classification (low complexity)
- Multi-class classification (higher complexity)
- Different dataset sizes and resolutions

---

## Key Findings

### 1. Strong performance in low-data settings
- Achieved ~96–97% accuracy on binary classification tasks using only ~80 training samples

### 2. Sensitivity to dataset complexity
- CIFAR-10 (downscaled) achieved ~50% accuracy despite similar training setup

### 3. Performance drops with more classes
- MNIST (10 classes): ~27% accuracy
- CIFAR-10 (10 classes): ~11–14% accuracy

### 4. Key Insight
QCNNs perform well on simple, low-resolution, low-class problems but struggle as:
- image complexity increases
- number of classes increases
- required qubits increase

---

## My Contribution
- Implemented QCNN architecture using PennyLane
- Designed experiments across multiple datasets and resolutions
- Analyzed performance trends with respect to:
  - image size
  - dataset complexity
  - number of classes
- Contributed to experimental design and result interpretation

---

## Technologies Used
- Python
- PennyLane
- PyTorch
- NumPy

---

## Key Takeaway
QCNNs show promise for low-data, low-complexity tasks but face scalability challenges as problem complexity increases.

---

## Paper
Springer Link: https://link.springer.com/chapter/10.1007/978-3-032-10250-8_8
