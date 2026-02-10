# Box-Office-Market-Analysis
Analysing  box office trends for actionable film production insights.
#  Movie Industry Box Office Analysis  
### Data-Driven Insights for Launching a New Movie Studio

##  Project Overview
This project analyzes historical movie box office performance to support strategic decision-making for a company planning to enter the film industry by launching a new movie studio.

Using data from **Box Office Mojo** and **IMDb**, the analysis identifies which movie genres generate the highest revenue, what factors influence box office success, and how budget size relates to profitability and risk. The goal is to provide **actionable, data-backed recommendations** that minimize financial risk while maximizing return on investment.

---

##  Business Problem
A new movie studio faces significant uncertainty:
- Which genres are most profitable?
- Do higher budgets guarantee higher returns?
- How important are ratings and audience popularity?
- Should the studio focus on domestic or international markets?

This project answers these questions using exploratory data analysis, statistical testing, and financial performance metrics.

---

##  Objectives
- Compare total box office revenue across movie genres
- Analyze relationships between revenue, ratings, popularity, and runtime
- Identify genres with the highest return on investment (ROI)
- Examine revenue trends over time
- Provide business-ready recommendations for a new movie studio

---

##  Stakeholders
- Executive leadership
- Investment and finance teams
- Production and content strategy teams
- Marketing and distribution teams

---

## Data Sources

### 1. Box Office Mojo
**File:** `bom.movie_gross.csv.gz`  
- Domestic gross revenue  
- Foreign gross revenue  

### 2. IMDb Database
**File:** `im.db` (SQLite)
- `movie_basics`: titles, release year, runtime, genres
- `movie_ratings`: average ratings and number of votes
## Data Sources
  
### 3. Rotten Tomatoes
– Critics and audience scores

### 4.The Numbers
– Detailed financial and production data for movies.

### 5.The Movie Database (TMDb)
– Movie information and posters

###  Data Integration
Datasets were merged using movie titles and release years to connect financial performance with audience and content attributes.

---

##  Data Cleaning & Preparation
- Removed missing and non-numeric revenue values
- Converted revenue columns to numeric formats
- Merged datasets into a unified analytical table
- Created total gross revenue (domestic + foreign)
- Applied log transformations to handle skewed distributions

---

##  Analytical Methods
- Exploratory Data Analysis (EDA)
- Genre-based revenue comparison
- Correlation analysis
- One-way ANOVA hypothesis testing
- Trend analysis over time
- Budget vs revenue and ROI analysis

---

##  Hypothesis Testing

**Null Hypothesis (H₀):**  
Mean total box office revenue is equal across all movie genres.

**Alternative Hypothesis (H₁):**  
Mean total box office revenue differs across movie genres.

**Results:**
- F-statistic ≈ 26.26  
- p-value ≪ 0.05  

**Conclusion:**  
There is a statistically significant difference in box office revenue across movie genres.

---

##  Key Findings
# Plots

This is an example plot from my analysis:

![Top Genres by Revenue](Top Performing Genres by Revenue.png)
![Return on Investment by genre](Average Investment vs. Market Return by Genre.png)

###  Genre Performance
- **Adventure, Action, and Sci-Fi** generate the highest total revenues.
- **Drama and Comedy** have broad appeal but lower revenue efficiency.
- **Documentary, News, Sport, and War** consistently underperform financially.

###  Profitability & ROI
- **Horror films** deliver the highest ROI:
  - Low production budgets
  - Strong global performance
  - Lower financial risk
- High-budget films generate high revenue but show large variability and lower efficiency.

###  Domestic vs Foreign Markets
- Strong positive correlation between domestic and foreign revenue.
- High-performing films tend to succeed globally, not just domestically.
- Foreign markets often contribute more than 50% of total revenue.

###  Ratings & Popularity
- Audience popularity (number of votes) correlates more strongly with revenue than ratings.
- High ratings alone do not guarantee financial success.

###  Industry Trends
- Film production peaked around 2015–2016.
- Total box office revenue increased steadily until 2018, followed by a decline likely influenced by market saturation and streaming growth.



##  Business Recommendations

1. **Enter the market with low-budget horror films**  
   - Highest ROI
   - Lower financial risk
   - Ideal for building early capital

2. **Delay high-budget blockbusters**  
   - Action, Adventure, and Sci-Fi should be pursued only after financial stability is achieved.

3. **Design films for global audiences**  
   - International markets are critical revenue drivers.





## Tools & Libraries
- Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy)
- SQLite
- Jupyter Notebook
- Tableau (for dashboarding and executive reporting)

