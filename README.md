
A Python project demonstrating **software quality control** using a simple Rock-Paper-Scissors game.  
This project shows how to structure code, manage dependencies, and test functionality with `pytest`.

---

## 📘 Overview

The repository contains:
- **apps/rps.py** – main game logic  
- **test/test_rps.py** – automated test cases  
- **pytest.ini** – test configuration  
- **requirements.txt** – project dependencies  

---

## Setup Instructions

### 1. Create a virtual environment
```
```bash
conda create -n quality-control python=3.11

### 2. activeate a virtual environment
conda activate quality-control

### 3. instal dependencies
pip install -r requirements.txt
```

including: 
pandas
python-dotenv
plotly
pytest


### 5. Run Game
```
python -m apps.rps
```


### 7. Run test

pytest -v


### Secret Credentials

For the stocks dashboard, you will need to acquire a "premium" [AlphaVantage](https://www.alphavantage.co/) API key (from the prof) and supply it as an environment variable. Create a local ".env" file and place inside contents like the following:

```sh
# this is the ".env" file...

# replace "demo" with your premium key:
ALPHAVANTAGE_API_KEY="demo"
```

Also, for the stocks tests to work on GitHub Actions, you will need to set a repository secret named `ALPHAVANTAGE_API_KEY` via the repository's settings on GitHub.

## Configuration

The stocks functionality requires an AlphaVantage API key. Obtain a premium AlphaVantage API Key (using the [form](https://www.alphavantage.co/support/#api-key) or shared by the prof).

Create a local ".env" file and store your environment variable in there:


```sh
# this is the ".env" file...

ALPHAVANTAGE_API_KEY="______________"



# This workflow will install Python dependencies, run tests and lint with a single version of Python
# For more information see: https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-python

name: Python application

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

permissions:
  contents: read

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v4
    - name: Set up Python 3.10
      uses: actions/setup-python@v3
      with:
        python-version: "3.10"
    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install flake8 pytest
        if [ -f requirements.txt ]; then pip install -r requirements.txt; fi
    - name: Lint with flake8
      run: |
        # stop the build if there are Python syntax errors or undefined names
        flake8 . --count --select=E9,F63,F7,F82 --show-source --statistics
        # exit-zero treats all errors as warnings. The GitHub editor is 127 chars wide
        flake8 . --count --exit-zero --max-complexity=10 --max-line-length=127 --statistics
    - name: Test with pytest
      env:
        # set environment variables to use during testing
        # ... using the repository secret values set securely via repo settings
        ALPHAVANTAGE_API_KEY: ${{ secrets.ALPHAVANTAGE_API_KEY }}
      run: |
        pytest



Run the stocks dashboard:

```sh
python -m apps.stocks
```


