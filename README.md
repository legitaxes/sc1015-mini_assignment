## Mini Assignment - Done By Jia Qi, Hui Ling & Denis
---
### Order of File:
1. Data-Cleaning-and-Transformation
2. EDA-of-Dataset
3. Base Model (Random Forest Regressor)
4. Prediction Models
5. Logistic Regression
---

### Short Report:
<u>**Introduction:**</u>

The dataset we are using is a dataset from kaggle where we are predicting `salary_in_usd` using various models.

We aim to answer which feature in the dataset is correlated to `salary_in_usd`, and does `salary_in_usd` increase or decrease based on the features. Additionally, we would like to explore which feature is the most significant in deciding `salary_in_usd` that would benefit data science students when searching for a job. Finally, we compare the salary in data science to the average salary in Singapore (referenced from [here](https://www.worlddata.info/average-income.php)).


<u>**Data Analysis:**</u>

We started by cleaning the dataset and transforming the data to make it usable for our models. Then, Exploratory Data Analysis techniques were done i.e exploring box plots and heatmaps of `salary_in_usd` to other variables. From the EDA we are able to see which variable we should include or exclude from our model. 


<u>**Prediction Models:**</u>

We used `Random Forest Regressor` as our base model to compare the rest of the models done here. The model was also further improved using `k-fold cross validation` and `gridsearch`, improvement of the model can be seen by the accuracy.


The models we tested to be used to compare are as follows (each with `k-fold cross validation` and `gridsearch` done to further improve the accuracy):

- ==1. Linear Regression==

- ==2. Decision Tree Regressor==

- ==3. Support Vector Machine==

<u>**Other Prediction Models:**</u>

We also attempted to transform the salary data into a binary classifier (labelled as `above average` or `below average`) and created a logistic regression model to predict whether `salary_in_usd` will be above or below average. The model accuracy was also further improved by using `k-fold cross validation` and `gridsearch`.


<u>**Conclusion:**</u>
In conclusion, we found that the feature that had the highest correlation with salary was the number of years of experience (`experience_level`). And the best model we should use to predict `salary_in_usd` is `Decision Tree Regressor` with the highest R^2 value score. 
We also found out whether the salary range was most influenced by job title and industry that the people who are working in and the average salary in the data science field is about 80% higher than the average salary in Singapore.

### Questions we are exploring: 
1. Which feature is correlated to salary (numerical)? and does the salary increase or decrease based on the feature?
2. Which feature is the most significant in deciding the range of the salary? (categorical)
3. Explore general summary of whether data science students, what are some qualities that would benefit them if they pay attention to when they are looking for a job. 
4. Salary in datascience compared to average in the world and also in singapore (not priority)
5. What is the predicted monthly salary in US dollars for Junior, Mid-level and Senior Developers, who work remotely more than 50% of the time, and located in the same country as the employee's residence? (To solve this problem, we would need to filter the dataset based on the given criteria, calculate the average salary in US dollars for the filtered employees, and then present the result)


---
### Guideline:
1. What is the format for the final Presentation?
    - submit a 10 minute video as your final presentation.
    - format it as a PPT/PDF/Google Slides presentation on the problem you chose, along with some snippets of your code from Jupyter Notebook/Google Colab, and relevant visualizations
    - **The idea for the presentation will be a complete video, explaining all the steps from your motivation to your data-driven solution to the problem**

---

### Individual Contributions:

**Data Cleaning/ Transformation/ Creating Features**
1. Create new variable to group `salary_in_usd` [done by @XaviaThe2nd]
2. Transform `experience_level` to categorical [done by @legitaxes]
3. Transform `company_size` to categorical [done by @legitaxes]
4. Transform `remote_ratio` to categorical [done by @legitaxes]
5. Transform `employment_type` to categorical [done by @legitaxes]
6. Think about how to deal with the outlier for `salary_in_usd`
   - Outliers are labeled with 'outlier' in new feature called `salary_outliers` & `salary_group` [done by @XaviaThe2nd]
   - Outliers are labeled, can easily exclude them if we want to [done by @XaviaThe2nd]
   - Create category to overcome outliers [done by @XaviaThe2nd]
7. Create a new feature called `job_type` & `domain` that categorizes `job_title` into different positions (i.e manager(lead, manager), engineer(developer), consultant (analyst, researcher, data scientist, specialist)) [done by @vvhuiling]
8. Split `company_location` into `continent` and group them in categorically [done by @vvhuiling]


**EDA Required Based on Our Problem**
1. Explore the various domain and management of `job_title`. for example: NLP, ETL, manager, etc. [done by @vvhuiling]
2. Create various box plots based on the other variables (done by @XaviaThe2nd & @vvhuiling)
3. Explore the domain and management of `job_title`. for example: NLP, ETL, manager, etc. [done by @vvhuiling] 
4. Explore whether people working in big company (`company_size`) earns more (or less) [done by @XaviaThe2nd]
5. Explore which job title allows you to work at home (`remote_ratio`, explore variables that affects `remote_ratio`) [done by @XaviaThe2nd]
6. Whether the `employee_residence` & `company_locations` affects `remote_ratio` [done by @XaviaThe2nd]
7. Look at whether `employment_type` affects other variables [done by @vvhuiling]
8. Look at whether people working in different country being paid in different currency (look at average of EUR paid in usd and USD) affects `salary_in_usd`. [done by @vvhuiling]
9. Look at whether `remote_ratio` & other variables that affects salary [done by @vvhuiling]


**Modelling / Machine Learning Algorithms + Doing Something New**
1. Hyperparameters search (gridsearch) (individual model has gridsearch)
2. K-fold Cross-validation (individual model has gridsearch)
3. Decision Tree Regressor (done by @legitaxes)
4. Random Forest Regressor (done by @legitaxes)
5. Use one hot encoding on Linear Regression model and compare it against using logistics regression model (done by @vvhuiling)
6. Logistic Regression (categorical) (done by @XaviaThe2nd)
7. Support Vector Machine (done by @legitaxes)


**MISCELLANEOUS**
1. Organized EDA file and added markdown comments to explain the code done (done @vvhuiling)


---
### References
1. Data Science Student Dataset: https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries

2. Brownlee, J. (2020, August 17). Ordinal and one-hot encodings for Categorical Data. MachineLearningMastery.com. Retrieved April 12, 2023, from https://machinelearningmastery.com/one-hot-encoding-for-categorical-data/#:~:text=For%20example%2C%20in%20the%20case,be%20calculated%20using%20linear%20algebra. 

3. Brownlee, J. (2020, August 2). A gentle introduction to k-fold cross-validation. MachineLearningMastery.com. Retrieved April 12, 2023, from https://machinelearningmastery.com/k-fold-cross-validation/ 

4. GeeksforGeeks. (2023, March 2). Random Forest regression in python. GeeksforGeeks. Retrieved April 12, 2023, from https://www.geeksforgeeks.org/random-forest-regression-in-python/ 

5. Linear SVC Machine learning SVM example with Python. Python programming tutorials. (n.d.). Retrieved April 12, 2023, from https://pythonprogramming.net/linear-svc-example-scikit-learn-svm-python/ 

6. Malik, F. (2022, March 7). What is grid search? Medium. Retrieved April 12, 2023, from https://medium.com/fintechexplained/what-is-grid-search-c01fe886ef0a#:~:text=Grid%20search%20is%20a%20tuning,us%20time%2C%20effort%20and%20resources. 

7. Mondal, S. (2023, February 14). Regression analysis: Beginners comprehensive guide (updated 2023). Analytics Vidhya. Retrieved April 12, 2023, from https://www.analyticsvidhya.com/blog/2020/12/beginners-take-how-logistic-regression-is-related-to-linear-regression/#:~:text=The%20Differences%20between%20Linear%20Regression,Logistic%20regression%20provides%20discreet%20output.  

---

### Instructions for GitHub Repo
- Make sure the README file is decently written (like a short report) to describe your work.
- README does not need to have all minor details, but it should broadly explain your work.
