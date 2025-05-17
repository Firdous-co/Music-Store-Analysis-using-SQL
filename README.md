🎵 Music Store Analysis using SQL
This project focuses on analyzing a digital music store database using Structured Query Language (SQL). It involves querying various aspects of the music store including customers, invoices, genres, artists, and sales data to gain valuable business insights.

📊 Objective
To extract actionable insights from a music store database by writing optimized SQL queries for:

Sales and revenue trends

Customer behavior

Popular genres and artists

Employee performance

Geographic trends

🗂️ Dataset
The dataset used in this project is a relational database modeled after a digital music store like iTunes. It includes the following tables:

Customers

Invoices

Invoice_Items

Tracks

Albums

Artists

Genres

Employees

📌 The dataset is publicly available and commonly used for SQL practice.

🛠️ Tools & Technologies
SQL (PostgreSQL / MySQL / SQLite)

DB Browser / pgAdmin / MySQL Workbench (for running queries)

ERD (Entity Relationship Diagram) for schema understanding

🔍 Key SQL Queries & Analysis Performed
Top 5 selling artists

Most popular music genre by country

Monthly revenue trend

Top customers based on total purchases

Employee-wise sales performance

Average invoice amount by country

Tracks with highest sales

Customer retention metrics

📌 Sample Query
sql
Copy
Edit
SELECT
    c.FirstName || ' ' || c.LastName AS Customer_Name,
    SUM(ii.UnitPrice * ii.Quantity) AS Total_Spent
FROM Customers c
JOIN Invoices i ON c.CustomerId = i.CustomerId
JOIN Invoice_Items ii ON i.InvoiceId = ii.InvoiceId
GROUP BY Customer_Name
ORDER BY Total_Spent DESC
LIMIT 10;
📈 Insights
Rock is the most popular genre globally.

The USA generates the highest revenue, followed by Canada and France.

Top customers are frequent buyers with higher invoice values.

Sales tend to spike during holiday seasons.

A small number of artists generate the majority of revenue.

🧩 ER Diagram

(Replace with your actual ER diagram image link if available.)

📁 Project Structure
SQL_Music_Store_Analysis-main/
│
├── Music Store Analysis-Questions.pdf         # Business questions to be answered
├── MusicDatabaseSchema.png                    # Entity Relationship Diagram (ERD)
├── Music_Store_Query.sql                      # SQL queries for analysis
├── Music_Store_database.sql                   # Database schema and data
├── album2.csv                                 # Supporting CSV file
├── music store data.zip                       # Compressed dataset
├── Raw-Music Store Analysis-SQL Project.zip   # Full raw project files
└── README.md                                  # Project documentation

🤝 Contributions
Contributions, suggestions, and improvements are welcome! Open a PR or raise an issue.
