# 🎯 02 — DSA Interview & Internship Prep
### Only What Gets Asked | Patterns That Solve 80% of Problems | 2026 Edition

> **File:** `02_DSA_Interview_Prep.md`
> **Part of:** DSA Repository → [Back to README](./README.md)
> **Previous:** [01_DSA_Masterguide.md](./01_DSA_Masterguide.md) | **Next:** [03_DSA_Practice_Repository.md](./03_DSA_Practice_Repository.md)

---

## 🎯 What You Got (~90 Pages):

### ONLY What Actually Gets Asked in 2026:

✅ **What to Study vs Skip** — Saves 40% time by cutting irrelevant topics
✅ **Complexity Cheat Sheet** — Every DS + algorithm in one table
✅ **Arrays & Strings (15%)** — The most asked topic in every round
✅ **Linked Lists (10%)** — Reversal, cycle, merge — 3 patterns cover 90%
✅ **Stacks & Queues (8%)** — Monotonic stack is the hidden gem
✅ **Hashing (12%)** — Frequency maps solve half of all array problems
✅ **Trees & BST (15%)** — Traversals + recursion + path problems
✅ **Heaps (5%)** — K-th element pattern appears constantly
✅ **Graphs (10%)** — BFS/DFS templates that work everywhere
✅ **Sorting & Searching (8%)** — Binary search variants are heavily tested
✅ **Dynamic Programming (12%)** — Top 10 DP problems cover 80% of DP asked
✅ **50 Most Asked Interview Questions** — Detailed answers + approach
✅ **14 Must-Know Patterns** — Code templates for every major pattern
✅ **How to Approach ANY Coding Problem** — The 7-step framework
✅ **2-Week Study Plan** — Day-by-day with problem targets
✅ **Readiness Checklist + Rapid Review** — Know when you're ready

---

## 🔥 Key Features:

### 1. What to Skip (Save Time!):
❌ AVL rotations in detail (only concept level needed — never implement in interviews)
❌ Red-Black tree implementation (concept only)
❌ B-trees and B+ trees (only asked for DB systems courses, not DSA rounds)
❌ Splay trees and other exotic trees (not asked)
❌ Bellman-Ford algorithm code (Dijkstra covers 90% of graph interview questions)
❌ Floyd-Warshall implementation (only for competitive programming)
❌ Suffix trees/arrays (competitive programming only)
❌ Segment tree with lazy propagation (advanced competitive — not interviews)
❌ Number theory beyond GCD + primes + modular (not in typical interviews)
❌ Randomized algorithms (concept only)
❌ String matching algorithms (KMP, Rabin-Karp) — know concept, not implementation
❌ Amortized analysis proofs — know the result, not the formal proof

### 2. What to MASTER (Asked 80%+ of the time):
⭐⭐⭐⭐⭐ **Arrays + Two Pointers + Sliding Window** (40% of all problems!)
⭐⭐⭐⭐⭐ **HashMap/HashSet patterns** (solves 50% of array problems instantly!)
⭐⭐⭐⭐⭐ **Binary Search** (not just on arrays — on answer space!)
⭐⭐⭐⭐⭐ **Tree traversals + recursion** (every tree problem uses one of 3 patterns)
⭐⭐⭐⭐⭐ **BFS/DFS templates** (solve ALL graph problems with small modifications)
⭐⭐⭐⭐⭐ **Big O analysis** (asked in every single interview round)
⭐⭐⭐⭐ **Linked List — reversal + cycle + merge** (3 patterns cover 90% of LL problems)
⭐⭐⭐⭐ **Stack — valid parentheses + monotonic stack** (appears constantly)
⭐⭐⭐⭐ **Dynamic Programming — top 10 classics** (coin change, LCS, knapsack, LIS)
⭐⭐⭐⭐ **Merge sort + Quick sort** (understand deeply, not just memorize)
⭐⭐⭐ **Heap/Priority Queue** (K-th largest/smallest appears in every company)
⭐⭐⭐ **Backtracking** (subsets, permutations, combination sum)
⭐⭐⭐ **Topological Sort + Union Find** (graph-heavy companies)
⭐⭐ **Trie** (string-heavy problems, autocomplete scenarios)

---

## 📊 Coverage Breakdown:

### Section 1: Complexity Cheat Sheet
### Section 2: Arrays & Strings
### Section 3: Linked Lists
### Section 4: Stacks & Queues
### Section 5: Hashing
### Section 6: Trees & BST
### Section 7: Heaps
### Section 8: Graphs
### Section 9: Sorting & Searching
### Section 10: Dynamic Programming
### Section 11: 50 Most Asked Interview Questions
### Section 12: 14 Must-Know Patterns with Code Templates
### Section 13: How to Approach Any Coding Problem
### Section 14: Language-Specific Tips
### Section 15: 2-Week Study Plan
### Section 16: Readiness Checklist + Last-Day Rapid Review

---
---

# Section 1: Complexity Cheat Sheet ⚡

## Data Structure Operations

| Data Structure | Access | Search | Insert | Delete | Space |
|----------------|--------|--------|--------|--------|-------|
| Array (static) | **O(1)** | O(n) | O(n) | O(n) | O(n) |
| Dynamic Array | **O(1)** | O(n) | **O(1)*** | O(n) | O(n) |
| Singly Linked List | O(n) | O(n) | **O(1)†** | **O(1)†** | O(n) |
| Stack | O(n) | O(n) | **O(1)** | **O(1)** | O(n) |
| Queue | O(n) | O(n) | **O(1)** | **O(1)** | O(n) |
| Hash Table | O(1)* | **O(1)*** | **O(1)*** | **O(1)*** | O(n) |
| BST (balanced) | O(log n) | **O(log n)** | **O(log n)** | **O(log n)** | O(n) |
| BST (worst case) | O(n) | O(n) | O(n) | O(n) | O(n) |
| Min/Max Heap | O(n) | O(n) | **O(log n)** | **O(log n)** | O(n) |
| Heap (peek min/max) | — | **O(1)** | — | — | — |
| Trie | — | **O(m)** | **O(m)** | **O(m)** | O(n×m) |
| Graph BFS/DFS | — | **O(V+E)** | — | — | O(V) |

*amortized | †with pointer to node | m = string/word length

## Sorting Algorithms

| Algorithm | Best | Average | Worst | Space | Stable | Notes |
|-----------|------|---------|-------|-------|--------|-------|
| Bubble | O(n) | O(n²) | O(n²) | O(1) | ✅ | Only good for nearly sorted |
| Selection | O(n²) | O(n²) | O(n²) | O(1) | ❌ | Minimum swaps |
| Insertion | **O(n)** | O(n²) | O(n²) | O(1) | ✅ | Best for small/nearly sorted |
| Merge | O(n log n) | O(n log n) | **O(n log n)** | O(n) | ✅ | Guaranteed, good for linked lists |
| Quick | O(n log n) | O(n log n) | O(n²) | O(log n) | ❌ | Fastest in practice |
| Heap | O(n log n) | O(n log n) | O(n log n) | **O(1)** | ❌ | In-place + guaranteed |
| Counting | O(n+k) | O(n+k) | O(n+k) | O(k) | ✅ | Only for integers |
| Python sort() | O(n) | O(n log n) | O(n log n) | O(n) | ✅ | Timsort |

## Graph Algorithms

| Algorithm | Time | Space | Use Case |
|-----------|------|-------|---------|
| BFS | O(V+E) | O(V) | Shortest path (unweighted), level order |
| DFS | O(V+E) | O(V) | Cycle detection, paths, connected components |
| Dijkstra | O((V+E) log V) | O(V) | Shortest path (non-negative weights) |
| Bellman-Ford | O(V×E) | O(V) | Shortest path (negative weights) |
| Topological Sort | O(V+E) | O(V) | DAG ordering, task scheduling |
| Union-Find | O(α(n)) ≈ O(1) | O(V) | Connected components, cycle detection |
| Kruskal's MST | O(E log E) | O(V) | Minimum spanning tree |

## Big O Growth — Visual Reminder

```
n = 1000:
O(1)       =             1 op
O(log n)   =            10 ops
O(n)       =         1,000 ops
O(n log n) =        10,000 ops
O(n²)      =     1,000,000 ops  ← starts getting slow
O(2ⁿ)      = 10^301 ops        ← impossible
```

---
---

# Section 2: Arrays & Strings 🔢

## Must-Know Array Patterns ⭐⭐⭐⭐⭐

### Pattern 1 — Prefix Sum
```python
# Build once: O(n). Query any range sum: O(1)
def build_prefix(arr):
    prefix = [0] * (len(arr) + 1)
    for i, x in enumerate(arr):
        prefix[i+1] = prefix[i] + x
    return prefix

def range_sum(prefix, l, r):   # inclusive indices
    return prefix[r+1] - prefix[l]
```
**Trigger:** "subarray sum", "range sum", "sum between indices"

