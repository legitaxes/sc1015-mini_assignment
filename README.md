## Mini Assignment - Done By Jia Qi, Hui Ling & Denis

---

### Order of Reading Each File: 🪞

1. Data-Cleaning-and-Transformation 🧹

2. EDA-of-Dataset 📊

3. Base Model (Random Forest Regressor) 🌲

4. Prediction Models 🔮

5. Logistic Regression 📈

---
### 📃 Report :

⭐ <u>**Introduction:** </u>

The dataset we are using is a dataset from [Kaggle](https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries) where it is a dataset of data science jobs. We are predicting `salary_in_usd` against other variables using various models we have been taught as well as other models that are not taught in the course.

We aim to answer which feature in the dataset is correlated to `salary_in_usd`, and does `salary_in_usd` increase or decrease based on the features. Additionally, we created various new features and transformed many variables to be able to fit into the model. We would like to explore which feature is the most significant in deciding `salary_in_usd` that would benefit data science students when searching for a job. Finally, we compare the salary in data science to the average salary in Singapore to determine whether Data Science job salaries are being paid higher or lower than the average Singapore income. (Average salary per annum referenced from [here](https://www.worlddata.info/average-income.php)).

🔎 <u>**Data Analysis:** </u>

We started by cleaning the dataset and transforming the data to make it usable for our models. Then, Exploratory Data Analysis techniques were done i.e exploring box plots and heatmaps of `salary_in_usd` to other variables. From the EDA we are able to see which variable we should include or exclude from our model.

🔮 <u>**Prediction Models:**</u>

We used `Random Forest Regressor` as our base model to compare the rest of the models done here. The model was also further improved using `k-fold cross validation` and `gridsearch`, improvement of the model can be seen by the accuracy.

  
  

The models we tested to be used to compare are as follows (each with `k-fold cross validation` and `gridsearch` done to further improve the accuracy):

1. Linear Regression

2. Decision Tree Regressor
  
3. Support Vector Machine

🎑 <u>**Other Prediction Models:**</u>

We also attempted to transform the salary data into a binary classifier (labelled as `above average` or `below average`) and created a logistic regression model to predict whether `salary_in_usd` will be above or below average. The model accuracy was also further improved by using `k-fold cross validation` and `gridsearch`.

📝 <u>**Conclusion:**</u>

In conclusion, we found that the feature that had the highest correlation with salary was the number of years of experience (`experience_level`). And the best model we should use to predict `salary_in_usd` is `Decision Tree Regressor` with the highest R^2 value score.

We also found out whether the salary range was most influenced by job title and industry that the people who are working in and the average salary in the data science field is about 80% higher than the average salary in Singapore.

  

### ❓Questions we are exploring:

1. Which feature is correlated to salary (numerical)? and does the salary increase or decrease based on the feature?

2. Which feature is the most significant in deciding the range of the salary? (categorical)

3. Explore general summary of whether data science students, what are some qualities that would benefit them if they pay attention to when they are looking for a job.

4. What is the salary in Data Science jobs like compared to the average in Singapore?

5. Which model performs the best compared to the base model (Random Forest Regressor)?
---

  

### Individual Contributions:


| <b>No.</b> | <b>Data Cleaning / Transformation / Creating Features</b>                                                                                                                                                                 | <b>Individual Contribution</b> |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| 1.         | Create new variable to group `salary_in_usd`                                                                                                                                                                              | Denis                          |
| 2.         | Transform `experience_level` to categorical variable                                                                                                                                                                      | Jia Qi                         |
| 3.         | Transform `company_size` to categorical variable                                                                                                                                                                          | Jia Qi                         |
| 4.         | Transform `remote_ratio` to categorical variable                                                                                                                                                                          | Jia Qi                         |
| 5.         | Transform `employment_type` to categorical variable                                                                                                                                                                       | Jia Qi                         |
| 6.         | Outliers are labeled with ‘outlier’ in new feature called `salary_outliers` & `salary_group`                                                                                                                              | Denis                          |
| 7.         | Creating new feature called `compare_avr_salary` to split salary between below or above national average                                                                                                                  | Denis                          |
| 8.         | Outliers labelled under `salary_group` as 'outlier'                                                                                                                                                                       | Denis                          |
| 9.         | Create a new feature called `job_type` & `domain` that categorizes `job_title` into different positions (i.e manager (lead, manager), engineer (developer), consultant (analyst, researcher, data scientist, specialist)) | Hui Ling                       |
| 10.        | Split `company_location` into `continent` and group them in categorically                                                                                                                                                 | Hui Ling                       |

  
  ---


| <b>No.</b> 	| <b>EDA Required Based on our Problem</b>                                                                                                                  	| <b>Individual Contribution</b> 	|
|------------	|-----------------------------------------------------------------------------------------------------------------------------------------------------------	|--------------------------------	|
| 1.         	| Explore the various domain and management of `job_title`. for example: NLP, ETL, manager, etc.                                                            	| Hui Ling                       	|
| 2.         	| Create various box plots on `salary_in_usd` based on the other variables                                                                                  	| Hui Ling & Denis               	|
| 3.         	| Explore the `domain` and `management` of `job_title`. for example: NLP, ETL, manager, etc.                                                                	| Hui Ling                       	|
| 4.         	| Explore whether people working in big company [`company_size`] earns more (or less)                                                                       	| Denis                          	|
| 5.         	| Whether `employee_residence` & `company_locations` affects `remote_ratio`                                                                                 	| Denis                          	|
| 6.         	| Explore which job title allows you to work at home (`remote_ratio`, explore variables that affects `remote_ratio`)                                        	| Denis                          	|
| 7.         	| Look at whether `employment_type` affects other variables                                                                                                 	| Hui Ling                       	|
| 8.         	| Look at whether people working in different country being paid in different currency (look at average of EUR paid in usd and USD) affects `salary_in_usd` 	| Hui Ling                       	|
| 9.         	| Look at whether `remote_ratio` & other variables that affects salary                                                                                      	| Hui Ling                       	|

  ---
  

| <b>No.</b> 	| <b>Modelling / Machine Learning Algorithms + Doing Something New</b> 	| <b>K-Fold Cross Validation</b> 	| <b>Gridsearch Hyperparameters</b> 	| <b>Individual Contribution</b> 	|
|------------	|----------------------------------------------------------------------	|:--------------------------------:	|:-----------------------------------:	|--------------------------------	|
| 1.         	| Random Forest Regressor                                              	| ✅                              	| ✅                                 	| Jia Qi                         	|
| 2.         	| Decision Tree Regressor                                              	| ✅                              	| ✅                                 	| Jia Qi                         	|
| 3.         	| Linear Regression Model w/ One Hot Encoding                          	| ✅                              	| ✅                                 	| Hui Ling                       	|
| 4.         	| Logistic Regression                                                  	| ✅                              	| ✅                                 	| Denis                          	|
| 5.         	| Support Vector Machine                                               	| ✅                              	| ✅                                 	| Jia Qi                         	|
  
  
---

| <b>No.</b> 	| <b>MISCELLANEOUS</b>                                                       	| <b>Individual Contribution</b> 	|
|------------	|----------------------------------------------------------------------------	|--------------------------------	|
| 1.         	| Organized EDA File and added markdown comments to explain code done in EDA 	| Hui Ling                       	|
| 2.         	| Github readme writeup 📝                                                    	| Jia Qi                         	|
| 4.         	| Video Editing 🎥                                                            	| Denis                          	|
| 5.         	| Slides                                                                     	| Jia Qi & Denis & Hui Ling      	|

---

### References

1. Data Science Student Dataset: https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries

2. Brownlee, J. (2020, August 17). Ordinal and one-hot encodings for Categorical Data. MachineLearningMastery.com. Retrieved April 12, 2023, from https://machinelearningmastery.com/one-hot-encoding-for-categorical-data/#:~:text=For%20example%2C%20in%20the%20case,be%20calculated%20using%20linear%20algebra

3. Brownlee, J. (2020, August 2). A gentle introduction to k-fold cross-validation. MachineLearningMastery.com. Retrieved April 12, 2023, from https://machinelearningmastery.com/k-fold-cross-validation/

4. GeeksforGeeks. (2023, March 2). Random Forest regression in python. GeeksforGeeks. Retrieved April 12, 2023, from https://www.geeksforgeeks.org/random-forest-regression-in-python/

5. Linear SVC Machine learning SVM example with Python. Python programming tutorials. (n.d.). Retrieved April 12, 2023, from https://pythonprogramming.net/linear-svc-example-scikit-learn-svm-python/

6. Malik, F. (2022, March 7). What is grid search? Medium. Retrieved April 12, 2023, from https://medium.com/fintechexplained/what-is-grid-search-c01fe886ef0a#:~:text=Grid%20search%20is%20a%20tuning,us%20time%2C%20effort%20and%20resources

7. Mondal, S. (2023, February 14). Regression analysis: Beginners comprehensive guide (updated 2023). Analytics Vidhya. Retrieved April 12, 2023, from https://www.analyticsvidhya.com/blog/2020/12/beginners-take-how-logistic-regression-is-related-to-linear-regression/#:~:text=The%20Differences%20between%20Linear%20Regression,Logistic%20regression%20provides%20discreet%20output