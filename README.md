# Customer-Segmentation-with-RFM-Analysis-using-KMeans


Project Objective  

1. Segment customers based on their purchasing behavior.  
2. Apply “RFM analysis” (Recency, Frequency, Monetary).  
3. Use “KMeans clustering” to identify meaningful customer groups.  
4. Provide “business insights” for targeted marketing and retention.
   
Dataset  

Columns Used: 
   - `InvoiceDate` → Used to calculate “Recency”.  
   - `Invoice` → Used to calculate “Frequency”.  
   - `Quantity * Price` → Used to calculate “Monetary value”.  
Granularity: Each row = a product purchased in a transaction.  
Preprocessing: Removed unused columns (e.g., `StockCode`), handled missing values.  

 Project Workflow 
 
1. Data Preparation  
    •	Loaded dataset and cleaned missing/irrelevant columns.  
    •	Created a reference date (`2012-01-01`) to compute “Recency”.  

2. RFM Analysis  
    •	“Recency”: Days since last purchase.  
    •	“Frequency”: Count of unique invoices per customer.  
    •	“Monetary”: Total spend (`Quantity × Price`).  
    •	Combined into an “RFM table” per customer.  

3. Feature Scaling
    •	Standardized RFM values using “StandardScaler”.  

4. Clustering using KMeans 
    •	Used “Elbow Method” to find optimal number of clusters.  
    •	Trained “KMeans with 3 clusters”.  
    •	Assigned cluster labels to each customer.  

5. Customer Grouping
    •	Cluster 3 → Whales (High Value Customers).  
    •	Cluster 2 → Lapsed Customers.  
    •	Cluster 1 → Average Customers.  

6. Visualization 
    •	Bar plot showing counts of customers per segment.  
    •	Summary table with average Recency, Frequency, Monetary per cluster.  

 Key Insights Gained  
 
        •	“High-value customers ("Whales")” purchase frequently, spend more, and are recent buyers.  
        •	“Lapsed customers” show high recency (haven’t purchased in a while) and low frequency.  
        •	“Average customers” are in-between — moderate spenders and activity.  
        •	The segmentation helps in “tailoring marketing strategies” per group. 

 Business Actions Based on Insights  
 
 Whales (High Value Customers)  
      •	Provide loyalty programs, VIP benefits, and exclusive offers.  
      •	Focus on retention with personalized services.  

Average Customers  
      •	Encourage more frequent purchases with promotions.  
      •	Upsell/cross-sell to increase their monetary value.  
      
Lapsed Customers
    •	Win-back campaigns with targeted discounts.  
    •	Re-engage via email reminders and special offers.  

