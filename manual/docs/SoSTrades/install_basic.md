---
date:
  created: 2024-12-11
draft: true
---
These basic instructions will install simply sostrades core on your local platform.
They were tested using a fresh LinuxMint21.1 in a VirtualBox with just a round of system & drivers update, plus installing git and vim.
 
# Basic install
 
## Setting up your environment
 
### Check or install basic development blocs
 
  `sudo apt-get install libmysqlclient-dev build-essential libldap2-dev libsasl2-dev python-dev-is-python3 libssl-dev`
 
### Install Python3.9.20 from source tarball

  - get [tarball from python website](https://www.python.org/downloads/release/python-3920/)
 
  - create or complete .local folder in your home directory with the following subfolders:<br> 
    pub, include, src, lib, bin, man
 
  - put the downloaded tarball in ~/.local/pub
 
  - move in the ~/.local/src folder and perform the installation classically
 
    > `tar xzvf ../pub/Python-3.9.20.tgz`  <br>
    > `cd Python-3.9.20`  <br>
    > `./configure --prefix=$HOME/.local`  <br>
    > `make`  <br>
    > `make test`  <br>
    > `make install` <br>
 
  - Use a new shell and check $HOME/.local/bin was added to your $PATH
 
### Install or upgrade pip,, install venv
 
    > `python3.9 -m pip install --upgrade pip`  <br>
    > `pip3.9 install virtualenv`  <br>
 
## Clone sostrades-core and install on your local system
 
  - clone [sostrades-dev-tools](https://github.com/os-climate/sostrades-dev-tools) to your local disk
 
    > `git clone https://github.com/os-climate/sostrades-dev-tools`
 
 
  - run the setup
 
  - move in the sostrades-dev-tools folder you just checked out from git
 
  `~/.local/bin/python3.9 scripts/PrepareDevEnv.py`
 
  `~/.local/bin/python3.9 scripts/PrepareVenv.py`
 
## Test your setup :-)

