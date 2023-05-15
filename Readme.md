# US Arrests Data Analysis

This project aims to perform a comprehensive analysis of the US Arrests dataset using PCA (Principal Component Analysis) and clustering techniques. The dataset contains statistics, in arrests per 100,000 residents, for assault, murder, and rape in each of the 50 US states in 1973, along with the percentage of the population living in urban areas.

## Dataset

The dataset used for this analysis is available in the file `UsArrests.csv`. It contains the following columns:

- `State`: Name of the US state
- `Murder`: Arrests per 100,000 residents for murder
- `Assault`: Arrests per 100,000 residents for assault
- `UrbanPop`: Percentage of the population living in urban areas
- `Rape`: Arrests per 100,000 residents for rape

## Pre-processing Steps

Before conducting the analysis, some pre-processing steps were performed on the dataset:

- **Data Loading**: The dataset was loaded from the CSV file using the pandas library.

- **Data Cleaning**: The dataset was checked for missing values, and it was found that there are no missing values in the dataset.

- **Data Scaling**: As PCA is sensitive to the scale of the variables, the data was standardized using the StandardScaler from the scikit-learn library to ensure all variables have the same scale.

## Principal Component Analysis (PCA)

PCA was applied to identify the underlying patterns and relationships in the dataset and to reduce the dimensionality of the data. The following steps were performed:

- **Explained Variance Ratio**: The explained variance ratio was analyzed to determine the number of principal components to retain.

- **PCA Transformation**: PCA was performed using the selected number of principal components. The results were stored in a DataFrame.

- **Loadings Analysis**: The loadings of each principal component were analyzed to identify the variables contributing the most to each component.

## Clustering Techniques

Two clustering techniques were applied to identify common patterns within the data:

- **K-means Clustering**: K-means clustering was performed to group the states based on their similarity in the dataset. The cluster labels were added to the PCA results DataFrame.

- **Hierarchical Clustering**: Hierarchical clustering was also applied to group the states based on their similarity. The cluster labels were added to the PCA results DataFrame.

## Clustering Results

The average values of the variables within each cluster were calculated and analyzed for both K-means and hierarchical clustering. The findings from the clustering results were as follows:

### K-means Clustering Results:

- Cluster 0: This cluster has lower average values for Murder, Assault, and Rape compared to Cluster 1. It also has a slightly lower average UrbanPop value. States in this cluster may represent regions with relatively lower crime rates and a lower percentage of the population living in urban areas.

- Cluster 1: This cluster has higher average values for Murder, Assault, and Rape compared to Cluster 0. It also has a slightly higher average UrbanPop value. States in this cluster may represent regions with relatively higher crime rates and a higher percentage of the population living in urban areas.

### Hierarchical Clustering Results:

- Cluster 0: This cluster has similar characteristics to Cluster 0 in the K-means results. It has lower average values for Murder, Assault, and Rape compared to Cluster 1, indicating regions with relatively lower crime rates and a lower percentage of the population living in urban areas.

**These findings suggest that the clustering algorithms have identified two main groups of states: one with relatively lower crime rates and a lower urban population.**
