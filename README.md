<h1 align="center">🎬 IMDB Movies Analysis</h1>

<p align="center">
  Exploratory data analysis of the 1,000 most popular IMDB movies from 2006 to 2016 using Python
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/Seaborn-Visualization-4C8CBF" alt="Seaborn">
  <a href="https://www.kaggle.com/PromptCloudHQ/imdb-data"><img src="https://img.shields.io/badge/Dataset-Kaggle-20BEFF?logo=kaggle&logoColor=white" alt="Kaggle"></a>
</p>

## 📌 Overview

This project explores the **IMDB Movie Data** dataset from Kaggle: the 1,000 most popular movies on IMDB between 2006 and 2016. It checks data quality, answers questions about ratings, revenue, votes, runtime, directors and genres with Pandas, and visualizes the results with Matplotlib and Seaborn.

---

## ⚡ At a Glance

| 🎞️ Movies | 📅 Years Covered | 🎭 Unique Genres | 💥 Action Movies |
|:---:|:---:|:---:|:---:|
| **1,000** | **2006 – 2016** | **20** | **303** |

---

## 🔄 Workflow

1. **Load & Inspect** – Reviewed the first and last rows, shape and data types (`head()`, `tail()`, `shape`, `info()`).
2. **Check Quality** – Found missing values in `Revenue (Millions)` and `Metascore`, and no duplicate rows.
3. **Analyze** – Used `groupby()`, `nlargest()`, filtering and string operations to answer the questions below.
4. **Feature Engineering** – Added a `Classify Rates` column that labels each movie by rating.
5. **Visualize** – Built bar plots, count plots and scatter plots with Seaborn.

> **Columns:** `Rank` · `Title` · `Genre` · `Description` · `Director` · `Actors` · `Year` · `Runtime (Minutes)` · `Rating` · `Votes` · `Revenue (Millions)` · `Metascore`

---

## 🧹 Data Quality

| Column | Non-null values | Missing |
|---|:---:|:---:|
| `Revenue (Millions)` | 872 | 128 |
| `Metascore` | 936 | 64 |
| All other columns | 1,000 | 0 |

Dropping every row with a missing value would leave **838** movies. **No duplicate rows** were found.

---

## 🔍 Key Findings

| Question | Result |
|---|---|
| Movies with runtime ≥ 180 minutes | The Wolf of Wall Street · The Hateful Eight · La vie d'Adèle · Grindhouse · Inland Empire |
| Longest movies | **Grindhouse** (191 min) · **The Hateful Eight** (187 min) |
| Year with the highest average votes | **2012** (≈ 285,226 votes per movie) |
| Year with the highest average revenue | **2009** (≈ $112.6M per movie) |
| Year with the highest average rating | **2007** (≈ 7.13) |
| Year with the lowest average rating | **2016** (≈ 6.44) |
| Highest average director rating | **Nitesh Tiwari** (8.8), then **Christopher Nolan** (≈ 8.68) |
| Highest revenue movie | **Star Wars: Episode VII - The Force Awakens** ($936.63M) |
| Number of Action movies | **303** |

**Top 10 highest revenue movies**

| # | Movie | Revenue (Millions) |
|:---:|---|:---:|
| 1 | Star Wars: Episode VII - The Force Awakens | 936.63 |
| 2 | Avatar | 760.51 |
| 3 | Jurassic World | 652.18 |
| 4 | The Avengers | 623.28 |
| 5 | The Dark Knight | 533.32 |
| 6 | Rogue One | 532.17 |
| 7 | Finding Dory | 486.29 |
| 8 | Avengers: Age of Ultron | 458.99 |
| 9 | The Dark Knight Rises | 448.13 |
| 10 | The Hunger Games: Catching Fire | 424.65 |

**Top 10 highest rated movies**

| # | Movie | Director | Rating |
|:---:|---|---|:---:|
| 1 | The Dark Knight | Christopher Nolan | 9.0 |
| 2 | Inception | Christopher Nolan | 8.8 |
| 3 | Dangal | Nitesh Tiwari | 8.8 |
| 4 | Interstellar | Christopher Nolan | 8.6 |
| 5 | Kimi no na wa | Makoto Shinkai | 8.6 |
| 6 | The Intouchables | Olivier Nakache | 8.6 |
| 7 | The Prestige | Christopher Nolan | 8.5 |
| 8 | The Departed | Martin Scorsese | 8.5 |
| 9 | The Dark Knight Rises | Christopher Nolan | 8.5 |
| 10 | Whiplash | Damien Chazelle | 8.5 |

**Movies per year**

| 2006 | 2007 | 2008 | 2009 | 2010 | 2011 | 2012 | 2013 | 2014 | 2015 | 2016 |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 44 | 53 | 52 | 51 | 60 | 63 | 64 | 91 | 98 | 127 | **297** |

**Movies per genre** (a movie can have several genres)

| Genre | Movies | Genre | Movies |
|---|:---:|---|:---:|
| Drama | **513** | Romance | 141 |
| Action | 303 | Sci-Fi | 120 |
| Comedy | 279 | Horror | 119 |
| Adventure | 259 | Mystery | 106 |
| Thriller | 195 | Fantasy | 101 |
| Crime | 150 | Biography | 81 |

The remaining genres are Family (51), Animation (49), History (29), Sport (18), Music (16), War (13), Western (7) and Musical (5).

---

## 🏷️ Rating Classes

Each movie is labeled by its rating:

| Class | Rule |
|---|---|
| **Excellent** | Rating ≥ 8 |
| **Good** | Rating ≥ 6 and < 8 |
| **Average** | Rating < 6 |

---

## 📊 Visualizations

| Plot | Shows |
|---|---|
| Bar plot | Average votes by year |
| Bar plot | Average revenue by year |
| Bar plot | Top 10 movies by runtime |
| Count plot | Number of movies per year |
| Bar plot | Top 10 movies by revenue |
| Bar plot | Top 10 rated movies, colored by director |
| Scatter plot | Rating vs. revenue |
| Scatter plot | Votes vs. rating |

## 👩‍💻 Author

**Marwa Samy** · [GitHub](https://github.com/marwa23-rgb)
