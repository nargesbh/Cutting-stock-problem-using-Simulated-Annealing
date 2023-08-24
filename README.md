# README for Jupyter Notebook Code

This repository contains Jupyter Notebook code for solving the Stock Cutting Optimization problem using Simulated Annealing. The problem involves finding the optimal way to cut a list of items with varying lengths from stock of a fixed length, with the goal of minimizing the number of stock pieces used.

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Test Cases](#test-cases)
- [Parameter Tuning](#parameter-tuning)
- [Conclusion](#conclusion)

## Introduction
Stock Cutting Optimization is a combinatorial optimization problem where the objective is to determine the optimal way to cut a set of items from a fixed-length stock to minimize waste. This repository provides a Jupyter Notebook implementation of the Simulated Annealing algorithm to solve this problem.

## Prerequisites
Before using this code, ensure you have the following libraries installed:
- `random`
- `math`
- `numpy`
- `pandas`
- `matplotlib`

You can install these libraries using pip:
```
pip install numpy pandas matplotlib
```

## Usage
1. Clone this repository to your local machine:
```
git clone https://github.com/your-username/stock-cutting-optimization.git
```

2. Navigate to the project directory:
```
cd dir_path
```

3. Open the Jupyter Notebook file using Jupyter Notebook or Jupyter Lab.

4. Run the code cells in the notebook with your desired input file and parameters. For example, edit and run the following cell:
```
Ts, all_costs, best_ans, iteration_num = main('input1.stock', 0.88, 30)
```
#### Input Parameters
- `input1.stock`: The input file containing problem data.
- `0.88`: The alpha parameter for controlling the cooling schedule.
- `30`: The initial temperature parameter (T) for simulated annealing.

#### Execution
The code will:
- Execute and provide the best solution found.
- Display the corresponding cost.
- Show the number of iterations.
- Generate a plot illustrating how the cost changes with temperature.

#### Code Structure
- **`HW4.ipynb`**: The Jupyter Notebook containing the code for solving the Stock Cutting Optimization problem using Simulated Annealing.
- **`input_maker(path)`**: Reads the input file and extracts the required data.
- **`cost(a)`**: Calculates the cost (number of stock pieces) for a given order.
- **`neighborhood_func(a)`**: Generates a neighboring solution by swapping two random indices in the order.
- **`neighborhood_func2(a)`**: Generates a neighboring solution by swapping the values of three random indices in the order.
- **`move_check(dc)`**: Determines whether to accept a neighbor solution based on the change in cost and current temperature.
- **`main(path, alpha, t)`**: The main algorithm that performs simulated annealing and returns the results.
- **`main2(path, alpha, t)`**: An alternative version of the main algorithm with a different approach to temperature updating.
- **Plotting functions**: Code for plotting the cost vs. temperature graph.

#### Test Cases
This code includes several test cases (`input1.stock`, `input2.stock`, `input3.stock`, `input4.stock`) to demonstrate its functionality. Each test case represents a different instance of the Stock Cutting Optimization problem. (Test cases can be found in HW.pdf)

#### Parameter Tuning
You can experiment with different values for the `alpha` (cooling rate) and `t` (initial temperature) parameters to observe their effects on the solution quality and convergence speed. The provided test cases have shown that appropriate parameter values can significantly impact the algorithm's performance.

#### Conclusion
Simulated Annealing is a powerful optimization technique for solving combinatorial optimization problems like Stock Cutting. With proper parameter tuning, it can efficiently find near-optimal solutions. This repository provides a flexible implementation for solving such problems.

