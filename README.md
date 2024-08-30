Crypto Portfolio Clustering Project
![image](https://github.com/Jvvne/Crypto_Portfolio_Clustering/assets/148028363/c7c64514-e06a-427b-9052-2bcd3f829064)

Project Goal:
# Project Title: Cryptocurrency Clustering Using K-Means

## Project Objective:
The primary objective of this project is to categorize cryptocurrencies into distinct clusters based on their price fluctuations over different timeframes (24 hours and 7 days) by leveraging the K-Means Clustering algorithm, a popular unsupervised machine learning technique.

## Data Overview:
The dataset used for this project is a CSV file titled `crypto_market_data.csv`, which includes information on the price changes of various cryptocurrencies.

## Project Workflow:

### 1. Data Import and Initial Analysis:
The first task is to load the CSV data into a pandas DataFrame. Following this, we conduct exploratory data analysis (EDA) by summarizing the statistics and employing visualizations with `HvPlot` to gain insights into the data's structure and behavior.

### 2. Data Preprocessing:
To prepare the data for clustering, we standardize the features using scikit-learn's `StandardScaler`. This step is essential to ensure that all features are on a comparable scale before applying the K-Means algorithm.

### 3. Determining the Optimal Number of Clusters:
To identify the best number of clusters (`k`), we utilize the "elbow method." This technique involves plotting the inertia (a metric that indicates how compact the clusters are) against various values of `k`. The optimal number of clusters is typically selected where the plot exhibits a noticeable "elbow," indicating a point where increasing `k` no longer significantly reduces inertia.
![image](https://github.com/user-attachments/assets/364f32e0-62dd-44f5-880c-94a598ed2e1d)

#### Elbow Chart:
- The elbow chart helps visualize the change in inertia across different `k` values, guiding us to select the most appropriate `k`.

### 4. Clustering Cryptocurrencies Using K-Means:
Once the optimal `k` value is determined, we apply the K-Means algorithm to cluster the cryptocurrencies based on their price changes. The resulting clusters are then visualized in a scatter plot, with each data point representing a cryptocurrency, color-coded according to its assigned cluster.
![image](https://github.com/user-attachments/assets/45e821f3-348f-4430-b25d-158baf0ed8f4)

#### Cluster Visualization:
- The scatter plot showcases the distribution of cryptocurrencies across clusters, making it easier to interpret the clustering results.

### 5. Enhancing Clustering with Principal Component Analysis (PCA):
After initial clustering, we employ Principal Component Analysis (PCA) to refine the clusters. PCA reduces the dataset's dimensionality by focusing on the features with the highest variance, which are most relevant for clustering. This step helps to remove less significant features, enhancing the clarity and effectiveness of the clustering.

### 6. Applying K-Means to PCA-Transformed Data:
With the dataset transformed by PCA, we rerun the K-Means clustering algorithm using the previously determined optimal `k` value. This allows us to observe how the clustering results differ when only the most significant features are considered.

### 7. Comparing Results - With and Without PCA:
To assess the impact of PCA on clustering, we generate visual comparisons between the results obtained from the original data and the PCA-transformed data:
![image](https://github.com/user-attachments/assets/5dd3897c-a898-4ed3-9797-b81f104aa675)

- **Elbow Curves Comparison:** Visualizing the elbow curves for both the original and PCA-transformed data to see how PCA affects the determination of the optimal `k`.
- **Cluster Scatter Plots Comparison:** Creating scatter plots for the clusters derived from the original data and the PCA-transformed data to observe differences in cluster distribution and clarity.

#### Impact Analysis:
- By analyzing the visual comparisons, it becomes evident that clustering with fewer features (after PCA) often leads to more distinct and interpretable clusters, as the reduction in features helps highlight the most critical variations in the data.

This approach ensures that the clustering process is both effective and insightful, providing a deeper understanding of the factors driving cryptocurrency price changes.


Impact of Using Fewer Features:
By visually analyzing the comparisons, you will observed that using fewer features (principal components) result in clusters more spread out and easier to interpret due to the reduced number of columns used.


1.Clone the repository to your local machine.

2.Ensure you have the required libraries installed.

3.Open crypto_investments.ipynb in Jupyter Notebook or Jupyter Lab.

4.Run the cells to see the analysis and visualizations.
