🎬 Movie Data Analysis

Exploratory Data Analysis of 19,808 MoviesA Python-based exploratory data analysis project on a movie dataset containing 19,808 movies and 14 attributes. The project uses Pandas, Matplotlib, and Seaborn to clean the dataset, explore movie trends, analyze ratings, votes, revenue, genres, actors, directors, and answer business-oriented questions.

📊 Dataset

The dataset contains the following columns:

id — Movie identifier

name — Movie title

year — Release year

rating — Movie rating

certificate — Certification

duration — Movie duration

genre — Movie genre(s)

votes — Number of votes

gross_income — Gross income

directors_id — Director identifier(s)

directors_name — Director name(s)

stars_id — Actor/Star identifier(s)

stars_name — Main stars

description — Movie description

The original dataset contains 19,808 rows and 14 columns. After cleaning, year, rating, duration, votes, and gross_income are numeric fields, while the remaining fields are categorical/text fields.

🧹 Data Cleaning

The project performs several preprocessing operations:

Duration

Values such as:

175 min
87 min
127 min

are converted into numeric minute values.

Votes

Comma separators are removed and the column is converted to integers:

df["votes"] = df["votes"].str.replace(",", "")
df["votes"] = df["votes"].astype(int)

Gross Income

Currency symbols and formatting characters are removed before converting the column to floating-point values:

df["gross_income"] = df["gross_income"].str.replace(",", "")
df["gross_income"] = df["gross_income"].str.replace("M", "")
df["gross_income"] = df["gross_income"].str.replace("$", "")
df["gross_income"] = df["gross_income"].astype(float)

The dataset contains no missing values, and the duplicate check returned 0 duplicate rows.

🔎 Exploratory Data Analysis

The project explores:

Movie rating distribution

Release year vs. rating

Gross income distribution

Vote distribution

Most frequent actors

Rating, votes, and gross-income correlations

Numeric feature correlations

Genre-level performance

Director performance

Certificate-level revenue and duration

Movie industry revenue by year

📈 Visualizations

The notebook creates multiple visualizations, including:

Rating distribution histogram

Year vs. rating scatter plot

Gross income and votes box plots

Top-actor charts

Correlation heatmaps

Numeric feature correlation heatmap

Other analysis-specific plots

💡 Key Analysis

Hidden Gems

Movies with relatively high ratings but comparatively low numbers of votes are investigated as potential "hidden gems."

Overhyped Movies

Movies with lower ratings but high vote counts or high gross income are analyzed to identify potentially overhyped movies.

Genre Analysis

The project calculates average ratings and average gross income across genres.

The dataset analysis reports:

Documentary as the highest-average-rated genre in one genre-level analysis, with an average rating of about 7.19.

Music, Romance, Sci-Fi as the genre combination with the highest average gross in the analysis, at approximately 209.73 million.

Highest-Grossing Director

Based on total gross income in this dataset:

Steven Spielberg is identified as the highest-grossing director, with a reported total gross of approximately $4.25 billion.

Votes vs. Gross Income

The correlation between votes and gross income is approximately:

0.63

This indicates a moderate positive relationship in this dataset.

Highest Revenue Year

The analysis identifies:

2021

as the year with the highest total industry revenue in the dataset, with reported total revenue of approximately:

$20.45 billion

Sequel Effect

Movies identified as sequel-like titles had a higher average gross income in this analysis:

Movie Type

Average Gross Income

Non-sequel

16.09 million

Sequel-like

25.45 million

This is an observed relationship in the dataset, not proof that being a sequel directly causes higher revenue.

🎯 Business-Oriented Questions

The project goes beyond basic EDA and investigates questions such as:

Which movies can be considered hidden gems?

Which movies appear overhyped?

Which actors appear most frequently?

Which genres have the highest ratings?

Which genres generate the highest average gross?

Which director has the highest total gross?

How does certification relate to gross income?

Are movie ratings improving over time?

Which actor appears in the most movies?

What is the relationship between votes and gross income?

Which director-actor combination appears most frequently?

Which year generated the highest total revenue?

Which genre performs best for debut directors?

Which director has the highest hit rate?

Do sequel-like movies earn more?

What movie characteristics could be considered when deciding what type of movie to fund?

🛠️ Technologies Used

Python

Pandas — data loading, cleaning, transformation, grouping and analysis

Matplotlib — visualization

Seaborn — statistical visualization

Jupyter Notebook / Google Colab

▶️ How to Run

1. Install dependencies

pip install pandas matplotlib seaborn

2. Place the dataset in the project directory

The notebook expects:

movies.csv

3. Load the dataset

import pandas as pd

df = pd.read_csv("movies.csv")

4. Run the notebook

Execute the cells sequentially to reproduce the data cleaning, exploratory analysis, visualizations, and business questions.

📁 Project Structure

movie-data-analysis/
│
├── movies.csv
├── movie_analysis.ipynb
└── README.md

📌 Conclusion

This project demonstrates an end-to-end exploratory data analysis workflow:

Raw Movie Dataset
        ↓
Data Inspection
        ↓
Data Cleaning
        ↓
Missing & Duplicate Checks
        ↓
Exploratory Data Analysis
        ↓
Visualization
        ↓
Correlation Analysis
        ↓
Business-Oriented Insights

The analysis shows how movie metadata such as ratings, votes, revenue, genre, year, actors, directors, and certification can be explored to identify trends and support data-driven movie-industry questions.

👨‍💻 Project Type

Exploratory Data Analysis (EDA) / Data Analytics

Built with Python and the Pandas, Matplotlib, and Seaborn ecosystem.