### Pattern 2 — Two Pointers on Sorted Array
```python
# Find pair summing to target in sorted array
left, right = 0, len(arr) - 1
while left < right:
    s = arr[left] + arr[right]
    if s == target: return [left, right]
    elif s < target: left += 1
    else: right -= 1
```
**Trigger:** "sorted array", "pair", "triplet", "remove duplicates in-place"

### Pattern 3 — Sliding Window (Fixed Size)
```python
# Max sum subarray of size k
window = sum(arr[:k])
max_sum = window
for i in range(k, len(arr)):
    window += arr[i] - arr[i-k]
    max_sum = max(max_sum, window)
```
**Trigger:** "subarray of size k", "window of length k"

### Pattern 4 — Sliding Window (Variable Size)
```python
# Longest subarray satisfying a condition
left = 0
state = {}   # or counter
for right in range(len(arr)):
    # Expand: add arr[right] to state
    while condition_violated(state):
        # Shrink: remove arr[left] from state
        left += 1
    max_len = max(max_len, right - left + 1)
```
**Trigger:** "longest subarray/substring", "minimum window"

### Pattern 5 — Kadane's (Maximum Subarray)
```python
max_sum = cur = arr[0]
for x in arr[1:]:
    cur = max(x, cur + x)
    max_sum = max(max_sum, cur)
```
**Trigger:** "maximum subarray sum", "largest sum contiguous"

## Must-Know String Techniques ⭐⭐⭐⭐⭐

```python
# Character frequency
from collections import Counter
freq = Counter(s)

# Check anagram
sorted(s1) == sorted(s2)            # O(n log n)
Counter(s1) == Counter(s2)          # O(n)

# Palindrome check (two pointers)
l, r = 0, len(s)-1
while l < r:
    if s[l] != s[r]: return False
    l += 1; r -= 1
return True

# Reverse a string
s[::-1]

# Join list to string (ALWAYS use join — not +=)
"".join(char_list)    # O(n) vs O(n²) with +=
```

---
---

# Section 3: Linked Lists 🔗

## The 3 Patterns That Cover 90% of LL Problems ⭐⭐⭐⭐⭐

### Pattern 1 — Reversal (Iterative)
```python
def reverse(head):
    prev, curr = None, head
    while curr:
        nxt = curr.next
        curr.next = prev
        prev = curr
        curr = nxt
    return prev    # new head
```
**Variants:** Reverse in groups of k, reverse between positions m and n

### Pattern 2 — Fast & Slow Pointers
```python
# Detect cycle
def has_cycle(head):
    slow = fast = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
        if slow == fast: return True
    return False

# Find middle (slow is at middle when fast reaches end)
def find_middle(head):
    slow = fast = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
    return slow
```
**Variants:** Find start of cycle, check if palindrome (reverse second half)

### Pattern 3 — Merge / Two-Pointer on Lists
```python
# Merge two sorted lists
def merge(l1, l2):
    dummy = ListNode(0)
    cur = dummy
    while l1 and l2:
        if l1.val <= l2.val:
            cur.next = l1; l1 = l1.next
        else:
            cur.next = l2; l2 = l2.next
        cur = cur.next
    cur.next = l1 or l2
    return dummy.next
```
**Variants:** Merge K sorted lists (use heap), remove nth from end

## Remove Nth Node From End ⭐⭐⭐⭐
```python
def remove_nth_from_end(head, n):
    dummy = ListNode(0, head)
    fast = slow = dummy
    for _ in range(n + 1):    # advance fast n+1 steps
        fast = fast.next
    while fast:
        fast = fast.next
        slow = slow.next
    slow.next = slow.next.next    # remove node
    return dummy.next
# One-pass, O(n) time, O(1) space
```

---
---

# Section 4: Stacks & Queues 📚

## Stack Patterns ⭐⭐⭐⭐⭐

### Valid Parentheses (Classic)
```python
def is_valid(s):
    stack = []
    pairs = {')':'(', '}':'{', ']':'['}
    for c in s:
        if c in '({[':
            stack.append(c)
        elif not stack or stack[-1] != pairs[c]:
            return False
        else:
            stack.pop()
    return not stack
```

### Monotonic Stack — Next Greater Element ⭐⭐⭐⭐
The most powerful and underrated stack pattern:
```python
def next_greater(arr):
    result = [-1] * len(arr)
    stack = []    # stores indices

    for i, val in enumerate(arr):
        # Pop elements smaller than current — current is their NGE
        while stack and arr[stack[-1]] < val:
            result[stack.pop()] = val
        stack.append(i)

    return result
# arr = [2, 1, 5, 3, 7]
# NGE  = [5, 5, 7, 7, -1]
# Time: O(n) — each element pushed/popped once
```

**Monotonic stack variants:**
- Next Greater Element → maintain increasing stack (pop when smaller)
- Previous Greater Element → same stack, process differently
- Largest Rectangle in Histogram → maintain increasing stack of heights
- Daily Temperatures → find next warmer day

### Largest Rectangle in Histogram ⭐⭐⭐⭐
```python
def largest_rectangle(heights):
    stack = []    # stack of indices with increasing heights
    max_area = 0
    heights.append(0)    # sentinel

    for i, h in enumerate(heights):
        while stack and heights[stack[-1]] > h:
            height = heights[stack.pop()]
            width = i if not stack else i - stack[-1] - 1
            max_area = max(max_area, height * width)
        stack.append(i)

    return max_area
# Time: O(n), Space: O(n)
```

## Queue / BFS Pattern ⭐⭐⭐⭐⭐
```python
from collections import deque

def bfs_template(start, target, graph):
    queue = deque([start])
    visited = {start}
    steps = 0

    while queue:
        for _ in range(len(queue)):    # process level by level
            node = queue.popleft()
            if node == target:
                return steps
            for neighbor in graph[node]:
                if neighbor not in visited:
                    visited.add(neighbor)
                    queue.append(neighbor)
        steps += 1

    return -1    # not reachable
```

---
---

# Section 5: Hashing 🗺️

## The HashMap Mindset ⭐⭐⭐⭐⭐

**Rule:** When you need O(1) lookup → think HashMap or HashSet first.

**The 3 HashMap patterns that appear in 50%+ of array problems:**

### Pattern 1 — Complement / Two Sum
```python
# "Find two numbers summing to target"
seen = {}
for i, num in enumerate(nums):
    if target - num in seen:
        return [seen[target - num], i]
    seen[num] = i
# Time: O(n). This pattern generalizes to: "find something paired with current"
```

### Pattern 2 — Frequency Count
```python
from collections import Counter, defaultdict

# Count occurrences
freq = Counter(arr)

# Find most common k elements
top_k = freq.most_common(k)

# Find elements appearing exactly once
singles = [x for x, c in freq.items() if c == 1]
```
**Trigger:** "frequency", "appears k times", "most common", "unique element"

### Pattern 3 — Grouping by Key
```python
from collections import defaultdict

# Group anagrams
groups = defaultdict(list)
for word in words:
    key = tuple(sorted(word))    # canonical form
    groups[key].append(word)

# Subarray sum equals k → count prefix sums
prefix_count = defaultdict(int)
prefix_count[0] = 1
total = count = 0
for num in nums:
    total += num
    count += prefix_count[total - k]
    prefix_count[total] += 1
```

### HashSet for O(1) Existence Check
```python
# Longest consecutive sequence — O(n) using set
nums_set = set(nums)
max_len = 0

for num in nums_set:
    if num - 1 not in nums_set:    # start of a sequence
        cur, length = num, 1
        while cur + 1 in nums_set:
            cur += 1; length += 1
        max_len = max(max_len, length)
```

---
---

# Section 6: Trees & BST 🌳

## The 3 Tree Recursion Patterns ⭐⭐⭐⭐⭐

Almost every tree problem uses one of these three patterns:

### Pattern 1 — Top-Down (Pass information down)
```python
def solve(node, state_from_parent):
    if not node: return base_case
    # use state_from_parent
    left = solve(node.left, new_state)
    right = solve(node.right, new_state)
    return combine(left, right)
```
Example: Path sum, max depth, count nodes

### Pattern 2 — Bottom-Up (Return information up)
```python
def solve(node):
    if not node: return base_value
    left_result = solve(node.left)
    right_result = solve(node.right)
    # compute current result from children
    return result_using(left_result, right_result, node.val)
```
Example: Height, diameter, balanced check

### Pattern 3 — Global Variable Pattern
```python
self.result = 0    # or float('-inf') etc.

def dfs(node):
    if not node: return 0
    left = dfs(node.left)
    right = dfs(node.right)
    # update global result using local info
    self.result = max(self.result, left + right)
    return max(left, right)    # return up
```
Example: Diameter, max path sum, any "update global, return local" problem

