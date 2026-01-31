# Global Superstore Profitability Analysis

A comprehensive retail data analysis project examining profitability patterns across 116 cities to identify underperforming segments and develop data-driven strategic recommendations.

**Timeline:** October 2025 - November 2025

---

## Executive Summary

This analysis uncovered critical profitability issues despite strong sales performance. Key finding: **116 cities and 10 states operate at negative profit**, with major markets like Philadelphia, Houston, and Chicago losing money despite high sales volume. The Central region generated **$501K in sales but only $39K in profit** due to excessive discounting and operational inefficiencies.

---

## Key Findings

### Geographic Performance
- **116 cities** with negative profit margins identified
- **10 states** losing money despite strong sales
- **Texas**: $170K sales, **-$25.7K profit** (worst performing state)
- **Philadelphia**: $109K sales, **-$13.8K profit** (worst performing city)

### Regional Analysis
- **West Region**: $725K sales, $108K profit (best performer, lowest discounts)
- **Central Region**: $501K sales, $39K profit (over-discounting destroying margins)
- **South Region**: Similar underperformance pattern to Central

### Category Insights
- **Technology**: Most profitable despite lowest sales volume
- **Office Supplies**: Strong margins with high demand
- **Furniture**: Loss-making in Central region (-$2,871)

### Critical Discovery
- **Discount correlation**: Near-zero impact on sales (r = -0.02), negative impact on profit (r = -0.22)
- Problem isn't demand—it's execution (pricing strategy, operational efficiency)

---

## Methodology

### Data Analysis
- **Dataset**: Sample Superstore from Kaggle (9,994 rows, 21 columns)
- **Scope**: 531 cities, 49 states, 3 product categories, 4 regions
- **Tools**: Python, Pandas, Matplotlib, Seaborn, Scikit-learn

### Exploratory Data Analysis
- Correlation analysis (sales vs. profit, discount impact)
- Regional and categorical performance comparison
- City-level profitability assessment
- Grouped analysis by region, category, segment

### Predictive Modeling
- **Linear Regression Model** to predict profit based on:
  - Sales volume
  - Discount rates
  - Quantity sold
- **Residual analysis** to identify cities underperforming vs. model expectations
- Region-specific model validation with scatter plots

---

## Technical Implementation

```python
# Key Technologies
- Python 3.x
- Pandas (data manipulation)
- Matplotlib & Seaborn (visualization)
- Scikit-learn (Linear Regression)
```

### Model Performance
- **West Region**: Strong upward trend, tight data clustering (excellent operational efficiency)
- **South Region**: Flat trend line, significant scatter (-$4K to +$3K range) indicating operational issues beyond discounting
- **East & Central**: Moderate consistency with slight operational inefficiencies

---

## Strategic Recommendations

### Immediate Actions
1. **Optimize discount strategy** in Central and South regions
2. **Address category mix** problems (especially Furniture in Central)
3. **Investigate operational inefficiencies** in high-sales/low-profit cities

### Expansion Strategy
1. **Profile successful cities** (use West region characteristics)
2. **K-means clustering** to identify ideal expansion markets
3. **Avoid replicating** Central/South mistakes in new markets

---

## Business Impact

This analysis provides actionable intelligence for:
- **Pricing optimization**: Data proves excessive discounting doesn't drive sales
- **Market prioritization**: Identify which underperforming cities to fix vs. exit
- **Expansion decisions**: Evidence-based market selection using profitable city profiles
- **Category strategy**: Focus on high-margin products (Technology, Office Supplies)

---

## Project Structure

```
Global-Superstore-Analysis/
├── Global-Superstore-Analysis-Project.ipynb   # Full analysis notebook
├── Sample-Superstore.csv                       # Dataset (if included)
└── README.md                                   # Project documentation
```

---

## Key Visualizations

- Regional sales vs. profit comparison (bar charts)
- Correlation heatmap (sales, discount, profit relationships)
- Scatter plots with regression lines (by region)
- Category performance analysis
- Top/bottom performers by city and state

---

## Insights for Data-Driven Strategy

> "High sales volume doesn't guarantee profitability. This analysis reveals that demand exists in underperforming markets—the real issues are pricing strategy, product mix, and operational execution."

### What Makes West Region Successful?
- Minimal discounting
- Consistent performance across categories
- Strong operational efficiency
- Balanced product mix

### What's Breaking Central/South?
- Over-aggressive discounting (no sales benefit)
- Furniture category losses
- Operational inefficiencies beyond model parameters
- Poor pricing discipline

---

## Future Work

- **Part 2 Analysis** (planned):
  - K-means clustering for market segmentation
  - Enhanced predictive modeling for expansion opportunities
  - Detailed operational recommendations by region
  - ROI projections for strategy implementation

---

## Contact

**Shaurya Ghai**
- LinkedIn: [linkedin.com/in/shauryaghai](https://www.linkedin.com/in/shauryaghai)
- GitHub: [github.com/ShauryaGhai](https://github.com/ShauryaGhai)

---

## License

This project is available for educational and portfolio purposes.
