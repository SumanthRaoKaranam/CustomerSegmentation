collab link of Customer Segmentation Project: 
https://colab.research.google.com/drive/13Jyh3IQDp4_MwlFz4Yb-yPRAe5akUuL8?usp=sharing

# Customer Segmentation

This project performs **customer segmentation** using **unsupervised machine learning techniques** such as KMeans and hierarchical clustering. The goal is to group customers based on features like age, annual income, and spending score to identify patterns and behaviors for marketing and business strategies.

---

## Dataset

- The dataset used is `Mall_Customers.csv`.  
- Key columns include:
  - `CustomerID` (removed during preprocessing)
  - `Gender`
  - `Age`
  - `Annual Income (k$)`
  - `Spending Score (1-100)`

---

## Preprocessing

- Dropped irrelevant columns (e.g., `CustomerID`).  
- Checked for missing values and ensured data completeness.  
- Normalized numerical features (`Age`, `Annual Income (k$)`, `Spending Score (1-100)`) using `StandardScaler`.

---

## Exploratory Data Analysis

- Visualized relationships between features using pairplots.  
- Observed distributions and correlations to understand customer behavior.

---

## Clustering Techniques

1. **KMeans Clustering**  
   - Used the **Elbow Method** to determine the optimal number of clusters.  
   - Fit KMeans with the optimal cluster number (e.g., 5) and assigned cluster labels.  
   - Evaluated clustering using **silhouette score**.  

2. **Hierarchical Clustering**  
   - Performed clustering using Ward linkage.  
   - Visualized clusters with a **dendrogram**.  

---

## Cluster Analysis

- Analyzed the clusters by computing the mean values of numeric features for each cluster.  
- Insights can be derived to understand customer segments for targeted marketing.  
- Segmented data saved as `customer_segments.csv`.

---

## Requirements

- Python >= 3.8  
- Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, scipy  
- Install libraries using:  
  ```bash
  pip install pandas numpy matplotlib seaborn scikit-learn scipy

Usage
Load the dataset:
df = pd.read_csv('Mall_Customers.csv')
Preprocess and normalize the data.
Apply KMeans and hierarchical clustering.
Visualize clusters using plots and analyze segments.
Save clustered data for further analysis:
df.to_csv('customer_segments.csv', index=False)

Author: Karanam Sumanth, B.E. in Information Technology, 2025
