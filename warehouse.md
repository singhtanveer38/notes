# Warehouse

## Definition

A data warehouse is a type of data management system that is designed to enable and support business intelligence (BI) activities, especially analytics. Data warehouses are solely intended to perform queries and analysis and often contain large amounts of historical data. The data within a data warehouse is usually derived from a wide range of sources such as application log files and transaction applications.

![Data warehouse overview](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d8/Data_Warehouse_Feeding_Data_Mart.jpg/220px-Data_Warehouse_Feeding_Data_Mart.jpg)

_Data warehouse overview_

![The basic architecture of a data warehouse
](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8d/Data_warehouse_architecture.jpg/330px-Data_warehouse_architecture.jpg)

_The basic architecture of a data warehouse_

---

## Consisting of

1. A relational database to store and manage data
2. An extraction, loading, and transformation (ELT) solution for preparing the data for analysis
3. Statistical analysis, reporting, and data mining capabilities
4. Client analysis tools for visualizing and presenting data to business users
5. Other, more sophisticated analytical applications that generate actionable information by applying data science and artificial intelligence (AI) algorithms, or graph and spatial features that enable more kinds of analysis of data at scale

---

## Characteristics

1. __Subject-oriented__: They can analyze data about a particular subject or functional area (such as sales).
2. __Integrated__: Data warehouses create consistency among different data types from disparate sources.
3. __Nonvolatile__: Once data is in a data warehouse, it’s stable and doesn’t change.
4. __Time-variant__: Data warehouse analysis looks at change over time.

---

## ETL-based data warehousing

The typical extract, transform, load (ETL)-based data warehouse uses staging, data integration, and access layers to house its key functions. The staging layer or staging database stores raw data extracted from each of the disparate source data systems. The integration layer integrates the disparate data sets by transforming the data from the staging layer often storing this transformed data in an operational data store (ODS) database. The integrated data are then moved to yet another database, often called the data warehouse database, where the data is arranged into hierarchical groups, often called dimensions, and into facts and aggregate facts. The combination of facts and dimensions is sometimes called a star schema. The access layer helps users retrieve data.

The main source of the data is cleansed, transformed, catalogued, and made available for use by managers and other business professionals for data mining, online analytical processing, market research and decision support. However, the means to retrieve and analyze data, to extract, transform, and load data, and to manage the data dictionary are also considered essential components of a data warehousing system. Many references to data warehousing use this broader context. Thus, an expanded definition for data warehousing includes business intelligence tools, tools to extract, transform, and load data into the repository, and tools to manage and retrieve metadata.

---

## ELT-based data warehousing

ELT-based data warehousing gets rid of a separate ETL tool for data transformation. Instead, it maintains a staging area inside the data warehouse itself. In this approach, data gets extracted from heterogeneous source systems and are then directly loaded into the data warehouse, before any transformation occurs. All necessary transformations are then handled inside the data warehouse itself. Finally, the manipulated data gets loaded into target tables in the same data warehouse.

---

## Information storage

There are three or more leading approaches to storing data in a data warehouse – the most important approaches are the dimensional approach and the normalized approach.

### Dimensional Approach

In a dimensional approach, transaction data is partitioned into "facts", which are generally numeric transaction data, and "dimensions", which are the reference information that gives context to the facts. For example, a sales transaction can be broken up into facts such as the number of products ordered and the total price paid for the products, and into dimensions such as order date, customer name, product number, order ship-to and bill-to locations, and salesperson responsible for receiving the order.

### Normalized Approach

In the normalized approach, the data in the data warehouse are stored following, to a degree, database normalization rules. Tables are grouped together by subject areas that reflect general data categories (e.g., data on customers, products, finance, etc.). The normalized structure divides data into entities, which creates several tables in a relational database. When applied in large enterprises the result is dozens of tables that are linked together by a web of joins. Furthermore, each of the created entities is converted into separate physical tables when the database is implemented.

---

## Cloud Data Warehouse

Traditional or on-premise data warehouse requires physical parts to be installed, which when tried to scale in later stages of development can be quite difficult, which include buying new hardware, physical location for setup. To overcome this problem, cloud data warehouse come into picture. When using cloud data warehouse, the user need to pay only for the services that is being used. 

The main advantage of cloud warehouses over traditional warehouses is that the user need not to worry about scaling, security and availability.

Major providers include Snowflake, Azure Synapse Analytics, Amazon Redshift, Google BigQuery, Azure SQL Database.

---

## Reference

1. [What Is a Data Warehouse? (by oracle)](https://www.oracle.com/in/database/what-is-a-data-warehouse/#:~:text=A%20data%20warehouse%20is%20a,large%20amounts%20of%20historical%20data.)
2. [Wikipedia](https://en.wikipedia.org/wiki/Data_warehouse)