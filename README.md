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

## Setup

Create and activate a virtual environment:

```sh
#Use this line to create an environment

conda create -n my-first-env-2025 python=3.11

#Use this line to activate the environment

conda activate my-first-env-2025
```


Install packages:

```sh
# pip install requirements

pip install -r requirements.txt
``` 
 
   

    
## Run the Rock-Paper-Scissors Game
 ```sh
 # run this to play a game of rock paper scissors

python -m app.rps
```

## Run the Stocks Dashboard
```sh
#run this to access a stock's information and generate dashboard

python -m apps.stocks    
``` 

## Secret Credentials
```sh
 # This is in the ".env" file. Replace "______________" with your premium key

ALPHAVANTAGE_API_KEY="______________"
```

## Run Test
```sh
# Test rock paper scissors game with this line

pytest test/test_rps.py

# Test stock dashboard with this line(issue with plotly module, currently working with prof on it)

pytest test/test_stocks.py

```
