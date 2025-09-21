# AnilyticsETL: Anime Data Processing and Insights Pipeline  

## 📌 Overview  
**AnilyticsETL** is an ETL (Extract, Transform, Load) pipeline designed to process and analyze anime-related datasets. It integrates multiple data sources, cleans and enriches them, and produces insights such as genre distributions, top anime lists, word clouds from synopses, and association rules for recommendation-like patterns.  

This project demonstrates how to combine structured and unstructured data for exploratory analysis and knowledge discovery.  

---

## 🌐 Static HTML Report
View the HTML version of the ETL pipeline here:  
[AnilyticsETL Demo](https://bubblipathic.github.io/AnilyticsETL/AnilyticsETL.html)

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

## 🚀 Tools
- **Python** (Pandas, NumPy, Regex, Collections)  
- **Visualization:** Matplotlib, Seaborn, WordCloud  
- **Data Mining:** MLxtend (Apriori, Association Rules)  
- **Database:** SQLite3  
- **Statistics:** SciPy (correlation, regression)

---

## 📈 Summary of Insights  

Through this ETL pipeline, several analyses were performed on the anime datasets to uncover patterns in viewer preferences and anime characteristics:  

### 📝 Synopsis Analysis  
**What it is:**  
- Processed and cleaned synopses from the top 100 highest-rated anime.  
- Tokenized and filtered stop words to identify the most common meaningful terms.  
- Generated frequency counts and word clouds for visual insights.  

**Findings:**  
- School-related terms (“school,” “high,” “year”) are linked to higher audience engagement, making high school settings broadly appealing.
- Epic narrative words (“one,” “all,” “must,” “become”) correlate with mainstream shounen popularity.

![Synopsis Analysis Visual](/Screenshots/Screenshot1.png)  

---

### 🎭 Genre and Drop Rate Analysis  
**What it is:**  
- Examined the relationship between **anime genres** and user engagement.  
- Looked at how often viewers dropped shows across different genres.  

**Findings:**  
- Anime with the School + Comedy + Romance mix are 3× more likely to be dropped, suggesting oversaturation and cliché storylines reduce viewer retention.
- Broad genres like Comedy, Adventure, and Fantasy alone have lower lift, suggesting they are safer but also more mainstream and competitive.

![Genre and Drop Rate Analysis Visual](/Screenshots/Screenshot2.png)  

---

### 🔗 Frequent Anime Sequences (Association Rules)  
**What it is:**  
- Applied the **Apriori algorithm** on user watchlists and ratings to discover frequent patterns.  
- Generated association rules to find which anime are often watched or liked together.  

**Findings:**  
- Long-running classics often co-occur, making them a strong backbone for recommendation engines.
- Users often consume entire franchise runs, so platforms should bundle or recommend sequels/spin-offs together.
- There are some  unexpected overlap (sci-fi thriller + school romcom) → audiences may not be limited to a single genre and can be cross-promoted to diverse titles.
- Insights suggest potential for **recommendation systems** based on frequent co-occurrence.  

![Genre and Drop Rate Analysis Visual](/Screenshots/Screenshot3.png)  



