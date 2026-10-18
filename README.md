# Customer Shopping Behavior Dashboard

## Overview

The **Customer Shopping Behavior Dashboard** is an end-to-end data
analytics project that explores customer purchasing patterns and product
performance. It combines Python, PostgreSQL, and Power BI to turn raw
shopping data into insights that can support business decisions.

The project covers the full analytics workflow: loading and exploring
the dataset, cleaning and preparing data, answering business questions
with SQL, and presenting findings in an interactive dashboard and a
written report.

## Dataset

The dataset contains **3,900 purchase records** and **18 columns**
describing customers and their shopping behavior.

Key fields include:

-   **Customer details:** age, gender, and location
-   **Purchase details:** item, category, purchase amount, season, size,
    and color
-   **Shopping behavior:** subscription status, discounts, previous
    purchases, purchase frequency, review ratings, and shipping type

During preparation, missing review ratings were handled using the median
rating for each product category. Column names were standardized, and
additional features such as `age_group` and `purchase_frequency_days`
were created.

> The dataset is used for analysis and reporting. Any business
> recommendations should be validated against the actual query results
> and dashboard figures.

## Tools

-   **Python** --- data loading, exploratory data analysis (EDA), data
    cleaning, and feature engineering
-   **Pandas** --- data manipulation and analysis
-   **Jupyter Notebook** --- interactive analysis and documentation of
    the workflow
-   **PostgreSQL** --- SQL queries to investigate business questions
-   **SQLAlchemy / database connector** --- connecting Python to
    PostgreSQL
-   **Power BI** --- interactive dashboard and data visualization
-   **PDF report** --- summary of the analysis and business
    recommendations

## Project Workflow

### 1. Load the Data

Loaded the CSV dataset into Python using Pandas and reviewed its shape,
column names, data types, and sample records.

### 2. Perform EDA

Explored the data using summary statistics and category-level checks to
understand customer characteristics, purchasing patterns, and potential
data-quality issues.

### 3. Clean and Prepare the Data

-   Checked missing values and handled missing review ratings.
-   Standardized column names for easier use in Python and SQL.
-   Created useful analysis features, including age groups and
    purchase-frequency intervals.
-   Reviewed overlapping discount-related fields and removed the
    redundant `promo_code_used` field from the prepared analysis
    dataset.

### 4. Analyze with PostgreSQL

Loaded the cleaned data into PostgreSQL and used SQL queries to
investigate questions such as:

-   How does revenue compare by gender and age group?
-   How do spending patterns differ between subscribers and
    non-subscribers?
-   Which products have the highest average ratings?
-   Which products are most frequently purchased within each category?
-   How do average purchase amounts compare by shipping type?
-   Which products are most associated with discount use?
-   How can customers be grouped as new, returning, or loyal?
-   Are customers with more than five previous purchases more likely to
    subscribe?

### 5. Build the Power BI Dashboard

Created an interactive Power BI dashboard to present customer and
shopping-behavior metrics in a visual format. The dashboard helps users
explore customer segments, product categories, revenue, and subscription
status using the visuals and filters included in the report.

### 6. Prepare the Report

Created a report documenting the project, the analysis questions, the
main business areas explored, and recommendations for further
investigation.

## Dashboard

The Power BI dashboard supports exploration of:

-   Customer subscription status
-   Sales and revenue by product category
-   Sales and revenue by age group
-   Customer segment comparisons using available report filters

**Dashboard file:** Add your `.pbix` file to the project repository and
link it here, for example: `Customer_Behaviour_Dashboard.pbix`.

To make the dashboard easier for recruiters to review, consider adding a
screenshot in this README:

``` markdown
![Customer Shopping Behavior Dashboard](images/dashboard_screenshot.png)
```

## Results and Business Value

The project creates a repeatable workflow for analyzing customer
shopping data and presenting it in a business-friendly format. It helps
investigate:

-   Customer segments and subscription behavior
-   Product and category performance
-   Revenue contribution across demographic groups
-   Discount use, ratings, and shipping patterns through SQL analysis

The analysis can help teams identify areas for further investigation,
customer engagement, and product or promotion review. Recommendations
should be based on the validated results rather than assumed from chart
titles alone.

## How to Run

### Requirements

-   Python 3.10+ (or a compatible Python environment)
-   Jupyter Notebook
-   PostgreSQL
-   Power BI Desktop
-   The project CSV dataset

### 1. Clone or Download the Project

``` bash
git clone <your-repository-url>
cd <your-project-folder>
```

### 2. Create and Activate a Virtual Environment (Optional)

``` bash
python -m venv .venv
```

On macOS/Linux:

``` bash
source .venv/bin/activate
```

On Windows:

``` bash
.venv\Scripts\activate
```

### 3. Install Python Packages

``` bash
pip install pandas numpy matplotlib seaborn sqlalchemy psycopg2-binary jupyter
```

Install any additional packages imported in your notebook.

### 4. Run the Notebook

``` bash
jupyter notebook
```

Open the project notebook and update the dataset path if needed.

### 5. Set Up PostgreSQL

-   Start your PostgreSQL server and create a database for the project.
-   Update the connection settings in your notebook.
-   Keep passwords and other credentials out of the notebook and Git
    repository. Use environment variables or a local `.env` file that is
    excluded from version control.
-   Run the notebook cells that load the cleaned data into PostgreSQL,
    then execute the SQL analysis queries.

### 6. Open the Power BI Dashboard

Open the `.pbix` file in Power BI Desktop. If the data source path or
PostgreSQL connection differs on your machine, update the source
settings and refresh the data.

### 7. Review the Report

Open the project PDF report for a concise summary of the analysis and
business questions.

## Suggested Repository Structure

``` text
Customer-Shopping-Behavior-Dashboard/
├── data/
│   └── customer_shopping_behavior.csv
├── notebooks/
│   └── customer_shopping_behavior_analysis.ipynb
├── sql/
│   └── analysis_queries.sql
├── powerbi/
│   └── Customer_Behaviour_Dashboard.pbix
├── reports/
│   └── Customer_Shopping_Behavior_Analysis_Report.pdf
├── images/
│   └── dashboard_screenshot.png
├── requirements.txt
└── README.md
```

Update the filenames and folders above to match the files in your actual
repository.

## Author

Nitin Khasdeo
Data Analytics Project \| Python · SQL · Power BI
