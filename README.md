# 🚨 RouteGuard — Dynamic Emergency Route Planner

<p align="center">
  <img src="https://img.shields.io/badge/Language-C%2B%2B-blue?style=for-the-badge&logo=cplusplus" />
  <img src="https://img.shields.io/badge/GUI-Qt-green?style=for-the-badge&logo=qt" />
  <img src="https://img.shields.io/badge/Algorithm-Dijkstra%20%7C%20A*-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />
</p>

> A real-time route optimization system for emergency vehicles that dynamically recalculates the fastest path under changing road conditions using Dijkstra's and A\* algorithms.

---

## 📌 Overview

RouteGuard is a high-performance C++ application that computes optimal routes for emergency vehicles (ambulances, fire trucks, police) in real time. As road conditions change — due to accidents, traffic congestion, or blockages — the system instantly recalculates the best available path, ensuring minimal response time.

---

## ✨ Features

- ⚡ **Real-time shortest path** using Dijkstra's and A\* algorithms with priority queues
- 🔄 **Dynamic graph updates** — handles live road blocks and congestion without full re-computation
- 🚦 **Traffic-aware edge weights** — models congestion as variable costs to prefer clear corridors
- 🗺️ **Alternative path suggestions** when the primary route is blocked
- 🖥️ **Interactive Qt dashboard** — visualizes routes, travel times, and path comparisons

---

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| Language | C++17 |
| GUI Framework | Qt 6 |
| Algorithms | Dijkstra, A\*, Priority Queue |
| Data Structures | Adjacency List Graph, Min-Heap |
| Build System | CMake |

---

## 🚀 Getting Started

### Prerequisites

```bash
# Install Qt6 and CMake
sudo apt install qt6-base-dev cmake g++
```

### Build & Run

```bash
git clone https://github.com/priyanshu-bhardwaj/RouteGuard.git
cd RouteGuard
mkdir build && cd build
cmake ..
make
./RouteGuard
```

---

## 📁 Project Structure

```
RouteGuard/
├── src/
│   ├── main.cpp
│   ├── graph.cpp / graph.h        # Graph model + edge weights
│   ├── dijkstra.cpp / dijkstra.h  # Dijkstra's algorithm
│   ├── astar.cpp / astar.h        # A* algorithm
│   └── dashboard.cpp / dashboard.h # Qt GUI
├── assets/
├── CMakeLists.txt
└── README.md
```

---

## 🧠 Algorithm Details

### Dijkstra's Algorithm
Used for exact shortest-path computation on graphs with non-negative edge weights. Runs in **O((V + E) log V)** with a min-heap.

### A\* Algorithm
Extends Dijkstra with a heuristic (Euclidean/Manhattan distance) to guide search toward the destination faster, ideal for geographic road networks.

### Dynamic Re-routing
When a road is blocked or congestion increases, affected edge weights are updated and only the impacted sub-graph is re-processed — avoiding a full recomputation.

---

## 📸 Screenshots

> *(Add screenshots of the Qt dashboard here)*

---

## 👤 Author

**Priyanshu Bhardwaj**
B.Tech Mechanical Engineering — IIT Guwahati
📧 p.bhardwaj@iitg.ac.in | bhardwajpriyanshu2102@gmail.com
🔗 [LinkedIn](https://linkedin.com/in/priyanshu-bhardwaj-4bb652213)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
