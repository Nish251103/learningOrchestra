# Usage
## Python package
* [learningOrchestra Client](https://riibeirogabriel.github.io/learningOrchestra/learning_orchestra_client_package) - The python package for learningOrchestra use

## Microservices REST API
* [database api](https://riibeirogabriel.github.io/learningOrchestra/database_api) - 
Microservice used to download and handling files in database;
* [projection](https://riibeirogabriel.github.io/learningOrchestra/projection) - 
Makes projections of stored files in database using spark cluster;
* [data type handler](https://riibeirogabriel.github.io/learningOrchestra/data_type_handler) - 
Changes fields file type between number and text;
* [histogram](https://riibeirogabriel.github.io/learningOrchestra/histogram) - 
Makes histograms of stored files in database;
* [t-SNE](https://riibeirogabriel.github.io/learningOrchestra/t_sne) - 
Makes a t-SNE image plot of stored files in database;
* [PCA](https://riibeirogabriel.github.io/learningOrchestra/pca) - 
Makes a PCA image plot of stored files in database; and
* [model builder](https://riibeirogabriel.github.io/learningOrchestra/model_builder) - 
Creates a prediction model from preprocessed files using spark cluster.

## Spark microservice
The projection, t-SNE, PCA and model builder microservices use the spark 
microservice to make your works, by default, this microservice has one instance, 
in case of you data processing require more computing processing, you can 
scale this microservice to earn computing power, to this, with learningOrchestra 
already deployed, in your master machine of you docker swarm cluster, run:

```
docker service scale microservice_sparkworker=NUMBER_OF_INSTANCES
```
The NUMBER_OF_INSTANCES is the amount of spark microservice instance which you 
desire to be created in your cluster, this number must be choosed according 
with your cluster resources and the resources requirements of your task.

## Database GUI
* [NoSQLBooster](https://nosqlbooster.com) - 
MongoDB GUI makes several database tasks, as files visualization, queries, 
projections and files extraction to formats as csv and json, read the 
[database api docs](https://riibeirogabriel.github.io/learningOrchestra/database_api) 
to learn how configure this tool.