## Key Tree Operations ⭐⭐⭐⭐⭐

```python
# All traversals
def inorder(node, result=[]):
    if node:
        inorder(node.left, result)
        result.append(node.val)    # Left → ROOT → Right
        inorder(node.right, result)

def preorder(node, result=[]):
    if node:
        result.append(node.val)    # ROOT → Left → Right
        preorder(node.left, result)
        preorder(node.right, result)

def postorder(node, result=[]):
    if node:
        postorder(node.left, result)
        postorder(node.right, result)
        result.append(node.val)    # Left → Right → ROOT

# Inorder of BST = sorted array → validate BST

# LCA (Lowest Common Ancestor) ⭐⭐⭐⭐⭐
def lca(root, p, q):
    if not root or root == p or root == q:
        return root
    left = lca(root.left, p, q)
    right = lca(root.right, p, q)
    if left and right: return root    # p and q on different sides
    return left or right

# Max Path Sum ⭐⭐⭐⭐
def max_path_sum(root):
    self_max = [float('-inf')]
    def dfs(node):
        if not node: return 0
        left = max(dfs(node.left), 0)    # ignore negative paths
        right = max(dfs(node.right), 0)
        self_max[0] = max(self_max[0], node.val + left + right)
        return node.val + max(left, right)
    dfs(root)
    return self_max[0]
```

## BST Key Facts ⭐⭐⭐⭐
```python
# Inorder gives sorted array
# Kth smallest → inorder traverse, count k steps
# Validate BST → pass min/max bounds
# Convert sorted array to balanced BST → binary split (mid as root)

def sorted_array_to_bst(nums):
    if not nums: return None
    mid = len(nums) // 2
    root = TreeNode(nums[mid])
    root.left = sorted_array_to_bst(nums[:mid])
    root.right = sorted_array_to_bst(nums[mid+1:])
    return root
```

---
---

# Section 7: Heaps ⛰️

## The K-th Element Pattern ⭐⭐⭐⭐⭐

Heap is the go-to for any "K largest", "K smallest", "K most frequent" problem:

```python
import heapq

# K largest elements — use MIN-heap of size K
def k_largest(nums, k):
    heap = nums[:k]
    heapq.heapify(heap)
    for num in nums[k:]:
        if num > heap[0]:
            heapq.heapreplace(heap, num)
    return sorted(heap, reverse=True)
# Time: O(n log k), Space: O(k)

# K smallest elements — use MAX-heap (negate values)
def k_smallest(nums, k):
    heap = [-x for x in nums[:k]]
    heapq.heapify(heap)
    for num in nums[k:]:
        if num < -heap[0]:
            heapq.heapreplace(heap, -num)
    return sorted([-x for x in heap])

# K most frequent elements
from collections import Counter
def top_k_frequent(nums, k):
    freq = Counter(nums)
    return heapq.nlargest(k, freq.keys(), key=freq.get)
# Time: O(n log k)
```

## Median From Data Stream ⭐⭐⭐⭐
```python
# Maintain two heaps: max-heap for lower half, min-heap for upper half
import heapq

class MedianFinder:
    def __init__(self):
        self.small = []   # max-heap (negate): lower half
        self.large = []   # min-heap: upper half

    def add_num(self, num):
        heapq.heappush(self.small, -num)
        # Balance: move max of small to large if needed
        if self.small and self.large and -self.small[0] > self.large[0]:
            heapq.heappush(self.large, -heapq.heappop(self.small))
        # Keep sizes balanced (small can be 1 larger)
        if len(self.small) > len(self.large) + 1:
            heapq.heappush(self.large, -heapq.heappop(self.small))
        if len(self.large) > len(self.small):
            heapq.heappush(self.small, -heapq.heappop(self.large))

    def find_median(self):
        if len(self.small) > len(self.large):
            return -self.small[0]
        return (-self.small[0] + self.large[0]) / 2
```

---
---

# Section 8: Graphs 🕸️

## The BFS Template (Shortest Path) ⭐⭐⭐⭐⭐
```python
from collections import deque

def bfs(graph, start):
    visited = {start}
    queue = deque([(start, 0)])    # (node, distance)
    while queue:
        node, dist = queue.popleft()
        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append((neighbor, dist + 1))
    return dist    # distance to last node reached
```

## The DFS Template (Connected Components, Paths) ⭐⭐⭐⭐⭐
```python
def dfs(graph, node, visited):
    visited.add(node)
    for neighbor in graph[node]:
        if neighbor not in visited:
            dfs(graph, neighbor, visited)

# Count connected components
def count_components(n, edges):
    graph = defaultdict(list)
    for u, v in edges:
        graph[u].append(v)
        graph[v].append(u)
    visited = set()
    count = 0
    for node in range(n):
        if node not in visited:
            dfs(graph, node, visited)
            count += 1
    return count
```

## Grid BFS/DFS (Very Common) ⭐⭐⭐⭐⭐
```python
# DFS on a grid — Number of Islands pattern
def num_islands(grid):
    rows, cols = len(grid), len(grid[0])
    count = 0

    def dfs(r, c):
        if r < 0 or r >= rows or c < 0 or c >= cols or grid[r][c] != '1':
            return
        grid[r][c] = '#'    # mark visited (in-place)
        for dr, dc in [(0,1),(0,-1),(1,0),(-1,0)]:
            dfs(r + dr, c + dc)

    for r in range(rows):
        for c in range(cols):
            if grid[r][c] == '1':
                dfs(r, c)
                count += 1
    return count
```

## Topological Sort — Course Schedule ⭐⭐⭐⭐
```python
from collections import deque, defaultdict

def can_finish(n, prerequisites):
    graph = defaultdict(list)
    in_degree = [0] * n

    for course, prereq in prerequisites:
        graph[prereq].append(course)
        in_degree[course] += 1

    queue = deque([i for i in range(n) if in_degree[i] == 0])
    completed = 0

    while queue:
        course = queue.popleft()
        completed += 1
        for next_course in graph[course]:
            in_degree[next_course] -= 1
            if in_degree[next_course] == 0:
                queue.append(next_course)

    return completed == n    # True if no cycle
```

---
---

# Section 9: Sorting & Searching 🔍

## Binary Search — 3 Templates ⭐⭐⭐⭐⭐

### Template 1 — Exact Match
```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    while left <= right:
        mid = left + (right - left) // 2
        if arr[mid] == target: return mid
        elif arr[mid] < target: left = mid + 1
        else: right = mid - 1
    return -1
```

### Template 2 — Find First True (Lower Bound)
```python
# Find leftmost position where condition is True
def lower_bound(arr, target):
    left, right = 0, len(arr)
    while left < right:
        mid = (left + right) // 2
        if arr[mid] >= target:    # condition
            right = mid
        else:
            left = mid + 1
    return left    # first position where arr[pos] >= target
```

### Template 3 — Binary Search on Answer Space ⭐⭐⭐⭐⭐
```python
# "Find minimum X such that condition(X) is satisfied"
def binary_search_answer(lo, hi, condition):
    while lo < hi:
        mid = (lo + hi) // 2
        if condition(mid):
            hi = mid        # try smaller
        else:
            lo = mid + 1    # too small, try larger
    return lo

# Example: Minimum speed to eat all bananas in H hours
def min_eating_speed(piles, H):
    import math
    def can_eat(k):
        return sum(math.ceil(p/k) for p in piles) <= H
    lo, hi = 1, max(piles)
    return binary_search_answer(lo, hi, can_eat)
```

## When to Use Which Sort ⭐⭐⭐⭐

```python
# In Python — always use built-in sort (Timsort — O(n log n), stable)
arr.sort()                      # in-place
sorted_arr = sorted(arr)        # new array

# Sort with custom key
arr.sort(key=lambda x: x[1])   # sort by second element
arr.sort(key=lambda x: (-x[1], x[0]))  # descending by [1], then asc by [0]

# When to know the algorithm for interview:
# "Which sort is stable?" → Merge, Insertion, Bubble, Counting
# "Which is fastest in practice?" → Quick Sort
# "Which guarantees O(n log n) worst case?" → Merge Sort, Heap Sort
# "Small nearly-sorted array?" → Insertion Sort
```

---
---

# Section 10: Dynamic Programming 🧩

## The DP Decision Framework ⭐⭐⭐⭐⭐

```
Step 1: Can I recognize this as DP?
        → Optimization problem (min/max/count)
        → Choices at each step
        → Overlapping subproblems (same computation repeated)

Step 2: Define the state
        → What does dp[i] or dp[i][j] represent?
        → Be precise: "dp[i] = minimum coins to make amount i"

Step 3: Write the recurrence
        → How does dp[i] depend on dp[i-1], dp[i-2], etc.?

Step 4: Set base cases
        → dp[0] = ? (usually 0 or 1)

Step 5: Determine computation order
        → Usually left to right (i from 0 to n)

Step 6: Return dp[n] (or max/min of dp array)
```

