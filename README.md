# AnilyticsETL: Anime Data Processing and Insights Pipeline  

## 📌 Overview  
**AnilyticsETL** is an ETL (Extract, Transform, Load) pipeline designed to process and analyze anime-related datasets. It integrates multiple data sources, cleans and enriches them, and produces insights such as genre distributions, top anime lists, word clouds from synopses, and association rules for recommendation-like patterns.  

This project demonstrates how to combine structured and unstructured data for exploratory analysis and knowledge discovery.  

---

## 🌐 Live Demo
View the HTML version of the ETL pipeline here:  
[AnilyticsETL Demo](https://bubblipathic.github.io/AnilyticsETL/)

---

## ⚙️ Features  
- **Extract**  
  - Load datasets including anime information, user ratings, complete watch status, and detailed synopses.  

- **Transform**  
  - Clean missing/unknown values and convert data types.  
  - Merge multiple sources into a consolidated dataset.  
  - Preprocess text data (tokenization, stop word removal).  
  - Generate word frequency counts and word clouds from anime synopses.  
  - Apply association rule mining (Apriori algorithm) to discover relationships between anime genres and user ratings.  
  - Compute statistical summaries and correlations.  

- **Load**  
  - Store processed data into a **SQLite database** for easy querying.  
  - Prepare datasets for downstream visualization and analytics.  

---

## 📂 Dataset - Anime Recommendation Database 2020 by hernan4444
- `anime.csv` → General anime information (scores, popularity, etc.)  
- `anime_with_synopsis.csv` → Titles, genres, and plot synopses  
- `animelist.csv` → User ratings and watch lists  
- `rating_complete.csv` → Full dataset of ratings  
- `watching_status.csv` → User watching status categories  

👉 [Link of Dataset in Kaggle](https://www.kaggle.com/datasets/hernan4444/anime-recommendation-database-2020)

---

## 📊 Outputs & Insights  
- **Cleaned Anime Dataset** with merged synopsis and score data.  
- **Top 100 Anime** ranked by user score.  
- **Most Common Words** from synopses, visualized in word clouds.  
- **Genre & Rating Analysis** through descriptive stats and visualizations.  
- **Association Rules** to uncover patterns in anime preferences.  
- **SQLite Database** for further querying and integration.  

---

## 🚀 Technologies  
- **Python** (Pandas, NumPy, Regex, Collections)  
- **Visualization:** Matplotlib, Seaborn, WordCloud  
- **Data Mining:** MLxtend (Apriori, Association Rules)  
- **Database:** SQLite3  
- **Statistics:** SciPy (correlation, regression)  

