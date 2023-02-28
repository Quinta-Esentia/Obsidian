
## Open [[Terminal]]:
	In jupyter lab, go: File -> New -> Terminal

# path to deleted files: 
- `home/sagemaker-user/.local/share/Trash/files`


# Use Sagemaker to download S3 files

1. Open Sagemaker (start instance, import pandas etc)
2. Read dataframe, example: `df = pd.read_csv('s3://hrds-projects/data-catalog/special-projects/APR/APR_CuEq_V6_4.csv')`
3. Write data to Sagemaker directory: `df.to_csv('/root/data/APR_CuEq_V6_4.csv', index = False)`
4. Right click file in SM file browser and click "download"