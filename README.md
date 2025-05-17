

# 🎵 Music Store Analysis Using SQL

This project involves analyzing a digital music store database using **Structured Query Language (SQL)** to extract meaningful insights from sales, customer behavior, genres, artists, and employee performance.

The dataset used in this analysis resembles the structure of a real-world music store like iTunes, and it provides a great opportunity to practice **data querying**, **aggregation**, and **insight generation** using SQL.

---

## 📊 Objective

To analyze the digital music store data by answering business questions and deriving actionable insights through optimized SQL queries. Key areas of focus include:

- Sales and revenue trends
- Customer purchasing behavior
- Genre and artist popularity
- Employee performance
- Geographic distribution of sales

---
## Database and Tools
* Postgre SQL
* PgAdmin4

Schema- Music Store Database  
![MusicDatabaseSchema](https://user-images.githubusercontent.com/112153548/213707717-bfc9f479-52d9-407b-99e1-e94db7ae10a3.png)

## 🗂️ Dataset Overview

The dataset includes the following relational tables:

| Table Name     | Description                              |
|----------------|------------------------------------------|
| `Customers`    | Stores customer details                  |
| `Invoices`     | Records of purchases                     |
| `Invoice_Items`| Tracks individual items sold             |
| `Tracks`       | Details about each song                  |
| `Albums`       | Albums and their associated tracks       |
| `Artists`      | Artist information                       |
| `Genres`       | Types of music genres                    |
| `Employees`    | Employee details and roles               |

---

## 🛠️ Tools & Technologies Used

- **SQL** (tested on PostgreSQL / MySQL / SQLite)
- **DB Browser for SQLite / pgAdmin / MySQL Workbench**
- **ERD (Entity Relationship Diagram)** for schema understanding

---

## 🔍 Key Analyses Performed

- Top 5 selling artists
- Most popular music genre by country
- Monthly revenue trends
- Top customers based on total spending
- Employee-wise sales performance
- Average invoice amount by country
- Track-wise sales ranking
- Customer retention metrics

---

### 🧪 Sample SQL Query

```sql
SELECT 
    c.FirstName || ' ' || c.LastName AS Customer_Name, 
    SUM(ii.UnitPrice * ii.Quantity) AS Total_Spent 
FROM Customers c 
JOIN Invoices i ON c.CustomerId = i.CustomerId 
JOIN Invoice_Items ii ON i.InvoiceId = ii.InvoiceId 
GROUP BY Customer_Name 
ORDER BY Total_Spent DESC 
LIMIT 10;
```

---

## 📈 Key Insights

- **Rock** is the most popular genre globally.
- The **USA** generates the highest revenue, followed by Canada and France.
- A small number of **top customers** contribute significantly to total sales.
- Sales tend to **spike during holiday seasons**.
- A few **artists generate the majority of revenue**.

---

## 📁 Project Structure

```
SQL_Music_Store_Analysis-main/
│
├── Music Store Analysis-Questions.pdf   # Business questions to be answered
├── MusicDatabaseSchema.png              # Entity Relationship Diagram (ERD)
├── Music_Store_Query.sql                # SQL queries for analysis
├── Music_Store_database.sql             # Database schema and data
├── album2.csv                           # Supporting CSV file
├── music store data.zip                 # Compressed dataset
├── Raw-Music Store Analysis-SQL Project.zip
└── README.md                            # Project documentation

---

## 🤝 Contributions

Contributions, suggestions, and improvements are welcome!  
Feel free to open an issue or submit a pull request.

---

## 📬 Contact

If you have any questions or need clarification regarding this project, feel free to reach out at:

📧 Email: firdousanjum620@gmail.com  
📍 Location: Bhubaneswar, Odisha, India

---

## 🚀 Let’s Connect!
