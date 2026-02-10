# Box-Office-Market-Analysis
## Project Overview

As the demand for original video content continues to grow, our company is preparing to enter the film industry by launching a new movie studio but the company currently lacks industry experience and clear insight into what drives film success at the box office.This project analyzes various film industry datasets to uncover trends that can guide a company's strategic entry into the entertainment industry
to provide practical, data-driven insights that can guide the company's decisions. The findings will help the stakeholders identify which types of films to prioritize, understand audience preferences, and allocate resources more effectively to improve the chances of box office success and long-term sustainability.
Analysing  box office trends for actionable film production insights.

Using data from **Box Office Mojo** and **IMDb**, the analysis identifies which movie genres generate the highest revenue, what factors influence box office success, and how budget size relates to profitability and risk. The goal is to provide **actionable, data-backed recommendations** that minimize financial risk while maximizing return on investment.



##  Objectives
### Main Objective
The main objective of this project is to analyze box office performance data in order to understand which types of films are most financially successful and use these insights to support strategic decision-making for a new movie studio.

This project aims to:
- Look at how box office revenue varies across different movie genres.
- Understand the relationship between movie ratings and box office performance.
- Identify key features of successful films, including genre, release timing, and runtime.
- Observe how movie performance has changed over time to gain insight into audience preferences.



##  Stakeholders
The **Primary stakeholders** include studio executives, producers, and investors who will use the findings to determine which film genres and production strategies are most likely to succeed at the box office.

**Secondary stakeholders** such as marketing and distribution teams will use the insights to plan promotion and release strategi


# Data Understanding
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



# Data Cleaning & Preparation
- Loaded datasets 
- Replace missing values using median 
- Converted revenue columns to numeric formats
- Merged datasets into a unified analytical table
- Created total gross revenue (domestic + foreign)
- Applied log transformations to handle skewed distributions



##  Data Analysis

## Genre-based revenue comparison

![Top 8 Genres](<images/Top Performing Genres by Revenue.png>)

Adventure, action, drama have the highest gross

Drama and comedy is highly watched but dont generate high revenues


## Trend analysis over time

![Top performing genres over years](<images/Top Genres by Revenue Over years.png>)

**Adventure** and **Action** dominate revenue throughout, with Adventure generally leading


## Budget vs revenue and ROI analysis

![alt text](<images/Average Investment vs. Market Return by Genre.png>)

In many high-performing films, foreign gross exceeds domestic gross


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


##  Key Findings

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

#### 1. Establish a market presence by prioritizing low budget films(High ROI)

Horror films show consistently low production budgets relative to other genres.Despite lower budgets, horror achieves high total gross relative to cost resulting in the highest median ROI among all genres.
Revenue distributions for horror are less volatile than action or adventure films,several horror titles achieved strong foreign gross performance, even without blockbuster-level budgets

#### Interpretation
Require less upfront capital
Generate disproportionately high returns
Expose the studio to lower downside risk
From a financial perspective, this makes horror the most capital-efficient genre in the dataset.

#### Business rationale
For a new studio with limited capital maximizing ROI is more important than maximizing raw revenue as Lower-budget productions reduce the probability of losses.

Conclusion:
Horror films provide the optimal entry strategy for capital accumulation and risk control, as supported by their superior ROI profile in your analysis.

#### 2.Scale Into High-Budget Genres After Stability (Action, Adventure, Sci-Fi)

Action, Adventure, and Sci-Fi generate the highest total box office revenue.However, these genres also exhibit:
Very high production budgets
Large variance in outcomes (both extreme successes and failures)
ROI for high-budget films is significantly lower and more volatile than for low-budget genres.
Several high-budget films failed to recoup proportional returns despite strong marketing.

### Interpretation
High revenue does not imply high efficiency,the findings show that blockbuster genres are Capital-intensive and Risk-heavy

Conclusion:
Delaying high-budget blockbusters until financial stability is achieved is justified by the high risk and low efficiency observed in the budget–ROI analysis.

#### 3. Design films for global audiences

Strong positive correlation (≈ 0.81) between domestic and foreign gross revenue indicate that successful films are rarely domestic-only successes

In many high-performing films, foreign gross exceeds domestic gross.

Genres with universal themes (Action, Adventure, Horror) perform consistently well internationally.

Total gross is driven more by global appeal than domestic success alone.


 Conclusion:
Designing films for global appeal is essential, as international markets are a primary contributor to total revenue according to the findings.




## Tools & Libraries
- Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy)
- SQLite
- Jupyter Notebook
- Tableau (for dashboarding and executive reporting)

## Tableau dashboard visualizations
[Interactive Dashboard](https://public.tableau.com/views/Box-Office-Market-Analysis/BuildingtheNextMajorMovieStudio?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)