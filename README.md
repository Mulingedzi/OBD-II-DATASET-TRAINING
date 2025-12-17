# OBD-II-DATASET-TRAINING
A machine learning framework for real-time OBD-II vehicle fault detection. Compares Random Forest, LightGBM, and Isolation Forest for high-accuracy, low-latency automotive diagnostics.
# Machine Learning for Real-Time OBD-II Fault Detection

This repository contains a Jupyter Notebook (`Training_OBDII.ipynb`) designed to evaluate and compare machine learning models for detecting faults in vehicle systems using **On-Board Diagnostics (OBD-II)** sensor data. The project specifically focuses on identifying anomalies in engine performance (RPM deviations) to support predictive maintenance.

## Project Overview

Traditional OBD-II diagnostics rely on static, rule-based thresholds which often lead to delayed fault detection. This research implements a data-driven approach using supervised and unsupervised machine learning to detect faults with high accuracy and low latency, making it suitable for real-time edge deployment.

### Key Features:
* **Data Preprocessing:** Automated handling of missing values using mean imputation.
* **Feature Engineering:** Automated labeling of engine faults based on statistical deviations (1 standard deviation from the mean).
* **Multi-Model Comparison:** Evaluation of **Random Forest**, **LightGBM**, and **Isolation Forest**.
* **Performance Metrics:** Analysis of Accuracy, Precision, Recall, F1-Score, ROC-AUC, and **Inference Latency**.

## Prerequisites

To run this notebook, you need a Python 3 environment (ideally **Google Colab**) with the following libraries installed:

```bash
pip install pandas numpy scikit-learn matplotlib lightgbm

## DATASET

The notebook is designed to work with vehicle sensor datasets in CSV format. The expected features include:
1 Engine RPM
2 Vehicle Speed
3 Throttle Position
4 Coolant Temperature
5 Engine Load

Note: The notebook includes a file upload step specifically for Google Colab users (files.upload()).

## Notebook Workflow
1 Data Acquisition: Uploading the raw CSV data via the Colab interface.
2 Cleaning: Filling missing values using mean imputation to maintain data integrity.
3 Labeling: Creating a target variable where a "Fault" is defined as an RPM value exceeding one standard deviation from the mean.
4 Scaling: Normalizing features using StandardScaler for consistent model performance.

## Model Training:

Random Forest: An ensemble method used for robust classification.
LightGBM: A gradient boosting framework optimized for speed and efficiency.
Isolation Forest: An unsupervised approach used to identify outliers/anomalies.
Evaluation: Generating a comparative report of all models to identify the most suitable candidate for real-time application.

## Usage
Open the Training_OBDII.ipynb file in Google Colab or Jupyter Notebook.
Run the first cell to import necessary libraries.
When prompted, upload your OBD-II dataset (CSV).
Execute the remaining cells sequentially to generate the performance metrics and comparison charts.

## Results Summary
The implementation identifies LightGBM as the strongest candidate for real-time deployment due to its:
Superior ROC-AUC: Achieving high predictive power (~0.9547).
Low Latency: Processing inference in approximately 0.1446 seconds, meeting the stringent time constraints of automotive systems.

##Author
Mulingedzi Angel Rakhumba Bachelor of ICT Honors
University of Mpumalanga
Email: 222525754@ump.ac.za



