**# KOAB-Titanic-3288**

# Titanic Survival Prediction Model Card

### Basic Information

* **Person or organization developing model**: Kevin Etesham, `kevinetesham4@gwmail.gwu.edu`; Liv Gao, `livgao26@gwmail.gwu.edu`; Acadia Grenier, `acadiagrenier@gwmail.gwu.edu`; Ben Eber, `ben.eber@gwmail.gwu.edu`
* **Model date**: December 9, 2024
* **Model version**: 1.0
* **License**: MIT
* **Model implementation code**: [titanic_3288.ipynb](https://github.com/kevinete4/KOAB-Titanic-3288/blob/main/titanic_3288.py)

* ### Intended Use
* **Primary intended uses**: This model is an *example* predictive model of the default classifier, with an *example* use case for determining the survivors of the Titanic Disaster
* **Primary intended users**: Students in GWU DNSC 3288 course.
* **Out-of-scope use cases**: Any use beyond an educational example is out-of-scope.

* ### Training Data

* Data dictionary: 

| Name | Modeling Role | Measurement Level| Description|
| ---- | ------------- | ---------------- | ---------- |
| **PassengerId** | input | int | ID for each passenger |
|**Survived**| input | float | 0 = Did not survive, 1 = Did survive  |
| **Pclass** | demographic information | int | Ticket Class: 1 = 1st, 2 = 2nd, 3 = 3rd |
| **Sex** | demographic information | object | male,female |
| **Age** | demographic information | int | age in years |
| **Name** | demographic information | object | Name of passenger |
| **SibSp** | demographic information | int | 	# of siblings / spouses aboard the Titanic |
| **Parch** | demographic information | int | 	# of parents / children aboard the Titanic |
| **Ticket** | demographic information | object | Ticket number |
| **Fare** | demographic information | float | Passenger fare |
| **Cabin** | demographic information | object | Cabin number |
| **Embarked** | demographic information | object | C = Cherbourg, Q = Queenstown, S = Southampton |

* **Source of training data**: Kaggle, Titanic - Machine Learning from Disater
* **How training data was divided into training and validation data**: 70% training, 21% validation, 9% test
* **Number of rows in training and validation data**:
  * Training data: 499 rows and 6 columns
  * Validation data: 150 rows and 6 columns
  * Testing data: 65 rows and 6 columns
 
* ### Test Data
* **Source of test data**: Kaggle, Titanic - Machine Learning from Disater
* **Number of rows in test data**: 65 rows
* **State any differences in columns between training and test data**: None

* ### Model details
* **Columns used as inputs in the final model**: 'PassengerId', 'Survived', 'Pclass', 'Name', 'Sex', 'Age', 'SibSp',
       'Parch', 'Ticket', 'Fare', 'Cabin', 'Embarked'
* **Column(s) used as target(s) in the final model**: 'Survived'
* **Type of model**: Extra Trees Classifier
* **Software used to implement the model**: Python, scikit-learn
* **Version of the modeling software**: 1.5.2
* **Hyperparameters or other settings of your model**: 
```
clf_ext = ExtraTreesClassifier(
    max_features=5,
    bootstrap=True,
    oob_score=True,
    criterion='entropy',
    min_samples_leaf=3,
    min_samples_split=8,
    n_estimators=20,
    random_state=SEED
    )
```
### Quantitative Analysis

* Models were assessed primarily with AUC and AIR. See details below:

| Train AUC | Validation AUC | Test AUC |
| ------ | ------- | -------- |
| 0.871 | 0.870  | Need* |

| Group | Validation AIR |
|-------|-----|
| #1 | 0.8345 |
| #2 | 0.8765 |
| #3 | 1.098 |
| #4 | 1.245 |

#### Correlation Heatmap
![Correlation Heatmap](![image](https://github.com/user-attachments/assets/b50f3ba9-6f61-42ac-96ff-6efe3ce6d3d5)






