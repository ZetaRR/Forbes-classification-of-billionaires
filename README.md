## Forbes Financial and Tech Billionaires
![Project Photo](https://mms.businesswire.com/media/20210826005471/en/1187937/5/Forbes-Black.jpg)
---
### Disclaimer 🔺
* Please open all .ipynb notebooks in google.colab , because github has problems with showing visualization packages.
![disclaimer](https://snipboard.io/uHI1v5.jpg)
---
### Project Overview 🔎🔎🔎
* In the given project binary classification was conducted, main idea is to make an algorithm that can divide between Financial and Tech billionaires from the API Forbes data.
---
### How this project will help? ❔❔❔
* This project can help journalist to fill information for upcoming billionaires, also conducted EDA helps to spot some correlations between different open-source information about billionaires/millionaires that could be used in social studies.
---
### Resources Used 🔨🔨🔨
* *Packages: pandas, catboost, shap, sklearn, google, numpy, matplotlib, seaborn, plotly, missingno, os, datetime, imblearn*
* *Data: Public Forbes API https://rapidapi.com/snldnc-kpCtDKbxo_F/api/forbes-worlds-billionaires-list/pricing*
---
### Details of Project 🚨🚨🚨
* This project was built using Google Colab. Therefore to view plotly plots you should view notebook by opening colab notebook.
* In this github repository there are two notebooks. First of them - ```ForbesData.ipynb``` which has data extraction from Forbes API. Second one is ```ForbesBinaryClassification.ipynb``` - which has EDA & Building model process.
---
### Phases in ForbesBinaryClassification 🚧🚧🚧
1. Installation & Import of required libraries
2. Structure Investigation
3. Exploratory Data Analysis (EDA)
4. Correlationship Analysis
5. Preprocessing dataframe for building models
6. Baseline models
7. Fine tuning
8. Interpretability
---
### Models 📠📠📠
* Ridge Classifier

![Ridge](https://snipboard.io/b6XKl0.jpg)
* LogisticRegression

![Logistic Regression](https://snipboard.io/v3TUbS.jpg)
* DecisionTree Classifier

![DecisionTreeClassifier](https://snipboard.io/BUJI8K.jpg)
* RandomForest Classifier

![RandomForestClassifier](https://snipboard.io/cWkwxd.jpg)
* GradientBoosting Classifier

![GradientBoostingClassifier](https://snipboard.io/D1JWON.jpg)
* AdaBoost Classifier

![AdaBoostClassifier](https://snipboard.io/yuSqBI.jpg)
* CatBoost Classifier

![CatBoost](https://snipboard.io/Jnwoe7.jpg)
* Voting Classifier (RandomForest Classifier with GradientBoosting Classifier (*hard voting*))

![Voting Classifier hard](https://snipboard.io/6o5aBr.jpg)
* Voting Classifier (RandomForest Classifier with GradientBoosting Classifier (*soft voting*))

![Voting Classifier easy](https://snipboard.io/SgkpeN.jpg)
* Bar plot containing Test accuracy results of Models
![df with results](https://snipboard.io/v1Tehl.jpg)
---
### Fine-tuning 🕹🕹🕹
* For fine-tuning RandomForestClassifier was choosen. ```GridSearchCV``` were used for finding optimal parameters. Fine-tuned parameters
1. ```n-estimators``` - The number of trees in the forest.
2. ```max_depth``` - The maximum depth of the tree. If None, then nodes are expanded until all leaves are pure or until all leaves contain less than min_samples_split samples.
3. ```min_samples_split``` - The minimum number of samples required to split an internal node
---
### Interpretability ⚙️⚙️⚙️
*SHAP — which stands for SHapley Additive exPlanations — is probably the state of the art in Machine Learning explainability. This algorithm was first published in 2017 by Lundberg and Lee and it is a brilliant way to reverse-engineer the output of any predictive algorithm. In a nutshell, SHAP values are used whenever you have a complex model (could be a gradient boosting, a neural network, or anything that takes some features as input and produces some predictions as output) and you want to understand what decisions the model is making.*

[Original Paper about SHAP values](https://arxiv.org/abs/1705.07874)
* Feature importance calculated by SHAP value
* 
![Feature importance calculated by SHAP value](https://snipboard.io/8gXJMb.jpg)
* How features influence decision-making in different cases (row[1])
* 
![features influence decision-making](https://snipboard.io/m4anhd.jpg)
* How features influence decision-making in different cases (row[20])
* 
![features influence decision-making](https://snipboard.io/AlDuRv.jpg)
---
### Reference
[1] https://towardsdatascience.com/shap-explained-the-way-i-wish-someone-explained-it-to-me-ab81cc69ef30

[2] https://stats.stackexchange.com/questions/558060/range-of-values-for-hyperparameter-fine-tuning-in-random-forest-classification
