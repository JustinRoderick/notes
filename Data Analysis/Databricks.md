## Different Data Architecture
##### Data Warehouse
- Purpose built for BI and reporting
- Data has a standardized schema and only supports structured data
- Uses closed and proprietary file formats
- Expensive to scale
#### Data Lakes
- Can store any type of raw data (text, images, videos)
- Supports unstructured and semi-structured data
- Does not need a schema
- Inexpensive storage
#### Data Lakehouses
- Best between both lakes and warehouses
- Built on a data lake so it can store all types of data, but is more structured like warehouses

## Databricks Environment

- Workspace: Overarching structure for a team that contains notebooks, jobs, and clusters
- Notebooks: Web based interfaces for writing and testing code (Similar to Jupyter Notebooks)
- Clusters: Compute resources and configs that run the notebooks and jobs. Houses the resources that manage Apache Spark nodes
- Metastore: Contains data metadata such as information about the tables






Clusters
Notebooks
Spark
Delta Lake
Workspace
Jobs
Libraries
Autoscaling

