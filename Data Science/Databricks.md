
# #DBFS

## View files & folders on DBFS
```python
display(dbutils.fs.ls('dbfs:/'))
display(dbutils.fs.ls('dbfs:/FileStore/'))
```

## Upload data to DBFS
To upload data:
1. Click `file` (top left menu) in a DB notebook
2. Click `Upload data to DBFS...`
3. Follow prompts (select location, a good default is somewhere in `dbfs:/FileStore/`)
4. Completion page includes code examples to load this data.

## Read csv files from DBFS

### Spark:
```Spark
df1 = spark.read.format("csv").option("header", "true").load("dbfs:/FileStore/data/APR_CuEq_V6_4.csv")
```

### Python (Pandas)
```python
import pandas as pd
df1 = pd.read_csv("/dbfs/FileStore/data/APR_CuEq_V6_4.csv")
```

### R
```R
require(SparkR)
df1 <- read.df("dbfs:/FileStore/data/APR_CuEq_V6_4.csv", "csv", header="true", delimiter= ",")
```

# Creat DB and Write Table
[Link](https://docs.databricks.com/data-governance/unity-catalog/create-schemas.html#language-Python)

Create Schema / DB
```python
spark.sql("USE CATALOG hive_metastore")
spark.sql("CREATE SCHEMA dexter_db_test")
```
See info
```SQL
DESCRIBE SCHEMA EXTENDED dexter_db_test
```
Write Table
```python
spark_df_filtered.write.saveAsTable("dexter_db_test.demo_HRsmall")
```
