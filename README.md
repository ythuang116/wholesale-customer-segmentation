# 🧠 Wholesale Customer Segmentation - Exploratory Clustering Analysis

This project explores customer segmentation for a wholesale distribution company based on their annual product spending. 

---

## 📦 Dataset Overview

The dataset contains **440 wholesale clients** in Portugal and their **annual spending** (standardized monetary units) across 6 product categories. It also includes metadata on **sales channel** and **region**.

| Column Name         | Description                                                   |
|---------------------|---------------------------------------------------------------|
| Channel             | 1 = Horeca (Hotel/Restaurant/Café), 2 = Retail                |
| Region              | 1 = Lisbon, 2 = Oporto, 3 = Other Regions                     |
| Fresh               | Spending on fresh products                                    |
| Milk                | Spending on milk products                                     |
| Grocery             | Spending on grocery products                                  |
| Frozen              | Spending on frozen products                                   |
| Detergents_Paper    | Spending on detergents and paper goods                        |
| Delicatessen        | Spending on deli items                                        |

Dataset Source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wholesale+customers)

---

## 🧪 Analysis Pipeline

1. **Preprocessing**:  
   - Filtered numerical spending columns for clustering  
   - Scaled features using StandardScaler

2. **Clustering**:  
   - Applied **K-Means** clustering (optimal k = 3 via Elbow & Silhouette)  
   - Cluster labels reattached to original data for profiling

3. **Profiling**:  
   - Analyzed each cluster’s average spending distribution and channel/region mix

4. **Visualization**:  
   - Used PCA plot and bar charts to illustrate segment traits

---

## Cluster Summary Table

| Cluster | # Clients | Total Spending | Fresh | Milk | Grocery | Frozen | Detergents Paper | Delicatessen |
|---------|-----------|----------------|-------|------|---------|--------|------------------|--------------|
| 0       | 45        | $76,376        | 14%   | 25%  | 38%     | 3%     | 17%              | 3%           |
| 1       | 393       | $27,649        | 44%   | 15%  | 20%     | 11%    | 6%               | 5%           |
| 2       | 2         | $158,280       | 22%   | 19%  | 11%     | 31%    | 0%               | 17%          |

---

## 🧭 Segment Insights & Recommendations

### **0. Daily Essentials Retailers**
- **Traits**: High spending on Milk and Grocery; low Fresh/Frozen.
- **Channel**: 98% Retail.
- **Interpretation**: Likely convenience or grocery stores focusing on daily consumer goods.
- **Suggestion**: Focus on dry-goods building and optimize delivery frequency to reduce operational costs.

### **1. Fresh Product Focused**
- **Traits**: High Fresh; low Detergents and Deli.
- **Channel**: 75% Horeca.
- **Interpretation**: Likely restaurants, cafés, or markets with frequent small orders.
- **Suggestion**: Ensure reliable, frequent, fresh deliveries tailored to their short inventory cycles.

### **2. High-Value Niche Clients**
- **Traits**: Extremely high overall spend; strong preference for Frozen and Delicatessen.
- **Channel**: Only 2 clients, and both of them are Horeca.
- **Interpretation**: Possibly boutique hotels or high-end establishments.
- **Suggestion**: Provide personalized service and premium cold-chain logistics to retain and grow strategic relationships.

---

## 🧠 Future Work

- Gather qualitative business-type information to validate cluster persona.
- Integrate monthly or quarterly sales data to analyze seasonal demand patterns.
- Study transaction-level data to uncover delivery frequency or minimum order size.


