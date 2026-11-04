#Market Basket Analysis

##Overview

This project uses Python to analyze retail transactions and identify products that occur together. The objective is to uncover potential cross-selling, product-bundling, and merchandising opportunities using frequent itemset mining and association rules.

##Business Questions

- Which products appear frequently in transactions?

- Which products are purchased together?

- Which associations have a lift greater than 1?

- Which combinations could be candidates for cross-selling or promotions?

##Dataset Summary

Unique transactions: **2,171**

Distinct product names after standardization: **39**

Average distinct products per transaction: **2.28**

Transactions containing at least two distinct products: **1,524** (approximately 70.2%)

The original transaction dataset is not included in the repository.

##Tools

- Python

- pandas and NumPy

- Matplotlib and Seaborn

- mlxtend

- Jupyter Notebook

##Methodology

- Inspect data quality and standardize product names.

- Examine transaction basket sizes.

- Construct a transaction-product basket matrix.

- Generate frequent itemsets using Apriori.

- Generate and filter association rules.

- Evaluate support, confidence, and lift.

- Export results and save visualizations.

##Analysis Parameters

- Minimum support: **0.01** (1%)

- Minimum confidence: **0.10** (10%)

- Minimum lift: greater than 1

The saved notebook output contains 58 frequent itemsets.

##Selected Findings

**Indomie Chicken Carton → Coca-Cola 50cl**

- Support: **1.06%**

- Confidence: **18.70%**

- Lift: **1.71**

- Transactions containing both products: 23

**Eva Water 75cl → Indomie Onion Single**

- Support: **1.66%**

- Confidence: **16.90%**

- Lift: **1.64**

- Transactions containing both products: 36

These associations may be useful for investigating cross-selling opportunities, but they do not establish causation or guarantee improved sales.

##Repository Structure

- basket_analysis.ipynb — analysis code and results.

- basket_analysis.html — static notebook export.

- results/ — frequent itemsets and filtered association rules in CSV format.

- visualizations/ — saved charts.

- report/ — project report.

- data/ — analysis dataset

- Business Applications

**The findings may inform product-bundling experiments, cross-selling recommendations, and merchandising decisions. Recommendations should be tested and evaluated using actual sales and profit outcomes**.

##Limitations

Association rules describe co-occurrence, not causation. A high lift does not necessarily indicate a commercially valuable relationship, especially when the number of transactions supporting the rule is small.