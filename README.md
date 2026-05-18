# PokéBST: Advanced Data Structures in C 

Welcome to **PokéBST** (formerly Pokedex Manager 3000), a robust, console-based Pokémon management system written entirely in C. 

This project simulates a Pokémon ecosystem where trainers (Owners) can catch Pokémon, engage in battles, evolve their roster, and even merge collections. Under the hood, the system is a rigorous exercise in memory management and complex data structures, utilizing **Binary Search Trees (BST)** and **Circular Linked Lists**.

## Technical Architecture

This project was built to practice deep algorithmic concepts and manual memory management:
* **Circular Linked List:** Used to manage the Pokémon trainers. This allows seamless, infinite navigation between owners without boundary limits.
* **Binary Search Tree (BST):** Each trainer's Pokédex is implemented as a BST. This ensures efficient insertion, searching, and traversal of Pokémon based on their IDs.
* **Breadth-First Search (BFS):** Utilized during the merging of two Pokédexes to copy the tree structures efficiently.
* **Memory Safety:** Strictly tested with `valgrind` to ensure zero memory leaks, even during complex tree-merging and node deletion operations.

## Core Features

* **Trainer Management:** Create new owners and navigate through them in a continuous circular loop.
* **Pokédex Expansion:** Insert new Pokémon into a trainer's BST, dynamically allocating memory and maintaining tree balance.
* **Battle System:** Let your creatures brawl! Battles are calculated using a custom algorithm: `Score = (1.5 × Attack) + (1.2 × HP)`.
* **Evolutions:** Evolve your Pokémon effortlessly. The system upgrades the Pokémon to `ID + 1` while maintaining the integrity of the BST.
* **Pokédex Merging:** Combine two trainers into one. The system uses a BFS algorithm to merge the BSTs, transferring all Pokémon to the victor while cleanly deleting and freeing the memory of the defeated trainer.

## Getting Started

### Prerequisites
* GCC Compiler
* Valgrind (for memory leak testing)

### Compilation
Compile the project with strict warning flags to ensure code quality:
```bash
gcc -Wall -Wextra -Werror -g -std=c99 ex6.c -o ex6
Execution
Run the program. It is highly recommended to run it through Valgrind to monitor memory usage:

Bash
valgrind --leak-check=full ./ex6 < input.txt
(Follow the interactive console prompts to create trainers, add Pokémon, and battle).

## Important Notes
Input Handling: The system robustly handles CRLF (\r\n) issues and trims trailing characters for cross-OS compatibility.

Disclaimer: No real Pokémon were harmed in the making of this BST. Please do not feed your Bulbasaur after midnight.

Author: Alon Cohen
Software Engineering, Bar-Ilan University
