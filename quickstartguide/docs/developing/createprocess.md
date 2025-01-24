# Creating own process

**A classical error is to forget adding empty `__init__.py` files 
  in all folder to be sure they are processed by platform pythonic explorations: <br>
  be sure there are `__init__.py` files in all your folders !**

## Move to your sos-trades-dev folder and load virtual environment

  - move in the sostrades-dev-tools where the platform was installed<br>
    `cd <path to your installation folder>\sostrades-dev-tools`
  
  - activate the virtual environment <br>
    `.\.venv\Scripts\activate`<br>
    You should see a `(.venv)` appear at the beginning of yout DOS prompt
    
  <font color="#ff0000"> **Every time you want to work with SoSTrades to develop or use the platform,<br>
    activate this virtual environment first by reruning this `.\.venv\Scripts\activate` command** </font>
    
## Create your folder structure in one of your module repository

  - move to one of your module's sos_processes folder <br>
    `.../sostrades-dev-tools/models/<your repository>/<your-module>/sos_processes` <br>
    `cd ...\sostrades-dev-tools\models\<your repository>\<your-module>\sos_processes`
    
  - add a folder for your new process <br>
    `mkdir <your-process-name>`<br>
    `cd <your-process-name>`<br>
    `type NUL > __init__.py`<br>
    
  - create a folder for your process documentation<br>
    `mkdir documentation`<br>
    `type NUL > documentation\__init__.py`
    
## Create your process

  - create a file `process.py` in which you will create a specific process builder<br>
    following instructions given in [this](https://sostrades-core.readthedocs.io/en/latest/how-to/create-process.html) developer's manual section
  
  - you might want to create a `usecase.py` file to initialize a reference for your process<br>
    following instructions given in [this](https://sostrades-core.readthedocs.io/en/latest/how-to/create-usecase.html) developer's manual section
  
  - finally create a file `documentation\process.md` 
    with your dfocumentation in [markdown](https://www.markdownguide.org/basic-syntax/) format
    
## Update ontology

   - move to `.../sostrades-dev-tools` folder <br>
    `cd ...\sostrades-dev-tools`
    
  - run the `UpdateOntology.py` script to initialize the ontology of parameters, models and processes :<br>
    `python scripts/UpdateOntology.py`<br>

## Check your process appear in the platform

  - start the platform, select the upper-left three horizontal bars and in the menu select Ontology/Processes
  
  - Use the Filter to check if your process appears
  
  - select the book icon at the end of your model line in list, to check informations were well retrieved (models used, documentation...)
  

  