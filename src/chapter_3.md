# 02. DSA (in Python)

Priority: **Core** = learn first, **Next** = after Core, **Later** = just know it exists.

**How to practice:** go topic by topic, easy problems first. Don't jump to the full NeetCode 150 yet. If you're stuck for 30-40 minutes, read the solution, understand it, then re-solve it from scratch the next day.

## A. Foundations

| Done | Concept                                                                  | Priority | What you should be able to do            |
| ---- | ------------------------------------------------------------------------ | -------- | ---------------------------------------- |
| ☐    | Time complexity, Big-O (O(1), O(log n), O(n), O(n log n), O(n²))         | Core     | State the complexity of your own code    |
| ☐    | Space complexity                                                         | Core     | Know when you're using extra memory      |
| ☐    | Reading constraints to guess the expected complexity                     | Core     | See `n ≤ 10^5` and know O(n²) won't work |
| ☐    | Python complexity of built-ins (list append/pop/insert, dict, set, `in`) | Core     | Avoid accidental O(n) inside loops       |
| ☐    | Edge cases (empty, single element, duplicates, negatives)                | Core     | Test your solution before submitting     |
| ☐    | Dry-running code on paper                                                | Core     | Trace a solution by hand                 |

## B. Core data structures

| Done | Concept                          | Priority | Typical problems                                             |
| ---- | -------------------------------- | -------- | ------------------------------------------------------------ |
| ☐    | Arrays / lists                   | Core     | Two Sum, Best Time to Buy and Sell Stock, Contains Duplicate |
| ☐    | Strings                          | Core     | Valid Anagram, Valid Palindrome                              |
| ☐    | Hashmaps / dictionaries          | Core     | Group Anagrams, Top K Frequent                               |
| ☐    | Sets                             | Core     | Longest Consecutive Sequence                                 |
| ☐    | Stacks                           | Core     | Valid Parentheses, Min Stack                                 |
| ☐    | Queues and deques                | Core     | Sliding window max (deque)                                   |
| ☐    | Linked lists                     | Next     | Reverse List, Merge Two Lists, Cycle detection               |
| ☐    | Trees (binary tree, BST)         | Next     | Max Depth, Invert Tree, Level Order Traversal                |
| ☐    | Heaps / priority queues          | Next     | Kth Largest Element, Merge K Lists                           |
| ☐    | Graphs (adjacency list / matrix) | Next     | Number of Islands, Clone Graph                               |
| ☐    | Tries                            | Later    | Implement Trie, Word Search II                               |
| ☐    | Union-Find (Disjoint Set)        | Later    | Number of Connected Components                               |
| ☐    | Segment tree, Fenwick tree       | Later    | Skip for now                                                 |

## C. Core patterns

| Done | Pattern                               | Priority | When to think of it                                     |
| ---- | ------------------------------------- | -------- | ------------------------------------------------------- |
| ☐    | Hashmap for lookup / counting         | Core     | "Have I seen this?", frequency counts                   |
| ☐    | Two pointers                          | Core     | Sorted array, pairs, palindromes                        |
| ☐    | Sliding window                        | Core     | Longest/shortest subarray or substring with a condition |
| ☐    | Prefix sums                           | Core     | Range sum queries, subarray sums                        |
| ☐    | Binary search (including on answer)   | Core     | Sorted data, "minimum that satisfies"                   |
| ☐    | Sorting + greedy choice               | Core     | Intervals, scheduling                                   |
| ☐    | Recursion                             | Core     | Anything that breaks into smaller identical problems    |
| ☐    | Backtracking                          | Core     | Subsets, permutations, combinations                     |
| ☐    | Fast and slow pointers                | Next     | Linked list cycle, middle node                          |
| ☐    | Monotonic stack                       | Next     | Next greater element, daily temperatures                |
| ☐    | BFS                                   | Next     | Shortest path in unweighted graphs, level order         |
| ☐    | DFS                                   | Next     | Tree/graph traversal, connected components              |
| ☐    | Intervals (merge, insert)             | Next     | Meeting rooms, merge intervals                          |
| ☐    | Top-K with heap                       | Next     | K closest, K most frequent                              |
| ☐    | Basic dynamic programming (1D)        | Next     | Climbing stairs, house robber, coin change              |
| ☐    | 2D DP (grids, strings)                | Later    | Unique paths, LCS, edit distance                        |
| ☐    | Topological sort                      | Later    | Course schedule                                         |
| ☐    | Dijkstra / shortest path with weights | Later    | Network delay time                                      |
| ☐    | Bit manipulation                      | Later    | Single number, counting bits                            |

## D. Algorithms

| Done | Concept                                      | Priority | What you should be able to do          |
| ---- | -------------------------------------------- | -------- | -------------------------------------- |
| ☐    | Linear and binary search                     | Core     | Write binary search without bugs       |
| ☐    | Basic sorting (bubble, selection, insertion) | Core     | Understand how sorting works           |
| ☐    | Merge sort, quick sort                       | Next     | Explain and implement merge sort       |
| ☐    | Python `sorted`, `sort`, custom `key`        | Core     | Sort by multiple criteria              |
| ☐    | Recursion trees, memoization                 | Next     | Turn plain recursion into DP           |
| ☐    | Tree traversals (pre/in/post/level)          | Next     | Write them recursively and iteratively |
| ☐    | Graph traversals (BFS / DFS)                 | Next     | Write both from memory                 |
| ☐    | Greedy algorithms                            | Next     | Know when greedy is valid              |
| ☐    | Minimum spanning tree (Kruskal, Prim)        | Later    | Know the idea                          |
| ☐    | KMP, string matching                         | Later    | Skip for now                           |

## E. Python tools for DSA

| Done | Concept                                       | Priority | Use                        |
| ---- | --------------------------------------------- | -------- | -------------------------- |
| ☐    | `collections.Counter`, `defaultdict`, `deque` | Core     | Counting, grouping, queues |
| ☐    | `heapq`                                       | Next     | Min-heap, top-K            |
| ☐    | `bisect`                                      | Next     | Binary search on lists     |
| ☐    | `sorted` with `key=lambda`                    | Core     | Custom sorting             |
| ☐    | `functools.lru_cache`                         | Next     | Easy memoization           |
| ☐    | Slicing tricks, `zip`, `enumerate`            | Core     | Cleaner code               |

## F. Problem-solving habits

| Done | Habit                                                        | Priority |
| ---- | ------------------------------------------------------------ | -------- |
| ☐    | Restate the problem and write 2-3 examples before coding     | Core     |
| ☐    | Start with brute force, then optimise                        | Core     |
| ☐    | Say the complexity out loud                                  | Core     |
| ☐    | Keep a small notebook: pattern, problem, what tripped you    | Core     |
| ☐    | Re-solve problems you failed after 1 day, then after 1 week  | Core     |
| ☐    | Practice explaining your solution out loud (interview style) | Next     |
| ☐    | Timed practice (30-40 min per problem)                       | Next     |

## Progress targets (by topic, not by date)

| Done | Target                                                                     |
| ---- | -------------------------------------------------------------------------- |
| ☐    | 10-15 easy problems each on arrays/strings, hashmaps                       |
| ☐    | Two pointers, sliding window, binary search, stack: 8-10 each              |
| ☐    | Linked list, tree, heap, graph: 8-10 each                                  |
| ☐    | Backtracking and 1D DP: 6-8 each                                           |
| ☐    | Mix of easy and medium until you can solve most mediums with some thinking |
