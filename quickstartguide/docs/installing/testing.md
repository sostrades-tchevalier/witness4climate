# Testing SoSTrades platform installation

## Starting the platform

  - move in the sostrades-dev-tools where the platform was installed<br>
    `cd <path to your installation folder>\sostrades-dev-tools`
  
  - activate the virtual environment <br>
    `.\.venv\Scripts\activate`<br>
    You should see a `(.venv)` appear at the beginning of yout DOS prompt
    
  <font color="#ff0000"> **Every time you want to work with SoSTrades to develop or use the platform,<br>
    activate this virtual environment first by reruning this `.\.venv\Scripts\activate` command** </font>
    
## Start the platform
  
  <small>We now directly use `python`instead of `<path_to_python_3.9_executable>` as we are in the proper virtual environment</small>
  
  - run the `StartSOSTrades.py` script (always from sos-trades-dev folder as previously)<br>
    `python scripts/StartSOSTrades.py`<br>
    This will take a little time and open several windows : follow the last open one (with a "ng serve" tab):<br>
    at some point it will state "Compiled successfully", meaning the platform is up and running
    <small> When running for the first time, you might have to answer a question on whether you want to share data with NVS,<br>
            and you can decide to share or not : it has no influence ou the platform execution.</small>

  **You can repeat this process whenever you want to relaunch the platform**


## Connect to the platform

  - open your browser and enter the following URL : [http://localhost:4200/](http://localhost:4200/) 
  
  - enter the user name provided during installation to `CreateUser.py`script<br>
   and use the password given in <br>`sostrades-dev-tools/platform/sostrades-webapi/sos_trades_api/secret/`
  
  
  **You can repeat this process whenever you want to connect to the platform**

  - at first connection, the home page is empty<br>
   later you'll find both the studies you starred as favorite as well as the last studies opened

     
## Generate a study from an available reference

   <small>To generate a study, you can start from a process which will create a study from scratch and everything to initialize,<br>
          or create a study from a reference which is a study already initialized as a reference which we will be able to tweak.<br>
          Here for testing we will generate from a reference to make testing easier :-) </small>
          
  - click on the top left three horizontal bars to open the menu, <br>
    and select `Study/Reference management` menu
  
  - filter the available references by entering in the toolbar in the "Filter" input field the word DICE<br>
    <small>Dynamic Integrated Climate-Economy model, referred to as the [DICE](https://en.wikipedia.org/wiki/DICE_model) model,
           is a simple neoclassical integrated assessment model developed by 2018 Nobel Laureate William Nordhaus 
           that integrates in the neoclassical economics, carbon cycle, climate science, 
           and estimated impacts allowing the weighing of subjectively guessed costs and subjectively guessed benefits 
           of taking steps to slow climate change. We will use it as a basic test of the platform.</small>
           
  - Move you mouse at the end of the line for the second item refered as "Dice Process" in the "Process" column, 
    until you see 3 icons appearing : a circling arrow icon, a download icon and a setting icon (gear wheel) :
    click on the circling arrow for a regeneration of the reference
    
  - Wait to see the bullet at the begining of the line  move to blue and indicate PENDING instead of initial "NOT GENERATED" state,
    then  update to "RUNNING", then finally to "FINISHED"
    
  - For the same second row which should now indicate FINISHED at the begining of the row, <br>
    select the "+" in the second "Create study" column, <br>
    enter a name for your study (first line), <br>
    and select "All users" for acces sgroup (last line).<br>
    Finally press "Ok" button to create your first study on your local platform.
    
  - After a waiting panel during study loading, you should have your first study on screen !
  