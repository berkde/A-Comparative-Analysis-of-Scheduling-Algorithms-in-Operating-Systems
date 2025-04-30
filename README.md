# A Comparative Analysis of Scheduling Algorithms in Operating Systems

This project simulates and compares three fundamental CPU scheduling algorithms: **First-Come-First-Served (FCFS)**, **Shortest Job Next (SJN)**, and **Round Robin (RR)**. It generates random processes with different arrival and burst times and evaluates each scheduling method based on key performance metrics.

---

## Project Overview

The script performs the following:

### 1. Imports Required Libraries
- Loads `random`, `pandas`, and `matplotlib` to handle data generation, analysis, and visualization.

### 2. Defines a Process Generator
- `generate_processes(num_processes)` creates a list of synthetic processes with random `arrival_time` and `burst_time`, then sorts them by arrival time.

### 3. Implements Scheduling Algorithms
- **FCFS**: Executes processes in the order of arrival; computes waiting and turnaround times.
- **SJN**: Picks the process with the shortest burst time among the arrived ones; also computes waiting and turnaround times.
- **Round Robin (RR)**: Processes are given equal time slices (quantum); supports preemption and computes both metrics.

### 4. Runs the Simulation
- `run_simulation()`:
  - Generates 1000 random processes.
  - Applies each of the three scheduling algorithms.

### 5. Creates Visual Comparisons
- Plots a bar chart comparing average waiting and turnaround times across algorithms.
- Plots another bar chart comparing throughput.

---

## Entry Point for Script Execution

If the file is run directly (`__main__`), it triggers the simulation and visualization pipeline.

---

## Features

- Generate synthetic process data.
- Implement core scheduling algorithms:
  - FCFS (First-Come-First-Served)
  - SJN (Shortest Job Next / Non-preemptive SJF)
  - Round Robin (with configurable quantum)
- Compute and visualize:
  - Average waiting time
  - Average turnaround time
  - System throughput
- Plot comparative bar charts for each algorithm.

---

## Algorithms Implemented

### First-Come-First-Served (FCFS)
- Non-preemptive.
- Processes are executed in the order they arrive.

### Shortest Job Next (SJN)
- Non-preemptive.
- Selects the process with the smallest burst time among those that have arrived.

### Round Robin (RR)
- Preemptive.
- Processes are assigned a time quantum and cycled through in a queue.

---

## Metrics Evaluated

- **Average Waiting Time**: Mean of time each process waits before getting CPU.
- **Average Turnaround Time**: Time from arrival to completion per process.
- **Throughput**: Number of processes completed per unit time.

---

## Visualizations

The notebook plots two bar charts:

1. **Average Waiting Time & Turnaround Time** per Algorithm  
2. **Throughput** per Algorithm

These provide an intuitive visual comparison of each algorithm’s performance.

---

## How to Run

### Prerequisites

- Python 3.7+
- Jupyter Notebook

Install required libraries:
```bash
pip install numpy pandas matplotlib notebook jupyterlab mistune
pip install --upgrade nbconvert
```

### Steps

1. Clone the repository or download the `.ipynb` file.
2. Open `ProcessSchedulingSimulation.ipynb` in Jupyter.
3. Run all cells to simulate the scheduling algorithms and view results.

### CLI (Optional)

You can also execute the notebook as a standalone script:
```bash
jupyter nbconvert --execute ProcessSchedulingSimulation.ipynb --to notebook
```

---

Would you like me to also generate a sample bar chart or add a `graph` folder reference in the README?