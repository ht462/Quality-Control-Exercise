# Quality Control — Python Software Project

A Python project demonstrating "software quality control" using a simple Rock-Paper-Scissors game and a Stocks Dashboard.  

##  Overview

The repository contains:

- `apps/rps.py` — main Rock-Paper-Scissors game logic  
- `apps/stocks.py` — stocks dashboard visualization  
- `test/test_rps.py` — automated test cases  
- `requirements.txt` — project dependencies  
- `.env` — API key configuration for stocks data  
- `.github/workflows/python-app.yml` — CI workflow for automated testing

---

## Setup Instructions
    Create a Virtual Environment
    ```sh
    conda create -n quality-control python=3.11
    ```

    Activate Virtual Environment
    ```sh
    conda activate quality-control
    ```

    Install dependencies: pandas, python-dotenv, plotly, pytest
    ```sh
    pip install -r requirements.txt
    ```

    
## Run the Rock-Paper-Scissors Game
    ```sh
    python -m apps.rps
    ``` 

## Run the Stocks Dashboard
    ```sh
    python -m apps.stocks    
    ``` 

## Secret Credentials
    this is the ".env" file
    replace "______________" with your premium key
    ```sh
    ALPHAVANTAGE_API_KEY="______________"
    ```

## Run Test
    ```sh
    pytest
    ```
