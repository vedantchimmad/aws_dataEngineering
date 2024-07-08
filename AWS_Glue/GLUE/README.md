# AWS Glue

---
## Data Catalog
Is a metadata repository 
* Data Bases
* Tables
* Schema Registry-For the streaming Job
* Connections
* Crawlers
  * Access your data
  * Extracts metadata and creates table definition in the aws glue data catalog 
  * Create and manage AWS glue table schema and manage partitions of the glue tables

### AWS Crawler Classifier 
* AWS Glue Crawler uses built in classifier to infer the schema
* Crawler uses the classifier to build the table
* Need to tweak the crawler so create the custom classifier 
* Custom classifier types are : CSV,JSOn,XML and GROK
* GROK Classifier can be used for fixed width file

### AWS Glue Job
* Script Location : Where we have to store our script 
* Python library path : Where we have to store python dependency library 
* Bookmark : Fetch only incremental data from the source
* Retries : How many times need to be retries in case of failure
* Parameters : Pass the required parameter 
* Job type :
  * Python shell job
    * DPU(Data Processing Unit - 1DPU provides 4vCPU and 16GB of memory)
    * Python version
  * Spark Job - Scala or python
### Glue ETL
* Type - Spark, Spark Streaming 
* Glue versioning - comes with associated python,scala and spark version
* Language - Scala,Python
* Worker type - G.1X,G.2X
* Requested number of worker
### Glue Workflow
* Workflow is used for orchestration
* Used when you want to orchestrate the triggers
### Glue Data 
* Visual data preparation tool, no need to write code
* For traditional data pipelines and feature engineering
* Over 250 transformations to curate data for AI/ML by up to 80% faster
* Data profiling,Data quality ruleset and data linage with automated job scheduling 
#### Key concept in data brew
* Data set : Data
* Data Profiling : You can run data profiling job to profile the data,Existing shape of the data
* Project : To perform transformation in your dataset 
* Recipe : To build a list of set ordered transformations which can be reused 
* Job : To run the transformation on the data set
* Data linage : Visual interface to show how data is flowing 
* Data quality : 
