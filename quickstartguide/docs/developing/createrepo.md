# Creating own repository

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
    
## Create your new repository folder

  - all repositories are to be located  in `sostrades-dev-tools/models`, 
    so add a folder for your new repositories in there<br> 
    `cd ...\sostrades-dev-tools\models`<br>
    `mkdir <your-new-repository>`<br>
    
  - add a `__init__.py` empty file<br>
    `cd <your-new-repository>`<br>
    `type NUL > __init__.py`<br>
    
## Update your virtual environment

  - open file `.../sostrades-dev-tools/.venv/Lib/site-packages/sostrades.pth`<br>
    `cd ...\sostrades-dev-tools` <br>
    `notepad .venv/Lib/site-packages/sostrades.pth`
  
  - add a line with the full path to your new **repository** at the end of the file,<br>
    the line you add should look like something like this<br>
    `C:\Users\<yourlogin>\...\git\sostrades-dev-tools\models\<your-new-repository>`
  
## Update your VS Code Configuration

  - Open the file`.../sostrades-dev-tools/.vscode/settings.json`<br>
    `cd ...\sostrades-dev-tools`<br>
    `notepad platform\sostrades-webapi\sos_trades_api\configuration_template\configuration.json`
    
  - Add your repository to the python.analysis.extraPaths section<br>
    `"python.analysis.extraPaths": [
        "./platform/sostrades-core",
        "./platform/sostrades-ontology",
        "./platform/sostrades-webapi",
        "./platform/sostrades-webgui",
        "./models/sostrades-optimization-plugins",
        "./models/witness-core",
        "./models/witness-energy",
        "./models/<your-new-repository>"
    ]`

