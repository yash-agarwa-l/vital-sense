# VitalSense AI Project

## Course  
UCS411  

## Institution  
Thapar Institute of Engineering and Technology, Patiala  

## Team Members  
- Aryaman Gudwani (102317279)  
- Daksh Jain (102497020)  
- Yash Agarwal (102317276)  

## Supervisor  
Ms. Kanika  

## Project Overview  
In emergency room (ER) settings, timely and accurate patient assessment is crucial for prioritizing medical care.  
Traditional triage methods are manual, time-consuming, and inconsistent, leading to delays, especially during high patient influxes.  

VitalSense is an AI-driven system that classifies patients into "Severe" and "Non-Severe" categories based on vital signs like heart rate, blood pressure, and oxygen saturation.  
This automation improves efficiency and ensures critical patients receive prompt care.  

## Dataset  
We use the **CVD Vital Signs dataset** from Kaggle, which includes:  
- Heart Rate (BPM)  
- Blood Pressure (Systolic & Diastolic)  
- Oxygen Saturation (SpO₂)  
- Respiratory Rate  
- Temperature  

**Dataset Link:** [CVD Vital Signs Dataset](https://www.kaggle.com/datasets/chidozieuzoegwu/cvd-vital-signs)  

## Machine Learning Models  
The following models are used for classification:  
- **Decision Trees** - Simple, interpretable model  
- **Random Forest** - Ensemble learning for better accuracy  
- **XGBoost** - Optimized gradient boosting technique  

## Accuracy and Model Improvement  
We measure performance using **accuracy** and other metrics like **precision, recall, and F1-score**.  
Steps to improve accuracy:  
1. **Data Cleaning** - Removing missing or incorrect values  
2. **Feature Selection** - Using only relevant vital signs  
3. **Model Selection** - Testing different algorithms  
4. **Hyperparameter Tuning** - Adjusting model settings for better performance  

## Future Scope  
- Deploying the model in a real-time ER environment  
- Integrating IoT devices for real-time vital sign monitoring  
- Enhancing predictive capabilities using deep learning  
