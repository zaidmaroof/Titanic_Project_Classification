# **Titanic Survival Prediction: A Machine Learning Pipeline**

## **Project Overview**

This project is a classic machine learning exercise using the renowned Titanic dataset. The primary goal was to build and evaluate classification models to predict whether a passenger survived the sinking of the Titanic based on their personal attributes.  
This notebook demonstrates the use of a modern, organized machine learning workflow, employing scikit-learn's **Pipeline** and **ColumnTransformer** functionality. As an aspiring AI/ML Engineer, my focus here was less on raw accuracy and more on building a **robust, reusable, and clean structure** for data preprocessing and model training.

## **Key Objectives and Techniques**

* **End-to-End Pipeline:** Implemented a single, cohesive Pipeline to handle all preprocessing (imputation, encoding, scaling) and modeling steps.  
* **ColumnTransformer:** Used ColumnTransformer to apply different transformation steps to different columns (e.g., numerical vs. categorical features).  
* **Hyperparameter Optimization:** Employed GridSearchCV combined with StratifiedKFold to systematically search for the best model parameters while maintaining a statistically sound cross-validation approach.  
* **Model Comparison:** Evaluated two distinct models—**Random Forest Classifier** and **Logistic Regression**—to compare their performance and, crucially, interpret their underlying feature importance.

## **Final Results**

After running the grid search and comparing the optimized Random Forest and Logistic Regression models, the best model achieved the following performance on the holdout test set:

| Model | Test Set Accuracy |
| :---- | :---- |
| **Random Forest** | 82.16% |
| **Logistic Regression** | 81.67% |

### **Insightful Finding**

While both models performed similarly, the feature importance (coefficients for Logistic Regression and feature importances for Random Forest) were vastly different. This highlights an important modeling principle: **similar performance doesn't mean similar behavior.** It suggests that a more detailed correlation analysis and potential feature engineering is needed to better understand the true predictive power of the underlying variables.

## **How to Run This Project**

### **Prerequisites**

You need Python 3.8+ installed on your system.

### **Setup**

1. **Clone the repository:**  
	```
   git clone   
   cd titanic-survival-prediction
	```
2. **Create a virtual environment (Recommended):**  
	```
   python \-m venv venv  
   source venv/bin/activate  \# On Linux/macOS  
   \# venv\\Scripts\\activate   \# On Windows
	```
3. Install dependencies:  
	```
   The necessary libraries are listed in requirements.txt.  
   pip install \-r requirements.txt
	```
4. Run the notebook:  
   Open the Jupyter Notebook and run all cells to execute the full data preparation, training, and evaluation workflow.  
   ```
   jupyter notebook "Titanic\_Project.ipynb"  
   ```
