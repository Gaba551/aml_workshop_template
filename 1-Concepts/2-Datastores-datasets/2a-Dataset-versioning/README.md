# Datasets & versioning in AML

Dataset versioning is a way to bookmark the state of your data so that you can apply a specific version of the dataset for future experiments.

This tutorial consists of two separate steps where the first one is necessary to start an automated ML run based on the first version of the dataset. The second part of the tutorial  focuses on creating a second version of the dataset. 

**When do you version a dataset?**

•	When new data is available for retraining

•	When you're applying different data preparation or feature engineering approaches

## Register and retrieve dataset versions

By registering a dataset, you can version, reuse, and share it across experiments and with colleagues. You can register multiple datasets under the same name and retrieve a specific version by name and version number.

**Good to know:**

•	When you create a dataset version, you're not creating an extra copy of data with the workspace. Because datasets are references to the data in your storage service, you have a single source of truth, managed by your storage service.

•	When you load data from a dataset, the current data content referenced by the dataset is always loaded. If you want to make sure that each dataset version is reproducible, we recommend that you not modify data content referenced by the dataset version. When new data comes in, save new data files into a separate data folder and then create a new dataset version to include data from that new folder.

•	You can use a dataset as the input and output of each Machine Learning pipeline step. When you rerun pipelines, the output of each pipeline step is registered as a new dataset version. Because Machine Learning pipelines populate the output of each step into a new folder every time the pipeline reruns, the versioned output datasets are reproducible.

In the first part of this tutorial you are going to register a dataset which will automatically be versioned as version 1. In the second part of the tutorial it is explained how to create a second version (version 2) of the original dataset (version 1).
