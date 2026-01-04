# OpenGL Conway's Game of Life

A real-time simulation of Conway's Game of Life built using **C++** and **OpenGL**. The simulation features a 32x32 grid with toroidal (wrapping) topology and hardware-accelerated rendering.



## 🚀 Features

* **Real-time Visualization:** Uses GLFW and GLEW for high-performance rendering.
* **Toroidal Grid:** The simulation space wraps around the edges, meaning cells on the far left interact with cells on the far right.
* **Fixed Time-Step:** The simulation logic is decoupled from the frame rate, updating every 50ms for consistent behavior.
* **Random Initialization:** Each new run starts with a randomized "seed" population.

## 🧠 Simulation Logic

The project implements the standard rules of cellular automata:

1.  **Underpopulation:** Any live cell with fewer than 2 live neighbors dies.
2.  **Survival:** Any live cell with 2 or 3 live neighbors lives on.
3.  **Overpopulation:** Any live cell with more than 3 live neighbors dies.
4.  **Reproduction:** Any dead cell with exactly 3 live neighbors becomes a live cell.



## 🛠️ Prerequisites

To build and run this project, you need the following libraries installed:

* **GLEW**: The OpenGL Extension Wrangler Library.
* **GLFW**: A multi-platform library for OpenGL development.
* **OpenGL**: Core graphics API.

## 📂 File Structure

* `main.cpp`: Contains the core logic, including the grid initialization, neighborhood checking, and the OpenGL render loop.

## ⚙️ How It Works

The simulation uses a **double-buffering** approach for the grid logic:
1.  The current state is stored in `players_arr`.
2.  The `check_surroundings` function calculates the next state based on the neighbors.
3.  The results are stored in `next_players_arr`.
4.  After all cells are calculated, `players_arr` is updated to the new state.

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
