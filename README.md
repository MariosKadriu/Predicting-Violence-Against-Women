# Predicting Violence Against Women

## Table of Contents

[Description](https://github.com/MariosKadriu/Predicting-Violence-Against-Women#-description)
 
[Dataset](https://github.com/MariosKadriu/Predicting-Violence-Against-Women#-dataset)

[Installation](https://github.com/MariosKadriu/Predicting-Violence-Against-Women#%EF%B8%8F-installation)

[Exploratory Data Analysis](https://github.com/MariosKadriu/Predicting-Violence-Against-Women#-exploratory-data-analysis)

[Data Preprocessing](https://github.com/MariosKadriu/Predicting-Violence-Against-Women#-data-preprocessing)

[Modeling and Evaluation](https://github.com/MariosKadriu/Predicting-Violence-Against-Women#-modeling-and-evaluation)


## 📝 Description

During my postgraduate studies in the Data and Web Science program at Aristotle University of Thessaloniki, I completed the aforementioned project as part of the Machine Learning course. The project's goal was to analyze the data, process it correctly, and then use it to train machine learning algorithms to anticipate the impact of abusive acts on the victims' subsequent lives. The target variable in the dataset is OUTCOME.

## 📚 Dataset

Violence Against Women dataset from the Pacific Data Hub data source comprises records gathered from several official international surveys reporting on indicators linked to violence against women in 22 Pacific Ocean nations. These data refer to the period 2006 - 2019.

Dataset can be found here: https://github.com/MariosKadriu/Predicting-Violence-Against-Women/blob/main/data/VAW.csv

## 🖥️ Installation

### 🛠️ Requirements
* Python >= 3.6
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Imbalanced-learn
* XGBoost

### ⚙️ Setup

All of the above packages can be installed from the following commands.

```bash
pip install numpy
pip install pandas
pip install matplotlib
pip install -U scikit-learn
pip install -U imbalanced-learn
pip install xgboost

```

## 🔍 Exploratory Data Analysis

### Number of cases per year
![image-1](https://user-images.githubusercontent.com/19438003/191947304-d93139ef-a8c4-49b1-9c7e-2c900b5d1b68.png)

### Number of cases per each pacific island country and territory
![image-2](https://user-images.githubusercontent.com/19438003/191947823-7b8adee3-9093-44be-b3bb-3c51b60223ad.png)

### Number of cases per topic
![image-3](https://user-images.githubusercontent.com/19438003/191947909-6edc16a2-a89b-4fc4-9ff1-6e4c756582cf.png)

### Number of cases per each women's condition
![image-4](https://user-images.githubusercontent.com/19438003/191948112-b8427c93-36b0-4e55-8b06-aa6663095401.png)

### Number of cases per each type of violence
![image-5](https://user-images.githubusercontent.com/19438003/191948222-2cc743a2-7955-4c58-9795-703263a60160.png)

### Number of cases per each perpetrator type
![image-6](https://user-images.githubusercontent.com/19438003/191948529-b6c9a817-125c-4453-ab04-9b27bfd4700d.png)

### Number of cases per each period of life
![image-7](https://user-images.githubusercontent.com/19438003/191948913-227fd53a-6fa1-4c5a-a023-3bcdb7d9774c.png)

### Number of cases per each outcome
![image-8](https://user-images.githubusercontent.com/19438003/191949386-b669d138-6865-4cdb-8310-ddfaf6717c6e.png)

## ⏳ Data Preprocessing

* Drop of insignificant features
* Seperate features into numerical features and categorical
* Impute missing values of numerical features using KNNImputer
* Impute missing values of categorical features using SimpleImputer
* Encode categorical features using OneHotEncoder
* Scaling features using MinMaxScaler
* PCA is used to reduce dimensionality by adjusting the variance of the input that is expected to be explained by the produced components.
* Over Sampling using RandomOverSampler in order to deal with the imbalance of classes in the dataset.
* Impute missing values of dependent variable OUTCOME: Outcome using Clustering
* K-Fold Cross Validation used to split all the samples in 10 groups of samples
* Saving final dataset with all values filled

## 🎯 Modeling and Evaluation

### Models

* Logistic Regression
* Decision Trees
* Random Forest
* K-Nearest Neighbors
* Naive Bayes
* Multilayer perceptron
* Support Vector Machine

### Evaluation Metrics

* Total Training Time
* Accuracy
* Precision
* Recall
* F1-Score

### Results

#### Scores when missing values of dependent variable OUTCOME were removed (used 544 rows for training)
![image-9](https://user-images.githubusercontent.com/19438003/191952434-8a30a530-e85e-44ae-b26f-544c6f5e40bb.jpg)

#### Scores after imputing missing values of dependent variable OUTCOME (used all rows for training)
![image-10](https://user-images.githubusercontent.com/19438003/191953168-fda35ec2-6b5f-4c30-83a3-d6d06ae88322.jpg)
