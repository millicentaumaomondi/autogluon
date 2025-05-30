# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Millicent Auma Omondi

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: Add your explanation
To submit the results, we had to extract the target variable "count" column and then save it as a csv, that is, submission.csv

### What was the top ranked model that performed?
TODO: Add your explanation
From the Autogluon, the top ranked model that performed well was WeightedEnsemble_L3 

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: Add your explanation
It shows that the dataset has no missing values, the data types and how the data is distributed.
For the new features from the datetime column, we parsed the datetime strings into year, month and day

### How much better did your model preform after adding additional features and why do you think that is?
TODO: Add your explanation
The model's performance improved slightly. This was due to the additional features, year, month and day, adding more information to the model during training.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation
Tuning the hyperparameters improved the model's performance as the score values increased.
Adding features improved the score slightly, from -49.001 to -48.984, and hyperparameter optimization (hpo) gave the biggest improvement to -48.767.


### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation
Finetuning step: Experimenting with different hyperparameters 

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|num_bag_folds=8|num_stack_levels=1|num_bag_sets=1|-49.00|
|add_features|num_bag_folds=8|num_stack_levels=1|num_bag_sets=1|-48.98|
|hpo|num_bag_folds=5|num_stack_levels=2|num_bag_sets=1|-48.77|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](model_test_score.png)

## Summary
TODO: Add your explanation
In this projectt we built and optimied a bike sharing demand model using Autogluon and submitted the results to kaggle.The best model was WeightedEnsemble_L3.  We started with a baseline model using default settings, and achieved an initial RMSE score of -49.00. By adding additional features like day, manth and year from the dataerime column, the model's performance slightly to an RMSE score of -48.98. Optimizing the hyperparameters improved the RMSE to -48.77. 
