# U.S. Amazon Repeat Purchase Analysis

This Python project explores which Amazon product categories shoppers buy
from again within 90 days and how quickly they return.

[View the notebook and charts](amazon_shopping_eda.ipynb)

## Key Findings

- **Pet food had the highest 90-day repeat purchase rate** among ranked
  categories. 44.8% of eligible shoppers bought from the category again
  (871 of 1,944).
- **Bread led at day 30.** 28.7% of eligible bread shoppers had repurchased
  by then, compared with 22.9% for pet food. By day 90, pet food reached
  44.8% and bread reached 43.2%.
- **The ranking varied by year.** Bread had a higher 90-day repeat rate
  than pet food in the 2020 and 2021 first-purchase groups.

## Business Recommendation

Test a day-30 reorder reminder for pet food shoppers who have yet to
repurchase. Compare their 90-day repeat rate with a randomly assigned
holdout group to measure the reminder's effect.

## Data and Method

The source file contains 1.85 million purchase records from 5,027 U.S.
Amazon shoppers. I used Python, pandas, and Matplotlib to clean the data,
calculate repeat purchase rates, and visualize the results.

I counted one purchase day per shopper and category. A repeat purchase
was a purchase in the same category on a later day, within 90 days of
the shopper's first observed purchase in that category. I used records
through October 31, 2022, required a full 90-day follow-up window, and
ranked categories with at least 100 eligible shoppers.

## How to Run

1. Download `amazon-purchases.csv` from
   [Open E-commerce 1.0 on Harvard Dataverse](https://doi.org/10.7910/DVN/YGLYDY).
2. Open `amazon_shopping_eda.ipynb` in Google Colab.
3. Upload the CSV to the Colab session and run the notebook from top to bottom.
