# 📊 Netflix Movies and TV Shows Data Analysis (SQL | PostgreSQL)

This project showcases an in-depth SQL-based analysis of Netflix's catalog of movies and TV shows using PostgreSQL. The dataset contains over 8,800 titles and is publicly available on Kaggle.

## 🗂️ Dataset Overview

- **Source**: [Kaggle - Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **Files Used**:
  - `netflix_titles.csv` – The main dataset used for analysis
  - `project_netflix.sql` – SQL script containing table creation, data analysis queries, and insights

## 📐 Schema

```sql
CREATE TABLE netflix (
  show_id       VARCHAR(5),
  type          VARCHAR(10),
  title         VARCHAR(250),
  director      VARCHAR(550),
  casts         VARCHAR(1050),
  country       VARCHAR(550),
  date_added    VARCHAR(55),
  release_year  INT,
  rating        VARCHAR(15),
  duration      VARCHAR(15),
  listed_in     VARCHAR(250),
  description   VARCHAR(550)
);
```

## 🔍 Key Analyses Performed

1. **Movie vs TV Show count**
2. **Most frequent rating per type**
3. **All movies released in a specific year (e.g., 2020)**
4. **Top 5 countries with the most content**
5. **Longest movie on Netflix**
6. **Content added in the last 5 years**
7. **All content by director ‘Rajiv Chilaka’**
8. **TV shows with more than 5 seasons**
9. **Genre-wise content count**
10. **Top 5 years with highest average content release from India**
11. **All movies categorized as Documentaries**
12. **Content with missing director information**
13. **Movies featuring actor Salman Khan in the last 10 years**
14. **Top 10 most featured actors in Indian content**
15. **Categorization of content into “Good” or “Bad” based on keywords in descriptions (`kill`, `violence`)**

## 💡 Tools & Technologies

- **PostgreSQL**
- **pgAdmin / SQL Workbench**
- **Excel** (for initial inspection)
- **Git & GitHub** (for version control)

## 📁 Project Structure

```
📦 Netflix_SQL_Project
├── project_netflix.sql         # All SQL queries and logic
├── netflix_titles.csv          # Raw dataset from Kaggle
└── README.md                   # Project overview and documentation
```

## 🚀 Getting Started

1. Clone this repository
2. Load the `netflix_titles.csv` into a PostgreSQL-compatible table as per the schema
3. Run the queries from `project_netflix.sql` to explore the insights

## 📌 Notes

- Some columns like `country`, `listed_in`, and `casts` contain multiple comma-separated values. These were split using `string_to_array()` and `unnest()` in PostgreSQL for accurate aggregation.
- Date parsing is handled with `TO_DATE()` based on the format 'Month DD, YYYY'.

## 📸 Sample Output Snippets

- Most frequent content rating for Movies vs TV Shows
- Genre distribution across the platform
- Longest movie titles and duration
- Year-wise trends in Indian content publication

## 📬 Contact

If you have any questions or suggestions, feel free to reach out via GitHub Issues or connect on [LinkedIn](https://www.linkedin.com).

---

⭐ *Don’t forget to star this repository if you found it helpful!*
