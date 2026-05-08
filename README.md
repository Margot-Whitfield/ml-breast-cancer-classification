# Breast Cancer Diagnosis Using Machine Learning
This project was completed for **INF2179H: Machine Learning with Applications in Python**  
Instructor: Mehdi Ataei  

## Group Members:  
- Franklin Li  
- Margot Whitfield  

## Project Overview
This project compares multiple machine learning models for breast cancer diagnosis using the UCI Wisconsin Diagnostic Breast Cancer dataset.
We evaluate models based on their ability to correctly identify malignant cases, with a strong emphasis on **recall**, since false negatives (missing a malignant tumor) carry significant clinical risk.

## Objective
To compare the predictive performance of different machine learning approaches in a high-stakes medical classification task.

Models included:
- Logistic Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting  
- XGBoost  
- Neural Network  

## Evaluation Metric
The primary evaluation metric is **Recall**, due to its importance in minimizing false negatives in cancer diagnosis.

While precision is also considered, recall is prioritized because failing to detect cancer has more severe consequences than false alarms.

## Rational

### Tree-Based Models
- Handle non-linear relationships effectively  
- Do not require feature scaling  
- Robust to multicollinearity  
- Strong performance on tabular medical datasets  

### Logistic Regression
- Provides a simple, interpretable baseline  
- Assumes linear relationships between features and outcome  
- Requires feature scaling  

### Neural Network
- Captures complex, non-linear patterns  
- Requires scaling and hyperparameter tuning  
- Less interpretable but flexible  
- May be limited by dataset size  

## Dataset
- UCI Wisconsin Diagnostic Breast Cancer dataset  
- 569 samples total  
  - 212 malignant (37%)  
  - 357 benign (63%)  
- Stratified sampling used to preserve class distribution  

## Methodology
- Stratified train-test split  
- Feature scaling where required  
- Grid search with 5-fold cross-validation (non-neural models)  
- Optimization based on recall  
- Feature importance analysis for interpretability  

## Results
| Model                | Precision | Recall | F1 Score | Accuracy |
|---------------------|----------|--------|----------|----------|
| Logistic Regression | 100.00   | 97.62  | 98.80    | 99.12    |
| Neural Network      | 100.00   | 97.62  | 98.80    | 99.12    |
| XGBoost             | 97.50    | 92.86  | 95.12    | 96.49    |
| Random Forest       | 100.00   | 90.48  | 95.00    | 96.49    |
| Gradient Boosting   | 100.00   | 90.48  | 95.00    | 96.49    |
| Decision Tree       | 97.37    | 88.10  | 92.50    | 94.74    |

## Insights
- Logistic Regression and Neural Networks achieved the highest recall
- Tree-based models provided strong interpretability via feature importance
- Perimeter Worst and Concave Points were dominant predictive features
- Ensemble models improved robustness but slightly reduced recall compared to simpler models

## Clinical Relevance
Reducing false negatives is critical in breast cancer diagnosis. High-recall models can help:
- Improve early detection rates  
- Reduce missed malignant cases  
- Support radiologists in decision-making  
- Enhance screening efficiency  

## Technologies 
- Python  
- Scikit-learn  
- XGBoost  
- Pandas, NumPy  
- Matplotlib 

## References
Dataset: UCI Machine Learning Repository  
- Wisconsin Diagnostic Breast Cancer Dataset
