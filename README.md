##### Table of contents:

* 1.Introduction
* 2.Dataset Source
* 3.Exploring The Data
* 4.Modelling The Data
* 5.Outcome For The Business Metric Of The Bank To Decide On Term Deposits
* 6.Technologies Used
* 7.Setup Environment
* 8.Attributes within dataset
* 9.References


###### Note: Refer the Setup Environment as there are two files namely: 1.BANK_classification_work.ipynb, 2.Function_script_Bank.ipynb


##### 1.Introduction

* General info: 

    * This dataset is about bank subscriptions and factors influencing customers to subscribe to term deposits. The data collected belongs to the period from May 2008 to November 2010.

    * No of records found within the data file are 41188.

    * No of features found within the data file is 21.

* Project Aim: The target is to design a classification algorithm to find "has the client subscribed a term deposit?" which is under the "y" feature of the dataset.

##### 2.Dataset Source:

* Bank Marketing Data Set. Retrieved from http://archive.ics.uci.edu/ml/datasets/Bank+Marketing

##### 3.Exploring The Data

* The objective is to perform exploratory data analysis by understanding features, descriptive figures (Plots/Boxplots, Cross-Correlation Plot) and skewness associated with the features.

* Encoding categorical features to better understand their relationship with term description. Transforming and normalizing features to prepare the data for the application of machine learning classification algorithms.

##### 4.Modelling The Data

* The objective is to split the data after EDA is completed. Train and test splits are performed on the data set in the ratio of 80:20 respectively.

* Performing the same modelling with other ML algorithms

* Validating the results of the model using statistical tools 

##### 5.Outcome For The Business Metric Of The Bank To Decide On Term Deposits:

* 1.As per our model the bank should focus on these aspects namely : 'age', 'campaign', 'consumer confidence index', 'euribor3m', 'no of people employed by the bank', to drive the no of customers subscribing to term deposits.

* 2.When we compared the feature selected model with the one without feature selection, there was 45% decrease in the false positives. Thus, making the business process for the bank more resource-efficient.

* 3.Within age customers within the age range 32-47 displayed more no of term subscriptions.

* 4.No of contacts to be performed under campaign should focus more on the first two contacts as that represents higher chances for term subscriptions.

* 5.With consumer 'consumer confidence index','euribor3m'and 'no of people employed by the bank' the business model should focus on experimenting with the needs of the customer as no clear patterns were observed.

##### 6.Technologies Used

* Jupyter Notebook for writing scripts in python3.

* Python ML, visualisation and model metrics libraries : pandas, numpy, matplotlib, seaborn, imblearn, sklearn (LogisticRegression, DecisionTreeClassifier, RandomForestClassifier, GridSearchCV, cross_val_score, MinMaxScaler,RFE, SMOTETomek, accuracy_score, precision_score, classification_report, recall_score, confusion_matrix, make_scorer, fbeta_score).


##### 7.Setup Environment.

* Anaconda for Python 3.8 environment for initiating Jupyterlab.

* Uploading data files from the source into Jupyter.

* Operating the python script to perform the analysis.

* There are two script files : 

    * 1.BANK_classification_work.ipynb - the complete end to end data analysis including EDA, data modelling, validation of results, recommendations.
    * 2.Function_script_Bank.ipynb - the complete end to end function script that can be applied by the user on the data set without coding.


##### 8. Attributes within dataset:

* ##### 1.bank client data:
    * 1 - age (numeric)
    * 2 - job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')
    * 3 - marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
    * 4 - education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
    * 5 - default: has credit in default? (categorical: 'no','yes','unknown')
    * 6 - housing: has housing loan? (categorical: 'no','yes','unknown')
    * 7 - loan: has personal loan? (categorical: 'no','yes','unknown')

* ##### 2.related with the last contact of the current campaign:
    * 8 - contact: contact communication type (categorical: 'cellular','telephone')
    * 9 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')
    * 10 - day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')
    * 11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.

* ##### 3.other attributes:
    * 12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
    * 13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
    * 14 - previous: number of contacts performed before this campaign and for this client (numeric)
    * 15 - poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')

* ##### 4.social and economic context attributes
    * 16 - emp.var.rate: employment variation rate - quarterly indicator (numeric)
    * 17 - cons.price.idx: consumer price index - monthly indicator (numeric)
    * 18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric)
    * 19 - euribor3m: euribor 3 month rate - daily indicator (numeric)
    * 20 - nr.employed: number of employees - quarterly indicator (numeric)
    * Output variable (desired target):
    * 21 - y - has the client subscribed a term deposit? (binary: 'yes','no')]


##### 9.References:

* [Moro et al., 2014] S. Moro, P. Cortez and P. Rita. A Data-Driven Approach to Predict the Success of Bank Telemarketing. Decision Support Systems, In press, http://dx.doi.org/10.1016/j.dss.2014.03.001

* Building a logistic regression in python. Retrieved from https://towardsdatascience.com/building-a-logistic-regression-in-python-step-by-step-becd4d56c9c8

* Feature selection with sklearn and pandas.Retrieved from https://towardsdatascience.com/feature-selection-with-pandas-e3690ad8504b

* "DSDJ",Kyle Mckiou's team for conceptual understanding of models and code methodology adopted.

