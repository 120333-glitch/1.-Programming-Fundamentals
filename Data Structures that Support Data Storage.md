# Implement Data Structures that Support Data Storage - Student Notes

Students implement data structures to **store, organise and access data efficiently** when developing software solutions. These structures support different ways of managing data depending on how it is used.

***

### Single‑Dimensional Arrays

A **single‑dimensional array** stores multiple values of the same data type in a linear sequence, accessed using an index. In Python, this is implemented using a list.  
**Example:** Storing student test scores.

```python
scores = [78, 85, 92]
```

***

### Multidimensional Arrays

A **multidimensional array** stores data in rows and columns and is implemented in Python as a list of lists. It is used to represent structured data such as grids.  
**Example:** A Sudoku board or game grid.

```python
grid = [
    [1, 2, 3],
    [4, 5, 6]
]
```

***

### Lists

A **list** is a dynamic data structure that can grow or shrink during program execution and can store multiple values in order.  
**Example:** A task list in a project management program.

```python
tasks = ["Design", "Code", "Test"]
```

***

### Trees

A **tree** is a hierarchical data structure made up of nodes with parent–child relationships. It is used to represent data with levels or branches.  
**Example:** A file system or decision tree.

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None
```

***

### Stacks

A **stack** is a data structure that follows the **Last In, First Out (LIFO)** principle, where the most recent item added is the first removed.  
**Example:** An undo feature in an application.

```python
stack = []
stack.append("Action")
stack.pop()
```

***

### Hash Tables

A **hash table** stores data as **key–value pairs**, allowing fast access to data using a unique key. In Python, this is implemented using a dictionary.  
**Example:** Storing student details using an ID as the key.

```python
student = {"id": 101, "name": "Alex"}
```

***

### One‑Sentence Syllabus Summary (Optional)

> Data structures such as arrays, lists, trees, stacks and hash tables are implemented to store and manage data efficiently within software solutions.

