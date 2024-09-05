# ReadMe - Client Data Exploration and Transformation

## Overview

This project involves exploring, transforming, and analyzing a dataset containing client order information. The dataset includes client details, order information, item categories, prices, and quantities. The goal is to prepare the data for analysis by calculating additional metrics, confirming accuracy against known values, and summarizing key insights about client activity.

## Part 1: Explore the Data

1. **Data Import and Initial Exploration**:
   - The dataset is imported using Pandas for exploration and manipulation.
   - Initial exploration includes viewing the first few rows, column names, and generating descriptive statistics using `.describe()` and `.info()` methods to understand the structure and content of the data.

2. **Exploratory Questions**:
   - Identify the top 3 item categories with the most entries.
   - Determine the subcategory with the most entries for the top category.
   - Find the 5 clients with the most entries.
   - Calculate the total number of units ordered by the top client.

## Part 2: Transform the Data

1. **Create New Columns**:
   - **Subtotal Calculation**: A new column `line_subtotal` is created to calculate the total price for each line (unit price * quantity).
   - **Shipping Price**: Based on total weight, shipping prices are calculated. For items over 50 pounds, a rate of $7 per pound is applied; otherwise, a rate of $10 per pound is used.
   - **Total Price and Sales Tax**: The total price for each line, including shipping and sales tax (9.25%), is calculated and stored in `total_price_with_tax`.
   - **Line Cost and Profit**: The cost and profit for each line are calculated based on unit cost, shipping price, and the total price with tax.

2. **Validation of Calculations**:
   - The calculations are validated by comparing the total prices for 3 specific orders against known receipt values.

## Part 3: Confirm Your Work

- The calculated totals for the 3 orders matched the email receipt values, confirming the accuracy of the transformations:
  - **Order ID 2742071**: $152,811.89
  - **Order ID 2173913**: $162,388.71
  - **Order ID 6128929**: $923,441.25

## Part 4: Summarize and Analyze

1. **Client Analysis**:
   - The top 5 clients by quantity are identified, and their total units purchased, shipping costs, revenue, and profit are summarized.
   - The data is formatted, and large monetary values are converted to millions for better readability.

2. **Summary Findings**:
   - **Client ID 24741** stands out with significantly higher orders, revenue, and profit compared to other clients. This highlights the critical role of key clients in driving business profitability.

## Running the Analysis

1. Ensure that you have the required dependencies installed:
   ```bash
   pip install pandas
   ```
2. Place the dataset (`client_dataset.csv`) in the same directory as the script.
3. Run the script to explore and analyze the dataset.

## Data Summary Output

The final summary table provides insights into the top 5 clients, including:
- Total units purchased
- Shipping price in millions
- Revenue in millions
- Profit in millions

## Findings

The analysis indicates that **Client ID 24741** plays a crucial role in overall profitability, contributing significantly more to the revenue and profit than other clients.

---

Feel free to modify the dataset path or analysis steps according to your project needs.
