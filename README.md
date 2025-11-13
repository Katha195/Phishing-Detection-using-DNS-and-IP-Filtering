# Phishing-Detection-using-DNS-and-IP-Filtering

This research project presents a machine learning-based system for detecting phishing URLs by analyzing DNS records and IP addresses.
Core Approach
The project combines traditional cybersecurity analysis with machine learning to identify malicious URLs. The system extracts technical features from URLs and uses logistic regression to classify them as either legitimate or phishing attempts.
Methodology (4-Step Process)
1. Data Collection

Dataset sourced from Kaggle containing both legitimate and malicious URLs
URLs categorized by DNS record count and phishing classification
Malicious URLs clearly labeled for supervised learning

2. DNS Record & IP Address Extraction

Python's socket and urlparse libraries used to extract DNS records and IP addresses
Handles edge cases like port numbers and unresolved domains
Ensures dataset integrity through exception handling

3. Model Training

Logistic regression model trained on extracted features
Key features: IP reputation, DNS record types, domain age, registration details, geolocation
Model produces probability scores (0-1) indicating likelihood of phishing
Binary classification: 0 for legitimate, 1 for phishing

4. Classification & Detection

Threshold set at 0.75 probability score
URLs exceeding threshold flagged as phishing
Real-time detection capability for new URLs

Results

Accuracy: 75% on test data
AUC: Evaluated using ROC curve analysis
Model successfully distinguishes between legitimate and phishing URLs
Performance metrics include precision, recall, and F1-score from confusion matrix

Significance
The project addresses the critical cybersecurity challenge of phishing attacks by providing an automated, data-driven detection system that can adapt to evolving threats while offering real-time protection for individuals and organizations.
