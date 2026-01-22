# Customer Segmentation with Clustering

## Overview  
This project segments e-commerce customers into groups with similar purchasing behaviour using unsupervised machine learning. The goal is to support more targeted marketing and customer retention by identifying patterns in purchase frequency, recency, customer lifetime value (CLV), and customer demographics.The analysis starts from product-level order data and builds a customer-level dataset through feature engineering. K-means clustering is then used to create customer segments, and multiple evaluation methods are applied to select a suitable number of clusters.

Although this project is presented in a retail setting, the same methods can be applied to many other sectors, such as banking, technology, travel, and healthcare, where organisations also need to understand different customer or user groups.

## Preview  
<img src="/customer_clusters_tsne.png" alt="2D visualisation of customer clusters after dimensionality reduction with t-SNE (perplexity=10)" width="750">

## Dataset and features  
The original dataset contains **951,669 rows** of product-level order information and 20 columns. After cleaning and aggregating by customer ID, the final dataset contains **68,300 customers**, with one row per customer.

Customer-level features used for clustering:

- **Frequency**: how often a customer purchases  
- **Recency**: time since the last purchase  
- **Customer lifetime value (CLV)**: total revenue contributed by the customer  
- **Average unit cost**: average spend per purchase  
- **Customer age**

## Methods  
- Exploratory Data Analysis (EDA)  
- Feature engineering (customer-level aggregation)  
- Scaling 
- K-means clustering  
- Selecting the number of clusters:
  - Elbow method  
  - Silhouette score  
  - Hierarchical clustering (dendrogram)  
- Dimensionality reduction for visualisation:
  - PCA  
  - t-SNE  

## Results (cluster summary)  
A 4-cluster solution was selected based on a combination of the elbow method, silhouette scores, and hierarchical clustering.

The clusters can be summarised as:

- **Cluster 3** has a higher average unit cost than the other clusters. These customers seem to spend more per order.  
- **Cluster 2** has a higher recency than the other clusters. These seem to be the recent customers.  
- **Cluster 1** has a higher frequency and CLV than the other clusters. These seem to be the frequent buyers who have spent more over time.  
- **Cluster 0** scores low-average compared to the other clusters when it comes to average unit cost, recency, frequency and CLV and has an average age. Cluster 0 seem to be the rest of the customers that do not have a high average unit cost, frequency or recency.  

## Business implications  
These segments can be used to support decisions such as:

- identifying high-value customers for loyalty or retention strategies  
- distinguishing newer or less engaged customers who may benefit from targeted re-engagement  
- tailoring marketing approaches by customer age group  
- comparing customer groups on purchasing behaviour and value, rather than treating the customer base as one population

## Tools  
Python  
- pandas, numpy  
- scikit-learn  
- scipy  
- matplotlib, seaborn 

## Repository contents  
- `Customer_segmentation.ipynb`: main analysis notebook (full workflow and code)  
- `Heerink_Fiona_CAM_C101_W6_Mini-project.pdf`: report with results and discussion  

 
