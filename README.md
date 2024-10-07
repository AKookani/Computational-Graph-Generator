# Computational Graph Generator

This project provides a Python-based tool to automatically generate computational graphs from mathematical expressions. A **computational graph** is a representation of mathematical expressions in graph form, where each node represents an operation or a variable, and the edges represent dependencies between operations.

## Features
- **Expression Parsing**: Convert a given mathematical expression into its symbolic form using **SymPy**.
- **Graph Construction**: Automatically build a computational graph using **NetworkX**, where each operation is represented as a node and operands as edges.
- **Graph Visualization**: Visualize the computational graph with **Matplotlib**, making it easy to understand the structure of the computation.

## How It Works
1. **Input**: You provide a mathematical expression as a string, for example: `"x * y + z**2"`.
2. **Processing**: The expression is parsed by SymPy, which breaks it down into components (e.g., variables, operators). A directed graph is created where each operation (e.g., addition, multiplication, exponentiation) is represented as a node.
3. **Output**: The generated computational graph is displayed using Matplotlib, showing the flow of computations.

### Example
For the expression `"x * y + z**2"`, the computational graph will show:
- A node for the multiplication operation (`x * y`)
- A node for the exponentiation operation (`z**2`)
- A node for the addition that combines these results

### Technologies Used
- **SymPy**: For parsing mathematical expressions.
- **NetworkX**: For constructing the directed graph of the expression.
- **Matplotlib**: For visualizing the computational graph.

## Usage

1. Install the required libraries:
   ```bash
   pip install sympy networkx matplotlib
   ```

2. Use the code to generate computational graphs from mathematical expressions. Example:
   ```python
   expression = "x * y + z**2"
   G = build_computational_graph(expression)
   visualize_graph(G)
   ```
