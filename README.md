# Content_Monetization_Modeler
Content_Monetization_Modeler_ad_Revenue

# 📺 Content Monetization Modeler

> **Predicting YouTube Ad Revenue using Machine Learning**

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?style=flat-square&logo=scikit-learn)
![Streamlit](https://img.shields.io/badge/Streamlit-App-red?style=flat-square&logo=streamlit)
![Pandas](https://img.shields.io/badge/Pandas-Data-green?style=flat-square&logo=pandas)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

---

## 📌 Project Overview

The **Content Monetization Modeler** is an end-to-end machine learning project that predicts YouTube ad revenue based on video performance metrics, audience engagement, and demographic data. It includes full exploratory data analysis, preprocessing, feature engineering, model training, evaluation, and an interactive **Streamlit web application** for real-time predictions.

---

## 🎯 Problem Statement

Content creators on YouTube often struggle to understand what drives their ad revenue. This project answers the question:

> *"Given a video's performance metrics, how much ad revenue can a creator expect to earn?"*

---

## 📊 Dataset

| Property | Value |
|---|---|
| Records | 122,400 rows |
| Features | 12 columns |
| Target Variable | `ad_revenue_usd` |
| Missing Values | ~5% in `likes`, `comments`, `watch_time_minutes` |
| Duplicates | 2,400 rows (~2%) |

### Features

| Column | Type | Description |
|---|---|---|
| `video_id` | String | Unique video identifier |
| `date` | Date | Upload/report date |
| `views` | Integer | Total views |
| `likes` | Float | Total likes |
| `comments` | Float | Total comments |
| `watch_time_minutes` | Float | Total watch time |
| `video_length_minutes` | Float | Video duration |
| `subscribers` | Integer | Channel subscribers |
| `category` | String | Gaming, Tech, Music, Education, Entertainment, Lifestyle |
| `device` | String | Mobile, Desktop, Tablet, TV |
| `country` | String | US, IN, CA, UK, DE, AU |
| `ad_revenue_usd` | Float | **Target — Ad revenue in USD** |

---

## 🗂️ Project Structure

```
content-monetization-modeler/
│
├── 📓 content_monetization_modeler.ipynb   ← Full ML notebook (run this first)
├── 🐍 app.py                               ← Streamlit web application
├── 📄 README.md                            ← You are here
│
├── 📁 model/                               ← Auto-created after running notebook
│   ├── best_model.pkl
│   ├── scaler.pkl
│   └── feature_columns.pkl
│
└── 📊 youtube_ad_revenue_dataset.csv       ← Dataset
```

---

## 🔧 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/content-monetization-modeler.git
cd content-monetization-modeler
```

### 2. Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn streamlit joblib jupyter
```

---

## 🚀 How to Run

### Step 1 — Run the Jupyter Notebook
```bash
jupyter notebook content_monetization_modeler.ipynb
```
Run all cells top to bottom. This will:
- ✅ Perform full EDA
- ✅ Clean and preprocess the data
- ✅ Engineer new features
- ✅ Train 5 regression models
- ✅ Evaluate and compare all models
- ✅ Save the best model to `model/` folder

### Step 2 — Launch the Streamlit App
```bash
streamlit run app.py
```
Open your browser at: **http://localhost:8501**

---

## 🤖 Models Trained

| Model | Type |
|---|---|
| Linear Regression | Baseline |
| Ridge Regression | Regularized Linear (L2) |
| Lasso Regression | Regularized Linear (L1) |
| Random Forest | Ensemble — 100 trees |
| Gradient Boosting | Ensemble — Sequential boosting |

### Evaluation Metrics Used
- **R²** — Proportion of variance explained
- **RMSE** — Root Mean Squared Error
- **MAE** — Mean Absolute Error

---

## 🛠️ Feature Engineering

| New Feature | Formula | Purpose |
|---|---|---|
| `engagement_rate` | (likes + comments) / views | Audience interaction quality |
| `avg_watch_time` | watch_time_minutes / views | Avg retention per viewer |
| `like_ratio` | likes / views | Proportion of viewers who liked |
| `month` | Extracted from date | Seasonal revenue patterns |

---

## 📱 Streamlit App

The web app has **3 tabs:**

| Tab | Description |
|---|---|
| 🔮 Prediction | Input video metrics → get instant revenue prediction |
| 📊 EDA Dashboard | Revenue distributions, category comparisons, heatmaps |
| 📈 Model Insights | Feature importance chart + key findings |

---

## 💡 Key Insights

1. 🥇 **`watch_time_minutes` is the #1 revenue driver** — correlation ~0.99
2. ⚠️ **Views ≠ Revenue** — raw views have only ~0.04 correlation
3. 📊 **Engagement matters** — higher engagement attracts better quality ads
4. 🌍 **US & CA viewers** generate slightly higher CPM rates
5. 📱 **Mobile viewers** generate marginally more revenue
6. 🌲 **Tree-based models** outperform linear models for this dataset

---

## 📦 Dependencies

```
pandas
numpy
matplotlib
seaborn
scikit-learn
streamlit
joblib
jupyter
```

---

## 🙌 Acknowledgements

- Dataset used for academic and learning purposes
- Built with [Scikit-learn](https://scikit-learn.org), [Streamlit](https://streamlit.io), and [Pandas](https://pandas.pydata.org)

---

## 📜 License

This project is licensed under the MIT License.

---

<p align="center">Made with ❤️ for Content Creators & Data Science</p>
