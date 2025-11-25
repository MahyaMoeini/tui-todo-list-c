
A terminal-based to-do list manager written in **C** using **ncurses**.  
This project was created as a university final project and focuses on clean C code, modular design, and an intuitive terminal user interface.

> 🎯 **Goal:** Build a fast, distraction-free task manager with priorities, categories, deadlines, subtasks, and persistent storage — all inside the terminal.

---

## 🖼 Pictures of terminal

<p align="center">
  <img src="https://github.com/user-attachments/assets/acf5537f-c423-42bc-bbd6-6a2c39edc84d" width="420" />
  <img src="https://github.com/user-attachments/assets/9ea649d0-1944-45b5-96d4-ddce784ca917" width="420" />
</p>




---

## 🔍 Overview
This application provides a **Text User Interface (TUI)** for managing tasks directly inside the terminal.

Each task supports:
- Title  
- Description / notes  
- Priority (1–9)  
- Multiple categories  
- Deadline (with date validation: `DD/MM/YYYY`)  
- Subtasks (with their own status)  
- Done / not-done state  

Panels include: Tasks, Subtasks, Categories, Deadline, Description.

---

## ✨ Features
- Full ncurses TUI  
- Keyboard-only navigation  
- Sorting by priority, deadline, alphabet  
- Multiple categories per task  
- Subtasks support  
- JSON saving/loading  
- Description editor  

---

## 🛠 Tech Stack
- C  
- ncurses  
- cJSON  
- Linux/WSL/macOS  

---

## 📁 Project Structure
```
tui-todo-list-c/
├── main.c
├── tasks.json
├── task_manager
├── README.md
└── assets/
    ├── main-view.png
    └── full-view.png
```

---

## ⚙️ Installation
```
git clone https://github.com/MahyaMoeini/tui-todo-list-c.git
cd tui-todo-list-c
sudo apt update
sudo apt install gcc libncurses5-dev libncursesw5-dev libcjson-dev
```

---

## 🧱 Build
```
gcc main.c -lncurses -lcjson -o task_manager
```

---

## ▶️ Run
```
./task_manager
```

---

## ⌨️ Keybindings
- j/k: move  
- a: add task  
- d: delete  
- e: edit  
- r: edit description  
- n: set deadline  
- SPACE: toggle done  
- c: category panel  
- l: subtask panel  
- h: back  
- s: sort  
- w: save  
- q: quit  

---

## 💾 Data Storage
JSON structure:
```
{
  "tasks": [
    {
      "title": "Task 1",
      "priority": 2,
      "deadline": "12/12/2025",
      "categories": ["cat1","cat2"],
      "subtasks":[{"title":"subtask1","done":true}],
      "description": "text...",
      "done": false
    }
  ]
}
```

---

## 🗺 Future Improvements
- Nested subtasks  
- Search/filter  
- Export formats  
- Mouse support  
- Unit tests  

---

## 📚 Learning Outcomes
- ncurses TUI
- Structs & pointers
- JSON parsing
- Persistent storage
- Linux workflow

---

## 👤 Author
**Mahya Moeini**  
GitHub: https://github.com/MahyaMoeini
