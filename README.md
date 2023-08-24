# Cutting Stock Problem Solver using Simulated Annealing

This repository contains a Python implementation for solving the Cutting Stock Problem using the Simulated Annealing algorithm. The Cutting Stock Problem is a combinatorial optimization problem often encountered in manufacturing and logistics, where you need to determine the most efficient way to cut large rolls of material (e.g., paper, steel) into smaller pieces to satisfy customer orders while minimizing waste.

## Problem Description

The Cutting Stock Problem involves:

1. A set of **orders**, each specifying the length and quantity of pieces required.
2. A set of **raw rolls** of a fixed length, from which the required pieces must be cut.
3. The goal is to find the **cutting patterns** that minimize waste while meeting all order requirements.

## Algorithm Used

The Cutting Stock Problem is solved using the Simulated Annealing algorithm:

1. **Initial Solution**: The algorithm starts with an initial solution, which is a set of cutting patterns. Initially, it may not be optimal.

2. **Cost Function**: A cost function is defined to measure the efficiency of a solution. In this case, it quantifies the amount of waste generated.

3. **Simulated Annealing**: The algorithm uses Simulated Annealing, a probabilistic optimization technique, to explore and exploit the solution space. It iteratively makes small changes to the cutting patterns and accepts these changes based on the change in the cost function and a temperature schedule.

4. **Temperature Schedule**: The temperature schedule controls the probability of accepting worse solutions initially and gradually reduces the probability as the algorithm progresses. This allows the algorithm to escape local optima.

5. **Termination**: The algorithm terminates when a stopping criterion is met, such as reaching a maximum number of iterations or a sufficiently low temperature.

## Parameters

- `initial_solution`: The initial set of cutting patterns.
- `temperature_schedule`: The schedule for reducing the temperature in the Simulated Annealing process.
- Other parameters and constraints specific to your implementation.

## Usage

To use this algorithm, follow these steps:

1. Clone this repository to your local machine.

2. Install the required Python libraries, if any, as mentioned in the repository.

3. Prepare your problem instance, specifying the orders and raw rolls.

4. Modify the parameters and constraints in the code to match your specific problem.

5. Run the code by executing the Python script.

6. The algorithm will apply Simulated Annealing to find the optimal cutting patterns that minimize waste while meeting all order requirements.

