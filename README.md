# Mind the Map: Exploring Task Similarities and Differences in the IBC Dataset

CSAI Project: Team HotCocoa
<br>
Anusha Nath Roy 2020101124
<br>
Freyam Mehta 2020101114
<br>
Srijan Chakraborty 2020115001

## Abstract

The primary objective of this project is to conduct a comprehensive analysis of the IBC dataset, a valuable resource for researchers in the neuroscience domain to exploit. Through the analysis, the aim is to uncover hidden patterns and insights within the data that may contribute to our understanding of the complex workings of the human brain. The focus of the study is centered around a cross-comparison of various tasks recorded in IBC release 2, with the purpose of identifying similarities and differences across tasks.

To achieve this, we used the z-maps of individuals as a powerful tool to uncover these patterns. By conducting this study, we hope to gain valuable insights into the hierarchical organization of brain areas and their functioning. The potential impact of this study extends beyond the academic community and could contribute to the development of improved cognitive and behavioral therapies for individuals affected by neurological disorders.

## Installation

Run `comparison.ipynb`. Adjust the z_map directory and mask directory before running.

## Methodology and Experiments

Our methodology involves using various data analysis techniques to gain insights into the organization of cognitive processes in the brain using the IBC dataset. Using the z-maps which have been publicly uploaded to the neurovault website, IBC Dataset Extension, we have used several different methods for data analysis and visualisation. These techniques include pattern analysis, hierarchical cluster analysis, dimensionality reduction, encoding and decoding, and statistical modeling. By applying these techniques, we aim to uncover patterns and relationships within the data that can provide valuable insights into the functioning of the human brain. We have run these visualisation and analysis techniques on 500 z-maps, collected for one user, over different sessions (00, 04 and 07) and for several different tasks. We have 100 labels for our z-maps.

1. Data Acquisition and Preprocessing: The first step in our methodology involves acquiring and preprocessing the IBC dataset, which is available on OpenNeuro. We also download z-maps available on NeuroVault and perform preliminary preprocessing/labelling.

2. Pattern Analysis: In this step, we generate mean z-maps for each task and plot the Representational Similarity Analysis (RSA). We also apply Dictionary Learning and generate RSA using the sparse codes. Furthermore, we visualize the spatial distribution of the dictionary components across the brain.

3. Hierarchical Cluster Analysis: We used dendrograms to visualize the clustering results and to identify groups of tasks that show similar neural patterns. We applied hierarchical clustering to both the RSA maps created from the z-map voxel activation data and the model weights used during decoding. This helped us to explore the clustering results using different perspectives.

4. Dimensionality Reduction: We perform dimensionality reduction to 2D and 3D using both Principal Component Analysis (PCA) and Multidimensional Scaling (MDS). This is carried out using the mean z-maps for each label. We then analyze it by running k-means cluster with different k values to check which tasks group together in this reduced dimensional space.

5. Decoding and Prediction: To gain a better understanding of the neural activity patterns associated with each task, decoding models were created using the mean z-maps for each task. These models were trained to predict the task label based on the voxel activation patterns. To obtain more detailed information about the neural representation of each task, separate decoding models were also trained for each individual task. The coefficients of the models were recorded for each label, which provide a measure of the importance of each voxel for predicting the task label.

6. Statistical Modeling: We used regression analysis to predict the tasks based on the brain activity patterns. Specifically, we created models to predict each task individually and recorded the coefficients of the model for each label. We then used these coefficients to create an RSA matrix, which allowed us to explore the similarity or dissimilarity between the tasks based on their coefficients. Finally, we applied hierarchical clustering to the RSA matrix to visualize the clustering results and to identify groups of tasks that show similar patterns of coefficients. This approach helped us to identify the most important brain regions and the patterns of brain activity that are most informative in predicting the cognitive tasks being performed.
