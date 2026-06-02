# Global Superstore Profitability Analysis
Retail profitability analysis identifying why high-sales regions lose money — using correlation analysis, residual-based market classification, and regression modeling on 9,994 transactions across 531 cities.

# Overview
This project investigates why certain high-sales regions and cities consistently lose money. Using the Global Superstore dataset, the goal was to move beyond surface-level sales metrics, identify the pricing and operational failures driving negative margins, and build a data-driven framework for fixing underperformers and identifying expansion targets.

# Dataset
9,994 transactions across 531 cities, 49 states, 3 product categories, and 4 regions.

# Key Findings
### Discounting destroys margin without driving sales:
Discounts have near-zero correlation with sales (r ≈ −0.02) but a clear negative correlation with profit (r ≈ −0.22). Central and South regions were aggressively discounting expecting more volume — but the data shows discounts don't move sales at all. Despite strong demand, 116 cities and 10 states operate at negative profit — Texas generates $170K in sales but loses $25K in profit. The demand exists. The execution is broken.
### West region as the benchmark:
West generated $725K in sales and $108K in profit with the lowest average discount of any region. Profitability comes from pricing discipline, not chasing volume.
### Residual analysis classified two types of underperformers:
A regression model predicting profit from sales, discount, and quantity was used diagnostically. Residuals separated fixable markets (Texas, Ohio — bad fundamentals, discount reduction will help) from structural exit candidates (Wyoming, West Virginia — underperforming even after accounting for fundamentals). The same analysis identified Minneapolis as a high-efficiency expansion target with a residual of +$505 per order.
### Furniture is structurally broken:
Furniture carries a residual of −$34 per order even after accounting for pricing and volume — meaning the problem isn't discounting alone. Technology and Office Supplies consistently outperform expectations.

# Methodology

EDA: regional, state, city, and category-level breakdowns with correlation analysis
Visualization: bar charts surfacing discount patterns and regional performance gaps
Regression modeling on 70/30 split; residuals used as a market classification tool


# Tools
Python, Pandas, Matplotlib, Seaborn, Scikit-learn
