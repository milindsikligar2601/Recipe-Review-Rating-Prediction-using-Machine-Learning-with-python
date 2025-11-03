---

## 📊 Project Overview

This project analyzes a dataset of over **18,000 recipe reviews** to predict user **star ratings (1–5)** using machine learning models.  
It explores user engagement features, identifies influential factors affecting ratings, and demonstrates predictive modeling with visual interpretation.

---

## 🎯 Objectives

1. Predict recipe review star ratings based on user and review features.  
2. Identify the most influential factors driving high or low ratings.  
3. Recommend improvements for review platforms and recipe authors.

---

## 🧾 Dataset Description

**Dataset:** `recipe_reviews_cleaned.csv`  
**Total Records:** ~18,000  

### Key Features:
| Feature | Description |
|----------|-------------|
| `likes_score` | Average likes per review |
| `dislike_index` | Ratio of dislikes to total interactions |
| `response_level` | Engagement level of the reviewer |
| `ranking_value` | Reviewer reputation or ranking |
| `vote_ratio` | Ratio of positive to negative votes |
| `region`, `device_type` | Reviewer demographics |
| `recipe_name` | Recipe title |
| `review_length`, `word_count` | Derived textual features |

---

## 🧹 Data Preparation & Cleaning

- Removed redundant index and placeholder columns.  
- Filled missing categorical values with `"Unknown"` and numeric values with median.  
- Normalized categorical values for consistency (`region`, `device_type`).  
- Converted timestamps to datetime format.  
- Derived new features: review length, word count, and likes/dislikes ratio.

---

## 📈 Exploratory Data Analysis (EDA)

Visual analyses were performed to understand data distribution and relationships:
- **Distribution of Star Ratings** — 5-star ratings dominate (imbalance issue).  
- **Correlation Heatmap** — Engagement metrics (likes, ranking value) strongly correlated with ratings.  
- **Feature Importance (Random Forest)** — Dislike index, response level, and ranking value are key predictors.  

---

## 🤖 Model Development

Two models were tested:

| Model | Description | Key Insights |
|--------|--------------|--------------|
| **Logistic Regression** | Baseline interpretable model | Biased toward 4–5 star ratings |
| **Random Forest Classifier** | Ensemble model capturing non-linear relations | Achieved better accuracy, precision, and recall |

---

## 📊 Model Evaluation

- **Logistic Regression:** Moderate accuracy, struggles with minority (1–2 star) classes.  
- **Random Forest:** Superior accuracy and F1-scores across most classes.  
- **ROC-AUC:** Random Forest achieved higher class separation.  
- **Class Imbalance:** Skewed distribution affects prediction for low ratings.

---

## 🧠 Insights & Recommendations

### Key Influential Factors
- **Dislike Index**, **Response Level**, and **Ranking Value** are most predictive.  
- High engagement and reputation metrics correlate with positive ratings.

### Recommendations
- **For Platforms:** Adjust algorithms to weigh engagement features and mitigate bias toward 5-star reviews.  
- **For Recipe Creators:** Encourage detailed and interactive reviews to improve credibility and platform visibility.

---

## ⚠️ Limitations
- Significant **class imbalance** — most reviews are 5-star.  
- Text content not deeply analyzed (no NLP-based sentiment or TF-IDF).  
- Limited diversity in user and recipe features.

---

## 🔮 Future Work
- Apply **SMOTE** or similar techniques for class balancing.  
- Use **advanced NLP models (e.g., BERT)** for sentiment analysis.  
- Include **time-based trends** for longitudinal insights.

---

## 🧰 Tools & Technologies

| Category | Tools |
|-----------|-------|
| Programming | Python (Pandas, NumPy, Scikit-learn) |
| Visualization | Matplotlib, Seaborn |
| Modeling | Logistic Regression, Random Forest |
| Reporting | Jupyter Notebook, PDF Report |

---

## 📂 Repository Contents

| File | Description |
|------|--------------|
| `Part4_final.ipynb` | Jupyter Notebook containing data cleaning, analysis, and model building |
| `Part4_Report_with_Visualization.pdf` | Final report summarizing EDA, model evaluation, and visual results |
| `recipe_reviews_cleaned.csv` | Cleaned dataset used for model training and testing |
| `README.md` | Project overview and documentation |

---

## 🏁 Conclusion

The Random Forest model successfully predicted recipe review ratings with higher accuracy and interpretability than Logistic Regression.  
Engagement-driven features proved most influential, revealing that user interaction metrics are critical in determining recipe popularity and perceived quality.

---
