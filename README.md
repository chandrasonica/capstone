### Capstone Project
Business Problem:
Based on the health data available for someone, identify if that person has a 10-year risk of future coronary heart disease (CHD).

**Author**
Chandra Soni
#### Executive summary
TBD
#### Rationale
Cardiovascular diseases (CVDs) are the number 1 cause of death globally, taking an estimated 17.9 million lives each year, which accounts for 31% of all deaths worlwide.

Most cardiovascular diseases can be prevented by addressing behavioral risk factors such as tobacco use, unhealthy diet and obesity, physical inactivity, and harmful use of alcohol using population-wide strategies.

People with cardiovascular disease or who are at high cardiovascular risk (due to the presence of one or more risk factors such as hypertension, diabetes, hyperlipidaemia or already established disease) need early detection and management, wherein a machine learning model can be of great help.


#### Research Question
Using this model, we are trying to assess if someone is a risk of future coronary heart disease (CHD). 
If we can identify such people, doctors can take preventive measures and suggest individuals be serious about taking care of their physical health.  

#### Data Sources
My dataset comes from the kaggle repository [link](https://www.kaggle.com/code/abrahamanderson/hearth-disease-prediction/datag).  
The dataset is publically available on the Kaggle website, and it is from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The classification goal is to predict whether the patient has 10-year risk of future coronary heart disease (CHD). The dataset provides the patients’ information. It includes over 4,000 records and 15 attributes.

#### Methodology
I used KNN, DTree, logistic regression, and SVM algorithms to find the best model with high accuracy.  Since we want to avoid FN, in this case, I will be looking at the model which gives the highest recall.

#### Results
`I first analyzed, visualized, and then cleaned the data. After that, I split the data for training and testing. I created 4 models with default values for KNN, DTree, logistic regression, and SVM. I see that the highest test accuracy is with Logistic regression and SVM, KNN was also comparable, but training time for SVM was really high, and for KNN, it was really low. Based on this I would go with logistic regression, but the data sample is really small, so we need to run these models with more data before concluding. `

```Here is the result

    model   train_accuracy  test_accuracy   train_time (sec)
model	train_accuracy	test_accuracy	train_time (sec)
0	KNN	0.867847	0.834906	0.009213
1	Dtree	1.000000	0.774764	0.032423
2	LGR	0.854572	0.857311	0.020705
3	SVM	0.857817	0.854953	0.354813


I then used GridSearch for hyperparameter tuning and did the training and testing again, below are the results. Now all models have comparable test accuracy, but training time had huge variance, SVM and KNN took a long time (I had to remove some of the parameters to make it finish on time). Logistic regression finished in only 0.5 sec.

model	train_accuracy	test_accuracy	train_time (sec)	
0	KNN	0.867847	0.834906	3.332418
1	Dtree	0.847788	0.852594	3.672317
2	LGR	0.854572	0.857311	0.506328
3	SVM	0.846608	0.853774	6.749078



#### Outline of project

**Link to the notebook:**

https://github.com/chandrasonica/capstone/blob/main/capstone.ipynb


##### Contact and Further Information