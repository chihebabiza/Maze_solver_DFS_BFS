# Maze Solver (Search Algorithms)

An AI-based maze solver that uses search algorithms to find the shortest path between two points. This project demonstrates the difference between **Depth-First Search (DFS)** and **Breadth-First Search (BFS)** by visualizing the path found and the states explored.

## 🚀 Features

* **Breadth-First Search (BFS):** Guarantees the shortest path by using a queue-based frontier.
* **Depth-First Search (DFS):** Explores as deep as possible first using a stack-based frontier.
* **Visual Output:** Generates a PNG image of the solved maze, highlighting the path and the cells explored by the AI.
* **Custom Maze Support:** Easily create and solve your own mazes using simple text files.

## 🛠 How It Works

The program treats the maze as a graph where each empty cell is a node.

1. It starts at point **A**.
2. It adds neighboring cells to a "frontier."
3. It removes a node from the frontier, marks it as "explored," and adds its neighbors to the frontier.
4. This repeats until point **B** is reached or no solution is found.

## 📋 Requirements

* **Python 3.x**
* **Pillow (PIL):** Used for generating the visual representation of the maze.
```bash
pip install Pillow

```



## 💻 Usage

1. **Prepare your maze:** Create a `.txt` file (e.g., `maze.txt`). Use `A` for the start, `B` for the goal, `#` for walls, and spaces for paths.
```text
###A#
#   #
# # #
# # B
#####

```


2. **Run the solver:**
```bash
python maze.py maze.txt

```


3. **Toggle Algorithms:**
* To use **DFS**: Ensure `frontier = StackFrontier()` is used in `maze.py`.
* To use **BFS**: Change the frontier to `frontier = QueueFrontier()` in `maze.py`.



## 📊 Comparison

| Algorithm | Data Structure | Shortest Path? | Performance |
| --- | --- | --- | --- |
| **DFS** | Stack (LIFO) | No | Fast, but can take a "long" way. |
| **BFS** | Queue (FIFO) | Yes | Explores more states, but finds the optimal path. |

## 🖼 Output Example

After running the script, the terminal will display the number of states explored and a text-based version of the maze. Additionally, a `maze.png` file will be generated:

* **Red:** Start Point (A)
* **Green:** Goal Point (B)
* **Yellow:** Final Path
* **Dark Red/Orange:** Explored Cells (if enabled)
