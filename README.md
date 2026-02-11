# Movie Industry Box Office Analysis  
### Data-Driven Insights for Launching a New Movie Studio

## Project Overview
This project analyzes historical movie box office performance to support strategic decision-making for a company planning to enter the film industry by launching a new movie studio.

Using data from **Box Office Mojo**,**IMDb** and **The Numbers** the analysis identifies which movie genres generate the highest revenue, what factors influence box office success, and how budget size relates to profitability and risk. The goal is to provide **actionable, data-backed recommendations** that minimize financial risk while maximizing return on investment.


## Business Problem
- Which genres are most profitable?
- Do higher budgets guarantee higher returns?
- Should the studio focus on domestic or international markets?

This project answers these questions using exploratory data analysis, statistical testing, and financial performance metrics.



## Objectives
- Compare total box office revenue across movie genres
- Analyze relationships between revenue, ratings, popularity, and runtime
- Identify genres with the highest return on investment (ROI)
- Examine revenue trends over time
- Provide business-ready recommendations for a new movie studio



## Stakeholders
 **Primary stakeholders** 
- studio executives
- producers
- investors 

**Secondary stakeholders** 
- marketing and distribution teams 



## Data Sources

### 1. Box Office Mojo

- Domestic gross revenue  
- Foreign gross revenue  

### 2. IMDb Database

- `movie_basics`: titles, release year, runtime, genres
- `movie_ratings`: average ratings and number of votes

### 3.The Numbers
- Movie budgets

###  Data Integration
Datasets were merged using movie titles and to connect financial performance with audience and content attributes.


## Data Cleaning & Preparation
- Removed and replaced missing and non-numeric revenue values
- Converted revenue columns to numeric formats
- Merged datasets into a unified analytical table
- Created total gross revenue (domestic + foreign)
- Applied log transformations to handle skewed distributions



## Analytical Methods
- Exploratory Data Analysis (EDA)
- Genre-based revenue comparison
- Correlation analysis
- One-way ANOVA hypothesis testing
- Trend analysis over time
- Budget vs revenue and ROI analysis



##  Key Findings

### Genre Performance
- **Adventure, Action, and Sci-Fi** generate the highest total revenues.
- **Drama and Comedy** have broad appeal but lower revenue efficiency.
- **Documentary, News, Sport, and War** consistently underperform financially.

### Profitability & ROI
- **Horror films** deliver the highest ROI:
  - Low production budgets
  - Strong global performance
  - Lower financial risk
- High-budget films generate high revenue but show large variability and lower efficiency.

###  Domestic vs Foreign Markets
- Strong positive correlation between domestic and foreign revenue.
- High-performing films tend to succeed globally, not just domestically.


###  Ratings & Popularity
- Audience popularity (number of votes) correlates more strongly with revenue than ratings.
- High ratings alone do not guarantee financial success.

###  Industry Trends
- Film production peaked around 2015–2016.
- Total box office revenue increased steadily until 2018, followed by a decline likely influenced by market saturation and streaming growth.

### Key Visualizations
Below are the critical visualizations that helped provide insights into the film industry:

![Top Genres by Revenue over years](<images/Top Genres by Revenue Over years.png>)


![Return on Investment by Genre](<images/Median Return on Investment by Genre.png>)


![Average Investment return by Genre](<images/Average Investment vs. Market Return by Genre.png>)


![Median Return on Investment by Genre](<images/Median Return on Investment by Genre.png>)

##  Conclusion

The analysis demonstrates that movie genre significantly influences box office revenue, with statistically significant differences across categories. While high-budget genres such as Action and Adventure generate the largest revenues, lower-budget genres—particularly Horror—offer superior return on investment and reduced financial risk. Strong correlations between domestic and foreign revenue highlight the importance of global market strategy. Collectively, these findings suggest that new studios should prioritize capital efficiency, global appeal, and marketing-driven visibility to maximize sustainable profitability.


## Tools & Libraries
- Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy)
- SQLite
- Jupyter Notebook
- Tableau (for dashboarding and executive reporting)

## Tableau dashboard visualizations
[Interactive Dashboard](https://public.tableau.com/views/Box-Office-Market-Analysis/BuildingtheNextMajorMovieStudio?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Runtime Information
- Total notebook runtime: 50.20 seconds
- Environment: Local machine (Python 3.11)