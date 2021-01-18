# Operationalizing machine learning

This repository includes an implementation the second project of the Udacity course *Machine Learning with Microsoft Azure*. It demonstrates various aspects of operationalizing a machine learning model, including automated Azure authentication, deployment and logging of an AutoML model, documentation and consumption of a model endpoint and the creation and deployment of machine learning pipelines.

## Architectural Diagram
*TODO*: Provide an architectual diagram of the project and give an introduction of each step. An architectural diagram is an image that helps visualize the flow of operations from start to finish. In this case, it has to be related to the completed project, with its various stages that are critical to the overall flow. For example, one stage for managing models could be "using Automated ML to determine the best model". 
![image](../architecture/architecture.svg)

## Key Steps
*TODO*: Write a short discription of the key steps. Remeber to include all the screenshots required to demonstrate key steps. 
1. Authentication
   
   Since the project is implemented on a personal Azure account, we can include an  automated authentication step by creating of a service principal. This is an isolated step      that is not used in the remainder of the project.
   
   *Creation of the service principal*
   ![image](../screenshots/service_prinicipal.png)
2. Automated ML Experiment

   The first official step of the project is the creation of an AutoML experiment using a bankmarketing dataset. We wish to predict the success of direct marketing in a banking    context. First we load the dataset into into Azure, then we run an AutoML experiment on the dataset, and finally we have a look at the best model it finds.
   
   *Bankmarketing dataset*
   ![image](../screenshots/bankmarketing_dataset.png)
   <br></br>
   
   *Completed AutoML experiment*
   ![image](../screenshots/bankmarketing_data_automl.png)
   <br></br>
   
   *Best model*
   ![image](../screenshots/best_model.png)
3. Deploy the best model

   We now deploy the best model AutoML has found using a Azure Container Instance. We enable authentication.
4. Enable logging

   We also enable Application Insights to generate logs. We then view these logs by running the Python script [logs.py](../logs.py).
   
   *Logs*
   ![image](../screenshots/logs.png)
5. Swagger Documentation

   We now consume the model endpoint with Swagger to generate documentation on its usage.
   
   *Swagger running on localhost*
   ![image](../screenshots/swagger.png)
6. Consume model endpoints

   Now that we know how to interact with th model endpoint, we can use it to make a prediction. This is done in in the script [endpoint.py](../endpoint.py). We also test the        performance of the model enpoint using Apache Benchmark (see also [benchmark.sh](../benchmark.sh)). 
   
   *Running endpoint.py*
   ![image](../screenshots/endpoint.png)
   <br></br>
   
   *Apache Benchmark*
   ![image](../screenshots/apache_bench.png)
7. Create and publish a pipeline

   In the final step of our project we create a pipeline aith a single AutoML step that takes the bankmarketing dataset as its input. We then publish this piepline and run it      from its REST endpoint.
   
   *Pipeline*
   ![image](../screenshots/pipeline.png)
   <br></br>
   
   *Pipeline endpoint*
   ![image](../screenshots/pipeline_end_point.png)
   <br></br>
   
   *Bankmarketing dataset with AutoML module (graphical representation of pipeline run)*
   ![image](../screenshots/bankmarketing_data_automl.png)
   <br></br>
   
   *Published pipeline overview*
   ![image](../screenshots/published_pipeline_overview.png)
   <br></br>
   
   *RunDetails widget in Jupyter notebook*
   ![image](../screenshots/run_details.png)
   <br></br>
   
   *Published pipeline run*
   ![image](../screenshots/pipeline_rest_end_point_run.png)
   <br></br>

## Screen Recording
A screencast describing this project can be found under: https://youtu.be/Dcg2eFTvSH0.

## Standout Suggestions
All the optional work has been mentioned in Key Steps under 1. Authentication and 6. Comsume Endpoints. 
