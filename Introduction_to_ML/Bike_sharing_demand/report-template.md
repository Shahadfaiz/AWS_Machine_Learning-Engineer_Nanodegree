# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Shahad Faiz

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I realized that we cannot submit negative prediction to the Kaggle competition, so we need to adjust any negative predictions to 0. Moreover, it’s essential to format the submission correctly according to the structure provided in the "sampleSubmission.csv" file.

### What was the top ranked model that performed?
The model WeightedEnsemble_L3 was the best performing model in step five of the project. 

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The exploratory analysis revealed that the time variable was incorrectly formatted as an object. To address this, we converted it to a datetime format and further extracted features such as month, day, day of the week, and time.

### How much better did your model preform after adding additional features and why do you think that is?
The model's performance improved significantly; initially, we had a score of around 1.82227, but after incorporating temporal variables, it dropped to 0.49663. This highlights the importance of time-related features.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
After adjusting some hyperparameters, the model's performance did not improve; instead, the score slightly increased. Initially, the model had a better score of 0.49663, but after tuning, it rose to 0.76297.

### If you were given more time with this dataset, where do you think you would spend more time?
I would definitely spend more time exploring the data, creating new features, and experimenting with different hyperparameter tuning strategies, as these could potentially improve the model's performance even further.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default|default|default|1.82227|
|add_features|default|default|default|0.49663|
|hpo||max_depth: 30|max_features: 0.92505|max_samples: 0.92904|0.76297|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

![report1](https://github.com/user-attachments/assets/0fb9618d-d091-4058-9f92-f7753aa11fc0)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![report2](https://github.com/user-attachments/assets/6349d741-c484-442a-949a-9e9c5a96c9ec)


## Summary
In summary, I was highly impressed with AutoGluon's performance on this dataset. It simplifies the process of finding efficient models, allowing us to concentrate more on improving data quality, feature engineering, and fine-tuning hyperparameters.

Moving forward, the next steps would involve deeper data exploration through visualizations and statistical analysis, selecting the best-performing model, and then fine-tuning its hyperparameters to aim for a competitive edge.
