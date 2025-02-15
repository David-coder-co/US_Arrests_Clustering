# US_Arrests_Clustering

This project analyzes the US Arrests dataset (1973) using Principal Component Analysis (PCA) and two clustering techniques to identify patterns in crime rates across US states. The goal is to extract meaningful insights, visualise relationships between variables, and group states based on crime trends.

### Dataset  

The dataset used in this project is the US Arrests dataset (1973) from the Kaggle challenge, stored in the file UsArrests.csv. It contains arrest rates per 100,000 residents for assault, murder, and rape, along with the percentage of the population living in urban areas. The data covers all 50 US states in the year 1973.

### Objectives

- Perform Principal Component Analysis (PCA) to reduce dimensionality and interpret data structure.
- Preprocess the dataset, including scaling and handling missing values (if any).
- Apply two clustering techniques to group states based on crime patterns.
- Interpret clusters and analyse common characteristics within each group.

## Methodology 

### 1. Data Preprocessing  
Before analysis, the dataset was carefully examined for missing values and inconsistencies. Since PCA and clustering techniques are sensitive to scale, feature scaling was applied by standardising the data using z-score normalisation. This ensures that all variables contribute equally to the analysis rather than being dominated by those with larger numerical ranges.  

### 2. Principal Component Analysis (PCA)  
PCA was used to reduce dimensionality while retaining the most important variance in the dataset. The principal components were calculated, and their explained variance ratio was analysed to determine how much information each component retains. The PCA results were visualised using scatter plots and biplots, helping to identify which features contribute most to crime patterns across states.  

###  3. Clustering Techniques 
Two clustering methods, K-Means clustering and Hierarchical clustering, were applied to group states based on their crime statistics. To determine the optimal number of clusters, the Elbow method was used for K-Means, analysing the within-cluster sum of squares. For Hierarchical clustering, a dendrogram was created to visualize relationships between states and identify natural groupings. The results were interpreted to uncover similarities in crime trends within each cluster.

## Refined Results & Insights

### PCA Findings:

- The first two principal components captured the majority of the variance, simplifying the dataset while preserving key patterns.
- Murder, Assault, and Rape rates strongly influenced the first principal component (PC1), indicating that states with high values for these crimes are grouped together.
- UrbanPop (percentage of urban population) had an opposite loading compared to crime variables, meaning states with higher urban populations generally had lower crime rates, while rural-dominated states experienced higher crime rates.

### Clustering Results:

- States were grouped into clusters based on crime rate similarities.
- The clustering analysis confirmed the PCA findings, showing that states with lower UrbanPop had higher crime rates, whereas highly urbanized states had lower crime rates.
This challenges the common perception that urbanization leads to higher crime and suggests other socio-economic factors might influence crime trends in rural areas.

## How to Run the Project
1. Clone the repository to your local environment.
2. Install dependencies: pip install -r requirements.txt
3. Run the analysis script: Capstone_task.ipynb
4. View visualizations in the output folder.

## Technologies Used
- Python (NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn)
- Visual Studio (for data analysis and visualization)

## Conclusion
- PCA helped reduce dimensionality and highlight key features affecting crime.
- Clustering techniques grouped states with similar crime trends.
- These insights can be useful for policy-making and crime prevention strategies


