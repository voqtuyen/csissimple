SHELL:= /bin/bash

.PHONY: linting formatting help docs build clean venv

PYTHON=python3

.DEFAULT_GOAL=help

# Define Macros
ACT=source venv/bin/activate

build:
	@. venv/bin/activate; \
	echo "Build pylint package"; \
	pip install pylint; \
	echo "--> Done"; \
	echo "Build yapf package"; \
	pip install yapf; \
	echo "--> Done";


venv:
	@echo "Create new environment"; \
	${PYTHON} -m venv venv; \
	echo "--> Done";


docs:
	@echo "Docs"


help:
	@echo "--------------HELP---------------"
	@echo "Usage: make [OPTION]"
	@echo "Mandatory arguments:"
	@echo "		build		Builds project's dependencies"
	@echo "		docs		Project's documentations"
	@echo "		help		Usage guide"
	@echo "		clean		Cleans build packages"
	@echo "		formatting	Formats python code automatically to conform to the \
		PEP8 style guide."
	@echo "		linting		Highlights syntactical and stylistic problems in \
		python source code."
	@echo "---------------------------------"


clean:
	rm -r venv


linting:
	echo "------------Linting--------------"; \
	${ACT}; \
	FILES=$$(find ./person -iname "*.py"); \
	echo "$${FILES}"; \
	pylint $${FILES};


formatting:
	echo "----------Auto-Formating---------"; \
	$(ACT); \
	yapf --recursive ./person --in-place;
