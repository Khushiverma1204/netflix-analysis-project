# Netflix Content Analysis

Analysis of Netflix's movie and TV show catalog using Python, SQL, and data visualization to uncover content trends.

## Tools Used
- Python (Pandas, NumPy)
- SQLite (SQL queries)
- Matplotlib (visualization)
- Jupyter Notebook

## Dataset
Netflix Movies and TV Shows dataset (Kaggle) — 8,807 titles with details on type, director, cast, country, release year, rating, and genre.

## Process
1. **Data Cleaning**: Handled missing values — filled `director`, `cast`, `country` with "Unknown" (30%, 9%, 9% missing respectively) rather than dropping rows, to preserve data for other analyses. Dropped rows with missing `date_added`, `rating`, `duration` (under 0.2% of data — negligible impact).
2. **SQL Analysis**: Loaded cleaned data into SQLite, wrote queries to analyze content type distribution, top content-producing countries, release trends by year, and rating distribution.
3. **Visualization**: Built charts with Matplotlib to visualize each finding.

## Key Findings
- Movies outnumber TV Shows roughly 2.4 to 1 (~6,000 vs ~2,500).
- The US leads content production among the top 10 countries; Egypt has the lowest count within that top 10.
- Content additions peaked in 2018; 2012 had the lowest count (236 titles) in the dataset.
- TV-MA is the dominant content rating (3,000+ titles), indicating the catalog skews toward mature content. NC-17 and UR are the rarest ratings (3 titles each).

## How to Run
1. Clone this repo
2. Install dependencies: `pip install pandas matplotlib`
3. Run `netflix_analysis.ipynb` in Jupyter Notebook