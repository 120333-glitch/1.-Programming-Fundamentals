# Sequential Files (Python) – Student Handout

## Syllabus Link

**Programming Fundamentals**

> *Use data structures of arrays, records, trees and sequential files*

***

## What is a Sequential File?

A **sequential file** stores data in a **fixed order** and is accessed **from the beginning to the end**.  
Records are read **one at a time, in sequence**.

✅ A **text file (.txt)** is the most common example of a sequential file  
✅ Each **line** usually represents one **record**

***

## Key Characteristics

*   Data is stored **chronologically or logically**
*   Records must be read **in order**
*   You **cannot jump directly** to the middle of the file
*   Often processed using **loops**

***

## Real‑World Analogy

A **cassette tape** 🎵  
To hear a song near the end, you must fast‑forward through all earlier songs.  
Sequential files work the same way.

***

## Why Use Sequential Files?

Sequential files are useful when:

*   Data is **simple**
*   Most or all records are processed
*   Data does not change often

Common uses:

*   Student marks
*   Attendance lists
*   Log files
*   Sensor data

***

## Sequential Files in Python

Python uses **text files** and the built‑in `open()` function.

### Writing to a Sequential File

```python
file = open("students.txt", "w")

file.write("Alice\n")
file.write("Ben\n")
file.write("Charlie\n")

file.close()
```

*   Each line is written **in order**
*   `\n` moves to a new line (new record)

***

### Reading from a Sequential File

```python
file = open("students.txt", "r")

for line in file:
    print(line.strip())

file.close()
```

*   File is read **from top to bottom**
*   Loop processes **one record at a time**

***

### Processing Data from a Sequential File

```python
file = open("students.txt", "r")

count = 0
for line in file:
    count += 1

file.close()
print("Number of students:", count)
```

*   Shows how sequential files are commonly used with **iteration**

***

## Advantages and Limitations

### Advantages

✅ Easy to use  
✅ Good for large amounts of simple data  
✅ Efficient when reading all records

### Limitations

❌ Slow to search  
❌ Inefficient for frequent updates  
❌ Must read earlier records first

***

## Comparison with Other Data Structures

| Data Structure      | Access Method            |
| ------------------- | ------------------------ |
| Array / List        | By index                 |
| Record              | By field                 |
| Tree                | By relationships         |
| **Sequential File** | **One record at a time** |

***

## Key Exam Tip ✅

If a question mentions:

*   **Text files**
*   **Reading data line by line**
*   **Processing all records**

👉 The correct data structure is **sequential file**.
