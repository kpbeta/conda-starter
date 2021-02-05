# stoch


### Setup

*To be used for the first time only - while creating this project on your computer.*

Initialize the conda environment.

```
    conda env create --prefix ./conda-env --file conda-environment.yml
```

---
### Instructions to switch into, install packages and switch

To start working on the project, get into the project folder and activate the project conda environment
```
    cd /path/to/project
    conda activate --prefix ./conda-env
```
The environment is activated. You should see `(/path/to/project/conda-env)` on the prompt on your terminal. You can start working on the project.

To add or remove packages, add or remove dependencies in `conda-environment.yml` file.
```
dependencies:
  - jupyterlab=1.2
  - pip=20.0
  - python=3.7
  - pandas=1.2   ## new package to be added
```
Save the file and update the environment.
```
    conda env update --prefix ./conda-env --file conda-environment.yml --prune
```
The above command updates the environment by adding the package.

**Alternatively**, if you want to install all packages fresh after cleaning the existing environment, run the following:
```
    conda env update --prefix ./conda-env --file conda-environment.yml --force
```

To stop working on the project and switch out of it, deactivate the environment.
```
    conda deactivate
```
You should see `(base)` on the prompt on the terminal now.

*You are done working for now. Go have fun. :)*

---
### Important instruction to run this program on PyCharm or similar IDE
Once the conda environment has been created by using the SETUP step above. You have to configure the interpreter to use
the existing `conda-env` environment.

---
### Pip with Conda
You can and, at times, have to use `pip` with `conda`. Refer to this documentation to understand the process.
[Anaconda Blog on Pip within Conda](https://www.anaconda.com/blog/using-pip-in-a-conda-environment)
