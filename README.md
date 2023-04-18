## Mini Assignment - Done By Jia Qi, Hui Ling & Denis

Predicting Salary of Data Science Job Salaries 🧑‍💼🧑‍💻💵

---

### 🪞Order of Reading Each File: 

1. 🧹 Data-Cleaning-and-Transformation 

2. 📊 EDA-of-Dataset 

3. 🌲Base Model (Random Forest Regressor) 

4. 🔮Prediction Models 

5. 📈Logistic Regression 

---
## 📃 Report :

### ⭐ **Introduction:** 

The dataset we are using is a dataset from [Kaggle](https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries) where it is a dataset of data science jobs. We are predicting `salary_in_usd` against other variables using various models we have been taught as well as other models that are not taught in the course.

We aim to answer which feature in the dataset is correlated to `salary_in_usd`, and does `salary_in_usd` increase or decrease based on the features. Additionally, we created various new features and transformed many variables to be able to fit into the model.  Below is a table for reference on what features are created:

| No. 	| Features Created     	| Remarks                                                                                                                                                                              	|
|-----	|----------------------	|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|
| 1.  	| `salary_group`       	| A classification of the different salary group ranging from "low", "low-mid", "mid", "mid-high", "high" as well as a label "outlier" if its beyond or below upper/lower bound of IEQ 	|
| 2.  	| `compare_avr_salary` 	| Splits salary between above or below Singapore's average salary (referenced from [here](https://www.worlddata.info/average-income.php))                                              	|
| 3.  	| `company_continent`  	| Classify the company location into different continent. <br>i.e. "AFRICA", "ASIA", "AUSTRALIA", "EUROPE", "NORTH AMERICA", "SOUTH AMERICA"                                           	|
| 4.  	| `employee_continent` 	| Classify the location of where the employee is working into different continents. <br>i.e. "AFRICA", "ASIA", "AUSTRALIA", "EUROPE", "NORTH AMERICA", "SOUTH AMERICA"                 	|
| 5.  	| `domain`             	| Classify `job_title` into different domains. <br>i.e. "Management", "Data Science", "Computer Vision", "AI", "Machine Learning", "NLP", "Unknown"                                    	|
| 6.  	| `job_type`           	| Classify `job_title` into different job types. <br>i.e. "Head", "Manager", "Developer", "Analyst", "Scientist", "Consultant", "Engineer"                                             	|


