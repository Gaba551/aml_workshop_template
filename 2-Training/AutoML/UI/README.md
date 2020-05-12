# Automated Machine Learning

Automated machine learning (automated ML) builds high quality machine learning models for you by automating model and hyperparameter selection. Bring a labelled dataset that you want to build a model for, automated ML will give you a high quality machine learning model that you can use for predictions.

If you are new to Data Science, automated ML will help you get jumpstarted by simplifying machine learning model building. It abstracts you from needing to perform model selection, hyperparameter selection and in one step creates a high quality trained model for you to use.

If you are an experienced data scientist, automated ML will help increase your productivity by intelligently performing the model and hyperparameter selection for your training and generates high quality models much quicker than manually specifying several combinations of the parameters and running training jobs. Automated ML provides visibility and access to all the training jobs and the performance characteristics of the models to help you further tune the pipeline if you desire.

## Using Automated Machine Learning

Follow the instructions in the [documentation](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-create-portal-experiments) for a full overview of the user interface.

1. Navigate to the left pane of your workspace. Select Automated Machine Learning under the Authoring (Preview) section.
![Automated ML tab](https://docs.microsoft.com/en-us/azure/machine-learning/service/media/how-to-create-portal-experiments/nav-pane.png).

1. Enter your experiment name, then select a compute from the list of your existing computes or [create a new compute](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-create-portal-experiments#create-an-experiment). 

1. Select a the IBM-Employee-Attrition dataset that you had created above.

1. Preview data and keep all columns selected for training.

1. Select the training job type: **Classification**
1. Select target column: **Attrition**

1. Open “**Advanced settings**”, set the 'Primary metric' to 'AUC_weighted' and training job time to 15 minutes (for the workshop).

![additional_configurations](additional_configurations.png).

Background information on additional configurations
•	**Primary metric**: Evaluation metric that the machine learning algorithm will be measured by.
•	**Automatic featurization**: Enables preprocessing. This includes automatic data cleansing, preparing, and transformation to generate synthetic features.
•	**Blocked algorithms**: Algorithms you want to exclude from the training job
•	**Exit criterion**: If a criteria is met, the training job is stopped.
•	**Validation**: Choose a cross-validation type and number of tests.
•	**Concurrency**: The maximum number of parallel iterations executed per iteration

Good to know: Preparation takes **10-15 minutes** to prepare the experiment run. Once running, it takes **2-3 minutes more for each iteration.**
Select **Refresh** periodically to see the status of the run as the experiment progresses.

1. Hit "**Start**" and wait for the training job to start. You’ll be able to see the models which are created during the run, click on any of the models to open the detailed view of that model, where you can analyze the [graphs and metrics](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-understand-automated-ml).

1. Once the run is completed, click **deploy the best model** to create a deployed endpoint from the model.


To learn more about automated ML, see documentation [here](https://docs.microsoft.com/en-us/azure/machine-learning/service/concept-automated-ml).

Optional Tasks:
- Once your model has been deployed, follow these [instructions](https://docs.microsoft.com/en-us/power-bi/service-machine-learning-integration) to consume the model from Power BI.

- Try the sample notebooks [here](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/automated-machine-learning).