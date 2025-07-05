# GITLite – Simplified Git-like Version Control System in C++

This project simulates a lightweight version control system similar to Git. It enables version tracking, branching, and data synchronization using advanced tree structures. The system was implemented in C++ and supports both **AVL Trees** and **Red-Black Trees**.


## 📁 File Structure
/GITLite
├── main.cpp # Entry point and command-line logic
├── avl.h # AVL Tree implementation
├── redblack.h # Red-Black Tree implementation
└── README.md # Project overview (this file)


## Main Concepts

- **Tree-Based File Storage**: Each CSV entry is stored in tree nodes. Nodes are written to separate files to simulate a distributed environment.
- **Merkle Tree Hashing**: Each node is hashed to enable data corruption detection and ensure integrity.
- **Command Interface**: Users can interact with the system using commands like `init`, `commit`, `branch`, and `checkout`.


## Features Implemented

### 📌 Repository Operations
- `init <filename>`  
  Initialize repository with AVL or Red-Black Tree. Loads CSV and stores data node-by-node in files.

- `commit "message"`  
  Saves current state with a message and generates a new version.

- `branch <branch_name>`  
  Creates a branch (stored as a folder) for independent work.

- `checkout <branch_name>`  
  Switches between existing branches.

- `log`  
  Shows commit history with timestamps and messages.

### Tree Operations
- Node addition, deletion, and updates
- Each change updates hashes for Merkle Tree consistency
- Tree stored partially in memory, mostly in files for efficiency

### Hashing
- Two methods:
  - **Instructor-defined Hash** (for int/string fields)
  - **SHA-256 Hash**

## 📦 Dataset Used

A real-world-style healthcare dataset in CSV format:
- Patient demographics
- Medical conditions
- Billing and insurance info
- Hospital stay and test results


