# Initial Requirements

## Business Problem

We need to build a scalable data platform for an e-commerce company.

The platform should collect data from multiple sources,
process the data, store it in a lakehouse, and make
trusted datasets available for analytics and data science.

## Data Sources

- Orders
- Customers
- Products
- Inventory
- Payments

## Initial Goals

1. Ingest raw data
2. Store raw data in the data lake
3. Transform raw data using Spark
4. Create Bronze, Silver and Gold layers
5. Provide analytical datasets
6. Implement data quality checks
7. Monitor pipeline execution


A thought on what should be served 
* How much revenue did we generate?
* Which products are selling?
* Which customers are most valuable?
* Which products are running out of stock?
* What is today’s revenue compared with yesterday?
* Are there suspicious order/payment patterns?
* Can data scientists access clean datasets?
* Can analysts query the data efficiently?
* Can we process millions of events every day?