# Virtual Environment Cheatsheet
## Installation 
This will install python if you don't already have it 

    sudo add-apt-repository ppa:deadsnakes/ppa.
    sudo apt-get update.
    sudo apt-get install python3.x.

### To install Venv: Only for python versions 3.x:
Venv is the standard virtual environment package. Every python distribution has its own venv and development tools. The command below will install venv for a particular python version. 

    sudo apt-get install python3.x-devel
    
### To install Virtualenv: For all python versions:
Virtualenv is a 3rd party library and it has one version which supports all of the python distributions. The command below can be run after installing python and  will install the library.

    pip install virtualenv

## Creating a new project with a virtual Environment
### Venv tool
The following command can be executed in the terminal to create a new virtual Environment called my_venv.
   
    python -m venv path/to/my_venv 

The next command will activate the Environment.

    source path/to/my_venv /Scripts/activate

Then your terminal username should have the "(my_venv)" prefix. 

    (my_venv) jackwarren@gypsum:~/Documents/repos/Point-GNN$

You can deactivate the environment at any time with the simple command:

    deactivate 

### Virtualenv
The following command can be executed in the terminal to create a new virtual Environment called my_venv.
   
    virtualenv --python="path/to/python/.exe" path/to/my_venv 

The next command will activate the Environment.

    source path/to/my_venv/bin/activate

Then your terminal username should have the "(venv)" prefix. 

    (my_venv) jackwarren@gypsum:~/Documents/repos/Point-GNN$

You can deactivate the environment at any time with the simple command:

    deactivate 

Now, this terminal will only access libraries that have been installed when the virtual env was activated. 

## Publishing A Project  
To check what libraries you have installed in your python virtual environment, you can run this command with the virtual environment activated to print out all libraries and versions.

    pip freeze

Good practice is to create a "requirements.txt" file in your project which will allow for anyone to set up the environment on there local machine. This can be done with the following command.

    pip freeze > requirements.txt

## Creating a Virtual environment from a requirements.txt

After creating a new virtual environment and activating it in the terminal, the following command can executed in the terminal with the requirements.txt file.

    pip install -r requirements.txt
