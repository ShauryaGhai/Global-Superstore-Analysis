# Global Superstore Profitability Analysis

This project analyzes retail profitability patterns using the Global Superstore dataset, focusing on why certain high-sales regions and cities consistently lose money. The goal was to move beyond surface-level sales metrics and identify execution and pricing issues driving negative margins, while also exploring how data can support smarter expansion decisions.

The analysis is based on 9,994 transactions across 531 cities and 49 states. Despite strong demand, over 100 cities and 10 states operate at negative profit. Major markets like Texas ($170K in sales, −$25K profit) and Philadelphia ($109K in sales, −$13.8K profit) highlight that demand exists, but execution is broken.

Correlation analysis showed that discounting has near-zero impact on sales (r ≈ −0.02) but a clear negative impact on profit (r ≈ −0.22), especially in the Central and South regions. The West region stood out as a benchmark, generating over $700K in sales and $100K+ in profit with minimal discounting and consistent performance.

Category-level analysis revealed that Technology and Office Supplies drive the strongest margins, while Furniture underperforms across regions, particularly in Central markets. A linear regression model using sales, discount, and quantity helped identify cities underperforming relative to expected profit, further reinforcing that operational efficiency matters more than sales volume.

This project reflects how data is used in real business and strategy contexts: identifying what’s broken, understanding why it’s broken, and using evidence to guide pricing, category focus, and market expansion decisions.

Tools & Tech: Python, Pandas, Matplotlib, Seaborn, Scikit-learn
Key Focus Areas: profitability analysis, discount strategy, regional performance, operational efficiency, data-driven market strategy
