# Customer-Behvaior-Analysis
1.Project Overview This project provides an end-to-end analysis of customer shopping behavior using a dataset of 3,900 transactions. By combining Python for data cleaning, SQL for business logic, and Power BI for visualization, the project uncovers critical insights into demographics, spending patterns, and subscription trends to drive strategic business decisions.

Dataset Summary
Size: 3,900 rows and 18 initial columns.

Demographics: Age, Gender, Location, and Subscription Status.

Transactional Data: Item purchased, Category, Purchase Amount, Season, and Size.

Behavioral Data: Review ratings, frequency of purchases, and shipping preferences.

Technical Workflow

Data Cleaning & Preparation (Python) Using pandas and numpy, the following steps were performed:

Missing Value Imputation: Replaced 37 missing values in the review_rating column using the median rating per product category.
+1

Standardization: Renamed columns to snake_case for consistency.

Feature Engineering:

Created age_group by binning customer ages into segments (Young Adult, Adult, Middle-aged, Senior).

Mapped purchase frequencies to a numeric purchase_frequency_days column.

Redundancy Check: Dropped promo_code_used after verifying it was 100% identical to discount_applied.

Database Integration (PostgreSQL/MySQL) The cleaned data was exported from Python into a relational database using SQLAlchemy to enable structured business querying.

Business Analysis (SQL) Key business questions addressed via SQL include:

Revenue by Gender: Male customers contributed $157,890 compared to $75,191 from female customers.

Subscription Impact: While there are more non-subscribers (2,847), subscribers and non-subscribers maintain a similar average spend (~$59).

Top Products: Identified top-rated items like Gloves (3.86) and Sandals (3.84).

Customer Segmentation: Classified the base into Loyal (3,116), Returning (701), and New (83) segments.

Visual Insights (Power BI) An interactive dashboard was built to track:
KPIs: Total customers (3.9K), Avg. Purchase ($59.76), and Avg. Rating (3.75).

Category Performance: "Clothing" and "Accessories" emerged as the highest revenue-generating categories.

Age Demographics: "Young Adults" represent the highest revenue-contributing age group.

Key Recommendations
Loyalty Programs: Implement rewards specifically for the "Returning" segment to convert them into "Loyal" customers.

Subscription Growth: Enhance exclusive benefits to increase the 27% subscription rate.

Targeted Marketing: Focus campaigns on high-revenue categories (Clothing) and the Young Adult demographic.

📂 Project Structure customer_behavior_analysis.ipynb: Python notebook for EDA and cleaning.

Customer Shopping Behavior Analysis.pdf: Detailed project report and SQL findings.

customer_shopping_behavior.csv: Original dataset.
