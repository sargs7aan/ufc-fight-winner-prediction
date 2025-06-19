# 🥊 UFC Fight Winner Prediction

This project uses machine learning models to predict the winner of UFC fights based on pre-fight statistics like fighter height, reach, win streak, and historical performance.

---

## 📂 Dataset

The dataset includes detailed statistics for both fighters in each match, including:

- Physical attributes (age, height, reach, weight)
- Average past performance (knockdowns, strikes, takedowns)
- Opponent-related stats (e.g., how often they get hit)
- Metadata (title fight status, weight class, number of rounds)
- Match outcome (Red or Blue corner win)

---

## 🎯 Project Goal

The main goal is to build a model that can predict the **winner of a fight**:
- `1` → Red fighter wins
- `0` → Blue fighter wins

---

## 🧠 Machine Learning Models Used

I trained multiple models to compare performance:

- **Logistic Regression**
- **Random Forest**
- **XGBoost**

To deal with class imbalance (more Red wins), I used:
- `class_weight='balanced'` for logistic regression and random forest
- `scale_pos_weight` in XGBoost

---

## 📊 Evaluation Metrics

Each model was evaluated using:
- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix (implicitly via classification report)

Example performance (balanced models):
| Model               | Accuracy |
|---------------------|----------|
| Random Forest (balanced) | ~0.65 |
| XGBoost (balanced)       | ~0.63 |

---

## 📈 Feature Engineering

I also experimented with engineered features like:
- Combining fighter and opponent averages
- Differences in reach, height
- Win/loss streaks

---

## 📉 Visualizations

- Class distribution (to show imbalance)
- XGBoost feature importance

---

## 🚀 How to Run

You can run this project in **Google Colab** or Jupyter Notebook.

1. Clone the repository
2. Upload the dataset (`data.csv`)
3. Run `main.ipynb`
4. (Optional) Install packages with:

```bash
pip install -r requirements.txt

