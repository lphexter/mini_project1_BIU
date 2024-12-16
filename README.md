# mini_project1_BIU
BIU python class mini project 1 - pandas / numpy practice

Note: using python >=3.13

Files:
1. Hexter_Project1.pynb - all code for the Project1 assignment
2. Additional images: box_plot_RAM.png & iris_features.png - because GitHub doesn't render everything, I included copies of some figures as png
3. laptop_price - dataset.csv - the actual dataset needed for the project
4. mini_project1_BIU.code-workspace: workspace configuration for the project
5. pyproject.toml & tox.ini: configuration files (for requirements and linting)

## On first run:
```bash 
#install Virtualenv is - a tool to set up your Python environments
pip install virtualenv
#create virtual environment (serve only this project):
python -m venv venv
#activate virtual environment
source venv/bin/activate
+ (venv) should appear as prefix to all command (run next command just after activating venv)
#update venv's python package-installer (pip) to its latest version
pip install --upgrade pip
#install projects packages
pip install -e .[dev]     
``` 

## Modify package dependencies (add/remove/update external modules/packages):
#### Add new module:
1. Add package to pyproject.toml
2. Run:
```bash 
pip install -e .[dev]
``` 

#### Remove new module:
1. Remove the package from pyproject.toml
2. Run:
```bash 
pip uninstall <package-name>
```
note: if you're don't remember the exact package name copy it from: 
```bash
pip list
```

#### Steps in case of a package failure:
Cases like package installation interuppted in the middle or something like that
1. Try to remove package and install it again.
2. If it doesn't help delete venv folder 
3. repeat 'On first run' steps


## Health check (Lint):
#### Lint Project:
Check formatting, type hinting, lint code & docstrings
```bash
tox run
```

## Build/pack the project
```bash
python -m build
```
