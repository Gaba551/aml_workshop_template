# Datastores

Azure Machine Learning datastores allows an user to securely connect to the Azure storage. Through registering it, there is no need to code it into your scripts. Underlying supporting cloud-based storages that can be registered as such:

•   Azure Blob Container
•   Azure File Share
•   Azure Data Lake
•   Azure Data Lake Gen2
•   Azure Blob Container
•   Azure SQL Database
•   Azure Database for PostgreSQL
•   Databricks File System
•   Azure Database for MySQL

It allows for having all the data necessary for one project in one place, even if the data comes from multiple sources.

# Datasets

Datasets are references to the data points in the data storage necessary for your machine learning model. No costs are incurred as they are no copies of the data. There are four options to register datasets:

•   Local files
•   Datastores (Azure cloud storage)
•   Web files
•   Open Datasets

Two data types are supported:

•   File: one or multiple files residing in the datastore or public URL
•   Tabular: data in a tabular format, allowing for loading it into a Pandas or DataFrame for data preprocessing.
