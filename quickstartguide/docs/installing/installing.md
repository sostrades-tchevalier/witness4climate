# Installing SoSTrades platform

You will need approximately 10GB of disk space to install the platform.


## Clone sostrades-dev-tools

  - select or create the base folder you want to install in and open a command prompt in it<br>
    You need the **path to this folder to have no spaces in it**, and be writable for you and the installation scripts you will launch.<br>
    `cd <my-installation-folder-path>`

  - clone sostrades-dev-tools in it<br>
    `git clone https://github.com/os-climate/sostrades-dev-tools`

## Install the platform
  
  <small> You might see some error messages concerning instalation of PETSC library, which you can ignore : <br>
          PETSC is a library for big matrix resolution on parallel super-computers - which you laptop is not anyway :-) </small>
          
  - move in the sostrades-dev-tools that was just created<br>
    `cd sostrades-dev-tools`
  
  - run the `PrepDevEnv.py` script from there **using your Python3.9.13 executable** <br>
    to create the development environment<br>
    `<path_to_python_3.9_executable> scripts\PrepareDevEnv.py`
    
## Create and activate a Python virtual environment

  - run the `PrepareVenv.py` script **using your Python3.9.13 executable** <br>
    to create a specific python virtual environment<br>
    `<path_to_python_3.9_executable> scripts\PrepareVEnv.py`
    
  - activate the virtual environment <br>
    `.\.venv\Scripts\activate`<br>
    You should see a `(.venv)` appear at the beginning of yout DOS prompt
    From there you can just inivoke `python` and in this virtual environment
    your python3.9 executable used to create the virtual environment will be used
    
  <font color="#ff0000"> **Every time you want to work with SoSTrades to develop or use the platform,<br>
    activate this virtual environment first by reruning this `.\.venv\Scripts\activate` command** </font>
    
## Configure and initialize the platform
  
  <small>We now directly use `python`instead of `<path_to_python_3.9_executable>` as we are in the proper virtual environment</small>
  
  - run the `Configuration.py` script (always from sos-trades-dev folder as previously)<br>
    `python scripts\Configure.py`
    
  - run the `NodeInstallation.py` script to install NVS local webserver capability<br>
    `python scripts\NodeInstallation.py`<br>
    At the end of the script it will ask you if you want to install NVS to build the web gui : answer yes
    
  - run the `CreateUser.py` script to create a local user account for you<br>
    `python scripts\CreateUser.py`<br>
    The script will ask you to input some information (user, name, last name and e-mail) : 
    leaving any of these fields empty will result in the script crashing, at least a character is required.<br>
    <br>
    <p>**The user you entered will need to be used when accessing the platform<br>
      The password you will need to connect is in a file located in <br>`sostrades-dev-tools\platform\sostrades-webapi\sos_trades_api\secret\`<br>
      You should keep both :-)**</p>
  
  - run the `UpdateOntology.py` script to initialize the ontology of parameters, models and processes :<br>
    `python scripts\UpdateOntology.py`<br>
  
    


    
    