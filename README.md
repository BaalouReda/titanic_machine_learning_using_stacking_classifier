# titanic_machine_learning_using_stacking_classifier
its a approch to solve the titanic problem on kaggle using stacking method
the link to the dataset : https://www.kaggle.com/code/aminemrhari/titanic-problem/data?select=train.csv
in this case study the goal was to determinate if the passanger had survived or not , so it's a classification problem .
the solution was in 3 steps :
1 a mini feature analayses where i studied each and every feature and its impact on the goal
2 a mini data cleaning :
-eleminating nan  or  filling  them with mean (i tried with most frequent but the results with the mean where better)  
-changing from categorical data to numercal data 
-elminating outliers and features who showed no impact on the goal n the features analyses phase.
3 devieding data into train test split ( i would liked to use variant decompositation but the data set is small and when i tried it the accuracy droped down )
4 application of 3 algorithms on the data set :
-knn: https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html
-svm: https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html
-Decision Tree:https://scikit-learn.org/stable/modules/tree.html
i tested the accuracy of each one of the models with 3 metrecs 
- accuracy_score 
-  f1_score
-  matthews_corrcoef
and sum the avg accuracy 
then i stacked the 3 models and usd the logistic regression as the final esstimator
  the results :
  for thrain data :
- accuracy_score : 88%
-  f1_score 88%
-  matthews_corrcoef :75%
avg=84%
  for test data :
- accuracy_score : 82%
-  f1_score 82%
-  matthews_corrcoef :62%
avg=69%
