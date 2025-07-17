# Graph Core Number Calculator
#Au-Yeung Fung Yin
#57269800

## Description

This Python script calculates the core number for each node in a graph. The core number is a concept in graph theory that represents the largest value `k` of a `k-core` that contains the node. A `k-core` of a graph is a maximal subgraph in which each vertex has at least degree `k`.

The script reads edge data from a file, constructs the graph, and computes the core number for each node. It then writes the results to a `result.txt` file.

## Getting Started

### Dependencies

Make sure you have Python installed on your system. This script was tested with Python 3.x.

### Installing

No installation is necessary. Just download the script, and you're ready to go.

### Executing program

1. Prepare your input file (e.g., `DBLP.txt`) in the format where the first line is skipped (assumed to be a header), and each subsequent line contains two integers representing an edge between two nodes in the graph.

2. Run the script with Python:

3. Check the output in result.txt, where each line contains a node and its corresponding core number, separated by a colon.