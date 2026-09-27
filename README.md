# leetcode

Solutions to LeetCode problems, written in Python — a running record of working through data structures and algorithms.

---

## What lives here

One file per problem, each one self-contained and runnable on its own.

A file is easiest to come back to when it carries a little context at the top:

```python
"""
1. Two Sum
https://leetcode.com/problems/two-sum/

Approach: one pass with a hash map from value to index.
Time:  O(n)
Space: O(n)
"""


class Solution:
    def twoSum(self, nums: list[int], target: int) -> list[int]:
        seen: dict[int, int] = {}

        for index, value in enumerate(nums):
            complement = target - value

            if complement in seen:
                return [seen[complement], index]

            seen[value] = index

        return []
```

The problem number, the link, the approach in one line, and the complexity — enough to remind you what you were thinking without rereading the whole solution.

---

## Suggested layout

Grouping by technique makes patterns easier to spot across problems:

```
leetcode/
├── arrays/           Two pointers, sliding window, prefix sums
├── strings/          Parsing, matching, building
├── hashing/          Maps and sets
├── linked-lists/     Traversal, reversal, cycle detection
├── trees/            Traversals, recursion, BSTs
├── graphs/           BFS, DFS, topological sort, union-find
├── dynamic-programming/
├── heaps/            Priority queues, top-k
└── binary-search/
```

---

## Getting started

### Prerequisites

- Python 3.10 or newer

```bash
git clone https://github.com/harshlaxkar07/leetcode.git
cd leetcode
python arrays/two_sum.py
```

---

## Related repositories

| Repository | What it covers |
|---|---|
| [`python`](https://github.com/harshlaxkar07/python) | Language fundamentals and standard-library practice |
