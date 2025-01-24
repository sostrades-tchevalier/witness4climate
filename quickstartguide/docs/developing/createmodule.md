# Creating own module

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
    
## Create the module folder structure in one of your repositories

  - move to one of your repositories `sostrades-dev-tools/models/<your repository>` <br>
    `cd ...\sostrades-dev-tools\models\<your repository`
    
  - add a folder for your new module in `sostrades-dev-tools/models/<your repository>` <br>
    `mkdir <your-new-module>`<br>
    `cd <your-new-module>`<br>
    `type NUL > __init__.py`<br>
    
  - create a models folder named `sos_wrapping` in your new `<your-new-module>`folder<br>
    `mkdir sos_wrapping`<br>
    `type NUL > sos_wrapping\__init__.py`
    
  - create a processes folder named `sos_processes` in your new `<your-new-module>`folder<br>
    `mkdir sos_processes`<br>
    `type NUL > sos_processes\__init__.py`
    
## Reference your new module on the platform

  - Locate and open the file <br>
    `.../sostrades-dev-tools/platform/sostrades-webapi/sos_trades_api/configuration_template/configuration.json`<br>
    `cd ...\sostrades-dev-tools` <br>
    `notepad platform\sostrades-webapi\sos_trades_api\configuration_template\configuration.json`
    
  - Add your repository module name (e.g. the name you would use in python import) :<br>
    `SOS_TRADES_PROCESS_REPOSITORY": [
         "sostrades_core.sos_processes",
         "sostrades_optimization_plugins.sos_processes",
         "climateeconomics.sos_processes",
         "energy_models.sos_processes",
         "<your-new-module>>.sos_processes"
       ],`
