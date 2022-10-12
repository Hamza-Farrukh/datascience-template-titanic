Titanic Survival- Overview
==========================

- Created a generalized template for the Machine Learning problems using sklearn pipelines and column transformer
- Engineered features to make the data more readable and useful
- Created pipelines and column transformer using sklearn
- Selected a Model and the parameters of the pipeline using the GridSearchCV
- Optimized the model using the GridSearchCV

----
Installation
------------
Following will be required to use the 
**Python version:** 3.10   
**Packages:** numpy, pandas, matplotlib, seaborn, sklearn, pickle, os   
**Data Source:** https://www.kaggle.com/competitions/titanic/data

---
Project Structure
--------------------

    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    └── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.

--------
Data Information
--------------------
The data had the following columns:   
- PassengerId
- Survived
- Pclass
- Name
- Sex
- Age
- SibSp
- Parch
- Ticket
- Fare
- Cabin
- Embarked

---
Exploratory Data Analysis 
-------------------------
I looked at the distributions of the data for various variables. Here are the few highlights from the analysis:

![alt text](reports/figures/age_dist.png "Age Distribution")
![alt text](reports/figures/fare_dist.png "Fare Distribution")
![alt text](reports/figures/pclass_hist.png "Pclass Histogram")
![alt text](reports/figures/correlation_heatmap.png "Correlation")

---
Model Building
--------------
I created the following Column Transformer pipelines to handle the data preprocessing:

![alt text](reports/figures/preprocessing_pipeline.png "Preprocessing Pipeline")

Then, I attached the Logistic Regression pipeline to the preprocessing pipeline and got the following:

![alt text](reports/figures/model_pipeline.png "Model Pipeline")

After this, I used the GridSearchCV to try out various preprocessing techniques and model algorithms and got the following model as the result:

![alt text](reports/figures/best_estimator.png "Best Estimator")

And then, I used the GridSearchCV to search through the various parameters to optimize the model.

---
Model Performance
-----------------
Here is how the model performed:

![alt text](reports/figures/initial_performance.png "Performance")

![alt text](reports/figures/confusion_matrix.png "Confusion Matrix")

---
License
-------
![License](https://spdx.org/licenses/MIT.html "LICENSE")
