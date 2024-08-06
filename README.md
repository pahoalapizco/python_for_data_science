# Numpy & Pandas for Data Analysis

**Version**: 1.0
**Author**: @pahoalapizco




## Prerequisites
- Anaconda >=4.x 

## Create environment
```bash
conda env create -f environment environment.yml
activate numpy_pandas_da
```

## Set up project's module
To move beyond notebook prototyping, all reusable code should go into the modules/ folder package. To use that package inside your project, install the project's module in editable mode, so you can edit files in the final folder and use the modules inside your notebooks :

```bash
pip install --editable .
```

To use the module inside your notebooks, add `%autoreload` at the top of your notebook :

```python
%load_ext autoreload
%autoreload 2
```

Example of module usage :

```python
from modules.utils.paths import data_dir
data_dir()
```

## Project organization

    numpy_pandas_da
        ├── data
        │   ├── processed      <- The final, canonical data sets for modeling.
        │   └── raw            <- The original, immutable data dump.
        │
        ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
        │                         the creator's initials, and a short `-` delimited description, e.g.
        │                         `1.0-initial-data-exploration`.
        │
        ├── .gitignore         <- Files to ignore by `git`.
        │
        ├── environment.yml    <- The requirements file for reproducing the analysis environment.
        │
        ├── README.md          <- The top-level README for developers using this project.
        │
        ├── setup.py           <- Makes project pip installable (pip install -e .)
        │                          so final can be imported.
        ├── .here              <- File that will stop the search if none of the other criteria
        │                         apply when searching head of project.
        │
        └── modules              <- Source code for use in this project.
            └── utils          <- Scripts to help with common tasks.
                └── paths.py   <- Helper functions to relative file referencing across project.

---