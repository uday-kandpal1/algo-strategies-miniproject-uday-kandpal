Algorithmic Strategies Mini-Project: Performance & Optimization
1. Problem Context
In software engineering, an "algorithm" is more than just a set of instructions; it is a strategy for resource management. As datasets grow, the difference between an O(n 
2
 ) and an O(nlogn) algorithm can mean the difference between a functional application and a system crash. This project explores five fundamental problems across four major algorithmic paradigms: Divide and Conquer, Greedy, Dynamic Programming, and Brute Force.

2. Implemented Strategies & Problems
I. Divide and Conquer: Merge Sort
Strategy: Recursively breaking a problem into two or more sub-problems of the same or related type, until these become simple enough to be solved directly.

Implementation: Used to sort large datasets by splitting arrays into halves and merging them back in order.

Complexity: O(nlogn).

II. Greedy Strategy: Fractional Knapsack
Strategy: Making the locally optimal choice at each stage with the hope of finding a global optimum.

Implementation: Selecting items based on the highest value-to-weight ratio. Unlike 0/1 Knapsack, items can be broken into smaller units.

Complexity: O(nlogn) (due to initial sorting).

III. Dynamic Programming: 0/1 Knapsack
Strategy: Solving complex problems by breaking them down into simpler sub-problems and storing the results (Tabulation) to avoid redundant calculations.

Implementation: Determining the maximum value of items that can fit in a knapsack where items cannot be split.

Complexity: O(n⋅W) where W is capacity.

IV. Dynamic Programming: Fibonacci Sequence
Strategy: Utilizing Memoization or Tabulation to transform a highly redundant recursive process into a linear one.

Implementation: Calculating the n 
th
  Fibonacci number by storing previous results in an array.

Complexity: O(n) time and O(n) space.

V. Brute Force: Travelling Salesman Problem (TSP)
Strategy: A straightforward approach that relies on sheer computing power to try every possible combination.

Implementation: Generating every possible permutation of city routes to find the absolute shortest path.

Complexity: O(n!) — The most extreme form of complexity.

3. Performance Observations
The "Exponential Wall"
In our testing, we observed that while Merge Sort and Fibonacci (DP) handle thousands of inputs with ease, the TSP Brute Force approach becomes unusable after just 12–15 cities. This is known as the "combinatorial explosion," where the number of operations (n!) grows faster than any modern processor can keep up with.

Space-Time Trade-off
The 0/1 Knapsack and Fibonacci DP implementations demonstrate the Space-Time Trade-off. By using a small amount of extra memory (a 2D table or 1D array), we reduced execution times from several minutes (in the case of naive recursion) to mere milliseconds.

4. Setup & Usage Instructions
Prerequisites
Python: 3.10+

Libraries: matplotlib, numpy, memory_profiler

Installation
Clone the Repo:

Bash
git clone https://github.com/yourusername/algo-strategies-mini-project.git
cd algo-strategies-mini-project
Initialize Environment:

Bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
pip install matplotlib numpy memory_profiler jupyterlab
Usage
To view performance graphs: Launch the Jupyter Notebook in the notebooks/ folder.

Bash
jupyter lab notebooks/algo_strategies_notebook.ipynb
To run the CLI tool: Execute the main Python script.

Bash
python src/main.py
5. Conclusion
This project confirms that Divide and Conquer and Dynamic Programming are essential for scalable software. While Greedy algorithms are efficient, they are only applicable to specific problems. Finally, Brute Force serves as a vital benchmark but highlights the necessity of heuristics in solving NP-hard problems like the Travelling Salesman.
