# customer_behavior_analysis
Data analytics project using Python, SQL and Power BI
> An end-to-end analysis of [dataset topic], from raw data to business insights, using Python, SQL, and Power BI.

![Dashboard Preview](images/dashboard_preview.png)

---

## Table of Contents

1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Tools & Technologies](#tools--technologies)
4. [Project Steps](#project-steps)
5. [Dashboard](#dashboard)
6. [Results & Key Insights](#results--key-insights)
7. [Project Structure](#project-structure)
8. [How to Run](#how-to-run)
9. [Deliverables](#deliverables)
10. [Author](#author)

---

## Overview

**Business problem:** [One or two sentences on the question this project answers. Example: "Which products and regions drive the most revenue, and where are we losing customers?"]

**Objective:** Turn raw data into clear, actionable insights by:

- Cleaning and exploring the data in Python
- Querying it with SQL to answer business questions
- Visualizing findings in an interactive Power BI dashboard
- Communicating results through a written report and presentation

---

## Dataset

| Item | Details |
|------|---------|
| **Source** | [Kaggle / company data / public API, with link] |
| **Size** | [e.g., 50,000 rows × 15 columns] |
| **Time period** | [e.g., Jan 2022 – Dec 2023] |
| **Format** | CSV |

**Key columns:**

| Column | Description |
|--------|-------------|
| `order_id` | Unique order identifier |
| `order_date` | Date the order was placed |
| `customer_id` | Unique customer identifier |
| `product_category` | Category of the product |
| `sales` | Revenue from the order |
| `region` | Customer region |

*(Replace with your actual columns.)*

---

## Tools & Technologies

| Category | Tools |
|----------|-------|
| **Programming** | Python (Pandas, NumPy, Matplotlib, Seaborn) |
| **Database** | PostgreSQL / MySQL / SQL Server *(keep the one you used)* |
| **Visualization** | Power BI |
| **Reporting** | Microsoft Word / PDF, PowerPoint |
| **Environment** | Jupyter Notebook, Git & GitHub |

---

## Project Steps

### 1. Data Loading
Loaded the dataset into Python using Pandas and checked its structure, data types, and size.

### 2. Exploratory Data Analysis (EDA)
- Reviewed summary statistics and distributions
- Identified trends, outliers, and correlations
- Created charts to understand patterns in the data

### 3. Data Cleaning
- Handled missing values and removed duplicates
- Fixed data types and inconsistent formats
- Treated outliers and created new features where needed (e.g., month, profit margin)
- Exported the cleaned dataset for SQL and Power BI

### 4. SQL Analysis
Loaded the cleaned data into [PostgreSQL / MySQL / SQL Server] and wrote queries to answer key business questions, using:

- Aggregations and `GROUP BY`
- Joins and subqueries
- CTEs and window functions

**Example query:**

```sql
-- Top 5 product categories by revenue
SELECT product_category,
       SUM(sales) AS total_revenue
FROM orders
GROUP BY product_category
ORDER BY total_revenue DESC
LIMIT 5;
```

*(Use `TOP 5` instead of `LIMIT 5` on SQL Server.)* All queries are in the [`sql/`](sql/) folder.

### 5. Power BI Dashboard
Connected Power BI to the cleaned data, built a data model, created DAX measures, and designed an interactive dashboard.

### 6. Report & Presentation
Summarized the methodology, findings, and recommendations in a written report and a PowerPoint deck for non-technical stakeholders.

---

## Dashboard

The interactive dashboard includes:

- **KPI cards:** Total Sales, Profit, Orders, Average Order Value
- **Trend analysis:** Performance over time
- **Breakdowns:** By category, region, and customer segment
- **Filters:** Date, region, and category slicers

![Dashboard Screenshot](images/dashboard_full.png)

📁 File: [`powerbi/dashboard.pbix`](powerbi/dashboard.pbix)

---

## Results & Key Insights

1. **[Insight 1]:** e.g., "Technology products generate 40% of revenue but only 25% of orders."
2. **[Insight 2]:** e.g., "Sales peak in Q4, with a 35% increase over the yearly average."
3. **[Insight 3]:** e.g., "The West region has the highest revenue, while the South has the lowest profit margin."
4. **[Insight 4]:** e.g., "Discounts above 30% lead to negative profit."

**Recommendations:**

- [Actionable recommendation based on Insight 1]
- [Actionable recommendation based on Insight 2]
- [Actionable recommendation based on Insight 3]

---

## Project Structure

```
project-name/
│
├── data/
│   ├── raw_data.csv
│   └── cleaned_data.csv
│
├── notebooks/
│   ├── 01_eda.ipynb
│   └── 02_data_cleaning.ipynb
│
├── sql/
│   ├── create_tables.sql
│   └── analysis_queries.sql
│
├── powerbi/
│   └── dashboard.pbix
│
├── reports/
│   ├── project_report.pdf
│   └── presentation.pptx
│
├── images/
│   └── dashboard_preview.png
│
├── requirements.txt
└── README.md
```

---

## How to Run

### Prerequisites

- Python 3.9+
- PostgreSQL / MySQL / SQL Server
- Power BI Desktop (Windows)

### 1. Clone the repository

```bash
git clone https://github.com/your-username/project-name.git
cd project-name
```

### 2. Set up the Python environment

```bash
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Run the notebooks

```bash
jupyter notebook
```

Open and run in order:
1. `notebooks/01_eda.ipynb`
2. `notebooks/02_data_cleaning.ipynb`

### 4. Set up the database

1. Create a new database (e.g., `analytics_db`).
2. Run `sql/create_tables.sql` to create the tables.
3. Import `data/cleaned_data.csv` into the table.
4. Run the queries in `sql/analysis_queries.sql`.

### 5. Open the dashboard

1. Open `powerbi/dashboard.pbix` in Power BI Desktop.
2. If prompted, update the data source path or database connection.
3. Click **Refresh** to load the data.

---

## Deliverables

| Deliverable | Link |
|-------------|------|
| 📊 Power BI Dashboard | [`powerbi/dashboard.pbix`](powerbi/dashboard.pbix) |
| 📄 Project Report | [`reports/project_report.pdf`](reports/project_report.pdf) |
| 🖥️ Presentation | [`reports/presentation.pptx`](reports/presentation.pptx) |




3. **[Insight 3]:** e.g., "The West region has the highest revenue, while the South has the lowest profit margin."
4. **[Insight 4]:** e.g., "Discounts above 30% lead to negative profit."
