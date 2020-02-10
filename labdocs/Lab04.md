# Working with Compute

Azure Machine Learning provides a flexible approach to defining the execution context for experiment scripts. In this lab, you'll explore *environments* and *compute targets*.

## Before You Start

Before you start this lab, ensure that you have completed the *Create an Azure Machine Learning Workspace* and *Create a Compute Instance* tasks in [Getting Started with Azure Machine Learning](Lab01.md). Then return to this lab.

## Manage Compute Contexts for an Experiment

In this task, you'll create an environment and provision a compute target on which to run experiments.

1. In [Azure Machine Learning studio](https://ml.azure.com), view the **Compute** page for your workspace; and on the **Compute Instances** tab, ensure your compute instance is running. If not, start it.
2. When the compute instance is running, click the **Jupyter** link to open the Jupyter home page in a new browser tab.
3. In the Jupyter home page, in the **Users/mslearn-aml-labs** folder, open the **04-Working_with_Compute.ipynb** notebook. Then read the notes in the notebook, running each code cell in turn.

    > **Tip**: If you cloned the repository previously, and the notebook file is not in the **Users/mslearn-aml-labs** folder, open a new terminal in your Jupyter environment and run the following commands to refresh the lab files (overwriting any changes you have made):

    ```bash
    cd Users/mslearn-aml-labs
    git reset --hard HEAD
    git pull
    ```

> **Important**: When you have finished the lab, close all Jupyter tabs and **Stop** your compute instance to avoid incurring unnecessary costs.
