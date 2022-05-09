# Pipeline

## ETL

+ Refers to Extract, Transform, Load.
+ Usually used in warehouses
+ The data is loaded from database/OLTP system, transformed and then loaded into the database

---

## Slowly Changing Dimension (SCD)

Stores current and historical data over time in a warehouse.

1. Type 1 SCDs - Overwriting
    
    + New data overrides existing data
    + Existing data is lost
    + Default type of dimension

2. Type 2 SCDs - Creating another dimension record

    + Retains full history of values
    + When the value of a chosen attribute changes, the current record is closed. A new record is created with the changed data values and this new record becomes the current record.
    + Each record contains the effective time and expiration time to identify the time period between which the record was active.

3. Type 3 SCDs - Creating a current value field

    + Stores two versions of values for certain selected level attributes. 
    + Each record stores the previous value and the current value of the selected attribute. 
    + When the value of any of the selected attributes changes, the current value is stored as the old value and the new value becomes the current value.

```
If only one previous history is needed, go for SCD 3
If all historical data is needed, go for SCD 2
If no is needed, go for SCD 1
```

---
## Tools

1. [Airbyte](https://airbyte.com/)

---

## Reference

1. [Build ETL pipeline with python](https://blog.devgenius.io/how-to-build-an-etl-pipeline-with-python-1b78407c3875)

2. [Automate ETL pipeline with airflow](https://blog.devgenius.io/how-to-automate-etl-pipelines-with-airflow-62484ee5ef4c)

3. [SCD](https://www.oracle.com/webfolder/technetwork/tutorials/obe/db/10g/r2/owb/owb10gr2_gs/owb/lesson3/slowlychangingdimensions.htm#:~:text=A%20Slowly%20Changing%20Dimension%20(SCD,the%20history%20of%20dimension%20records.))