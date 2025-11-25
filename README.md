# TUI To-Do List (C / ncurses)

A text-based task manager with a Terminal User Interface (TUI) written in **C** using **ncurses**.  
This project was originally developed as a university final project and focuses on clean C code, data structures, and terminal UI design.

## Features

- Full TUI layout with separate panels for:
  - Task list
  - Task description
  - Categories
  - Subtasks
  - Deadlines
- Priority for each task (1–9)
- Mark tasks as **done / not done**
- Add / edit / delete tasks
- Add **notes/description** for each task
- Add **multiple categories** per task
- Add **deadline** per task (with validation for `DD/MM/YYYY` format)
- **Sorting** tasks by:
  - Priority
  - Nearest deadline
  - Alphabetical order
- Simple **subtasks** support (add / delete / toggle done)
- **Save & load** all tasks to/from a JSON file
- Keyboard-driven control (no mouse needed)

## Tech Stack

- **Language:** C
- **Library:** ncurses
- **Data format:** JSON (for persistence)

## Project Structure

```text
tui-todo-list-c/
├─ main.c        # main source file with TUI and logic
├─ tasks.json    # sample saved tasks (optional)
├─ README.md
└─ .gitignore