## Top 10 DP Problems — Must Master All ⭐⭐⭐⭐⭐

### 1. Climbing Stairs (Base DP)
```python
def climb_stairs(n):
    if n <= 2: return n
    dp = [0] * (n + 1)
    dp[1] = 1; dp[2] = 2
    for i in range(3, n + 1):
        dp[i] = dp[i-1] + dp[i-2]
    return dp[n]
# Same as Fibonacci. Time: O(n), Space: O(n) → O(1) with variables
```

### 2. Coin Change (Unbounded Knapsack variant)
```python
def coin_change(coins, amount):
    dp = [float('inf')] * (amount + 1)
    dp[0] = 0
    for i in range(1, amount + 1):
        for coin in coins:
            if coin <= i:
                dp[i] = min(dp[i], dp[i - coin] + 1)
    return dp[amount] if dp[amount] != float('inf') else -1
# dp[i] = min coins to make i. Time: O(amount × coins)
```

### 3. 0/1 Knapsack
```python
def knapsack(weights, values, W):
    n = len(weights)
    dp = [[0] * (W + 1) for _ in range(n + 1)]
    for i in range(1, n + 1):
        for w in range(W + 1):
            dp[i][w] = dp[i-1][w]    # don't take
            if weights[i-1] <= w:
                dp[i][w] = max(dp[i][w], dp[i-1][w - weights[i-1]] + values[i-1])
    return dp[n][W]
# Time: O(n×W), Space: O(n×W) → can reduce to O(W)
```

### 4. Longest Common Subsequence
```python
def lcs(s1, s2):
    m, n = len(s1), len(s2)
    dp = [[0] * (n + 1) for _ in range(m + 1)]
    for i in range(1, m + 1):
        for j in range(1, n + 1):
            if s1[i-1] == s2[j-1]:
                dp[i][j] = dp[i-1][j-1] + 1
            else:
                dp[i][j] = max(dp[i-1][j], dp[i][j-1])
    return dp[m][n]
```

### 5. Longest Increasing Subsequence
```python
def lis(nums):
    dp = [1] * len(nums)
    for i in range(1, len(nums)):
        for j in range(i):
            if nums[j] < nums[i]:
                dp[i] = max(dp[i], dp[j] + 1)
    return max(dp)
# Time: O(n²). Optimizable to O(n log n) with patience sorting + binary search
```

### 6. Edit Distance
```python
def edit_distance(word1, word2):
    m, n = len(word1), len(word2)
    dp = [[0] * (n + 1) for _ in range(m + 1)]
    for i in range(m + 1): dp[i][0] = i
    for j in range(n + 1): dp[0][j] = j
    for i in range(1, m + 1):
        for j in range(1, n + 1):
            if word1[i-1] == word2[j-1]:
                dp[i][j] = dp[i-1][j-1]
            else:
                dp[i][j] = 1 + min(dp[i-1][j],    # delete
                                   dp[i][j-1],    # insert
                                   dp[i-1][j-1])  # replace
    return dp[m][n]
```

### 7. Unique Paths (Grid DP)
```python
def unique_paths(m, n):
    dp = [[1] * n for _ in range(m)]
    for i in range(1, m):
        for j in range(1, n):
            dp[i][j] = dp[i-1][j] + dp[i][j-1]
    return dp[m-1][n-1]
# Paths = combinations(m+n-2, m-1) — also solvable with math
```

### 8. Word Break
```python
def word_break(s, wordDict):
    word_set = set(wordDict)
    dp = [False] * (len(s) + 1)
    dp[0] = True
    for i in range(1, len(s) + 1):
        for j in range(i):
            if dp[j] and s[j:i] in word_set:
                dp[i] = True
                break
    return dp[len(s)]
```

### 9. House Robber
```python
def rob(nums):
    if len(nums) == 1: return nums[0]
    prev2, prev1 = 0, 0
    for num in nums:
        curr = max(prev1, prev2 + num)
        prev2 = prev1
        prev1 = curr
    return prev1
# dp[i] = max money from first i houses
# dp[i] = max(dp[i-1], dp[i-2] + nums[i])
```

### 10. Partition Equal Subset Sum
```python
def can_partition(nums):
    total = sum(nums)
    if total % 2 != 0: return False
    target = total // 2
    dp = {0}    # set of achievable sums
    for num in nums:
        dp = {s + num for s in dp} | dp
    return target in dp
```

---
---

# Section 11: 50 Most Asked Interview Questions ❓

## Arrays & Strings (Q1–Q12)

---

**Q1. What is the time complexity of accessing an element in an array by index?** ⭐⭐⭐⭐⭐

O(1). Arrays store elements in contiguous memory. The address of any element is calculated directly: `base_address + index × element_size`. No traversal needed.

---

**Q2. How would you find two numbers in an array that sum to a target value?** ⭐⭐⭐⭐⭐

Use a HashMap: iterate through the array, for each element check if `target - element` exists in the map. If yes, return the pair. If no, store the element in the map. Time: O(n), Space: O(n). The brute force O(n²) nested loop is unacceptable for any interview.

---

**Q3. How do you find the maximum subarray sum?** ⭐⭐⭐⭐⭐

Kadane's algorithm: maintain a `current_sum` and `max_sum`. For each element, `current_sum = max(element, current_sum + element)` — decide whether to extend the current subarray or start fresh. Update `max_sum` if `current_sum` is larger. Time: O(n), Space: O(1).

---

**Q4. How do you check if a string is a palindrome?** ⭐⭐⭐⭐⭐

Two pointers: place one at the start and one at the end, move inward, comparing characters. If any pair mismatches, return False. Time: O(n), Space: O(1). Alternatively: `s == s[::-1]` but that uses O(n) space.

---

**Q5. How do you check if two strings are anagrams?** ⭐⭐⭐⭐⭐

Sort both and compare: O(n log n). Or count character frequencies using Counter and compare: O(n) time and space. For follow-up "check if any permutation of s1 is a substring of s2" — use sliding window with character frequency.

---

**Q6. How do you find the longest substring without repeating characters?** ⭐⭐⭐⭐⭐

Sliding window with a HashMap storing last seen index of each character. Maintain `left` pointer. When `s[right]` was seen at index `k`, set `left = max(left, k+1)`. Update `max_len = max(max_len, right - left + 1)`. Time: O(n), Space: O(min(n,charset)).

---

**Q7. How do you find the missing number in an array of 1 to n?** ⭐⭐⭐⭐

Expected sum = n(n+1)/2. Actual sum = sum(array). Missing = expected - actual. Time: O(n), Space: O(1). XOR approach: XOR all numbers 1 to n, XOR with all array elements — remaining value is the missing number.

---

**Q8. How do you rotate an array k positions to the right?** ⭐⭐⭐⭐

Three-reverse trick: (1) reverse entire array, (2) reverse first k elements, (3) reverse remaining n-k elements. Time: O(n), Space: O(1). Alternatively: `arr = arr[-k:] + arr[:-k]` but this uses O(n) extra space.

---

**Q9. How do you find duplicates in an array?** ⭐⭐⭐⭐

HashSet: iterate and check/add. O(n) time and space. For "no extra space" constraint: sort then check adjacent elements — O(n log n) time, O(1) space. For "array contains 1 to n" — use cyclic sort or Floyd's cycle detection on value-as-index.

---

**Q10. What is the sliding window technique?** ⭐⭐⭐⭐⭐

A technique that maintains a "window" over a contiguous portion of an array or string. Instead of recomputing the window's state from scratch each step, we add the new right element and remove the old left element in O(1). Used for: maximum sum of k elements, longest substring with condition, minimum window substring. Reduces O(n²) brute force to O(n).

---

**Q11. How would you find the longest common prefix among an array of strings?** ⭐⭐⭐

Sort the array — the first and last strings will have the most different characters. Find the common prefix of just these two: compare character by character. Time: O(n log n + m) where m = length of common prefix.

---

**Q12. How do you merge two sorted arrays?** ⭐⭐⭐⭐

Two pointer approach: maintain a pointer for each array, compare elements, add the smaller to result, advance that pointer. When one array is exhausted, append the rest of the other. Time: O(m+n), Space: O(m+n).

---

## Linked Lists (Q13–Q18)

---

**Q13. How do you reverse a singly linked list?** ⭐⭐⭐⭐⭐

Iterative: maintain three pointers — `prev=None, curr=head`. In each step: save `next_node = curr.next`, set `curr.next = prev`, move `prev = curr`, move `curr = next_node`. Return `prev` (new head). Time: O(n), Space: O(1). Recursive version uses O(n) stack space.

