# Installing Python 3.9.13

Python 3.9 is currently required to run SoSTrades platform, and 3.9.13 is the latest version for which a Windows installer is available making it easy for you to install.

## Get Python3.9.13 installer

  - go to [https://www.python.org/downloads/release/python-3913/](https://www.python.org/downloads/release/python-3913/)

  - go at the bottom of the page and select the Windows installer (64-bits) to download it

  - open a command prompt (type command in the search next to the start button)

  - move to your download folder (`cd %HOMEDRIVE%%HOMEPATH%\Downloads`)

  - find the downloaded pyton installer (should be a python-3.9.13-amd64.exe in file there)

  - check the MD5 signature of what you downloaded match the one displayed on the download webpage 
    (currently e7062b85c3624af82079794729618eca but double check !) 
    using windows built-in utility : <BR> `CertUtil -hashfile python-3.9.13-amd64.exe MD5`

## Run the python installer

  - run python-3.9.13-amd64.exe 

  - select the local install (for user only and not for all users)

## Spot the installed python3.9 interpreter 
  It should be located in `C:\Users\<login name>\AppData\Local\Programs\Python\Python39\python.exe` :

  - open your local `AppData` folder.<br>
    <small>Beware it's a hidden folder by default in your user directory, so if you do not see it, you need to go in your File Explorer options menu 
    (select the 3 dots in the toolbar to access options), 
    select the "View" tab and click the "Show hidden files, folders and drives" option</small>

  - Move to `AppData\Local\Programs\Python\Python39` and spot the python.exe file

  - Select it and copy it as path ("Copy as Path" in the contextual menu or Ctrl-Shift-C)
   
  **This python.exe is the one you will have to use for running the SoSTrades installation scripts, <br>
    so you'll have to use the full path to be sure you're using it !**
   