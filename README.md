
# Empirical Performance Analysis of BFS and DFS

## 1. Introduction

This project focuses on the implementation and performance analysis of two uninformed search algorithms: Breadth-First Search (BFS) and Depth-First Search (DFS).

BFS explores nodes level by level using a queue, whereas DFS explores a path as deeply as possible using a stack. The project compares these algorithms on a graph and observes their execution performance.

## 2. Aim

To implement Breadth-First Search (BFS) and Depth-First Search (DFS) algorithms and analyze their performance using execution time, node exploration, and profiling techniques.

## 3. Objectives

- To understand the working of BFS and DFS algorithms.
- To implement both algorithms in Python.
- To represent a graph using nodes and edges.
- To compare the execution time of BFS and DFS.
- To count the nodes explored by each algorithm.
- To use `timeit` for execution-time measurement.
- To use `py-spy` for performance profiling.
- To document the system architecture using C4 diagrams.

## 4. Technologies Used

- **Programming Language:** Python
- **Algorithms:** Breadth-First Search (BFS) and Depth-First Search (DFS)
- **Time Measurement:** `timeit`
- **Profiling Tool:** `py-spy`
- **Architecture Documentation:** C4 Model
- **Version Control:** Git and GitHub

## 5. Algorithms Used

### 5.1 Breadth-First Search (BFS)

Breadth-First Search explores a graph level by level. It visits the starting node first and then explores its neighbouring nodes.

BFS uses a **queue** data structure, which follows the FIFO (First In, First Out) principle.

**Advantages:**
- Finds the shortest path in an unweighted graph when a path exists.
- Explores nodes systematically, level by level.

**Limitation:**
- May require more memory to store nodes waiting in the queue.

### 5.2 Depth-First Search (DFS)

Depth-First Search explores one path as deeply as possible before backtracking to explore other paths.

DFS can be implemented using a **stack** data structure, which follows the LIFO (Last In, First Out) principle.

**Advantages:**
- Can use less memory than BFS in some graph structures.
- May reach a particular goal quickly depending on the graph structure and traversal order.

**Limitation:**
- Does not guarantee the shortest path in an unweighted graph.
- Its performance depends on the graph structure and the order in which nodes are explored.

## 6. System Overview

The system accepts a graph, a starting node, and a goal node. It executes BFS and DFS to search for the goal and records the search results and performance measurements.

The system includes the following main components:

1. **Graph Data:** Stores the nodes and connections.
2. **BFS Component:** Searches the graph using a queue.
3. **DFS Component:** Searches the graph using a stack.
4. **Performance Measurement:** Measures execution time and supports profiling.

## 7. C4 Architecture Diagrams

### Level 1: System Context Diagram

This diagram shows the interaction between the user and the graph search system. The user provides the search requirements, and the system returns the search result and performance information.

![C4 Level 1 - System Context Diagram](./d1.drawio.png)

### Level 2: Container Diagram

This diagram shows the main containers of the system: the Python Search Application, Graph Data, and Performance Measurement using `timeit` and `py-spy`.

![C4 Level 2 - Container Diagram](./d2.drawio.png)

### Level 3: Component Diagram

This diagram describes the internal components of the application. The BFS component uses a queue, the DFS component uses a stack, and the performance measurement component records execution information.

![C4 Level 3 - Component Diagram](./d3.png.png)

### Level 4: Code Diagram

The code-level design represents the internal implementation of the system, including graph creation, BFS and DFS functions, node exploration, and performance measurement.

The implementation is available in [`main.py`](./main.py).

## 8. Performance Measurement

Performance measurement helps compare the behaviour of BFS and DFS under the selected graph and goal conditions.

### 8.1 Execution Time Using `timeit`

The Python `timeit` module is used to measure the execution time of the algorithms. Multiple runs can help reduce the effect of small variations in execution time.

### 8.2 Profiling Using `py-spy`

`py-spy` is a Python profiling tool that helps observe where a Python program spends its execution time. It can support the analysis of performance bottlenecks.

### 8.3 Node Exploration

The number of explored nodes is recorded to understand how much of the graph each algorithm visits before finding the goal or completing the search.

**Note:** Actual performance results depend on the graph structure, starting node, goal node, traversal order, and system environment.

## 9. BFS and DFS Comparison

| Feature | BFS | DFS |
|---|---|---|
| Search strategy | Level by level | Deep path first |
| Data structure | Queue | Stack |
| Shortest path | Guaranteed in an unweighted graph | Not guaranteed |
| Memory usage | Can be higher | Can be lower in some cases |
| Performance | Depends on graph and goal | Depends on graph and traversal order |

Neither algorithm is always faster. The better choice depends on the graph and the requirements of the search.

## 10. How to Run the Project

### Prerequisites

- Python 3 installed
- Git installed (if cloning the repository)

### Steps

1. Clone or download this repository.
2. Open the project folder in a terminal or code editor.
3. Run the Python program:

```bash
python main.py
```

If your system uses the `python3` command, run:

```bash
python3 main.py
```

Follow the program's prompts, if any, and observe the search output.

## 11. Repository Structure

```text
SLE3/
├── README.md
├── CONTRIBUTIONLOG.md
├── main.py
├── SLE3_25UAM049_GouriKudalkar.pdf
├── d1.drawio.png
├── d2.drawio.png
└── d3.png.png
```

## 12. Applications

- Pathfinding in graphs
- Network traversal
- State-space search in Artificial Intelligence
- Exploring connected nodes
- Understanding uninformed search strategies

## 13. Conclusion

This project demonstrates the implementation and comparison of BFS and DFS for graph searching. BFS uses a queue and explores nodes level by level, while DFS uses a stack and explores paths deeply before backtracking.

Execution-time measurement, node counting, and profiling provide useful information for evaluating algorithm behaviour. The project also documents the system design using the C4 architecture model.

The results should be interpreted according to the graph structure and experimental conditions rather than assuming that one algorithm is always better than the other.

## 14. References

- Python Documentation: https://docs.python.org/3/
- Python `timeit` Documentation: https://docs.python.org/3/library/timeit.html
- py-spy Documentation: https://github.com/benfred/py-spy
- GitHub Repository: https://github.com/kudalkargouri-crypto/SLE3
