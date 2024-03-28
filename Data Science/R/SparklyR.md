



# Load data


Troubleshooting error: `Error: org.apache.spark.SparkException: Missing Credential Scope.`  
- tried `spark_disconnect(sc)`  
- looked at https://community.databricks.com/s/feed/0D58Y00009bzqi1SAA  
- tried reconnecting to cluster
- tried restarting cluster 

`dfs <- spark_read_csv(sc, path = 's3://hrds-projects/data-catalog/special-projects/APR/APR_CuEq_V6_4.csv', header = TRUE, infer_schema = TRUE, escape =  "\"")`

#coding