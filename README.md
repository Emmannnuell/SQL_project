# Online Book Platform Analysis: Catalog Optimization & Customer Insights (SQL & Pandas) 📚

## 🎯 The Challenge
In digital entertainment and e-commerce platforms, data-driven decisions are vital for keeping users engaged. This project simulates a real-world case study analyzing a digital bookstore's relational database. The strategic objective was to extract actionable insights regarding catalog distribution, content volume per publisher, author ratings, and the behavioral patterns of highly active customers ("Power Users") to guide the Product and Content teams' strategic planning.

## 🛠️ The Process
I designed a fully automated and reproducible data pipeline that bridges relational databases with Python analytics:

* **Data Architecture & Tooling:** Leveraged **Python 3.12** and **Pandas** for data manipulation, using **SQLAlchemy** to establish seamless connection strings with a local **SQLite** database engine, ensuring full project portability.
* **Relational Database Modeling:** Worked with an interconnected 5-table ecosystem: `books` (central catalog), `authors`, `publishers`, `ratings`, and `reviews` (qualitative feedback).
* **Advanced Query Engineering:** Crafted optimized SQL scripts utilizing advanced relational logic—such as Common Table Expressions (**CTEs / `WITH` clauses**), **`HAVING`** filters, conditional aggregations, and multi-table **`LEFT JOIN`** operations—to prevent redundant subqueries and minimize data retrieval times.

## 📈 Strategic Metrics & Queries Resolved
Through targeted SQL execution, I successfully modeled and resolved the following core business requirements:

1. **Catalog Timeline Filter:** Isolated and counted books published after January 1, 2000, to evaluate modern inventory growth.
2. **Engagement Performance Per Asset:** Calculated the exact review volume and the average customer rating for every individual book in the database.
3. **Content Leadership Identification:** Located the leading publisher specializing in high-density content (books exceeding 50 pages) to determine key inventory suppliers.
4. **Author Quality Benchmark:** Identified the highest-rated author by applying a **`HAVING`** clause to filter out outliers and focus exclusively on writers with a statistically significant review volume.
5. **Power User Behavioral Analysis:** Determined the average number of text reviews authored by the platform's most active clients ("Power Users") using a **`WITH` (CTE)** block combined with a **`LEFT JOIN`**.

> **🚀 Engineering & Reproducibility Note:** To ensure this repository is completely autonomous and executable out-of-the-box, the notebook includes a pipeline that automatically initializes the SQLite database and populates the tables with structural sample data, allowing the advanced queries to run in real time.

## 📂 Repository Structure
* `analisis_libros_sql.ipynb`: Complete Jupyter Notebook documenting the ETL workflow, database connection strings, and the execution of advanced SQL queries.
* `database/`: Local SQLite relational database file containing the schema definitions and populated sample datasets.
