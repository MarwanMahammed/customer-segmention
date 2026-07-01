# Advanced Customer Segmentation using RFM & K-Means Clustering

## 📌 Project Overview
This project delivers a data-driven customer segmentation framework for an online retail dataset. By utilizing the **RFM (Recency, Frequency, Monetary)** behavioral model and **K-Means Clustering** (Unsupervised Machine Learning), we segmented **4,338 unique customers** into distinct behavioral groups. This enables targeted marketing strategies, increases customer retention, and optimizes campaign ROI.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Manipulation:** Frameworks like Pandas, NumPy
* **Machine Learning:** Scikit-learn (KMeans, StandardScaler)
* **Data Visualization:** Matplotlib, Seaborn

---

## 🚀 Data Preprocessing & Quality Audit
1. **Handling Missing Data:** Missing `CustomerID` records were carefully dropped. Statistical imputation (like Mode) was strictly avoided to prevent massive data distortion during aggregation.
2. **Temporal Boundaries:** Transaction times were logged uniformly at midnight (`00:00`), so analysis was shifted from an hourly focus to highly reliable **Monthly & Day-of-Week patterns**.
3. **Feature Engineering:** Calculated **Recency** (days since last purchase), **Frequency** (total unique orders), and **Monetary** (total spend) per customer.
4. **Transformation:** Applied **Log Transformation** to fix data skewness and **StandardScaler** to normalize feature weights before clustering.

---

## 📊 Model Evaluation & Cluster Selection
We evaluated the model using the joint insights of the **Elbow Method** and **Silhouette Score**:
* **K = 2** was selected because it achieved the **Global Maximum** on the Silhouette Score, ensuring mathematically optimal separation, maximum stability, and clear business boundaries.

---

## 📈 Final Customer Profiles

| Cluster ID | Strategic Segment Label | Recency | Frequency | Monetary | Action Plan |
| :---: | :--- | :---: | :---: | :---: | :--- |
| **Cluster 0** | **High-Value Champions** | Low | High | Very High | VIP Loyalty Programs & Cross-selling |
| **Cluster 1** | **Dormant / At-Risk** | High | Low | Low | Win-back Drip Campaigns & Feedback Surveys |

---

## 📁 Repository Structure
* `notebooks/`: Contains the complete end-to-end Jupyter Notebook code.
* `reports/`: Contains the final English PDF report and presentation slides.

---
*Developed as part of the NTI Machine Learning track deliverables for evaluation on July 7, 2026.*
