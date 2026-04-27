# 🎬 Netflix OTT Content Analysis & Recommendation System

![Python](https://img.shields.io/badge/Python-3.11-blue?style=flat&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?style=flat&logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-red?style=flat&logo=scikit-learn)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat)

> A complete end-to-end data analysis project on Netflix's content library — including data cleaning, exploratory data analysis, trend analysis, visualizations, and a content-based recommendation system.

---

## 📌 Project Overview

This project performs a full analysis of Netflix's movies and TV shows dataset. It uncovers patterns in content type, genres, ratings, and production trends — and builds a **TF-IDF based recommendation engine** that suggests similar titles.

---

## 🖼️ Dashboard Preview

> 📊 A full 6-panel analytics dashboard is generated inside the notebook covering content split, genres, yearly trends, ratings, movie duration, and top countries.

---

## 📁 Project Structure

```
netflix-analysis/
│
├── Netflix_OTT_Analysis.ipynb   # Main Jupyter Notebook
├── netflix_titles.csv           # Dataset (download from Kaggle)
├── netflix_dashboard.png        # Auto-generated dashboard image
├── index.html                   # Exported HTML version of notebook
└── README.md                    # Project documentation
```

---

## 📊 Dataset

- **Source:** [Netflix Movies and TV Shows – Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **Size:** ~8,800 titles
- **Columns:** show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description

> ⚠️ Download `netflix_titles.csv` from Kaggle and place it in the same folder as the notebook before running.

---

## 🔍 What's Inside

### 1. Data Cleaning
- Handled missing values across all columns
- Fixed swapped `rating` and `duration` values
- Removed duplicates
- Converted `date_added` to datetime format

### 2. Feature Engineering
- Extracted `year_added` and `month_added` from date
- Created `duration_int` (numeric duration)
- Created `primary_genre` and `genres_list`

### 3. Exploratory Data Analysis
- Content type distribution (Movies vs TV Shows)
- Top 15 most popular genres
- Ratings distribution overall and by type
- Movie duration histogram
- TV Show seasons analysis

### 4. Trend Analysis
- Content added per year (stacked area chart)
- Year-over-Year growth rate
- Top genre growth trends (2013–Present)
- Monthly seasonality analysis

### 5. Advanced Visualizations
- Genre × Rating Heatmap
- Top 10 content-producing countries
- Full 6-panel analytics dashboard

### 6. Recommendation System
- Feature: TF-IDF on description + genre + rating + cast + director
- Similarity: Cosine Similarity
- Function: `recommend(title, n=5)` returns top N similar titles

---

## 🤖 Recommendation System Usage

```python
# Get top 5 recommendations for a title
recommend('Stranger Things')

# Get top 5 from same content type only
recommend('The Dark Knight', n=5, same_type=True)
```

---

## 🛠️ Tech Stack

| Library | Purpose |
|--------|---------|
| `pandas` | Data manipulation |
| `numpy` | Numerical operations |
| `matplotlib` | Visualizations |
| `seaborn` | Statistical plots |
| `scikit-learn` | TF-IDF & Cosine Similarity |

---

## ▶️ How to Run

**1. Clone the repository**
```bash
git clone https://github.com/kashvi43/netflix-analysis.git
cd netflix-analysis
```

**2. Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn notebook ipykernel
```

**3. Download the dataset**

Get `netflix_titles.csv` from [Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows) and place it in the project folder.

**4. Run the notebook**
```bash
jupyter notebook
```
Open `Netflix_OTT_Analysis.ipynb` → Run All Cells

---

## 💡 Key Business Insights

- 📺 ~70% Movies, ~30% TV Shows — but TV Shows are growing faster
- 🎭 International Movies & Dramas dominate the library
- 🔞 TV-MA is the most common rating — Netflix targets adult audiences
- 📈 Massive content surge between 2016–2019
- 🌍 USA is #1 producer; India, UK, Japan are rising markets
- 📅 July & December are peak months for content addition

---

## 🚀 Future Improvements

- Use BERT / sentence-transformers for semantic similarity
- Add collaborative filtering with user ratings
- Enrich with IMDb ratings via API
- Deploy as a Streamlit web app
- Add choropleth world map for country-wise content

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙋‍♀️ Author

**Kashvi Kaur**  
📧 kaurkashvi43@gmail.com.com  
🔗  [GitHub](https://github.com/kashvi43)

---

⭐ If you found this project helpful, please give it a star on GitHub!
