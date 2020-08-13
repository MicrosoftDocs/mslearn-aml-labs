# Analyzing and Mitigating Unfairness in Models

Machine learning models can often encapsulate unintentional bias that results in unfairness. For example, a machine learning model that predicts whether or not a patient should be tested for diabetes may predict more accurately for some age groups than others, with the result that a subsection of the patient population is either deprived of appropriate preventative health checks or subjected to unnecessary clinical testing.

## Before You Start

Before you start this lab, ensure that you have completed the *Create an Azure Machine Learning Workspace* and *Create a Compute Instance* tasks in [Getting Started with Azure Machine Learning](Lab01.md). Then return to this lab.

## Use FairLearn to analyze and mitigate unfairness

In this task, you'll train a model and use the **Fairlearn** package to analyze it for disparity of predictive performance across specific subsections of the population. You'll also integrate FairLearn analysis into an Azure Machine Learning workspace.

> **Note**: The Fairlearn package used in this exercise has dependencies on specific versions of common Python packages. To avoid potential conflicts, you're going to create a separate Conda environment and associated Jupyter kernel specifically for this exercise.

1. In [Azure Machine Learning studio](https://ml.azure.com), view the **Compute** page for the workspace you created in the [Getting Started with Azure Machine Learning](Lab01.md) lab; and on the **Compute Instances** tab, ensure your compute instance is running. If not, start it.
2. When the compute instance is running, click the **Jupyter** link to open the Jupyter home page in a new browser tab.
3. In the notebook environment, on the **New** menu, click **Terminal**. This will open a new tab with a command shell.
4. In the terminal, enter the following commands to create a new Conda environment and Jupyter kernel that includes all of the packages you need to work with FairLearn.

    ```
    conda create -y -n fair python=3.6 scikit-learn pandas numpy
    conda activate fair
    pip install azureml-sdk[notebooks] azureml-contrib-fairness fairlearn==0.4.6
    conda install -y ipykernel
    ipython kernel install --user --name=aml-fair
    conda deactivate
    ```

5. In the Jupyter home page, in the **Users/mslearn-aml-labs** folder, open the **11-Fairlearn.ipynb** notebook.
6. Make sure the notebook is connected to the **aml-fair** kernel. Then read the notes in the notebook, running each code cell in turn.

    > **Tip**: If you cloned the repository previously, and the notebook file is not in the **Users/mslearn-aml-labs** folder, open a new terminal in your Jupyter environment and run the following commands to refresh the lab files (overwriting any changes you have made):

    ```bash
    cd Users/mslearn-aml-labs
    git reset --hard HEAD
    git pull
    ```

> **Important**: When you have finished the lab, close all Jupyter tabs and **Stop** your compute instance to avoid incurring unnecessary costs.
