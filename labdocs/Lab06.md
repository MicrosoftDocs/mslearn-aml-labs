# Deploying a Model as a Real-Time Service

There's no point in training and registering models if you don't plan to make them available for applications to use. In this lab, you'll deploy a model as a web service for real-time inferencing.

## Before You Start

Before you start this lab, ensure that you have completed the *Create an Azure Machine Learning Workspace* and *Create a Compute Instance* tasks in [Getting Started with Azure Machine Learning](Lab01.md). Then return to this lab.

## Create a Real-time Inferencing Service

In this task, you'll create a real-time inferencing service as an Azure Container Instance (ACI).

1. In [Azure Machine Learning studio](https://ml.azure.com), view the **Compute** page for your workspace; and on the **Compute Instances** tab, ensure your compute instance is running. If not, start it.
2. When the compute instance is running, click the **Jupyter** link to open the Jupyter home page in a new browser tab.
3. In the Jupyter home page, in the **Users/mslearn-aml-labs** folder, open the **03-Deploying_a_model.ipynb** notebook. Then read the notes in the notebook, running each code cell in turn.

    > **Tip**: If you cloned the repository previously, and the notebook file is not in the **Users/mslearn-aml-labs** folder, open a new terminal in your Jupyter environment and run the following commands to refresh the lab files (overwriting any changes you have made):

    ```bash
    cd Users/mslearn-aml-labs
    git reset --hard HEAD
    git pull
    ```

> **Important**: When you have finished the lab, close all Jupyter tabs and **Stop** your compute instance to avoid incurring unnecessary costs.
