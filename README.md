Crypto-Scam-Detection
A machine learning pipeline for detecting fraudulent cryptocurrency transactions. Using XGBoost and Random Forest classifiers, this project analyzes transaction patterns to identify scams with a prioritized focus on minimizing False Negatives (missed scams) through strategic threshold optimization.
Project Overview
This project addresses the growing challenge of security in decentralized finance (DeFi). We developed a predictive model to identify scam transactions within a cryptocurrency dataset, balancing the trade-offs between precision and recall to ensure maximum security for users.

Technical Implementation & Workflow
Data Analysis & Preprocessing: Conducted comprehensive Exploratory Data Analysis (EDA) including missing value heatmaps and feature distributions for gas fees and transaction intervals.

Model Selection: 
Evaluated multiple classification algorithms, including Random Forest and XGBoost, to determine the most effective architecture for fraud detection.

Threshold Engineering (The Core Work): 
* Analyzed the inverse relationship between Precision and Recall specifically for the "Scam" class.
Optimized the classification threshold to 0.3 (lowered from the default 0.5) to prioritize sensitivity.
Successfully reduced False Negatives from 140 to 84, ensuring that fewer scams are missed by the system at the cost of slightly higher false alarms.

Key Performance Metrics
*Initial Findings: At a 0.5 threshold, the model missed 1,401 scams with a recall of 0.56.
*Optimized Results: By adjusting the threshold to 0.3, we achieved a recall of 0.97, successfully capturing the vast majority of fraudulent activity.

Critical Findings:
The Threshold Trade-offThe most significant part of this group activity was the discovery of the Inverse Relationship between Precision and Recall for the Scam class.
Metric                            Default (0.5 TH)        Optimized (0.3 TH)
*Recall (Scam Detection)              0.56                      0.97
*False Negatives (Missed Scams)       140                        84
*Scam Precision                       0.34                      0.30

Future Scope
*Cost-Sensitive Learning: Quantifying the exact financial loss of a missed scam versus the operational cost of a false flag to further automate threshold selection.
*Feature Engineering: Exploring advanced blockchain-specific features to improve the precision of the current model.
