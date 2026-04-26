# AI-Based Network Intrusion Detection using ML

Built an RF + XGBoost–based intrusion detection system to classify network traffic into attack types with high accuracy.  
Applied feature engineering and SMOTE, and deployed a model for real-time BENIGN vs ATTACK prediction.

## Project Overview

This project detects malicious network traffic using machine learning models trained on labeled network flow records. The system classifies traffic into multiple attack categories and provides a probability score for whether a live traffic sample is benign or malicious.

## Key Features

- Trained an RF + XGBoost ensemble classifier on 120K network traffic records
- Detected 5 attack types: DoS, PortScan, BruteForce, Bot, and WebAttack
- Extracted 21 traffic features including flow duration, byte rates, and TCP flag counts
- Used SMOTE to handle class imbalance between benign and attack traffic
- Compared Logistic Regression, Decision Tree, Random Forest, and XGBoost
- Achieved 99.93% accuracy and 99.81% F1 score
- Saved the trained model using joblib for reusable inference
- Built a prediction function for BENIGN vs ATTACK classification with probability score

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- imbalanced-learn
- Matplotlib
- Seaborn
- joblib

## Machine Learning Workflow

1. Load and clean network traffic dataset
2. Perform feature engineering on traffic flow attributes
3. Handle class imbalance using SMOTE
4. Train and compare multiple ML models
5. Evaluate models using accuracy, precision, recall, F1 score, and confusion matrix
6. Save the best-performing model
7. Run live-style prediction using the trained classifier

## Results

| Model | Accuracy | F1 Score |
|---|---:|---:|
| RF + XGBoost Ensemble | 99.93% | 99.81% |

## Future Improvements

- Integrate with Snort or Suricata alerts for real-time IDS deployment
- Add more attack classes and larger real-world traffic samples
- Build a dashboard for live monitoring and alert visualization
- Deploy the model as a REST API using Flask or FastAPI
