# UCB-Capstone
UC Berkeley Capstone Project by Armando C Cova

Fall 2024

Exploration of Machine Learning techniques in Human Resources Management
---------------------------------------------------------------------------

We followed the main tenants of the CRISP methodology to explore the application of ML techniques to HR management. In particular we studied absenteeism using a publicly available information database created with records of absenteeism at work from July 2007 to July 2010 at a courier company in Brazil ([link](https://archive.ics.uci.edu/dataset/445/absenteeism+at+work)). 

We performed an exploratory data analysis of absenteeism and how it was connected to several key factors (features) in the database. A summary of main findings is given below:
* The total number of absenteeism hours was 5124.
  
* The average absence time was 7.4 hr. The STD was 13.6 hr.
  
* Half of the absent workers were away for 3 hr or less
  
* The maximum absence time was 120 hr (15 days)
  
* The average Service time of absentees was 12.6 years with minimum of 1 and a maximum of 29 years. 75% of absentees had less than 16 years of service.
  
* The mean Age of absentees was 36.3 years with a minimum of 27 years and a maximum of 58 years. 75% of absentees were younger than 40 yo
  
* The average distance from their residence location to work for absentees was 29.9 Km
    
* There were 44 individuals with perfect attendance record (6% of total)
  
* By extension, 94% of individuals reported absences during the year 

* The main reasons for absences were medical consultation (21.4%), dental consultation (16.1%), physiotherapy(9.8%), diseases of the musculoskeletal system and connective tissue (7.9%), injuries (5.7%) and patient follow-up(5.5%)

* The majority of absent hours were caused by diseases of the musculoskeletal system and connective tissue (842 hr); injury, poisoning and certain other consequences of external causes (729 hr); as well as medical(424 hr) and dental(335 hr) consultations. There were significant absences due to diseases of the respiratory(276 hr) and digestive(297 hr) systems.

* The months with the most absenteeism cases were March (12%), February (10.3%) and July (9.3%)
  
* The months with the most absenteeism time were March (765 hr), July (734 hr), April (482 hr) and November (473 hr)
  
* The days with the most absence cases were Monday (22.1%), Wednesday (20.8%), Tuesday (20.3%) and Friday (19.8%)
  
* The days with the most absenteeism hours were Monday (1489 hr), Tuesday (1229 hr), Wednesday (1115 hr) and Friday (738 hr)
  
* Absence cases were almost equally distributed across seasons with Autumn having a slight uptick (27.2%)
  
* The season with the most absenteeism hours was Autumn (1492 hr), followed by Spring (1241) and Winter (1239) which differed very little.

* None of the absentees were subject to disciplinary action prior to being absent
  
* The majority of the absentees (82%) had high school education

* Employees with this level of education had the most absenteeism hours (4393 hr)

* large majority of absentees (58.5%) had children

* The largest number of absenteeism hours were seen in employees with 2 children (1649 hr)
  
* 56.2 percent of absentees were social drinkers. The largest number of absenteeism hours were in the social drinker group (3226 hr)
  
* 6.6 percent of absentees were social smokers. The largest number of absenteeism hours were in the non-smoker group (4773 hr)
  
* 37.8% of absenteeism cases were found in employees who owned pets. The total number of absenteeism hours for pet owners was 1983 hr. The largest number of hours belonged to the no-pet ownership group (3141 hr)
  
* 32.2% of absenteeism cases were found in employees with obesity. The total number of absenteeism hours for these employees was 1461 hr
  
* 31.9% of absenteeism cases were found in employees who were overweight. The total number of absenteeism hours for these employees was 1931 hr.
  
* 40.4% of absenteeism cases were found in employees who were younger than 35 years old. 38.8% of cases were found in the 35 to 40 years old bracket
  
* The largest number of absent hours (1777 hr) were found in the 33-40 year old bracket
  
* 43.7% of absenteeism cases were found in employees with a 240 to 250 Workload average a day
  
* 61.5% of absentees had a transportation expense between 175 and 280
  
* 67.7% of absentees live 25 Km or farther from work. The largest group of absentees (27.9%) live 50+ Km from work
  
* 88.9% of absences were in employees with 9 to 18 years of service
  
* The largest number of absence hours (3182 hr) were found in the group with 9-14 years of service


Following this statistical analysis we proceeded to model absenteeism in an attempt to develop a tool for predicting employee absences. For this purpose we framed the modeling as a binary classification problem that captured the influence of significant absenteeism events, considered as such when the employee absence time was > 4 Hr.  We employed a variety of known classification methods (KNN, Decision Tree, Logistic Regression, SVM, Random Forest, Naive Bayes, etc) and compared their predictive performance on test data sets. The performance metrics used were accuracy, precision, recall and F1 scores. Hyperparameter searches on the different estimators were carried out using different methods (GridSearch, RadomizedSearch, BayesianSearch) in an attempt to optimize performance for accuracy, precision and F1 scores. The best performing models were GradientBoost, Random Forest and KNN (details in the presentation Exploring ML-AI techniques in HR management v1p0 - Armando Cova.pptx attached)

