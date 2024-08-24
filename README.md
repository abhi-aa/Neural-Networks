# Neural Networks Lab - Lab 4

This repository contains the implementation and analysis of various neural network configurations to approximate a given mathematical function and solve the XOR problem. The lab exercises explore different neural network architectures, activation functions, and data processing techniques.

## **Lab Objectives**

- **Function Approximation:** Implement different configurations of neural networks to approximate the function: $y = 0.2x^4 + 2x^3 + 0.1x^2 + 10$.
  where \( x \) is a real number between \(-1\) and \(1\) inclusive.

- **XOR Problem:** Implement a neural network from scratch to solve the XOR classification problem.

## **Implementation Steps**

### **1. Data Generation**

- **Task:** Create 30,000 samples with \( x \) values uniformly distributed between \(-1\) and \(1\), and compute corresponding \( y \) values using the given function.
- **Function:** `generate_data`
- **Output:** Initial plot of the function.

### **2. Data Shuffling**

- **Task:** Write a function to shuffle the data based on an input argument.
- **Function:** `get_dataset(shuffle=True)`

### **3. Data Splitting**

- **Task:** Split the data into training, validation, and test sets with specified ratios.
- **Function:** `split_data(train_ratio, val_ratio, test_ratio)`

### **4. Data Scaling**

- **Task:** Scale the data to be within the range of 0 and 1.
- **Function:** `scale_data(data)`

### **5. Error Metrics**

- **Task:** Calculate Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R-squared (R²) score.
- **Function:** `calculate_errors(actual, predicted)`

## **Neural Network Configurations**

Two neural network structures are implemented with different hyperparameters:

### **Structure 1**
- **Layers:**
  - Fully Connected Layer (12 units)
  - Fully Connected Layer (8 units)
  - Fully Connected Layer (4 units)

### **Structure 2**
- **Layers:**
  - Fully Connected Layer (24 units)

### **Common Parameters for All Cases**
- **Data Split Ratios:** 30% training, 20% validation, 50% test
- **Number of Epochs:** 20
- **Batch Size:** 12
- **Loss Function:** MSE
- **Optimizer:** Adam

## **Experiment Cases**

The following cases are evaluated:

1. **Case 1:** Shuffled, unscaled data, Structure 1, ReLU activation.
2. **Case 2:** Shuffled, unscaled data, Structure 2, ReLU activation.
3. **Case 3:** Shuffled, unscaled data, Structure 1, tanh activation.
4. **Case 4:** Shuffled, scaled data, Structure 1, ReLU activation.
5. **Case 5:** Shuffled, scaled data, Structure 1, tanh activation.

Each case is also repeated without shuffling the data.

## **XOR Problem**

- **Task:** Solve the XOR classification problem using a neural network designed from scratch, without using any high-level APIs.
- **Implementation:** Include the design of layers, activation functions, loss function, etc., in the code.
