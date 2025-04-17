# simple_sales_report summary using SQLite & Python

## Project Summary

This project demonstrates how to build a mini **sales analysis tool** using only Python and SQLite , without any external database setup. It showcases how to use SQL inside Python to extract key insights from a database and visualize them with simple plots.

Key operations include:
- Creating a local SQLite database
- Running SQL queries inside Python using `sqlite3`
- Using `pandas` to handle query results
- Plotting total revenue per product using `matplotlib`

This is a great beginner-friendly project that blends SQL, Python, and data visualization in one compact workflow.

---
## Project Objective

- Create a sample SQLite database called `sales_data.db`
- Run SQL queries to calculate:
  - Total quantity sold per product
  - Total revenue per product
- Display the output using `print` and visualize with a simple bar chart
- Save the visualization as an image (`sales_chart.png`)

---
## Tools & Libraries Used

- Python 3.x
- SQLite (via `sqlite3`)
- pandas
- matplotlib
---
## Steps of Workflow

1. **Create the SQLite Database**
   - Used `sqlite3.connect()` to create a database file `sales_data.db`.
   - Created a table named `sales` with fields: `id`, `product`, `quantity`, `price`.

2. **Insert Sample Sales Data**
   - Inserted a few rows of dummy data representing product sales.

3. **Run SQL Query from Python**
   - Queried total quantity and revenue per product using:
     ```sql
     SELECT product, SUM(quantity) AS total_qty, SUM(quantity * price) AS revenue
     FROM sales
     GROUP BY product;
     ```

4. **Load Results with pandas**
   - Fetched the query result using `pd.read_sql_query()`.

5. **Print the Output**
   - Displayed the results in a clean table format using `print(df)`.

6. **Create a Simple Bar Chart**
   - Used `matplotlib` to plot `product` vs `revenue`.

7. **Save the Chart**
   - Exported the bar chart as `sales_chart.png` using `plt.savefig()`.

 ---


