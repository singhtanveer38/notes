# Databases

## Database 
+ Usually referred as Online Transaction Processing (OLTP).
+ Used to store daily transactions by companies/organisations.
+ Sources include applications, e.g., online shopping portal, bank transactions etc.

---

## Warehouse
+ Usually referred as Online Analytical Processing (OLAP).
+ Used for analysis.
+ Source include OLTP.
+ Data is moved from OLTP to OLAP which includes ETL(extract, transform, load) or ELT(extract, load, transform).

### Characteristics

1. __Subject-oriented__: They can be used to analyze data about a particular subject or functional area (such as sales).
2. __Integrated__: Data warehouses integrate data from various sources.
3. __Nonvolatile__: Once data is in a data warehouse, it’s stable and doesn’t change.
4. __Time-variant__: Data warehouse consists of historical data.

### Data Mart
+ Subset of Data Warehouse
+ Single subject oriented

```
Data Warehouse is used to create organisation wise report whereas Data Mart is used to create department wise report.
```
### Operations
![The basic architecture of a data warehouse
](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8d/Data_warehouse_architecture.jpg/330px-Data_warehouse_architecture.jpg)

_The basic architecture of a data warehouse_

The data from various sources such as applications or databases/OLTP systems is processed through an ETL pipeline and stored in the warehouse. For further analysis, the data is divided into different data marts and provided to the user.

## Incremental Loads

 An incremental load is a process where new and updated data from some source is loaded into a destination, whereas matching data is ignored. That last part about matching data is the key. If the data is identical in both source and destination, the best thing we can do is leave it be.

## High Water Mark

The boundary between the used space and unused space in a data block.

```
DELETE does not resets high water mark, TRUNCATE does.
```

---

## Reference

1. [What Is a Data Warehouse by Oracle](https://www.oracle.com/in/database/what-is-a-data-warehouse/#:~:text=A%20data%20warehouse%20is%20a,large%20amounts%20of%20historical%20data.)
2. [Wikipedia](https://en.wikipedia.org/wiki/Data_warehouse)
3. [Cloud Data Storage Explained by IBM](https://youtube.com/playlist?list=PLOspHqNVtKAAXDobTc9kBWwnfgzNV2k_a)
4. [Data warehousing concepts by Naresh T](https://youtube.com/playlist?list=PL6ZxnSyAoSoCE4nLbJxgoZ5DJziSLyBGN)