# 🏦 **Credit Card Fraud Detection Using Unsupervised Learning**

This project explores how **unsupervised machine learning** can be used to detect unusual credit card customer behavior and identify potential fraud risks **without any labeled fraud data**.
By analyzing spending, repayment, and cash-advance patterns, the system uncovers **customer segments** and highlights **anomalous activity** worthy of deeper investigation.

---

## 📌 **Project Overview**

Traditional fraud detection relies on labeled historical fraud cases, which are often incomplete or unavailable.
This project solves that challenge using unsupervised learning techniques, enabling fraud and anomaly detection purely from behavior patterns.

The project includes:

* Customer segmentation
* Anomaly detection
* Dimensionality reduction for visualization
* Behavioral pattern interpretation
* Outlier identification

---

## 📁 **Dataset Description**

The dataset contains **8,950 credit card customers** and includes **18 behavioral features**, such as:

* Balance behavior
* Purchase types and frequency
* Cash advances
* Payment amounts and frequency
* Credit limit
* Full-payment percentage
* Tenure of account activity

These features allow for deep behavioral pattern discovery and profiling.

---

## 🧹 **Data Preparation**

Key preprocessing steps include:

* Removing non-informative identifier columns
* Handling missing values through interpolation
* Detecting and removing extreme outliers using statistical thresholds
* Standardizing features for consistent behavior comparison

This ensures reliable clustering and meaningful anomaly detection.

---

## 🔍 **Unsupervised Learning Methods**

### **1. K-Means Clustering**

Used to group customers with similar financial behaviors.
Silhouette analysis determined that **8 clusters** best represent the natural groupings within the dataset.

These clusters reveal segments such as:

* Low-usage customers
* High-value spenders
* Customers heavily reliant on cash advances
* EMI-focused shoppers
* Customers with high balances but regular payments
* High-risk customers with overdue payments

---

### **2. PCA Visualization**

To simplify interpretation, **Principal Component Analysis (PCA)** was used to transform the 18-dimensional dataset into two visual components.

The results clearly separate major customer groups and validate the structure revealed by clustering.

---

### **3. DBSCAN Anomaly Detection**

DBSCAN, a density-based model, identifies customers whose behavior deviates significantly from typical patterns.

Customers classified as outliers often exhibit characteristics such as:

* Unusually high cash advances
* Large balances with minimal repayment
* Irregular or inconsistent spending behavior

These represent potential fraud risk or financially unstable customer profiles.

---

### **4. Isomap Visualization**

Isomap, a nonlinear dimensionality reduction method, was used to visualize DBSCAN results.
This highlights dense clusters of normal customer behavior and isolates sparse, abnormal activity—making anomalies easy to interpret visually.

---

## 📊 **Key Results**

* **Eight meaningful customer segments** discovered through clustering
* **Anomalous customers identified** via DBSCAN
* **Visual validation** of clusters using PCA and Isomap
* **Unsupervised learning successfully detects suspicious patterns** without any fraud labels
* Provides a foundation for **early fraud detection** and **customer risk scoring**

---

## 🚀 **Future Work**

To build a complete fraud detection ecosystem:

* Apply deep learning–based anomaly detection (autoencoders)
* Incorporate time-series transaction analysis
* Combine unsupervised and supervised learning when fraud labels become available
* Deploy the model as a real-time fraud detection API
* Utilize advanced clustering methods like HDBSCAN for improved anomaly separation

---
