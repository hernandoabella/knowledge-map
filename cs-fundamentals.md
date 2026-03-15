# 🧩 CS Fundamentals

> What separates a programmer from an engineer. The foundation everything else assumes.

---

## 📚 Data Structures

| Structure | Best for | Complexity |
|-----------|---------|------------|
| **Array / List** | Index access, iteration | O(1) read, O(n) insert |
| **Hash Map** | Fast lookup by key | O(1) avg insert/lookup/delete |
| **Stack** | LIFO: call stack, undo, DFS, parsing | O(1) push/pop |
| **Queue** | FIFO: BFS, job scheduling, buffers | O(1) enqueue/dequeue |
| **Linked List** | Frequent insert/delete at known position | O(1) insert if pointer known |
| **BST / AVL** | Sorted data with O(log n) operations | O(log n) balanced |
| **Heap / Priority Queue** | Always-accessible min or max | O(1) peek, O(log n) insert |
| **Graph** | Relationships, networks, routing | Varies |
| **Trie** | Prefix matching, autocomplete | O(L) per key |
| **Union-Find** | Connected components, Kruskal's MST | Near O(1) amortized |
| **Segment Tree** | Range queries + point updates | O(log n) query/update |
| **Bloom Filter** | Probabilistic membership check — no false negatives | O(k) |

---

## ⚡ Algorithms

| Algorithm | Type | When to use |
|-----------|------|-------------|
| **Binary Search** | Search | Sorted array — O(log n) |
| **BFS** | Graph | Shortest path unweighted, level-order traversal |
| **DFS** | Graph | Cycle detection, topological sort, connected components |
| **Dijkstra** | Graph | Shortest path with non-negative weights |
| **Bellman-Ford** | Graph | Shortest path with negative weights |
| **A* Search** | Graph | Heuristic-guided pathfinding (game dev, navigation) |
| **Dynamic Programming** | Optimization | Overlapping subproblems + optimal substructure |
| **Greedy** | Optimization | Locally optimal choices yield global optimum |
| **Sliding Window** | Arrays/Strings | Subarray/substring problems in O(n) |
| **Two Pointers** | Arrays | In-place pair comparisons on sorted data |
| **Merge Sort** | Sorting | O(n log n) guaranteed, stable |
| **Quick Sort** | Sorting | O(n log n) avg, in-place, cache-friendly |
| **Topological Sort** | DAG | Order dependencies (build systems, course prereqs) |
| **Kruskal's / Prim's** | Graph | Minimum Spanning Tree |

---

## 📐 Time & Space Complexity

```
O(1)        → Constant      — hash map lookup, array index
O(log n)    → Logarithmic   — binary search, balanced BST
O(n)        → Linear        — single array scan, BFS/DFS
O(n log n)  → Linearithmic  — merge sort, Dijkstra (w/ heap)
O(n²)       → Quadratic     — nested loops (avoid in prod for large n)
O(n³)       → Cubic         — naive matrix multiplication
O(2ⁿ)       → Exponential   — subsets, brute force (use DP to optimize)
O(n!)       → Factorial     — permutations (TSP brute force)
```

> Space complexity: track auxiliary space (stack depth, memo tables, output size).
> Amortized analysis: average cost over a sequence of ops (e.g. dynamic array resizing).

---

## 🏗️ Programming Paradigms

| Paradigm | Core ideas |
|----------|-----------|
| **OOP** | Encapsulation, inheritance, polymorphism, abstraction |
| **Functional** | Pure functions, immutability, composition, higher-order functions |
| **Reactive** | Data streams, observables, backpressure (RxJS, Akka Streams) |
| **Concurrent** | Threads, goroutines, async/await, actor model, CSP channels |
| **Declarative** | Express what, not how — SQL, HTML, CSS, Prolog |
| **Procedural** | Step-by-step imperative instructions — C, early Python |

---

## 🔧 SOLID Principles

| Letter | Principle | What it means |
|--------|-----------|--------------|
| **S** | Single Responsibility | A class/module should have only one reason to change |
| **O** | Open/Closed | Open for extension, closed for modification |
| **L** | Liskov Substitution | Subtypes must be substitutable for their base types |
| **I** | Interface Segregation | Many specific interfaces > one general-purpose interface |
| **D** | Dependency Inversion | Depend on abstractions, not concretions |

---

## 🏛️ Design Patterns

### Creational — object creation mechanisms

| Pattern | What it does |
|---------|-------------|
| **Singleton** | One global instance — logger, config, DB connection pool |
| **Factory / Abstract Factory** | Create objects without specifying concrete class |
| **Builder** | Construct complex objects step by step — fluent interface |
| **Prototype** | Clone existing objects instead of creating new ones |

### Structural — class/object composition

| Pattern | What it does |
|---------|-------------|
| **Adapter** | Make incompatible interfaces work together |
| **Decorator** | Add behavior to objects dynamically without subclassing |
| **Facade** | Simplified interface to a complex subsystem |
| **Proxy** | Control access to another object |
| **Composite** | Treat individual and group objects uniformly |

### Behavioral — object communication

| Pattern | What it does |
|---------|-------------|
| **Observer** | Event subscriptions — notify dependents on state change |
| **Strategy** | Swap algorithms at runtime without changing client code |
| **Command** | Encapsulate requests as objects — undo/redo, queuing |
| **Iterator** | Sequential access to elements without exposing structure |
| **Template Method** | Define algorithm skeleton, let subclasses fill in steps |
| **Chain of Responsibility** | Pass request along a chain of handlers |

---

## 🗺️ Suggested Roadmap

```
Arrays + Hash Maps + Strings
    → Recursion + Stack / Queue
    → Trees + Graphs (BFS/DFS)
    → Dynamic Programming
    → SOLID + design patterns
    → System design (see system-design.md)
```
