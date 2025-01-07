---
date:
  created: 2024-12-11
draft: true
---

These basic instructions will install simply sostrades core on your local platform.
It will enable you to run studies with a minimum setup, not benefiting but not needing neither any cloud, access rights, traceability or interactive GUI.

# Basic install

## Setting up your environment

- Check or install basic development blocs

> `sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl`


- Install [pyenv](https://github.com/pyenv/pyenv) (guidelines below are from [RealPython article](https://realpython.com/intro-to-pyenv/) ). This will allow you avoid interferences between various versions of python and libraries that might be installed on your local platform...

> `curl https://pyenv.run | bash`


- Install Python3.9 using pyenv (yes, we have moving to a higher version of python in our dolist :-)

> `pyenv install 3.9.21`

- Install Python virtual environment and activate it (if you need to deactivate it later, you can just type `deactivate`, which is an alias that the `activate` script will have created). Again this will allow you to have a specific set of libraries installed for your python interpreter without interferences.

> `python -m venv <venv directory>`
>
> `source <venv directory>/bin/activate`


## Clone sostrades-core and install on your local system

- Clone [sostrades-core](https://github.com/os-climate/sostrades-core) to your local disk

> `git clone https://github.com/os-climate/sostrades-core.git`

- Install needed python libraries requirements for sostraces-core through pip

> `pip install -r sostrades-core/requirements.in`

- Run the setup

> `cd sostrades-core; python setup.py install`

## Test your setup :-)

test: python

bla bla