---

**Q14. How do you detect a cycle in a linked list?** ⭐⭐⭐⭐⭐

Floyd's cycle detection (fast & slow pointers): move slow 1 step, fast 2 steps per iteration. If they ever meet, there is a cycle. If fast reaches null, no cycle. Time: O(n), Space: O(1). HashSet approach also works but uses O(n) space.

---

**Q15. How do you find the middle of a linked list?** ⭐⭐⭐⭐

Fast and slow pointers: move slow 1 step, fast 2 steps. When fast reaches the end, slow is at the middle. For even-length lists, slow ends at the second middle node. Time: O(n), Space: O(1).

---

**Q16. How do you merge two sorted linked lists?** ⭐⭐⭐⭐

Use a dummy head node. Compare the heads of both lists, attach the smaller to the result, advance that list's pointer. Continue until one list is exhausted, then attach the rest. Time: O(m+n), Space: O(1) — just pointer manipulation.

---

**Q17. How do you remove the nth node from the end of a linked list?** ⭐⭐⭐⭐

Two-pointer one-pass: advance fast pointer n+1 steps from a dummy node before head. Then move both slow and fast until fast reaches null. Slow.next is the node to remove. Time: O(n), Space: O(1).

---

**Q18. What is the difference between array and linked list?** ⭐⭐⭐⭐⭐

Array: contiguous memory, O(1) random access, O(n) insert/delete (shifting), fixed or amortized size. Linked list: non-contiguous memory, O(n) access (no random access), O(1) insert/delete at known position, no size limit. Choose array for read-heavy workloads, linked list for frequent insertions/deletions at non-end positions.

---

## Stacks, Queues, Hashing (Q19–Q27)

---

**Q19. What problems can be solved with a stack?** ⭐⭐⭐⭐⭐

Balanced parentheses validation, next greater/smaller element (monotonic stack), expression evaluation, function call simulation, undo operations, DFS traversal, largest rectangle in histogram, daily temperatures. The key insight: use a stack whenever you need to "remember" elements to compare with future elements.

---

**Q20. What is a monotonic stack?** ⭐⭐⭐⭐

A stack that maintains elements in a monotonically increasing or decreasing order. When a new element violates the monotonic property, we pop elements until the property is restored. The popped elements have found their "answer" (next greater/smaller element). Solves next greater element, daily temperatures, largest rectangle problems all in O(n).

---

**Q21. What is the difference between a stack and a queue?** ⭐⭐⭐⭐

Stack is LIFO — last element added is first removed (like a stack of plates). Queue is FIFO — first element added is first removed (like a queue at a store). Stack uses push/pop. Queue uses enqueue/dequeue. Stack used for DFS, recursion simulation. Queue used for BFS, scheduling.

---

**Q22. How do you implement a queue using two stacks?** ⭐⭐⭐⭐

Use two stacks: `s1` (for enqueue) and `s2` (for dequeue). Enqueue: push to s1. Dequeue: if s2 is empty, pop all elements from s1 to s2 (reverses order), then pop from s2. Amortized O(1) per operation.

---

**Q23. When would you use a HashMap vs an array for frequency counting?** ⭐⭐⭐⭐

Use array when the key space is small and known (e.g., 26 letters, 256 ASCII characters) — `count = [0] * 26`. Use HashMap when the key space is large, sparse, or unknown. Array is slightly faster (cache-friendly) but limited to integer/char keys within a range.

---

**Q24. What is the time complexity of HashMap operations and why isn't it always O(1)?** ⭐⭐⭐⭐

Average case is O(1) due to hash function mapping keys directly to indices. Worst case is O(n) when all keys collide to the same hash bucket (extremely rare with a good hash function). Java's HashMap and Python's dict use well-designed hash functions that make collision rates very low in practice.

---

**Q25. How do you find the first non-repeating character in a string?** ⭐⭐⭐⭐

Two-pass with HashMap: first pass builds frequency count, second pass finds the first character with count 1. Time: O(n), Space: O(1) (limited character set). Or use `OrderedDict` to maintain insertion order.

---

**Q26. How do you find the top K frequent elements?** ⭐⭐⭐⭐

Build frequency map with Counter. Use a min-heap of size K: maintain the K most frequent elements. For each frequency, if heap has K elements and current frequency > heap min, replace. Return heap contents. Time: O(n log k). Alternatively: bucket sort by frequency — O(n).

---

**Q27. Explain the concept of hashing and collision resolution.** ⭐⭐⭐⭐

Hashing converts a key to an array index via a hash function, enabling O(1) average-case operations. Collision (two keys → same index) is resolved by chaining (linked list at each index) or open addressing (probe for next empty slot). Python uses open addressing with a probe sequence. Java HashMap uses chaining (upgraded to red-black tree for large chains in Java 8).

---

## Trees & Graphs (Q28–Q40)

---

**Q28. What are the different tree traversals and when would you use each?** ⭐⭐⭐⭐⭐

Inorder (L-Root-R): BST traversal gives sorted output. Used for BST problems. Preorder (Root-L-R): Root comes first — used for copying/serializing a tree. Postorder (L-R-Root): Root comes last — used for deleting a tree, evaluating expression trees. Level order (BFS): used for problems requiring level-by-level processing, shortest path in trees.

---

**Q29. What is a balanced binary tree? Why does it matter?** ⭐⭐⭐⭐

A balanced binary tree has abs(height(left) - height(right)) ≤ 1 for every node. It matters because operations on a BST are O(height). A balanced tree of n nodes has height O(log n), giving O(log n) operations. An unbalanced BST (e.g., inserting sorted data) degenerates to a linked list with O(n) height, making all operations O(n).

---

**Q30. What is the difference between a binary tree and a BST?** ⭐⭐⭐⭐⭐

A binary tree is any tree where each node has at most 2 children. A BST (Binary Search Tree) is a binary tree WITH the ordering property: left subtree values < node < right subtree values. This property enables O(log n) search, insert, and delete in a balanced BST versus O(n) in a general binary tree.

---

**Q31. How would you find the Lowest Common Ancestor (LCA) of two nodes?** ⭐⭐⭐⭐

Recursive approach: if root is null, or equals p or q, return root. Recursively find LCA in left and right subtrees. If both return non-null, current node is the LCA. If only one returns non-null, that is the LCA. For BST: if both p and q are less than root, go left; if both greater, go right; otherwise current root is LCA. Time: O(n) general, O(h) for BST.

---

**Q32. How do you serialize and deserialize a binary tree?** ⭐⭐⭐

Use preorder traversal with null markers: serialize by preorder with "#" for null nodes, separated by commas. Deserialize by splitting the string and recursively building the tree using a queue. Time: O(n), Space: O(n).

---

**Q33. What is a graph and how is it different from a tree?** ⭐⭐⭐⭐⭐

A graph is a collection of vertices and edges. A tree is a special graph that is connected, acyclic, and has exactly n-1 edges for n nodes. Graphs can have cycles, disconnected components, and multiple edges. Trees have a root; graphs have no root concept. All trees are graphs, but not all graphs are trees.

---

**Q34. What is the difference between BFS and DFS?** ⭐⭐⭐⭐⭐

BFS uses a queue, explores level by level, finds shortest path in unweighted graphs. DFS uses a stack (or recursion), explores as deep as possible first, used for cycle detection, finding all paths, topological sort. BFS is generally better for shortest path; DFS for problems requiring exploring all possibilities. Both are O(V+E).

---

**Q35. How do you detect a cycle in a directed graph?** ⭐⭐⭐⭐

DFS with three states per node: unvisited (0), in current path/gray (1), fully processed/black (2). If during DFS we reach a gray node, we've found a cycle. Alternatively, topological sort (Kahn's): if the sorted output doesn't contain all nodes, there is a cycle.

---

**Q36. What is topological sort and when is it used?** ⭐⭐⭐⭐

Topological sort is a linear ordering of vertices in a DAG (Directed Acyclic Graph) such that for every directed edge u→v, u comes before v. Used for: course prerequisites (can you complete all courses?), build systems (what to compile first?), task scheduling. Implemented with DFS (reverse postorder) or BFS/Kahn's algorithm (in-degree approach). Time: O(V+E).

---

**Q37. How does Dijkstra's algorithm work?** ⭐⭐⭐⭐

Dijkstra finds shortest paths from a source to all vertices in a weighted graph with non-negative weights. Start with all distances as infinity, source as 0. Use a min-heap (priority queue) to always process the vertex with the current shortest known distance. For each processed vertex, relax its neighbors (update distances if shorter path found). Time: O((V+E) log V). Does NOT work with negative edge weights.

---

**Q38. What is the difference between Dijkstra and BFS for shortest path?** ⭐⭐⭐⭐

