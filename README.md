# Mushroom Classification Project - Pearl Thakkar
This project analyzes a mushroom dataset to classify whether a mushroom is edible or poisonous based on its features.

## Dataset
Kaggle dataset : https://www.kaggle.com/datasets/uciml/mushroom-classification?select=mushrooms.csv

The dataset has 8124 mushrooms and 22 features, and everything is categorical (no numeric values).

## Problem Setup
- Input: mushroom features (odor, cap-shape, gill-color, etc.)
- Output: class (edible = e, poisonous = p)

## Initial Observations
When I first explored the dataset, I noticed that most features had multiple categories, but one feature stood out a lot — **odor**.
Some odor types were almost always poisonous, while others were almost always edible, so I decided to test that first.

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

---

## Takeaways

- Odor is clearly the most important feature
- Even a simple rule works really well
- But combining features using ML gives perfect classification

One interesting takeaway for me was that doing simple analysis first (like checking one feature at a time) actually helped a lot before jumping into models.

---

## Files
- `Pearl Thakkar - Mushroom Classification.ipynb` → full notebook with all code and outputs
