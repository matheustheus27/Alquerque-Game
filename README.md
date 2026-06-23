# Alquerque — Classic Board Game Simulation 🎲🤖

An interactive desktop simulation of the ancient strategy board game **Alquerque** (originally known in Arabic as *El-Quirkat*), the historical predecessor to modern Checkers/Draughts. This application was engineered as a practical software evaluation for the **Programming Languages Laboratory (LLP)** course in the Computer Engineering curriculum at CEFET-MG.

---

## 👥 Authorship & Faculty

* **Professor:** Dr. Andrei Rimsa Álvares
* **Student:** Matheus Thiago de Souza Ferreira

---

## 🛠️ Software Architecture & Qt Directory Layout

The game loop and reactive visual state machine are engineered utilizing the event-driven native desktop framework **Qt (C++)**.

```text
├── Assets/              # Graphical runtime elements (Sprites, textures, buttons)
├── Alquerque.cpp        # Implementation: Main game loop, board state matrix rules
├── Alquerque.h          # Header: Main application blueprints & structural macros
├── Alquerque.pro        # Qt Project compilation configuration metadata
├── Alquerque.qrc        # Qt Resource compilation script (Assets virtual binding)
├── Alquerque.ui         # XML layout descriptor for the Qt User Interface window
├── Hole.cpp             # Implementation: Dynamic board slot cell states and captures
├── Hole.h               # Header: State descriptors for individual coordinate cells
├── main.cpp             # System bootstrap entry point initialization
└── .gitignore
```

## Core Architecture Breakdown:
* Dynamic Board Cells (`Hole.cpp` / `Hole.h`): Encapsulates individual cell coordinate states (empty, occupied by Player 1, or occupied by Player 2), tracking valid vector step arrays for movement validation.
* Game Engine Window (`Alquerque.cpp` / `Alquerque.h`): Tracks current turns, capture requirements, victory conditions, and translates UI mouse clicks into valid matrix coordinates.
* Qt Resource System (`Alquerque.qrc`): Packs the graphic sheets from the `Assets/` directory into the binary footprint, ensuring seamless portability of runtime textures.

## 🚀 Compilation & Running Guide
1. Prerequisites
Ensure you have a configured C++ toolchain and the Qt SDK / Qt Creator IDE configured on your local operating system.

2. Loading the Environment
Open your project inside Qt Creator by choosing to import an existing project and selecting the underlying setup configuration template file:
```bash
Alquerque.pro
```

3. Build & Run Pipelines
* Step 3.1: Execute a qmake task routine via the IDE interface to map the build directories and source pointers.
* Step 3.2: Trigger the Build option (`Ctrl + B`) to compile the underlying UI header descriptors (`ui_Alquerque.h`) and asset binaries.
* Step 3.3: Run the native desktop application (`Ctrl + R`).

## 🔧 Core Tech Stack
* Language Platform: C++ (ISO Standard)
* GUI Engine Library: Qt Widgets Module
* Build System Automation: qmake pipeline configuration
