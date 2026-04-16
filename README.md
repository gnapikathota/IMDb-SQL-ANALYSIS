🎬 IMDb SQL Analysis Project
Data Exploration • Insights • Query Optimization • Portfolio Project

📌 Project Overview
This project analyzes the IMDb movie dataset using SQL to uncover insights about movie performance, ratings, genres, cast, and industry trends.
It demonstrates skills in data cleaning, joins, CTEs, window functions, subqueries, and analytical SQL used in real-world analytics workflows.

📂 Dataset Description
The project uses publicly available IMDb datasets (or Kaggle equivalents).
Typical tables include:

movie 

ratings 

genres 

director_mapping

role_mapping

names

🎯 Objectives
Analyze movie rating trends across years and genres

Identify top-performing actors, directors, and production teams

Explore correlations between movies, ratings

Build reusable SQL queries for analytics

Demonstrate SQL proficiency for portfolio and hiring purposes

🛠️ Tools & Technologies

SQL (MySQL)

DBMS: (Workbench)

📊 Key SQL Concepts Used
Joins (INNER)

CTEs

Window Functions (ROW_NUMBER, RANK, DENSE_RANK)

Aggregations & Grouping

Subqueries

Data Cleaning using SQL

Case statements

Query optimization techniques

📝 Project Structure
Code
📁 imdb-sql-analysis
│── 📄 README.md
│── 📄 schema_diagram.png
│── 📄 imdb_queries.sql
│── 📄 insights_summary.pdf
│── 📁 data/
│     └── *.ZIP file
🔍 Sample Insights

Action and Drama are the most frequently produced genres

Movies with >8 IMDb rating show strong clustering around specific directors

Average movie runtime has increased over the last 20 years

Top 10 actors with the highest average movie rating

Directors with the most consistently high-rated films

🧠 Example SQL Queries
1️⃣ Top 10 Highest-Rated Movies
sql
SELECT title, year, rating
FROM titles t
JOIN ratings r ON t.id = r.movie_id
WHERE r.votes > 50000
ORDER BY r.rating DESC
LIMIT 10;
2️⃣ Most Popular Genres
sql
SELECT genre, COUNT(*) AS movie_count
FROM genres
GROUP BY genre
ORDER BY movie_count DESC;
