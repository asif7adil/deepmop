# HSPC Deep learning

<p align="center">
    <em>Deep learning modeling for hspc </em>
</p>

## Project Description

This project aims to develop deep learning models for predicting the HSPC mobilization response to G-CSF treatment. 
## Environment Setup

As this project contains both R and Python code, we will use conda to manage the environment. The `environment.yml` file contains the necessary packages for both languages.

### Python

We're primarily using Makefile to manage the environment and requirements. The `Makefile` contains the necessary commands to create the environment and install the requirements.

To create the environment, run the following command:

```bash
make create_environment
```

To activate the environment, run the following command:

```bash
conda activate dl_hspc
```

If you need to install a new package, you can either add it to the `environment.yml` file and run the following command:

```bash
make requirements
```

or you can run the following command:

```bash
conda install -n hspc package_name
```

And then record the new package in the `environment.yml` file manually.

### R

For R, we will use the `renv` package to manage the environment. The `renv.lock` file contains the necessary packages for R.

To restore the R environment, run the following command:

```R
renv::restore()
```

When you run the `renv::restore()` command, it will create a new environment with the necessary packages. You can activate the environment by running the following command:

```R
renv::activate()
```

Furthermore, running R console from the project root will automatically activate the environment.

To install the necessary packages, run the following command:

```R
renv::install("package_name")
```

To save the environment, run the following command:

```R
renv::snapshot()
```

This will update the `renv.lock` file with the new packages.


## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make create_environment` or `make requirements`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for processing.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see mkdocs.org for details
│
├── notebooks          <- Jupyter or Quarto notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for hspc.
│                         and configuration for tools like ruff.
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── environment.yml   <- The requirements file for reproducing the analysis environment.
│
└── hspc                <- Source code for use in this project.
    │
    ├── __init__.py    <- Makes hspc a Python module
    │
    ├── data           <- Scripts to process data
    │   └── make_dataset.py
    │
    └── visualization  <- Scripts to create exploratory and results oriented visualizations
        └── visualize.py
```

---

## Contributing

As this is a collaborative project, we encourage the use of separate branches for each new feature or bug fix. Once the feature or bug fix is complete, a pull request can be opened to merge the changes into the main branch.

---

<small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">Cookiecutter Data Science project template</a>. #cookiecutterdatascience</small>
