# Cluster-Analysis-on-Wine-Dataset

## Problem Statement

The objective of this project is to implement clustering algorithms to analyze numerical data related to wine. The objective is to partition the dataset into clusters and visualize the results through plots, using the scikit-learn library. The clustering models' performance is assessed using the Silhouette Score, a metric indicating the quality of clustering results.

However, a critical issue arises due to the lack of standardization in the wine dataset. The Proline feature values exhibit a wide range, with some values significantly smaller than others. This non-uniform scaling poses a challenge, especially for algorithms sensitive to input feature scales, such as K-Means, Support Vector Machines, and Principal Component Analysis. To address this, the project proposes Z-score normalization as a preprocessing step, aiming to standardize the data by transforming features to have a mean of 0 and a standard deviation of 1.

The problem statement is to enhance the current clustering models by implementing Z-score normalization on the wine dataset. This involves integrating code for data standardization using Z-score normalization and evaluating the impact on clustering performance. The goal is to ensure that clustering algorithms, particularly KMeans, provide more accurate and meaningful insights into the underlying structure of the wine data after standardization. The success of the project will be measured by improvements in the Silhouette Score for the clustering models on the training, validation, and testing sets.

## About the Dataset

This dataset is adapted from the Wine Data Set from https://archive.ics.uci.edu/ml/datasets/wine by removing the information about the types of wine for unsupervised learning.

The following descriptions are adapted from the UCI webpage:

These data are the results of a chemical analysis of wines grown in the same region in Italy but derived from three different cultivars. The analysis determined the quantities of 13 constituents found in each of the three types of wines.

The attributes are:

1. Alcohol
2. Malic acid
3. Ash
4. Alcalinity of ash
5. Magnesium
6. Total phenols
7. Flavanoids
8. Nonflavanoid phenols
9. Proanthocyanins
10. Color intensity
11. Hue
12. OD280/OD315 of diluted wines
13. Proline

## Key Findings from the Project

1. **Clustering Model Comparison:**
   - **KMeans:**
     - Training Set: 0.28
     - Validation Set: 0.27
     - Testing Set: 0.29
   - **Agglomerative Clustering:**
     - Training Set: 0.28
     - Validation Set: 0.27
     - Testing Set: 0.29
   - **PCA with KMeans:**
     - Training Set: 0.56
     - Validation Set: 0.46
     - Testing Set: 0.20

2. **Silhouette Score Interpretation:**
   - A Silhouette Score close to 1 indicates well-separated and distinct clusters.
   - Higher scores suggest better-defined cluster structures.

3. **KMeans and Agglomerative Clustering:**
   - Similar performance in terms of Silhouette Score across training, validation, and testing sets.
   - Scores indicate moderate clustering quality.

4. **PCA with KMeans:**
   - Achieved notably higher Silhouette Score on the training set.
   - Lower scores on the validation and testing sets suggest potential overfitting or reduced generalizability.

5. **General Observation:**
   - Clustering quality varies across models and datasets.
   - PCA with KMeans shows strong performance on the training set but struggles on new data.

6. **Recommendation:**
   - Further investigation needed to enhance the generalization capability of PCA with KMeans.
   - Exploration of additional clustering algorithms or feature engineering could improve overall model performance.


## Build From Sources and run the Selenium scraper 


1. Clone the repo

```bash
git clone https://github.com/samiulabir201/Cluster-Analysis-on-Wine-Dataset
```

2. Initialize and activate the virtual environment

```bash
pip install virtualenv
virtualenv venv
.\venv\Scripts\activate
```

3. You will get a file named `wine-clustering.csv` containing all the required fields. Alternatively, check the data here: [https://github.com/samiulabir201/Demographics-of-Best-CS-Scientist/blob/main/selenium_scraper/best_cs_scientist_details.csv](https://github.com/samiulabir201/Cluster-Analysis-on-Wine-Dataset/blob/main/wine-clustering.csv)

## Analytics   

**Kmeans Clustering on Training data**
<img width="495" alt="Screen Shot 2024-02-05 at 9 14 49 PM" src="https://github.com/samiulabir201/Cluster-Analysis-on-Wine-Dataset/assets/78860039/19adc403-4b1c-4523-8ff2-cc868849f086">

**Hierarchical clustering**
<img width="579" alt="Screen Shot 2024-02-05 at 9 13 20 PM" src="https://github.com/samiulabir201/Cluster-Analysis-on-Wine-Dataset/assets/78860039/5867e6a7-753f-485f-991e-4faf5f538b0d">

Agglomerative Clustering on Train Data:

<img width="450" alt="Screen Shot 2024-02-05 at 9 12 09 PM" src="https://github.com/samiulabir201/Cluster-Analysis-on-Wine-Dataset/assets/78860039/d4933528-4ffd-429b-b561-9469f4d92df5">

Agglomerative Clustering on Test Data:
<img width="460" alt="Screen Shot 2024-02-05 at 9 11 44 PM" src="https://github.com/samiulabir201/Cluster-Analysis-on-Wine-Dataset/assets/78860039/9dc55fd8-2a40-4778-be98-5cc17952f3f7">

Agglomerative Clustering on Validation Data:
<img width="449" alt="Screen Shot 2024-02-05 at 9 11 25 PM" src="https://github.com/samiulabir201/Cluster-Analysis-on-Wine-Dataset/assets/78860039/3f5b145d-b57c-4723-844c-c84b62b89817">

**Principal Component Analysis with Kmeans**
Data after PCA
<img width="429" alt="Screen Shot 2024-02-05 at 9 10 31 PM" src="https://github.com/samiulabir201/Cluster-Analysis-on-Wine-Dataset/assets/78860039/0dea21b4-f29f-4ecc-8c27-b4c0a01f3799">

Silhouette train set Score: 0.5603726386000918Í
<img width="504" alt="Screen Shot 2024-02-05 at 9 09 20 PM" src="https://github.com/samiulabir201/Cluster-Analysis-on-Wine-Dataset/assets/78860039/52f90994-debc-495d-b03f-9d08b80be12c">

Silhouette Score on Validation Set: 0.45732291140211623
<img width="504" alt="Screen Shot 2024-02-05 at 9 07 06 PM" src="https://github.com/samiulabir201/Cluster-Analysis-on-Wine-Dataset/assets/78860039/35b53b4f-3be7-4d12-b787-37cbd47262e2">

Silhouette Score on Test Set: 0.20189294490586665
<img width="502" alt="Screen Shot 2024-02-05 at 9 06 29 PM" src="https://github.com/samiulabir201/Cluster-Analysis-on-Wine-Dataset/assets/78860039/a9d1f307-9622-4906-af2b-980d384a95bf">

