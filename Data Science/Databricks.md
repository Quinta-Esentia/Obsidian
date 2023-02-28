
# #DBFS

## View files & folders on DBFS
In python:
`display(dbutils.fs.ls('dbfs:/'))`
`display(dbutils.fs.ls('dbfs:/FileStore/'))`

## Upload data to DBFS
To upload data:
1. Click `file` (top left menu) in a DB notebook
2. Click `Upload data to DBFS...`
3. Follow prompts (select location, a good default is somewhere in `dbfs:/FileStore/`)
4. Completion page includes code examples to load this data.

## Read csv files from DBFS

### PySpark:
    df1 = spark.read.format("csv").option("header", "true").load("dbfs:/FileStore/data/APR_CuEq_V6_4.csv")

### pandas
    import pandas as pd

    df1 = pd.read_csv("/dbfs/FileStore/data/APR_CuEq_V6_4.csv")

### R
    %r

    require(SparkR)

    df1 <- read.df("dbfs:/FileStore/data/APR_CuEq_V6_4.csv", "csv", header="true", delimiter= ",")