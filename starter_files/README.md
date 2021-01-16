# Operationalizing machine learning

This repository includes an implementation the second project of the Udacity course *Machine Learning with Microsoft Azure*. It demonstrates various aspects of operationalizing a machine learning model, including automated Azure authentication, deployment and logging of an AutoML model, documentation and consumption of a model endpoint and the creation and deployment of machine learning pipelines.

## Architectural Diagram
*TODO*: Provide an architectual diagram of the project and give an introduction of each step. An architectural diagram is an image that helps visualize the flow of operations from start to finish. In this case, it has to be related to the completed project, with its various stages that are critical to the overall flow. For example, one stage for managing models could be "using Automated ML to determine the best model". 

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
   
   *Completed AutoML experiment*
   ![image](../screenshots/bankmarketing_data_automl.png)
   
   *Best model*
   ![image](../screenshots/best_model.png)
3. Deploy the best model
4. Enable logging
5. Swagger Documentation
6. Consume model endpoints
7. Create and publish a pipeline

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
