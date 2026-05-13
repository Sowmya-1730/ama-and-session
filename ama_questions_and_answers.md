# AMA Questions and Answers

## 1. How to get ASCII value of a character in Python?

### Answer
ASCII value of a character can be obtained using the `ord()` function.

### Example
```python
char = 'A'
print(ord(char))
```

### Output
```python
65
```

---

## 2. How to see Git commit history?

### Answer
Use the following command:

```bash
git log
```

### Useful Variations
```bash
git log --oneline
```

Shows commit history in short format.

```bash
git log --graph
```

Displays commits in graph structure.

---

## 3. What is detached HEAD state in Git?

### Answer
Detached HEAD state occurs when you checkout a specific commit instead of a branch.

### Example
```bash
git checkout <commit_id>
```

In this state:
- You can view old commits
- Changes can be made
- But commits are not attached to any branch unless a new branch is created

### To Create Branch from Detached HEAD
```bash
git checkout -b new_branch
```

---

## 4. What is the difference between `==` operator and `is` in Python?

### Answer

| Operator | Purpose |
|---|---|
| `==` | Checks values equality |
| `is` | Checks memory location (object identity) |

### Example
```python
a = [1, 2]
b = [1, 2]

print(a == b)
print(a is b)
```

### Output
```python
True
False
```

---

## 5. How does Python run a program?

### Answer
Python follows these steps:

1. Source code is written in `.py` file
2. Python compiler converts code into bytecode
3. Bytecode is stored in `.pyc` files
4. Python Virtual Machine (PVM) executes the bytecode

### Flow
```text
Python Code → Bytecode → Python Virtual Machine → Output
```

---

## 6. How to find all Java files in Linux system?

### Answer
Use the `find` command.

### Command
```bash
find / -name "*.java"
```

### Explanation
- `/` → search from root directory
- `-name` → search by file name
- `"*.java"` → all Java files

---

## 7. How to sort contents of a file in Linux?

### Answer
Use the `sort` command.

### Example
```bash
sort file.txt
```

### Reverse Sorting
```bash
sort -r file.txt
```

---

## 8. Why do we use lambda functions in Python?

### Answer
Lambda functions are anonymous functions used for short and simple operations.

### Syntax
```python
lambda arguments: expression
```

### Example
```python
square = lambda x: x * x
print(square(5))
```

### Output
```python
25
```

### Advantages
- Shorter syntax
- Useful with `map()`, `filter()`, and `sorted()`

---

## 9. What is `git checkout`?

### Answer
`git checkout` is used to:
- Switch branches
- Restore files
- Move to specific commits

### Examples

#### Switch Branch
```bash
git checkout main
```

#### Create and Switch Branch
```bash
git checkout -b feature_branch
```

---

## 10. How to recover deleted branch in Git?

### Answer
Use `git reflog` to find deleted branch commit.

### Steps

#### Step 1
```bash
git reflog
```

#### Step 2
Copy commit ID.

#### Step 3
```bash
git checkout -b recovered_branch <commit_id>
```

---

## 11. What is the use of `free` command in Linux?

### Answer
`free` command shows memory usage information.

### Command
```bash
free -h
```

### Displays
- Total memory
- Used memory
- Free memory
- Swap memory

---

## 12. Why do we use virtual environment in Python?

### Answer
Virtual environment isolates project dependencies.

### Advantages
- Avoids package conflicts
- Different projects can use different package versions
- Keeps system Python clean

### Create Virtual Environment
```bash
python -m venv venv
```

### Activate Virtual Environment

#### Linux/Mac
```bash
source venv/bin/activate
```

#### Windows
```bash
venv\Scripts\activate
```

---

## 13. What is recursion in Python?

### Answer
Recursion is a process where a function calls itself.

### Example
```python
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n - 1)

print(factorial(5))
```

### Output
```python
120
```

---

## 14. Why does `.gitignore` start with a dot?

### Answer
In Linux and Unix systems:
- Files starting with `.` are hidden files
- `.gitignore` is a hidden configuration file used by Git

### Purpose
It tells Git which files/folders should not be tracked.

### Example
```text
__pycache__/
venv/
*.log
```

---

## 15. How to go to a particular directory in Linux?

### Answer
Use the `cd` command.

### Example
```bash
cd Documents
```

### Go to Parent Directory
```bash
cd ..
```

### Go to Home Directory
```bash
cd ~
```