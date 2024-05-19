# Atelier 3
## Part 1

### Skip Gram Embedding:

- **SVR**:
  - MSE: 1.488
  - MAE: 0.834
  - Cross-Validation MSE: 1.400
  - Cross-Validation MAE: 0.819

- **Linear Regression**:
  - MSE: 1.142
  - MAE: 0.805
  - Cross-Validation MSE: 1.454
  - Cross-Validation MAE: 0.938

- **Decision Tree**:
  - MSE: 1.860
  - MAE: 0.928
  - Cross-Validation MSE: 2.382
  - Cross-Validation MAE: 1.065

### CBOW Embedding:

- **SVR**:
  - MSE: 1.716
  - MAE: 0.884
  - Cross-Validation MSE: 1.511
  - Cross-Validation MAE: 0.815

- **Linear Regression**:
  - MSE: 1.144
  - MAE: 0.804
  - Cross-Validation MSE: 1.451
  - Cross-Validation MAE: 0.934

- **Decision Tree**:
  - MSE: 1.720
  - MAE: 0.913
  - Cross-Validation MSE: 2.315
  - Cross-Validation MAE: 1.081

### Overall Comparison:

- **SVR**:
  - Performs similarly between Skip Gram and CBOW embeddings.
  - Slightly lower errors for Skip Gram.
  - More stable performance across different folds (lower variance) indicated by similar MSE and MAE between validation and test sets.

- **Linear Regression**:
  - Performs better with Skip Gram embeddings.
  - Higher variance between validation and test sets compared to SVR.

- **Decision Tree**:
  - Performs better with Skip Gram embeddings.
  - Higher variance between validation and test sets compared to SVR.

### Conclusion Part 1:

- **SVR** seems to be the most stable model with consistent performance across both embedding methods.
- **Linear Regression** and **Decision Tree** show higher variance in performance, with Skip Gram embeddings generally yielding better results.
- Consider the specific requirements of your task (interpretability, computational resources, etc.) when selecting the best model for your application.


## Part 2

### Skip Gram Embedding && Model Performance Summary:

### Logistic Regression
**Accuracy:** 0.355

**Classification Report:**
```
               precision    recall  f1-score   support

  Irrelevant       0.00      0.00      0.00       172
    Negative       0.31      0.68      0.43       266
     Neutral       0.46      0.30      0.36       285
    Positive       0.39      0.32      0.35       277

    accuracy                           0.35      1000
   macro avg       0.29      0.32      0.28      1000
weighted avg       0.32      0.35      0.31      1000
```

### Decision Tree
**Accuracy:** 0.866

**Classification Report:**
```
               precision    recall  f1-score   support

  Irrelevant       0.85      0.89      0.87       172
    Negative       0.86      0.89      0.87       266
     Neutral       0.88      0.84      0.86       285
    Positive       0.87      0.86      0.86       277

    accuracy                           0.87      1000
   macro avg       0.87      0.87      0.87      1000
weighted avg       0.87      0.87      0.87      1000
```

### Naive Bayes
**Accuracy:** 0.269

**Classification Report:**
```
               precision    recall  f1-score   support

  Irrelevant       0.00      0.00      0.00       172
    Negative       0.27      0.99      0.42       266
     Neutral       0.00      0.00      0.00       285
    Positive       0.71      0.02      0.04       277

    accuracy                           0.27      1000
   macro avg       0.25      0.25      0.11      1000
weighted avg       0.27      0.27      0.12      1000
```

### Conclusion Part 2:
Based on the performance metrics, the Decision Tree model significantly outperformed both the Logistic Regression and Naive Bayes models in terms of accuracy and f1-score across all classes. The Decision Tree achieved an accuracy of 86.6% and consistently high precision, recall, and f1-scores for all sentiment categories. In contrast, Logistic Regression and Naive Bayes struggled particularly with the "Irrelevant" and "Neutral" classes, showing poor precision and recall. 

Therefore, for this sentiment analysis task using Skip-Gram embeddings, the Decision Tree model is the most effective, providing the best balance between precision and recall across all sentiment categories.

## What I Learned During This Lab:
- Text Embeddings
- Skip-Gram Embeddings
- Continuous Bag of Words (CBOW) Embeddings
## Conclusion

Through this lab, I gained a comprehensive understanding of how to use text embeddings and Word2Vec. I learned the differences between Skip-Gram and CBOW embeddings, the process of averaging embeddings for sentence-level representations, and how to evaluate and compare the performance of various machine learning models. This knowledge is fundamental for tackling a wide range of NLP tasks and effectively leveraging textual data in machine learning applications.
