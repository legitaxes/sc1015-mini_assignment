## Mini Assignment - Done By Jia Qi, Hui Ling & Denis

   
### Task Sheet:
**Data Cleaning/ Transformation/ Creating Features**
1. Split `company_location` to continent level and group them in categorically [assigned @vvhuiling]
2. Think about how to deal with the outlier for `salary_in_usd`
   - Ommit outliers *(not yet decided)*
3. Create a new feature that categorizes `job_title` into different positions (i.e manager(lead, manager), engineer(developer), consultant (analyst, researcher, data scientist, specialist)) [assigned @vvhuiling]
4. Look into One hot encoding (transform categorical values into different forms) and maybe implement them to categorical variables

**EDA Required Based on Our Problem**
1. Explore the domain and management of `job_title`. for example: NLP, ETL, manager, etc. [assigned @vvhuiling]
2. Explore whether people working in big company (`company_size`) earns more (or less) [assigned @XaviaThe2nd]
3. Explore which job title allows you to work at home (`remote_ratio`, explore variables that affects `remote_ratio`) [assigned @XaviaThe2nd]
4. Whether the `employee_residence` & `company_locations` affects `remote_ratio` [assigned @XaviaThe2nd]
5. Look at whether `employment_type` affects other variables [assigned @legitaxes]
6. People working in different being paid in different currency (look at average of EUR paid in usd and USD) affects `salary_in_usd`. [assigned @legitaxes]
7. Ultimately look at whether `remote_ratio` & other variables that affects salary [assigned @legitaxes]



**Modelling / Machine Learning Algorithms + Doing Something New**
1. Use one hot encoding on one model and compare it against using the same model
2. Hyperparameters search (gridsearch)
3. DecisionTree
4. K-fold Cross-validation
5. Regression
6. Classfication
7. Support Vector Machine
8. Random Forest Regressor


**Data Driven Insights & Recommendation**
1. 


---
### Grading Scheme:
![alt text](https://cdn.discordapp.com/attachments/1065968545671958530/1083018055724052520/image.png "grading scheme of overall project")

### Guidelines:
1. What is an "interesting problem" based on the dataset?


2. What do you mean by "data preparation and cleaning"?
    - Preparing means cleaning the data, resizing/reshaping the data, removing outliers (if necessary), balancing imbalanced classes (if necessary), grouping the rows/columns as necessary, etc. This is an important part of any DS/ML project. You may also have to join/merge multiple data sources, plus extract/scrape data from various online sources to work on your problem.


3. How much of visualization should be presented?
    - Part of the 20% in EDA, so **do not spend the bulk of time on cool visualization tools**
    - Do standard exploration of the data, and standard statistical visualizations, as done during the course, just to understand your data well enough, and gather relevant insights that you can present in support of your business case.


4. How much of machine learning techniques should I use for the project?
    - may use any tool and technique that you have seen during the course, for Regression and Classification, but make sure that it is actually required to solve the problem you formulate on the dataset you choose.
    - may choose to use new models that you have not seen in the course, like Random Forest for regression, Naive Bayes for classification, or the Xtra Module techniques like clustering, anomaly detection, etc.

5. What do you mean by "learning something new" beyond the course?
    - make you learn something new. Try to use a new ML model for regression or classification, beyond what we have already covered in the course


6. What is the format for the final Presentation?
    - submit a 10 minute video as your final presentation.
    - format it as a PPT/PDF/Google Slides presentation on the problem you chose, along with some snippets of your code from Jupyter Notebook/Google Colab, and relevant visualizations
    - **The idea for the presentation will be a complete video, explaining all the steps from your motivation to your data-driven solution to the problem**

---
### Question we are exploring: 
1. Which feature is correlated to salary (numerical)? and does the salary increase or decrease based on the feature?
2. Which feature is the most significant in deciding the range of the salary? (categorical)
3. Explore general summary of whether data science students, what are some qualities that would benefit them if they pay attention to when they are looking for a job. 
4. Salary in datascience compared to average in the world and also in singapore (not priority)

---
### Individual Contributions:

**Data Cleaning/ Transformation/ Creating Features**
1. Create new variable to group `salary_in_usd` [completed, done by @XaviaThe2nd]
2. Transform `experience_level` to categorical [completed, done by @legitaxes]
3. Transform `company_size` to categorical [completed, done by @legitaxes]
4. Transform `remote_ratio` to categorical [completed, done by @legitaxes]
5. Transform `employment_type` to categorical [completed, done by @legitaxes]
6. Think about how to deal with the outlier for `salary_in_usd`
   - Outliers are labeled with 'outlier' in new feature called `salary_outliers` & `salary_group` [done by @XaviaThe2nd]
   - Ommit outliers *(not yet decided)*
   - Create category to overcome outliers [done by @XaviaThe2nd]


---
### References
online/offline references go here

---

### Instructions for GitHub Repo
Some instructions that you may follow for the GitHub repository:
- Make sure all your codes/notebooks plus the data is on the repository for the TA to check.
- Make sure the README file is decently written (like a short report) to describe your work.
- README does not need to have all minor details, but it should broadly explain your work.
- README does not need to be too huge. Keep it simple, compact, but sufficiently detailed.
- Don't go over the top please. Try to make the README a 3 to 5 minute read -- not more.
