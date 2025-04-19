# Experiment 11(a): Representation of Graph

## Aim
To write a Python program to generate a graph for a given fixed degree sequence.

---

## Algorithm

1. **Start the program**:
   - Read the degree sequence from the user input.
   - The degree sequence represents the number of edges connected to each vertex in the graph.
   
2. **Define the graph representation**:
   - Create an adjacency matrix to represent the graph. The matrix will be a square matrix where each element `mat[i][j]` is `1` if there's an edge between vertex `i` and vertex `j`, and `0` otherwise.

3. **Construct the graph**:
   - Loop through all pairs of vertices (`i`, `j`).
   - If both vertices `i` and `j` have remaining degrees greater than `0`, decrement their degree and add an edge between them in the matrix.

4. **Display the adjacency matrix**:
   - Print the adjacency matrix in a human-readable format.
   
5. **End the program**:
   - The graph is now represented by the adjacency matrix, and the program prints the matrix.

---

## Program

```

```

## OUTPUT

## RESULT
