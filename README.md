**# KOAB-Titanic-3288**

# Titanic Survival Prediction Model Card

### Basic Information

* **Person or organization developing model**: Kevin Etesham, `kevinetesham4@gwmail.gwu.edu`; Liv Gao, 'livgao26@gwmail.gwu.edu'; Acadia Grenier, 'acadiagrenier@gwmail.gwu.edu'; Ben Eber, 'ben.eber@gwmail.gwu.edu'
* **Model date**: December 9, 2024
* **Model version**: 1.0
* **License**: MIT
* **Model implementation code**: [titanic_3288.py] (https://github.com/kevinete4/KOAB-Titanic-3288/blob/main/titanic_3288.py)

* ### Intended Use
* **Primary intended uses**: This model is an *example* predictive model of the default classifier, with an *example* use case for determining the survivors of the Titanic Disaster
* **Primary intended users**: Students in GWU DNSC 3288 course.
* **Out-of-scope use cases**: Any use beyond an educational example is out-of-scope.

* ### Training Data

* Data dictionary: 

| Name | Modeling Role | Measurement Level| Description|
| ---- | ------------- | ---------------- | ---------- |
| **PassengerId** | input | int | ID for each passenger |
|**Survived**| input | int | 0 = Did not survive, 1 = Did survive  |
| **Pclass** | demographic information | int | Ticket Class: 1 = 1st, 2 = 2nd, 3 = 3rd |
| **Sex** | demographic information | int | 1 = male; 2 = female |
| **Age** | demographic information | int | age in years |
| **Name** | demographic information | Str | Name of passenger |
| **SibSp** | demographic information | int | 	# of siblings / spouses aboard the Titanic |
| **Parch** | demographic information | int | 	# of parents / children aboard the Titanic |
| **Ticket** | demographic information | int | Ticket number |
| **Fare** | demographic information | int | Passenger fare |
| **Cabin** | demographic information | int | Cabin number |
| **Embarked** | demographic information | int | C = Cherbourg, Q = Queenstown, S = Southampton |
