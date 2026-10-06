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



## Business Requirements

### Data Volume

Assumption:
The platform initially processes approximately 100 GB of data per day.

The architecture should be capable of scaling beyond the initial volume.

### Data Loading

The platform should support incremental ingestion.

Full loads may be required for initial ingestion or specific recovery scenarios.

### Data Freshness

Initial assumption:
Most analytical data can be available within 1 hour of source data arrival.

Real-time requirements will be evaluated for specific use cases.

### Data Retention

Initial assumption:
Raw data will be retained for 2 years.

Curated datasets may have different retention requirements.

### Data Consumers

The data platform will serve:

- Data Analysts
- Data Scientists
- Business Intelligence dashboards
- Downstream applications



## Open Questions

1. What are the actual source systems?
2. What is the expected daily data volume?
3. How frequently does each source produce data?
4. Which datasets require incremental ingestion?
5. Which datasets require historical tracking?
6. Which dimensions require SCD Type 1 vs Type 2?
7. What freshness SLA does each dataset require?
8. What are the data retention requirements?
9. Who consumes each dataset?
10. What happens when source data is late or missing?
11. What happens when the same data arrives twice?
12. What happens when the source schema changes?
13. What are the expected data quality rules?
14. What happens when a pipeline fails halfway through?
15. What are the security/access requirements?