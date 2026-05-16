# Neural Network Fundamentals and Training Behavior Analysis

## Project Overview

This project builds and evaluates a feed-forward neural network model for a supervised learning problem using customer churn prediction data.

The objective is to understand:
- Forward propagation
- Loss calculation
- Backpropagation
- Parameter updates
- Neural network training behaviour

The project also compares different hyperparameter configurations to study their impact on model performance.

---

# Dataset Description

Dataset: `customer_churn_nn.csv`

Target Variable:
- `churn`
  - 1 = Customer churned
  - 0 = Customer retained

Example Features:
- region
- plan_type
- contract_type
- payment_method
- monthly_charges
- tenure
- support_calls

---

# Approach

## 1. Dataset Understanding
Performed:
- Dataset shape inspection
- Data type analysis
- Missing value check
- Statistical summary
- Target distribution visualization

---

## 2. Data Preprocessing
Steps performed:
- Removed identifier column (`customer_id`)
- Handled missing values using:
  - Median imputation for numerical columns
  - Most frequent imputation for categorical columns
- Encoded categorical variables using OneHotEncoder
- Scaled numerical features using StandardScaler
- Split dataset into training and testing sets

---

## 3. Neural Network Model Building
Built a feed-forward neural network using TensorFlow/Keras.

Model architecture:
- Input layer
- Hidden layer with ReLU activation
- Additional hidden layer
- Output layer with Sigmoid activation

Configuration:
- Loss Function: Binary Crossentropy
- Optimizer: Adam
- Evaluation Metric: Accuracy

---

## 4. Training and Evaluation
The model was trained on the training dataset and evaluated using:
- Training Accuracy
- Testing Accuracy
- Training Loss
- Testing Loss
- Confusion Matrix
- Classification Report

Evaluation graphs were saved in:
- `results/evaluation_outputs.png`

---

## 5. Hyperparameter Experiments
Multiple experiments were conducted by varying:
- Number of neurons
- Learning rate
- Number of epochs

Results were compared and saved in:
- `results/model_comparison_table.csv`

---

# Observations

- Feature scaling improved neural network convergence.
- ReLU activation helped the model learn non-linear patterns efficiently.
- Increasing neurons improved learning capacity but also increased training time.
- Very high learning rates caused unstable training.
- The final model achieved good generalization because training and testing accuracy were relatively close.
- No severe overfitting was observed.

---

# Repository Structure

part-1-neural-network-analysis/

├── README.md  
├── notebook.ipynb  
├── requirements.txt  
└── results/  
  ├── model_comparison_table.csv  
  └── evaluation_outputs.png  

---

# Requirements

Install dependencies using:

```bash
pip install -r requirements.txt