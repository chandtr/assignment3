**Business Objective :**
The business goal is to find a model that can explain success of a contact. Such model can increase campaign efficiency by identifying the main characteristics that affect success, helping in a better management of the available resources (e.g. human effort, phone calls, time) and selection of a high quality and affordable set of potential buying customers.

Models Explored :
The performance of the classifiers we encountered in this section, namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines.
    
Data Used :
The data is from a Portugese banking institution and is a collection of the results of multiple marketing campaigns.
Reference data is available in the data folder data/bank-additional/bank-additional-full.csv

Approach :
Created the base model with basic logisticregression with default parameters. 
We got 63 features after the transformations we trained the model with top 19 highest correlated features.
Training the model with top 19 highest correlated features and just 5000 rows taking 25 minutes to train. So tried to split the dataset and train them with the small chunk of 5000 records. There are 8 chunks has been created 

Observations:
For comparing the logisticRegression with DecisionTree, KNN and SVC, we have 41000 records for this training, 
we have used couple of hyperparameters, C value for LogisticRegression, various max depth value for DecisionTrees, various n values for KNearestNeighbours, SVC with various C and Kernel values.
Time Taken :   Training time for decisiontree was better, may be because i have used the max depth of 6, all the SVC took so long to train compare to LogisticRegression and KNN.
Accuracy Score : Training Accuracy and Testing Accuracy are mostly very similar. DecisionTree and KNN are performing better for those top 19 features and hyper parameters

Following Features are highly impacting the success of the cantact and the model accuracy score is 92% average between those 4 different models,
  Last Contact duration, 
  Previous Contanct successful/failure outcome, 
  number of contacts before this, 
  Cellular Communication, 
  Contact during March, April, October, September, December, 
  no default in credit, 
  job might be admin, retired or student, 
  marital status is single, 
  Grauduated for university degree, 
  Increase in the Consumer Price Index and Age
