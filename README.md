# Student Performance Prediction (Deep Learning)

This project aims to predict the **Performance Index** of students based on various academic and socio-economic factors using a Deep Neural Network (DNN).

## 📋 Project Objectives
- Clean and preprocess a multi-feature dataset (33 features).
- Handle categorical data using **Label Encoding**.
- Apply **Feature Scaling** to optimize Gradient Descent performance.
- Build and train a Regression model using **TensorFlow/Keras**.

## 📊 Dataset Features
The dataset includes 649 instances with 33 columns such as:
- **Academic:** Study time, previous failures, and grades (G1, G2).
- **Socio-economic:** Parent's education, job, and family size.
- **Lifestyle:** Alcohol consumption, health, and extracurricular activities.

## 🛠️ Data Preprocessing Pipeline
1. **Cleaning:** Handled duplicates and checked for missing values (Dataset was clean with 0 nulls).
2. **Encoding:** Converted 17 categorical (string) columns into numerical values.
3. **Scaling:** Used `StandardScaler` to normalize features, ensuring the Neural Network converges faster.
4. **Splitting:** Divided the data into 80% Training and 20% Testing sets.

## 🧠 Model Architecture
I designed a **Sequential Neural Network** with the following structure:
- **Input Layer:** Matches the number of features (32).
- **Hidden Layer 1:** 32 Neurons (ReLU activation).
- **Hidden Layer 2:** 16 Neurons (ReLU activation).
- **Output Layer:** 1 Neuron (Linear activation for Regression).

**Optimization:**
- **Optimizer:** Adam (Adaptive Moment Estimation).
- **Loss Function:** Mean Squared Error (MSE).
- **Metric:** Mean Absolute Error (MAE).

## 📈 Results
The model achieved a significant reduction in error during training:
- **Final MAE:** ~1.2 (Meaning the prediction is off by only 1.2 points on average).
- **Efficiency:** The Loss curve showed smooth convergence over 100 epochs.

## 📂 Files
- `Student_Performance_NN.ipynb`: Full implementation from cleaning to evaluation.
- `Student_Performance.csv`: The raw dataset.
