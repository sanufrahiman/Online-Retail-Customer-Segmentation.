
# Online Retail Customer Segmentation.

A brief description of what this project does and who it's for


## Problem Description
To identify major customer segments on a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

## Data Description
Attribute Information:

InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation.
StockCode: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.
Description: Product (item) name. Nominal.
Quantity: The quantities of each product (item) per transaction. Numeric.
InvoiceDate: Invice Date and time. Numeric, the day and time when each transaction was generated.
UnitPrice: Unit price. Numeric, Product price per unit in sterling.
CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.
Country: Country name. Nominal, the name of the country where each customer resides.
## Exploratory data analysis

From the graph we can see that:\
Most of the customers are from United Kingdom ,Germany ,France ,EIRE and Spain.\
least number of customers from Lithuania,Brazil, Czech Republic ,Bahrain and Saudi Arabia.
## Feature engineering- Conclusions
Most of the customers have purches the items in Thursday ,Wednesday and Tuesday.\
Most numbers of customers have purches the gifts in the month of November ,October and December September.\
Less numbers of customers have purches the gifts in the month of April ,january and February.\
From this graph we can see that in AfterNoon Time most of the customers have purches the item.\
Most of the customers have purches the items in Aftrnoon ,moderate numbers of customers have purches the items in Morning and least numbers of customers have purches the items in Evening.\
## Further Conclusions

Created the RFM model (Recency, Frequency,Monetary value).\
Performed K-Means Clustering\
Applied Silhouette Score Method on Recency and Monetary.\
Applied silhouette Score Method on Frequency and Monetary.\
Applied Elbow Method on Frequency and Monetary.\
Applied DBSCAN to Method on Frquency and Monetary.\
Customers are well separate when we cluster them by Frequency and Monetary.\
Applied Silhouette Method on Recency ,Frequency and Monetary.\
Applied Elbow Method on Recency ,Frequency and Monetary.\
Used Dendogram to find the optimal number of clusters.\
By applying different clustering algorithem to our dataset, obtained the optimal number of cluster equal to 2.\
Applied DBSCAN to Recency ,Frequency and Monetary and saw that Customers are well separate when we cluster them by Recency ,Frequency and Monetary and optimal number of cluster is equal to 3.\

The following summary is obtained:\
+--------+--------------------------------+------+---------------------------+
| SL No. |           Model_Name           | Data | Optimal_Number_of_cluster |
+--------+--------------------------------+------+---------------------------+
|   1    | K-Means with silhouette_score  |  RM  |             2             |
|   2    |  K-Means with Elbow methos     |  RM  |             2             |
|   3    |            DBSCAN              |  RM  |             2             |
|   4    | K-Means with silhouette_score  |  FM  |             2             |
|   5    |  K-Means with Elbow methos     |  FM  |             2             |
|   6    |            DBSCAN              |  FM  |             2             |
|   7    | K-Means with silhouette_score  | RFM  |             2             |
|   8    |  K-Means with Elbow methos     | RFM  |             2             |
|   9    |   Hierarchical clustering      | RFM  |             2             |
|   10   |            DBSCAN              | RFM  |             3             |
+--------+--------------------------------+------+---------------------------+