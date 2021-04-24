SHELL := /bin/bash # change shell
PYTHON = python3 # difine python variable
.PHONY = help setup test run clean

# Defining an array variable
FILES = app.py
.DEFAULT_GOAL = help

help:
	@echo "----------------------------Documents----------------------------"
	@echo "------To setup virtualenv for the project type 'make venv'-------"
	@echo "------To build the project type 'make build'---------------------"
	@echo "------To run the project type 'make run'-------------------------"
	@echo "-----------------------------------------------------------------"

venv:
	@echo "Create and build virtualenv for development"; \
	virtualenv -p python3 venv; \
	source venv/bin/activate; \
	pip install -r requirements.txt;

install:
	pip install black
	pip install flake8
	pip install virtualenv

build: clean venv help
	@echo "Build package for development"; \

convention:
	@echo 'Refactor your file according to Flake8 !'
	flake8 .
	black ${FILES}	
run:
	${PYTHON} ${FILES}

clean:
	@echo "Clean development environment"; \
	find . -path "*/*.pyc"  -delete
	rm -rf build; \
	rm -rf dist; \
	rm -rf *.egg-info; \
	rm -rf venv;
