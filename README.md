# CVRP approach using quantum computing

Few quantum approaches for CVRPTW problems. It isn't fully ended version and it's not well described. If you want to use it, I recommend you to change only file paths in main. 

## API Usage

* Prepare test scenario according to Input specification.
* Read the test by function read_full_test or read_test.

## Input specification

You need to prepare 2 files :

* Graph file in simple csv format, named vertex_weights.csv, containing 3 columns as edges: id of first vertes, id of second vertex and weight of edge. Graph is directed.
* Scenario text file. Format is described in 'example_scenario'.

## Running

* Choose a solver.
* Read test by read_test function or read_full_test from input.py
* Run solve function from solver in same way as in main.


## Available solvers :

* FullQuboSolver - solving VRP problem only by quantum annealing, working for small cases
* AveragePartitionSolver - improved version of previous one, but using only qunatum annealing, working for small cases and only for VRP
* DBScanSolver - hybrid algorithm for VRP and CVRP with equal capacities, working for bigger cases, based on https://arxiv.org/abs/1812.02300
* SolutionPartitioningSolver - hybrid algorithm for CVRP, working for cases with 200 deliveries if used with DBScanSolver. (as parameter - example in main)
