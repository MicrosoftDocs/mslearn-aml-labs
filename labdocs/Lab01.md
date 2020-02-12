# Lab 1: Getting Started with Azure Machine Learning

In this exercise, you will create the Azure Machine Learning workspace and a compute instance, and clone the lab files to your workspace. You'll then run a simple Python experiment in your workspace.

## Before You Start

Azure Machine Learning (Azure ML) is a Microsoft Azure-based service for running data science and machine learning workloads at scale in the cloud. To use Azure Machine Learning, you will need an Azure subscription. If you do not already have one, you can sign up for a free trial at [https://azure.microsoft.com](https://azure.microsoft.com).

## Create an Azure Machine Learning Workspace

As its name suggests, a workspace is a centralized place to manage all of the Azure ML assets you need to work on a machine learning project.

1. Sign into the [Azure portal](https://portal.azure.com) and create a new resource - search for "machine learning" and select **Machine Learning**. Specify a unique workspace name, create a new resource group in the region nearest to your location, and select the **Enterprise** workspace edition.

   > **Note**: Basic edition workspaces have lower cost, but don't include capabilities like Auto ML, the Visual Designer, and data drift monitoring. For more details, see [Azure Machine Learning pricing](https://azure.microsoft.com/pricing/details/machine-learning/).

2. When the workspace and its associated resources have been created, view the workspace in the portal. You can manage workspace assets in the Azure portal, but for data scientists, this tool contains lots of irrelevant information and links that relate to managing general Azure resources. An alternative, Azure ML-specific web interface for managing workspaces is available.
3. In the Azure portal blade for your Azure Machine Learning workspace, click the link to launch **Azure Machine Learning studio**; or alternatively, in a new browser tab, open [https://ml.azure.com](https://ml.azure.com). If prompted, sign in using the Microsoft account associated with your Azure subscription and select your Azure subscription and workspace.
4. View the Azure Machine Learning studio interface for your workspace - you can manage all of the assets in your workspace from here.

## Create a Compute Instance

You can perform many machine learning tasks in the *Studio* interface, but it's also important to be able to script configuration tasks and data experiments to make them easier to repeat and automate. *Compute Instances* provide a virtual machine that you can use as a hosted development workstation to do this.

1. In the Azure Machine Learning studio web interface for your workspace, view the **Compute** page. This is where you'll manage all the compute targets for your data science activities.
2. On the **Compute Instances** tab, add a new compute instance, giving it a unique name and using the **STANDARD_DS3_V2** VM type template. You'll use this VM as a development environment.
3. If necessary, click **Refresh** periodically until the compute instance you created has started. Then click its **Jupyter** link to open Jupyter Notebooks on the VM.
4. In the notebook environment, on the **New** menu, click **Terminal**. This will open a new tab with a command shell.
5. The Azure Machine Learning SDK is already installed in the compute instance image, but it's worth ensuring you have the latest version, with the optional packages you'll need in this lab; so enter the following command to update the SDK packages:

    ```bash
    pip install --upgrade azureml-sdk[notebooks,automl,explain]
    ```

    > **More Information**: For more details about installing the Azure ML SDK and its optional components, see the [Azure ML SDK Documentation](https://docs.microsoft.com/python/api/overview/azure/ml/install?view=azure-ml-py).

6. Next, run the following commands to change the current directory to the **Users** directory, and retrieve the notebooks you will use in this lab:

    ```bash
    cd Users
    git clone https://github.com/microsoftdocs/mslearn-aml-labs
    ```

7. After the command has completed, close the terminal tab and view the home page in your Jupyter notebook file explorer. Then open the **Users** folder - it should contain an **mslearn-aml-labs** folder, containing the files you will use in the rest of this lab.

## Use the Azure Machine Learning SDK in a Notebook

1. In the **Users/mslearn-aml-labs** folder, open the **01-Getting_Started_with_Azure_ML.ipynb** notebook. Then read the notes in the notebook, running each code cell in turn.
2. When you have finished the lab, close all Jupyter tabs and **Stop** your compute instance to avoid incurring unnecessary costs.
