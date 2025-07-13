# 🌍 Worldwide Travel Cities Dataset (Ratings and Climate)

This dataset includes curated information on 560 global cities, combining travel ratings, thematic tags (like beaches, culture, cuisine), budget levels, and climate data in a structured format — ideal for travel recommendation engines, statistical analysis, or machine learning projects.

---

## 📁 Dataset Overview

- **Cities:** 560
- **Continents/Regions:** Global
- **Data Type:** CSV
- **Primary Use Cases:** 
  - Travel recommendations
  - Climate-based clustering
  - User preference matching
  - Statistical testing (ANOVA, t-tests)

---

## 📊 Column Summary

| Column Name         | Type         | Description                                 |
|---------------------|--------------|---------------------------------------------|
| `id`                | Categorical  | Unique ID for each city                     |
| `city`              | Categorical  | Name of the city                            |
| `country`           | Categorical  | Country the city belongs to                 |
| `region`            | Categorical  | Geographical region (e.g., Europe, Asia)    |
| `short_description` | Categorical  | Brief textual summary of the city           |
| `latitude`          | Continuous   | Geographic latitude                         |
| `longitude`         | Continuous   | Geographic longitude                        |
| `avg_temp_monthly`  | Categorical  | Monthly average, max, and min temps (in JSON format) |
| `ideal_durations`   | Categorical  | Ideal travel durations (multi-label: "Weekend", "One week", etc.) |
| `budget_level`      | Categorical  | Estimated cost level for visiting the city  |
| `culture`           | Categorical  | Indicates strong cultural offering          |
| `adventure`         | Categorical  | Indicates potential for adventure tourism   |
| `nature`            | Categorical  | Indicates natural scenic importance         |
| `beaches`           | Categorical  | Indicates beach-related tourism             |
| `nightlife`         | Categorical  | Indicates nightlife options                 |
| `cuisine`           | Categorical  | Indicates culinary richness                 |
| `wellness`          | Categorical  | Indicates availability of wellness retreats |
| `urban`             | Categorical  | Indicates if it's an urban destination      |
| `seclusion`         | Categorical  | Indicates if the city offers seclusion      |

---

**The colab analysis contains:

-*Data Reading*

-*Data Preprocessing/cleaning*

-*Pandas Analysis*

-*Encoding*

-*Correlation Analysis*

-*Statistical Analysis*

---

## 🧩 10 Medium-Level Pandas Questions

| No. | Question                                                                 | Key Concepts Used                       |
|-----|--------------------------------------------------------------------------|------------------------------------------|
| 1   | What are the top 10 cities with the highest average temperature in July? | `.sort_values()`, `.iloc[]`, column filter |
| 2   | Count how many cities have `"culture"` and `"adventure"` tags both active. | Boolean filtering, `&` operator           |
| 3   | What is the average `avg_6` (June temperature) for cities in Europe?     | Filtering + `.mean()`                    |
| 4   | Find cities with `"Short trip"` as ideal duration and `avg_rating > 4.5`. | Boolean mask, column filtering           |
| 5   | Which country has the most cities in the dataset?                        | `.value_counts()`                        |
| 6   | List cities where max August temperature (`max_8`) exceeds 35°C.         | Conditional filtering                    |
| 7   | Count how many cities are coastal (`beaches == 1`) and also urban.       | Compound condition                       |
| 8   | What’s the average rating for cities tagged with `"wellness"`?           | Grouping or filtering + `.mean()`        |
| 9   | Create a new column: `temp_range_7` = `max_7` - `min_7`.                 | Vectorized column operation              |
| 10  | Which regions have the lowest average January (`avg_1`) temperatures?    | Grouping by region + `.mean()`           |

---

## 🧠 5 Complex Pandas Questions

| No. | Question                                                                 | Key Concepts Used                        |
|-----|--------------------------------------------------------------------------|-------------------------------------------|
| 1   | Rank cities within each region based on `avg_rating`, highest to lowest. | `.groupby()`, `.rank()`, `.sort_values()` |
| 2   | Create a heatmap DataFrame of `avg` temperatures for all 12 months for top 10 cities by rating. | `.iloc[]`, `.sort_values()`, reshaping   |
| 3   | Identify cities with stable temperatures: max monthly range (max - min) < 5°C across all months. | Row-wise operation using `.apply()`      |
| 4   | Create a city profile score combining multiple factors: rating, culture, cuisine, and budget. | Weighted scoring with normalization       |
| 5   | For each country, determine the month with the highest average temperature. | `.groupby()`, `.idxmax()`, column-wise ops |

---

## 🚀 Use Cases with This Dataset

| Use Case                                          | Description                                                                 |
|--------------------------------------------------|-----------------------------------------------------------------------------|
| 🌡️ Climate Profiling                             | Analyze how temperatures vary by city/month using 36 climate columns        |
| 📊 Preference-Based Recommendations              | Match user input (tags, climate, trip duration) with city profiles          |
| 💸 Budget-Based Clustering                       | Cluster cities by `budget_level`, climate, and `avg_rating`                |
| 🧳 Seasonality and Trip Planning                 | Suggest cities ideal for specific seasons based on monthly weather          |
| 🔍 Exploratory Data Analysis (EDA)               | Perform feature correlation, distribution analysis, and data quality checks |

---
