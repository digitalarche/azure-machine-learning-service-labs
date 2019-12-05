# Visual Studio Code Setup

1. Install [Visual Studio Code](https://code.visualstudio.com/docs/setup/setup-overview) on your machine.

2. Install the latest version of [Anaconda](https://www.anaconda.com/distribution/).

3. Setup a new conda environment for Azure Auto ML. The easiest way to do that is to download the automl_setup script for your machine (Windows-automl_setup.cmd, Linux-automl_setup_linux.sh, Mac-automl_setup_mac.sh) and the YAML file (Windows-automl_env.yml, Linux-automl_env.yml, Mac-automl_env_mac.yml) from the following [GitHub repository](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/automated-machine-learning). Open command prompt or terminal and go to the directory where the two files are saved and run the script file. The script will creates a new conda environment called `azure_automl`, and install the necessary packages.

4. From starter-artifacts navigate to the [visual-studio-code](../../starter-artifacts/visual-studio-code) and download the project files to your local computer. Also remember to maintain the folder structure as shown in `starter-artifacts/visual-studio-code`. During the labs, other files will be either downloaded or created, thus maintaining the folder structure will help keeping the files within their respective lab folders.

5. When you are ready to start a lab: (1) start Visual Studio Code, (2) go to File->Open Menu, and (3) open the **folder** for the lab. For example, to work on `lab-1`, open the folder `01-model-training` from Visual Studio Code. This will ensure that the current working directory for the quickstart is set correctly.  

6. In VS code, when you open a python notebook for the first time, use Select Interpreter command from the Command Palette (⇧⌘P) and select the azure_automl as your interpreter.
