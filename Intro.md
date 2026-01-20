
- Installing the gcloud CLI
- Create a project
- Go to cloud storage > Create a bucket > Create a folder > Uploading files
- Go to BigQuery > Create dataset > Create table > Google Cloud Storage > Create table > Select the data files amd create a table 
- During table creation, if necessary, insert JSON code to manually select the type of each column.


- Go to GCP CLI and signed with you account > select your project 
- gcloud info
- bq mk -t etl_db.tb_voos (Creating a table using BigQuery)
- bq load --autodetect --source_format=NEWLINE_DELIMITED_JSON etl_db.tb_voos gs://base_voos_sergio/raw_data/2023-07-30.json
- bq load --schema schema.json --source_format=NEWLINE_DELIMITED_JSON etl_db.tb_voos gs://base_voos_sergio/raw_data/2023-07-30.json (Using a file Schema)