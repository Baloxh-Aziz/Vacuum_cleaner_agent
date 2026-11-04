# 🤖 Vacuum Cleaner Agent Simulation

A simple reflex-agent simulation of a vacuum cleaner robot that cleans two rooms (Room A and Room B) based on their state (dirty/clean), while managing battery life.

## 📋 Overview

This project simulates a basic **simple reflex agent** (a classic AI concept) that:

1. Randomly generates the state (`dirty`/`clean`) of Room A and Room B each cycle
2. Checks each room and cleans it if dirty, consuming more battery
3. If a room is already clean, it skips cleaning and consumes less battery
4. Keeps a running score of total rooms cleaned
5. Repeats the cycle until battery level drops to the exit threshold (20), then returns to the charging station

## ⚙️ How It Works

| Action                  | Battery Cost |
| ----------------------- | ------------- |
| Cleaning a dirty room    | 5             |
| Checking an already-clean room | 2      |

- Starting battery: **100**
- Stop condition: battery ≤ **20**
- Score: incremented by 1 for every room actually cleaned

## 📈 Sample Output

- The agent prints the initial state of both rooms each cycle
- Logs whether each room was cleaned or skipped, along with the battery level after each action
- At the end, prints the final battery level and total score (rooms cleaned)

## 🛠️ Tech Stack

- **Python 3**
- `random` — to simulate random room states
- `time` — to simulate cleaning delay
