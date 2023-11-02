# Ensembl Python Template

[![Documentation Status](https://readthedocs.org/projects/template-python/badge/?version=latest)](http://template-python.readthedocs.io/en/latest/?badge=latest) [![Build Status](https://travis-ci.com/Ensembl/template-python.svg?branch=main)](https://travis-ci.com/Ensembl/template-python)

Ensembl Python project template.

This repo structure can be forked and used as the base template for developing a Python package (app or library). It contains boilerplate code and configuration for unit testing, linting, type checking, automatic documentation and CI/CD.

## Getting Started

This template is a simple but fully functioning Python project.

### Template Project Layout

```
.
├── .gitignore             <- File patterns to be ignored by Git
├── docs                   <- Folder with boilerplate for auto-generated Sphinx docs
│   ├── setup
│   │   ├── build_docs.sh  <- Script to generate modules files and build docs
│   │   └── Makefile
│   └── source
│       ├── _static
│       │   └── style.css
│       ├── _templates
│       │   └── layout.html
│       ├── conf.py        <- Sphinx configuration
│       ├── index.rst
│       ├── install.rst
│       └── license.rst
├── LICENSE                <- License text
├── NOTICE                 <- Notice file (required by License)
├── pyproject.toml         <- This project and Python tools packaging configuration
├── README.md              <- This file
├── setup.py               <- Setuptools stub required to install the project in dev mode
├── src                    <- Root folder for this project source code
│   └── ensembl
│       └── template
│           ├── __init__.py
│           └── hello_world.py
└── tests                <- Root folder for tests code
    └── test_hello_world.py
```

### Creating a new project

The best and easiest way to use this template is to go to [GitHub](https://github.com/Ensembl/template-python) and on the top right click on the button "Use this template -> Create a new repository" and follow the steps to create your own repository based on the code found here.

Alternatively, you can also clone this repository:
```
git clone --depth 1 --branch main https://github.com/Ensembl/template-python.git
```

Next, remove the `git` repository data and rename the main folder:
```
rm -rf template-python/.git
mv template-python <NEW_PROJECT_NAME>
cd <NEW_PROJECT_NAME>
git init
```

Later, the following files (or folder names) will need to be modified:
- `NOTICE`: Substitute "Ensembl Python Template" with your project's name
- `pyproject.toml`: Change package name and other settings
- `docs/conf.py`: Change accordingly to project's name
- `docs/install.rst`: Change installation instructions accordingly
- `README.md`: Write a meaningful README for your project

Finally, once done with the basic customisation, create the initial commit:
```
cd <NEW_PROJECT_NAME>
git add .
git commit -m 'Initial commit'
```

### Installing the development environment (with pyenv)

```
pyenv virtualenv <PYTHON_VERSION> <VIRTUAL_ENVIRONMENT_NAME>
cd <NEW_PROJECT_NAME>
pyenv local <VIRTUAL_ENVIRONMENT_NAME>
pip install -e .[dev]
```

### Testing

Run test suite:
```
cd <NEW_PROJECT_NAME>
pytest
```

To run tests, calculate and display testing coverage stats:
```
cd <NEW_PROJECT_NAME>
coverage run -m pytest
coverage report -m
```


### Generate documentation
```
cd <NEW_PROJECT_NAME>
./docs/setup/build_docs.sh
```
Open automatically generated documentation page at `docs/_build/html/index.html`


### Automatic formatting
```
cd <NEW_PROJECT_NAME>
black --check src tests
```
Use `--diff` to print a diff of what Black would change, without actually changing the files.

To actually reformat all files contained in `src` and `test`:
```
cd <NEW_PROJECT_NAME>
black src tests
```


### Linting and type checking
```
cd <NEW_PROJECT_NAME>
pylint src tests
mypy src tests
```
`pylint` will check the code for syntax, name errors and formatting style. `mypy` will use type hints to statically type check the code.

It should be relatively easy (and definitely useful) to integrate both `pylint` and `mypy` in your IDE/Text editor.


## Useful resources

### Python Documentation
- [Official Python Docs](https://docs.python.org/3/)

### Python distributions and virtual environments management
- [Pyenv docs](https://github.com/pyenv/pyenv#readme)
- [Pyenv virtualenv docs](https://github.com/pyenv/pyenv-virtualenv#readme)

### Auto-generating documentation
- [Spinx Docs](https://www.sphinx-doc.org/en/master/index.html)

### Linting, type checking and formatting
- [Pylint](https://www.pylint.org/)
- [Mypy](https://mypy.readthedocs.io/en/stable/)
- [Black](https://black.readthedocs.io/en/stable/)
- [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html#38-comments-and-docstrings)

### Testing
- [pytest](https://docs.pytest.org/en/6.2.x/)
- [Coverage](https://coverage.readthedocs.io/)

### Development tools
- [IPython](https://ipython.org/)

### Distributing
- [Packaging Python](https://packaging.python.org/tutorials/packaging-projects/)
- [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0#apply)
- [Semantic Versioning](https://semver.org/)
