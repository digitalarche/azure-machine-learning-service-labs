# Lab 0: Setting up your environment 

If a lab environmnet has not be provided for you, this lab provides the instructions to get started in your own Azure Subscription.

The following summarizes the lab requirements if you want to setup your own environment (for example, on your local machine). If this is your first time peforming these labs, it is highly recommended you follow the Quick Start instructions below rather that setup your own environment from scratch.

The labs have the following requirements:
- Azure subscription
- One of the following environments:
    - Visual Studio 2017 and the Visual Studio Tools for AI 
    - PyCharm
    - Azure Databricks Workspace
- For the deep learning lab, you will need a VM or cluster with CPU capabilities.

Depending on which environment you use, there are different requirements. These are summarized as follows:
- Visual Studio 2017 and PyCharm
    - A Python 3.x Anaconda environment named `azureml` with:
        - The latest version of the Azure Machine Learning Python SDK installed. Use `pip install --upgrade azureml-sdk[notebooks,automl] azureml-dataprep` to install the latest version.
        - The following pip installable packages:
            - numpy, pandas, scikitlearn, keras and tensorflow-gpu 
    - For the deep learning lab, make sure you have your GPU drivers properly installed.
- Azure Databricks
    - An Azure Databricks Workspace
    - A two-node Azure Databricks cluster with the following Python libraries attached:
            - numpy, pandas, scikitlearn, keras and tensorflow-gpu

The following sections describe the setup process for each environment.

# Quickstart: Visual Studio 2017 and PyCharm
The quickest way to get going with the labs is to deploy the Deep Learning Virtual Machine (DLVM). 

1. Follow these instructions for [creating an Deep Learning Virtual Machine](https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/provision-deep-learning-dsvm). Be sure you do the following:
    - OS Type: Select Windows 2016
    - Location: Choose a region that provides NC series VM's, such as East US, East US 2, North Central US, South Central US and West US 2. Be sure to visit the [Azure Products by Region](https://azure.microsoft.com/regions/services/) website for the latest.
    - Virtual Machine size: NC6
2. Once the VM is ready, download the remote desktop (RDP) file from the Overview blade of your VM in the Azure Portal and login. If you are unfamiliar with this process, see [Connect to a VM](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/connect-logon).
3. Once you are connected to your DLVM, open the Start Menu and run `Anaconda Prompt`. 
4. Activate the azureml conda environment by running `activate azureml`.
5. To ensure tensorflow uses a GPU, you will need to uninstall and reinstall Keras and Tensorflow in a specific order. Run these commands in sequence:
    - `pip uninstall keras`
    - `pip uninstall tensorflow-gpu`
    - `pip uninstall tensorflow`
    - `pip install keras`
    - `pip install tensorflow-gpu==1.10.0`
 6. Upgrade the installed version of the Azure Machine Learning SDK by running the following command:
    - `pip install --upgrade azureml-sdk[notebooks,automl] azureml-dataprep`
7. If you will be using Visual Studio for the labs, launch Visual Studio 2017 from the Start menu and login with your Microsoft Account. Allow Visual Studio a few moments to get ready. Once you see the Tools for AI Start Page displayed in Visual Studio, the setup is complete.
8. If you will be using PyCharm for the labs, launch PyCharm from the Start menu. Make you intial default selections and once you are at the Welcome to PyCharm new project dialog the setup is complete.
9. Your Virtual Machine is now ready to support any of the labs using either the Visual Studio or PyCharm environments.     


# Quickstart: Azure Databricks