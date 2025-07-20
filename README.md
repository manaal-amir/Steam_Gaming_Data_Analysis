# Steam Gaming Data Analysis


This project explores and analyzes Steam game data to uncover patterns in pricing, genres, and player reviews. It also applies machine learning models to predict game popularity and player ratings.  

The goal is to demonstrate how **data science and machine learning** can support decision-making in the gaming industry, such as optimizing pricing strategies and understanding player preferences.

---

## Dataset

The dataset was sourced from [Steam](https://store.steampowered.com/) and contains information about thousands of games, including:  

- `price`: Discounted price of the game  
- `all_reviews`: Player reviews (numeric and text)  
- `genre`: Game genres (e.g., Action, Strategy, Indie)  
- `release_date`, `developer`, `publisher` and more  

---

## Process

### 1️⃣ Data Cleaning
- Removed duplicates and rows with missing critical values.  
- Cleaned the `price` column (removed `$` symbols and converted to numeric).  
- Extracted numeric ratings from `all_reviews`.  
- Parsed multiple genres from the `genre` field.  

---

### 2️⃣ Exploratory Data Analysis (EDA)
- **Price Distribution:** Most games are priced low or free, with a few expensive outliers.  
- **Top 5 Genres:**  
  🎨 Indie, ⚔️ Action, 🧭 Adventure, 🕹️ Casual, 🧠 Strategy.  
- **Correlation Heatmap:** Minimal correlation between price and rating.

---

### 3️⃣ Hypothesis Testing
- **T-Test (Free vs Paid Games):**  
  *Result:* No significant difference in ratings between free and paid games.  
  (*T = -0.04, P = 0.9651*)  

- **ANOVA (Across Top Genres):**  
  *Result:* Significant differences in ratings between genres.  
  (*F = 5.41, P = 0.0002*)  

- **Pearson Correlation (Price vs Rating):**  
  🔗 *Result:* No meaningful correlation.  
  (*r = 0.01, P = 0.6559*)  

---

### 4️⃣ Machine Learning Models
- **Classification Model:** Predicted if a game is "popular" (above median rating).  
  *Random Forest Classifier achieved 100% accuracy.*  
  *Feature importance:* Ratings dominate prediction; price has minimal influence.

- **Regression Model:** Predicted numeric player ratings.  
  *Result:* Extremely low RMSE (0.0), likely due to dataset characteristics or overfitting.  

---

## Key Findings

1. **Indie games dominate the Steam platform**, making them crucial for trend analysis.  
2. **Price has little to no correlation with user ratings** – expensive games are not always better reviewed.  
3. **Genre affects ratings** significantly, with certain genres receiving consistently higher/lower ratings.  
4. **Ratings are the strongest predictor of game popularity**, while price contributes minimally.  

These insights can guide developers and publishers in pricing strategies, genre focus, and marketing decisions.

---

## Skills Demonstrated
- Data Cleaning & Preprocessing

- Exploratory Data Analysis (EDA)

- Statistical Hypothesis Testing (T-Test, ANOVA, Pearson correlation)

- Machine Learning (Classification & Regression)

- Data Visualization (Seaborn, Matplotlib)

