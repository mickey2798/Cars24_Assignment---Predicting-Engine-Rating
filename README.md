# Cars24_Assignment---Predicting-Engine-Rating

### Objective:
Your task is to write a small Python or R script that predicts the engine rating based on the inspection parameters using only the provided dataset. You need to find all the cases/outliers where the rating has been given incorrectly as compared to current condition of the engine.

This task is designed to test your Python or R ability, your knowledge of Data Science techniques, your ability to find trends, outliers, relative importance of variables with deviation in target variable and your ability to work effectively, efficiently and independently within a commercial setting.

This task is designed as well to test your hyper-tuning abilities or lateral thinking.
 
### Deliverables:
·         One Python or R script
·         One requirements text file including an exhaustive list of packages and version numbers used in your solution
·         Summary of your insights
·         List of cases which are outliers/incorrectly rated as high or low and it should be backed with analysis/reasons.
·        model object files for reproducibility.

 
### Your solution should at a minimum do the following:
·         Load the data into memory
·         Prepare the data for modelling
·         EDA of the variables
·         Build a model on training data
·         Test the model on testing data
·         Provide some measure of performance
·         Outlier analysis and detection


Please answer the following:

1.Briefly describe your approach to this problem and the steps you took

I. By analysing the data, we get to know Dataset has number of missing values. 
II. Did  Data pre-processing by handling  missing values and then worked on categorical data using one –hot encoding technique
III. Used Various Machine learning models for training and testing  data, starting from basics to ensembling. 
IV.  Got a reasonable MSE score on SVR and on ensemble Regressor.
2.            Basics:

a. How well does your model work?

• My model worked well with the ensemble regressor, as it combine the decisions from multiple models 
to improve the overall performance. 

b.How do you know for sure that’s how well it works?

• This model works well for sure because when we calculated mean_squared_error for our model(ensemble regressor), 
it came out to be 0.0383 which is much better i.e, our error is quite low.

c.What stats did you use to prove its predictive performance and why?

• As our model, Predicting Engine Rating , is a regression problem, we use mean squared error. 
Since the errors are squared before they are averaged in MSE, it gives a relatively high weight to large errors. 
This means the MSE should be more useful when large errors are particularly undesirable.
d.What issues did you encounter?

• Lots of missing values are there which needed to be handled  for best fit model
• Handled categorical data using One- hot encoding for multivariable
• Highly imbalanced data

e.What insights did you obtain from this data? For example: What features are important? Why? What visualizations help you understand the data?

• As we have to handle lot of missing values here, we have to choose features that have enough data to train our model better
• Using heatmap visualization, we get to know about features/columns that have lots of missing values . So we removed those features with more than 50% missing values
• By visualizing ratings-plots, we came to know that our data is highly imbalanced. So we can’t use Accuracy as our performance metric
3.Next steps:

a.What other data (if any) would have been useful?

• There could have been numerous data about the wear and tear of the engine which could have been used but also numerical data 
like the life of the engine and fuel type related life is also detectable as 
diesel engines have a lesser life than petrol engines, number of accidents, number of services etc. 
Some of these variable could have acted as constraints or good predictors 
but with a good and strong correlation for determining the output.

b.What are some other things you would have done if you had more time?

• I would have used more time to identify more anomalies in data and specifically used that time to build a good model 
for the data as it took me a little more than usual time to determine the best 
possible methods to find the prediction model.

• I would have dealt with the ratings imbalance Problem. Generally, Whenever this problem arises in 
classification problem I use a technique known as SMOTE(Synthetic Minority Oversampling Technique). 
As this is a Regression problem, We can use 
SMOGN(Synthetic Minority Over-Sampling Technique for Regression with Gaussian Noise).
