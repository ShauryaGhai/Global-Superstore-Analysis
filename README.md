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

### Personal Motivation & Approach

**Why I chose this dataset:**  
I wanted to replicate what data-driven strategists and consultants actually do in the real world. I've observed how stores perform well in some locations but struggle in others, which made me curious about the strategic questions businesses face:
- Why do certain regions underperform?
- Based on data insights, which new markets should they enter next?

The Sample Superstore dataset from Kaggle was perfect for this—it has clean data with essential variables (regions, cities, product categories, customer segments) needed to analyze performance gaps and make market entry decisions.

**My goal**: Learn how to leverage data science in business decision-making by identifying the right variables, recognizing patterns through independent analysis, and making data-driven predictions.

---

### Analysis Deep Dive: What The Numbers Really Show

**Dataset Scope:**
- 9,994 transactions
- 531 unique cities across 49 states  
- 3 product categories with multiple sub-categories
- 4 distinct geographic regions
- 4 customer segments (Consumer, Corporate, Home Office)

**The Discount Problem (Most Critical Finding):**
```
Correlation Analysis:
- Discount vs Sales: r = -0.02 (essentially ZERO impact)
- Discount vs Profit: r = -0.22 (NEGATIVE impact)
```

**This means:** Central and South's aggressive discounting is destroying margins without even driving sales growth. This finding is crucial because it proves the problem is 100% self-inflicted.

**Region-by-Region Breakdown:**

**West Region** (The Success Model):
- Sales: $725K+ 
- Profit: $108K+
- Strategy: Minimal discounting, consistent category performance
- Efficiency: Model predictions closely match actual profits (tight scatter)

**Central Region** (The Problem Child):
- Sales: $501K (strong demand!)
- Profit: Only $39K (terrible margin)
- **Furniture Category Loss**: -$2,871 
- Issue: Over-discounting without sales benefit

**South Region:**
- Similar underperformance pattern to Central
- Significant scatter in profit predictions (-$4K to +$3K)
- Indicates operational problems BEYOND just discounting

**East Region:**
- Moderate performance 
- Slight operational inefficiencies but manageable

---

### Cities & States: The Alarming Truth

**Worst Performing States** (despite strong sales):
1. **Texas**: $170K sales → **-$25.7K profit**
2. **Ohio**: $78K sales → -$17K profit  
3. **Pennsylvania**: $117K sales → -$15.6K profit
4. **Illinois**: $80K sales → -$12.6K profit
5. **North Carolina**: $56K sales → -$7.5K profit

**Worst Performing Cities:**
1. **Philadelphia**: $109K sales → **-$13.8K profit**
2. **Houston**: $64.5K sales → -$10.2K profit
3. **San Antonio**: $21.8K sales → -$7.3K profit
4. **Lancaster**: $9.9K sales → -$7.2K profit  
5. **Chicago**: $48.5K sales → -$6.7K profit

**The pattern**: High sales cities losing money = demand exists, execution is broken.

---

### Category Performance: Technology Wins, Furniture Loses

**Technology:**
- Lowest sales volume
- **Highest profitability** (best margins)
- Consistent performance across regions

**Office Supplies:**
- Highest sales volume
- Strong profit margins
- Room to potentially increase margins given high demand

**Furniture:**
- Underperforming everywhere
- **Critical in Central region**: -$2,871 loss
- Product-specific problems beyond regional issues

---

### Linear Regression Model Results

**Model Approach:**
Built regression model using:
- Independent variables: Sales, Discount, Quantity
- Dependent variable: Profit
- Goal: Predict expected profit, then analyze residuals to find cities underperforming vs. expectations

**Region-Specific Model Validation:**

**West**: 
- Strong upward trend line
- Tight data clustering around predictions
- **Interpretation**: Excellent operational efficiency—what you predict is what you get

**South**:
- Flat trend line
- Massive scatter (residuals from -$4K to +$3K)
- **Interpretation**: Model is useless here because actual profit is unpredictable—operational chaos beyond the variables we measured

**East & Central**:
- Moderate consistency
- Some scatter indicating slight operational inefficiencies
- Better than South, worse than West

**Key Insight**: The model working well in West but failing in South proves that South's problems go deeper than just sales/discounts/quantity. There are hidden operational inefficiencies destroying value.

---

### Strategic Implications: What I Learned

**1. High Sales ≠ Profitability**  
Texas generates $170K in sales but loses $25K. Philadelphia does $109K in sales but loses $14K. The demand is there—the business model execution is broken.

**2. Discounting is Pure Value Destruction**  
Data proves excessive discounts have:
- Near-zero correlation with increased sales
- Significant negative correlation with profit
- Central/South need to stop discounting immediately

**3. West Region Holds the Answers**  
West's success isn't luck—it's:
- Pricing discipline (minimal discounts)
- Operational consistency
- Balanced product mix
- These traits should be replicated in expansion

**4. Furniture Needs Special Attention**  
Furniture loses money almost everywhere, especially Central. Either:
- Fix the furniture supply chain/pricing
- Or reduce furniture inventory in problem regions

**5. Operational Efficiency Matters More Than Sales Volume**  
South's model failure (flat trend, high scatter) shows that operational problems beyond pricing/sales/quantity are destroying profit. These need investigation:
- Returns/refunds?
- Shipping costs?
- Inventory management?
- Staff efficiency?

---

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
