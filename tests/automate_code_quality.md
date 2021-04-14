# Python Code Reviews


## Code Analysis/Linting
- Linting highlights syntactical and stylistic problems in your Python source code, which oftentimes helps you identify and correct subtle programming errors or unconventional coding practices that can lead to errors
- Two most popular python linters: Pylint and Flake8

### Flake8
Flask8 is a simple wrapper around pyflakes, pycodestyle and mccabe

- Install `Flake8`
    ```bash
    pip install flake8
    ```
- Add an extension for the `pycodestyle` (doc strings) tool to flake8

    - Install `flake8-docstrings`
        ```bash
        pip install flake8-docstrings
        ```
    - You can set the pydocstyle convention at the command line. Possible conventions are: pep257, numpy, google.
        ```bash
        flake8 --docstring-convention google .
        ```
- Add an extension for `pep8-naming` (naming convention) tool to flake8
    ```bash
    pip install pep8-naming
    ```
- Run flake8:
    ```bash
    flake8 .        # lint the whole project
    flake test.py   # lint test.py file
    ```
 
### Pylint

# Code Formatting



## Reference
- https://speakerdeck.com/pycon2018/kyle-knapp-automating-code-quality?slide=15
- https://microsoft.github.io/code-with-engineering-playbook/code-reviews/recipes/Python.html
- https://code.visualstudio.com/docs/python/linting