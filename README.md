# N-Queens Search Optimization Engine

A Python project that solves the N-Queens problem using classical AI local-search methods, including hill climbing, hill climbing with sideways moves, and random-restart search.

## Overview

This project explores how different heuristic search strategies perform on the N-Queens problem. The solver represents each board as a one-dimensional list where the index is the row and the value is the queen's column in that row.

The heuristic function is:

**h(state) = number of attacking pairs of queens**

The goal is to reach a board with **h(state) = 0**, meaning no queens attack each other.

## Features

- Configurable board size `n`
- Basic hill-climbing search
- Hill climbing with sideways moves
- Random-restart hill climbing
- Random-restart hill climbing with sideways moves
- Step-by-step search history logging
- Experimental benchmarking across multiple trial counts
- Exportable text results for analysis

## Algorithms Implemented

### 1. Basic Hill Climbing
Moves to a randomly chosen best neighbor only if it strictly improves the heuristic.

### 2. Hill Climbing with Sideways Moves
Allows movement to equal-valued neighbors, with a cap on consecutive sideways steps to help escape plateaus.

### 3. Random-Restart Hill Climbing
Restarts the search from a new random board until a solution is found.

### 4. Random-Restart Hill Climbing with Sideways Moves
Combines restart strategy with sideways exploration for higher reliability.

## Key Results (8-Queens)

Across repeated experiments:

- Basic hill climbing solved the problem at roughly **13–15%**
- Hill climbing with sideways moves solved it at roughly **94–96%**
- Average restart counts dropped from about **5.6** to nearly **0**
- Trials were benchmarked across **50, 100, 200, 500, 1000, and 1500** runs

These results show that sideways exploration dramatically improves reliability by helping the search escape plateaus and shallow local minima.

## Tech Stack

- **Language:** Python
- **Concepts:** Classical AI, heuristic search, local search, stochastic optimization
