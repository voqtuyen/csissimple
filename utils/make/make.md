# Use Makefile in Python project

## Overview

### make
- The make utility is a software engineering tool for managing computer programs. It is most useful when a program has many parts. To simplify compiling and linking, make reduces human errors (e.g., typos, incorrect file names) and automatically knows when it is necessary to re-build one or more of the files.
    - For example, we normally need to do the following commands to create a virtual environment for python project.

        ```python3
        virtualenv -p python3 venv
        source venv/bin/activate
        pip install -r requirements.txt
        ```
    - Could we create a command alias for those commands? Yes, define this rule inside a makefile.
        ```makefile
        venv:
            virtualenv -p python3 venv
            source venv/bin/activate
            pip install -r requirements.txt
        ```

- You can use *make* with any programming language whose compiler can be run with a shell command. Indeed, *make* is not limited to programs. You can use it to describe any task where some files must be updated automatically from others whenever the others change.

### makefile

- You need a file called a *makefile* to tell make what to do. Most often, the *makefile* tells make how to compile and link a program.

## Practice



## Reference

- https://www.gnu.org/software/make/manual/make.html#Reading
- https://cs.utsa.edu/sites/default/files/2020-05/UnixMakeUtility.pdf