# 🛒 Capstone Project: End-to-End Retail Data Pipeline with Airflow, Python, and PostgreSQL

## 📘 Overview
This project builds a complete **data pipeline** using **Apache Airflow**, **PostgreSQL**, **Python**, and **Matplotlib** to automate the process of extracting order data, calculating daily revenue, and visualizing sales trends.

The pipeline is orchestrated in Airflow with three key stages:
1. **Fetch Order Data** → Extract data from PostgreSQL and store it as a CSV file.
2. **Process Daily Revenue** → Calculate daily total revenue using Pandas.
3. **Plot Daily Revenue** → Generate a visual trend chart of daily sales revenue.

---

## 🧠 Key Objectives
- Demonstrate data engineering skills using Airflow for scheduling and orchestration.  
- Practice ETL concepts (Extract, Transform, Load).  
- Build automated workflows for analytics.  
- Generate insights from retail sales data.

---

## 🧰 Tools & Technologies Used
- **Python** 🐍  
- **Apache Airflow** (workflow orchestration)  
- **PostgreSQL** (data source)  
- **Pandas** (data manipulation)  
- **Matplotlib** (data visualization)  

---

## 📁 Project Structure
```bash
data-engineering-portfolio/
│
├── airflow_dags/
│   ├── daily_sales_revenue_analysis.py   # The main Airflow DAG script
│
├── airflow_output/
│   ├── daily_sales_data.csv              # Extracted order data
│   ├── daily_revenue.csv                 # Aggregated daily revenue
│   ├── daily_revenue_plot.png            # Visualization of daily sales
│
└── README.md
```

---

## ⚙️ How to Install Dependencies

Before running the DAG, ensure you have the required dependencies installed:

```bash
pip install apache-airflow pandas matplotlib psycopg2-binary
```

## 🚀 How to Run the DAG

1. Place the DAG file (`daily_sales_revenue_analysis.py`) inside your Airflow `dags/` directory.  

2. Make sure your Airflow environment is running:  
   ```bash
   airflow webserver -p 8080
   airflow scheduler

3. Open the Airflow Web UI in your browser:
   ```bash
   http://localhost:8080

4. Locate the DAG named `daily_sales_revenue_analysis`.
     - Turn it ON to enable scheduling.
     - Click Trigger DAG ▶️ to run it manually.
  
5. Monitor the DAG run in the Airflow UI.
   When it completes successfully, check your `airflow_output`/ folder for:
      - `daily_sales_data.csv` → extracted order data
      - `daily_revenue.csv` → aggregated revenue data
      - `daily_revenue_plot.png` → generated visualization
