# Experiment 11(e): Adjacency List Representation of a Graph

## Aim
To write a Python program to demonstrate the adjacency list representation of a given graph.

---

## Algorithm

1. **Create a Node Class**:
   - Define a class `AdjNode` to represent each node in the adjacency list:
     - Store the vertex number.
     - Store a reference to the next adjacent node.

2. **Graph Class**:
   - Define a class `Graph` to represent the graph using an adjacency list:
     - Initialize the number of vertices and create an array to store the adjacency lists.
   
3. **Add an Edge**:
   - Define a method `add_edge(src, dest)` to add an edge between two vertices:
     - Add `dest` to the adjacency list of `src`.
     - Add `src` to the adjacency list of `dest` (for undirected graphs).
   
4. **Print the Graph**:
   - Define a method `print_graph()` to print the graph:
     - Traverse each vertex’s adjacency list and print the vertex along with its adjacent nodes.

5. **Main Program**:
   - Create a graph object with `V` vertices.
   - Add edges using the `add_edge()` method.
   - Print the adjacency list representation using `print_graph()`.

---

## Program

```
class AdjNode:
	def __init__(self, data):
		self.vertex = data
		self.next = None


# A class to represent a graph. A graph
# is the list of the adjacency lists.
# Size of the array will be the no. of the
# vertices "V"
class Graph:
	def __init__(self, vertices):
		self.V = vertices
		self.graph = [None] * self.V

	# Function to add an edge in an undirected graph
	def add_edge(self, src, dest):
		# Adding the node to the source node
		node = AdjNode(dest)
		node.next = self.graph[src]
		self.graph[src] = node

		# Adding the source node to the destination as
		# it is the undirected graph
		node = AdjNode(src)
		node.next = self.graph[dest]
		self.graph[dest] = node

	
	def print_graph(self):
	    for i in range(V):
	        print(f"Adjacency list of vertex {i}\n head",end=" ")
	        temp=self.graph[i]
	        while temp:
	            print(f"-> {temp.vertex}",end=" ")
	            temp=temp.next
	        print("\n")
	            
		
		
		#Write Code here





# Driver program to the above graph class
if __name__ == "__main__":
	V = 5
	graph = Graph(V)
	graph.add_edge(0, 1)
	graph.add_edge(0, 4)
	graph.add_edge(1, 2)
	graph.add_edge(1, 3)
	graph.add_edge(1, 4)
	graph.add_edge(2, 3)
	graph.add_edge(3, 4)

	graph.print_graph()


```

## OUTPUT
![Screenshot (277)](https://github.com/user-attachments/assets/139b603f-43b9-406a-a31e-ac142ec4258f)

## RESULT
Thus the python program was initialised and executed successfully.
