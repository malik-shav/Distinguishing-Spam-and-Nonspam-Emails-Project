Distinguishing Spam and Nonspam Emails Using Unsupervised Learning Algorithms

Summary:
- The objective of this task is to analyze the Spambase dataset and distinguish between spam and non-spam emails using unsupervised learning techniques. 

Data:
- The dataset contains frequency of certain words used in an email, percentage of a certain character that is included in an email, and average, sum and lenght of uninterrupted capital letters used. The data does contain a target variable, which will be ommited from the data due to the use of unsupervised learning. However, target variable will be used to calculate ARI score and will be compared to Silhoutte score. The data was collected using reported spam emails by individuals and non-spam emails came from reported personal emails. The data can be accessed from kaggle by accessing the link: https://www.kaggle.com/somesh24/spambase

Methods:
- The analysis begins by understanding the variables, their data types, and if any missing values are present. Data is cleaned, processed, and analyzed using descriptive statistics and visualizations. Target variable is deleted to treat this task as an unsupervised learning. Variables are scaled and features are selected using PCA based on 95% data conservation. Scaled data will be applied to KMeans clustering algorithm to find optimum number of clusters using the elbow method and Silhouette Coefficient. Two reduced data's, from PCA and UMAP, will be applied to both KMeans and Hierarchical clustering algorithms. Total of 5 models is present. Models will be evaluated based on how well clusters are seperated visually, their Silhouette Coefficient, and ARI score.

Model Performance and Insights
- All 5 models were set to distinguish two clusters, spam and non-spam emails. Each of those models were able to identify a number of spam emails but two were better and comparabable in performance. Model 3 and 5 were able to identify more than 400 spam emails. Between those two, model 3 is superior based on higher ARI score of 0.0099, even though its silhouette score of 0.50 is much lower than silhouette score's of model 1, 2, and 3. However, performance of model 3 is not sufficient for deployment.

- The total spam emails found from 4600 samples accounted for 39.4%. By analyzing the frequency of the words used, it is very clear that words as "you, your, free, and our" are a major contributer to an email being spam or not.

Recommendation:
- Models performance is not enough for deployment. Model needs to be revisited in the future and worked on finding the the best hyperparameters with addition of more data. Other types of clustering algorithms as Guassian Mixture model and DBSCAN, can be attempted. 
