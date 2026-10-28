# Project Title: The Digital Lifestyle Analysis of 500 Youths

## 📊 Project Overview
This project explores the complexities of digital behavior among 500 youths, utilizing a multi-language workflow (Python and R) to uncover latent patterns in high-dimensional data. The study focuses on the tension between predictive simplicity and structural heterogeneity.

### Supervised Learning
•	**Random Forest Regression/Classification (Python)**: Implemented to test the hypothesis of predictability within the sample. The model was used to assess whether the variance in digital lifestyles is governed by a limited set of key features or exhibits a high degree of multifaceted heterogeneity.

### Unsupervised Learning
•	**FAMD & K-Means Clustering (Python)**: To accommodate a mixed-type feature space (numerical, ordinal, and nominal), Factor Analysis of Mixed Data (FAMD) was utilized for dimensionality reduction, providing a basis for K-Means clustering to optimize behavioral segmentation via silhouette analysis.
•	**PCA, MCA, and Hierarchical Clustering (R)**: To validate the findings from the FAMD approach, a bifurcated analysis was conducted using PCA for continuous variables and MCA for categorical variables. This was synthesized through Hierarchical Clustering to explore the dendrogram structure and validate the complex, nuanced distribution of the participants.

## Dataset Description
The dataset contains 500 records following the variables: 
•	Demographics: Age, Gender
•	Metrics used: Daily Screen Time Hours, Preferred Device, Social Media Usage Hours, Gaming Activity, Tech Savviness, Streaming Subscriptions, and Privacy Awareness Level 

## Analysis Workflow
This project was executed through three distinct analytical pipelines. Each workflow consists of a technical implementation (code) and a comprehensive synthesis of the results (report).

1. **Predictive Modeling via Random Forest (Python)**
Objective: To determine the degree of predictability within the digital behavior sample and identify whether a small set of dominant features could classify the target variable. 
•	Workflow: Data Preprocessing → Feature Engineering → Random Forest Ensemble Training → Model Evaluation
•	Technical Outcome: The model failed to yield a statistically significant prediction result. This suggests that the device choice is not driven by a few linear or non-linear predictors, but rather by a complex, multifaceted interplay of variables, confirming the high heterogeneity of the sample. 
•	Deliverables: [View Technical Code] (./technical_code/Random Forest_Python.ipynb) | [Read Full Analysis Report] (./full_reports/Random Forest_Python.pdf)

2. **Mixed-Data Segmentation: FAMD & K-Means (Python)**
Objective: To reduce the dimensionality of a mixed-type feature space (numerical, ordinal, and nominal) and identify cohesive behavioral clusters. 
•	Workflow:
-	Dimensionality Reduction: FAMD was iteratively tested with 5, 10, and 16 components. 
-	Variance Analysis: Scree plots indicated a linear decrease in eigenvalues (ranging from 4.34 to 4.85 for the first 5 components), suggesting that variance is distributed across several dimensions rather than dominated by a few. 
-	Clustering Optimization: K-means clustering was applied to the FAMD projections. Silhouette analysis was used to optimize the cluster count, resulting in the selection of 2 components and 3 clusters (Silhouette Score: 0.36).

•	Deliverables: [View Technical Code] (./technical_code/FA KMeans_Python.ipynb) | [Read Full Analysis Report] (./full_reports/FA KMeans_Python.pdf)

3. **Structural Validation: PCA-MCA & Hierarchical Clustering (R)**
Objective: To cross-validate the clustering results using a bifurcated approach to dimensionality reduction and a nested grouping strategy. 
•	Workflow:
-	Bifurcated Reduction: PCA was applied to the numerical subset, and MCA was applied to the categorical subset.
-	Agglomerative Clustering: HC was performed on the combined scaled scores using Euclidean distance and Ward’s minimum variance method.
-	Selection Logic: A dendrogram was used to visualize the nested structure. Despite modest mean Silhouette values (0.13-0.15), a 2-cluster solution was selected as the most stable representation of the underlying structural divide. 
•	Deliverables: [View Technical Code] (./technical_code/PCA_MCA_R.Rmd) | [Read Full Analysis Report] (./full_reports/PCA MCA HC_R.pdf)


## 📈 Synthesis of Results
Across three different analytical lenses—predictive (Random Forest) and descriptive (FAMD/K-Means and PCA-MCA/Hierarchical)—a consistent theme emerged: **the high dimensionality and heterogeneity of digital lifestyles**.
The absence of a clear "elbow" in the scree plots and the modest silhouette scores across both Python and R clustering methods indicate that the participants do not fall into neatly separated categories. Instead, they exist on a spectrum of digital behaviors. The fact that both clustering methods converged on a small number of groups (2 or 3) despite the data's complexity suggests a broad, primary divide in how these 500 participants engage with digital technology, even if the boundaries between those groups are fluid.

## 🚀 Getting Started
## Prerequisites
To execute the Python analysis, make sure you have Python 3.x installed along with the required libraries:
•	pandas
•	matplotlib
•	numpy
•	seaborn
•	sklearn
•	altair
•	factor_analyzer
•	prince

To run the R analysis, make sure you have R 4.1.0 or later installed along with the required libraries:
•	FactoMineR
•	factoextra
•	tidyverse
•	cluster
•	ggrepel
•	reshape2

## Execution Steps
1.	Download the Files: Download or clone this repository directly from GitHub to your local machine.
2.	Install Dependencies: Open your terminal or command prompt and install the required Python libraries listed above.
3.	Run Analyses: Execute project_1_py.ipynb within your environment to view the statistical summary and generate the visualization plots.

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.