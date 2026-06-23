# Retail Sales Dashboard
### Multi-Branch Sales Performance Analysis | Power BI & SQL

## Business Context
A retail company with multiple branches across Chile needed a centralized 
view of their sales and cost performance. Leadership had no reliable way to 
track which cities were most profitable, how managers were performing, or 
whether the business was growing month over month.

## The Solution
I designed an interactive Power BI dashboard connected to a MySQL database, 
enabling leadership to explore performance across cities, product categories, 
and time periods — all in real time.

## Dashboard Features
- **Net Utility by City** — horizontal bar chart showing profitability 
  per branch
- **City with Highest Utility per Month** — table identifying the top 
  performing city each month
- **Top 3 Managers of the Month** — ranking of managers by net utility 
  in the current month
- **Month-over-Month Growth** — waterfall chart tracking business growth 
  trends
- **Sales by City Map** — geographic visualization of total sales across 
  all branches
- **Interactive Filters** — slice by product category and branch

## Key DAX Measures Built
- Net Utility = Total Sales - Total Costs
- Month-over-Month Growth rate
- Dynamic Top 3 Managers using TOPN + ADDCOLUMNS
- City with highest utility per month using TOPN + ISINSCOPE

## Tools Used
| Tool | Purpose |
|------|---------|
| MySQL | Data storage and querying |
| SQL | Filtering last 12 months of data |
| Power BI Desktop | Dashboard and visualizations |
| DAX | Custom measures and calculations |

## Key Technical Decisions
- Connected Power BI directly to MySQL using Database authentication
- Used `DATE_FORMAT(CURDATE() - INTERVAL 11 MONTH, '%Y-%m-01')` to 
  dynamically filter the last 12 months without hardcoding dates
- Replaced SUMMARIZE with ADDCOLUMNS for reliable CALCULATE behavior 
  inside TOPN
- Built a custom date table to avoid duplicate months across years

## Screenshots
*(Add screenshots of the dashboard here)*
