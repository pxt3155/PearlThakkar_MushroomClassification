# Mushroom Classification Project
This project analyzes a mushroom dataset to classify whether a mushroom is edible or poisonous based on its features.

## Overview
In this project, I worked with a mushroom classification dataset to predict whether a mushroom is edible or poisonous based on its features. I started by exploring the dataset to understand the structure and identify important patterns. A key feature 'odor' was used to then create a baseline. I trained Logistic Regression and Decision Tree models using all features to compare their performance with the baseline. Both models achieved perfect accuracy on the test data, showing that the dataset is highly structured and that combining features leads to better predictions.

Overall, this project focuses on understanding the data, building a simple baseline, and then using machine learning models to improve and confirm the results.

## Dataset
Kaggle dataset : https://www.kaggle.com/datasets/uciml/mushroom-classification?select=mushrooms.csv

The dataset has 8124 mushrooms and 22 features, and everything is categorical (no numeric values).

## Problem Setup
- Input: mushroom features (odor, cap-shape, gill-color, etc.)
- Output: class (edible = e, poisonous = p)

## Initial Observations
When I first explored the dataset, I noticed that most features had multiple categories, but one feature stood out a lot — **odor**.
Some odor types were almost always poisonous, while others were almost always edible, so I decided to test that first.

<img width="565" height="354" alt="image" src="https://github.com/user-attachments/assets/f1228f74-a96f-4123-8524-35e9c1362fb9" />


---

## Baseline (Simple Rule)
I created a simple rule using only the odor feature.

This alone gave me about **98.52% accuracy**, which showed that the dataset is highly structured.

---

## Machine Learning Models

### Logistic Regression
Since all features were categorical, I converted them into binary columns.

After training the model:
- Accuracy = **100%**


### Decision Tree
I also trained a decision tree to see how it makes decisions.

- Accuracy = **100%**

<img width="654" height="361" alt="image" src="https://github.com/user-attachments/assets/cea876c6-6e29-4a41-a1db-003090ab6202" />


The tree confirmed what I saw earlier, that odor is one of the first splits, but it also uses other features like spore-print color and stalk features.

---

## Manual Rule Attempt
I tried writing a manual rule using if-else statements (mainly based on odor).

That only got about **80% accuracy**. This shows that while odor is very strong, the full models combine multiple features to get a better idea of the overall results.

---

## Comparison

| Method | Accuracy |
|--------|--------|
| Odor Rule | 98.52% |
| Logistic Regression | 100% |
| Decision Tree | 100% |

<img width="533" height="334" alt="image" src="https://github.com/user-attachments/assets/1544537d-2014-4c3d-b898-10138d32b135" />


---

## Key Takeaways

- Odor is clearly the most important feature
- Even a simple rule works really well
- Combining features using ML gives much better classification

One important takeaway for me was that doing simple analysis first (like checking one feature at a time) actually helped a lot before jumping into models.

---

## Files
- `Pearl Thakkar - Mushroom Classification.ipynb` : detailed notebook with all code and outputs
