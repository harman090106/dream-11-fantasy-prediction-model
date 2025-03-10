# Fantasy Cricket Prediction Model

## Overview
This repository contains the code for a **fantasy cricket prediction model**, designed to select the best 11 players for a given ODI match. The model uses **historical player statistics, recent form, and optimization techniques** to generate an optimal Dream11 team.

## Features
- **Automated Team Selection**: Predicts the best 11 players based on player stats and match conditions.
- **Player Performance Prediction**: Uses **Random Forest** to predict fantasy points.
- **Role-Based Optimization**: Ensures a balanced team composition using **Linear Programming (LP)**.
- **Integration with Real Match Data**: Processes **match-by-match stats** for accurate predictions.
- **Dockerized Model**: Enables easy deployment and validation for the Dream11 Gameathon.

## Data Used
The model relies on:
1. **Match Highlights Data**: Contains match results, team info, and pitch details.
2. **Overall Player Stats**: Aggregated player statistics over their careers.
3. **Ball-by-Ball Data**: Helps compute detailed player performance metrics.
4. **Fantasy Points Data**: Captures real-world fantasy scoring patterns.
5. **ICC Team Rankings**: Adds context to player performances.
6. **Recent Form Metrics**: Incorporates performance trends over the last two months.

## How It Works
### 1. **Data Processing**
- Extracts match-by-match player stats.
- Computes fantasy points for each player.
- Aggregates stats based on career, recent form, and pitch conditions.

### 2. **Player Score Prediction**
- Trains a **Random Forest** model on historical data.
- Predicts fantasy scores for the 30-player squad.

### 3. **Optimized Team Selection**
- Uses **Linear Programming** to pick the best 11 players.
- Ensures role distribution (Batsmen, Bowlers, All-Rounders, Wicket-Keepers).

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/fantasy-cricket-prediction.git
   cd fantasy-cricket-prediction
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the prediction model:
   ```sh
   python predict_team.py --team1 IND --team2 ENG --match_no 5
   ```

## Docker Deployment
1. Build the Docker image:
   ```sh
   docker build -t fantasy-cricket .
   ```
2. Run the container:
   ```sh
   docker run -p 5000:5000 fantasy-cricket
   ```

## File Structure
```
|-- data/              # Match data and player stats
|-- models/            # Trained models
|-- notebooks/         # Jupyter notebooks for analysis
|-- src/
    |-- data_loader.py # Loads and processes data
    |-- model.py       # Training and prediction
    |-- optimizer.py   # Team selection algorithm
    |-- predict_team.py# Main script for team prediction
|-- Dockerfile         # Docker setup
|-- requirements.txt   # Dependencies
|-- README.md          # Documentation
```

## Future Improvements
- Fine-tune **prediction model hyperparameters**.
- Integrate more **advanced ensemble models**.
- Improve the handling of **match-day uncertainties**.

## Contributions
Feel free to raise issues and contribute via pull requests!

## License
This project is licensed under the MIT License.

---
Developed by **Harman** for the **Dream11 Gameathon** 🚀

