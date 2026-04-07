# Secure and Privacy-Preserving Machine Learning via Homomorphically Encrypted Neural Network Inference

“Can we make a machine learning model give predictions without ever seeing the user’s actual data?”
That is what homomorphic encryption helps with.

Normally, if a hospital wants to use a cloud ML model to predict whether a tumor is malignant or benign, they must send the patient’s medical values to the cloud in plain form. That is a privacy risk.

## Project Overview

In conventional cloud-based machine learning systems, user data must usually be sent in plaintext to the model for inference, which creates serious privacy concerns, especially in domains such as healthcare. This project addresses that issue by integrating **CKKS-based homomorphic encryption** with a lightweight neural network inference workflow.

The notebook performs the following tasks:

- Loads and preprocesses the **Breast Cancer Wisconsin dataset**
- Trains a **baseline plaintext neural network**
- Trains an **HE-friendly neural network** using a polynomial activation function
- Sets up the **CKKS homomorphic encryption scheme** using TenSEAL
- Encrypts test samples and performs encrypted inference
- Compares plaintext and encrypted inference in terms of:
  - Accuracy
  - Latency
  - Memory usage
  - Ciphertext size
  - Scalability

## Motivation

Sensitive medical data should not be exposed during prediction. Homomorphic Encryption enables computation directly on encrypted data, allowing inference without revealing the input values. This project explores the practicality, limitations, and tradeoffs of such a system.

## Features

- Privacy-preserving encrypted inference prototype
- Breast cancer diagnosis prediction
- Baseline vs encrypted inference comparison
- HE-compatible neural network design
- Performance analysis with latency and memory overhead
- Scalability study on encrypted inference

## Dataset

This project uses the **Breast Cancer Wisconsin Dataset** in CSV format.

Expected folder structure:

```bash
├── breast_cancer_dataset/
│   └── data.csv
│
├── training.ipynb
├── README.md
└── requirements.txt
├── he_inference_summary.csv
└── he_scalability_results.csv
