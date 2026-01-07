# Cycling-equipment-accessories-KPI-Dashboard
Power BI Dashboard

**1. Project Summary**

- The goal of this project was to design and develop an interactive KPI dashboard in Power BI that helps track sales performance of cycling equipment and accessories. The dashboard provides insights into revenue, profit, and key business drivers, allowing management to monitor performance across products, geographies, and customer segments.

- **The project followed the end-to-end BI development lifecycle: data preparation, modeling, DAX calculations, visualization design, and interactive dashboard building.**

<img width="1170" height="680" alt="image" src="https://github.com/user-attachments/assets/8216ae87-ed17-4c24-aa6b-ad01ac356053" />
<img width="987" height="608" alt="image" src="https://github.com/user-attachments/assets/944d5d68-aa5a-4474-ad0c-4d4b79a25bd8" />
<img width="1165" height="673" alt="image" src="https://github.com/user-attachments/assets/d878274d-ebbc-4958-a7fc-aee3bc656557" />
<img width="1165" height="678" alt="image" src="https://github.com/user-attachments/assets/5ab16356-707c-40fc-ab40-9af52224226f" />


**2. Steps Used**
**Step 1: Understanding Business Requirements**

**Objective: Track performance of cycling equipment & accessories sales.**

**Key KPIs:**

- Total Sales (Revenue)

- Total Profit

- Profit Margin %

- Quantity Sold

- Top Customers & Top Products

- Sales by Region, Category, and Sub-Category

- Dashboard must allow drill-throughs and interactive filtering.

**Step 2: Data Loading & Transformation (Power Query)**

- Connected to raw data sources (CSV/Excel files provided in the course).

**Cleaned data:**

- Removed duplicates, nulls, unnecessary columns.

- Ensured proper data types (e.g., date fields, numeric formats).

- Standardized product categories and region names.

- Applied Power Query transformations for consistency.

**Step 3: Data Modeling**-

 Built a star schema with:
- Fact Table → Sales Transactions (Revenue, Profit, Quantity, Date, Product ID, Customer ID).
- Dimension Tables → Products, Customers, Geography, Calendar.
Defined relationships:
- One-to-many between dimensions and fact table.
- Calendar table linked for time intelligence (YTD, MTD, YoY).

**Step 4: DAX Calculations (Measures)**

Created calculated measures for KPIs, e.g.:

**Total Sales** = SUM(Sales[Revenue])

**Total Profit** = SUM(Sales[Profit])

**Profit Margin %** = DIVIDE([Total Profit],[Total Sales])

**Sales YTD, MTD** = CALCULATE([Total Sales], DATESYTD(…))

- Top N Products / Customers using RANKX functions.

**Step 5: Dashboard Design & Visualization**

- Built a KPI card section (Total Sales, Profit, Margin, Quantity).

**Added charts:**

- Bar/Column Chart → Sales by Product Category/Subcategory.

**Map → Sales by Region.**

- Line Chart → Monthly Sales Trend.

- Tables → Top Customers, Top Products.

- Used Slicers for interactive filtering by region, category, and time.

- Applied conditional formatting to highlight performance gaps.

**Step 6: Dashboard Enhancements**

- Added drill-throughs to analyze customer and product details.

- Applied bookmarks & navigation buttons for smooth storytelling.

- Used color themes (green for growth, red for decline).

- Optimized performance by hiding unnecessary columns & enabling aggregations.

**3. Results / Outcomes**

- Single-page interactive KPI dashboard created in Power BI.

Business Users can now:

- Track Total Sales, Profit, and Margins at a glance.

- Identify top-performing products and customers.

- Monitor regional sales performance via interactive maps.

- Compare sales trends month-over-month and year-over-year.

- Perform ad-hoc analysis by slicing & drilling into data.

