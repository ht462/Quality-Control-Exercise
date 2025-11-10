

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
```bash
conda create -n my-first-env-fall-2025 python=3.11
### 2. activeate a virtual environment
conda activate my-first-env-fall-2025

### 3. instal dependencies
pip install -r requirements.txt

including: 
pandas
python-dotenv
plotly
pytest

### 4. Game Logic
def determine_winner(u, c):
    if u == c:
        return "TIE GAME"
    elif (u == "rock" and c == "scissors") or \
         (u == "paper" and c == "rock") or \
         (u == "scissors" and c == "paper"):
        return "USER WINS"
    else:
        return "COMPUTER WINS"

### 5. Run Game
python -m apps.rps

### 6. Testing

from apps.rps import determine_winner

def test_winners():
    assert determine_winner("rock", "rock") == "TIE GAME"
    assert determine_winner("rock", "paper") == "COMPUTER WINS"
    assert determine_winner("rock", "scissors") == "USER WINS"
    assert determine_winner("paper", "rock") == "USER WINS"
    assert determine_winner("scissors", "rock") == "COMPUTER WINS"
### 7. Run test

pytest -v




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
```bash
conda create -n my-first-env-fall-2025 python=3.11
### 2. activeate a virtual environment
conda activate my-first-env-fall-2025

### 3. instal dependencies
pip install -r requirements.txt

including: 
pandas
python-dotenv
plotly
pytest

### 4. Game Logic
def determine_winner(u, c):
    if u == c:
        return "TIE GAME"
    elif (u == "rock" and c == "scissors") or \
         (u == "paper" and c == "rock") or \
         (u == "scissors" and c == "paper"):
        return "USER WINS"
    else:
        return "COMPUTER WINS"

### 5. Run Game
python -m apps.rps

### 6. Testing

from apps.rps import determine_winner

def test_winners():
    assert determine_winner("rock", "rock") == "TIE GAME"
    assert determine_winner("rock", "paper") == "COMPUTER WINS"
    assert determine_winner("rock", "scissors") == "USER WINS"
    assert determine_winner("paper", "rock") == "USER WINS"
    assert determine_winner("scissors", "rock") == "COMPUTER WINS"
### 7. Run test

pytest -v