We would also like to explore which feature is the most significant in deciding `salary_in_usd` that would benefit data science students when searching for a job. Finally, we compare the salary in data science to the average salary in Singapore to determine whether Data Science job salaries are being paid higher or lower than the average Singapore income. (Average salary per annum referenced from [here](https://www.worlddata.info/average-income.php)).


### 🔎 **Data Analysis:** 

We started by cleaning the dataset by transforming the data to make it usable for our models. 
Below is a table of a summary of what feature was transformed:
| No. 	| Features Transformed to Categorical 	| New Feature Name to Classify 	| Remarks                                                                                                                                                                                                         	|
|-----	|-------------------------------------	|------------------------------	|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|
| 1.  	| `experience_level`                  	| `experience_levelN`          	| 5 different categories created <br>    1. 0 ( Entry Level )<br>    2. 1 ( Junior MI Mid Level )<br>    3. 2 ( Intermediate SE Senior-level )<br>    4. 3 ( Expert EX Executive-level )<br>    5. 4 ( Director ) 	|
| 2.  	| `company_size`                      	| `company_sizeN`              	| 3 different categories created <br>    1. 0 - S less than 50 employees (small) <br>    2. 1 - M 50 to 250 employees (medium) <br>    3. 2 - L more than 250 employees (large)                                   	|
| 3.  	| `employement_type`                  	| `employment_typeN`           	| 4 different categories created <br>    1. 0 - PT Part-time <br>    2. 1 - FT Full-time <br>    3. 2 - CT Contract <br>    4. 3 - FL Freelance                                                                   	|
| 4.  	| `remote_ratio`                      	| NIL                          	| 3 different categories created <br>    1. 0 - No remote work / less than 20%<br>    2. 1 - 50% Partially remote <br>    3. 2 - 100% Fully remote (more than 80%)                                                	|
| 5.  	| `company_continent`                 	| `company_continentN`         	| 6 different categories created<br>    1. 0 : Europe<br>    2. 1 : Asia<br>    3. 2 : North America<br>    4. 3 : Australia<br>    5. 4 : South America<br>    6. 5 : Africa                                     	|
| 7.  	| `employee_continent`                	| `employee_continentN`        	| 6 different categories created <br>    1. 0 : Europe<br>    2. 1 : Asia<br>    3. 2 : North America<br>    4. 3 : Australia<br>    5. 4 : South America<br>    6. 5 : Africa                                    	|

We have also analyzed what are the distributions of the variables are like to see where majority of our data are for each variable. For example, `salary_group` majority of the datapoints are in the low-mid range. 

Exploratory Data Analysis techniques such as plotting various box plots and heatmaps of `salary_in_usd` to other variables to see the salary are at for each data category of the variable we are comparing to. 
Then based on the EDA we will be able to see which variable we should include or exclude from our model.


### 🔮 **Prediction Models:**

We used `Random Forest Regressor` as our base model to compare to the rest of the models done in this project. All of the models  we did were all further improved using `k-fold cross validation` and `gridsearch`. The improvement of the model can be seen by the accuracy increase or whether the R^2 value is more realistic.

The models we have implemented to compare to the base model are as follows:

1. Linear Regression

2. Decision Tree Regressor
  
3. Support Vector Machine


### 🎑 **Bonus: Logistic Regression Model**

We also attempted to predict whether the `salary_in_usd` will be higher or lower than Singapore's average salary. We started by transforming `salary_in_usd` into a variable called `compare_avr_salary` which is a binary classifier that indicates if a salary is`above average` or `below average`. We then created a logistic regression model to predict whether `salary_in_usd` will be above or below average. The model accuracy was also further improved by using `k-fold cross validation` and `gridsearch` (to select best hyperparameters for the model).

### 📝 <u>**Conclusion:**</u>

In conclusion, we found that the feature that had the highest correlation with salary was the number of years of experience (`experience_level`). And the best model we should use to predict `salary_in_usd` is our base model which is `Random Forest Regressor` with the highest R^2 value score out of all the models we have computed.

We also found out whether the salary range was most influenced by job title and industry that the people who are working in and the average salary in the data science field is about 80% higher than the average salary in Singapore.


### ❓Questions we are exploring:

| No. 	|  🤔❓Questions                                                                                                                                                          	|
|-----	|---------------------------------------------------------------------------------------------------------------------------------------------------------------------	|
| 1.  	| Which feature is correlated to salary (numerical)? and does the salary increase or decrease based on the feature?                                                   	|
| 2.  	| Which feature is the most significant in deciding the range of the salary? (categorical)                                                                            	|
| 3.  	| Explore general summary of whether data science students, what are some qualities that would benefit them if they pay attention to when they are looking for a job. 	|
| 4.  	| What well does the salary in Data Science jobs fare compared to the average in Singapore?                                                                           	|
| 5.  	| Which model performs the best compared to the base model (Random Forest Regressor)?                                                                                 	|
---

  

## Individual Contributions:


| No. 	| Data Cleaning / Transformation / Creating Features                                                                                                                                                                        	| Individual Contribution 	|
|-----	|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|-------------------------	|
| 1.  	| Create new variable to group `salary_in_usd`                                                                                                                                                                              	| Denis                   	|
| 2.  	| Transform `experience_level` to categorical variable                                                                                                                                                                      	| Jia Qi                  	|
| 3.  	| Transform `company_size` to categorical variable                                                                                                                                                                          	| Jia Qi                  	|
| 4.  	| Transform `remote_ratio` to categorical variable                                                                                                                                                                          	| Jia Qi                  	|
| 5.  	| Transform `employment_type` to categorical variable                                                                                                                                                                       	| Jia Qi                  	|
| 6.  	| Transform `company_continent` & `employee_continent` to categorical variable                                                                                                                                              	| Jia Qi                  	|
| 7.  	| Outliers are labeled with ‘outlier’ in new feature called `salary_outliers` & `salary_group`                                                                                                                              	| Denis                   	|
| 8.  	| Creating new feature called `compare_avr_salary` to split salary between below or above national average                                                                                                                  	| Denis                   	|
| 8.  	| Outliers labelled under `salary_group` as 'outlier'                                                                                                                                                                       	| Denis                   	|
| 9.  	| Create a new feature called `job_type` & `domain` that categorizes `job_title` into different positions (i.e manager (lead, manager), engineer (developer), consultant (analyst, researcher, data scientist, specialist)) 	| Hui Ling                	|
| 10. 	| Split `company_location` into `continent` and group them in categorically                                                                                                                                                 	| Hui Ling                	|
  
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
| 1.         	| Organized EDA File and added markdown comments to explain code done in EDA 📙	| Hui Ling                       	|
| 2.         	| Github readme Writeup 📝                                                    	| Jia Qi                         	|
| 4.         	| Video Editing 🎥                                                            	| Denis                          	|
| 5.         	| Slides 🎯                                                                     	| Jia Qi & Denis & Hui Ling      	|

---

### References

1. _Average income around the world_. Worlddata.info. (n.d.). Retrieved April 18, 2023, from https://www.worlddata.info/average-income.php

2. Bhatia, R. (2022, June 15). _Data Science Job Salaries_. Kaggle. Retrieved April 18, 2023, from https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries

3. Brownlee, J. (2020, August 17). _Ordinal and one-hot encodings for Categorical Data_. MachineLearningMastery.com. Retrieved April 12, 2023, from https://machinelearningmastery.com/one-hot-encoding-for-categorical-data/#:~:text=For%20example%2C%20in%20the%20case,be%20calculated%20using%20linear%20algebra.

4. Brownlee, J. (2020, August 2). _A gentle introduction to k-fold cross-validation_. MachineLearningMastery.com. Retrieved April 12, 2023, from https://machinelearningmastery.com/k-fold-cross-validation/

5. GeeksforGeeks. (2023, March 2). _Random Forest regression in python_. GeeksforGeeks. Retrieved April 12, 2023, from https://www.geeksforgeeks.org/random-forest-regression-in-python/

6. _Linear SVC Machine learning SVM example with Python_. Python programming tutorials. (n.d.). Retrieved April 12, 2023, from https://pythonprogramming.net/linear-svc-example-scikit-learn-svm-python/

7. Malik, F. (2022, March 7). _What is grid search?_ Medium. Retrieved April 12, 2023, from https://medium.com/fintechexplained/what-is-grid-search-c01fe886ef0a#:~:text=Grid%20search%20is%20a%20tuning,us%20time%2C%20effort%20and%20resources.

8. Mondal, S. (2023, February 14). _Regression analysis: Beginners comprehensive guide (updated 2023)_. Analytics 
 Vidhya. Retrieved April 12, 2023, from https://www.analyticsvidhya.com/blog/2020/12/beginners-take-how-logistic-regression-is-related-to-linear-regression/#:~:text=The%20Differences%20between%20Linear%20Regression,Logistic%20regression%20provides%20discreet%20output.