# Python Code Review Automation


## Code Review Tools
### Code Analysis/Linting
- Linting highlights syntactical and stylistic problems in your Python source code, which oftentimes helps you identify and correct subtle programming errors or unconventional coding practices that can lead to errors
- Two most popular python linters: Pylint and Flake8

#### Flake8
Flake8 is a simple wrapper around pyflakes, pycodestyle and mccabe

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
 
#### Pylint
- Install `Pylint`
    ```bash
    pip install pylint
    ```
- Run `Pylint`
    ```
    pylint src    # lint the src directory
    ```

### Automatic Code Formatting
#### Black
- Black is a PEP 8 compliant opinionated formatter. Black reformats entire files in place. It is not configurable. It doesn't take previous formatting into account. Your main option of configuring Black is that it doesn't reformat blocks that start with # fmt: off and end with # fmt: on, or lines that ends with # fmt: skip. Pay attention that # fmt: on/off have to be on the same level of indentation
- Back code style: [reference](https://github.com/psf/black/blob/master/docs/the_black_code_style.md)!
- Usage
  - Install `black`
      ```bash
      pip install black
      ```

  - Run `black` formatter
      ```bash
      black [file/dir]
      ```

#### Autopep8
- Install `autopep8`
    ```bash
    pip install autopep8
    ```

- Run `autopep8` formatter
    ```bash
    autopep8 [file/dir] --in-place
    ```

#### yapf
Yet Another Python Formatter (yapf) is a python formatter from Google based on ideas from gofmt. This is also more configurable and a good option for automatic code formatting.

- Install `yapf`
    ```bash
    pip install yapf
    ```

- Run `yapf` formatter
    ```bash
    yapf [file/dir] --in-place
    ```

## Code Review Automation


## Reference
- https://speakerdeck.com/pycon2018/kyle-knapp-automating-code-quality?slide=15
- https://microsoft.github.io/code-with-engineering-playbook/code-reviews/recipes/Python.html
- https://code.visualstudio.com/docs/python/linting