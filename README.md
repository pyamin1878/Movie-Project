# Movie-Project
## Business Understanding
Our company has decided to create a new movie studio, we are tasked with providing actionable insights into what types of films have done historically well at the box office as well as deciding what films to create.

> What defines success for a film?
- Box office Revenue
- ROI (Return on Investement)
- Positive Reviews
- Social and Cultural Impact
> Questions to be addressed in our analysis 

- What defines success for a film- does popularity equate to profitability?
- What type of films have historically seen the greatest ROI?
- Do higher production budgets lead to higher revenues?

## Data Understanding
We were given 5 raw datasets from [IMDb](https://www.imdb.com/), [Box Office Mojo](https://www.boxofficemojo.com/), [The numbers](https://www.the-numbers.com/), [TMDB](https://www.themoviedb.org/), and [Rotten Tomatoes](https://www.rottentomatoes.com/) located in the [Data](https://github.com/pyamin1878/Movie-Project/tree/main/Data) directory. 

From these datasets the ones that proved most insightful for our analysis were from IMDb and The Numbers. IMDb contained a [SQL](https://docs.python.org/3/library/sqlite3.html) database with plenty of data points on movies and ratings. The Numbers on the otherhand displayed financials such as worldwide gross, budget, and other financial metrics. 

In our combined dataset we ended up analyzing 1490 movies
## Data Prep & Cleaning
![Alt text](Images/IMDB_ERD.jpeg)

- Two sets of data are extracted from IMDb: `movie_basics` (basic movie information) and `movie_ratings` (ratings and votes).
These datasets are then combined into a single DataFrame (a tabular data structure), focusing on titles, runtime, genres, ratings, and votes.

- This dataset is read and processed to extract budget, gross revenue, and release dates.

- The release dates are converted to a date format, and a new column for the year is created.

- Monetary values (like budget and revenue) are converted from text to numeric values for analysis.

- A new column for 'Return on Investment' (ROI) is created to evaluate the financial performance of the movies.
### Merging the Data
- The cleaned IMDb and The Numbers data are merged based on movie titles and release years to create a comprehensive dataset.
- Unnecessary columns are dropped, and the data is cleared of any missing values.
- The data is sorted based on ROI in descending order.

### Cleaned Data

## Analyses + Results/Recommendations 

### Recommendation 1

**Genre**: 

Focus on producing a movie that blends horror, mystery, and thriller genres. This combination has been identified as having the highest Return on Investment, making it a safe bet for the studio's initial projects and satisfying stakeholders.

![Alt text](Images/genres.png)

### Recommendation 2

**Runtime**: 

Runtime recommendation: Aim for a movie runtime of under 2 hours. This length aligns with audience preferences, ensuring broader appeal and impact.

![Alt text](Images/runtime_new.png)

### Recommendation 3

**Budget**: 

Adopt a low-budget strategy, focusing on movies that require minimal investment but yield high ROI. This approach reduces financial risk and fosters creativity in storytelling.

![Alt text](Images/budget_new.png)

## Conclusions and Next Steps

## Repo Structure 
```
├── Data
├── Images
├── Notebooks
│   ├── 
│   ├── 
├── .gitignore
├── Final.ipynb
├── LICENSE
├── README.md
```