BFS finds shortest path in unweighted graphs (each edge has weight 1). Dijkstra finds shortest path in weighted graphs with non-negative weights. BFS is O(V+E). Dijkstra is O((V+E) log V). If the graph is unweighted, BFS is simpler and faster; if weighted, Dijkstra is needed.

---

**Q39. What is Union-Find and what problems does it solve?** ⭐⭐⭐⭐

Union-Find (Disjoint Set Union) efficiently maintains a partition of elements into non-overlapping sets. `find(x)` returns which set x belongs to. `union(x,y)` merges the sets of x and y. With path compression and union by rank, each operation is nearly O(1). Used for: number of connected components, cycle detection in undirected graphs, minimum spanning tree (Kruskal's).

---

**Q40. How do you find the number of connected components in a graph?** ⭐⭐⭐⭐

Iterate through all unvisited nodes. For each unvisited node, do a BFS or DFS marking all reachable nodes as visited. Increment a counter. Return the counter — it equals the number of connected components. Time: O(V+E). Also solvable with Union-Find.

---

## Sorting, Searching, DP (Q41–Q50)

---

**Q41. Why is merge sort preferred over quick sort in certain scenarios?** ⭐⭐⭐⭐

Merge sort guarantees O(n log n) worst case while quick sort degrades to O(n²) on sorted/reverse-sorted data (unless using random pivot). Merge sort is stable (preserves relative order of equal elements) while quick sort is not. Merge sort is preferred for linked lists (no random access needed), external sorting (data doesn't fit in RAM), and when stability is required.

---

**Q42. How does binary search work and what are its requirements?** ⭐⭐⭐⭐⭐

Binary search requires a sorted, random-access collection. It repeatedly halves the search space: compare target with the middle element, eliminate the half that cannot contain the target. After log₂(n) steps at most, either the target is found or confirmed absent. Time: O(log n), Space: O(1). The critical bug to avoid: use `mid = left + (right - left) // 2` to prevent integer overflow.

---

**Q43. What is the worst case for quick sort and how can it be avoided?** ⭐⭐⭐⭐

Worst case O(n²) occurs when the pivot is always the minimum or maximum (e.g., sorted array with last element as pivot). Avoided by: random pivot selection, "median of three" pivot (choose median of first, middle, last), or using introsort (switches to heap sort when recursion depth exceeds threshold) — used by C++ STL and Python's sort.

---

**Q44. What is counting sort and when can it be used?** ⭐⭐⭐

Counting sort works for integer keys within a known range [0, k]. Count occurrences of each value, then output values in order of their counts. Time: O(n+k), Space: O(k). Only useful when k is small relative to n. Used for sorting student grades (0-100), character frequencies, age distributions.

---

**Q45. What is dynamic programming and how is it different from recursion?** ⭐⭐⭐⭐⭐

Dynamic programming is an optimization technique for problems with overlapping subproblems and optimal substructure. Pure recursion recomputes the same subproblems exponentially. DP avoids this by storing results (memoization = top-down DP with cache, tabulation = bottom-up DP with table). Example: naive fibonacci is O(2ⁿ) recursive, O(n) with DP. DP is recursion + remembering + optimal.

---

**Q46. What is the difference between memoization and tabulation?** ⭐⭐⭐⭐

Memoization (top-down): recursive approach with a cache. Computes only needed subproblems. More natural to think about. Can hit recursion depth limit for large inputs. Tabulation (bottom-up): iterative approach filling a table. Computes ALL subproblems from smallest to largest. No recursion overhead. Usually faster in practice. Same asymptotic complexity.

---

**Q47. How do you identify if a problem can be solved with DP?** ⭐⭐⭐⭐⭐

Two required properties: (1) Optimal substructure — optimal solution to the problem can be built from optimal solutions to subproblems. (2) Overlapping subproblems — the same subproblems appear multiple times. Trigger words: "minimum/maximum", "count the ways", "longest/shortest", "is it possible", "total number of". If the problem has choices at each step and you want the best outcome, think DP.

---

**Q48. What is the time and space complexity of the coin change problem?** ⭐⭐⭐⭐

Time: O(amount × number of coins) — for each amount from 1 to target, iterate through all coins. Space: O(amount) for the dp array. This is pseudo-polynomial — it is polynomial in the value of amount, not in the number of bits to represent it.

---

**Q49. What is the difference between greedy and dynamic programming?** ⭐⭐⭐⭐

Greedy makes locally optimal choices at each step without reconsidering. Fast: O(n) or O(n log n) typically. Works when local optimum = global optimum (activity selection, fractional knapsack). DP explores all possibilities via subproblems. Slower but correct for problems where greedy fails (0/1 knapsack, coin change with arbitrary coins). First try greedy, prove it works, otherwise use DP.

---

**Q50. How do you approach a problem you've never seen before in an interview?** ⭐⭐⭐⭐⭐

The 7-step framework:
1. Clarify the problem — ask about constraints, edge cases, examples
2. State the brute force — shows you understand the problem
3. Identify the bottleneck — what makes brute force slow?
4. Think of data structures/patterns that address the bottleneck
5. Code the optimized solution — speak while coding
6. Test with examples — trace through your code
7. Analyze complexity — state time and space before interviewer asks

Never start coding without talking. Interviewers value your thinking process as much as the solution.

---
---

# Section 12: 14 Must-Know Patterns 🎯

## Pattern 1 — Two Pointers
**When:** Sorted array, pair/triplet finding, palindrome, remove duplicates
**Template:**
```python
left, right = 0, len(arr) - 1
while left < right:
    if condition(arr[left], arr[right]):
        process(); left += 1; right -= 1
    elif need_larger:
        left += 1
    else:
        right -= 1
```

## Pattern 2 — Sliding Window
**When:** "Subarray/substring of size k", "longest with condition", "minimum window"
```python
left = 0; state = {}
for right in range(len(s)):
    # add s[right] to state
    while condition_violated(state):
        # remove s[left] from state
        left += 1
    # update answer using (right - left + 1)
```

## Pattern 3 — Fast & Slow Pointers (Floyd's Cycle)
**When:** Cycle detection, middle of list, palindrome linked list
```python
slow = fast = head
while fast and fast.next:
    slow = slow.next
    fast = fast.next.next
    if slow == fast: return True  # cycle
return False
```

## Pattern 4 — Merge Intervals
**When:** "Overlapping intervals", "merge ranges", "meeting rooms"
```python
intervals.sort(key=lambda x: x[0])    # sort by start
merged = [intervals[0]]
for start, end in intervals[1:]:
    if start <= merged[-1][1]:         # overlap
        merged[-1][1] = max(merged[-1][1], end)
    else:
        merged.append([start, end])
```

## Pattern 5 — Cyclic Sort
**When:** "Array with numbers 1 to n", "find missing/duplicate"
```python
i = 0
while i < len(nums):
    j = nums[i] - 1    # where nums[i] should be
    if nums[i] != nums[j]:
        nums[i], nums[j] = nums[j], nums[i]
    else:
        i += 1
# Now scan for misplaced elements
```

## Pattern 6 — Binary Search on Answer
**When:** "Minimum/maximum X such that condition holds", "capacity", "split"
```python
lo, hi = min_possible, max_possible
while lo < hi:
    mid = (lo + hi) // 2
    if condition(mid):
        hi = mid        # try smaller (minimize)
    else:
        lo = mid + 1    # too small
return lo
```

## Pattern 7 — BFS (Level Order / Shortest Path)
**When:** Shortest path in unweighted graph, level-by-level tree processing
```python
from collections import deque
queue = deque([start]); visited = {start}
while queue:
    node = queue.popleft()
    for neighbor in graph[node]:
        if neighbor not in visited:
            visited.add(neighbor)
            queue.append(neighbor)
```

## Pattern 8 — DFS / Backtracking
**When:** All combinations/permutations/subsets, path finding, N-Queens
```python
def backtrack(start, current):
    if is_solution(current):
        result.append(current[:])
        return
    for choice in get_choices(start):
        current.append(choice)        # choose
        backtrack(next_start, current) # explore
        current.pop()                 # un-choose
```

## Pattern 9 — Dynamic Programming (Top-Down / Memoization)
**When:** Optimization problem with overlapping subproblems
```python
from functools import lru_cache

@lru_cache(maxsize=None)
def dp(state):
    if base_case(state):
        return base_value
    return optimal(dp(sub_state_1), dp(sub_state_2), ...)
```

## Pattern 10 — Dynamic Programming (Bottom-Up / Tabulation)
**When:** Same as top-down but iterative (avoids recursion depth limit)
```python
dp = [initial_value] * (n + 1)
dp[0] = base_case
for i in range(1, n + 1):
    dp[i] = f(dp[i-1], dp[i-2], ...)    # recurrence
return dp[n]
```

## Pattern 11 — Monotonic Stack
**When:** "Next greater/smaller element", "daily temperatures", "histogram"
```python
stack = []    # stores indices, maintains increasing/decreasing order
result = [-1] * len(arr)
for i, val in enumerate(arr):
    while stack and arr[stack[-1]] < val:    # pop while smaller
        result[stack.pop()] = val             # val is their NGE
    stack.append(i)
```

## Pattern 12 — Heap / Priority Queue
**When:** "K largest/smallest", "merge K sorted", "running median"
```python
import heapq
heap = []
for num in nums:
    heapq.heappush(heap, num)          # O(log n)
    if len(heap) > k:
        heapq.heappop(heap)            # maintain size k
# heap[0] is the kth largest
```

## Pattern 13 — Trie
**When:** "Prefix", "autocomplete", "word search", "starts with"
```python
trie = {}
def insert(word):
    node = trie
    for c in word:
        node = node.setdefault(c, {})
    node['#'] = True    # end of word marker

def search(word):
    node = trie
    for c in word:
        if c not in node: return False
        node = node[c]
    return '#' in node
```

## Pattern 14 — Union-Find
**When:** "Connected components", "number of islands", "redundant connection"
```python
parent = list(range(n))
def find(x):
    if parent[x] != x:
        parent[x] = find(parent[x])    # path compression
    return parent[x]
def union(x, y):
    px, py = find(x), find(y)
    if px == py: return False    # already connected
    parent[px] = py
    return True
```

---
---

# Section 13: How to Approach Any Coding Problem 🧠

## The 7-Step Framework ⭐⭐⭐⭐⭐

This is not just advice — this is the literal procedure top candidates follow in every interview.

### Step 1: Understand the Problem (2–3 minutes)
```
Ask / confirm:
- What is the exact input format? (array of integers? string? linked list?)
- What should I return? (index? value? boolean? new structure?)
- Are there constraints? (n ≤ 10⁵? values ≥ 0? sorted?)
- Edge cases: empty input, single element, all same values, duplicates?
- Can I modify the input?
```

### Step 2: Work Through Examples (2 minutes)
```
Take the given example and trace through it manually.
Create your OWN example — especially edge cases.
This shows the interviewer you are thorough, and often reveals
the algorithm naturally.
```

### Step 3: State the Brute Force First (1 minute)
```
Always state the naive O(n²) or O(n³) solution FIRST.
"The brute force would be to check every pair — O(n²).
Can I do better?"
This demonstrates problem understanding even if you don't implement it.
```

### Step 4: Optimize — Think Out Loud (3–5 minutes)
```
Ask yourself:
- What is the bottleneck? (usually the inner loop)
- Can I use extra space (HashMap/HashSet) to eliminate searching?
- Does sorting the input unlock a two-pointer approach?
- Can I precompute something? (prefix sum, sorted order)
- Which of the 14 patterns fits here?
- Can I reduce from O(n²) → O(n log n) with sorting?
- Can I reduce from O(n) search → O(1) with HashMap?
```

### Step 5: Code the Optimized Solution (10–15 minutes)
```
Speak while you code. Say what you're doing and why.
Write clean code — meaningful variable names, not i,j,k for everything.
Handle edge cases AS YOU CODE, not as an afterthought.
Don't write everything silently then explain — explain AS YOU WRITE.
```

### Step 6: Test Your Code (3–5 minutes)
```
Trace through your code with the given example.
Test the edge cases you identified in Step 1.
Common bugs to check:
- Off-by-one errors in loops (< vs <=)
- Null/None checks for linked list problems
- Empty input handling
- Integer overflow (rare in Python, common in Java/C++)
```

### Step 7: State the Complexity
```
Always finish with:
"This solution has time complexity O(_) and space complexity O(_)."
If asked "can you do better?" — think about the theoretical lower bound.
Comparison-based sorting cannot be better than O(n log n).
```

---

## Pattern Recognition Triggers ⭐⭐⭐⭐⭐

```
"Sorted array" + "pair/triplet"    → Two Pointers
"Subarray/substring" + "max/min"   → Sliding Window
"Subarray sum = k"                 → Prefix Sum + HashMap
"Linked list" + "cycle"            → Fast & Slow Pointers
"Linked list" + "reverse/middle"   → Iteration with 3 pointers
"Tree traversal"                   → DFS (recursion)
"Shortest path" in graph           → BFS (unweighted) / Dijkstra (weighted)
"All combinations/permutations"    → Backtracking
"Optimization" + "choices"         → Dynamic Programming
"K largest/smallest"               → Heap of size K
"Prefix matching"                  → Trie
"Connected components"             → Union-Find / BFS / DFS
"Next greater element"             → Monotonic Stack
"Sorted" + "find position"         → Binary Search
"Intervals" + "overlap"            → Sort by start + merge
"1 to n" + "missing/duplicate"     → Cyclic Sort or XOR
```

---
---

# Section 14: Language-Specific Tips 💻

## Python Tips for DSA

```python
# Collections module — use these constantly
from collections import defaultdict, Counter, deque, OrderedDict

# defaultdict — never check "key in dict" before accessing
graph = defaultdict(list)    # graph[node].append(neighbor) — no KeyError

# Counter — frequency counting in one line
freq = Counter(arr)
most_common_3 = freq.most_common(3)

# deque — O(1) appendleft and popleft (list.insert(0,x) is O(n)!)
from collections import deque
queue = deque()
queue.appendleft(x)    # O(1)
queue.popleft()        # O(1)

# heapq — min-heap
import heapq
heap = []
heapq.heappush(heap, val)
min_val = heapq.heappop(heap)

# Max-heap: negate values
heapq.heappush(heap, -val)
max_val = -heapq.heappop(heap)

# lru_cache — memoization decorator
from functools import lru_cache

@lru_cache(maxsize=None)
def dp(n):
    if n <= 1: return n
    return dp(n-1) + dp(n-2)

# enumerate — use instead of range(len)
for i, val in enumerate(arr):  # i = index, val = value

# zip — iterate two arrays together
for a, b in zip(arr1, arr2):
    ...

# Sorting with key
arr.sort(key=lambda x: (x[1], -x[0]))   # sort by [1] asc, then [0] desc

# Infinity
float('inf')    # positive infinity
float('-inf')   # negative infinity

# Integer division
n // 2          # floor division (always use this, not n / 2 for indices)

# String to list and back
chars = list(s)
s = ''.join(chars)

# Set operations
intersection = set1 & set2
union = set1 | set2
difference = set1 - set2

# sys.setrecursionlimit — for deep recursion
import sys
sys.setrecursionlimit(10**6)
```

## Java Tips for DSA

```java
// Use ArrayList (dynamic) not array when size unknown
List<Integer> list = new ArrayList<>();

// Stack
Deque<Integer> stack = new ArrayDeque<>();
stack.push(x);      // push to top
stack.pop();        // pop from top
stack.peek();       // peek top

// Queue (use ArrayDeque, not LinkedList)
Deque<Integer> queue = new ArrayDeque<>();
queue.offer(x);     // enqueue
queue.poll();       // dequeue
queue.peek();       // peek front

// Priority Queue (min-heap by default)
PriorityQueue<Integer> minHeap = new PriorityQueue<>();
PriorityQueue<Integer> maxHeap = new PriorityQueue<>(Collections.reverseOrder());

// HashMap
Map<Integer, Integer> map = new HashMap<>();
map.getOrDefault(key, 0);    // get with default
map.put(key, map.getOrDefault(key, 0) + 1);   // increment

// HashSet
Set<Integer> set = new HashSet<>();
set.contains(x);    // O(1)

// String to char array and back
char[] chars = s.toCharArray();
String s = new String(chars);

// StringBuilder (not String + for concatenation!)
StringBuilder sb = new StringBuilder();
sb.append(c);
String result = sb.toString();

// Sorting
Arrays.sort(arr);
Arrays.sort(arr, (a, b) -> b - a);    // reverse
```

## C++ Tips for DSA

```cpp
// STL containers
#include <vector>
#include <map>
#include <unordered_map>
#include <set>
#include <unordered_set>
#include <queue>
#include <stack>
#include <algorithm>

// Use unordered_map (O(1)) not map (O(log n)) for most problems
unordered_map<int, int> freq;
freq[x]++;    // auto-initializes to 0

// Priority Queue (max-heap by default!)
priority_queue<int> maxHeap;    // max at top
priority_queue<int, vector<int>, greater<int>> minHeap;    // min at top

// Sorting with lambda
sort(arr.begin(), arr.end(), [](int a, int b){ return a > b; });

// INT_MAX, INT_MIN
#include <climits>
int x = INT_MAX;    // 2^31 - 1
```

---
---

# Section 15: 2-Week Study Plan 📅

**Daily commitment: 2–3 hours**
→ Morning: 1.5 hours — learn concept + study pattern
→ Evening: 1 hour — solve 2–3 problems

## Week 1 — Core Patterns

| Day | Topic | Problems to Solve | Target |
|-----|-------|------------------|--------|
| **Day 1** | Big O + Arrays + Prefix Sum | Two Sum, Max Subarray, Contains Duplicate | 3 Easy |
| **Day 2** | Two Pointers + Sliding Window | Valid Palindrome, 3Sum, Longest Substring No Repeat | 3 Easy/Med |
| **Day 3** | Hashing patterns | Group Anagrams, Top K Frequent, Longest Consecutive | 3 Medium |
| **Day 4** | Binary Search (all 3 templates) | Binary Search, Search in Rotated, Find Min in Rotated | 3 Medium |
| **Day 5** | Linked List (all 3 patterns) | Reverse LL, Detect Cycle, Merge Two Sorted | 3 Easy/Med |
| **Day 6** | Stacks (basic + monotonic) | Valid Parentheses, Daily Temperatures, Next Greater | 3 Medium |
| **Day 7** | Queues + BFS on grids | Number of Islands, Max Area of Island, Flood Fill | 3 Medium |

## Week 2 — Trees, DP, Advanced

| Day | Topic | Problems to Solve | Target |
|-----|-------|------------------|--------|
| **Day 8** | Tree traversals + recursion | Max Depth, Diameter, Invert Binary Tree | 3 Easy/Med |
| **Day 9** | BST + LCA + paths | Validate BST, LCA, Path Sum, Kth Smallest in BST | 3 Medium |
| **Day 10** | Heap patterns | Kth Largest, Top K Frequent, Merge K Lists | 3 Medium |
| **Day 11** | Graph BFS/DFS | Clone Graph, Course Schedule, Pacific Atlantic | 3 Medium |
| **Day 12** | DP Part 1 — 1D DP | Climbing Stairs, House Robber, Coin Change | 3 Medium |
| **Day 13** | DP Part 2 — 2D DP | Unique Paths, LCS, Edit Distance, Knapsack | 3 Medium |
| **Day 14** | Backtracking + Review | Subsets, Permutations, Combination Sum | 3 Medium |

## Daily Practice (Every Day)
- ✅ Solve at least 2 problems — one easy, one medium
- ✅ State the approach and complexity BEFORE coding
- ✅ Review 1 problem you got wrong yesterday
- ✅ Read the editorial for any problem taking >45 minutes

## After Week 2
- Target: 50+ problems solved
- LeetCode daily — 1 medium problem every morning
- Join weekly contest — even finishing 2/4 is progress
- Company-specific lists: LeetCode tags → filter by company → last 6 months

---
---

# Section 16: Readiness Checklist ✅

## You Are Ready for Coding Rounds When You Can:

### Complexity Analysis
- [ ] Calculate Big O for any code snippet in under 30 seconds
- [ ] State time AND space complexity for every solution you write
- [ ] Know when O(n log n) is the best possible (comparison sort)
- [ ] Explain why HashMap gives O(1) average vs O(n) worst case

### Arrays & Strings
- [ ] Implement Kadane's algorithm from memory
- [ ] Solve sliding window problems with both fixed and variable window
- [ ] Implement prefix sum and use it for O(1) range queries
- [ ] Recognize two-pointer vs sliding window vs prefix sum triggers

### Linked Lists
- [ ] Reverse a linked list iteratively in under 3 minutes
- [ ] Detect and find the start of a cycle (Floyd's algorithm)
- [ ] Find the middle of a linked list with fast/slow pointers
- [ ] Remove nth node from end in one pass

### Stacks & Queues
- [ ] Solve valid parentheses without looking at code
- [ ] Explain and implement monotonic stack for next greater element
- [ ] Implement BFS using deque from scratch

### Hashing
- [ ] Solve two sum and all variants (3sum, 4sum) using HashMap
- [ ] Group anagrams and any "group by canonical form" problem
- [ ] Subarray sum equals k using prefix sum + HashMap

### Trees
- [ ] Implement all 4 traversals (inorder, preorder, postorder, level order) from memory
- [ ] Find height, diameter, LCA of a binary tree
- [ ] Validate a BST using min/max bounds
- [ ] Identify which of the 3 tree patterns a problem uses in under 1 minute

### Graphs
- [ ] Implement BFS and DFS from scratch for any graph representation
- [ ] Solve number of islands and connected components
- [ ] Implement topological sort using Kahn's algorithm
- [ ] Use Union-Find for cycle detection and connected components

### Sorting & Searching
- [ ] Implement merge sort and quick sort from scratch
- [ ] Use all 3 binary search templates without looking at notes
- [ ] Apply binary search on answer space to optimization problems

### Dynamic Programming
- [ ] Solve all 10 DP classics without help (coin change, knapsack, LCS, LIS, edit distance...)
- [ ] Identify when a problem needs DP vs greedy in under 30 seconds
- [ ] Convert any recursive solution to bottom-up DP

### Interview Behavior
- [ ] Follow the 7-step framework for every problem
- [ ] Speak while coding — never code in silence
- [ ] Test with examples and edge cases before saying "done"
- [ ] Handle "wrong answer" gracefully — debug methodically, not randomly

---

## 🔥 Last-Day Rapid Review — Memorize This Block

```
COMPLEXITY:
Array access O(1) | Array search O(n) | Insert/Delete O(n)
HashMap/Set all O(1) average | BST balanced O(log n) | Heap O(log n)
BFS/DFS O(V+E) | Dijkstra O((V+E)logV) | Sort O(n log n)
Binary Search O(log n) | Merge Sort O(n logn) space O(n) | Quick Sort O(n logn) avg

BIG O ORDER: O(1) < O(logn) < O(n) < O(nlogn) < O(n²) < O(2ⁿ) < O(n!)

14 PATTERN TRIGGERS:
Two Pointers     → sorted + pair/palindrome/duplicates
Sliding Window   → subarray/substring + max/min condition
Fast & Slow      → cycle + middle of list
Merge Intervals  → overlapping intervals
Cyclic Sort      → 1 to n array, missing/duplicate
Binary Search    → sorted + find/minimize/maximize
BFS              → shortest path + level order + nearest
DFS/Backtrack    → all paths + combinations + permutations
DP Top-Down      → recursion + overlapping + cache
DP Bottom-Up     → table filling + base cases
Monotonic Stack  → next greater/smaller + histogram
Heap             → K largest/smallest + running median
Trie             → prefix + word search + autocomplete
Union-Find       → connected components + cycle undirected

KEY ALGORITHMS:
Kadane's:     cur = max(x, cur+x); ans = max(ans, cur)
Floyd's:      slow.next, fast.next.next — meet = cycle
Two Sum:      seen[complement] → found; else seen[num]=i
Valid Parens: push '({[', pop if matching closing, return stack empty
Reverse LL:   prev=None; while cur: nxt=cur.next; cur.next=prev; prev=cur; cur=nxt
Binary Search: mid = left+(right-left)//2; left<=right while loop
DFS tree:     if not node: return; left=dfs(node.left); right=dfs(node.right); return f(left,right)
BFS graph:    deque; visited set; level by level with len(queue) loop

DP PATTERNS:
Fibonacci family: dp[i] = dp[i-1] + dp[i-2]
Coin change:      dp[i] = min(dp[i-coin]+1 for coin in coins if coin<=i)
0/1 Knapsack:     dp[i][w] = max(dp[i-1][w], dp[i-1][w-wt]+val)
LCS:              dp[i][j] = dp[i-1][j-1]+1 if match, else max(dp[i-1][j], dp[i][j-1])
Grid paths:       dp[i][j] = dp[i-1][j] + dp[i][j-1]
```

---

## 📝 Next Steps

**Today:**
1. Code Two Sum, Valid Parentheses, and Reverse Linked List from scratch
2. Memorize the Big O complexity table — know it cold
3. Pick ONE pattern (Two Pointers) and solve 3 problems with it

**This Week:**
1. Complete Sections 2–10 of this file
2. Solve 2 problems daily — always state complexity before coding
3. Implement the 14 pattern templates in your code editor

**Every Day Until Interview:**
- Solve 1 medium LeetCode problem under a 30-minute timer
- Trace through your solution manually before running it
- Review this rapid review block every morning

---

> **Navigation:** [← 01_DSA_Masterguide.md](./01_DSA_Masterguide.md) | [Back to README](./README.md) | [03_DSA_Practice_Repository.md →](./03_DSA_Practice_Repository.md)

---

*File: `02_DSA_Interview_Prep.md` | Version 1.0 | 2026*
*Part of the DSA Repository*
*Companion to Operating Systems and Computer Networks interview prep files*
