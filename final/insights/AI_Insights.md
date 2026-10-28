# AI Insights and Recommendations

I gave an AI tool the EDA numbers and the model results and asked for insights in simple words and what the business should do. I checked every number against the notebooks.

The short auto version (made by `notebooks/03_ai_insights.ipynb`) is in `auto_insights.txt`.

## Trends

- Revenue is 19.88M and profit is 9.92M, so the margin is about 50%. It stays almost the same every year.
- Sales grow about 10% a year (5.26M in 2013, 5.84M in 2014, 6.35M in 2015). 2016 has only Jan - May.
- July is the best month and August is the weakest (2013 - 2015).
- No sales on Sunday at all, and Saturday is about half of a normal day.
- California is 44% of revenue. Tailspin Toys is the biggest buying group.
- 566 lines lost money and 492 of them are Halloween zombie masks.

## The model

- Target: will a sale line be High Profit (profit above 120) or not.
- Random Forest is the best with 99.6% accuracy. Only 21 wrong out of 5,280 test lines.
- Decision Tree 99.3%, Logistic Regression 95.3%, SVM 88.9%.
- Linear Regression predicts the profit value with R2 = 0.70, so it gets the general idea but is not exact.
- The model mostly looks at Quantity and Unit Price, then item weight and lead time. This makes sense, profit is basically (price - cost) x quantity.
- Bags are High Profit 91% of the time and Packets only 38%.

## Recommendations

1. Push bigger orders (discounts on large quantity), because quantity is the number one driver of high profit.
2. Check the price of the Halloween masks or stop selling them, they make most of the losses.
3. Use the model before confirming an order to see if it will be high profit, and send low profit orders to a salesperson to upsell.
4. Plan stock and staff for July and do a promotion in August.
5. Grow outside California, the other states are much smaller.
6. Saturday is weak, a small online offer on weekends could help.
