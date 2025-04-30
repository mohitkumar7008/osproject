Mark-and-Sweep Garbage Collector (C Implementation)
📦 Project Overview
This project implements a Mark-and-Sweep Garbage Collection (GC) algorithm in the C programming language. It simulates memory management in an operating system by automatically identifying and reclaiming unused memory. The program demonstrates how garbage collection can be manually handled in languages like C, which do not have built-in memory management.

🧠 Key Features
Simulates dynamic memory allocation with a custom memory heap.

Implements the classic two-phase mark-and-sweep algorithm:

Mark Phase: Identifies all reachable (in-use) memory blocks.

Sweep Phase: Frees all unreachable memory blocks.

Command-line interface for:

Allocating objects

Setting root references

Running garbage collection

Viewing heap state

🛠️ How It Works
Allocation: Objects are allocated dynamically using a custom allocator (gc_alloc()).

Root Management: Objects can be registered as roots to simulate references from active parts of a program.

Mark Phase: Starting from roots, the GC traverses all reachable objects recursively and marks them.

Sweep Phase: Unmarked objects are considered garbage and are deallocated.

Memory Visualization: The heap and its state can be printed to observe the GC process.

🚀 Getting Started
Prerequisites
A C compiler (e.g., gcc)

Linux/macOS/Windows (any platform that supports C)

Compilation
bash
Copy
Edit
gcc -o mark_sweep_gc main.c gc.c
Running
bash
Copy
Edit
./mark_sweep_gc
Use the interactive command-line menu to allocate objects, set roots, and run GC.

📁 File Structure
bash
Copy
Edit
.
├── gc.h             # Header file defining object and GC structure
├── gc.c             # Implementation of mark and sweep logic
├── main.c           # CLI interface to interact with GC
└── README.md        # Project documentation
📋 Sample Commands
Allocate Objects
Allocate objects with optional links to simulate references.

Set Roots
Define which objects are considered as root nodes.

Run Garbage Collection
Execute the GC algorithm to clean up unreferenced objects.

Print Heap State
View all objects, their links, and their marked/unmarked status.

🧪 Example Output
css
Copy
Edit
Allocated object A
Allocated object B linked to A
Set A as root
Running GC...
Marked A
Marked B
GC complete. 0 objects freed.
📚 Concepts Demonstrated
Manual memory management

Garbage collection algorithms

Graph traversal (DFS for marking phase)

Simulated heap structures

📌 Limitations
Does not handle cyclic references unless linked properly.

Only simulates heap and object references (not real C pointers).

Educational purpose — not production-ready.

🤝 Contributions
Pull requests are welcome! If you have ideas to extend the GC (like generational GC, compaction, or reference counting), feel free to contribute.
