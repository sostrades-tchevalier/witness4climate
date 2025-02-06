# Understanding the basics

<font color="#ff0000">
  This is just an overview of the local development files organization,
  please follow the next sections for detailed disciplines or models creation :-)
</font>

## From a simple python model to a full study in SoSTrades

![model to discipline to process to use case to study schema](https://www.witness4climate.org/html/images/Model2Study.png "From simple python model to full SoSTrades study")

As shown in the schema above, in oder to be able to use my model in SoSTrades, I'll need to

  - Wrap my model in an SoSTrades *discipline*

  - Optionally add postprocessing graphs to display the model results

  - Optionally add test of my model to be able to embark my model in the DevSecOps pipeline
    (can be ignored if only to be used in local, but still recommended anyway :-)

  - Create a *process* using my discipline

  - Create a *usecase* to define default input data for future studies
    that will be created from this process

  - From there I'll be able to instanciate, run and analyze
    any number of *studies* from the process, with various set of inputs

## Disciplines

Once installed on your local disk, the sostrades-dev-tools should look like this :
![Initial filesystem tree after install](https://www.witness4climate.org/html/images/quickstart-initialtree.png "Initial filesystem tree after install")

  - under `sostrades-dev-tools/models` are *repositories*,
    and you can add your owns as additional folders here as presented in next sections

  - in each *repository*, you'll be able to add *modules* folders or folder trees,
    that are generally used to organize *disciplines* related to same system or subsystem

  - at 'leaves' of this repository tree of modules, are *discipline* folders,
    which SoSTrades will recognize because of containing a file named `<your-discipline-name>_disc.py`

  - in *discipline* folders, you can have a 'documentation' optional subfolder
    in which you can create a `documentation/<your-discipline-name>.md` with your dfocumentation in markdown format
    (this documentation will be made available interactively in the SoSTrades tools if it exists)


So if I created a repository "myrepo" with a module "mymodule" and a discipline "mydiscipline",
the disk structure should look like this:

![Initial filesystem tree after adding discipline](https://www.witness4climate.org/html/images/quickstart-disciplinetree.png "Initial filesystem tree after adding discipline")

(see in the following sections the additional setup to be done to be sure your additional repositories are recognized !)

## Processes

  - in your *module* folder, you can create a `sos_processes` folder to add *processes*

  - for each *process* you want to create, create a folder in the `sos_processes` folder with the name of your process

  - in that `models/<my-repository>/<my-module>/sos_processes/<my-process>` folder,
    you'll need to create a `process.py` file describing the *disciplines* you want to simulate and the namespace in which they interact with others,
    and a `usecase.py` file initializing the default studies created from your process (that you'll see in the GUI as *reference* study)

So if I created a repository "myrepo" with a module "mymodule" and a discipline "mydiscipline", and add a "myprocess" process to it,
the disk structure should look like this:

![Initial filesystem tree after adding process](https://www.witness4climate.org/html/images/quickstart-processtree.png "Initial filesystem tree after adding process")

## __init__.py files !

A classical error is to forget adding empty `__init__.py` files
in all folder to be sure they are processed by platform pythonic explorations: <br>
  be sure there are `__init__.py` files in all your folders !