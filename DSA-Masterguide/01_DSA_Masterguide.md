# 📖 01 — Data Structures & Algorithms Masterguide
### Deep Theory | Every Concept | From Zero to Advanced

> **File:** `01_DSA_Masterguide.md`
> **Part of:** DSA Repository → [Back to README](./README.md)
> **Audience:** Complete beginners building a strong foundation
> **Pair with:** `03_DSA_Practice_Repository.md` for hands-on problems

---

## 📌 Table of Contents

| # | Section |
|---|---------|
| 1 | [What Is DSA and Why It Matters](#1-what-is-dsa-and-why-it-matters) |
| 2 | [Complexity Analysis — Big O](#2-complexity-analysis--big-o) |
| 3 | [Arrays](#3-arrays) |
| 4 | [Strings](#4-strings) |
| 5 | [Linked Lists](#5-linked-lists) |
| 6 | [Stacks](#6-stacks) |
| 7 | [Queues](#7-queues) |
| 8 | [Hashing](#8-hashing) |
| 9 | [Trees](#9-trees) |
| 10 | [Binary Search Tree](#10-binary-search-tree) |
| 11 | [Heaps](#11-heaps) |
| 12 | [Graphs](#12-graphs) |
| 13 | [Sorting Algorithms](#13-sorting-algorithms) |
| 14 | [Searching Algorithms](#14-searching-algorithms) |
| 15 | [Recursion & Backtracking](#15-recursion--backtracking) |
| 16 | [Dynamic Programming](#16-dynamic-programming) |
| 17 | [Greedy Algorithms](#17-greedy-algorithms) |
| 18 | [Divide and Conquer](#18-divide-and-conquer) |
| 19 | [Two Pointers & Sliding Window](#19-two-pointers--sliding-window) |
| 20 | [Advanced Trees](#20-advanced-trees) |
| 21 | [Advanced Graphs](#21-advanced-graphs) |
| 22 | [Bit Manipulation](#22-bit-manipulation) |
| 23 | [Mathematical Algorithms](#23-mathematical-algorithms) |
| 24 | [Learning Roadmap](#24-learning-roadmap) |
| 25 | [Common Mistakes to Avoid](#25-common-mistakes-to-avoid) |
| 26 | [What to Do While and After Learning](#26-what-to-do-while-and-after-learning) |
| 27 | [Career Paths and Platforms](#27-career-paths-and-platforms) |
| 28 | [Glossary](#28-glossary) |

---
---

# 1. What Is DSA and Why It Matters

## The Real Definition

**Data Structures** are ways of organizing and storing data so that operations on it — accessing, inserting, deleting, searching — can be performed efficiently.

**Algorithms** are step-by-step procedures for solving problems. An algorithm takes input, processes it through a defined sequence of operations, and produces output.

Together, DSA is the answer to one fundamental question every computer program must answer: **How do I organize my data and how do I process it — as efficiently as possible?**

## Why Every Technical Interview Tests DSA

When a company asks you a DSA question, they are not testing whether you memorized a sorting algorithm. They are testing:

**Problem-solving ability** — Can you break a complex problem into smaller parts?

**Reasoning under constraints** — Can you optimize for speed or memory when given tight limits?

**Communication** — Can you explain your thinking clearly?

**Foundation quality** — A person who understands DSA well will write better code in any language, on any problem.

Google, Amazon, Microsoft, Flipkart, Razorpay, Swiggy — every product company uses DSA coding rounds as the primary filter. Even service companies like TCS and Infosys now have DSA sections in their hiring tests.

## The Mental Model — Before You Write a Line of Code

Every time you solve a problem, ask these questions in order:

```
1. What is the INPUT?       → What data am I given? What is its structure?
2. What is the OUTPUT?      → What exactly do I need to return?
3. What are the CONSTRAINTS?→ Size limits? Time? Space?
4. What DATA STRUCTURE fits?→ Array? HashMap? Tree? Graph?
5. What ALGORITHM applies?  → Sort? BFS? DP? Two Pointers?
6. What is the COMPLEXITY?  → Time: O(?), Space: O(?)
7. Can I DO BETTER?         → Is there a more efficient approach?
```

This framework — practiced daily — is what separates good candidates from great ones.

---
---

# 2. Complexity Analysis — Big O

## Why Complexity Analysis Matters

Two programs that solve the same problem correctly are NOT equally good. A program that sorts 1 million numbers in 1 second is better than one that takes 16 minutes — even if both produce the correct output.

Complexity analysis gives us a mathematical language to compare algorithms independent of hardware, programming language, or specific input values. It answers: **as the input size grows, how does the performance grow?**

## Big O Notation — The Language of Efficiency

Big O notation describes the **upper bound** of an algorithm's growth rate — the worst case scenario.

We drop constants and lower-order terms because we care about behavior at scale:

```
5n² + 3n + 7  →  O(n²)
2n + 100      →  O(n)
n/2           →  O(n)
log₂(n) + 5   →  O(log n)
```

## The Big O Hierarchy — Fastest to Slowest

```
O(1)      Constant   — best possible. Same time regardless of input size.
O(log n)  Logarithmic — excellent. Doubles input? Adds one step.
O(n)      Linear     — good. Proportional to input size.
O(n log n)           — acceptable. Most efficient comparison-based sorts.
O(n²)     Quadratic  — bad for large n. Two nested loops.
O(2ⁿ)     Exponential — very bad. Doubles with each added element.
O(n!)     Factorial  — worst. Only for tiny inputs.
```

### Visualizing the Difference

```
n = 1,000 elements:

O(1)       →         1 operation
O(log n)   →        10 operations
O(n)       →     1,000 operations
O(n log n) →    10,000 operations
O(n²)      → 1,000,000 operations
O(2ⁿ)      → 10^301 operations   ← impossible
```

## Rules for Calculating Big O

### Rule 1: Drop Constants
```python
for i in range(n):      # O(n)
    print(i)
for j in range(n):      # O(n)
    print(j)
# Total: O(n) + O(n) = O(2n) → O(n)
```

### Rule 2: Drop Lower Order Terms
```python
for i in range(n):          # O(n)
    for j in range(n):      # O(n²)
        print(i, j)
# Total: O(n² + n) → O(n²)
```

### Rule 3: Different Inputs = Different Variables
```python
def func(a, b):
    for x in a:          # O(a)
        print(x)
    for y in b:          # O(b)
        print(y)
# Total: O(a + b)   NOT O(n) — two different arrays!
```

### Rule 4: Nested Loops Multiply
```python
for i in range(n):        # O(n)
    for j in range(n):    # O(n)
        print(i, j)       # O(n × n) = O(n²)
```

### Rule 5: Recursive = Look at the Recursion Tree
```python
def fibonacci(n):
    if n <= 1: return n
    return fibonacci(n-1) + fibonacci(n-2)
# Each call makes 2 more calls → O(2ⁿ)
```

## Common Examples — Calculate Before Reading Answer

**Example 1:**
```python
for i in range(n):
    print(i)           # → O(n)
```

**Example 2:**
```python
for i in range(n):
    for j in range(i, n):
        print(i, j)    # → O(n²) — inner loop is n, n-1, n-2... ≈ n²/2 → O(n²)
```

**Example 3:**
```python
i = n
while i > 1:
    i = i // 2         # → O(log n) — halving each step
```

**Example 4:**
```python
for i in range(n):
    j = 1
    while j < n:
        j *= 2         # → O(n log n) — outer O(n), inner O(log n)
```

## Space Complexity

Space complexity measures how much extra memory an algorithm uses as input grows.

```python
def sum_array(arr):
    total = 0              # O(1) space — just one variable
    for x in arr:
        total += x
    return total           # Space: O(1)

def copy_array(arr):
    result = []
    for x in arr:
        result.append(x)   # Creates new array of same size
    return result          # Space: O(n)

def merge_sort(arr):
    ...                    # Creates new arrays at each level
                           # Space: O(n) — stores n elements total across levels
```

## Complexity of Common Operations — Master Table

### Data Structure Operations

| Data Structure | Access | Search | Insert | Delete | Space |
|----------------|--------|--------|--------|--------|-------|
| Array | O(1) | O(n) | O(n) | O(n) | O(n) |
| Dynamic Array | O(1) | O(n) | O(1)* | O(n) | O(n) |
| Singly Linked List | O(n) | O(n) | O(1)** | O(1)** | O(n) |
| Doubly Linked List | O(n) | O(n) | O(1)** | O(1)** | O(n) |
| Stack | O(n) | O(n) | O(1) | O(1) | O(n) |
| Queue | O(n) | O(n) | O(1) | O(1) | O(n) |
| Hash Table | O(1)* | O(1)* | O(1)* | O(1)* | O(n) |
| BST (balanced) | O(log n) | O(log n) | O(log n) | O(log n) | O(n) |
| BST (unbalanced) | O(n) | O(n) | O(n) | O(n) | O(n) |
| Min/Max Heap | O(n) | O(n) | O(log n) | O(log n) | O(n) |
| Trie | — | O(m) | O(m) | O(m) | O(n×m) |

*amortized or average | **with pointer to node

### Sorting Algorithms

| Algorithm | Best | Average | Worst | Space | Stable? |
|-----------|------|---------|-------|-------|---------|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ Yes |
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) | ❌ No |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ Yes |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | ✅ Yes |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) | ❌ No |
| Heap Sort | O(n log n) | O(n log n) | O(n log n) | O(1) | ❌ No |
| Counting Sort | O(n+k) | O(n+k) | O(n+k) | O(k) | ✅ Yes |
| Radix Sort | O(nk) | O(nk) | O(nk) | O(n+k) | ✅ Yes |

---
---

# 3. Arrays

## What Is an Array?

An array is a collection of elements stored at **contiguous memory locations**. All elements are of the same data type. Each element is accessible directly by its **index** (position).

```
Index:   0     1     2     3     4
       ┌─────┬─────┬─────┬─────┬─────┐
Array: │  10 │  20 │  30 │  40 │  50 │
       └─────┴─────┴─────┴─────┴─────┘
Address: 1000  1004  1008  1012  1016   (each int = 4 bytes)
```

**Why O(1) access?** Because the memory address of any element can be calculated directly:
`address = base_address + (index × element_size)`

No searching needed. Jump directly to the address.

## Static vs Dynamic Arrays

**Static Array:** Fixed size declared at creation. Size cannot change. Used in C, C++.
```c
int arr[5] = {10, 20, 30, 40, 50};  // Fixed size 5 forever
```

**Dynamic Array:** Automatically resizes when full. Used in Python (list), Java (ArrayList), C++ (vector).

**How dynamic resizing works:**
1. Start with capacity = 1
2. When full, create new array with capacity × 2
3. Copy all elements to new array
4. This doubling strategy means insertions are O(1) **amortized** (average) even though occasional copies are O(n)

```
Python list internal behavior:
size 1 → full → resize to 2
size 2 → full → resize to 4
size 4 → full → resize to 8
...

Total copies for n insertions ≈ 1 + 2 + 4 + ... + n ≈ 2n → O(1) per insertion on average
```

## Key Array Operations

```python
arr = [10, 20, 30, 40, 50]

# Access — O(1)
print(arr[2])          # 30

# Search — O(n) worst case
def linear_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i
    return -1

# Insert at end — O(1) amortized
arr.append(60)

# Insert at index — O(n) (shifts elements right)
arr.insert(2, 25)      # [10, 20, 25, 30, 40, 50, 60]

# Delete by index — O(n) (shifts elements left)
arr.pop(2)             # removes index 2 → [10, 20, 30, 40, 50, 60]

# Delete by value — O(n)
arr.remove(30)

# Traverse — O(n)
for element in arr:
    print(element)

# Reverse — O(n)
arr.reverse()          # in-place
reversed_arr = arr[::-1]  # creates new array

# Sort — O(n log n)
arr.sort()             # in-place Timsort
sorted_arr = sorted(arr)  # returns new sorted array
```

## 2D Arrays (Matrix)

A 2D array is an array of arrays — rows and columns.

```python
matrix = [
    [1, 2, 3],    # row 0
    [4, 5, 6],    # row 1
    [7, 8, 9]     # row 2
]

# Access element at row 1, col 2
print(matrix[1][2])    # 6

# Traverse all elements — O(m × n)
for row in matrix:
    for val in row:
        print(val)

# Number of rows
rows = len(matrix)        # 3

# Number of columns
cols = len(matrix[0])     # 3
```

**Common 2D array operations in interviews:**
- Transpose: swap matrix[i][j] with matrix[j][i]
- Rotate 90°: transpose then reverse each row
- Spiral order traversal
- Layer-by-layer processing

## Important Array Techniques

### Prefix Sum
Precompute cumulative sums so any range sum is O(1) instead of O(n).

```python
arr = [3, 1, 4, 1, 5, 9, 2, 6]
n = len(arr)

# Build prefix sum — O(n)
prefix = [0] * (n + 1)
for i in range(n):
    prefix[i+1] = prefix[i] + arr[i]
# prefix = [0, 3, 4, 8, 9, 14, 23, 25, 31]

# Query: sum from index l to r (inclusive) — O(1)
def range_sum(l, r):
    return prefix[r+1] - prefix[l]

print(range_sum(2, 5))   # arr[2]+arr[3]+arr[4]+arr[5] = 4+1+5+9 = 19
```

### Kadane's Algorithm — Maximum Subarray Sum
Find the contiguous subarray with the maximum sum.

```python
def max_subarray(arr):
    max_sum = arr[0]
    current_sum = arr[0]

    for i in range(1, len(arr)):
        # Either extend current subarray or start fresh
        current_sum = max(arr[i], current_sum + arr[i])
        max_sum = max(max_sum, current_sum)

    return max_sum

# arr = [-2, 1, -3, 4, -1, 2, 1, -5, 4]
# Answer: 6 (subarray [4, -1, 2, 1])
# Time: O(n), Space: O(1)
```

---
---

# 4. Strings

## What Is a String?

A string is a sequence of characters. In most languages, strings are **immutable** — you cannot change a character in place. Any modification creates a new string.

```python
s = "hello"
s[0] = 'H'    # ❌ TypeError in Python — strings are immutable

s = 'H' + s[1:]  # ✅ creates new string "Hello"
```

**Why immutability matters for complexity:**
```python
# This looks like O(n) but is actually O(n²)!
result = ""
for char in s:
    result += char    # Each += creates a NEW string and copies

# The correct approach — O(n):
chars = []
for char in s:
    chars.append(char)
result = "".join(chars)   # One join operation at the end
```

## String Operations and Complexity

```python
s = "hello world"

# Length — O(1) in Python (stored)
n = len(s)

# Access character — O(1)
print(s[0])        # 'h'

# Slice — O(k) where k is slice length
sub = s[2:5]       # 'llo'

# Concatenation — O(n+m) creates new string
s2 = s + " python"

# Find substring — O(n×m) naive, O(n) with KMP
idx = s.find("world")    # 6

# Split — O(n)
words = s.split(" ")     # ['hello', 'world']

# Join — O(n)
joined = "-".join(words) # 'hello-world'

# Convert to list of chars — O(n)
chars = list(s)

# Reverse — O(n)
rev = s[::-1]     # 'dlrow olleh'

# Upper/Lower — O(n)
upper = s.upper()

# Replace — O(n)
new_s = s.replace("world", "python")

# Check if palindrome — O(n)
def is_palindrome(s):
    return s == s[::-1]
```

## Important String Techniques

### Character Frequency with HashMap
```python
from collections import Counter

s = "aabbbcccc"
freq = Counter(s)    # {'c': 4, 'b': 3, 'a': 2}

# Or manual:
freq = {}
for char in s:
    freq[char] = freq.get(char, 0) + 1
```

### Sliding Window for Substrings
Find the longest substring without repeating characters:
```python
def length_of_longest_substring(s):
    char_index = {}
    max_len = 0
    left = 0

    for right in range(len(s)):
        if s[right] in char_index and char_index[s[right]] >= left:
            left = char_index[s[right]] + 1
        char_index[s[right]] = right
        max_len = max(max_len, right - left + 1)

    return max_len
# Time: O(n), Space: O(min(m,n)) where m = charset size
```

### Two Pointers for Palindrome Check
```python
def is_palindrome(s):
    left, right = 0, len(s) - 1
    while left < right:
        if s[left] != s[right]:
            return False
        left += 1
        right -= 1
    return True
# Time: O(n), Space: O(1)
```

---
---

# 5. Linked Lists

## What Is a Linked List?

A linked list is a linear data structure where elements (called **nodes**) are stored at non-contiguous memory locations. Each node contains:
1. **Data** — the value stored
2. **Next** — a pointer/reference to the next node

```
Linked List: 10 → 20 → 30 → 40 → None

Node structure:
┌──────┬──────┐   ┌──────┬──────┐   ┌──────┬──────┐
│  10  │  ●───┼──►│  20  │  ●───┼──►│  30  │ None │
└──────┴──────┘   └──────┴──────┘   └──────┴──────┘
 data   next        data   next        data   next
```

**Why use linked list over array?**
- Insert/delete at beginning or middle: O(1) if you have the pointer (no shifting!)
- Dynamic size — no need to declare size upfront
- Trade-off: No O(1) random access, extra memory for pointers

## Node Implementation

```python
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

# Create: 1 → 2 → 3
head = ListNode(1)
head.next = ListNode(2)
head.next.next = ListNode(3)
```

## Traversal

```python
def traverse(head):
    current = head
    while current:
        print(current.val)
        current = current.next
# Time: O(n), Space: O(1)
```

## Core Operations

### Insert at Beginning — O(1)
```python
def insert_at_beginning(head, val):
    new_node = ListNode(val)
    new_node.next = head
    return new_node    # new_node is the new head
```

### Insert at End — O(n)
```python
def insert_at_end(head, val):
    new_node = ListNode(val)
    if not head:
        return new_node
    current = head
    while current.next:    # traverse to last node
        current = current.next
    current.next = new_node
    return head
```

### Delete a Node — O(n) to find, O(1) to delete
```python
def delete_node(head, val):
    dummy = ListNode(0)    # dummy node before head handles edge cases
    dummy.next = head
    current = dummy
    while current.next:
        if current.next.val == val:
            current.next = current.next.next    # skip the node
            break
        current = current.next
    return dummy.next
```

## Reverse a Linked List — Must Know ⭐⭐⭐⭐⭐

```python
def reverse_list(head):
    prev = None
    current = head

    while current:
        next_node = current.next    # save next
        current.next = prev         # reverse the pointer
        prev = current              # move prev forward
        current = next_node         # move current forward

    return prev    # prev is now the new head

# Visual:
# Before: 1 → 2 → 3 → None
# Step 1: None ← 1   2 → 3 → None
# Step 2: None ← 1 ← 2   3 → None
# Step 3: None ← 1 ← 2 ← 3
# Return: 3 (new head)
# Time: O(n), Space: O(1)
```

## Detect Cycle — Floyd's Algorithm ⭐⭐⭐⭐⭐

```python
def has_cycle(head):
    slow = head
    fast = head

    while fast and fast.next:
        slow = slow.next           # moves 1 step
        fast = fast.next.next      # moves 2 steps

        if slow == fast:           # they meet inside cycle
            return True

    return False    # fast reached end → no cycle

# Why it works: if cycle exists, fast gains 1 step per iteration
# on slow, eventually catches up (like two runners on a circular track)
# Time: O(n), Space: O(1)
```

## Find Middle of Linked List

```python
def find_middle(head):
    slow = head
    fast = head

    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next

    return slow    # slow is at middle when fast reaches end
# Time: O(n), Space: O(1)
```

## Doubly Linked List

Each node has both `next` and `prev` pointers.

```python
class DListNode:
    def __init__(self, val=0):
        self.val = val
        self.next = None
        self.prev = None

# Structure:
# None ← 1 ↔ 2 ↔ 3 → None
```

**Advantages over singly:** Can traverse backward. Delete a node without needing the previous node (O(1) delete with node reference).

**Use cases:** Browser history (forward/back), LRU Cache implementation, Doubly Ended Queue (Deque).

## Circular Linked List

Last node's `next` points back to the first node instead of None.

```
1 → 2 → 3 → 4
↑_____________|
```

**Use cases:** Round-robin scheduling, multiplayer game turns, circular buffer.

---
---

# 6. Stacks

## What Is a Stack?

A stack is a linear data structure following **LIFO — Last In, First Out**. Think of a stack of plates — you add to the top and remove from the top.

```
PUSH 10, 20, 30:       POP:
   [30]  ← TOP           [20]  ← TOP (30 removed)
   [20]                  [10]
   [10]
```

**Key operations:**
- **push(x):** Add element to top — O(1)
- **pop():** Remove and return top element — O(1)
- **peek()/top():** View top without removing — O(1)
- **isEmpty():** Check if empty — O(1)

## Implementation

### Using Python List
```python
stack = []

stack.append(10)    # push
stack.append(20)
stack.append(30)

top = stack[-1]     # peek → 30
stack.pop()         # pop → removes 30
print(stack)        # [10, 20]
```

### Implementing from Scratch
```python
class Stack:
    def __init__(self):
        self.items = []

    def push(self, item):
        self.items.append(item)

    def pop(self):
        if self.is_empty():
            raise IndexError("Pop from empty stack")
        return self.items.pop()

    def peek(self):
        if self.is_empty():
            raise IndexError("Peek at empty stack")
        return self.items[-1]

    def is_empty(self):
        return len(self.items) == 0

    def size(self):
        return len(self.items)
```

## The Call Stack — How Your Program Actually Works

Every function call uses a stack internally:

```python
def c():
    print("C executing")

def b():
    c()
    print("B executing")

def a():
    b()
    print("A executing")

a()

# Call stack during execution:
# ┌─────┐
# │  c  │  ← currently executing
# │  b  │
# │  a  │
# └─────┘
# When c() returns → popped. b() resumes.
# When b() returns → popped. a() resumes.
```

**Stack overflow:** Happens when too many function calls are pushed — usually from infinite recursion.

## Classic Stack Problems

### Valid Parentheses ⭐⭐⭐⭐⭐
```python
def is_valid(s):
    stack = []
    mapping = {')': '(', '}': '{', ']': '['}

    for char in s:
        if char in '({[':
            stack.append(char)
        elif char in ')}]':
            if not stack or stack[-1] != mapping[char]:
                return False
            stack.pop()

    return len(stack) == 0

# "()[]{}" → True
# "([)]"   → False
# Time: O(n), Space: O(n)
```

### Next Greater Element ⭐⭐⭐⭐
```python
def next_greater_element(arr):
    n = len(arr)
    result = [-1] * n
    stack = []    # stores indices

    for i in range(n):
        while stack and arr[i] > arr[stack[-1]]:
            idx = stack.pop()
            result[idx] = arr[i]
        stack.append(i)

    return result

# arr = [4, 5, 2, 10, 8]
# NGE  = [5, 10, 10, -1, -1]
# Time: O(n), Space: O(n)
```

---
---

# 7. Queues

## What Is a Queue?

A queue is a linear data structure following **FIFO — First In, First Out**. Think of a line at a billing counter — first person in line is served first.

```
ENQUEUE 10, 20, 30:    DEQUEUE:
FRONT → [10][20][30] ← REAR    FRONT → [20][30] ← REAR (10 removed)
```

**Key operations:**
- **enqueue(x):** Add to rear — O(1)
- **dequeue():** Remove from front — O(1)
- **peek()/front():** View front — O(1)
- **isEmpty():** Check if empty — O(1)

## Implementation

### Using collections.deque (Best in Python)
```python
from collections import deque

queue = deque()
queue.append(10)      # enqueue to rear
queue.append(20)
queue.append(30)

front = queue[0]      # peek → 10
queue.popleft()       # dequeue → removes 10
print(queue)          # deque([20, 30])
```

### Circular Queue
A fixed-size queue that wraps around. Uses modular arithmetic to reuse space.

```python
class CircularQueue:
    def __init__(self, k):
        self.queue = [None] * k
        self.head = 0
        self.tail = -1
        self.size = 0
        self.capacity = k

    def enqueue(self, val):
        if self.size == self.capacity:
            return False    # full
        self.tail = (self.tail + 1) % self.capacity
        self.queue[self.tail] = val
        self.size += 1
        return True

    def dequeue(self):
        if self.size == 0:
            return False    # empty
        self.head = (self.head + 1) % self.capacity
        self.size -= 1
        return True
```

## Priority Queue (Heap-Based)

A priority queue dequeues the element with **highest priority** (typically smallest or largest value) first — not necessarily the one inserted first.

```python
import heapq

# Min-heap (default in Python) — smallest element dequeued first
pq = []
heapq.heappush(pq, 5)
heapq.heappush(pq, 1)
heapq.heappush(pq, 3)

print(heapq.heappop(pq))    # 1 (smallest)
print(heapq.heappop(pq))    # 3
print(heapq.heappop(pq))    # 5

# Max-heap trick: negate values
heapq.heappush(pq, -5)
heapq.heappush(pq, -1)
print(-heapq.heappop(pq))   # 5 (largest)
```

## Deque (Double Ended Queue)

A deque supports insert and delete from **both ends** in O(1).

```python
from collections import deque

dq = deque()
dq.appendleft(10)   # insert at front
dq.append(20)       # insert at rear
dq.popleft()        # remove from front
dq.pop()            # remove from rear
```

**Use case:** Sliding window maximum — maintain a deque of indices.

---
---

# 8. Hashing

## What Is Hashing?

Hashing converts a key into an array index using a **hash function**. The goal is to store and retrieve values in O(1) time.

```
key = "apple"
hash("apple") = 7 % 10 = 7     → store value at index 7

index: 0  1  2  3  4  5  6  7  8  9
       [  ][  ][  ][  ][  ][  ][  ][val][  ][  ]
```

## Hash Function Properties

A good hash function is:
- **Deterministic:** Same key always produces same hash
- **Uniform:** Keys spread evenly across the table (minimize collisions)
- **Fast:** O(1) to compute

## Collision Handling

A **collision** occurs when two different keys produce the same hash. Two main strategies:

### 1. Chaining (Open Hashing)
Each index stores a linked list of all keys that hash to it.

```
index 3: [("cat", 5)] → [("bat", 8)] → None
```

- Search: O(1) average, O(n) worst (all keys collide)
- Used in Python dict, Java HashMap

### 2. Open Addressing (Linear Probing)
If index is taken, try the next slot (or use a probe sequence).

```
hash("cat") = 3, slot 3 is taken → try slot 4 → try slot 5...
```

## HashMap in Python

```python
# Create
d = {}
d = dict()

# Insert/Update — O(1) average
d["name"] = "Alice"
d["age"] = 25

# Access — O(1) average
print(d["name"])           # "Alice"
print(d.get("age", 0))     # 25 (0 is default if key missing)

# Delete — O(1) average
del d["age"]

# Check existence — O(1) average
if "name" in d:
    print("key exists")

# Iterate
for key, value in d.items():
    print(key, value)

# All keys / values
keys = d.keys()
values = d.values()
```

## HashSet in Python

```python
# Create
s = set()
s = {1, 2, 3}

# Add — O(1)
s.add(4)

# Remove — O(1)
s.remove(4)        # raises KeyError if not found
s.discard(4)       # safe — no error if not found

# Check membership — O(1)
print(3 in s)      # True

# Set operations
a = {1, 2, 3}
b = {2, 3, 4}
print(a | b)       # union: {1, 2, 3, 4}
print(a & b)       # intersection: {2, 3}
print(a - b)       # difference: {1}
```

## Classic Hashing Patterns

### Two Sum — The Most Classic Hash Problem ⭐⭐⭐⭐⭐
```python
def two_sum(nums, target):
    seen = {}    # value → index
    for i, num in enumerate(nums):
        complement = target - num
        if complement in seen:
            return [seen[complement], i]
        seen[num] = i
    return []

# Time: O(n), Space: O(n)
# Key insight: for each element, check if its complement was seen before
```

### Detect Duplicates
```python
def contains_duplicate(nums):
    return len(nums) != len(set(nums))
# Time: O(n), Space: O(n)
```

### Group Anagrams ⭐⭐⭐⭐
```python
from collections import defaultdict

def group_anagrams(strs):
    groups = defaultdict(list)
    for s in strs:
        key = tuple(sorted(s))    # "eat" → ('a', 'e', 't')
        groups[key].append(s)
    return list(groups.values())

# ["eat","tea","tan","ate","nat","bat"]
# → [["eat","tea","ate"], ["tan","nat"], ["bat"]]
# Time: O(n × k log k) where k = max string length
```

---
---

# 9. Trees

## What Is a Tree?

A tree is a **hierarchical** (non-linear) data structure. Unlike linear structures (arrays, linked lists), trees branch. Each tree has:

- **Root:** The topmost node (no parent)
- **Parent/Child:** A node with connections below it
- **Leaf:** A node with no children
- **Edge:** Connection between two nodes
- **Height:** Longest path from root to any leaf
- **Depth:** Distance from root to a specific node

```
            1          ← Root (depth 0)
           / \
          2   3        ← depth 1
         / \   \
        4   5   6      ← depth 2 (leaves 4, 5, 6)

Height of tree = 2
Height of node 2 = 1
```

## Binary Tree

A binary tree is a tree where each node has **at most 2 children** — left and right.

```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right

# Build the tree above:
root = TreeNode(1)
root.left = TreeNode(2)
root.right = TreeNode(3)
root.left.left = TreeNode(4)
root.left.right = TreeNode(5)
root.right.right = TreeNode(6)
```

## Tree Traversals ⭐⭐⭐⭐⭐

Traversal = visiting every node exactly once in a specific order.

### Inorder (Left → Root → Right)
```python
def inorder(root):
    if not root:
        return
    inorder(root.left)
    print(root.val)       # visit root BETWEEN left and right
    inorder(root.right)

# Result for tree above: 4, 2, 5, 1, 3, 6
# KEY FACT: Inorder traversal of a BST gives SORTED order!
```

### Preorder (Root → Left → Right)
```python
def preorder(root):
    if not root:
        return
    print(root.val)       # visit root FIRST
    preorder(root.left)
    preorder(root.right)

# Result: 1, 2, 4, 5, 3, 6
# Use: Serialize/copy a tree. Root is always first.
```

### Postorder (Left → Right → Root)
```python
def postorder(root):
    if not root:
        return
    postorder(root.left)
    postorder(root.right)
    print(root.val)       # visit root LAST

# Result: 4, 5, 2, 6, 3, 1
# Use: Delete a tree (delete children before parent). Evaluate expression trees.
```

### Level Order (BFS — Level by Level)
```python
from collections import deque

def level_order(root):
    if not root:
        return []
    result = []
    queue = deque([root])

    while queue:
        level_size = len(queue)
        level = []

        for _ in range(level_size):
            node = queue.popleft()
            level.append(node.val)
            if node.left:
                queue.append(node.left)
            if node.right:
                queue.append(node.right)

        result.append(level)

    return result
# Result: [[1], [2, 3], [4, 5, 6]]
# Time: O(n), Space: O(n)
```

## Important Tree Properties

### Height of a Binary Tree
```python
def height(root):
    if not root:
        return -1    # or 0 depending on convention
    left_height = height(root.left)
    right_height = height(root.right)
    return 1 + max(left_height, right_height)
# Time: O(n), Space: O(h) where h = height
```

### Count Nodes
```python
def count_nodes(root):
    if not root:
        return 0
    return 1 + count_nodes(root.left) + count_nodes(root.right)
```

### Diameter of Binary Tree
Longest path between any two nodes (may not pass through root):
```python
def diameter(root):
    max_diameter = [0]

    def depth(node):
        if not node:
            return 0
        left = depth(node.left)
        right = depth(node.right)
        max_diameter[0] = max(max_diameter[0], left + right)
        return 1 + max(left, right)

    depth(root)
    return max_diameter[0]
# Time: O(n), Space: O(h)
```

### Check if Balanced
A balanced tree has abs(left_height - right_height) ≤ 1 for every node:
```python
def is_balanced(root):
    def check(node):
        if not node:
            return 0
        left = check(node.left)
        if left == -1:
            return -1
        right = check(node.right)
        if right == -1:
            return -1
        if abs(left - right) > 1:
            return -1
        return 1 + max(left, right)

    return check(root) != -1
```

---
---

# 10. Binary Search Tree

## What Is a BST?

A Binary Search Tree is a binary tree with one critical property:

**For every node N:**
- All nodes in N's **left subtree** have values **less than** N
- All nodes in N's **right subtree** have values **greater than** N

```
         8
        / \
       3   10
      / \    \
     1   6    14
        / \   /
       4   7 13

BST property holds everywhere:
- 3 < 8, and 10 > 8 ✓
- 1 < 3, and 6 > 3 ✓
- All nodes in left subtree of 8 (1,3,4,6,7) < 8 ✓
- All nodes in right subtree of 8 (10,13,14) > 8 ✓
```

## BST Operations

### Search — O(log n) average, O(n) worst
```python
def search(root, target):
    if not root:
        return None
    if root.val == target:
        return root
    elif target < root.val:
        return search(root.left, target)    # go left
    else:
        return search(root.right, target)   # go right
```

### Insert — O(log n) average
```python
def insert(root, val):
    if not root:
        return TreeNode(val)
    if val < root.val:
        root.left = insert(root.left, val)
    elif val > root.val:
        root.right = insert(root.right, val)
    return root    # val == root.val: duplicate, don't insert
```

### Delete — O(log n) average (3 cases)
```python
def delete(root, key):
    if not root:
        return None

    if key < root.val:
        root.left = delete(root.left, key)
    elif key > root.val:
        root.right = delete(root.right, key)
    else:
        # Case 1: Leaf node — just remove
        if not root.left and not root.right:
            return None

        # Case 2: One child — replace with child
        if not root.left:
            return root.right
        if not root.right:
            return root.left

        # Case 3: Two children
        # Find inorder successor (smallest in right subtree)
        successor = root.right
        while successor.left:
            successor = successor.left
        root.val = successor.val            # copy successor value
        root.right = delete(root.right, successor.val)  # delete successor

    return root
```

## BST Key Properties

1. **Inorder traversal gives sorted array** — fundamental property used in many problems
2. **Minimum value:** Go left until no more left → leftmost node
3. **Maximum value:** Go right until no more right → rightmost node
4. **Height balanced BST:** Operations are O(log n). Degenerate (sorted input) is O(n)

## Validate a BST ⭐⭐⭐⭐
```python
def is_valid_bst(root, min_val=float('-inf'), max_val=float('inf')):
    if not root:
        return True
    if root.val <= min_val or root.val >= max_val:
        return False
    return (is_valid_bst(root.left, min_val, root.val) and
            is_valid_bst(root.right, root.val, max_val))
# Time: O(n), Space: O(h)
```

---
---

# 11. Heaps

## What Is a Heap?

A heap is a **complete binary tree** (all levels filled except possibly the last, filled left to right) that satisfies the **heap property**:

- **Min Heap:** Every node is ≤ its children → root is the minimum
- **Max Heap:** Every node is ≥ its children → root is the maximum

```
Min Heap:        Max Heap:
     1                9
    / \              / \
   3   2            7   8
  / \ / \          / \ / \
 6  4 5  7        2  3 4  5
```

**Key insight:** A heap is NOT fully sorted — it only guarantees the root is min/max. The heap property is maintained efficiently.

## Heap as Array

A heap is stored in an array — the tree structure is implicit:
```
For node at index i:
  Left child  = 2i + 1
  Right child = 2i + 2
  Parent      = (i - 1) // 2

Min Heap: [1, 3, 2, 6, 4, 5, 7]
Index:     0  1  2  3  4  5  6

  0:1 → children at 1:3 and 2:2
  1:3 → children at 3:6 and 4:4
  2:2 → children at 5:5 and 6:7
```

## Heap Operations

### Insert (Push) — O(log n)
Add to end of array, then "bubble up" (sift up):
```
Insert 0 into min heap [1, 3, 2, 6, 4, 5, 7]:
1. Add to end: [1, 3, 2, 6, 4, 5, 7, 0]
2. 0 < parent(3) → swap: [1, 3, 2, 0, 4, 5, 7, 6]
3. 0 < parent(1) → swap: [0, 3, 2, 1, 4, 5, 7, 6]
4. 0 is at root → done
```

### Extract Min — O(log n)
Remove root, put last element at root, "bubble down" (sift down):
```
Extract min from [1, 3, 2, 6, 4, 5, 7]:
1. Remove 1, put last (7) at root: [7, 3, 2, 6, 4, 5]
2. 7 > min(left=3, right=2) → swap with 2: [2, 3, 7, 6, 4, 5]
3. 7 > min(left=5) → swap with 5: [2, 3, 5, 6, 4, 7]
4. 7 is leaf → done. Return 1.
```

## Python heapq Module

```python
import heapq

# Min heap
heap = []
heapq.heappush(heap, 5)
heapq.heappush(heap, 1)
heapq.heappush(heap, 3)

print(heap[0])              # peek minimum → 1
print(heapq.heappop(heap))  # extract minimum → 1
print(heapq.heappop(heap))  # → 3
print(heapq.heappop(heap))  # → 5

# Build heap from list — O(n)
arr = [5, 1, 3, 2, 4]
heapq.heapify(arr)          # arr becomes [1, 2, 3, 5, 4]

# Max heap trick — negate all values
max_heap = []
heapq.heappush(max_heap, -5)
heapq.heappush(max_heap, -1)
heapq.heappush(max_heap, -3)
print(-heapq.heappop(max_heap))   # 5 (maximum)

# K largest elements
import heapq
def k_largest(nums, k):
    return heapq.nlargest(k, nums)   # O(n log k)

# K smallest elements
def k_smallest(nums, k):
    return heapq.nsmallest(k, nums)  # O(n log k)
```

## Classic Heap Problem — Kth Largest Element ⭐⭐⭐⭐⭐
```python
def find_kth_largest(nums, k):
    # Maintain a min-heap of size k
    # The kth largest = the minimum of the top k largest
    heap = nums[:k]
    heapq.heapify(heap)    # O(k)

    for num in nums[k:]:
        if num > heap[0]:
            heapq.heapreplace(heap, num)    # O(log k)

    return heap[0]

# Time: O(n log k), Space: O(k)
```

---
---

# 12. Graphs

## What Is a Graph?

A graph is a collection of **vertices (nodes)** connected by **edges**. Unlike trees, graphs can have cycles, and there is no root.

```
Undirected Graph:         Directed Graph (Digraph):
    A—B                       A → B
   /|  \                      ↑     ↓
  D | C  |                    D ← C
   \|/                        
    E
```

**Types of graphs:**
- **Directed/Undirected:** Edges have direction or not
- **Weighted/Unweighted:** Edges have weights (distances, costs) or not
- **Cyclic/Acyclic:** Contains a cycle or not (DAG = Directed Acyclic Graph)
- **Connected/Disconnected:** All vertices reachable from any vertex or not

## Graph Representations

### 1. Adjacency List (Most Common)
```python
# Undirected graph
graph = {
    'A': ['B', 'D', 'E'],
    'B': ['A', 'C'],
    'C': ['B', 'E'],
    'D': ['A', 'E'],
    'E': ['A', 'C', 'D']
}

# Directed graph from edge list
from collections import defaultdict

def build_graph(edges):
    graph = defaultdict(list)
    for u, v in edges:
        graph[u].append(v)
        # For undirected: graph[v].append(u)
    return graph

edges = [(0,1),(0,2),(1,3),(2,3)]
graph = build_graph(edges)
# {0: [1,2], 1: [0,3], 2: [0,3], 3: [1,2]}
```

### 2. Adjacency Matrix
```python
# For n vertices: n×n matrix
# matrix[i][j] = 1 if edge from i to j, else 0
n = 4
matrix = [[0]*n for _ in range(n)]
matrix[0][1] = 1    # edge 0→1
matrix[0][2] = 1    # edge 0→2

# Space: O(V²) — wasteful for sparse graphs
# Edge check: O(1)
# Get neighbors: O(V)
```

**Which to use?**
- Adjacency list: sparse graphs (most real problems) — O(V+E) space
- Adjacency matrix: dense graphs, frequent edge queries — O(V²) space

## BFS — Breadth First Search ⭐⭐⭐⭐⭐

BFS explores all neighbors at the current level before going deeper. Uses a **queue**.

```python
from collections import deque

def bfs(graph, start):
    visited = set()
    queue = deque([start])
    visited.add(start)
    order = []

    while queue:
        node = queue.popleft()
        order.append(node)

        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)

    return order

# Use BFS for:
# - Shortest path in UNWEIGHTED graph
# - Level-by-level processing
# - Finding connected components
# Time: O(V + E), Space: O(V)
```

## DFS — Depth First Search ⭐⭐⭐⭐⭐

DFS explores as far as possible along each branch before backtracking. Uses a **stack** (or recursion).

```python
# Recursive DFS
def dfs(graph, node, visited=None):
    if visited is None:
        visited = set()
    visited.add(node)
    print(node)

    for neighbor in graph[node]:
        if neighbor not in visited:
            dfs(graph, neighbor, visited)

    return visited

# Iterative DFS
def dfs_iterative(graph, start):
    visited = set()
    stack = [start]
    order = []

    while stack:
        node = stack.pop()
        if node not in visited:
            visited.add(node)
            order.append(node)
            for neighbor in graph[node]:
                if neighbor not in visited:
                    stack.append(neighbor)

    return order

# Use DFS for:
# - Detecting cycles
# - Topological sort
# - Finding all paths
# - Connected components
# Time: O(V + E), Space: O(V)
```

## Detect Cycle in Undirected Graph
```python
def has_cycle_undirected(graph):
    visited = set()

    def dfs(node, parent):
        visited.add(node)
        for neighbor in graph[node]:
            if neighbor not in visited:
                if dfs(neighbor, node):
                    return True
            elif neighbor != parent:    # visited but not parent → cycle!
                return True
        return False

    for node in graph:
        if node not in visited:
            if dfs(node, -1):
                return True
    return False
```

## Number of Islands ⭐⭐⭐⭐⭐
```python
def num_islands(grid):
    if not grid:
        return 0

    rows, cols = len(grid), len(grid[0])
    count = 0

    def dfs(r, c):
        if r < 0 or r >= rows or c < 0 or c >= cols or grid[r][c] == '0':
            return
        grid[r][c] = '0'    # mark as visited (sink the island)
        dfs(r+1, c)
        dfs(r-1, c)
        dfs(r, c+1)
        dfs(r, c-1)

    for r in range(rows):
        for c in range(cols):
            if grid[r][c] == '1':
                count += 1
                dfs(r, c)

    return count
# Time: O(m × n), Space: O(m × n) worst case recursion
```

---
---

# 13. Sorting Algorithms

## Why Learn Sorting From Scratch?

In practice, you use built-in sort functions. But interviews ask about sorting because it tests:
- Understanding of algorithm design strategies
- Ability to analyze time/space complexity
- Knowledge of trade-offs (stability, in-place, worst-case)

## Bubble Sort — O(n²)

Repeatedly swap adjacent elements that are out of order. Largest element "bubbles" to the end each pass.

```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        swapped = False
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
        if not swapped:    # optimization: early exit if sorted
            break
    return arr

# Best: O(n) with swapped optimization
# Average/Worst: O(n²)
# Space: O(1) — in-place
# Stable: Yes
```

## Selection Sort — O(n²)

Find the minimum element in the unsorted portion and place it at the beginning.

```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        min_idx = i
        for j in range(i+1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]
    return arr

# Always O(n²) — no early exit possible
# Space: O(1) — in-place
# Stable: No
```

## Insertion Sort — O(n²) average, O(n) best

Build a sorted portion one element at a time. Insert each new element into its correct position in the sorted portion.

```python
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and arr[j] > key:
            arr[j+1] = arr[j]    # shift right
            j -= 1
        arr[j+1] = key           # insert in correct position
    return arr

# Best: O(n) — already sorted
# Average/Worst: O(n²)
# Space: O(1) — in-place
# Stable: Yes
# Best for: nearly sorted small arrays. Used as final step in Timsort.
```

## Merge Sort — O(n log n) ⭐⭐⭐⭐⭐

**Divide and Conquer:** Divide array in half, recursively sort each half, merge sorted halves.

```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr

    mid = len(arr) // 2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])

    return merge(left, right)

def merge(left, right):
    result = []
    i = j = 0

    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1

    result.extend(left[i:])
    result.extend(right[j:])
    return result

# Always O(n log n) — best, average, worst
# Space: O(n) — not in-place
# Stable: Yes
# Best for: large datasets, linked lists, external sorting
```

**Recursion tree for n=8:**
```
        [8 elements]
       /             \
  [4 elements]   [4 elements]
  /       \       /       \
[2][2]   [2][2] [2][2]   [2][2]
/ \ / \  / \ / \ ...
[1][1][1][1]...

Depth = log₂(8) = 3 levels
Each level does O(n) work total
Total: O(n log n)
```

## Quick Sort — O(n log n) average ⭐⭐⭐⭐⭐

**Divide and Conquer:** Choose a pivot, partition array so all elements less than pivot are left, greater are right, then recursively sort both halves.

```python
def quick_sort(arr, low=0, high=None):
    if high is None:
        high = len(arr) - 1
    if low < high:
        pivot_idx = partition(arr, low, high)
        quick_sort(arr, low, pivot_idx - 1)
        quick_sort(arr, pivot_idx + 1, high)
    return arr

def partition(arr, low, high):
    pivot = arr[high]    # choose last element as pivot
    i = low - 1          # pointer for smaller elements

    for j in range(low, high):
        if arr[j] <= pivot:
            i += 1
            arr[i], arr[j] = arr[j], arr[i]

    arr[i+1], arr[high] = arr[high], arr[i+1]
    return i + 1

# Best/Average: O(n log n)
# Worst: O(n²) — when array is already sorted and pivot is always min/max
# Space: O(log n) — recursion stack
# Stable: No
# Best for: general purpose, cache-friendly, usually fastest in practice
```

## When to Use Which Sort?

```
Small array (n < 50):              Insertion Sort
Nearly sorted data:                Insertion Sort
Need stable sort + guaranteed O(n log n): Merge Sort
General purpose (most cases):     Quick Sort
Need O(1) extra space:             Heap Sort
Integer keys with small range:    Counting Sort
Large range of integers:          Radix Sort
```

---
---

# 14. Searching Algorithms

## Linear Search — O(n)

Check every element until found. Works on any array (sorted or unsorted).

```python
def linear_search(arr, target):
    for i, val in enumerate(arr):
        if val == target:
            return i    # return index
    return -1           # not found
```

## Binary Search — O(log n) ⭐⭐⭐⭐⭐

Works ONLY on sorted arrays. Repeatedly halves the search space.

```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1

    while left <= right:
        mid = left + (right - left) // 2    # avoid overflow vs (left+right)//2

        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1    # target is in right half
        else:
            right = mid - 1   # target is in left half

    return -1    # not found

# Time: O(log n), Space: O(1)
```

**Why `mid = left + (right - left) // 2` instead of `(left + right) // 2`?**
In languages with fixed integer sizes (Java, C++), `left + right` can overflow if both are large. The form `left + (right - left) // 2` is always safe.

## Binary Search on Answer — The Powerful Variant ⭐⭐⭐⭐

Binary search doesn't just search arrays — it searches the **answer space** for optimization problems.

Pattern: "Find the minimum/maximum value X such that condition(X) is satisfied."

```python
# Template:
def binary_search_answer(lo, hi, condition):
    result = -1
    while lo <= hi:
        mid = lo + (hi - lo) // 2
        if condition(mid):
            result = mid
            hi = mid - 1    # or lo = mid + 1 depending on min/max
        else:
            lo = mid + 1    # or hi = mid - 1
    return result
```

## Find First and Last Position ⭐⭐⭐⭐
```python
def search_range(nums, target):
    def find_first(nums, target):
        left, right = 0, len(nums) - 1
        result = -1
        while left <= right:
            mid = (left + right) // 2
            if nums[mid] == target:
                result = mid
                right = mid - 1    # keep going left to find FIRST
            elif nums[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return result

    def find_last(nums, target):
        left, right = 0, len(nums) - 1
        result = -1
        while left <= right:
            mid = (left + right) // 2
            if nums[mid] == target:
                result = mid
                left = mid + 1    # keep going right to find LAST
            elif nums[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return result

    return [find_first(nums, target), find_last(nums, target)]
# Time: O(log n), Space: O(1)
```

## Search in Rotated Sorted Array ⭐⭐⭐⭐
```python
def search_rotated(nums, target):
    left, right = 0, len(nums) - 1

    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return mid

        # Check which half is sorted
        if nums[left] <= nums[mid]:      # left half is sorted
            if nums[left] <= target < nums[mid]:
                right = mid - 1
            else:
                left = mid + 1
        else:                             # right half is sorted
            if nums[mid] < target <= nums[right]:
                left = mid + 1
            else:
                right = mid - 1

    return -1
# Time: O(log n)
```

---
---

# 15. Recursion & Backtracking

## What Is Recursion?

Recursion is when a function calls itself to solve a smaller version of the same problem.

Every recursive function needs:
1. **Base case:** The condition that stops recursion (prevents infinite loop)
2. **Recursive case:** The call that moves toward the base case

```python
def factorial(n):
    if n == 0:       # base case
        return 1
    return n * factorial(n - 1)    # recursive case

# factorial(4) = 4 × factorial(3)
#              = 4 × 3 × factorial(2)
#              = 4 × 3 × 2 × factorial(1)
#              = 4 × 3 × 2 × 1 × factorial(0)
#              = 4 × 3 × 2 × 1 × 1 = 24
```

## The Recursion Tree

Visualizing recursion as a tree helps understand time complexity:

```python
def fibonacci(n):
    if n <= 1: return n
    return fibonacci(n-1) + fibonacci(n-2)

# Tree for fib(4):
#           fib(4)
#          /      \
#       fib(3)   fib(2)
#       /    \   /    \
#    fib(2) fib(1) fib(1) fib(0)
#    /    \
# fib(1) fib(0)
#
# Total calls ≈ 2ⁿ → O(2ⁿ)
```

## Memoization — Fix Overlapping Subproblems

```python
def fibonacci_memo(n, memo={}):
    if n in memo:
        return memo[n]
    if n <= 1:
        return n
    memo[n] = fibonacci_memo(n-1, memo) + fibonacci_memo(n-2, memo)
    return memo[n]
# O(2ⁿ) → O(n) with memoization!
```

## Backtracking — The Pattern ⭐⭐⭐⭐⭐

Backtracking explores all possibilities by:
1. Making a choice
2. Recursing to explore that choice
3. **Undoing the choice** (backtrack) and trying the next option

```
Template:
def backtrack(state, choices):
    if is_solution(state):
        add to results
        return

    for choice in choices:
        make_choice(choice)
        backtrack(new_state, remaining_choices)
        undo_choice(choice)    ← This is the backtrack step
```

### Generate All Subsets ⭐⭐⭐⭐
```python
def subsets(nums):
    result = []

    def backtrack(start, current):
        result.append(current[:])    # add a copy of current subset

        for i in range(start, len(nums)):
            current.append(nums[i])         # choose
            backtrack(i + 1, current)       # explore
            current.pop()                   # unchoose (backtrack)

    backtrack(0, [])
    return result

# nums = [1,2,3]
# Result: [[], [1], [1,2], [1,2,3], [1,3], [2], [2,3], [3]]
# Time: O(2ⁿ × n)
```

### Generate All Permutations ⭐⭐⭐⭐
```python
def permutations(nums):
    result = []

    def backtrack(current, remaining):
        if not remaining:
            result.append(current[:])
            return

        for i in range(len(remaining)):
            current.append(remaining[i])
            backtrack(current, remaining[:i] + remaining[i+1:])
            current.pop()

    backtrack([], nums)
    return result
# Time: O(n × n!)
```

### N-Queens ⭐⭐⭐
```python
def solve_n_queens(n):
    result = []
    queens = []    # queens[i] = column of queen in row i

    def is_valid(row, col):
        for r, c in enumerate(queens):
            if c == col or abs(r - row) == abs(c - col):
                return False
        return True

    def backtrack(row):
        if row == n:
            result.append(queens[:])
            return
        for col in range(n):
            if is_valid(row, col):
                queens.append(col)
                backtrack(row + 1)
                queens.pop()

    backtrack(0)
    return result
```

---
---

# 16. Dynamic Programming

## What Is Dynamic Programming?

Dynamic Programming (DP) solves problems by breaking them into **overlapping subproblems** and storing solutions to avoid recomputation.

**When to use DP:**
1. **Optimal substructure:** Optimal solution contains optimal solutions to subproblems
2. **Overlapping subproblems:** Same subproblems are solved multiple times

**Two approaches:**
- **Top-Down (Memoization):** Recursion + cache
- **Bottom-Up (Tabulation):** Iterative + table

## Classic DP Problems

### Fibonacci — The Hello World of DP ⭐⭐⭐⭐

```python
# Top-Down (Memoization)
def fib_memo(n, memo={}):
    if n in memo: return memo[n]
    if n <= 1: return n
    memo[n] = fib_memo(n-1, memo) + fib_memo(n-2, memo)
    return memo[n]

# Bottom-Up (Tabulation)
def fib_tab(n):
    if n <= 1: return n
    dp = [0] * (n + 1)
    dp[1] = 1
    for i in range(2, n + 1):
        dp[i] = dp[i-1] + dp[i-2]
    return dp[n]

# Space Optimized — O(1) space
def fib_opt(n):
    if n <= 1: return n
    a, b = 0, 1
    for _ in range(2, n + 1):
        a, b = b, a + b
    return b
```

### 0/1 Knapsack ⭐⭐⭐⭐⭐

```
Problem: Given items with weights and values, and a knapsack of capacity W,
find maximum value achievable without exceeding weight limit.
Each item: either take it (1) or leave it (0).
```

```python
def knapsack(weights, values, W):
    n = len(weights)
    # dp[i][w] = max value using first i items with capacity w
    dp = [[0] * (W + 1) for _ in range(n + 1)]

    for i in range(1, n + 1):
        for w in range(W + 1):
            # Don't take item i
            dp[i][w] = dp[i-1][w]
            # Take item i (if it fits)
            if weights[i-1] <= w:
                dp[i][w] = max(dp[i][w],
                               dp[i-1][w - weights[i-1]] + values[i-1])

    return dp[n][W]

# weights = [1, 3, 4, 5], values = [1, 4, 5, 7], W = 7
# Answer: 9 (take items with weights 3 and 4)
# Time: O(n × W), Space: O(n × W)
```

### Longest Common Subsequence (LCS) ⭐⭐⭐⭐⭐

```
LCS of "ABCBDAB" and "BDCAB" is "BCAB" (length 4)
A subsequence doesn't need to be contiguous.
```

```python
def lcs(text1, text2):
    m, n = len(text1), len(text2)
    # dp[i][j] = LCS length of text1[:i] and text2[:j]
    dp = [[0] * (n + 1) for _ in range(m + 1)]

    for i in range(1, m + 1):
        for j in range(1, n + 1):
            if text1[i-1] == text2[j-1]:
                dp[i][j] = dp[i-1][j-1] + 1
            else:
                dp[i][j] = max(dp[i-1][j], dp[i][j-1])

    return dp[m][n]
# Time: O(m × n), Space: O(m × n)
```

### Coin Change ⭐⭐⭐⭐⭐

```
Given coin denominations and a target amount,
find minimum number of coins to make the amount.
```

```python
def coin_change(coins, amount):
    # dp[i] = minimum coins to make amount i
    dp = [float('inf')] * (amount + 1)
    dp[0] = 0    # 0 coins needed for amount 0

    for i in range(1, amount + 1):
        for coin in coins:
            if coin <= i:
                dp[i] = min(dp[i], dp[i - coin] + 1)

    return dp[amount] if dp[amount] != float('inf') else -1

# coins = [1, 5, 6, 9], amount = 11 → 2 (5 + 6)
# Time: O(amount × len(coins)), Space: O(amount)
```

### Longest Increasing Subsequence (LIS) ⭐⭐⭐⭐

```python
def lis(nums):
    n = len(nums)
    dp = [1] * n    # every element is LIS of length 1 by itself

    for i in range(1, n):
        for j in range(i):
            if nums[j] < nums[i]:
                dp[i] = max(dp[i], dp[j] + 1)

    return max(dp)
# nums = [10, 9, 2, 5, 3, 7, 101, 18]
# LIS = [2, 5, 7, 101] or [2, 3, 7, 18] → length 4
# Time: O(n²), Space: O(n)
# Can be optimized to O(n log n) with binary search
```

### DP Thinking Framework

```
Step 1: Define dp[i] or dp[i][j] — what does it represent?
Step 2: Find the recurrence — how does dp[i] relate to smaller subproblems?
Step 3: Identify base cases
Step 4: Determine order of computation (usually i from 0 to n)
Step 5: Return dp[n] or dp[m][n]
```

---
---

# 17. Greedy Algorithms

## What Is a Greedy Algorithm?

A greedy algorithm makes the **locally optimal choice** at each step, hoping to reach the globally optimal solution.

**Greedy works when:** Local optimum leads to global optimum (the greedy choice property).
**Greedy fails when:** A locally good choice blocks a globally better solution (need DP instead).

## Activity Selection Problem ⭐⭐⭐⭐

```
Given n activities with start and end times, select maximum
number of non-overlapping activities.

Greedy choice: Always pick the activity that finishes earliest.
```

```python
def activity_selection(start, end):
    n = len(start)
    # Sort by end time
    activities = sorted(zip(start, end), key=lambda x: x[1])

    selected = [activities[0]]
    last_end = activities[0][1]

    for i in range(1, n):
        if activities[i][0] >= last_end:    # starts after last ends
            selected.append(activities[i])
            last_end = activities[i][1]

    return selected
# Time: O(n log n) for sort, O(n) for selection
```

## Fractional Knapsack ⭐⭐⭐

Unlike 0/1 Knapsack (DP), fractional knapsack allows taking fractions of items.

```python
def fractional_knapsack(weights, values, W):
    # Sort by value/weight ratio descending
    items = sorted(zip(weights, values), key=lambda x: x[1]/x[0], reverse=True)

    total_value = 0
    remaining = W

    for weight, value in items:
        if remaining >= weight:
            total_value += value
            remaining -= weight
        else:
            total_value += value * (remaining / weight)    # take fraction
            break

    return total_value
```

## Jump Game ⭐⭐⭐⭐

```
Given array where arr[i] = max jumps from position i,
can you reach the last index?
```

```python
def can_jump(nums):
    max_reach = 0

    for i, jump in enumerate(nums):
        if i > max_reach:
            return False    # can't reach this position
        max_reach = max(max_reach, i + jump)

    return True
# Greedy: track the furthest position reachable at each step
# Time: O(n), Space: O(1)
```

---
---

# 18. Divide and Conquer

## The Strategy

Divide and Conquer works in three steps:
1. **Divide:** Split problem into smaller subproblems
2. **Conquer:** Solve subproblems recursively
3. **Combine:** Merge solutions of subproblems

**Examples:** Merge Sort, Quick Sort, Binary Search, Fast Power.

## Fast Power (Binary Exponentiation) ⭐⭐⭐

```python
def fast_power(base, exp):
    if exp == 0:
        return 1
    if exp % 2 == 0:
        half = fast_power(base, exp // 2)
        return half * half
    else:
        return base * fast_power(base, exp - 1)

# Normal: 2^10 = 2×2×2×...×2 → 10 multiplications → O(n)
# Fast: 2^10 = (2^5)² = ((2^2)²×2)² → 4 multiplications → O(log n)
```

## Maximum Subarray (Divide and Conquer approach)

```python
def max_subarray_dc(arr, left, right):
    if left == right:
        return arr[left]

    mid = (left + right) // 2

    # Max subarray in left half
    left_max = max_subarray_dc(arr, left, mid)
    # Max subarray in right half
    right_max = max_subarray_dc(arr, mid+1, right)
    # Max subarray crossing the midpoint
    cross_max = max_crossing(arr, left, mid, right)

    return max(left_max, right_max, cross_max)

def max_crossing(arr, left, mid, right):
    left_sum = float('-inf')
    total = 0
    for i in range(mid, left-1, -1):
        total += arr[i]
        left_sum = max(left_sum, total)

    right_sum = float('-inf')
    total = 0
    for i in range(mid+1, right+1):
        total += arr[i]
        right_sum = max(right_sum, total)

    return left_sum + right_sum
# Time: O(n log n) — compare with Kadane's O(n)
```

---
---

# 19. Two Pointers & Sliding Window

## Two Pointers Pattern

Use two pointers to traverse an array or linked list — reduces O(n²) brute force to O(n).

### Pair Sum in Sorted Array ⭐⭐⭐⭐⭐
```python
def two_sum_sorted(arr, target):
    left, right = 0, len(arr) - 1

    while left < right:
        current_sum = arr[left] + arr[right]
        if current_sum == target:
            return [left, right]
        elif current_sum < target:
            left += 1     # need larger sum → move left pointer right
        else:
            right -= 1    # need smaller sum → move right pointer left

    return []
# Time: O(n), Space: O(1)
```

### Remove Duplicates from Sorted Array ⭐⭐⭐⭐
```python
def remove_duplicates(nums):
    if not nums:
        return 0
    slow = 0
    for fast in range(1, len(nums)):
        if nums[fast] != nums[slow]:
            slow += 1
            nums[slow] = nums[fast]
    return slow + 1
# Time: O(n), Space: O(1)
```

### Container With Most Water ⭐⭐⭐⭐
```python
def max_area(height):
    left, right = 0, len(height) - 1
    max_water = 0

    while left < right:
        water = min(height[left], height[right]) * (right - left)
        max_water = max(max_water, water)

        if height[left] < height[right]:
            left += 1     # move the shorter side to find better
        else:
            right -= 1

    return max_water
# Time: O(n), Space: O(1)
```

## Sliding Window Pattern ⭐⭐⭐⭐⭐

A window that slides over the data. Maintains a running state to avoid recomputing from scratch.

### Fixed Size Window — Maximum Sum Subarray of Size K
```python
def max_sum_subarray(arr, k):
    window_sum = sum(arr[:k])    # first window
    max_sum = window_sum

    for i in range(k, len(arr)):
        window_sum += arr[i] - arr[i-k]    # add new, remove old
        max_sum = max(max_sum, window_sum)

    return max_sum
# Time: O(n), Space: O(1)
```

### Variable Size Window — Longest Subarray with Sum ≤ K
```python
def longest_subarray_sum(arr, k):
    left = 0
    current_sum = 0
    max_len = 0

    for right in range(len(arr)):
        current_sum += arr[right]           # expand window

        while current_sum > k:              # shrink window if constraint violated
            current_sum -= arr[left]
            left += 1

        max_len = max(max_len, right - left + 1)

    return max_len
# Time: O(n), Space: O(1)
```

---
---

# 20. Advanced Trees

## AVL Tree (Balanced BST)

An AVL tree is a self-balancing BST where the height difference between left and right subtrees (balance factor) is at most 1 for every node.

**Why needed:** Regular BST degenerates to O(n) if inputs are sorted. AVL guarantees O(log n).

**Balance factor:** height(left) - height(right) ∈ {-1, 0, 1}

When balance factor becomes ±2, **rotations** restore balance:
- Left rotation, Right rotation, Left-Right rotation, Right-Left rotation

**Operations:** O(log n) for search, insert, delete — guaranteed.

## Trie (Prefix Tree) ⭐⭐⭐⭐

A tree where each node represents a character. The path from root to a node spells a prefix.

```
Words: ["cat", "car", "card", "care", "bat"]

        root
       /    \
      c      b
      |      |
      a      a
     / \     |
    t   r    t
       / \
      d   e
```

```python
class TrieNode:
    def __init__(self):
        self.children = {}
        self.is_end = False

class Trie:
    def __init__(self):
        self.root = TrieNode()

    def insert(self, word):
        node = self.root
        for char in word:
            if char not in node.children:
                node.children[char] = TrieNode()
            node = node.children[char]
        node.is_end = True

    def search(self, word):
        node = self.root
        for char in word:
            if char not in node.children:
                return False
            node = node.children[char]
        return node.is_end

    def starts_with(self, prefix):
        node = self.root
        for char in prefix:
            if char not in node.children:
                return False
            node = node.children[char]
        return True

# Time per operation: O(m) where m = word length
# Space: O(n × m) total for all words
# Use for: autocomplete, spell check, IP routing, word search
```

## Segment Tree (Concept)

A segment tree is used for range queries (sum, min, max) and point updates on arrays.

```
Array: [1, 3, 5, 7, 9, 11]

         [36]           ← sum of all
        /      \
     [9]        [27]    ← sum of first half, second half
    /   \      /   \
  [4]  [5]  [16]  [11]  ← sum of quarters
  / \ / \   / \
 [1][3][5][7][9][11]    ← leaves = original array

Range sum query [1,4]: 3+5+7+9 = 24 → O(log n)
Point update: change arr[2] = 10 → update O(log n)
```

Build: O(n) | Query: O(log n) | Update: O(log n)

---
---

# 21. Advanced Graphs

## Dijkstra's Algorithm — Shortest Path (Non-negative Weights) ⭐⭐⭐⭐⭐

Find the shortest path from a source to all other vertices in a weighted graph with non-negative weights.

```python
import heapq

def dijkstra(graph, start):
    # graph = {node: [(neighbor, weight), ...]}
    distances = {node: float('inf') for node in graph}
    distances[start] = 0
    heap = [(0, start)]    # (distance, node)

    while heap:
        dist, node = heapq.heappop(heap)

        if dist > distances[node]:    # outdated entry
            continue

        for neighbor, weight in graph[node]:
            new_dist = dist + weight
            if new_dist < distances[neighbor]:
                distances[neighbor] = new_dist
                heapq.heappush(heap, (new_dist, neighbor))

    return distances

# Time: O((V + E) log V) with min-heap
# Does NOT work with negative weights!
```

## Bellman-Ford Algorithm — Handles Negative Weights

Relax all edges V-1 times. Detect negative cycles on the Vth iteration.

```python
def bellman_ford(edges, n, start):
    # edges = [(u, v, weight), ...]
    dist = [float('inf')] * n
    dist[start] = 0

    for _ in range(n - 1):    # relax V-1 times
        for u, v, w in edges:
            if dist[u] != float('inf') and dist[u] + w < dist[v]:
                dist[v] = dist[u] + w

    # Check for negative cycles
    for u, v, w in edges:
        if dist[u] + w < dist[v]:
            return None    # negative cycle detected

    return dist
# Time: O(V × E), Space: O(V)
```

## Topological Sort — For DAGs ⭐⭐⭐⭐

Linear ordering of vertices such that for every directed edge u→v, u comes before v. Only possible in a DAG (no cycles).

```python
from collections import deque

def topological_sort_bfs(graph, in_degree, n):
    # Kahn's Algorithm (BFS-based)
    queue = deque([i for i in range(n) if in_degree[i] == 0])
    result = []

    while queue:
        node = queue.popleft()
        result.append(node)

        for neighbor in graph[node]:
            in_degree[neighbor] -= 1
            if in_degree[neighbor] == 0:
                queue.append(neighbor)

    return result if len(result) == n else []    # empty if cycle exists
# Time: O(V + E)
# Use: Task scheduling, build systems, course prerequisites
```

## Union-Find (Disjoint Set Union) ⭐⭐⭐⭐

Efficiently track which elements belong to the same set. Union two sets. Find which set an element belongs to.

```python
class UnionFind:
    def __init__(self, n):
        self.parent = list(range(n))
        self.rank = [0] * n

    def find(self, x):
        if self.parent[x] != x:
            self.parent[x] = self.find(self.parent[x])    # path compression
        return self.parent[x]

    def union(self, x, y):
        px, py = self.find(x), self.find(y)
        if px == py:
            return False    # already in same set
        # Union by rank
        if self.rank[px] < self.rank[py]:
            px, py = py, px
        self.parent[py] = px
        if self.rank[px] == self.rank[py]:
            self.rank[px] += 1
        return True

    def connected(self, x, y):
        return self.find(x) == self.find(y)

# Find: O(α(n)) ≈ O(1) amortized with path compression
# Union: O(α(n)) ≈ O(1) amortized
# Use: Connected components, cycle detection, Kruskal's MST
```

## Minimum Spanning Tree — Kruskal's Algorithm ⭐⭐⭐

Find the subset of edges that connects all vertices with minimum total weight.

```python
def kruskal(n, edges):
    # edges = [(weight, u, v)]
    edges.sort()    # sort by weight
    uf = UnionFind(n)
    mst_weight = 0
    mst_edges = []

    for weight, u, v in edges:
        if uf.union(u, v):    # if not already connected
            mst_weight += weight
            mst_edges.append((u, v, weight))

    return mst_weight, mst_edges
# Time: O(E log E) for sorting
```

---
---

# 22. Bit Manipulation

## Why Bit Manipulation?

Operations on individual bits are extremely fast (single CPU instruction). Many elegant solutions exist using bit operations.

## Bitwise Operators

```python
a = 0b1010    # 10 in decimal
b = 0b1100    # 12 in decimal

a & b   # AND:  0b1000 = 8  (1 where BOTH are 1)
a | b   # OR:   0b1110 = 14 (1 where EITHER is 1)
a ^ b   # XOR:  0b0110 = 6  (1 where they DIFFER)
~a      # NOT:  -11 (flips all bits, including sign)
a << 1  # Left shift:  0b10100 = 20  (multiply by 2)
a >> 1  # Right shift: 0b0101 = 5    (divide by 2)
```

## Essential Bit Tricks ⭐⭐⭐⭐

```python
# Check if number is even
is_even = (n & 1) == 0

# Check if bit i is set
is_set = (n >> i) & 1

# Set bit i
n |= (1 << i)

# Clear bit i
n &= ~(1 << i)

# Toggle bit i
n ^= (1 << i)

# Remove lowest set bit
n &= (n - 1)        # Use: count number of 1 bits

# Get lowest set bit
lowest = n & (-n)   # or n & (~n + 1)

# Check if power of 2
is_power_of_2 = n > 0 and (n & (n-1)) == 0

# Count set bits (Brian Kernighan's algorithm)
def count_bits(n):
    count = 0
    while n:
        n &= n - 1    # removes lowest set bit each time
        count += 1
    return count
```

## XOR Tricks ⭐⭐⭐⭐

**XOR properties:**
- a ^ a = 0 (any number XOR itself = 0)
- a ^ 0 = a (any number XOR 0 = itself)
- XOR is commutative and associative

```python
# Find single number (all others appear twice) ⭐⭐⭐⭐⭐
def single_number(nums):
    result = 0
    for n in nums:
        result ^= n
    return result
# [4, 1, 2, 1, 2] → 4 ^ 1 ^ 2 ^ 1 ^ 2 = 4 ^ 0 ^ 0 = 4
# Time: O(n), Space: O(1)

# Swap without temp variable
a ^= b
b ^= a
a ^= b
```

---
---

# 23. Mathematical Algorithms

## GCD — Euclidean Algorithm ⭐⭐⭐

```python
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

# gcd(48, 18):
# 48 % 18 = 12 → gcd(18, 12)
# 18 % 12 = 6  → gcd(12, 6)
# 12 % 6 = 0   → gcd(6, 0) → return 6
# Time: O(log(min(a,b)))

def lcm(a, b):
    return a * b // gcd(a, b)
```

## Sieve of Eratosthenes — Find All Primes ⭐⭐⭐⭐

```python
def sieve(n):
    is_prime = [True] * (n + 1)
    is_prime[0] = is_prime[1] = False

    for i in range(2, int(n**0.5) + 1):
        if is_prime[i]:
            for j in range(i*i, n+1, i):    # mark multiples of i
                is_prime[j] = False

    return [i for i in range(2, n+1) if is_prime[i]]

# Time: O(n log log n), Space: O(n)
```

## Modular Arithmetic ⭐⭐⭐

Used heavily in competitive programming to prevent overflow.

```python
MOD = 10**9 + 7    # common modulus in competitive programming

# (a + b) % MOD = ((a % MOD) + (b % MOD)) % MOD
# (a × b) % MOD = ((a % MOD) × (b % MOD)) % MOD
# (a - b) % MOD = ((a % MOD) - (b % MOD) + MOD) % MOD

def power_mod(base, exp, mod):
    result = 1
    base %= mod
    while exp > 0:
        if exp & 1:
            result = result * base % mod
        base = base * base % mod
        exp >>= 1
    return result
# Time: O(log exp)
```

---
---

# 24. Learning Roadmap

## Phase 0 — Prerequisites (Week 1)

Before DSA, ensure you are comfortable with:
- A programming language — Python, Java, or C++ (Python recommended for clarity)
- Basic syntax: variables, loops, functions, conditionals, arrays
- Basic math: logarithms, basic probability, modular arithmetic

**One-week goal:** Write 20 simple programs from scratch without help.

---

## Phase 1 — Foundation (Weeks 2–4)

**Week 2:** Big O Analysis + Arrays + Strings
- Understand all Big O notations — calculate complexity for any code snippet
- Master array operations, prefix sum, Kadane's algorithm
- String immutability, sliding window for strings

**Week 3:** Linked Lists + Stacks + Queues
- Implement linked list from scratch
- Reverse linked list, detect cycle (Floyd's), find middle
- Valid parentheses (stack), next greater element
- BFS using queue

**Week 4:** Hashing + Binary Search
- HashMap patterns — two sum, frequency counting, anagram detection
- Binary search — standard + rotated array + search on answer space

**Milestone:** Solve 30 Easy problems on LeetCode from these topics.

---

## Phase 2 — Core Data Structures (Weeks 5–8)

**Week 5:** Trees
- Tree traversals (all 4) — code from memory
- Height, diameter, balanced check
- Level order BFS, path sum problems

**Week 6:** BST + Heaps
- BST insert, delete, validate
- Heap operations, kth largest/smallest
- Top K elements pattern

**Week 7:** Graphs
- Build graph from edge list
- BFS and DFS from scratch
- Number of islands, connected components, cycle detection

**Week 8:** Recursion + Backtracking
- Fibonacci with memoization
- Subsets, permutations, combination sum
- N-Queens conceptually

**Milestone:** Solve 50 Medium problems from these topics.

---

## Phase 3 — Algorithms (Weeks 9–12)

**Week 9:** Sorting + Dynamic Programming basics
- Implement merge sort and quick sort from scratch
- Fibonacci DP, coin change, climbing stairs
- 0/1 Knapsack

**Week 10:** DP — Classic Problems
- LCS, LIS, Edit distance
- DP on grids (unique paths, minimum path sum)

**Week 11:** Advanced Graphs
- Dijkstra's algorithm
- Topological sort
- Union-Find

**Week 12:** Two Pointers + Sliding Window + Bit Manipulation
- All patterns
- Practice 20 problems specifically on each pattern

**Milestone:** Solve 100+ total problems (30 Easy, 60 Medium, 10 Hard).

---

## Phase 4 — Interview Ready (Ongoing)

- Solve 1 Medium problem daily on LeetCode
- Time yourself — aim for 20-30 minutes per medium problem
- Practice explaining your approach out loud
- Take mock interviews (Pramp, Interviewing.io)
- Review problems you got wrong — understand the pattern

---
---

# 25. Common Mistakes to Avoid

**Mistake 1: Not Solving Problems on Paper First**
Always think before typing. Write the approach, trace through an example manually, THEN code. Jumping directly to code without thinking leads to wrong, inefficient solutions.

**Mistake 2: Not Analyzing Complexity Before Submitting**
Before submitting, state: "My solution is O(n log n) time and O(n) space." This habit prevents submitting O(n²) solutions that will TLE (Time Limit Exceeded) on large inputs.

**Mistake 3: Memorizing Solutions Instead of Understanding Patterns**
Memorizing the solution to "Two Sum" does nothing if you cannot recognize it in a different context. Learn the PATTERN — frequency map + complement check — not the code.

**Mistake 4: Skipping Easy Problems**
Many beginners skip Easy problems because they seem trivial. Easy problems build the foundation. Even at senior levels, interviewers test Easy + Medium combinations. Master every Easy.

**Mistake 5: Only Using One Approach**
When stuck, ask: Can I solve this with sorting? With hashing? With two pointers? With DP? Force yourself to think of multiple approaches even when you already have one.

**Mistake 6: Not Practicing with Time Limits**
In real interviews, you have 20–30 minutes per problem. Practice under time pressure. Use a timer. This is a separate skill from problem-solving.

**Mistake 7: Forgetting Edge Cases**
Always test your solution against: empty array, single element, all same elements, negative numbers, very large inputs, and the exact boundary conditions. State edge cases out loud in interviews.

**Mistake 8: Learning DSA Without Coding**
Reading solutions and thinking "I understand this" is very different from writing it from scratch. You must type every solution yourself. Understanding ≠ ability.

---
---

# 26. What to Do While and After Learning

## While Learning

**Code every single day.** Minimum 1 problem per day. Even 20 minutes of focused problem solving beats 3-hour weekend sessions.

**Implement every data structure from scratch at least once.** Write a linked list, a stack, a binary search tree, a hash map, a min-heap from scratch. This forces real understanding.

**Keep an error log.** When you get a problem wrong, write: what was your approach, what was wrong about it, what is the correct approach, and what pattern does the correct approach use.

**Discuss problems with peers.** Explaining a solution to someone else is the deepest test of understanding.

**Revisit problems.** After solving a problem, come back in 3 days and solve it again without looking at your previous solution. Spaced repetition builds long-term retention.

## After Learning

**Build a problem log on GitHub.** Document every problem solved — category, approach, complexity, key insight. This becomes a searchable personal reference.

**Aim for 150+ problems before major interviews.** Distribution: 40% Easy, 50% Medium, 10% Hard.

**Participate in LeetCode contests.** Weekly and biweekly contests test speed and accuracy under pressure. Even finishing 2/4 problems initially is progress.

**Study company-specific problems.** LeetCode has company tags. Google favorites: Trees, Arrays, DP. Amazon favorites: Trees, Arrays, Graphs. Study the last 6 months of problems for your target company.

---
---

# 27. Career Paths and Platforms

## Platforms for Practice

| Platform | Best For | Free? |
|----------|---------|-------|
| **LeetCode** | Primary practice — most interview-relevant | Free (premium optional) |
| **GeeksForGeeks** | Theory explanations + Indian company questions | Free |
| **HackerRank** | Company assessment simulation | Free |
| **Codeforces** | Competitive programming + speed | Free |
| **InterviewBit** | Structured interview prep by topic | Free |
| **Pramp** | Mock interviews with peers | Free |

## Company-Wise Focus

**Google / Meta / Microsoft:** Arrays, Trees, Graphs, DP, System Design (senior roles). Expect 4-5 rounds. Problems are medium-hard with multiple optimal solutions expected.

**Amazon:** Trees, Arrays, Graphs, OOP design. Leadership principles matter as much as code.

**Flipkart / Razorpay / Swiggy / Zomato:** Arrays, Strings, Hashing, Trees, DP. Medium difficulty. Move fast.

**TCS / Infosys / Wipro (service companies):** Basic DSA, mostly Easy-Medium. Aptitude + coding combined.

**Startups:** Practical problems, focus on code quality, less algorithmic puzzle focus.

---
---

# 28. Glossary

**Abstract Data Type (ADT):** A data type defined by behavior (operations) rather than implementation. Stack and Queue are ADTs.

**Adjacency List:** Graph representation using a list/dictionary of neighbors for each vertex.

**Adjacency Matrix:** Graph representation using a 2D array where matrix[i][j] = 1 if edge exists.

**Amortized Analysis:** Average cost per operation over a sequence of operations. Dynamic array append is O(1) amortized.

**Backtracking:** Algorithm that builds a solution incrementally and abandons partial solutions when they fail constraints.

**Balance Factor:** In AVL tree: height(left subtree) - height(right subtree). Must be in {-1, 0, 1}.

**Base Case:** The condition in a recursive function that stops further recursion.

**BFS (Breadth First Search):** Graph traversal visiting all nodes at current depth before going deeper. Uses a queue.

**Big O Notation:** Upper bound on algorithm's growth rate. Describes worst-case asymptotic behavior.

**BST (Binary Search Tree):** Binary tree where left children < node < right children.

**Complete Binary Tree:** All levels fully filled except possibly the last, which is filled left to right.

**DAG (Directed Acyclic Graph):** Directed graph with no cycles.

**DFS (Depth First Search):** Graph traversal exploring as far as possible along each branch before backtracking. Uses stack/recursion.

**Divide and Conquer:** Algorithm design strategy — divide into subproblems, solve recursively, combine.

**DP (Dynamic Programming):** Optimization technique for problems with overlapping subproblems and optimal substructure.

**Edge:** Connection between two vertices in a graph.

**Greedy Algorithm:** Makes the locally optimal choice at each step.

**Hash Collision:** Two different keys mapping to the same hash value.

**Hash Function:** Function mapping keys to array indices.

**Heap:** Complete binary tree satisfying heap property (min or max).

**In-degree:** Number of incoming edges to a vertex.

**Inorder Traversal:** Left → Root → Right. Gives sorted output for BST.

**Kadane's Algorithm:** O(n) algorithm for maximum subarray sum.

**LCS (Longest Common Subsequence):** Longest subsequence common to two sequences.

**LIS (Longest Increasing Subsequence):** Longest strictly increasing subsequence.

**Memoization:** Caching results of recursive calls to avoid recomputation.

**Min Heap:** Complete binary tree where every node ≤ its children. Root = minimum.

**MST (Minimum Spanning Tree):** Subset of edges connecting all vertices with minimum total weight.

**Node:** An element in a data structure containing data and pointers.

**Out-degree:** Number of outgoing edges from a vertex.

**Postorder Traversal:** Left → Right → Root.

**Prefix Sum:** Array where prefix[i] = sum of first i elements. Enables O(1) range sum queries.

**Preorder Traversal:** Root → Left → Right.

**Priority Queue:** Queue where dequeue always returns the highest-priority element.

**Recursion:** Function calling itself to solve smaller version of same problem.

**Segment Tree:** Tree data structure for range queries and point updates in O(log n).

**Sliding Window:** Technique maintaining a window of elements with a running state as it slides.

**Space Complexity:** Amount of extra memory an algorithm uses as function of input size.

**Stack:** LIFO (Last In First Out) data structure.

**Tail Recursion:** Recursive call is the last operation. Some languages optimize to iteration.

**Time Complexity:** How runtime grows as function of input size.

**Topological Sort:** Linear ordering of DAG vertices respecting edge directions.

**Traversal:** Visiting every node in a data structure exactly once.

**Trie:** Tree where paths from root spell out strings. Used for prefix operations.

**Two Pointers:** Technique using two indices to traverse array, reducing O(n²) to O(n).

**Union-Find:** Data structure tracking disjoint sets with near-O(1) union and find.

**Vertex:** A node in a graph.

**XOR:** Bitwise exclusive OR. Key properties: a^a=0, a^0=a.

---

> **Navigation:** [Back to Repository README](./README.md) | [Next: 02_DSA_Interview_Prep.md →](./02_DSA_Interview_Prep.md)

---

*File: `01_DSA_Masterguide.md` | Version 1.0 | 2026*
*Part of the DSA Repository*
*Language: Python (most readable). Concepts apply to Java, C++, and any language.*
