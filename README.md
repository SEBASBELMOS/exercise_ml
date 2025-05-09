# **Exercise in class - ML**  💻

## **Overview**

This repository contains the solution to an in-class machine learning exercise using an e-commerce dataset from Mercado Libre Argentina (MLA). The objective is to preprocess a dataset of product listings, conduct exploratory data analysis (EDA), and train a machine learning model to predict whether a product is new or used (`condition`). The project covers data cleaning, feature engineering, model training, and evaluation, with deliverables organised in Jupyter notebooks and a clean dataset.

## **Dataset**

The dataset (`MLA_100k.jsonlines`) comprises 100,000 product listings with 48 features, including:

- **Target Variable**: `condition` (new or used)

- **Key Features**: `price`, `accepts_mercadopago`, `listing_type_id`, `free_shipping`, `local_pick_up`, `mode`, `initial_quantity`, `available_quantity`, `status`, `automatic_relist`, `buying_mode`.

- **Format**: JSON Lines, with structured fields (e.g. shipping)

## Project Structure

| Folder/File            | Description |
|------------------------|------------|
| **data/**             | Data used in the project (ignored in .gitignore) |
| **docs/**              | Documentation, Guides and workshop PDFs |
| **model/**              | AI Model |
| **notebooks/**        | Jupyter Notebooks |
| ├── 01_EDA.ipynb | Exploratory Data Analysis  |  
| ├── 02_model-training.ipynb   | Model Selection and Training   | 
| **requirements.txt**             | Libraries and modules used in the project | 
| **README.md**         | This file |

---

## Installation and Setup

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/SEBASBELMOS/exercise_ml.git
    cd exercise_ml
    ```

2. **Installing the dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3. **Execution**
    Run all the notebooks to create the EDA, transformations and model.
    
---

## **Results**

**Model Performance Metrics:**

| Model              | Accuracy | Precision | Recall  | F1-Score | ROC-AUC |
|--------------------|----------|-----------|---------|----------|---------|
| Logistic Regression| 0.748981 | 0.884574  | 0.528232| 0.661464 | 0.859171|
| Random Forest      | 0.824252 | 0.778080  | 0.869405| 0.821211 | 0.904274|
| XGBoost            | 0.829937 | 0.809726  | 0.828330| 0.818922 | 0.915702|
| Gradient Boosting  | 0.820377 | 0.803846  | 0.810989| 0.807402 | 0.909765|
| KNN                | 0.811874 | 0.783764  | 0.821394| 0.802138 | 0.884308|

- **Accuracy:** Overall correctness.

- **Precision:** Accuracy of positive predictions.

- **Recall:** Ability to find all positives.

- **F1-Score:** Balance of precision and recall.

- **ROC-AUC:** Overall ability to distinguish classes ("New" vs. "Used.").

## **Conclusion**

Among the evaluated models, XGBoost achieved the best performance with an accuracy of 0.8299 and a ROC-AUC of 0.9157, indicating strong predictive capability in distinguishing product conditions. Random Forest and Gradient Boosting also performed well, with accuracies above 0.82, while Logistic Regression lagged behind due to its lower recall and F1-score. 

The results highlight the effectiveness of ensemble methods for this classification task. The final XGBoost model has been saved for deployment, offering a practical solution for e-commerce product classification.

---

## **Author**  
Created by **Sebastian Belalcazar Mosquera**. Connect with me on [LinkedIn](https://www.linkedin.com/in/sebasbelmos/) for feedback, suggestions, or collaboration opportunities!

---