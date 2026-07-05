# predict-blood-donations
# Predict Blood Donations 🩸

**Internship Project — MedTourEasy (Data Analyst Trainee, 2021)**

A machine learning model that predicts the probability of a person donating blood again, helping blood banks and hospitals plan supply ahead of time instead of relying on manual guesswork.

## 🚩 Problem

Blood demand fluctuates throughout the year — for example, donations slow down during holiday seasons. Without a reliable forecast, hospitals struggle to keep an adequate supply on hand. Manually predicting who is likely to donate again is difficult and doesn't scale.

## 🎯 Objectives

- Build a model to evaluate and predict the likelihood of future blood donations
- Remove the need for manual, guesswork-based donation predictions
- Make the model usable in real-world blood donation camps and hospitals

## 🛠️ Tools & Tech Stack

- **Environment:** Anaconda, Jupyter Notebook
- **Language:** Python 3.9
- **Libraries:** Pandas, NumPy, Scikit-learn, TPOT (automated model selection)

## 🧭 Approach (Waterfall Model)

1. **Understanding the problem** — defining what "future donation" means and why it matters
2. **Requirements gathering** — identifying the data needed
3. **Data collection & inspection** — loading and exploring the blood transfusion dataset
4. **Feature engineering** — creating the target column, checking class balance, log-normalizing skewed features
5. **Model selection** — using TPOT for automated pipeline/model selection
6. **Training & testing** — splitting data into train/test sets and training a logistic regression model
7. **Evaluation** — measuring performance using AUC score

## 📊 Results

- TPOT-selected pipeline achieved an **AUC score of 0.7850**
- Log-normalizing the training data improved AUC by an additional **~0.5%**
- This outperformed a naive baseline (always predicting "no donation"), which would only match the ~76% class distribution
- Logistic regression was chosen for its **interpretability** — it's possible to see how much each feature contributes to the prediction

## 📁 About the Data

The dataset tracks donor transfusion history (recency, frequency, monetary value, and time since first donation) and whether the donor gave blood again in a given period.

## 🔗 References

- [Give Life: Predict Blood Donations dataset & notebook reference](https://github.com/Raspiani/Give-Life-Predict-Blood-Donations)
- [Red Cross: History of Blood Transfusion](https://www.redcrossblood.org/donate-blood/blood-donation-process/what-happens-to-donated-blood/blood-transfusions/history-blood-transfusion.html)

---

*Completed as part of a Data Analyst Trainee internship at MedTourEasy, April 2021.*
