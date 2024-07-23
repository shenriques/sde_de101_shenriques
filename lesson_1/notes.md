# What Do Data Engineers Do?

## Intro

- Know the outcomes expected for a company to be data driven and help them get there

## Responsibilities 

### 1. Move data between systems

- Main responsibility
- **Extract** data from sources (e.g. API, cloud storage, databases, static files)
- **Transform** data via mapping, filtering, enrichment, changing the structure, denormalising, aggregating etc
- **Load** data into destination system (e.g. cloud storage file system, data warehouse, cache database)
- Common tools: Pandas, Spark, Dask, Flink, Beam, Debezium, Kafka, Docker, Kubernetes

### 2. Manage data warehouses

- Usually company data ends up in a data warehouse, requiring a DE to:
- **Warehouse data modelling**
    - Model data for analytical queries (usually aggregation queries on large tables)
- **Ensure warehouse performance**
    - Ensure queries are fast
    - Scale warehouse as needed
- **Ensure data quality**
- Common modeling techniques: Kimball modeling, Data Vault, Data Lake
- Common frameworks: Great expectations, dbt for data quality
- Common warehouses: Snowflake, Redshift, Bigquery, Clickhouse, Postgres

### 3. Schedule, execute and monitor pipelines

- Schedule pipelines to run at a certain time / in response to an event
- Execute pipelines and ensuring they can scale / have the right permissions, etc
- Monitoring for failures, deadlocks, and long-running tasks
- Manage metadata such as time of the run, end to end time taken, failure reasons, etc
-  Common frameworks: Airflow, dbt, Prefect, Dagster, AWS Glue, AWS Lambda, Streaming pipeline using Flink/Spark/Beam
-  Common databases: MySQL, Postgres, Elastic search and data warehouses
-  Common storage systems: AWS S3, GCP cloud store
-  Common monitoring systems: Datadog, Newrelic

### 4. Serve data to the end-users

- Once data is available in your data warehouse, serve it to end-users e.g. analysts, an application, external clients, etc
- Depending on the end-user you may have to set up
- Data visualization/Dashboard tool: for data analysis and sharing charts easily
- Permissions for the data
    - If it’s a table, granting correct permissions to applications / end-users
    - If it’s cloud storage, granting cloud users appropriate permissions, etc
- Data endpoints (API): if application/external clients need API-based access to your data. 
        - Need to set up a sever to send data via the API endpoint for this to work  
- Data dumps from the system for clients: Some clients may require data dumps from your system. 
    - Set up a data pipeline to facilitate this
- Common tools/languages: Looker, Tableau, Metabase, Superset, role-based permissions(for your system), Python/Scala/Java/Go for API endpoints, pipeline tools for client data dumps

### 5. Data strategy for the company

Coming up with the data strategy involves:
- Deciding what data to collect, how to collect it, and store it securely.
- Evolving data architecture for custom data needs.
- Educating end users on how to use data effectively.
- Deciding what data (if any) to share with external clients.
- Common tools/frameworks: Confluence, google docs, RFC documents, brainstormings, meetings

### 6. Deploy ML models to production

- Data scientists / analysts develop sophisticated models that closely model the working of a specific business process. 
- Data engineers optimise models to be used in production at model deployment stage by:
    - Optimizing training and inference: Setting up a batch/online learning pipelines. Ensuring the model is appropriately sized.
    - Setting up monitoring: Setting up monitoring and logging systems for the ML model.
- Common frameworks: Seldon core, AWS MLOps

## Conclusion

- Number of responsibilities depends on the company, team structure and workload
- Main objective: enable company wide use of data for decision making
- Bigger the company = narrower / deeper your responsibilities