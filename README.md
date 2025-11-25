# TUI To-Do List (C / ncurses)

A terminal-based to-do list manager written in **C** using **ncurses**.  
This project was created as a university final project and focuses on clean C code, modular design, and an intuitive terminal user interface.

> 🎯 **Goal:** Build a fast, distraction-free task manager with priorities, categories, deadlines, subtasks, and persistent storage — all inside the terminal.

---


### Full TUI Example (with tasks, categories, subtasks)
![Full View](assets/full-view.png)

### Empty State / Initial UI
![Main View](assets/main-view.png)

---

## 🔍 Overview

This application provides a **Text User Interface (TUI)** for managing tasks directly inside the terminal.

Each task supports:

- Title  
- Description / notes  
- Priority (1–9)  
- Multiple categories  
- Deadline (with date validation: DD/MM/YYYY)  
- Subtasks (with their own status)  
- Done / not-done state  

The layout includes separate panels for:

- **Tasks**
- **Subtasks**
- **Categories**
- **Deadline**
- **Description**

All data is stored in a JSON file and loaded automatically on startup.

---

## ✨ Features

- 🖥 **Full TUI layout** using ncurses  
- ⌨️ **Keyboard-only navigation** (Vim-inspired keys)  
- 🔢 Task priority and sorting  
- 📂 Multiple categories per task  
- 📅 Deadlines with validation  
- 🧩 Subtasks (add, delete, toggle)  
- 📝 Description editor  
- 💾 JSON-based save/load system  
- 📊 Sorting options:
  - By priority  
  - By deadline  
  - Alphabetically  

---

## 🛠 Tech Stack

- **Language:** C  
- **UI Library:** ncurses  
- **Data Storage:** JSON (cJSON)  
- **Platform:** Linux / macOS / Windows (via WSL)  

---

## 📁 Project Structure

```text
tui-todo-list-c/
│
├── main.c
├── tasks.json
├── task_manager
├── README.md
└── assets/
    ├── main-view.png
    └── full-view.png


⚙️ Installation

1. Clone the repository
git clone https://github.com/MahyaMoeini/tui-todo-list-c.git
cd tui-todo-list-c

2. Install dependencies (Ubuntu / WSL)
sudo apt update
sudo apt install gcc libncurses5-dev libncursesw5-dev libcjson-dev

🧱 Build

Compile the project:

gcc main.c -lncurses -lcjson -o task_manager


If your main file’s name differs, adjust the command accordingly.

▶️ Run
./task_manager

⌨️ Keybindings
Key	Action
j	Move down
k	Move up
a	Add new task
d	Delete task
e	Edit task name
r	Edit description
n	Set deadline
SPACE	Toggle status (done / not done)
c	Category panel
l	Subtask panel
h	Back to main task panel
s	Sort tasks
w	Save to file
q	Quit application


💾 Data Storage

Tasks are stored in a JSON file with the structure:

{
  "tasks": [
    {
      "title": "Task 1",
      "priority": 2,
      "deadline": "12/12/2025",
      "categories": ["cat1", "cat2"],
      "subtasks": [
        { "title": "subtask1", "done": true }
      ],
      "description": "text here...",
      "done": false
    }
  ]
}

🗺 Future Improvements

Nested subtasks (multi-level hierarchy)

Search and filter (by priority, category, deadline)

Export tasks to Markdown / JSON / PDF

Mouse support

Unit tests and modularization

📚 Learning Outcomes

This project demonstrates:

Building TUIs with ncurses

Using structs, dynamic arrays, and pointers in C

Parsing and generating JSON with cJSON

Managing complex UI state

Saving/loading persistent data

Linux/WSL development workflow

👤 Author

Your Name
GitHub: @https://github.com/MahyaMoeini
