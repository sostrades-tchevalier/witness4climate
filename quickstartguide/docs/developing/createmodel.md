# Creating own model

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

  - move to one of your module's sos_wrapping folder <br>
    `.../sostrades-dev-tools/models/<your repository>/<your-module>/sos_wrapping` <br>
    `cd ...\sostrades-dev-tools\models\<your repository>\<your-module>\sos_wrapping`
    
  - add a folder for your new model <br>
    `mkdir <your-model-name>`<br>
    `cd <your-model-name>`<br>
    `type NUL > __init__.py`<br>
    
  - create a folder for your model documentation<br>
    `mkdir documentation`<br>
    `type NUL > documentation\__init__.py`
    
## Create your model

  - create a file `<your-model-name>_disc.py` in which you will create a class <your-model-name><br>
    following instructions given in [this](https://sostrades-core.readthedocs.io/en/latest/how-to/wrap-model.html) developer's manual section
  
  - you might want to add graphs to your model <br>
    following instructions from [this](https://sostrades-core.readthedocs.io/en/latest/how-to/create-postprocessing.html) developer's manual section
  
  - create a file `documentation\<your-model-name>.md` 
    with your dfocumentation in [markdown](https://www.markdownguide.org/basic-syntax/) format
    
## Update ontology

   - move to `.../sostrades-dev-tools` folder <br>
    `cd ...\sostrades-dev-tools`
    
  - run the `UpdateOntology.py` script to initialize the ontology of parameters, models and processes :<br>
    `python scripts/UpdateOntology.py`<br>

## Check your model appear in the platform

  - start the platform, select the upper-left three horizontal bars and in the menu select Ontology/Models
  
  - Use the Filter to check if your model appears
  
  - select the book icon at the end of your model line in list, to check informations were well retrieved (inputs, outputs, documentation...)
  

  