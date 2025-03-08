# VitalSense AI Project

## 1. Project Overview  

### 1.1 Problem Statement  
In emergency room (ER) settings, **timely and accurate patient assessment** is crucial for prioritizing medical care.  
Traditional triage methods rely on **manual evaluation** by healthcare professionals, which can be:  
- **Time-consuming** during peak hours  
- **Inconsistent** due to human error  
- **Prone to delays**, especially during staff shortages  

This problem was particularly evident during the **COVID-19 pandemic**, where a high influx of patients and limited staff resources led to delayed triage and inadequate prioritization.  

### 1.2 Our Solution  
We propose **VitalSense**, an AI-driven system designed to **automate emergency room triage** by analyzing key vital signs to determine a patient’s severity level.  

VitalSense processes real-time **physiological data** and classifies patients into two categories:  
- **Severe** - Requires immediate medical attention  
- **Non-Severe** - Can wait for further evaluation  

By automating this classification, VitalSense aims to:  
- Reduce reliance on **manual assessments**  
- Minimize **delays in patient care**  
- Ensure that **critical patients receive timely treatment**  

---

## 2. Dataset  

### 2.1 Dataset Description  
We are using the **CVD Vital Signs dataset** from Kaggle, which contains **real-time physiological data** collected from clinical settings.  

The dataset includes the following vital signs:  
- **Heart Rate (BPM)** - Measures heartbeats per minute  
- **Blood Pressure (Systolic & Diastolic)** - Tracks cardiovascular health  
- **Oxygen Saturation (SpO₂)** - Indicates oxygen levels in the blood  
- **Respiratory Rate** - Monitors breathing patterns  
- **Temperature** - Detects fever or hypothermia  

This dataset includes **23,469 rows** and **8 columns**, making it a suitable choice for supervised learning.  

**Dataset Link:** [CVD Vital Signs Dataset](https://www.kaggle.com/datasets/chidozieuzoegwu/cvd-vital-signs)  

### 2.2 Data Preprocessing  
Before training our model, we performed **extensive data preprocessing**, including:  
- **Handling missing values** by imputing median values  
- **Standardizing numerical features** using Min-Max Scaling  
- **Feature engineering** to derive additional insights from vital signs  
- **Splitting data into training (80%) and testing (20%) sets**  

---

## 3. Machine Learning Models  

We experimented with multiple machine learning algorithms and selected the following models for classification:  

### 3.1 Decision Trees  
- A **simple, interpretable model** that splits data based on feature conditions.  
- Useful for identifying key thresholds for vital signs.  

### 3.2 Random Forest  
- An **ensemble learning method** that combines multiple decision trees.  
- Provides **higher accuracy and robustness** compared to individual decision trees.  

### 3.3 XGBoost  
- A **gradient boosting technique** optimized for high performance.  
- Known for its **speed and accuracy** in classification tasks.  

We trained all models on labeled patient data to predict whether a patient falls into the **severe** or **non-severe** category.  

---

## 4. Model Performance Evaluation  

To evaluate the effectiveness of our models, we used the following **performance metrics**:  

### 4.1 Accuracy  
\[
\text{Accuracy} = \left( \frac{\text{Correct Predictions}}{\text{Total Predictions}} \right) \times 100
\]
- Measures the overall correctness of the model.  
- However, accuracy alone can be misleading in an **imbalanced dataset**.  

### 4.2 Precision  
\[
\text{Precision} = \frac{\text{True Positives}}{\text{True Positives} + \text{False Positives}}
\]
- Indicates how many predicted **severe** cases were actually severe.  

### 4.3 Recall  
\[
\text{Recall} = \frac{\text{True Positives}}{\text{True Positives} + \text{False Negatives}}
\]
- Measures how many actual **severe** cases were correctly identified.  

### 4.4 F1-Score  
\[
\text{F1-Score} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}
\]
- A balanced measure that considers both precision and recall.  

---

## 5. Accuracy Improvement Techniques  

We implemented several techniques to enhance model accuracy and reliability:  

### 5.1 Data Cleaning  
- Removed **incomplete or incorrect values**.  
- Standardized **numerical units** (e.g., BPM, temperature).  

### 5.2 Feature Engineering  
- Focused on **critical features** like heart rate, blood pressure, and SpO₂.  
- Eliminated irrelevant or redundant features.  

### 5.3 Model Selection and Hyperparameter Tuning  
- Experimented with different models to determine the **best-performing algorithm**.  
- Used **Grid Search** and **Random Search** to optimize hyperparameters.  
- Adjusted:  
  - Number of trees in **Random Forest** (10, 50, 100)  
  - Learning rate in **XGBoost** (0.01, 0.1, 0.3)  

---

## 6. Future Scope  

This project has significant potential for **real-world applications** and can be further improved by:  

### 6.1 Deployment in Real-Time ER Systems  
- Integrating the model into **hospital management software** for real-time decision-making.  
- Providing **automated alerts** for high-risk patients.  

### 6.2 IoT-Based Monitoring  
- Connecting IoT devices to **continuously monitor** patient vitals.  
- Reducing human intervention by automating **data collection**.  

### 6.3 Deep Learning for Enhanced Predictions  
- Implementing **Recurrent Neural Networks (RNNs)** for time-series analysis of patient vitals.  
- Using **CNNs or LSTMs** for more advanced **pattern recognition**.  

---

## 7. Installation and Usage  

### 7.1 Requirements  
To run this project, install the required dependencies:  

```bash
pip install numpy pandas scikit-learn xgboost matplotlib seaborn

